---
title: 概要
description: Real-Time CDP Collaborationの配信先について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
TQID: https://experienceleague.adobe.com/1VvnSt3Z65dfQBfXnjJJi3H0Oj9BxFStexq3icVKxkY
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 3%

---

# 宛先の概要

{{limited-availability-release-note}}

配信先は、ターゲットオーディエンスを外部プラットフォームに送信するために使用される統合機能です。 これらの統合により、様々なマーケティングチャネルやプラットフォームでオーディエンスをアクティベートし、キャンペーンや顧客エンゲージメントで使用できます。

共同作業者は、キャンペーンで使用するために、Adobe Experience Platformなどの外部プラットフォームにオーディエンスを送信する宛先を設定できます。 共同作業者は、接続の設定済み宛先に送信されるプロジェクト [&#128279;](../collaborate/activate.md)内のオーディエンスを[&#x200B; アクティブ化できます。 ライセンス認証は、接続](/help/guide/connect/establishing-connections.md#configure-connection-settings)で設定されたオーディエンスのライセンス認証設定に応じて、いずれかの共同作業者によって実行できます。

>[!IMPORTANT]
>
>現在、共同作業者がプロジェクト内のオーディエンスをアクティブ化すると、接続で設定された宛先に自動的に送信されます。 共同作業者がプロジェクト内のオーディエンスをアクティブ化するには、宛先を&#x200B;**設定する必要があります。**

## 宛先の設定 {#configure-destinations}

宛先を設定するには、**[!UICONTROL セットアップ]**&#x200B;に移動し、**[!UICONTROL 自分の宛先]** タブを選択します。 ここでは、利用可能なすべての宛先を表示できます。

>[!NOTE]
>
> 現在、Collaboration内のセルフサービスの宛先として利用できるのはAdobe Experience Platformのみです。 Amazon S3やSnowflakeなどの配信先の設定をご希望の場合は、Adobe担当者にお問い合わせください。

![&#x200B; セットアップ ワークスペースの「My destinations」タブに、使用可能な宛先が表示されます。](/help/assets/destinations/overview/my-destinations-overview.png)

宛先の設定を開始するには、選択した宛先内の「**[!UICONTROL セットアップ]**」オプションを選択します。 特定の宛先の設定について詳しくは、[使用可能な宛先](#available-destinations)の表のガイドを参照してください。

![Adobe Experience Platformの宛先に対して、「設定」オプションがハイライト表示された「自分の宛先」ワークスペース。](/help/assets/destinations/overview/my-destinations-set-up.png)

### 使用可能な宛先 {#available-destinations}

Collaborationで設定するには、次の宛先を使用できます。 その宛先の設定ガイドを表示するには、以下の表で宛先名を選択します。 現在利用できない宛先の設定に興味がある場合は、Adobe担当者にお問い合わせください。

| 宛先 | 対象 |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | 使用可能 |
| [!DNL Amazon S3] | 近日リリース予定 |
| [!DNL Snowflake] | 近日リリース予定 |
| [!DNL Google Cloud Storage] | 近日リリース予定 |
| [!DNL Azure Blob Storage] | 近日リリース予定 |

>[!NOTE]
>
>このテーブルの&#x200B;**[!DNL Google Cloud Storage]**&#x200B;は、**宛先** （Collaborationがアクティベーション中にオーディエンスを送信する場所）を指します。 **[!UICONTROL セットアップ]** ワークスペースのGCS バケットを&#x200B;**から** ソースオーディエンスするには、[&#x200B; オーディエンスソーシング用GCSの設定](../setup/configure-gcs-audience-sourcing.md)を参照してください。

## 次の手順

宛先を設定したら、プロジェクト内で[&#x200B; ターゲットオーディエンスのアクティブ化](../collaborate/activate.md)を開始できます。
