---
title: Amazon Marketing Cloud
description: Real-Time CDP CollaborationでのAmazon Marketing Cloudの共同作業について説明します。
audience: publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 1a1b8fec-384b-465f-832d-0772c518fdf1
source-git-commit: f0e260d9bf15a0230940c967e6d73e7431625358
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 20%

---

# Amazon Marketing Cloud

{{limited-availability-release-note}}

[!DNL Amazon Marketing Cloud] （[!DNL AMC]）との接続を確立した後、広告主は[&#x200B; プロジェクトを作成](../manage-projects.md#create-project)して[!DNL AMC]と共同作業を行い、高度な分析機能を活用することができます。 プロジェクトを作成したら、**[!UICONTROL もっと知る]** セクションを使用してオーディエンスインサイトを比較し、キャンペーンに関連するオーディエンスを見つけることができます。

>[!IMPORTANT]
>
>[!DNL AMC]でサポートされているユースケースは、**オーディエンスの検出**&#x200B;と&#x200B;**測定**&#x200B;のみです。 現在、[!DNL AMC]のプロジェクト内で利用できるのは、**[!UICONTROL もっと知る]** セクションのみです。

## 最新情報 {#discover}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="オーディエンスの比較"
>abstract="オーディエンスを Amazon Ads がリーチしたすべての消費者と比較します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="関連するオーディエンス"
>abstract="DSP インプレッションのみを考慮して、オーディエンスの重複が最も高い Amazon ターゲティング セグメント（これらのセグメントは DSP でのみターゲット設定できます）。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="解決済み ID"
>abstract="Amazon の ID 解決がオーディエンスデータを使用して解決できた ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="重複する広告表示 ID"
>abstract="これは、アップロードされたオーディエンスのうち、Amazon Ads 経由で広告にも表示された「解決済み ID」の数を表します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="重複率"
>abstract="Amazon Ads 経由で広告に表示された「解決済み ID」の割合。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Amazon 広告商品ごとの分類"
>abstract="Amazon Ads スポンサー商品または Amazon Ads DSP がリーチした「重複広告表示 ID」の分類。"

「**[!UICONTROL もっと知る]**」セクションでは、AMC オーディエンスを、Amazon Adsがリーチしたすべてのコンシューマーと比較できます。 また、DSPのインプレッションのみを考慮して、オーディエンスの重なりが最も大きいAmazon ターゲティングセグメントを表示することもできます（これらのセグメントはDSPでのみターゲットにできます）。

>[!IMPORTANT]
>
>オーディエンスデータは、[!DNL Amazon Ads] アカウントにアップロードされたオーディエンスから処理されます。 Experience Platformの配信先機能を使用してオーディエンスを[!DNL Amazon Ads] アカウントに送信する方法については、[Amazon Ads接続](https://experienceleague.adobe.com/ja/docs/experience-platform/destinations/catalog/advertising/amazon-ads) ガイドを参照してください。

![Amazon Marketing Cloudを使用したプロジェクトの「もっと知る」セクション。](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### オーディエンスの比較 {#compare-audiences}

「**[!UICONTROL オーディエンスの比較]**」セクションでは、[!DNL AMC]のオーディエンスとAmazon Adsでリーチしたコンシューマーとの重なり方に関するインサイトを提供します。 「**[!UICONTROL オーディエンスを比較]**」セクションでは、次の指標を表示できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL 解決済みID] | ID [!DNL Amazon’s Identity Resolution]の数は、オーディエンスデータを使用して解決できました。 |
| [!UICONTROL 重複する広告露出ID] | [!DNL Amazon Ads]経由で広告に公開された、アップロードされたオーディエンスからの[!UICONTROL 解決済みID]の数。 |
| [!UICONTROL 重複%] | [!DNL Amazon Ads]経由で広告に公開された[!UICONTROL 解決済みID]の割合。 |
| [!UICONTROL Amazon広告の商品別の分類] | [!UICONTROL &#x200B; スポンサー製品]または[!UICONTROL DSP]のいずれかによって、[!UICONTROL 重複する広告露出ID]の内訳に達しました。 各IDは、広告で公開されたIDの総数に対する個別の割合として表されます。 IDは[!UICONTROL &#x200B; スポンサー製品]と[!UICONTROL DSP]の両方に属することができるため、合計が100%にならない場合があります。 |


### 関連するオーディエンス {#relevant-audiences}

**[!UICONTROL 関連オーディエンス]** セクションでは、DSP インプレッションのみを考慮して、オーディエンスが最も重なっている[!DNL Amazon] ターゲットセグメントまたはオーディエンスに関するインサイトを提供します（これらのセグメントはDSPでのみターゲットにできます）。 関連するあらゆるオーディエンスを切り替えて、各セクションで次の指標を確認できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL 解決済みID] | ID [!DNL Amazon’s Identity Resolution]の数は、オーディエンスデータを使用して解決できました。 |
| [!UICONTROL 重複する広告露出ID] | これは、[!DNL Amazon Ads]を介して広告に公開された、アップロードされたオーディエンスからの[!UICONTROL 解決済みID]の数を表します。 これは、DSP インプレッションのみを考慮します。 |
| [!UICONTROL 重複%] | [!DNL Amazon Ads]経由で広告に公開された[!UICONTROL 解決済みID]の割合。 |
| [!UICONTROL &#x200B; カテゴリ &#x200B;] | オーディエンスが属するカテゴリ。 オーディエンスは複数のカテゴリに属することができます。 |

### [!DNL Amazon Marketing Cloud]との重複を検出 {#discover-overlaps}

「**[!UICONTROL Amazon Marketing Cloudとの重複を見つける]**」セクションでは、オーディエンスが[!DNL Amazon]個のターゲットセグメントまたはオーディエンスとどのように重複しているかについてのインサイトを提供します。 次の指標を表示できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL 解決済みID] | ID [!DNL Amazon’s Identity Resolution]の数は、オーディエンスデータを使用して解決できました。 |
| [!UICONTROL 重複する広告露出ID] | これは、[!DNL Amazon Ads]を介して広告に公開された、アップロードされたオーディエンスからの[!UICONTROL 解決済みID]の数を表します。 これは、DSP インプレッションのみを考慮します。 |
| [!UICONTROL 重複%] | [!DNL Amazon Ads]経由で広告に公開された[!UICONTROL 解決済みID]の割合。 |
