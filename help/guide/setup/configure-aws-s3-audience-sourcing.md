---
title: オーディエ  [!DNL Amazon S3]  スソーシング用の設定
description: ストレージをセルフサービスのデータソースとして設定および接続し  [!DNL Amazon S3] 、オーディエンスデータをReal-Time CDP Collaborationに取り込む方法について説明します。
source-git-commit: 7a2bfb524d77d42690f3abe848a59aae5b16b667
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 1%

---

# オーディエンスソーシング用の [!DNL Amazon S3] の設定

Adobe Real-Time CDP Collaboration UI で [!DNL Amazon S3] ストレージを設定および接続し、アクティベーションと重複分析のためにオーディエンスデータをソースする方法について説明します。

>[!IMPORTANT]
>
>このガイドに従う前に、AWS アカウントでAdobeの IAM ロールを認証する手順を完了している必要があります。\
>詳細な設定手順については、**[オーディエンスソーシングのAWS権限の設定](./configure-aws-permissions-audience-sourcing.md)** ガイドを参照してください。

## 概要 {#overview}

このワークフローを使用して、[!DNL Amazon S3] から直接ファーストパーティオーディエンスをソース化および管理します。 設定後、Collaborationは S3 バケットからオーディエンスを自動的にソース化し、インサイトとアクティベーションで使用できるようにします。

S3 を通じて提供されるオーディエンスは、Adobe Experience Platformから提供されるオーディエンスと同じガバナンスおよびデータ処理ルールに従います。

## 前提条件 {#prerequisites}

S3 データ接続を設定する前に、次を確認します。

* **[!DNL Amazon S3]オーディエンスソーシング仕様（v1.1）** に準拠するオーディエンスファイルを含む **[アクティブな](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)** バケットにアクセスできます。
* AWSで **IAM ロール** を作成し、（アクセス/秘密鍵ではなく **想定されるロール** メソッドを使用してバケットにアクセスする権限をAdobeに付与しました。 手順について詳しくは、**[オーディエンスソーシングのAWS権限の設定](./configure-aws-permissions-audience-sourcing.md)** を参照してください。 IAM 役割には、次の権限が含まれている必要があります。

   * `ListBucket`
   * `GetBucketLocation`
   * `GetObject`

* 次の値の準備が整いました。

   * **IAM ロール Amazon リソース名（ARN）**
   * **S3 バケット名**
   * **フォルダーパス** （オーディエンスファイルを含むディレクトリのプレフィックス）

>[!NOTE]
>
>オーディエンスファイルは、許可された S3 バケットの **ルートフォルダーパス** に配置する必要があります。 サブフォルダー構造はサポートされていません。

## [!DNL Amazon S3] 接続の設定 {#configure-aws-s3-connection}

