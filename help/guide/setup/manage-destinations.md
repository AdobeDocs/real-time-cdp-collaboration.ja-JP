---
title: 宛先の設定と管理
description: Real-Time CDP Collaborationで配信先を設定および管理する方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: b4b26761-46ac-420f-b9f7-6e829d67aec9
TQID: https://experienceleague.adobe.com/3JoqIEJ0ilX3NHYOVersSkaa98kgPzOhqk94UP6Xc50
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 401
ht-degree: 1%

---

# 宛先の設定と管理

{{limited-availability-release-note}}

配信先は、ターゲットオーディエンスを外部プラットフォームに送信するために使用される統合機能です。 これらの統合により、様々なマーケティングチャネルやプラットフォームでオーディエンスをアクティベートし、キャンペーンや顧客エンゲージメントで使用できます。

共同作業者は、キャンペーンで使用するために、Adobe Experience Platformなどの外部プラットフォームにオーディエンスを送信する宛先を設定できます。 共同作業者は、接続の設定済み宛先に送信されるプロジェクト ](../collaborate/activate.md)内のオーディエンスを[ アクティブ化できます。 ライセンス認証は、接続](/help/guide/connect/establishing-connections.md#configure-connection-settings)で設定されたオーディエンスのライセンス認証設定[に応じて、いずれかの共同作業者によって実行できます。

![ アクティブなAdobe Experience Platformの宛先が表示されている設定ワークスペースの「My destinations」タブ。](/help/assets/setup/manage-destinations/my-destinations-overview.png)

宛先について詳しくは、[宛先の概要](../destinations/overview.md) ガイドを参照してください。

## 宛先の設定 {#configure-destinations}

宛先は、Collaborationの&#x200B;**[!UICONTROL Setup]** セクションで設定されます。 宛先を設定するには、**[!UICONTROL セットアップ]**&#x200B;に移動し、**[!UICONTROL 自分の宛先]** タブを選択します。 ここでは、利用可能なすべての宛先を表示できます。

>[!IMPORTANT]
>
>宛先を設定および管理するには、ユーザーに&#x200B;**オーディエンスデータの管理**&#x200B;権限が割り当てられている役割が必要です。 役割の管理について詳しくは、[役割の管理](../permissions/manage-roles.md) ガイドを参照してください。

![ セットアップ ワークスペースの「My destinations」タブに、使用可能な宛先が表示されます。](/help/assets/setup/manage-destinations/my-destinations.png)

宛先の設定プロセスは、設定する宛先によって異なります。 使用可能な宛先とその設定ガイドについては、[使用可能な宛先](../destinations/overview.md#available-destinations) カタログを参照してください。

>[!NOTE]
>
>現在、Real-Time CDP Collaboration内のセルフサービスの宛先として利用できるのはAdobe Experience Platformのみです。 別の目的地の設定をご希望の場合は、Adobe担当者にお問い合わせください。

## 宛先の削除 {#delete-destinations}

宛先を削除すると、アカウントから削除され、以前に送信されたオーディエンスが宛先から削除され、今後のオーディエンスがその宛先に送信されなくなります。

宛先を削除するには、**[!UICONTROL 設定]** セクションの「**[!UICONTROL My destinations]**」タブに移動します。 削除する宛先の&#x200B;**[!UICONTROL 削除]** オプションを選択します。

![Adobe Experience Platformの宛先に対して、「削除」オプションが強調表示されたMy destinations ワークスペース。](/help/assets/setup/manage-destinations/delete-destination.png)

確認ダイアログが表示され、宛先を削除することを確認できます。 宛先を削除するには、**[!UICONTROL 削除]**&#x200B;を選択します。

![削除オプションがハイライト表示された宛先を削除ダイアログ。](/help/assets/setup/manage-destinations/delete-destination-confirmation.png)

## 次の手順

宛先を設定したら、プロジェクト内で[ ターゲットオーディエンスをアクティブ化](../collaborate/activate.md)するために、接続内で共同作業を開始できます。
