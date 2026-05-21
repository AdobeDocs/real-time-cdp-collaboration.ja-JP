---
title: オーディエンスソーシング用に [!DNL Amazon S3] を設定
description: Real-Time CDP Collaborationにオーディエンスデータを取り込むために、セルフサービスのデータソースとして [!DNL Amazon S3]  ストレージを設定して接続する方法について説明します。
exl-id: 566ceb1b-a72a-413d-b07d-409723892616
source-git-commit: 7ce74c7f87432c026e673c2197b0b8c3f91fb6f0
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 8%

---

# オーディエンスソーシング用に[!DNL Amazon S3]を設定

Adobe Real-Time CDP Collaboration UIで[!DNL Amazon S3] ストレージを設定し、ソースオーディエンスデータに接続してアクティベーションおよび重複分析を行う方法について説明します。

>[!IMPORTANT]
>
>このガイドに従う前に、AWS アカウント内でAdobeのIAM ロールを認証する手順を完了している必要があります。\
>ステップバイステップの設定手順については、「**[オーディエンスソーシング用AWS権限の設定](./configure-aws-permissions-audience-sourcing.md)** ガイド」を参照してください。

## 概要 {#overview}

このワークフローを使用して、[!DNL Amazon S3]から直接1st パーティオーディエンスを取得および管理します。 設定後、CollaborationはS3 バケットからオーディエンスを自動的にソースし、インサイトとアクティベーションに利用できるようにします。

S3を通じてソースされたオーディエンスは、Adobe Experience Platformからソースされたオーディエンスと同じガバナンスおよびデータ処理ルールに従います。

## 前提条件 {#prerequisites}

S3 データ接続を設定する前に、次の点を確認してください。

* **[Audience Sourcing Specification （v1.3）](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf)**&#x200B;に準拠するオーディエンスファイルを含むアクティブな&#x200B;**[!DNL Amazon S3]バケット**&#x200B;にアクセスできます。
* AWSで&#x200B;**IAM ロール**&#x200B;を作成しました。このロールは、**想定されたロール** メソッド （アクセス/秘密鍵ではありません）を使用してバケットへのアクセス権をAdobeに付与します。 詳しい手順については、**[オーディエンスソーシングに対するAWS権限の設定](./configure-aws-permissions-audience-sourcing.md)**&#x200B;を参照してください。 IAMの役割には、次の権限を含める必要があります。

   * `ListBucket`
   * `GetBucketLocation`
   * `GetObject`

* 次の値を用意しています。

   * **IAM ロール Amazon リソース名（ARN）**
   * **S3 バケット名**
   * **フォルダーパス** （オーディエンスファイルを含むディレクトリ接頭辞）

>[!NOTE]
>
>オーディエンスファイルは、承認済みS3 バケットの&#x200B;**ルートフォルダーパス**&#x200B;に配置する必要があります。 サブフォルダー構造はサポートされていません。

## [!DNL Amazon S3]接続の設定 {#configure-aws-s3-connection}

**[!UICONTROL セットアップ]** ワークスペース内の&#x200B;**[!UICONTROL マイオーディエンス]** タブから、追加アイコン（![追加アイコン &#x200B;](/help/assets/icons/plus.png)）を選択します。 **[!UICONTROL Audience]**&#x200B;を選択します。

これが初めてのオーディエンスの場合は、**[!UICONTROL 追加]** オプションを選択することもできます。

![追加アイコンと「オーディエンスを追加」オプションが表示された設定ワークスペースの「マイオーディエンス」タブ。](../../assets/setup/add-manage-audiences/add-audiences.png)

オーディエンスを追加ワークフローが表示されます。 「**[!UICONTROL 新しいデータ接続を追加]**」を選択し、「**[!UICONTROL 次へ]**」を選択します。

