---
title: オーディエンスソーシングのAWS権限の設定
description: Real-Time CDP Collaborationでのオーディエンスソーシング用に、AWSの安全な読み取り専用アクセス権をAdobeに付与するための、Identity and Access Management （IAM）権限の  [!DNL Amazon S3]  定方法について説明します。
source-git-commit: 4f223890dabb4897c9e9264655ff9217e323dc91
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# オーディエンスソーシングのAWS権限の設定

このガイドを使用して、Amazon S3 バケットにAWSの安全な読み取り専用アクセスを付与するAdobe Identity and Access Management （IAM）ポリシーとロールを設定します。 このアクセス権により、Real-Time CDP Collaborationは S3 バケットからオーディエンスをソース化できます。

## 前提条件 {#prerequisites}

続行する前に、次の要件を満たしており、必要な情報にアクセスできることを確認してください。

### 必要なAWS権限

この設定を行うには、お使いのアカウントにAWS管理者アクセス権が必要です。 管理者アクセス権により、Adobeの S3 バケットへのアクセスの認証に必要な IAM ポリシーとロールを作成および管理できるようになります。 管理者権限がない場合は、先に進む前にAWS管理者にお問い合わせください。

### 必要な情報

以下の手順を実行する際は、次の情報に注意してください。 これらの詳細は、[[!DNL Amazon S3]  オーディエンスソーシング UI ガイド ](./configure-aws-s3-audience-sourcing.md) で使用されます。

* オーディエンスファイルが格納される S3 バケット名。
* オーディエンスファイルがあるフォルダーパス（接頭辞）。
* 新しく作成した IAM ロールのAmazon リソース名（ARN） （例：`arn:aws:s3:::my-company-data/audience-files/`）

>[!TIP]
>
>Amazon リソース名（ARN）は、S3 バケットや IAM ロールなどのAWS リソースを一意に識別します。 バケットとオプションのフォルダーパスを指定するには、次の形式を使用します。
>
>```
>arn:aws:s3:::<bucket-name>/<optional-folder-path>
>```

## IAM ポリシーの作成 {#create-policy}

設定を開始するには、まず、S3 バケットに **読み取り専用アクセス** を許可する IAM ポリシーを作成します。 このポリシーを設定すると、Adobeはオーディエンスソーシングに必要なファイルを読み取ることができますが、書き込みまたは削除の権限は付与されません。

[AWS Management Console](https://aws.amazon.com/console/) を開き、**[!DNL IAM]**/**[!DNL Policies]**/**[!DNL Create policy]** に移動します。

AWSのポリシーを作成ワークスペースで、「**JSON**」タブを選択し、次のサンプルポリシーを貼り付けます。

>[!NOTE]
>
>`<Your AWS ARN for bucket folder path>` と `<Your AWS ARN for bucket>` を特定の S3 ARN に置き換えます。 バケットのフォルダーパスを指定する場合は、ARN の末尾に `/*` を含めます（例：`arn:aws:s3:::my-company-data/audience-files/*`）。 これにより、Adobeが指定されたフォルダーパス内のすべてのファイルとサブフォルダーにアクセスできるようになります。

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

ポリシー設定を確認し、「**[!DNL Create policy]**」を選択します。 後の手順で使用するために、ポリシー名を記録します。

>[!TIP]
>
>バケット名およびフォルダーパスを特定するには、**Amazon S3 Management Console** を開きます。 **バケット** ページで、バケット名を選択して開きます。 **オブジェクト** ビューにはファイルとフォルダーが一覧表示され、ページ上部のパスには現在のフォルダーパスが表示されます。

## IAM 役割の作成 {#create-role}

次に、IAM 役割を作成し、Real-Time CDP Collaboration AWS IAM 役割を **trusted entity** として設定します。 これにより、Adobeのサービスが役割を引き受け、S3 オーディエンスデータを安全に読み取ることができます。

Amazon S3 Management Console の「**[!DNL IAM]**」タブで、**[!DNL Roles]**/**[!DNL Create role]** に移動します。

[!DNL Step 1] ワークフローの [!DNL Create role] で、「**[!DNL Trusted entity type]**」セクションの「**[!DNL Custom trust policy]**」を選択します。 次に、**[!DNL Custom trust policy]** エディターで、次の例を貼り付け、`<Adobe IAM Role ARN>` を実際の地域の値に置き換えます。

* お住まいの地域に適したAdobe IAM 役割 ARN:

| 領域 | Adobe IAM ロール ARN |
|---------|-------------------|
| 北米 | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-va6-role` |
| オーストラリア | `arn:aws:iam::590183896800:role/rtcdp-collab-prod-aus3-role` |

信頼ポリシーの例は次のとおりです。

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

ポリシーを確認し、「**次へ**」を選択して続行します。

[!DNL Step 2] ワークフロー **[!DNL Add permissions]**[!DNL Create role] セクションで、作成した IAM ポリシーを検索して添付します [ 前 ](#create-policy)。 ポリシーを選択し、続けて **[!DNL Next]** を選択して [!DNL Step 3] きます。

「[!DNL Step 3] **[!DNL Name review, and create - Role details]**」セクションで、役割名（例：`s3-iam-role`）と説明（オプション）を入力します。

このページには、信頼済みエンティティポリシー、権限ポリシーの概要、内部組織およびトラッキング用に追加したタグが表示されます。

最後に、「**役割を作成**」を選択して、設定を確定します。

>[!IMPORTANT]
>
>ロールの作成後に、Amazon リソース名（ARN）を記録する必要があります。 **オーディエンスソーシング用のAWS S3 の設定** ワークフローの [S3 接続の認証 ](./configure-aws-s3-audience-sourcing.md) 手順で、IAM 役割 ARN を指定する必要があります。

## 次の手順 {#next-steps}

この設定により、Adobeに S3 バケットへの読み取り専用アクセスが許可され、Adobeの IAM ロールとの信頼済み接続が確立されます。

次に、[ オーディエンスソーシング用のAWS S3 の設定 ](./configure-aws-s3-audience-sourcing.md) に進んで、S3 バケットをCollaborationに接続します。

オーディエンスのソーシングについて詳しくは、[Sourceとオーディエンスの管理 ](./onboard-audiences.md) を参照してください。
