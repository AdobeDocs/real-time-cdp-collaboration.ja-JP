---
title: 注釈の概要
description: Real-Time CDP Collaborationの宛先について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 5cbbf5c4-4caa-40da-97be-690d95c1201c
source-git-commit: 4ef7f8c7c27935f0e5b3620da63e7129f2714b37
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 6%

---

# 宛先の概要

{{limited-availability-release-note}}

宛先は、ターゲットオーディエンスを外部プラットフォームに送信するために使用される統合です。 これらの統合により、キャンペーンや顧客エンゲージメントで使用するために、様々なマーケティングチャネルやプラットフォームにわたってオーディエンスをアクティブ化できます。

共同作業者は、キャンペーンで使用するオーディエンスを外部プラットフォーム（Adobe Experience Platformなど）に送信するように宛先を設定できます。 コラボレーターは次に [ プロジェクト内のオーディエンスをアクティブ化 ](../collaborate/activate.md) でき、それが接続の設定された宛先に送信されます。 アクティベーションは、オーディエンスアクティベーションの設定 [ 接続で設定 ](/help/guide/connect/establishing-connections.md#configure-connection-settings) に応じて、いずれかの共同作業者が行うことができます。

>[!IMPORTANT]
>
>現在、共同作業者がプロジェクト内のオーディエンスをアクティブ化すると、接続の設定された宛先に自動的に送信されます。 共同作業者がプロジェクト内のオーディエンスをアクティブ化する前に、宛先を設定する **必要があります**。

## 宛先の設定 {#configure-destinations}

宛先を設定するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL 宛先]**」タブを選択します。 ここでは、使用可能なすべての宛先を表示できます。

>[!NOTE]
>
> 現在、Collaboration内でセルフサービスの宛先として使用できるのはAdobe Experience Platformのみです。 Amazon S3 やSnowflakeなどの宛先の設定に興味がある場合は、Adobe担当者にお問い合わせください。

![ 使用可能な宛先を表示する、設定ワークスペースの「自分の宛先」タブ ](/help/assets/destinations/overview/my-destinations-overview.png)

宛先の設定を開始するには、選択した宛先内で **[!UICONTROL 設定]** オプションを選択します。 特定の宛先の設定について詳しくは、[ 使用可能な宛先 ](#available-destinations) 表のガイドを参照してください。

![Adobe Experience Platformの宛先用に「設定」オプションがハイライト表示された宛先ワークスペース ](/help/assets/destinations/overview/my-destinations-set-up.png)

### 使用可能な宛先 {#available-destinations}

Collaborationで設定を行う場合は、以下の宛先を使用できます。 その宛先の設定ガイドを表示するには、以下の表で宛先名を選択します。 現在利用できない宛先を設定したい場合は、Adobe担当者にお問い合わせください。

| 宛先 | 対象 |
| --- | --- |
| [Adobe Experience Platform](./experience-platform.md) | 利用可能 |
| Amazon S3 | 準備中 |
| Snowflake | 準備中 |
| Google Cloud Storage | 準備中 |
| Azure Blob ストレージ | 準備中 |

## 次の手順

宛先を設定したら、プロジェクト内で [ ターゲットオーディエンスのアクティブ化 ](../collaborate/activate.md) を開始できます。