![新しいデータ接続を追加オプションがハイライト表示されたオーディエンスを追加ワークスペース。](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### データ接続として[!DNL Amazon S3]を選択 {#select-aws-s3}

**[!UICONTROL Amazon S3]**&#x200B;をデータ接続として選択し、次に&#x200B;**[!UICONTROL 次]**&#x200B;を選択します。

![選択可能なオプションとして[!DNL Amazon S3]を含むデータ接続の選択画面。](../../assets/setup/aws-audience-sourcing/select-s3-data-connection.png)

### オーディエンスファイルの要件の確認 {#review-audience-requirements}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications"
>title="オンボーディング用にデータを準備"
>abstract="Amazon S3 for Collaboration から取り込むオーディエンスデータをフォーマットおよび構造化する方法について詳しくは、オーディエンスソーシング仕様ガイドを参照してください。"
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="詳しくは、ガイドを参照してください。"

オーディエンスファイルの構造化を説明するダイアログが表示されます。 **[[!UICONTROL Audience Sourcing Specification]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1_3.pdf)**&#x200B;へのリンクを使用して、Collaborationでオーディエンスデータを正しく読み取るために[!DNL Amazon S3]からオーディエンスデータを書式設定および構造化する方法を説明します。

>[!IMPORTANT]
>
>Adobeが[!DNL Amazon S3] ストレージからデータを取得して処理できるように、[!DNL Amazon S3] ユーザーとしてAdobeを承認している必要があります。

オーディエンスファイルは、オーディエンスソーシング仕様に準拠している必要があります。 一致キーは、必要な形式に基づいて自動的にマッピングされます。

主要な検討事項は次のとおりです。

* ファイルはCSV形式で、複数の値に対してカンマを区切り記号として使用し、パイプ （`|`）を使用する必要があります。
* 複数のファイルをアップロードする場合は、すべてのファイルに同じ列が含まれていることを確認します。
* 各オーディエンスレコードには`AUDIENCE_ID`と、少なくとも`HASHED_EMAIL_SHA_256`、`HASHED_PHONE_SHA_256`、`HASHED_IPV4_SHA_256`、`CRM_ID`、`LOYALTY_ID`、`ADFIXUS_ID`などの一致キーが含まれている必要があります。
* Collaborationのソーシング設定時に、選択した内容に基づいて1～6日ごとにデータが更新されます。

![&#x200B; オーディエンスソーシング仕様へのリンクを含む「ソーシング用にデータを準備」ダイアログ。](../../assets/setup/aws-audience-sourcing/prepare-data-sourcing-dialog.png)

### S3 接続の認証 {#authenticate-s3-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="フォルダーパス形式"
>abstract="オーディエンスファイルが格納されている [!DNL Amazon S3] バケット内のフォルダーパス（接頭辞）を入力します。<br><ul><li>パスの先頭にスラッシュ（/）を使用しないでください。</li><li>パスの末尾にスラッシュを含めます。</li><ul><br>有効な例：`base/path/`<br>無効な例：`/base/path`"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_amazon_s3"
>title="Amazon S3 のオーディエンスを追加"
>abstract="Amazon S3 ストレージを接続するには、Adobe サービスユーザーを認証して、処理用のオーディエンスデータを取得します。 Experience League で説明されている手順に従い、アドビに対して、Amazon S3 ストレージへのアクセスを許可します。"

次に、S3 バケットをCollaborationに接続するための[!DNL Amazon S3]資格情報を入力します。

**[オーディエンスソーシングに対するAWS権限の設定](./configure-aws-permissions-audience-sourcing.md)**&#x200B;で説明されている手順に従って、Adobeにユーザーへのアクセス権を付与します。
[!DNL Amazon S3] ストレージ。 完了したら、次のUI フィールドに値を入力します。

* IAM 役割
* S3 バケット名
* フォルダーパス

![IAMの役割、S3 バケット名、フォルダーパスのフィールドを含む[!DNL Amazon S3]接続フォーム。](../../assets/setup/aws-audience-sourcing/s3-authentication-credentials-form.png)

### 同意の確認 {#confirm-consent}

次に、続行する前に、同意オプトアウトが削除されたことを確認する必要があります。 確認ボックスにチェックを入れ、**[!UICONTROL OK]**&#x200B;にチェックを入れて確認します。

![続行する前に確認が必要な同意オプトアウト確認ダイアログ。](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### 認証結果を検証 {#validate-authentication}

接続後、システムは資格情報を検証し、次のいずれかのメッセージを表示します。

| ステータス | メッセージ | 説明 |
|---| ---|---|
| **成功** | **[!UICONTROL 認証が成功しました]** | [!DNL Amazon S3]への接続が正常に確立されました。 |
| **失敗** | **[!UICONTROL 認証に失敗しました]** | 資格情報を確認して、もう一度試してください。 |
| **アクセスが拒否されました** | **[!UICONTROL アクセスが拒否されました]** | この[!DNL Amazon S3] バケットにアクセスするために必要な権限が資格情報にありません。 アクセス設定を確認するか、管理者にお問い合わせください。 |
| **無効なファイル形式** | **[!UICONTROL 無効なファイル形式]** | オーディエンスデータが予期された構造と一致しません。 ファイルがオーディエンスソーシング仕様に準拠していることを確認してください。 |
| **オーディエンスファイルが見つかりません** | **[!UICONTROL オーディエンスファイルが見つかりません]** | オーディエンスファイルが指定されたフォルダーパスに存在し、パスにアクセスできることを確認してください。 |
| **内部エラー** | **[!UICONTROL 内部エラーが発生しました]** | 再試行してください。 問題が解決しない場合は、カスタマーサポートにお問い合わせください。 |


### 接続の詳細を提供 {#provide-connection-details}

S3 データ接続のわかりやすい名前とオプションの説明を入力します。 次のUI フィールドに値を入力します。

* **[!UICONTROL データ接続名]** （必須）
* **[!UICONTROL データ接続の説明]** （オプション）

![接続名と説明のフィールドを含むデータ接続の詳細フォーム。](../../assets/setup/aws-audience-sourcing/s3-connection-name-description.png)

### 自動マッピングされたID フィールドの確認 {#auto-mapped-fields}

**[!UICONTROL マッピング]**&#x200B;画面は読み取り専用です。 変換を追加、削除、または適用することはできません。 Collaborationは、オーディエンスソーシング仕様に基づいて、オーディエンスファイルのソース ID フィールドをターゲットフィールドに自動的にマッピングします。

マッピングされたフィールドを視覚的に確認し、**[!UICONTROL 次へ]**&#x200B;を選択して続行します。

![自動マッピングされたソースおよびターゲット ID フィールドを表示するフィールドマッピング画面。](../../assets/setup/aws-audience-sourcing/s3-field-mapping-auto-mapped.png)

### スケジュール更新頻度と日付範囲 {#schedule-refresh}

**[!UICONTROL スケジュール]** ビューが表示されます。 ドロップダウンメニューを使用して、1日から6日の間の更新頻度を選択し、アクティブな日付範囲を設定します。 カレンダーアイコンを使用して、開始日と終了日を指定します。

>[!IMPORTANT]
>
>Collaboration クレジットを効果的に管理するには、更新の頻度を、基礎となるS3 データの更新頻度と一致するか、それを超えるように設定します。 サポートされる最小の更新間隔は、6日ごとに1回です。

![更新頻度オプションと日付範囲の設定を含むスケジュール設定画面。](../../assets/setup/aws-audience-sourcing/s3-schedule-refresh-frequency.png)

### 接続を確認して完了 {#review-and-complete}

最後に、サマリー画面で設定を確認します。 このビューには、次のセクションの概要が含まれています。

* **[!UICONTROL データ接続]**：設定したIAMの役割、S3 バケット名、フォルダーパスが表示されます。
* **[!UICONTROL 詳細]**: データ接続の名前とオプションの説明を表示して、後で識別できるようにします。
* **[!UICONTROL マッピング]**: アップロードしたオーディエンスファイルのソースフィールド（`HASHED_EMAIL`など）が、Collaborationで使用されるターゲットフィールド（ハッシュ化された電子メールなど）にどのようにマッピングされるかを一覧表示します。
* **[!UICONTROL スケジュール]**：接続がオーディエンスデータを更新する頻度と、ソーシング用にアクティブな日付範囲を要約します。

セクションを編集する必要がある場合は、鉛筆アイコンを選択します。 すべてのセクションを確認するには、**[!UICONTROL 完了]**&#x200B;を選択します。

![&#x200B; データ接続、詳細、マッピング、スケジュールのセクションを表示するレビューの概要画面。](../../assets/setup/aws-audience-sourcing/s3-connection-review-summary.png)

データ接続が正常に作成され、オーディエンスのソーシングが進行中であることを示すダイアログ確認が表示されます。

## ソース別オーディエンスの確認 {#review-sourced-audiences}

設定が完了すると、CollaborationはS3 バケットからオーディエンスのソーシングを開始します。 [!DNL Amazon S3] バケットを介してソースされたオーディエンスは、**[!UICONTROL マイオーディエンス]** タブに表示され、Experience Platformからソースされたオーディエンスと同じ機能と情報を持ちます。

オーディエンスのソーシングが進行中の場合は、画面の上部にバナーが表示されます。 個々のオーディエンスは、ソーシング完了後にのみ表示されます。

![&#x200B; 「オーディエンス」タブには、[!DNL Amazon S3]人のオーディエンスのソーシングが進行中であることが表示されます。](../../assets/setup/aws-audience-sourcing/s3-audiences-sourcing-in-progress.png)

S3 オーディエンスがソースされると、利用可能なオーディエンスのリストが表形式またはカードビューで提供されます。

>[!TIP]
>
>オーディエンスのソーシング時間は、S3 データのサイズと設定した更新頻度によって異なります。 データセットが大きい場合や更新スケジュールの頻度が低い場合は、**[!UICONTROL 自分のオーディエンス]** ワークスペースに表示されるまでに時間がかかる場合があります。

![&#x200B; ソース別オーディエンスの表形式のリストを表示する「オーディエンス」タブ。](../../assets/setup/aws-audience-sourcing/s3-audiences-list-view.png)

グリッド表示またはテーブル表示で、行アイテムを選択するか、**[!UICONTROL オーディエンスを表示]**&#x200B;して、特定のオーディエンスの概要を表示します。 オーディエンスのステータス、ソース、データ接続名が表示され、次の詳細パネルが表示されます。

**[!UICONTROL ID]**: データが使用可能になると、合計ID数と分類が表示されます。
**[!UICONTROL カテゴリ]**: オーディエンスの整理またはフィルタリングに使用されるタグを一覧表示します。
**[!UICONTROL 接続アクセス]**: オーディエンスがプライベート、パブリック、または特定の共同作業者と共有されているかどうかを示します。
**[!UICONTROL メタデータの可視化]**：共同作業者に表示されるオーディエンス情報（ID数、重複率、インデックスなど）を定義します。

このビューを使用して、コラボレーションプロジェクトでオーディエンスを使用する前に、オーディエンスの設定と表示設定を確認します。

詳しくは、[&#x200B; オーディエンスダッシュボードの表示ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#view-audiences-dashboard)を参照してください。

## S3 データ接続の表示 {#view-s3-connection}

新しく追加された[!DNL Amazon S3]接続は、**[!UICONTROL データ接続]** タブですぐに利用できます。 オーディエンスソースは[!UICONTROL Amazon S3]として表示されます。

S3 データ接続には、他のオーディエンスデータ接続と同じ機能と詳細が含まれていますが、このビューからオーディエンスを直接追加または編集することはできません。

>[!NOTE]
>
>[!DNL Amazon S3] データ接続は編集できません。 接続が作成されると、更新頻度などの設定を変更することはできません。 設定を更新するには、既存の接続を削除し、新しい接続を作成する必要があります。

![&#x200B; ソーシングステータス情報を含む[!DNL Amazon S3] データ接続を示す「My data connections」タブ。](../../assets/setup/aws-audience-sourcing/s3-data-connections-tab.png)

## 次の手順 {#next-steps}

これで、Collaborationのデータソースとして[!DNL Amazon S3] ストレージを正常に設定および接続しました。 このワークフローを完了することで、アクティベーションや重複分析のために、ファーストパーティのオーディエンスデータを安全にソーシングすることが可能になりました。

代わりに[!DNL Google Cloud Storage]を使用するには、[&#x200B; オーディエンスソーシング用GCSの設定](./configure-gcs-audience-sourcing.md)を参照してください。

ソーシングが完了すると、オーディエンスは&#x200B;**[!UICONTROL マイオーディエンス]** ワークスペースに表示され、コラボレーションとアクティベーションの準備が整います。 管理オプションについて詳しくは、[&#x200B; オーディエンスのソースと管理に関するドキュメント &#x200B;](./onboard-audiences.md)を参照してください。
