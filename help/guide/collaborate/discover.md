---
title: 重複の検出とオーディエンスの比較
description: 自分と共同作業者のオーディエンスの重複を見つけます。 キャンペーンで使用する最適なオーディエンスを見つける方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 24%

---

# 重複の検出とオーディエンスの比較

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL 検出]** ワークスペースは、**オーディエンス検出** ユースケースが [ 接続処理中に ](../connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

広告主とパブリッシャーの共同作業スペース内で [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md) した後、オーディエンスを共同作業者のオーディエンスと比較できるようになりました。 これにより、オーディエンス間の重複を検出し、一致するキーや ID 別に分類されたインサイトを取得できます。 これにより、広告主は、アクティベーションのためにパブリッシャーと共有するオーディエンスを決定できます。

>[!IMPORTANT]
>
>更新または更新されていない [ データスケッチ ](/help/guide/glossary.md#sketches) は、7 日後に削除されます。 これが発生すると、このページの様々な重複レポートに表示される数値がゼロになり、これらの有効期限切れのオーディエンスに対するオーディエンス共有が使用できなくなります。 データスケッチは、[ アクティブな更新スケジュール ](/help/guide/setup/onboard-audiences.md#schedule) を使用したオーディエンスに対して自動的に更新されます。

![ 重複を検出 ](/help/assets/collaborate/discover-overlaps/discover-overlaps.png)

オーディエンスの検出と比較に使用する一致キーは、（パブリッシャーと接続 [ 時に設定され ](/help/guide/connect/establishing-connections.md#connection-settings) す。 キャンペーンを実行するための準備として示された重複率を変更するには、一致キーを削除できますが、この時点では新しい一致キーを追加できません。 それには、共同作業者の間の [ 接続設定 ](/help/guide/connect/establishing-connections.md#connection-settings) に移動します。

![ 一致キーを編集画面 ](/help/assets/collaborate/discover-overlaps/edit-match-keys.png)

## 前提条件 {#prerequisites}

**[!UICONTROL Collaborate]** ワークフローの「**[!UICONTROL Discover]**」タブの機能を最大限に活用するために、以下は既に達成されています。

* [インポートされたオーディエンス](/help/guide/setup/onboard-audiences.md)
* [ オーディエンス検出 ](/help/guide/connect/establishing-connections.md) ユースケースが有効な、目的の広告主またはパブリッシャーとの **接続**
* 自分と共同作業者の間で [ プロジェクトが作成されました ](/help/guide/collaborate/manage-projects.md)

上記の前提条件が満たされたら、自分のオーディエンスと共同作業者のオーディエンスの重複を調査し、比較することができます。

## オーディエンスの比較 {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="オーディエンスの比較"
>abstract="ユーザーと共同作業者のオーディエンスの重複を検出します。ドロップダウンセレクターの設定を調整すると、共同作業者の 1 つ以上のオーディエンスに対する 1 つ以上のオーディエンスの重複を検出できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="ID 数"
>abstract="選択したオーディエンスに含まれる、選択した ID を持つプロファイルの数"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="共同作業者 ID 数"
>abstract="共同作業者の選択したオーディエンスに含まれる、選択した ID を持つプロファイルの数"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="重複 ID 数"
>abstract="ユーザーと共同作業者のオーディエンスの両方に存在する、選択した ID を持つプロファイルの数"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="重複 ID の割合"
>abstract="ユーザーと共同作業者の選択したオーディエンス間でプロファイルが重複している割合。"

オーディエンスの比較カードを使用して、と共同作業者のオーディエンスの重複に関する豊富な情報を取得します。 次のオーディエンスの組み合わせのいずれかを選択して比較できます。

* 共同作業者のオーディエンスの 1 つに対するオーディエンスの 1 つ
* 共同作業者のすべてのオーディエンスに対するオーディエンスの 1 つ
* 共同作業者のオーディエンスの 1 つに対するすべてのオーディエンス
* 共同作業者のすべてのオーディエンスに対するすべてのオーディエンス

表示される情報は以下に関連しています。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID 数]** （自分の ID） | 選択したオーディエンスに含まれる、選択した ID を持つプロファイルの数。 |
| **[!UICONTROL ID 数]** （共同作業者） | 共同作業者が選択したオーディエンスに含まれる、選択した ID を持つプロファイルの数。 |
| **[!UICONTROL 重複する ID]** | ユーザーと共同作業者のオーディエンスの両方に存在する、選択した ID を持つプロファイルの数。 |
| **[!UICONTROL 重複率]** | ユーザーと共同作業者の選択したオーディエンス間でプロファイルが重複している割合。 |
| **[!UICONTROL 一致キーによる ID の分類]** | ユーザーと共同作業者がプロジェクトで合意した一致キーに基づいて、個々の一致キーによる重複計算で ID の構成を表示します。 |

{style="table-layout:auto"}

>[!TIP]
>
>重複率の数値は、必ずしもすべてのオーディエンスで使用できるとは限りません。 重複率インジケーターの表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。

## 関連するオーディエンス {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="関連するオーディエンス"
>abstract="重複の割合に基づくと、これらの媒体社オーディエンスがキャンペーンに適している可能性があります。<br><br><b>ID 数</b>は、媒体社のオーディエンスサイズです。<br><br> <b>重複 ID</b> は、推奨される媒体社オーディエンスとすべての広告主オーディエンス間の重複を表します。<br><br><b>重複％</b>は、重複する ID の数を<i>すべて</i>の広告主オーディエンスのサイズで割った値を表します。"

**[!UICONTROL 検出]** モジュールの **[!UICONTROL 関連オーディエンス]** ビューには、重複率に基づいて、上位 5 つのオーディエンスのキュレートされたリストが表示されます。 この機能を使用すると、現在のデータと最も重複しているオーディエンスをすばやく特定できるので、キャンペーンをより効果的にターゲット設定できます。

* **[!UICONTROL ID 数]** は、パブリッシャーのオーディエンスサイズです。
* **[!UICONTROL 重複する ID]** は、推奨される公開者オーディエンスとすべての広告主オーディエンスの重複を表します。
* **[!UICONTROL 重複 %]** は、重複する ID の数を広告主オーディエンスの *すべて* サイズで割った値を表します。

![ 関連オーディエンス表示 ](/help/assets/collaborate/discover-overlaps/relevant-audiences-highlighted.png)

## 重複の検出 {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="個々のオーディエンスとの重複の検出"
>abstract="このオーディエンスの母集団と、その共同作業者の ID の集合体との重複に関するインサイトを取得します。"

![ 異なるオーディエンスビューとの重複を検出 ](/help/assets/collaborate/discover-overlaps/discover-overlaps-cards-view.png)

共同作業者のオーディエンスに関する詳細な情報を取得し、すべてのオーディエンスの母集団全体の数または特定のオーディエンスに対してこれらのオーディエンスを比較する重複情報を表示します。

>[!TIP]
>
>スクリーンショットに示されている数値の一部は、すべてのオーディエンスで常に使用できるとは限らない場合があります。 表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。

## 次の手順

目的のオーディエンスを探索して発見したら、パブリッシャーとキャンペーンで使用する必要があるオーディエンスを [ 共有 ](/help/guide/collaborate/share.md) します。
