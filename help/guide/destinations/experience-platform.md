---
title: Adobe Experience Platformを宛先として設定
description: Real-Time CDP CollaborationでAdobe Experience Platformを宛先として設定および管理する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1489'
ht-degree: 11%

---

# Adobe Experience Platformを宛先として設定

{{limited-availability-release-note}}

プロジェクトからAdobe Experience Platformに対してオーディエンスをアクティブ化するには、この宛先を設定します。 Adobe Experience Platformに対してオーディエンスをアクティブ化すると、様々なマーケティングチャネルでのオーディエンスのセグメント化、分析およびアクティブ化にプラットフォームの機能を活用できます。 Adobe Experience Platformについて詳しくは、[Experience Platformの概要 ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"} を参照してください。

>[!WARNING]
>
>作成した後で宛先を更新することはできません。 設定を変更する必要がある場合は、既存の宛先を削除し、新しい宛先を作成する必要があります。

## 宛先の設定 {#configure-destination}

Adobe Experience Platformを宛先として設定するには、**[!UICONTROL 設定]** に移動し、「**[!UICONTROL 宛先]**」タブを選択します。 Adobe Experience Platformの **[!UICONTROL 設定]** を選択します。

![Adobe Experience Platform宛先の「設定」オプションがハイライト表示された宛先ワークスペース ](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

**[!UICONTROL 宛先を作成]** ワークフローが表示されます。

![Adobe Experience Platformの宛先を作成ワークフロー ](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### サンドボックスの設定 {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="オーディエンスの有効期限"
>abstract="Adobe Experience Platform でオーディエンスが使用できなくなるまでの期間です。デフォルトの有効期限は 30 日ですが、1～30 日の任意の値に設定できます。"

まず、オーディエンスデータを送信するサンドボックスを選択する必要があります。

>[!IMPORTANT]
>
>ユーザーがアクセスできるサンドボックスのみを選択できます。 デフォルトでは、すべてのCollaboration ユーザーが **Prod** サンドボックスにアクセスできます。 追加のサンドボックスにアクセスできるようにするには、管理者がユーザーに割り当てられた役割に追加のサンドボックスを追加する必要があります。 役割の管理について詳しくは、[ 役割の管理 ](../permissions/manage-roles.md) ガイドを参照してください。

「**[!UICONTROL サンドボックスを設定]**」セクションで、「**[!UICONTROL サンドボックス]**」ドロップダウンを選択するか、サンドボックスの名前を入力します。

![ 宛先を作成ワークフローでハイライト表示されたサンドボックスのドロップダウン。](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

または、「**[!UICONTROL サンドボックスを参照]**」を選択して、使用可能なすべてのサンドボックス、**[!UICONTROL タイプ]**、**[!UICONTROL ステータス]**、**[!UICONTROL 地域]** を表示することができます。 使用するサンドボックスを選択し、「**[!UICONTROL 保存]**」を選択します。

次に、**[!UICONTROL オーディエンスの有効期限]** を設定します。 デフォルトでは、オーディエンスの有効期限は 30 日に設定されています。 有効期限は 1～30 日の任意の期間で設定できます。 有効期限が切れると、オーディエンスはAdobe Experience Platformで使用できなくなります。

![ 宛先を作成ワークフローでハイライト表示されたオーディエンスの有効期限セクション。](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

### アクティベーションマッピングの作成 {#create-activation-mapping}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_matchkeys"
>title="アクティベーション一致キー"
>abstract="アクティベーション一致キーは、組織の作成時に選択した一致キーに基づいて表示されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_activation_mapping"
>title="詳細情報"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_target_namespaces"
>title="ターゲット名前空間"
>abstract="ターゲット名前空間は、一致キーが Adobe Experience Platform でマッピングされる ID 名前空間を指定します。ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。"

アカウントで有効になっているすべての一致キーは、デフォルトでアクティベーションマッピングに含まれます。 一致キーをターゲット名前空間に直接マッピングしない場合は、「リンクされたキー」オプションを使用して、別の一致キーに置き換えることができます。 リンク キーの詳細については、[ 以下のセクション ](#linked-keys) を参照してください。

#### ターゲット名前空間のマッピング {#map-target-namespaces}

各一致キーをターゲット名前空間にマッピングするには、一致キーの横にある **[!UICONTROL ターゲット名前空間]** フィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 リストでターゲット名前空間を検索するか、特定の名前空間を検索します。 一致キーに使用するターゲット名前空間を選択し、「**[!UICONTROL 選択]**」を選択します。

>[!IMPORTANT]
>
>ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。 例えば、**[!UICONTROL ハッシュ化されたメール]** 一致キーは、Adobe Experience Platformの **[!UICONTROL メール（SHA256、小文字）]** ID 名前空間にマッピングする必要があります。 **[!UICONTROL ハッシュ化されたメール]** 一致キーを **[!UICONTROL メール]** ID 名前空間にマッピングすることはできません。この名前空間は、ハッシュ化された値をサポートしていないからです。

![ 「選択」オプションがハイライト表示されたソースフィールドを選択ダイアログ…](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

アクティベーションマッピングに含める一致キーごとに、このプロセスを繰り返します。 一致キーを含めない場合は、そのキーを削除するか、「リンクされたキー」オプションを使用して別の一致キーに置き換えることができます。

#### リンクキー {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="リンクキー"
>abstract="リンク付けされたキーを使用すると、アクティベーション中に元の一致キーの代わりに別の一致キーを使用するように指定できます。プロファイルをアクティブ化するには、元の一致キーとリンク付けされた一致キーの両方に値が必要です。"

リンク付けされたキーを使用すると、アクティベーション中に元の一致キーの代わりに別の一致キーを使用するように指定できます。リンクされたキーの動作をより深く理解するために、次の例を考えてみましょう。

retailerは、アクティブ化するデータをExperience Platformに CRM システムに送信します。 retailerでは、オーディエンスをアクティブ化する際に一致率を高めるために、ハッシュ化された IP を自分のアカウントの一致キーとして有効にしました。 ただし、retailerの CRM システムでは、ハッシュ化された IP を ID 名前空間としてサポートしていないので、Experience Platformに対してオーディエンスをアクティブ化する際に、代わりに CRM ID 一致キーを使用します。 retailerでは、「リンクされたキー」オプションを使用すると、ハッシュ化された IP の代わりに CRM ID を使用して、オーディエンスをExperience Platformに対してアクティブ化できます。

>[!NOTE]
>
>プロファイルをアクティブ化するには、元の一致キーとリンクされた一致キーの両方に値が必要です。 例えば、ハッシュ化された ID が CRM ID にリンクされている場合、アクティブ化するには、プロファイルにハッシュ化された ID と CRM ID の両方の値が必要です。 いずれかの値が指定されていない場合、プロファイルはアクティブ化されません。

リンクキーを使用するには、代わりに使用する一致キーの横にある **[!UICONTROL リンクキー]** オプションをオンにします。 「**[!UICONTROL リンクされたキー]** セクションが表示され、マッピングを作成するように求められます。

![ 宛先を作成ワークフローでハイライト表示された「リンクされたキー」オプションとセクション。](/help/assets/destinations/adobe-experience-platform/linked-key.png)

使用する **[!UICONTROL リンクキー]** をドロップダウンメニューから選択します。 上記の例では、retailerは **[!UICONTROL CRM ID]** をリンクキーとして選択します。

![ 宛先を作成ワークフローでハイライト表示されたリンクされたキー ](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

次に、リンクされたキーのターゲット名前空間をまだ指定していない場合は、指定します。 **[!UICONTROL アクティベーションマッピングを作成]** セクションで一致キーのターゲット名前空間を既に選択している場合、これが自動入力されます。 リンクされたキーのターゲット名前空間をまだ選択していない場合は、ここで選択できます。

リンクされたキーの横にある **[!UICONTROL ターゲット名前空間]** フィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 リストでターゲット名前空間を検索するか、特定の名前空間を検索します。 リンクされたキーに使用するターゲット名前空間を選択し、「**[!UICONTROL 選択]**」を選択します。

![ ソースフィールドを選択ダイアログ ](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

これで、リンクされたキーが設定されました。

>[!NOTE]
>
>アクティブ化マッピングごとに使用できるリンクされたキーターゲット名前空間は 1 つだけです。 例えば、ハッシュ化された ID を CRM ID にリンクした場合、別のフィールドのリンクされたキーオプションを切り替えると、CRM ID にもリンクされます。

すべての一致キーのマッピングが完了したら、設定を確認します。 「**[!UICONTROL プレビュー]**」セクションには、設定の概要が表示されます。

![ 宛先を作成ワークフローの「プレビュー」セクション ](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>現在、各一致キーは、個別のオーディエンスとしてExperience Platformに対してアクティブ化されます。 例えば、一致キーとして [!UICONTROL &#x200B; ハッシュ化されたメール &#x200B;] と [!UICONTROL &#x200B; ハッシュ化された電話 &#x200B;] がある場合、オーディエンスがアクティブ化されると、Audience Portal で 2 つの異なるオーディエンスが作成されます。

設定に問題がなければ、「**[!UICONTROL 宛先を作成]**」を選択します。 宛先が正常に作成されたことを示す確認メッセージが表示されます。

## Adobe Experience Platformを宛先として使用

Experience Platformを宛先として設定したら、プロジェクトを通じて、プラットフォームへの [ オーディエンスのアクティブ化 ](../collaborate/activate.md) を開始できます。 現在、アクティベーションプロセスは、共同作業者によって開始される単一ステップのプロセスです。 例えば、広告主がオーディエンスをアクティブ化すると、そのオーディエンスはパブリッシャーの事前設定済み宛先（Experience Platform）に送信されます。 パブリッシャーは、オーディエンスを宛先に送信するために、追加の手順を実行する必要はありません。 同じことがブランド間のコラボレーションパターンにも当てはまります。

>[!IMPORTANT]
>
>共同作業者がオーディエンスをアクティベートするには、Experience Platformを宛先として設定する **&#x200B;**&#x200B;必要があります *前* 必要があります。 宛先が設定されていない場合、オーディエンスは送信され、プロジェクト内の「**[!UICONTROL アクティベート]** タブに表示されますが、Experience Platformにはアクティベートされません。

オーディエンスがアクティブ化されると、Real-Time CDP Collaborationをオリジンとして、Experience Platformの [ オーディエンスポータル ](#audience-portal) で使用できるようになります。  これらのオーディエンスは、キャンペーンや顧客エンゲージメントで使用できます。

### オーディエンスポータル {#audience-portal}

これで、Adobe Experience Platformを宛先として設定したので、オーディエンスポータルでアクティブ化されたオーディエンスを表示できます。 オーディエンスポータルは、オーディエンスを表示および管理できるAdobe Experience Platform内の中央ハブです。 オーディエンスポータルでオーディエンスをフィルタリングする際のオリジンとしてReal-Time CDP Collaborationが提供されるようになりました。

>[!IMPORTANT]
>
>お客様は、Adobe Experience Platformに対してアクティブ化するオーディエンスに対して、必要なデータ使用ラベルを適用する責任があります。 詳しくは、[ データ使用ラベル ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"} ガイドを参照してください。

![ フィルターオプションでReal-Time CDP Collaborationをオリジンとして使用するオーディエンスポータル。](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

Audience Portal について詳しくは、[Audience Portal の概要 ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} ガイドを参照してください。
