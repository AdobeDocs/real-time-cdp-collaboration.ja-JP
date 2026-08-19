---
title: データ接続を管理
description: Real-Time CDP Collaborationで一致キー、スケジューリング、ユースケース、オーディエンスフィルタリングなど、データ接続を管理する方法について説明します
audience: administrator, data engineer
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
TQID: https://experienceleague.adobe.com/QvkEpR1fJMZ5BXrucAzEtxFNSfSMS-2hIZvMSg63ySE
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 07471fb3690c3ff57d21231da3d126cf9545677a
workflow-type: tm+mt
source-wordcount: 1299
ht-degree: 7%

---

# データ接続を管理

{{limited-availability-release-note}}

## 概要

Real-Time CDP Collaborationのデータ接続を使用して、様々なプラットフォームからオーディエンスを獲得できます。 既存のデータ接続の一致キーを管理し、データの更新をスケジュールする方法について説明します。 さらに、異なる属性によってオーディエンスをフィルタリングし、より詳細なインサイトを得ることができます。

>[!NOTE]
>
>新しいデータ接続を作成するには、[&#x200B; オーディエンスの追加と管理](./onboard-audiences.md)を参照してください。

## データ接続の表示

既存のデータ接続を表示するには、**[!UICONTROL 設定]**&#x200B;に移動し、**[!UICONTROL データ接続]** タブを選択します。 現在のデータ接続がすべて表示され、各接続の概要が表示されます。 一致キー、スケジュールの詳細、オーディエンスなど、データ接続の情報を包括的に表示するには、対応する接続で「**[!UICONTROL データ接続を表示]**」を選択します。

![自分のデータ接続のタブ ビューが表示され、ハイライト表示されたワークスペースの設定](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### 一致キー {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="一致キー"
>abstract="一致キーは、様々なソースのデータの一致方法を決定します。 以下に示す一致キーは、ソースフィールドをマッピングしたターゲットフィールドです。"

一致キーは、ソースフィールドを[&#x200B; マッピングしたターゲットフィールドです。](./onboard-audiences.md#map-fields) 一致キーの仕組みについて詳しくは、[一致キー](./onboard-account.md#set-up-match-keys) ガイドを参照してください。

![一致キーセクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### スケジュール設定 {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="スケジュール設定"
>abstract="データ接続のスケジュールの詳細を表示し、必要に応じて設定を編集します。"

データ接続のスケジュール設定を表示および管理します。 スケジュール設定により、オーディエンスが更新される頻度が決まります。

データ接続を作成した後、データ接続ワークスペースの「**[!UICONTROL スケジューリング]**」セクションから、その更新頻度、開始日、終了日を直接更新できます。

>[!NOTE]
>
>Adobe Experience Platformからオーディエンスを取得する場合、データ接続が確立されてから24時間以内にオーディエンスを利用できるようになります。 最初のソーシング後、オーディエンスデータは、定義された頻度に従って更新されます。

スケジュール設定について詳しくは、オーディエンスの設定に関するガイドの「[&#x200B; スケジュール設定」セクション &#x200B;](/help/guide/setup/onboard-audiences.md#schedule)を参照してください。

![&#x200B; スケジュール セクションがハイライト表示されたデータ接続のワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## データ接続を編集 {#edit-data-connection}

次の節では、既存のデータ接続の一致キーとスケジュール設定を更新する方法について説明します。

### 一致キーを編集 {#edit-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_edit_measurement_data_connection_enrichment"
>title="エンリッチメント"
>abstract="エンリッチメントのオフはサポートされていません。 代わりに、エンリッチメント結合キーを変更できます。"
>additional-url="https://www.adobe.com/go/rtcdp-collaboration-manage-dataconnections_jp" text="エンリッチメント"

>[!IMPORTANT]
>
>データ接続の一致キーを編集する前に、次の点に注意してください。
>
>* データ接続には、アカウントに設定された一致キーのみを使用できます。
>* 現時点では、データ接続に照合キーを追加できますが、照合キーを有効にすると、削除できません。

「**[!UICONTROL 一致キー]**」セクションから「**[!UICONTROL 編集]**」を選択します。

![編集オプションがハイライト表示された「キーの一致」セクション。](/help/assets/setup/manage-data-connection/edit-match-keys.png){zoomable="yes"}

データ接続に対する変更が、関連するすべてのオーディエンスに適用されることを示す確認ダイアログが表示されます。 確認するには、**[!UICONTROL OK]**&#x200B;を選択してください。 この確認は後でスキップできます。

![&#x200B; データ接続の変更がすべての関連オーディエンスに適用されることを示す確認ダイアログ。](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

**[!UICONTROL キーの一致]** ダイアログで、ソースフィールドと対応するターゲットフィールド（キーの一致）の間の既存のマッピングを表示できます。 マッピングソースフィールドを更新して一致キーを編集したり、マッピングフィールドの行を追加して新しい一致キーを入力したりできます。

![&#x200B; ソースフィールドと対応するターゲットフィールドの間の既存のマッピングを表示するキーマッチダイアログ。](/help/assets/setup/manage-data-connection/match-keys-dialog.png){zoomable="yes"}

#### 一致キーを追加 {#add-match-keys}

「**[!UICONTROL フィールドを追加]**」を選択して、新しいフィールド行を追加します。

![&#x200B; フィールドを追加を選択すると、一致キーダイアログに、入力の準備ができた空の新しいマッピングフィールドが表示されます。](/help/assets/setup/manage-data-connection/add-new-field.png){zoomable="yes"}

次に、空のソースフィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示され、**[!UICONTROL ID名前空間]**&#x200B;および&#x200B;**[!UICONTROL プロファイル属性]** オプションが表示されます。 リストをフィルタリングし、検索オプションを使用して目的のソースフィールドを見つけることができます。

必要なソースフィールドを選択し、続いて&#x200B;**[!UICONTROL 選択]**&#x200B;します。

![GAID オプションを選択したソースフィールドを選択ダイアログ。](/help/assets/setup/manage-data-connection/select-source-field.png){zoomable="yes"}

**[!UICONTROL プロファイル属性]** オプションでは、一部のソースフィールドが、オブジェクトの配列であるリスト内でモデル化されます。 これらのリストフィールドを展開し、その中にネストされたフィールドを選択して、一致キーにマッピングできます。 詳しくは、[&#x200B; マップフィールド &#x200B;](./onboard-audiences.md#map-fields) ガイドを参照してください。

**[!UICONTROL キーを一致]** ダイアログで、ドロップダウンメニューを使用して、新しいソースフィールドをターゲットフィールドにマッピングします。 使用可能なすべてのターゲットフィールドは、共同作業者アカウントに設定された一致キーです。 必要なターゲットフィールドが表示されない場合は、[&#x200B; アカウントの照合キー](./onboard-account.md#edit-match-keys)を編集して追加します。

例えば、プレーンテキストメールのソースフィールドを&#x200B;**[!UICONTROL ハッシュ化されたメール]**&#x200B;のターゲットフィールドにマッピングする場合に、ハッシュ化されていないフィールドをハッシュ化されたターゲットフィールドにソーシングする場合は、**[!UICONTROL 変換を適用]** オプションを使用します。

![新しいソースフィールドとマッピングするために使用可能なすべてのターゲットフィールドを表示するドロップダウンメニュー。](/help/assets/setup/manage-data-connection/select-target-field.png){zoomable="yes"}

##### [!DNL Demdex ID (ECID)]を追加 {#add-demdex-id-ecid}

一致キーとして[!DNL Demdex ID (ECID)]を追加する場合は、最初にアカウント設定[&#128279;](../setup/onboard-account.md#set-up-match-keys)で有効になっていることを確認してください。 [!DNL Demdex ID (ECID)]について詳しくは、[&#x200B; サポートされている一致キー](../setup/onboard-account.md#supported-match-keys)を参照してください。

**[!UICONTROL 一致キー]** ダイアログで、新しいマッピングフィールド行を追加します。 次に、ソースフィールドとして&#x200B;**[!UICONTROL ECID]**&#x200B;を選択し、ドロップダウンリストからターゲットフィールドとして&#x200B;**[!UICONTROL Demdex ID （ECID）]**&#x200B;を選択します。

![Demdex ID （ECID）一致キーのマッピングフィールドを含む一致キーダイアログがハイライト表示されます。](/help/assets/setup/manage-data-connection/demdex-id-ecid-match-key.png){zoomable="yes"}

フィールドのマッピングが完了したら、更新を確認し、**[!UICONTROL 確認]**&#x200B;を選択して変更を適用します。

![確認オプションがハイライト表示された更新されたフィールドマッピングを表示するキーマッチダイアログ。](/help/assets/setup/manage-data-connection/review-and-confirm.png){zoomable="yes"}

確認ダイアログは、一致キーが正常に更新されたことを確認します。

### スケジュールの編集 {#edit-scheduling}

データ接続を作成した後、データ接続ワークスペースの「**[!UICONTROL スケジューリング]**」セクションから、その更新頻度、開始日、終了日を直接更新できます。

既存のデータ接続の頻度を編集することで、オーディエンスの更新頻度をより適切に制御できます。 スケジュールを編集するには、スケジューリングカードのデータ接続内から&#x200B;**[!UICONTROL 編集]**&#x200B;を選択します。

![編集オプションがハイライト表示されたスケジューリングセクション。](/help/assets/setup/manage-data-connection/edit-scheduling.png){zoomable="yes"}

データ接続に対する変更が、関連するすべてのオーディエンスに適用されることを示す確認ダイアログが表示されます。 確認するには、**[!UICONTROL OK]**&#x200B;を選択してください。 この確認は後でスキップできます。

![&#x200B; データ接続の変更がすべての関連オーディエンスに適用されることを示す確認ダイアログ。](/help/assets/setup/manage-data-connection/confirm-data-connection-changes.png){zoomable="yes"}

**[!UICONTROL スケジュール]** ダイアログで、ドロップダウンメニューを選択して&#x200B;**[!UICONTROL 頻度]**&#x200B;を更新します。 毎日、または2～6日ごとに実行するように更新頻度を設定します。

![頻度ドロップダウンを含むスケジュール ダイアログが拡張され、オーディエンスの更新頻度オプションが表示されました。](../../assets/setup/manage-data-connection/edit-frequency.png){zoomable="yes"}

次に、オーディエンスが入力され、更新される期間を更新する場合は、**[!UICONTROL 日付範囲]**&#x200B;を選択します。

![日付範囲ドロップダウンを表示するスケジュール ダイアログが拡張され、オーディエンスの母集団と更新の開始日と終了日を編集できるようになりました。](../../assets/setup/manage-data-connection/edit-date-range.png){zoomable="yes"}

完了したら、更新を確認し、**[!UICONTROL 保存]**&#x200B;を選択して変更を適用します。

![更新と保存オプションを強調表示するスケジュール ダイアログ。](../../assets/setup/manage-data-connection/scheduling-dialog.png){zoomable="yes"}

## データ接続を削除 {#delete-data-connection}

データ接続を削除すると、Collaboration全体で、基盤となるオーディエンス、関連する設定、使用がすべて削除されます。 このアクションは取り消せません。

既存のデータ接続を削除するには、個々のデータ接続のワークスペース内の削除アイコン（![削除アイコン &#x200B;](/help/assets/common/delete.svg)）を選択します。

![削除オプションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

確認ダイアログが表示されます。 データ接続の削除を完了するには、**[!UICONTROL 削除]**&#x200B;を選択します。

![削除オプションがハイライト表示されたデータ接続を削除ダイアログ。](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## オーディエンス管理 {#manage-audiences}

データ接続に接続されたオーディエンスのリストがワークスペースの下部に表示されます。 このリストには、ステータス、ソース、接続アクセスなど、各オーディエンスの概要が表示されます。 オーディエンスのカテゴリ、接続アクセス、メタデータの表示を編集するには、オーディエンス名を選択します。 オーディエンスの管理に関する完全なガイドについては、[個々のオーディエンスの表示](./onboard-audiences.md#view-individual-audiences) ガイドを参照してください。

![&#x200B; オーディエンスがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## 次の手順

データ接続を管理すると、オーディエンスと共同作業者が検索できるオーディエンスとの重複を[発見](/help/guide/collaborate/discover.md)できます。
