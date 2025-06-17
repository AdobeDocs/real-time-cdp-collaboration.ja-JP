---
title: Adobe Experience Platformを宛先として設定
description: Real-Time CDP CollaborationでAdobe Experience Platformを宛先として設定および管理する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: c36814b8dc975b5ea243688981481de49a8219fd
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 2%

---

# Adobe Experience Platformを宛先として設定

{{limited-availability-release-note}}

プロジェクトからAdobe Experience Platformに対してオーディエンスをアクティブ化するには、この宛先を設定します。 Adobe Experience Platformに対してオーディエンスをアクティブ化すると、様々なマーケティングチャネルでのオーディエンスのセグメント化、分析およびアクティブ化にプラットフォームの機能を活用できます。 Adobe Experience Platformについて詳しくは、[Experience Platformの概要 ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"} を参照してください。

>[!NOTE]
>
>現在、Real-Time CDP Collaborationの宛先を設定できるのはパブリッシャーのみです。

## 宛先の設定 {#configure-destination}

Adobe Experience Platformを宛先として設定するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL 宛先]**」タブを選択します。 Adobe Experience Platformの **[!UICONTROL 設定]** を選択します。

![Adobe Experience Platform宛先の「設定」オプションがハイライト表示された宛先ワークスペース ](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

**[!UICONTROL 宛先を作成]** ワークフローが表示されます。

![Adobe Experience Platformの宛先を作成ワークフロー ](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### サンドボックスを設定 {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="オーディエンスの有効期限"
>abstract="オーディエンスがAdobe Experience Platformで使用できなくなるまでの期間です。 デフォルトの有効期限は 30 日ですが、1～30 日の任意の値に設定できます。"

まず、オーディエンスデータを送信するサンドボックスを選択する必要があります。

>
>
>ユーザーがアクセスできるサンドボックスのみを選択できます。 デフォルトでは、すべてのReal-Time CDP Collaboration ユーザーが **Prod** サンドボックスにアクセスできます。 追加のサンドボックスにアクセスできるようにするには、管理者がユーザーに割り当てられた役割に追加のサンドボックスを追加する必要があります。 役割の管理について詳しくは、[ 役割の管理 ](../permissions/manage-roles.md) ガイドを参照してください。

「**[!UICONTROL サンドボックスを設定]**」セクションで、「**[!UICONTROL サンドボックス]**」ドロップダウンを選択するか、サンドボックスの名前を入力します。

![ 宛先を作成ワークフローでハイライト表示されたサンドボックスのドロップダウン。](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

または、「**[!UICONTROL サンドボックスを参照]**」を選択して、使用可能なすべてのサンドボックス、**[!UICONTROL タイプ]**、**[!UICONTROL ステータス]**、**[!UICONTROL 地域]** を表示することができます。 使用するサンドボックスを選択し、「**[!UICONTROL 保存]**」を選択します。

次に、**[!UICONTROL オーディエンスの有効期限]** を設定します。 デフォルトでは、オーディエンスの有効期限は 30 日に設定されています。 有効期限は 1～30 日の任意の期間で設定できます。 有効期限が切れると、オーディエンスはAdobe Experience Platformで使用できなくなります。

![ 宛先を作成ワークフローでハイライト表示されたオーディエンスの有効期限セクション。](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### アクティベーションマッピングを作成 {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="アクティベーション一致キー"
>abstract="アクティベーションの一致キーは、組織の作成時に選択した一致キーに基づいて表示されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="ターゲット名前空間"
>abstract="Target 名前空間は、一致キーがAdobe Experience Platformでマッピングされる ID 名前空間を指定します。 ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。"

次に、アクティベーションマッピングを作成して、オーディエンスデータをAdobe Experience Platformに送信する方法を定義する必要があります。 組織の作成時に選択した各 [ 一致するキー ](../setup/onboard-organization.md#set-up-match-keys) をターゲット名前空間にマッピングできます。 Target 名前空間は、Adobe Experience Platformで一致キーのマッピング先となる [ID 名前空間 ](https://experienceleague.adobe.com/ja/docs/experience-platform/identity/features/namespaces#standard){target="_blank"} を指定します。

>
>
>ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。 例えば、**[!UICONTROL ハッシュ化されたメール]** 一致キーは、Adobe Experience Platformの **[!UICONTROL メール（SHA256、小文字）]** ID 名前空間にマッピングする必要があります。 **[!UICONTROL ハッシュ化されたメール]** 一致キーを **[!UICONTROL メール]** ID 名前空間にマッピングすることはできません。この名前空間は、ハッシュ化された値をサポートしていないからです。

各一致キーの横にある **[!UICONTROL ターゲット名前空間]** フィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 リストでターゲット名前空間を検索するか、特定の名前空間を検索します。 一致キーに使用するターゲット名前空間を選択し、「**[!UICONTROL 選択]**」を選択します。

![ 「選択」オプションがハイライト表示されたソースフィールドを選択ダイアログ…](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

すべての一致キーのマッピングが完了したら、設定を確認してから「**[!UICONTROL 作成]**」を選択し、宛先の作成を完了します。

## Adobe Experience Platformを宛先として使用

Adobe Experience Platformを宛先として設定したら、プロジェクトを通じて、プラットフォームへの [ オーディエンスのアクティブ化 ](../collaborate/activate.md) を開始できます。 現在、アクティベーションプロセスは、広告主によって開始される単一ステップのプロセスです。 広告主がオーディエンスをアクティブ化すると、そのオーディエンスはパブリッシャーの事前設定済み宛先（この場合はAdobe Experience Platform）に送信されます。 パブリッシャーは、オーディエンスを宛先に送信するために、追加の手順を実行する必要はありません。

>[!IMPORTANT]
>
>共同作業者がオーディエンスをアクティベートするには、Adobe Experience Platformを宛先として設定する **&#x200B;**&#x200B;必要があります *前* 必要があります。 宛先が設定されていない場合、オーディエンスは送信され、プロジェクト内の「**[!UICONTROL アクティベート]** タブに表示されますが、Adobe Experience Platformにはアクティベートされません。

オーディエンスがアクティブ化されると、Real-Time CDP Collaborationをオリジンとして、Experience Platformの [ オーディエンスポータル ](#audience-portal) で使用できるようになります。  これらのオーディエンスは、キャンペーンや顧客エンゲージメントで使用できます。

### オーディエンスポータル {#audience-portal}

これで、Adobe Experience Platformを宛先として設定したので、オーディエンスポータルでアクティブ化されたオーディエンスを表示できます。 オーディエンスポータルは、オーディエンスを表示および管理できるAdobe Experience Platform内の中央ハブです。 オーディエンスポータルでオーディエンスをフィルタリングする際のオリジンとしてReal-Time CDP Collaborationが提供されるようになりました。

>[!IMPORTANT]
>
>お客様は、Adobe Experience Platformに対してアクティブ化するオーディエンスに対して、必要なデータ使用ラベルを適用する責任があります。 詳しくは、[ データ使用ラベル ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"} ガイドを参照してください。

![ フィルターオプションでReal-Time CDP Collaborationをオリジンとして使用するオーディエンスポータル。](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Audience Portal について詳しくは、[Audience Portal の概要 ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} ガイドを参照してください。
