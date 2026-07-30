---
title: 宛先の接続要件
description: Real-Time CDP Collaborationでサポートされる宛先を設定するために必要な接続情報を確認します。
audience: admin, publisher
source-git-commit: c84582bb81289ce761c664af7db177535ff00a00
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%

---

# 宛先の接続要件

Real-Time CDP Collaborationで宛先を設定する前に、宛先プロバイダーが必要とする資格情報と接続情報を取得します。

ここでは、Collaborationで使用可能な認証方法の概要を説明します。 資格情報の作成、権限の割り当て、ネットワークアクセスの設定、宛先システムの準備について詳しくは、リンクされたAdobe Experience Platformの宛先に関するドキュメントを参照してください。

>[!NOTE]
>
>リンクされたAdobe Experience Platformのドキュメントには、標準の宛先ワークフローが記載されています。 Real-Time CDP Collaborationで宛先を設定する際に、一部の手順、フィールド、またはオプションが適用されない場合があります。

## 一目で確認できる要件 {#requirements-at-a-glance}

| 宛先 | 認証または接続方法 | 始める前に準備する | 詳細な要件 |
|---|---|---|---|
| [!DNL Amazon S3] | アクセスキーと秘密鍵、または想定される役割 | AWS アクセスキーのペアまたはIAM ロール ARN、バケットおよびフォルダーの情報 | [[!DNL Amazon S3] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3) |
| SFTP | パスワードまたはSSH キー | サーバードメイン、ポート、ユーザー名、認証資格情報、フォルダーパス | [SFTP宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp) |
| [!DNL Azure Blob Storage] | 接続文字列 | Azure storageの接続文字列、コンテナ、フォルダーの情報 | [[!DNL Azure Blob Storage] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob) |
| [!DNL Google Cloud Storage] | アクセスキーIDとシークレットアクセスキー | [!DNL Google Cloud Storage]相互運用性の資格情報、バケット、およびフォルダー情報 | [[!DNL Google Cloud Storage] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage) |
| [!DNL Snowflake Batch] | [!DNL Snowflake] データ共有 | [!DNL Snowflake] アカウント ID、地域、プライベートリンクのステータス、およびプライベートリストへのアクセス | [[!DNL Snowflake Batch] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch) |
| [!DNL Data Landing Zone] | 別途認証は必要ありません | 保存先フォルダーのパスとファイル出力の環境設定 | [[!DNL Data Landing Zone] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone) |

## コネクターのメモ {#connector-notes}

宛先を設定する前に、次のコネクタ固有の認証方法とワークフローの違いを確認します。

### [!DNL Amazon S3] {#amazon-s3}

Collaborationでは、**[!UICONTROL アクセスキー]**&#x200B;および&#x200B;**[!UICONTROL 想定される役割]**&#x200B;の認証がサポートされています。 アクセスキー認証には、アクセスキーとシークレットアクセスキーが必要です。 ロールの想定による認証には、Adobeが引き受けることができるAWS IAM ロールのARNが必要です。

資格情報、役割、権限の設定については、[宛先 [!DNL Amazon S3] への認証](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#authenticate)を参照してください。

### SFTP {#sftp}

Collaborationでは、**[!UICONTROL SFTP （パスワード]**&#x200B;付き）と&#x200B;**[!UICONTROL SFTP （SSH キー]**&#x200B;付き）の認証がサポートされています。 どちらの方法でも、サーバードメイン、ポート、ユーザー名が必要です。 ポートのデフォルト値は`22`です。

SSH キー形式、サーバー、ネットワーク、およびネットワークの要件については、[SFTP認証の情報](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/sftp#authentication-information)を参照してください。

### [!DNL Azure Blob Storage] {#azure-blob-storage}

Collaborationは、ストレージアカウントの接続文字列を使用して[!DNL Azure Blob Storage]を認証します。

接続文字列を取得し、ストレージ権限を割り当てる方法については、[宛先 [!DNL Azure Blob Storage] への認証](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob#authenticate)を参照してください。

### [!DNL Google Cloud Storage] {#google-cloud-storage}

Collaborationには、[!DNL Google Cloud Storage]の相互運用性の設定を通じて生成された[!DNL Google Cloud Storage] アクセス キーIDとシークレット アクセス キーが必要です。

資格情報の生成とバケット権限の要件については、[宛先 [!DNL Google Cloud Storage] への認証](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage#authenticate)を参照してください。

### [!DNL Snowflake Batch] {#snowflake-batch}

[!DNL Snowflake Batch]は、ファイルを顧客管理ストレージに書き出す代わりに、[!DNL Snowflake] データ共有を使用します。 Collaborationでは、個別の認証手順はありません。 宛先の作成時に、Snowflake アカウント ID、リージョン、プライベートリンクのステータス、アカウントの所有権の確認を入力します。

アカウントの準備とプライベートリストの要件については、[[!DNL Snowflake Batch] 宛先ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/warehouse/snowflake-batch)を参照してください。

### [!DNL Data Landing Zone] {#data-landing-zone}

[!DNL Data Landing Zone]はAdobeによってプロビジョニングされており、Collaborationで個別の認証手順を必要としません。 宛先作成時に、宛先フォルダーのパスとファイル出力設定を指定します。

AWSでプロビジョニングされた[!DNL Data Landing Zone]へのアクセスについて詳しくは、[AWSでプロビジョニングされたデータランディングゾーンへの認証](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone#authenticate-dlz-aws)を参照してください。

## 次の手順 {#next-steps}

必要な接続情報を取得したら、[宛先を設定して管理します](./manage-destinations.md)。
