---
title: クレジット消費アクティビティの追跡
description: 組織のクレジット消費アクティビティをReal-Time CDP Collaborationでトラッキングする方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 4fc9b4e814f7392e1dfdb5847b7189d7d6e21702
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 6%

---

# クレジット消費アクティビティの追跡 {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="詳細情報"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**90 日間の超過期間**：適格な地域のお客様は、その地域で利用可能な日から始まる 90 日間の超過期間の対象外となります。 この間、顧客は、クレジットの使用権限を超過した場合に超過手数料を負担しません。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>与信消費表は日別に切り上げられ、集計されてモニタリングされます。 **[!UICONTROL マイアクティビティ]** ダッシュボード内の数値は、*推定* クレジット消費を表しています。 請求に使用される *実際* のクレジット消費は、内部システムで追跡され、リクエストに応じて利用できます。 その情報を入手するには、Adobe担当者にお問い合わせください。

推定クレジット消費アクティビティにアクセスするには、メインナビゲーションで **[!UICONTROL 設定]** に移動し、「**[!UICONTROL マイアクティビティ]**」タブを選択します。

![ クレジット消費の詳細を表示するマイアクティビティダッシュボード ](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>**[!UICONTROL マイアクティビティ]** ビューには、Collaboration ユーザーインターフェイスの様々な部分におけるユーザーアクションに関する情報は含まれません。 [ 監査ログ ](/help/guide/setup/audit-logs.md) 機能を使用して、その情報を取得します。

## アクティビティダッシュボードについて {#understand-dashboard}

アクティビティダッシュボードには、アカウント内のすべてのクレジットを消費する操作の包括的なリストが表示されます。 各行は個別のアクティビティを表し、クレジット使用状況に関する主要な情報を提供します。

>[!NOTE]
>
>**[!UICONTROL Audience Management]** アクティビティは別の共同作業者に関連付けられていないので、これらのアクティビティタイプの **[!UICONTROL 接続 ID]** と **[!UICONTROL 接続名]** の列は、**[!UICONTROL -]** 値を示しています。

| 列 | 説明 |
|------------|--------------|
| **[!UICONTROL 日付]** | アクティビティが発生した日付（MM/DD/YYYY 形式で表示）。 |
| **[!UICONTROL 接続 ID]** | クレジットを消費するアクティビティに関連付けられた各接続の一意の ID。英数字の文字列で表されます。 |
| **[!UICONTROL 接続名]** | 接続とクレジットを消費するアクティビティに関連付けられた共同作業者の名前。 |
| **[!UICONTROL アクティビティ]** | 実行されたアクティビティのタイプ。例えば、**アクティベーション – マッチング**、**アクティベーション – エグレス**、**Audience Management** などです。 |
| **[!UICONTROL 処理済みの入力]** | アクティビティに対して処理された入力（ID や行など）の合計数。 |
| **[!UICONTROL 使用したクレジットの合計]** | アクティビティによって消費されたクレジットの合計数。 |
| **[!UICONTROL マイクレジットシェア]** | アクティビティに使用されるクレジットのうち、アカウントの部分。 |

{style="table-layout:auto"}

## アクティビティのタイプ {#types-of-activities}

**[!UICONTROL アクティビティ]** 列には、様々なタイプのクレジット消費操作が表示されます。

* **[!UICONTROL Audience Management]**：クレジットは、オーディエンスがCollaborationをソースとする際に使用されます。 クレジットは、すべてのオーディエンスにわたってCollaboration内でインデックス作成された ID の数（百万単位）と、そのインデックス作成の頻度（毎日、3 日ごと、または毎週）の関数として使用されます。 詳しくは、[ オーディエンスのソーシングと管理 ](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。
* **[!UICONTROL アクティベーション – 一致]** - クレジットは、アクティベーション用に一致して準備された ID の数の関数として消費されます。 詳しくは、[ オーディエンスのアクティブ化 ](/help/guide/collaborate/activate.md) ガイドを参照してください。
* **[!UICONTROL アクティベーション – 出力]** - クレジットは、ID 数の関数として宛先に送信される。 これは常に、オーディエンスを受け取った共同作業者に請求されます。 詳しくは、[ オーディエンスのアクティブ化 ](/help/guide/collaborate/activate.md) ガイドを参照してください。
* **[!UICONTROL 測定]** - Collaborationでアクティビティを実行して、キャンペーンのパフォーマンスレポートとインサイトを生成します。 クレジットは、すべてのキャンペーンのキャンペーンレポートの行数とレポートの頻度（毎日、3 日ごと、または週ごと）に基づいて消費されます。

## クレジット消費の管理 {#manage-credit-consumption}

クレジット消費を効果的に管理する手順は、次のとおりです。

1. **理解** 各アクティビティに関連付けられた与信消費。 アクティビティごとに使用されるクレジットのテーブルについては [0}Collaborationの製品説明 } を確認してください。](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank}
2. **定期的な監視**：アクティビティダッシュボードを頻繁に確認して、使用パターンを把握します。
3. **接続別に追跡**：接続名を使用して、最もクレジットを消費している接続を特定します。
