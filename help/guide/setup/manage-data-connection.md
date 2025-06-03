---
title: データ接続を管理
description: Real-Time CDP Collaborationでの一致キー、スケジュール、ユースケース、オーディエンスフィルタリングなど、データ接続を管理する方法について説明します
audience: administrator, data engineer
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 18%

---

# データ接続を管理

{{limited-availability-release-note}}

## 概要

Real-Time CDP Collaborationのデータ接続を使用して、様々なソースからオーディエンスを読み込みます。 既存のデータ接続の一致キーを管理し、データの読み込みをスケジュールする方法を説明します。 さらに、様々な属性でオーディエンスをフィルタリングして、より詳細なインサイトを得ることができます。

## データ接続の表示

既存のデータ接続を表示するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL マイデータ接続]**」タブを選択します。 現在のすべてのデータ接続が表示され、各接続の概要が簡単に示されます。 一致キー、スケジュールの詳細、オーディエンスなど、データ接続の情報の完全な表示については、対応する接続で **[!UICONTROL データ接続を表示]** を選択します。

![ 「マイデータ接続」タブビューが表示およびハイライト表示されたワークスペースを設定 ](/help/assets/setup/manage-data-connection/my-data-connections.png){zoomable="yes"}

### 一致キー {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="一致キー"
>abstract=" 一致キーは、様々なソースのデータの一致方法を決定します。ユースケースとプライバシーガイドラインに最も関連性の高い一致キーを選択します。"

一致キーは、様々なデータソースのオーディエンス間でメンバーを紐付けるために使用される識別子です。データ接続用に最初に選択した一致キーは編集できません。

使用可能な一致キーは次のとおりです。

- **ハッシュ化されたメール**

![ 「キーを一致させる」セクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png){zoomable="yes"}

### スケジュール設定 {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="スケジュール設定"
>abstract="このビューには、データ接続に対して最初に選択したスケジュール設定オプションが表示されます。"

データ接続に最初に選択したスケジュール オプションは編集できません。 スケジュールオプションについて詳しくは、オーディエンスの読み込みワークフロードキュメントの [ スケジュールセクション ](/help/guide/setup/onboard-audiences.md#schedule) を参照してください。

![ 「スケジュール」セクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png){zoomable="yes"}

## データ接続を削除

データ接続を削除すると、基になるオーディエンス、関連する設定およびプラットフォーム全体での使用状況がすべて削除されます。 このアクションは取り消せません。

既存のデータ接続を削除するには、個々のデータ接続のワークスペース内にある削除アイコン（![ 削除アイコン ](/help/assets/common/delete.svg)）を選択します。

![ 削除オプションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/delete-data-connection.png){zoomable="yes"}

確認ダイアログが表示されます。 **[!UICONTROL 削除]** を選択して、データ接続の削除を終了します。

![ 「削除」オプションがハイライト表示されたデータ接続を削除ダイアログ ](/help/assets/setup/manage-data-connection/delete-data-connection-confirm.png){zoomable="yes"}

## オーディエンス管理 {#manage-audiences}

データ接続に接続されているオーディエンスのリストが、ワークスペースの下部に表示されます。 リストには、ステータス、ソース、接続アクセスなど、各オーディエンスの簡単な概要が表示されます。 オーディエンスのカテゴリ、接続アクセスまたはメタデータ表示を編集するには、オーディエンスの名前を選択します。 オーディエンスの管理に関する完全なガイドについては、[ 個々のオーディエンスの表示 ](./onboard-audiences.md#view-individual-audiences) ガイドを参照してください。

![ オーディエンスがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png){zoomable="yes"}

## 次の手順

データ接続を管理すると、共同作業者が検出可能にしたオーディエンスとオーディエンスの間で [ 重複を検出 ](/help/guide/collaborate/discover.md) できます。