**[!UICONTROL 設定]** ワークスペース内の **[!UICONTROL マイオーディエンス]** タブで、追加アイコン（![&#x200B; 追加アイコン](/help/assets/icons/plus.png)）を選択してから、**[!UICONTROL オーディエンス]** を選択します。

初めてオーディエンスを使用する場合は、「**[!UICONTROL 追加]**」オプションを選択することもできます。

![&#x200B; 追加アイコンと「オーディエンスを追加」オプションが表示された設定ワークスペースの「マイオーディエンス」タブ &#x200B;](../../assets/setup/add-manage-audiences/add-audiences.png)

オーディエンスを追加ワークフローが表示されます。 **[!UICONTROL 新しいデータ接続を追加]** を選択してから、「**[!UICONTROL 次へ]**」を選択します。

![&#x200B; 「新しいデータ接続を追加」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### データ接続として「[!DNL Amazon S3]」を選択します {#select-aws-s3}

データ接続として **[!UICONTROL 0&rbrace;Amazon S3&rbrace; を選択し、続いて]** 次へ **[!UICONTROL を選択します。]**

![&#x200B; 選択可能なオプションとして [!DNL Amazon S3] を含むデータ接続選択画面 &#x200B;](../../assets/setup/aws-audience-sourcing/select-s3-data-connection.png)

### オーディエンスファイルの要件を確認する {#review-audience-requirements}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sourcing_specifications"
>title="オンボーディング用にデータを準備"
>abstract="Amazon S3 for Collaborationのオーディエンスデータを書式設定および構造化する方法については、オーディエンスソーシング仕様ガイドを参照してください。"
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-audience-sourcing" text="ガイドを参照してください"

オーディエンスファイルをどのように構造化する必要があるかを説明するダイアログが表示されます。 **[[!UICONTROL オーディエンスソーシングの仕様]](../../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.1.pdf)** へのリンクを使用して、[!DNL Amazon S3] for Collaborationのオーディエンスデータを書式設定および構造化して正しく読み取る方法を確認します。

>[!IMPORTANT]
>
>Adobeが [!DNL Amazon S3] ストレージからデータを取得して処理できるように、Adobeを [!DNL Amazon S3] ユーザーとして承認している必要があります。

オーディエンスファイルは、オーディエンスソーシング仕様に準拠している必要があります。 一致キーは、必要な形式に基づいて自動的にマッピングされます。

主な考慮事項は次のとおりです。

* ファイルは、複数の値に対してコンマを区切り文字およびパイプ（`|`）として使用し、CSV 形式である必要があります。
* 複数のファイルをアップロードする場合は、すべてのファイルに同じ列が含まれていることを確認します。
* 各オーディエンスレコードには、`AUDIENCE_ID` と、少なくとも一致キー（`HASHED_EMAIL_SHA_256`、`HASHED_PHONE_SHA_256`、`HASHED_IPV4_SHA_256`、`CRM_ID`、`LOYALTY_ID`、`ADFIXUS_ID` など）が含まれている必要があります。
* データ更新は、Collaborationでのソーシング設定での選択内容に基づいて、1 ～ 6 日ごとに行われます。

![&#x200B; オーディエンスソーシングの仕様へのリンクが含まれているソーシング用データの準備ダイアログ &#x200B;](../../assets/setup/aws-audience-sourcing/prepare-data-sourcing-dialog.png)

### S3 接続の認証 {#authenticate-s3-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_sources_s3_folderpath"
>title="フォルダーパスの形式"
>abstract="オーディエンスファイルが格納されている [!DNL Amazon S3] バケット内のフォルダーパス（接頭辞）を入力します。<br><ul><li>パスの先頭にスラッシュ（/）を使用しないでください。</li><li>パスの末尾に末尾のスラッシュを含めます。</li><ul><br> 有効な例：`base/path/`<br> 無効な例：`/base/path`"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_amazon_s3"
>title="Amazon S3 のオーディエンスを追加"
>abstract="Amazon S3 ストレージを接続するには、Adobe サービスユーザーを認証して、処理用のオーディエンスデータを取得してください。 Experience Leagueで説明されている手順に従って、Amazon S3 ストレージへのアクセスをAdobeに許可します。"

次に、S3 バケットをCollaborationに接続するための [!DNL Amazon S3] 資格情報を指定します。

**[オーディエンスソーシングのAWS権限の設定](./configure-aws-permissions-audience-sourcing.md)** で説明する手順に従って、Adobeへのアクセス権を付与します
[!DNL Amazon S3] ストレージ。 完了したら、次の UI フィールドに値を入力します。

* IAM 役割
* S3 バケット名
* フォルダーパス

![IAM 役割、S3 バケット名およびフォルダーパスのフィールドを持つ [!DNL Amazon S3] 接続フォーム &#x200B;](../../assets/setup/aws-audience-sourcing/s3-authentication-credentials-form.png)

### 同意確認を確認 {#confirm-consent}

その後、続行する前に、同意オプトアウトが削除されたことを確認する必要があります。 確認ボックスに続いて **[!UICONTROL OK]** をチェックして、確定します。

![&#x200B; 続行する前に確認が必要な同意オプトアウト確認ダイアログ &#x200B;](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### 認証結果の検証 {#validate-authentication}

接続後、システムにより資格情報が検証され、次のいずれかのメッセージが表示されます。

| ステータス | メッセージ | 説明 |
|---| ---|---|
| **成功** | **[!UICONTROL 認証に成功]** | [!DNL Amazon S3] への接続が正常に確立されました。 |
| **失敗** | **[!UICONTROL 認証できませんでした]** | 資格情報を確認して、もう一度試してください。 |
| **アクセスが拒否されました** | **[!UICONTROL アクセスが拒否されました]** | 資格情報には、この [!DNL Amazon S3] バケットにアクセスするために必要な権限がありません。 アクセス設定を確認するか、管理者に問い合わせてください。 |
| **無効なファイル形式** | **[!UICONTROL 無効なファイル形式]** | オーディエンスデータが、期待された構造に一致しません。 ファイルがオーディエンスソーシング仕様に準拠していることを確認してください。 |
| **オーディエンスファイルが見つかりません** | **[!UICONTROL オーディエンスファイルが見つかりません]** | 指定したフォルダーパスにオーディエンスファイルが存在し、そのパスにアクセスできることを確認してください。 |
| **内部エラー** | **[!UICONTROL 内部エラーが発生しました]** | もう一度やり直してください。 問題が解決しない場合は、カスタマーサポートにお問い合わせください。 |


### 接続の詳細を入力 {#provide-connection-details}

S3 データ接続のわかりやすい名前と、オプションで説明を入力します。 次の UI フィールドに値を入力します。

* **[!UICONTROL データ接続名]** （必須）
* **[!UICONTROL データ接続の説明]** （オプション）

![&#x200B; 接続名と説明のフィールドを含むデータ接続の詳細フォーム &#x200B;](../../assets/setup/aws-audience-sourcing/s3-connection-name-description.png)

### 自動マッピングされた ID フィールドを確認 {#auto-mapped-fields}

**[!UICONTROL マッピング]** 画面は読み取り専用です。 変換を追加、削除、適用することはできません。 Collaborationは、オーディエンスソーシング仕様に基づいて、オーディエンスファイルのソース ID フィールドをターゲットフィールドに自動的にマッピングします。

マッピングされたフィールドを視覚的に確認し、「**[!UICONTROL 次へ]**」を選択して続行します。

![&#x200B; 自動マッピングされたソースおよびターゲット ID フィールドを示すフィールドマッピング画面。](../../assets/setup/aws-audience-sourcing/s3-field-mapping-auto-mapped.png)

### 更新頻度と日付範囲のスケジュール設定 {#schedule-refresh}

**[!UICONTROL スケジュール]** ビューが表示されます。 ドロップダウンメニューを使用して、更新頻度を 1～6 日の間で選択し、アクティブな日付範囲を設定します。 開始日と終了日を指定するには、カレンダーアイコンを使用します。

>[!IMPORTANT]
>
>Collaboration クレジットを効果的に管理するには、更新頻度を、基になる S3 データの更新頻度と一致または上回るように設定します。 サポートされる更新間隔の最小値は、6 日に 1 回です。

![&#x200B; 更新頻度オプションと日付範囲の設定を含むスケジュール設定画面 &#x200B;](../../assets/setup/aws-audience-sourcing/s3-schedule-refresh-frequency.png)

### 接続のレビューと完了 {#review-and-complete}

最後に、概要画面で設定を確認します。 このビューには、次のセクションの概要が含まれます。

* **[!UICONTROL データ接続]**：設定した IAM 役割、S3 バケット名およびフォルダーパスが表示されます。
* **[!UICONTROL 詳細]**：後で識別できるように、データ接続の名前と説明（オプション）が表示されます。
* **[!UICONTROL マッピング]**：アップロードしたオーディエンスファイル（例：`HASHED_EMAIL`）のソースフィールドを、Collaborationで使用されるターゲットフィールド（例：ハッシュ化されたメール）にどのようにマッピングするかをリストします。
* **[!UICONTROL スケジュール]**：接続がオーディエンスデータとソーシングのアクティブな日付範囲を更新する頻度の概要を示します。

セクションを編集する必要がある場合は、鉛筆アイコンを選択します。 「**[!UICONTROL 完了]**」を選択して、すべてのセクションを確定します。

![&#x200B; データ接続、詳細、マッピング、スケジュールの各セクションが表示されている概要の確認画面 &#x200B;](../../assets/setup/aws-audience-sourcing/s3-connection-review-summary.png)

データ接続が正常に作成され、オーディエンスソーシングが処理中であることを示すダイアログ確認が表示されます。

## ソースとなるオーディエンスのレビュー {#review-sourced-audiences}

設定が完了すると、Collaborationは S3 バケットからのオーディエンスのソーシングを開始します。 [!DNL Amazon S3] バケットをソースとするオーディエンスは、「**[!UICONTROL マイオーディエンス]** タブに表示され、Experience Platformをソースとするオーディエンスと同じ機能と情報を持ちます。

オーディエンスソーシングが進行中の場合は、バナーが画面の上部に表示されます。 個々のオーディエンスは、ソーシングが完了した後にのみ表示されます。

![&#x200B; オーディエンスのソーシングが進行中であることを示す「オーディ [!DNL Amazon S3] ンス」タブ &#x200B;](../../assets/setup/aws-audience-sourcing/s3-audiences-sourcing-in-progress.png)

S3 オーディエンスがソーシングされると、使用可能なオーディエンスのリストが表形式またはカード形式で表示されます。

>[!TIP]
>
>オーディエンスソーシング時間は、S3 データのサイズと設定した更新頻度によって異なります。 データセットが大きい場合や頻繁な更新スケジュールが少ない場合は、**[!UICONTROL マイオーディエンス]** ワークスペースに表示されるのに時間がかかる場合があります。

![&#x200B; ソースとなるオーディエンスの表形式のリストを表示する「オーディエンス」タブ。](../../assets/setup/aws-audience-sourcing/s3-audiences-list-view.png)

グリッド表示またはテーブル表示の場合は、行項目または **[!UICONTROL オーディエンスを表示]** を選択して、特定のオーディエンスの概要を表示します。 オーディエンスのステータス、ソース、データ接続名が、次の詳細なパネルと共に表示されます。

**[!UICONTROL ID]**：データが利用可能になると、合計 ID 数と分類を表示します。
**[!UICONTROL カテゴリ]**：オーディエンスの整理またはフィルタリングに使用するタグをリストします。
**[!UICONTROL 接続アクセス]**：オーディエンスがプライベート、パブリック、特定の共同作業者と共有のどれであるかを示します。
**[!UICONTROL メタデータの表示]**：共同作業者に表示するオーディエンス情報（ID 数、重複率、インデックスなど）を定義します。

共同作業プロジェクトでオーディエンスを使用する前に、このビューを使用してオーディエンスの設定と表示設定を確認します。

詳しくは、[&#x200B; オーディエンスダッシュボードのドキュメントを表示 &#x200B;](https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#view-audiences-dashboard) を参照してください。

## S3 データ接続の表示 {#view-s3-connection}

新しく追加された [!DNL Amazon S3] 接続は、すぐに「**[!UICONTROL マイデータ接続]** タブで使用できます。 オーディエンスソースは [!UICONTROL Amazon S3] として表示されます。

S3 データ接続には、他のオーディエンスデータ接続と同じ機能および詳細が含まれています。ただし、このビューから直接オーディエンスを追加または編集することはできません。

>[!NOTE]
>
>[!DNL Amazon S3] データ接続は編集できません。 接続を作成した後は、更新頻度などの設定を変更できません。 設定を更新するには、既存の接続を削除して新しい接続を作成する必要があります。

![&#x200B; ソーシングステータス情報を含む [!DNL Amazon S3] データ接続を表示する「マイデータ接続」タブ。](../../assets/setup/aws-audience-sourcing/s3-data-connections-tab.png)

## 次の手順 {#next-steps}

これで、[!DNL Amazon S3] ストレージをCollaborationのデータソースとして正常に設定し、接続できました。 このワークフローを完了することで、アクティベーションと重複分析のためのファーストパーティオーディエンスデータの安全なソーシングが可能になりました。

ソーシングが完了すると、オーディエンスが **[!UICONTROL マイオーディエンス]** ワークスペースに表示され、共同作業やアクティベーションを行う準備が整います。 管理オプションについて詳しくは、[&#x200B; オーディエンスのソースおよび管理ドキュメント &#x200B;](./onboard-audiences.md) を参照してください。
