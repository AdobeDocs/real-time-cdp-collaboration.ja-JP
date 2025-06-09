---
title: 重複の検出とオーディエンスの比較
description: 自分と共同作業者のオーディエンスの重複を見つけます。 キャンペーンで使用する最適なオーディエンスを見つける方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 11%

---

# 重複の検出とオーディエンスの比較

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL 検出]** ワークスペースは、**オーディエンス検出** ユースケースが [ 接続処理中に ](../connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

[ プロジェクトの作成 ](/help/guide/collaborate/manage-projects.md) 後、オーディエンスを共同作業者と比較できます。 これは、キャンペーンに関連するオーディエンスを特定し、アクティベーション用にパブリッシャーに送信するオーディエンスを決定するのに役立ちます。

>[!IMPORTANT]
>
>更新または更新されていない [ データスケッチ ](/help/guide/glossary.md#sketches) は、7 日後に削除されます。 これが発生すると、このページの様々な重複レポートに表示される数値がゼロになり、これらの有効期限切れのオーディエンスに対するオーディエンス共有が使用できなくなります。 データスケッチは、[ アクティブな更新スケジュール ](/help/guide/setup/onboard-audiences.md#schedule) を使用したオーディエンスに対して自動的に更新されます。

オーディエンスの検出と比較に使用する一致キーは、[ 接続プロセス中 ](/help/guide/connect/establishing-connections.md#connection-settings) に設定されます。 一致キーは、オーディエンス間の重複の計算に使用され、オンとオフを切り替えることができます。 一致キーを編集するには、「**[!UICONTROL 一致キーを編集]** オプションを選択します。 この

![ オーディエンスインサイトを表示する、「ダイコバー」タブワークスペース。](/help/assets/collaborate/discover/discover-overview.png)

**[!UICONTROL マッチキーを編集]** ダイアログが開き、使用しないマッチキーを切り替えることができます。 「**[!UICONTROL 保存]**」を選択して変更を保存します。

![Discover ワークスペースの一致するキーを編集ダイアログ ](/help/assets/collaborate/discover/edit-match-keys.png)

## 前提条件 {#prerequisites}

プロジェクト内で「**[!UICONTROL 検出]**」タブを使用するには、次のものが必要です。

* 組織への [ 読み込まれたオーディエンス ](/help/guide/setup/onboard-audiences.md)
* [ オーディエンス検出 ](/help/guide/connect/establishing-connections.md) ユースケースが有効になっている共同作業者で **接続**
* 自分と共同作業者の間で [ プロジェクトが作成されました ](/help/guide/collaborate/manage-projects.md)

これらの前提条件が満たされたら、自分と共同作業者のオーディエンスの重複を調査および比較できます。

## オーディエンスの比較 {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="オーディエンスの比較"
>abstract="ユーザーと共同作業者のオーディエンスの重複を検出します。ドロップダウンセレクターの設定を調整すると、共同作業者の 1 つ以上のオーディエンスに対する 1 つ以上のオーディエンスの重複を検出できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づいて、選択したオーディエンス内の一意の ID の数。"
>
>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="共同作業者 ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づいて、共同作業者のオーディエンス内の一意の ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="重複 ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づいて、ユーザーと共同作業者のオーディエンスの両方に存在する一意の ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="重複 ID の割合"
>abstract="自分と共同作業者が選択したオーディエンスの間で重複する ID の割合。"

「オーディエンスを比較」セクションを使用すると、と共同作業者のオーディエンスの重複に関する豊富な情報を取得できます。 オーディエンスの選択を変更するには、「**[!UICONTROL オーディエンスを比較]** セクションの上部にあるドロップダウンセレクターを使用します。 オーディエンスの 1 つまたはすべてを選択し、共同作業者のオーディエンスの 1 つまたはすべてを選択して、相互に比較できます。

![ 「オーディエンスを比較」セクションでハイライト表示されたオーディエンスセレクターを含む検出ワークスペース。](/help/assets/collaborate/discover/compare-audiences-selector.png)

「オーディエンスを比較」セクションには、自分と共同作業者がプロジェクトで合意した一致キーに基づく次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID 数]** （自分の ID） | 選択したオーディエンス内の一意の ID の数。 |
| **[!UICONTROL ID 数]** （共同作業者） | 共同作業者のオーディエンス内の一意の ID の数。 |
| **[!UICONTROL 重複する ID]** | ユーザーと共同作業者のオーディエンスの両方に存在する一意の ID の数。 |
| **[!UICONTROL 重複 %]** | ユーザーと共同作業者の選択したオーディエンス間でプロファイルが重複している割合。 |
| **[!UICONTROL 一致キーによる ID の分類]** | プロジェクトで選択した各一致キーの ID の分類。各共同作業者の選択オーディエンスに基づきます。 |

{style="table-layout:auto"}

>[!TIP]
>
>重複率の数値は、必ずしもすべてのオーディエンスで使用できるとは限りません。 重複率インジケーターの表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。

## 関連するオーディエンス {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="関連するオーディエンス"
>abstract="重複の割合に基づくと、これらの媒体社オーディエンスがキャンペーンに適している可能性があります。<br><br><b>ID 数</b>は、媒体社のオーディエンスサイズです。<br><br> <b>重複 ID</b> は、推奨される媒体社オーディエンスとすべての広告主オーディエンス間の重複を表します。<br><br><b>重複％</b>は、重複する ID の数を<i>すべて</i>の広告主オーディエンスのサイズで割った値を表します。"

**[!UICONTROL 検出]** タブの **[!UICONTROL 関連オーディエンス]** セクションには、共同作業者のオーディエンスとすべてのオーディエンスの重複率に基づいて、上位 5 つのオーディエンスのキュレートされたリストが表示されます。 この機能を使用すると、重複度が最も高いオーディエンスをすばやく特定でき、キャンペーンをより効果的にターゲット設定できるようになります。 セクションの右上にあるページセレクターを使用して、関連するオーディエンスを切り替えます。

![ 関連するオーディエンスのセクションがハイライト表示された Discover ワークスペース。](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>共同作業者のオーディエンスの表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。 共同作業者がすべてのオーディエンスをプライベートに設定している場合、このセクションにはオーディエンスが表示されません。

**[!UICONTROL 関連するオーディエンス]** セクションには、推奨される各オーディエンスに関する次の情報が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID 数]** | オーディエンス内の一意の ID の名前。 |
| **[!UICONTROL 重複する ID]** | 推奨オーディエンスとすべてのオーディエンスの間で重複する一意の ID の数。 |
| **[!UICONTROL 重複 %]** | 推奨オーディエンスとすべてのオーディエンスの間で重複する ID の割合。 |
| **[!UICONTROL オーディエンスのカテゴリ]** | 共同作業者がオーディエンスに割り当てたカテゴリ。 |
| **[!UICONTROL 一致キー]** | 共同作業者がオーディエンス用に選択した一致するキー。 |

{style="table-layout:auto"}

>[!NOTE]
>
>共同作業者のオーディエンスの表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。 共同作業者がすべてのオーディエンスをプライベートに設定している場合、このセクションにはオーディエンスが表示されません。

## 重複の検出 {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="個々のオーディエンスとの重複の検出"
>abstract="オーディエンスと共同作業者のオーディエンスの重複に関するインサイトを取得します。"

重複を検出して、オーディエンスを共同作業者のオーディエンスと比較する方法に関するインサイトを得ます。 デフォルトでは、このセクションは、すべてのオーディエンスを共同作業者の各オーディエンスと比較します。 セクションの下部にあるページネーションコントロールを使用して、使用可能なオーディエンス間を移動します。

![ 「重複を検出」セクションがハイライト表示された検出ワークスペース。](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>共同作業者のオーディエンスの表示は、共同作業者が [ メタデータの表示セクション ](/help/guide/setup/onboard-audiences.md#metadata-visibility) でオーディエンスに対して選択した設定によって異なります。 共同作業者がすべてのオーディエンスをプライベートに設定している場合、このセクションにはオーディエンスが表示されません。

オーディエンスの選択を変更するには、「**[!UICONTROL オーディエンスを変更]**」を選択します。

![ 「オーディエンスを変更」オプションがハイライト表示された Discover ワークスペース。](/help/assets/collaborate/discover/change-audience.png)

**[!UICONTROL オーディエンスを変更]** ダイアログが開き、特定のオーディエンスを使用して共同作業者のオーディエンスと比較できます。 目的のオーディエンスを選択するか、選択を解除してすべてのオーディエンスを選択してから、「**[!UICONTROL 保存]**」を選択します。

![Discover ワークスペースのオーディエンスを変更ダイアログ。](/help/assets/collaborate/discover/change-audience-selection.png)

目的のオーディエンスを選択すると、「**[!UICONTROL 重複を検出]**」セクションにオーディエンスごとに次の情報が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID 数]** | オーディエンス内の一意の ID の名前。 |
| **[!UICONTROL 重複する ID]** | 推奨オーディエンスとすべてのオーディエンスの間で重複する一意の ID の数。 |
| **[!UICONTROL 重複 %]** | 推奨オーディエンスとすべてのオーディエンスの間で重複する ID の割合。 |
| **[!UICONTROL オーディエンスのカテゴリ]** | 共同作業者がオーディエンスに割り当てたカテゴリ。 |
| **[!UICONTROL 一致キー]** | 共同作業者がオーディエンス用に選択した一致するキー。 |

{style="table-layout:auto"}

## 次の手順

目的のオーディエンスを探索して検出したら、キャンペーンで使用するオーディエンスを [ アクティブ化 ](/help/guide/collaborate/activate.md) します。
