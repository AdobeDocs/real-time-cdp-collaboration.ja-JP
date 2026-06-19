---
title: ソースの概要
description: Adobe Real-Time CDP Collaborationのソースコネクタについて説明します
audience: admin, publisher, advertiser
source-git-commit: b30d1b01e929e586404faac34650c7fd479d071b
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 6%

---

# ソースの概要

Adobe Real-Time CDP Collaborationでは、オーディエンスデータの出所はソース（データ接続）となります。 Adobe アプリケーション、クラウドベースのストレージ、ローカルシステムのファイルなど、様々なソースタイプに接続して、Collaboration プロジェクトのオーディエンスを[&#x200B; ソースおよび管理](./onboard-audiences.md)できます。 オーディエンスのソーシングワークフローでは、組織のニーズにもとづいて好みのソースを選択し、設定できます。

## ソースを接続 {#connect-a-source}

ソースを接続するには、ソーシングワークフローを入力する必要があります。 まず、**[!UICONTROL 設定]** ワークスペース内の&#x200B;**[!UICONTROL マイオーディエンス]** タブに移動します。

追加アイコン（![追加アイコン。](/help/assets/icons/plus.png)）を選択します 次に、**[!UICONTROL Audience]**&#x200B;を選択して、ソーシングワークフローを開始します。

![追加オプションとオーディエンスオプションがハイライト表示された自分のオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/add-audiences.png)

ワークフロー中に、ソースを選択して新しいデータ接続を追加するように求められます。 選択するソースによって、オーディエンスデータをCollaborationに取り込む方法が決まります。 サポートされているすべてのソースの一覧については、[使用可能なソース &#x200B;](#available-sources)の表を参照してください。

![新しいデータ接続を追加オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-data-connection.png)

ソースを選択した後、ワークフローは、認証、フィールドマッピング、スケジューリング、オーディエンスの選択など、接続固有の設定手順をガイドします。

### 利用可能なソース {#available-sources}

Collaborationでは、次のソースを使用できます。 そのソースのステップバイステップのソーシングガイドを表示するには、以下の表でソース名を選択します。 現在利用できないソースに興味がある場合は、Adobe担当者にお問い合わせください。

| ソース | 説明 | 対象 |
| --- | --- | --- |
| [Adobe Experience Platform](./onboard-audiences.md) | 接続しているExperience Platformインスタンスからオーディエンスを取り込み、既存の顧客セグメントを再利用できます。 | 使用可能 |
| [Amazon S3](./configure-aws-s3-audience-sourcing.md) | S3 バケットを接続して、クラウドインフラストラクチャから大規模なファーストパーティデータセットを取得します。 | 使用可能 |
| [[!DNL Snowflake]](./configure-snowflake-audience-sourcing.md) | [!DNL Snowflake Secure Data Share]を接続して、大規模なオーディエンスデータセットを取り込みます。 | 使用可能 |
| [[!DNL Google Cloud Storage]](./configure-gcs-audience-sourcing.md) | GCS バケットを接続して、[!DNL Google Cloud]環境に保存されているオーディエンスデータを取り込みます。 | 使用可能 |
| [CSV ファイルのアップロード &#x200B;](./upload-csv-audience-sourcing.md) | フォーマットされたCSV ファイルをローカルシステムから直接アップロードします。 | 使用可能 |
| Adobe Audience Manager | 既存のAudience Manager セグメントをCollaboration プロジェクトに取り込みます。 | *近日リリース予定* |
| [[!DNL Azure Blob Storage]](./configure-azure-storage-audience-sourcing.md) | [!DNL Azure Blob Storage] コンテナーを接続して、[!DNL Microsoft Azure]環境から1st パーティデータセットを取得します。 | 使用可能 |
| [[!DNL Azure Data Lake Storage]](./configure-azure-storage-audience-sourcing.md) | [!DNL Azure Data Lake Storage Gen 2] アカウントを接続して、[!DNL Azure] データレイクに保存されているオーディエンスデータを取り込みます。 | 使用可能 |

{style="table-layout:auto"}

## 次の手順

ソースを接続してオーディエンスを取り込んだら、詳細の表示、設定の更新、または既存のソースの削除を行うことができます。 詳しくは、[&#x200B; データ接続の管理](./manage-data-connection.md) ガイドを参照してください。
