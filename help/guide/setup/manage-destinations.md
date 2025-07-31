---
title: 宛先の設定と管理
description: Real-Time CDP Collaborationの宛先を設定および管理する方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 1%

---

# 宛先の設定と管理

{{limited-availability-release-note}}

宛先は、ターゲットオーディエンスを外部プラットフォームに送信するために使用される統合です。 これらの統合により、キャンペーンや顧客エンゲージメントで使用するために、様々なマーケティングチャネルやプラットフォームにわたってオーディエンスをアクティブ化できます。

共同作業者は、キャンペーンで使用するオーディエンスを外部プラットフォーム（Adobe Experience Platformなど）に送信するように宛先を設定できます。 コラボレーターは次に [ プロジェクト内のオーディエンスをアクティブ化 ](../collaborate/activate.md) でき、それが接続の設定された宛先に送信されます。 アクティベーションは、オーディエンスアクティベーションの設定 [ 接続で設定 ](/help/guide/connect/establishing-connections.md#configure-connection-settings) に応じて、いずれかの共同作業者が行うことができます。

![ アクティブなAdobe Experience Platformの宛先を表示する、設定ワークスペースの「マイ宛先」タブ ](/help/assets/setup/manage-destinations/my-destinations-overview.png)

宛先について詳しくは、[ 宛先の概要 ](../destinations/overview.md) ガイドを参照してください。

## 宛先の設定 {#configure-destinations}

宛先は、Collaborationの **[!UICONTROL 設定]** セクションで設定します。 宛先を設定するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL 宛先]**」タブを選択します。 ここでは、使用可能なすべての宛先を表示できます。

>[!IMPORTANT]
>
>宛先を設定および管理するには、ユーザーに **オーディエンスデータの管理** 権限が割り当てられている必要があります。 役割の管理について詳しくは、[ 役割の管理 ](../permissions/manage-roles.md) ガイドを参照してください。

![ 使用可能な宛先を表示する、設定ワークスペースの「自分の宛先」タブ ](/help/assets/setup/manage-destinations/my-destinations.png)

宛先の設定プロセスは、設定している宛先によって異なります。 使用可能な宛先とその設定ガイドを表示するには、[ 使用可能な宛先 ](../destinations/overview.md#available-destinations) カタログを参照してください。

>[!NOTE]
>
>現在、Real-Time CDP Collaboration内でセルフサービスの宛先として使用できるのはAdobe Experience Platformのみです。 別の宛先の設定に興味がある場合は、Adobe担当者にお問い合わせください。

## 宛先の削除 {#delete-destinations}

宛先を削除すると、アカウントから宛先が削除され、以前に送信されたオーディエンスが宛先から削除され、今後その宛先に送信されるオーディエンスが防止されます。

宛先を削除するには、「設定 **[!UICONTROL セクションの「]** 宛先 **[!UICONTROL タブに移動]** ます。 削除する宛先の **[!UICONTROL 削除]** オプションを選択します。

![Adobe Experience Platformの宛先について、「削除」オプションがハイライト表示された宛先ワークスペース ](/help/assets/setup/manage-destinations/delete-destination.png)

確認ダイアログが表示され、宛先の削除を確認できます。 「**[!UICONTROL 削除]**」を選択して、宛先を削除します。

![ 「削除」オプションがハイライト表示された宛先を削除ダイアログ ](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## 次の手順

宛先を設定したら、接続内で共同作業を開始し、プロジェクト内で [ ターゲットオーディエンスをアクティブ化 ](../collaborate/activate.md) できます。
