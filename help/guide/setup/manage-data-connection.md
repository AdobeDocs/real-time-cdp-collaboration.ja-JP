---
title: データ接続を管理
description: Real-Time CDP Collaborationでの一致キー、スケジュール、ユースケース、オーディエンスフィルタリングなど、データ接続を管理する方法について説明します
audience: administrator, data engineer
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 5%

---

# データ接続を管理

{{limited-availability-release-note}}

## 概要

Real-Time CDP Collaborationのデータ接続を使用して、様々なプラットフォームからオーディエンスをソース化します。 一致キーを管理し、既存のデータ接続のデータ更新をスケジュールする方法を説明します。 さらに、様々な属性でオーディエンスをフィルタリングして、より詳細なインサイトを得ることができます。

## データ接続の表示

既存のデータ接続を表示するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL マイデータ接続]**」タブを選択します。 現在のすべてのデータ接続が表示され、各接続の概要が簡単に示されます。 一致キー、スケジュールの詳細、オーディエンスなど、データ接続の情報の完全な表示については、対応する接続で **[!UICONTROL データ接続を表示]** を選択します。

![ 「マイデータ接続」タブビューが表示およびハイライト表示されたワークスペースを設定 ](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### 一致キー {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="一致キー"
>abstract=" 一致キーは、様々なソースのデータの一致方法を決定します。以下に示す一致キーは、ソースフィールドをマッピングしたターゲットフィールドです。"

一致キーは、[ ソースフィールドをマッピング ](./onboard-audiences.md#map-fields) したターゲットフィールドです。 マッチ キーの仕組みについては、[ マッチ キー ](./onboard-account.md#set-up-match-keys) ガイドを参照してください。

![ 「キーを一致させる」セクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### スケジュール設定 {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="スケジュール設定"
>abstract="データ接続のスケジュールの詳細を表示し、必要に応じて設定を編集します。"

データ接続のスケジュール設定を表示および管理します。 スケジュールによって、オーディエンスの更新頻度が決定されます。

データ接続が作成されたら、データ接続ワークスペースの **[!UICONTROL スケジュール]** セクションから直接更新頻度、開始日、終了日を更新できます。

>[!NOTE]
>
>Adobe Experience Platformからオーディエンスを取得する場合、オーディエンスは、データ接続が確立されてから 24 時間以内に使用可能になります。 初期ソーシング後、定義した頻度に従って、オーディエンスデータが更新されます。

スケジュールについて詳しくは、オーディエンスの設定ガイドの [ スケジュールの節 ](/help/guide/setup/onboard-audiences.md#schedule) を参照してください。

![ スケジュールセクションがハイライト表示されたデータ接続のワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## データ接続を編集 {#edit-data-connection}

既存のデータ接続の一致キーとスケジュール設定を更新する方法については、次の節を参照してください。

### 一致キーを編集 {#edit-match-keys}

>[!IMPORTANT]
>
>データ接続の一致キーを編集する前に、次の点に注意してください。
>
>* データ接続に使用できるのは、お使いのアカウントに設定されている一致キーのみです。
>* 現時点では、データ接続に追加の一致キーを追加できますが、一致キーを有効にすると、削除できなくなります。

**[!UICONTROL キーを一致]** セクションから **[!UICONTROL 編集]** を選択します。

![ 「編集」オプションがハイライト表示された「キーを一致」セクション ](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

確認ダイアログが表示され、データ接続に対する変更がすべての関連オーディエンスに適用されることを説明します。 「**[!UICONTROL OK]**」を選択して確定します。 今後、この確認をスキップするように選択できます。

![ データ接続に対する変更がすべての関連オーディエンスに適用されることを示す確認ダイアログ。](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

**[!UICONTROL 一致キー]** ダイアログでは、ソースフィールドとそれに対応するターゲットフィールド（一致キー）との既存のマッピングを表示できます。 マッピングされたソースフィールドを更新することで一致キーを編集したり、マッピングフィールド行を追加して新しい一致キーを入力したりできます。

![ ソースフィールドと対応するターゲットフィールドとの既存のマッピングを表示するキーを一致ダイアログ ](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### 一致キーを追加 {#add-match-keys}

**[!UICONTROL フィールドを追加]** を選択して、新しいフィールド行を追加します。

![ 「フィールドを追加」を選択すると、一致キーを選択ダイアログに入力可能な空の新しいマッピングフィールドが表示されます。](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

次に、空のソースフィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが開き、**[!UICONTROL ID 名前空間]** および **[!UICONTROL プロファイル属性]** オプションが表示されます。 リストをフィルターし、検索オプションで目的のソースフィールドを見つけることができます。

目的のソースフィールドを選択し、続いて **[!UICONTROL 選択]** をクリックします。

![GAID オプションが選択されたソースフィールドを選択ダイアログ ](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

**[!UICONTROL キーを一致]** ダイアログで、ドロップダウンメニューを使用して、新しいソースフィールドをターゲットフィールドにマッピングします。 使用可能なすべてのターゲットフィールドは、共同作業者アカウント用に設定された一致キーです。 必要なターゲットフィールドが表示されない場合は、[ アカウントの一致キーを編集 ](./onboard-account.md#edit-match-keys) して追加します。

プレーンテキストのメールソースフィールドを **[!UICONTROL ハッシュ化されたメール]** ターゲットフィールドにマッピングする場合など、ハッシュ化されていないフィールドをハッシュ化されたターゲットフィールドにソース化するには、**[!UICONTROL 変換を適用]** オプションを使用します。

![ 新しいソースフィールドにマッピングするために使用可能なすべてのターゲットフィールドを表示するドロップダウンメニュー。](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

フィールドのマッピングが完了したら、更新を確認し、「**[!UICONTROL 確認]**」を選択して変更を適用します。

![ 「確認」オプションがハイライト表示された更新済みフィールドマッピングを示すキーを一致ダイアログ ](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

一致キーが正常に更新されたことを確認するダイアログが表示されます。

### スケジュールの編集 {#edit-scheduling}

データ接続が作成されたら、データ接続ワークスペースの **[!UICONTROL スケジュール]** セクションから直接更新頻度、開始日、終了日を更新できます。

既存のデータ接続の頻度を編集して、オーディエンスの更新頻度をより詳細に制御できます。 スケジュールを編集するには、スケジュールカードのデータ接続内から **[!UICONTROL 編集]** を選択します。

![ 「編集」オプションがハイライト表示された「スケジュール」セクション。](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

確認ダイアログが表示され、データ接続に対する変更がすべての関連オーディエンスに適用されることを説明します。 「**[!UICONTROL OK]**」を選択して確定します。 今後、この確認をスキップするように選択できます。

![ データ接続に対する変更がすべての関連オーディエンスに適用されることを示す確認ダイアログ。](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

**[!UICONTROL スケジュール]** ダイアログで、ドロップダウンメニューを選択して **[!UICONTROL 頻度]** を更新します。 更新頻度を、毎日または 2 ～ 6 日ごとに実行するように設定します。

![ 頻度ドロップダウンを含むスケジュールダイアログが展開され、オーディエンスの更新頻度オプションが表示されました。](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

次に、オーディエンスの入力および更新を行う期間を更新する場合は、「**[!UICONTROL 日付範囲]**」を選択します。

![ 日付範囲ドロップダウンを表示するスケジュールダイアログが展開され、オーディエンス母集団と更新の開始日と終了日を編集できるようになりました。](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

完了したら、更新を確認し、「**[!UICONTROL 保存]**」を選択して変更を適用します。

![ 「更新と保存」オプションがハイライト表示されたスケジュールダイアログ ](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## データ接続を削除

データ接続を削除すると、Collaboration全体で、基になるすべてのオーディエンス、関連する設定および使用状況が削除されます。 このアクションは取り消せません。

既存のデータ接続を削除するには、個々のデータ接続のワークスペース内にある削除アイコン（![ 削除アイコン ](/help/assets/common/delete.svg)）を選択します。

![ 削除オプションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

確認ダイアログが表示されます。 **[!UICONTROL 削除]** を選択して、データ接続の削除を終了します。

![ 「削除」オプションがハイライト表示されたデータ接続を削除ダイアログ ](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## オーディエンス管理 {#manage-audiences}

データ接続に接続されているオーディエンスのリストが、ワークスペースの下部に表示されます。 リストには、ステータス、ソース、接続アクセスなど、各オーディエンスの簡単な概要が表示されます。 オーディエンスのカテゴリ、接続アクセスまたはメタデータ表示を編集するには、オーディエンスの名前を選択します。 オーディエンスの管理に関する完全なガイドについては、[ 個々のオーディエンスの表示 ](./onboard-audiences.md#view-individual-audiences) ガイドを参照してください。

![ オーディエンスがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## 次の手順

データ接続を管理すると、共同作業者が検出可能にしたオーディエンスとオーディエンスの間で [ 重複を検出 ](/help/guide/collaborate/discover.md) できます。
