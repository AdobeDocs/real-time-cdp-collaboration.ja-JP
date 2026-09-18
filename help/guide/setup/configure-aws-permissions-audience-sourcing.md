---
title: オーディエンスソーシング用のAWS権限の設定
description: AWS Identity and Access Management （IAM）権限を設定して、Real-Time CDP Collaborationでオーディエンスソーシング用の[!DNL Amazon S3] バケットにAdobeの安全で読み取り専用のアクセス権を付与する方法を説明します。
exl-id: a48b800f-4bb3-4be6-af8e-b42a65a25c5b
source-git-commit: f0e260d9bf15a0230940c967e6d73e7431625358
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 1%
---
# オーディエンスソーシングのAWS権限の設定

このガイドでは、AWS Identity and Access Management （IAM）のポリシーとロールを設定し、AdobeにAmazon S3 バケットへの安全な読み取り専用アクセス権を付与する方法を説明します。 このアクセスにより、Real-Time CDP CollaborationはS3 バケットからオーディエンスをソースできます。

## 前提条件 {#prerequisites}

続行する前に、次の要件を満たし、必要な情報にアクセスできることを確認してください。

### 必要なAWS権限

この設定を完了するには、アカウントにAWS管理者アクセス権が必要です。 管理者アクセスにより、AdobeのS3 バケットへのアクセスを承認するために必要なIAM ポリシーとロールを作成および管理できるようになります。 管理者権限がない場合は、続行する前にAWS管理者に連絡してください。

### 必要な情報

次の手順を実行する際は、次の情報に注意してください。 これらの詳細は、[[!DNL Amazon S3]  オーディエンスのソーシング UI ガイド &#x200B;](./configure-aws-s3-audience-sourcing.md)で使用されています。

* オーディエンスファイルが保存されるS3 バケット名。
* オーディエンスファイルが配置されているフォルダーのパス（プレフィックス）。
* 新しく作成したIAM ロールのAmazon リソース名（ARN）（例：`arn:aws:s3:::my-company-data/audience-files/`）

>[!TIP]
>
>Amazon リソース名（ARN）は、S3 バケットやIAM ロールなどのAWS リソースを一意に識別します。 バケットとオプションのフォルダーパスを指定するには、次の形式を使用します。
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## IAM ポリシーの作成 {#create-policy}

セットアップを開始するには、まず、S3 バケットに&#x200B;**読み取り専用アクセス**&#x200B;を付与するIAM ポリシーを作成します。 このポリシーにより、Adobeはオーディエンスのソーシングに必要なファイルを読み取ることができますが、書き込み権限や削除権限は付与されません。

[AWS Management Console](https://aws.amazon.com/console/)を開き、**[!DNL IAM]** > **[!DNL Policies]** > **[!DNL Create policy]**&#x200B;に移動します。

AWS Create policy ワークスペースで、「**JSON**」タブを選択し、次のポリシー例を貼り付けます。

>[!NOTE]
>
>`<Your AWS ARN for bucket folder path>`と`<Your AWS ARN for bucket>`を特定のS3 ARNに置き換えます。 バケット フォルダーのパスを指定する場合は、ARNの末尾に`/*`を含めます（例：`arn:aws:s3:::my-company-data/audience-files/*`）。 これにより、Adobeは、指定したフォルダーパス内のすべてのファイルとサブフォルダーにアクセスできるようになります。

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket",
        "s3:GetBucketLocation"
      ],
      "Resource": "<Your AWS ARN for bucket folder path>"
    },
    {
      "Sid": "Statement2",
      "Effect": "Allow",
      "Action": [
        "s3:ListBucket"
      ],
      "Resource": "<Your AWS ARN for bucket>"
    }
  ]
}
```

ポリシー設定を確認し、**[!DNL Create policy]**&#x200B;を選択します。 後の手順で使用するポリシー名を記録します。

>[!TIP]
>
>バケット名とフォルダーパスを見つけるには、**Amazon S3 Management Console**&#x200B;を開きます。 **バケット** ページで、バケット名を選択して開きます。 **オブジェクト** ビューにはファイルとフォルダーが一覧表示され、ページ上部のパスには現在のフォルダーのパスが表示されます。

## IAM ロールの作成 {#create-role}

次に、IAM ロールを作成し、Real-Time CDP Collaboration AWS IAM ロールを&#x200B;**信頼済みエンティティ**&#x200B;として設定します。 これにより、AdobeのサービスがS3 オーディエンスデータを安全に読み取ることができます。

Amazon S3 Management Consoleの「**[!DNL IAM]**」タブで、**[!DNL Roles]** > **[!DNL Create role]**&#x200B;に移動します。

[!DNL Create role] ワークフローの[!DNL Step 1]で、**[!DNL Trusted entity type]** セクションで「**[!DNL Custom trust policy]**」を選択します。 次に、**[!DNL Custom trust policy]** エディターで、次の例を貼り付け、`<Adobe IAM Role ARN>`を地域の値に置き換えます。

* お住まいの地域に適したAdobe IAM ロール ARN:

| 領域 | Adobe IAM Role ARN |
|---------|-------------------|
| 北米 | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| オーストラリア | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |
| EMEA | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-deu1-role` |

信頼ポリシーの例：

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": {
        "AWS": "<Adobe IAM Role ARN>"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

ポリシーを確認し、**次へ**&#x200B;を選択して続行します。

[!DNL Create role] ワークフローの[!DNL Step 2] **[!DNL Add permissions]** セクションで、[以前](#create-policy)に作成したIAM ポリシーを検索して添付します。 ポリシーの後に&#x200B;**[!DNL Next]**&#x200B;を選択して、[!DNL Step 3]に続行します。

[!DNL Step 3] **[!DNL Name review, and create - Role details]** セクションで、役割の名前（例：`s3-iam-role`）とオプションの説明を入力します。

このページには、信頼できるエンティティ ポリシー、権限ポリシーの概要、内部組織とトラッキング用に追加した可能性のあるタグが表示されます。

最後に、**役割を作成**&#x200B;を選択して、設定を確認します。

>[!IMPORTANT]
>
>ロールを作成した後、Amazon リソース名（ARN）を記録する必要があります。 [&#x200B; オーディエンスソーシング用にAWS S3を設定](./configure-aws-s3-audience-sourcing.md) ワークフローの&#x200B;**S3接続の認証**&#x200B;手順で、IAM ロール ARNを指定する必要があります。

## 次の手順 {#next-steps}

この設定により、AdobeにS3 バケットへの読み取り専用アクセス権が付与され、AdobeのIAM ロールとの信頼関係が確立されます。

次に、[&#x200B; オーディエンスソーシング用にAWS S3を設定](./configure-aws-s3-audience-sourcing.md)に進み、S3 バケットをCollaborationに接続します。

オーディエンスのソーシングについて詳しくは、[Sourceとオーディエンスの管理](./onboard-audiences.md)を参照してください。
