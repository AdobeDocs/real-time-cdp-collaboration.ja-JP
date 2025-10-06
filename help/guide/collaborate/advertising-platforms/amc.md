---
title: AmazonMarketing Cloud
description: Real-Time CDP CollaborationでのAmazon Marketing Cloudとの共同作業について説明します。
audience: publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 57b847c25edbf88f4708bda74be41fe6141472a7
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 20%

---

# AmazonMarketing Cloud

{{limited-availability-release-note}}

[!DNL Amazon Marketing Cloud] （[!DNL AMC]）との接続を形成した後、広告主は [&#x200B; プロジェクトを作成 &#x200B;](../manage-projects.md#create-project) して [!DNL AMC] との共同作業を行い、高度な分析機能を活用できます。 プロジェクトを作成した後、「**[!UICONTROL 検出]**」セクションを使用して、オーディエンスインサイトを比較し、キャンペーンに関連するオーディエンスを検出できます。

>[!IMPORTANT]
>
>[!DNL AMC] でサポートされているユースケースは **オーディエンス検出** と **測定** のみです。 現在、**[!UICONTROL を使用したプロジェクト内では]** 検出 [!DNL AMC] セクションのみを使用できます。

## 検出 {#discover}

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

**[!UICONTROL 検出]** セクションでは、AMC オーディエンスを、Amazon広告で到達したすべてのコンシューマーと比較できます。 また、DSPのインプレッションのみを考慮して、オーディエンスの重複度が最も高いAmazonのターゲティングセグメントを表示することもできます（これらのセグメントは、DSPでのみターゲット設定できます）。

>[!IMPORTANT]
>
>オーディエンスデータは、[!DNL Amazon Ads] アカウントにアップロードされたオーディエンスから処理されます。 送信方法Experience Platform Ads 宛先機能を使用してオーディエンスを [!DNL Amazon Ads] アカウントに送信する方法については、[Amazon Ads connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/amazon-ads) ガイドを参照してください。

![Amazon Marketing Cloudを使用したプロジェクトの Discover セクション。](/help/assets/collaborate/advertising-platforms/amc-discover.png){zoomable="yes"}

### オーディエンスの比較 {#compare-audiences}

**[!UICONTROL オーディエンスの比較]** セクションでは、[!DNL AMC] オーディエンスがAmazon広告で到達したコンシューマーとどのように重なっているかについて、インサイトが得られます。 「**[!UICONTROL オーディエンスを比較]** セクションでは、次の指標を表示できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL &#x200B; 解決された ID] | [!DNL Amazon’s Identity Resolution] がオーディエンスデータを使用して解決できた ID の数。 |
| [!UICONTROL &#x200B; 重複する公開済み ID] | [!UICONTROL &#x200B; 経由で広告にも公開された、アップロードされたオーディエンスの &#x200B;] 解決済み ID[!DNL Amazon Ads] の数。 |
| [!UICONTROL &#x200B; 重複 %] | [!UICONTROL &#x200B; を介して広告に公開された &#x200B;] 解決済み ID[!DNL Amazon Ads] の割合。 |
| [!UICONTROL Amazon広告商品ごとの内訳 &#x200B;] | [!UICONTROL &#x200B; スポンサー付き商品 &#x200B;] または [!UICONTROL DSP] のいずれかによって到達した [!UICONTROL &#x200B; 重複する広告公開済み ID] の分類。 各は、広告に公開された ID の合計数に対する個々の割合として表されます。 ID は [!UICONTROL &#x200B; スポンサー商品 &#x200B;] と [!UICONTROL DSP] の両方に属している可能性があるので、割合は合計で 100% にならない場合があります。 |


### 関連するオーディエンス {#relevant-audiences}

**[!UICONTROL 関連するオーディエンス]** セクションでは、DSPのインプレッションのみを考慮して、オーディエンスの重 [!DNL Amazon] が最も大きいオーディエンスのターゲティングセグメントまたはオーディエンスに関するインサイトが提供されます（これらのセグメントはDSPでのみターゲット設定できます）。 すべての関連オーディエンスを切り替えることができ、各セクション内で次の指標を表示できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL &#x200B; 解決された ID] | [!DNL Amazon’s Identity Resolution] がオーディエンスデータを使用して解決できた ID の数。 |
| [!UICONTROL &#x200B; 重複する公開済み ID] | これは、アップロードされたオーディエンスのうち、[!UICONTROL &#x200B; 経由で広告にも公開された &#x200B;] 解決済み ID[!DNL Amazon Ads] の数を表します。 これは、DSPのインプレッションのみを考慮します。 |
| [!UICONTROL &#x200B; 重複 %] | [!UICONTROL &#x200B; を介して広告に公開された &#x200B;] 解決済み ID[!DNL Amazon Ads] の割合。 |
| [!UICONTROL &#x200B; カテゴリ &#x200B;] | オーディエンスが属するカテゴリ（複数可）。 オーディエンスは複数のカテゴリに属することができます。 |

### Discover と [!DNL Amazon Marketing Cloud] の重複 {#discover-overlaps}

**[!UICONTROL Amazon Marketing Cloudとの重複の検出]** の節では、オーディエンスが [!DNL Amazon] のターゲティングセグメント（オーディエンス）とどのように重複するかについてのインサイトを提供します。 次の指標を表示できます。

| 指標 | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| [!UICONTROL &#x200B; 解決された ID] | [!DNL Amazon’s Identity Resolution] がオーディエンスデータを使用して解決できた ID の数。 |
| [!UICONTROL &#x200B; 重複する公開済み ID] | これは、アップロードされたオーディエンスのうち、[!UICONTROL &#x200B; 経由で広告にも公開された &#x200B;] 解決済み ID[!DNL Amazon Ads] の数を表します。 これは、DSPのインプレッションのみを考慮します。 |
| [!UICONTROL &#x200B; 重複 %] | [!UICONTROL &#x200B; を介して広告に公開された &#x200B;] 解決済み ID[!DNL Amazon Ads] の割合。 |