---
title: クレジット消費アクティビティの追跡
description: 組織のクレジット消費アクティビティをReal-Time CDP Collaborationでトラッキングする方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 3aec9806d2ea920d656bb0981f22ba31fd8ae3ee
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# クレジット消費アクティビティの追跡

{{limited-availability-release-note}}

**[!UICONTROL マイアクティビティ]** タブを使用して、すべてのコラボレーションアクティビティにわたる組織の推定クレジット消費を監視および追跡します。 この機能は、様々な接続やアクティビティでクレジットがどのように使用されているかに関する詳細なインサイトを提供し、リソースの効果的な管理を支援します。

>[!IMPORTANT]
>
>与信消費表は日別に切り上げられ、集計されてモニタリングされます。 **[!UICONTROL マイアクティビティ]** ダッシュボード内の数値は、*推定* クレジット消費を表しています。 請求に使用される *実際* のクレジット消費は、内部システムで追跡され、リクエストに応じて利用できます。 その情報を入手するには、Adobe担当者にお問い合わせください。

推定クレジット消費アクティビティにアクセスするには、メインナビゲーションで **[!UICONTROL 設定]** に移動し、「**[!UICONTROL マイアクティビティ]**」タブを選択します。

![ クレジット消費の詳細を表示するマイアクティビティダッシュボード ](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>**[!UICONTROL マイアクティビティ]** ビューには、Real-Time Collaboration CDP ユーザーインターフェイスの様々な部分におけるユーザーアクションに関する情報は含まれません。 [ 監査ログ ](/help/guide/setup/audit-logs.md) 機能を使用して、その情報を取得します。

## アクティビティダッシュボードについて {#understand-dashboard}

アクティビティダッシュボードには、組織内のすべてのクレジットを消費する操作の包括的なリストが表示されます。 各行は個別のアクティビティを表し、クレジット使用状況に関する主要な情報を提供します。

>[!NOTE]
>
>**[!UICONTROL Audience Management]** アクティビティは別の共同作業者に関連付けられていないので、これらのアクティビティタイプの **[!UICONTROL 接続 ID]** と **[!UICONTROL 接続名]** の列は、**[!UICONTROL N/A]** 値を示します。

| 列 | 説明 |
|------------|--------------|
| **[!UICONTROL 日付]** | アクティビティが発生した日付（MM/DD/YYYY 形式で表示）。 |
| **[!UICONTROL 接続 ID]** | クレジットを消費するアクティビティに関連付けられた各接続の一意の ID。英数字の文字列で表されます。 |
| **[!UICONTROL 接続名]** | 接続とクレジットを消費するアクティビティに関連付けられた共同作業者の名前。 |
| **[!UICONTROL アクティビティ]** | 実行されたアクティビティのタイプ（**アクティベーション – 共有**、**アクティベーション – 出力**、**Audience Management** など）。 |
| **[!UICONTROL 処理済みの入力]** | アクティビティに対して処理された入力（ID や行など）の合計数。 |
| **[!UICONTROL 使用したクレジットの合計]** | アクティビティによって消費されたクレジットの合計数。 |
| **[!UICONTROL マイクレジットシェア]** | アクティビティに使用されるクレジットのうち、組織の部分。 |

{style="table-layout:auto"}

## アクティビティのタイプ {#types-of-activities}

**[!UICONTROL アクティビティ]** 列には、様々なタイプのクレジット消費操作が表示されます。

* **[!UICONTROL Audience Management]**：クレジットは、オーディエンスがReal-Time CDP Collaborationに読み込まれる際に使用されます。 クレジットは、すべてのオーディエンスにわたってReal-Time CDP Collaboration内でインデックス作成された ID の数（百万単位）と、請求期間中のそのインデックス作成の頻度（毎日、3 日ごと、または毎週）の関数として使用されます。 詳しくは、[ オーディエンスのインポートと管理 ](/help/guide/setup/onboard-audiences.md) を参照してください。
* **[!UICONTROL 有効化 – 共有]** - クレジットは、請求期間中にReal-Time CDP Collaborationから有効化された ID の数の関数として消費されます。 詳しくは、Real-Time CDP Collaborationでの [ 共有 ](/help/guide/collaborate/share.md) および [ オーディエンスのアクティブ化 ](/help/guide/collaborate/activate.md) を参照してください。
* **[!UICONTROL 有効化 – 出力]** - クレジットは、請求期間中にReal-Time CDP Collaborationから有効化された ID の数の関数として消費されます。 詳しくは、Real-Time CDP Collaborationでの [ 共有 ](/help/guide/collaborate/share.md) および [ オーディエンスのアクティブ化 ](/help/guide/collaborate/activate.md) を参照してください。
* **[!UICONTROL オーディエンスの重複]** - クレジットは、データのスケッチを使用してオーディエンスの重複を分析する際に使用されます。 データスケッチは、オーディエンスデータの要約を簡略化したもので、データのプライバシーを維持しながら 2 つのオーディエンスの類似度を判断するのに役立ちます。 詳しくは、[ 「検出」タブでのオーディエンスの重複 ](/help/guide/collaborate/discover.md) を参照してください。
* **[!UICONTROL Audience Measurement]** - Real-Time CDP Collaborationでアクティビティを実行して、キャンペーンのパフォーマンスレポートとインサイトを生成します。 クレジットは、すべてのキャンペーンのキャンペーンレポートの行数とレポートの頻度（日別、3 日別または週別）に基づいて消費されます。


<!--

**[!UICONTROL Audience Overlaps]** – Credits are consumed as a function of the number of matched IDs across 2 or more shared audiences throughout the billing period. Read more about [audience overlaps in the discover tab](/help/guide/collaborate/discover.md).

Collaboration Measurement – Credits are consumed as a function of the number of rows existing in campaign reports across all campaigns, and the frequency of that reporting (daily, every three days, or weekly).

-->


## クレジット消費の管理 {#manage-credit-consumption}

クレジット消費を効果的に管理する手順は、次のとおりです。

1. **理解** 各アクティビティに関連付けられたクレジット消費。 アクティビティごとに使用されるコラボレーションクレジットのテーブルについては [&#128279;](https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank}0&rbrace;Real-Time CDP Collaborationの製品説明 &rbrace; を確認してください。
2. **定期的な監視**：アクティビティダッシュボードを頻繁に確認して、使用パターンを把握します。
3. **接続別に追跡**：接続名を使用して、最もクレジットを消費しているパートナーシップを特定します。

<!--

## Pagination and navigation

The activity list is paginated to improve performance and readability. Use the navigation controls at the bottom of the table to move between pages and adjust how many records you can view at once.

-->
