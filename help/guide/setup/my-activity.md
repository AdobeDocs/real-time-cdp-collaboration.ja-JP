---
title: クレジット消費アクティビティの追跡
description: Real-Time CDP Collaborationで組織のクレジットウォレットを表示し、クレジット使用状況を追跡する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b24d63e7-60f4-4cdb-ab1b-77c284543486
TQID: https://experienceleague.adobe.com/hDvkKFUCBYvsX8wntcYFrL6qZTxOo5CZOWAbxNwk7mw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 681f4af47a58a2ce66b25b09d793d0b5b127df39
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 2%

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

クレジットウォレットとクレジット消費アクティビティにアクセスするには、メインナビゲーションの&#x200B;**[!UICONTROL 設定]**&#x200B;に移動し、**[!UICONTROL マイアクティビティ]** タブを選択します。

![ クレジットがプロビジョニングされたクレジットウォレット、クレジットが消費されたクレジット、利用可能なクレジット、およびクレジット消費アクティビティテーブルが表示された「マイアクティビティ」タブ。](/help/assets/setup/my-activity-credits/activity-dashboard.png)

>[!TIP]
>
>**[!UICONTROL 自分のアクティビティ]** ビューには、Real-Time CDP Collaboration インターフェイスの他の領域からのユーザーアクションは含まれていません。 [監査ログ ](/help/guide/setup/audit-logs.md)機能を使用して、その情報を取得します。

## マイアクティビティビューについて {#understand-dashboard}

**[!UICONTROL マイアクティビティ]** ビューを使用して、クレジットの使用状況を監視し、クレジットを消費するアクティビティを確認します。 このビューには、クレジットウォレットとアクティビティテーブルが含まれます。

クレジットウォレットには、プロビジョニングされたクレジット、消費されたクレジット、利用可能なクレジットが表示されます。

| 指標 | 説明 |
|---------|-------------|
| **[!UICONTROL クレジットがプロビジョニングされました]** | アカウントにプロビジョニングされたクレジットの数。 |
| **[!UICONTROL クレジットが消費されました]** | 最新の1日の更新時にアカウントが消費したクレジットの数。 |
| **[!UICONTROL 利用可能なクレジット]** | プロビジョニングされたクレジットから消費されたクレジットを差し引いて計算した、アカウントで利用可能なクレジットの数。 |

{style="table-layout:auto"}

アクティビティ テーブルには、日付、アクティビティ タイプ、処理済み入力、使用されたクレジット別の1日のクレジット消費レコードが一覧表示されます。

>[!NOTE]
>
>**[!UICONTROL オーディエンス管理]** アクティビティは別の共同作業者に関連付けられていないので、これらのアクティビティタイプの&#x200B;**[!UICONTROL 接続ID]**&#x200B;と&#x200B;**[!UICONTROL 接続名]**&#x200B;列には&#x200B;**[!UICONTROL ～]**&#x200B;の値が表示されます。

| 列 | 説明 |
|------------|--------------|
| **[!UICONTROL 日付]** | アクティビティが発生した日付。MM/DD/YYYY形式で表示されます。 |
| **[!UICONTROL 接続ID]** | クレジット消費アクティビティに関連付けられた各接続の一意の識別子（英数字の文字列で表されます）。 |
| **[!UICONTROL 接続名]** | 接続とクレジット消費アクティビティに関連付けられている共同作業者の名前。 |
| **[!UICONTROL アクティビティ]** | 実行されたアクティビティのタイプ。例：**[!UICONTROL アクティベーション – オーディエンスアクセス （1回）]**、**[!UICONTROL アクティベーション – オーディエンスアクセス （繰り返し）]**、**[!UICONTROL アクティベーション – オーディエンスエグレス （1回）]**、**[!UICONTROL アクティベーション – オーディエンスエグレス （繰り返し）]**、または&#x200B;**[!UICONTROL オーディエンス管理]**。 |
| **[!UICONTROL 入力が処理されました]** | アクティビティで処理された入力（IDや行など）の合計数。 |
| **[!UICONTROL 合計クレジット使用済み]** | アクティビティで消費されたクレジットの合計。 |
| **[!UICONTROL 自分のクレジット共有]** | アクティビティに使用されたクレジットのアカウントの部分。 |

{style="table-layout:auto"}

## アクティビティの種類 {#types-of-activities}

**[!UICONTROL アクティビティ]**&#x200B;列には、クレジットを消費する操作の種類が表示されます。

* **[!UICONTROL Audience Management]**: オーディエンスがCollaborationに送信されると、クレジットが消費されます。 クレジットは、すべてのオーディエンスに対してCollaboration内でインデックス作成されるIDの数と、そのインデックス作成の頻度（毎日、3日ごと、毎週など）の関数として消費されます。 詳しくは、[ オーディエンスの取得と管理](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。
* **[!UICONTROL アクティベーション – オーディエンスアクセス （1回）]**: アクティベーションワークフローを通じてオーディエンスアクセスが1回処理されると、クレジットが消費されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL アクティベーション – オーディエンスアクセス （繰り返し）]**: アクティベーションワークフローを通じて繰り返しスケジュールでオーディエンスアクセスが処理されると、クレジットが消費されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL アクティベーション – オーディエンスエグレス （1回）]**: アクティベーションワークフローを通じて、宛先へのオーディエンスのエグレスが1回処理されると、クレジットが消費されます。 このアクティビティは、オーディエンスを受信する共同作業者に課金されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL アクティベーション – オーディエンス エグレス （繰り返し）]**: アクティベーション ワークフローを通じて、繰り返しスケジュールで宛先へのオーディエンス エグレスが処理されると、クレジットが消費されます。 このアクティビティは、オーディエンスを受信する共同作業者に課金されます。 詳しくは、「[ オーディエンスのアクティベーション ](/help/guide/collaborate/activate.md) ガイド」を参照してください。
* **[!UICONTROL Measurement]**: Collaborationでキャンペーンパフォーマンスレポートとインサイトを生成すると、クレジットが消費されます。 クレジットは、すべてのキャンペーンのキャンペーンレポートの行数と、毎日、3日ごと、毎週などのレポートの頻度にもとづいて消費されます。

## クレジット消費量の管理 {#manage-credit-consumption}

クレジット消費を効果的に管理するには：

1. **各アクティビティに関連するクレジット消費量を**&#x200B;理解します。 アクティビティごとに使用されるクレジットの表については、[Collaboration製品の説明](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html){target=_blank}を確認してください。
2. **利用状況を定期的に監視**：利用可能なクレジットとアクティビティテーブルを確認して、オーディエンス管理、オーディエンスアクセス、オーディエンスエグレス、測定アクティビティ全体の利用パターンを把握します。
3. **接続で追跡**：接続名を使用して、最もクレジットを消費している接続を特定します。
