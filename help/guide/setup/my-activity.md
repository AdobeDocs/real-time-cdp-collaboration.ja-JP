---
title: クレジット消費アクティビティの追跡
description: Real-Time CDP Collaborationで組織のクレジット使用状況を追跡する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
source-git-commit: 4fc9b4e814f7392e1dfdb5847b7189d7d6e21702
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 7%

---

# クレジット消費アクティビティの追跡 {#track-credit-consumption-activity}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_my_activity"
>title="詳細情報"
>abstract=""

{{limited-availability-release-note}}

>[!BEGINSHADEBOX]

**90日間の無料期間**：対象地域のお客様は、地域の利用可能日から90日間の無料期間が適用されます。 この間、顧客は、クレジットの使用権限を超えた場合、超過料金は発生しません。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>クレジット消費テーブルは切り上げられ、監視のために日別に集計されます。 **[!UICONTROL My Activity]** ダッシュボードの数値は、*推定* クレジット消費量を表しています。 請求に使用された&#x200B;*実際の* クレジット消費量は、社内システムで追跡され、リクエストに応じて利用できます。 Adobeの担当者にお問い合わせください。

予測クレジット消費アクティビティにアクセスするには、メインナビゲーションの&#x200B;**[!UICONTROL 設定]**&#x200B;に移動し、**[!UICONTROL マイアクティビティ]** タブを選択します。

クレジット消費の詳細を表示する![ マイアクティビティダッシュボード ](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>**[!UICONTROL 自分のアクティビティ]** ビューには、Collaboration ユーザーインターフェイスの別の部分でのユーザーアクションに関する情報が含まれていません。 [監査ログ ](/help/guide/setup/audit-logs.md)機能を使用して、その情報を取得します。

## アクティビティダッシュボードについて {#understand-dashboard}

アクティビティダッシュボードには、アカウント内のすべてのクレジット消費操作の包括的なリストが表示されます。 各行は明確なアクティビティを表し、クレジットの使用に関する重要な情報を提供します。

>[!NOTE]
>
>**[!UICONTROL オーディエンス管理]** アクティビティは別の共同作業者に関連付けられていないので、これらのアクティビティタイプの&#x200B;**[!UICONTROL 接続ID]**&#x200B;と&#x200B;**[!UICONTROL 接続名]**&#x200B;列は&#x200B;**[!UICONTROL ～]**&#x200B;の値を示しています。

| 列 | 説明 |
|------------|--------------|
| **[!UICONTROL 日付]** | アクティビティが発生した日付。MM/DD/YYYY形式で表示されます。 |
| **[!UICONTROL 接続ID]** | クレジット消費アクティビティに関連付けられた各接続の一意の識別子（英数字の文字列で表されます）。 |
| **[!UICONTROL 接続名]** | 接続とクレジット消費アクティビティに関連付けられている共同作業者の名前。 |
| **[!UICONTROL アクティビティ]** | 実行されたアクティビティのタイプ（**Activation - Matching**、**Activation - Egress**、**Audience Management**&#x200B;など）。 |
| **[!UICONTROL 入力が処理されました]** | アクティビティで処理された入力（IDや行など）の合計数。 |
| **[!UICONTROL 合計クレジット使用済み]** | アクティビティで消費されたクレジットの合計数です。 |
| **[!UICONTROL 自分のクレジット共有]** | アクティビティに使用されたクレジットのアカウントの部分。 |

{style="table-layout:auto"}

## アクティビティの種類 {#types-of-activities}

**[!UICONTROL アクティビティ]**&#x200B;列には、クレジットを消費する操作の種類が表示されます。

* **[!UICONTROL Audience Management]**: オーディエンスがCollaborationに送信されると、クレジットが消費されます。 クレジットは、すべてのオーディエンスに対してCollaboration内でインデックス作成されるIDの数（数百万単位）と、そのインデックス作成の頻度（毎日、3日ごと、または毎週）の関数として消費されます。 詳しくは、[ オーディエンスの取得と管理](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。
* **[!UICONTROL アクティベーション – 一致]** - クレジットは、一致し、アクティベーション用に準備されたIDの数の関数として消費されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL アクティベーション – エグレス]** - クレジットは、ID数の関数として消費され、宛先に送信されます。 これは常に、オーディエンスを受信する共同作業者に課金されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL Measurement]** - Collaborationでアクティビティを実行して、キャンペーンパフォーマンスレポートとインサイトを生成します。 クレジットは、すべてのキャンペーンのキャンペーンレポートの行数とレポートの頻度（毎日、3 日ごと、または週ごと）に基づいて消費されます。

## クレジット消費量の管理 {#manage-credit-consumption}

クレジット消費を効果的に管理するには：

1. **各アクティビティに関連するクレジット消費量を**&#x200B;理解します。 アクティビティごとに使用されるクレジットの表については、[Collaboration製品の説明](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank}を確認してください。
2. **定期的に監視**：使用状況パターンを理解するために、アクティビティ ダッシュボードを頻繁に確認します。
3. **接続で追跡**：接続名を使用して、最もクレジットを消費している接続を特定します。
