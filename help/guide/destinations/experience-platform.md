---
title: Adobe Experience Platformを宛先として設定
description: Real-Time CDP CollaborationでAdobe Experience Platform as a destinationを設定および管理する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 594610a0-9102-448a-b59b-ec162ef9dd57
TQID: https://experienceleague.adobe.com/vOAlNzIaEKC6cZC-zMxShPTn77kmV3WbUuvZU8Svzh4
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1534
ht-degree: 14%

---

# Adobe Experience Platformを宛先として設定

{{limited-availability-release-note}}

この宛先を設定して、プロジェクトからAdobe Experience Platformにオーディエンスをアクティブ化します。 Adobe Experience Platformでオーディエンスをアクティベートすることで、様々なマーケティングチャネルをまたいでオーディエンスをセグメンテーション、分析、アクティベーションするためのAdobe Marketo Engageの機能を活用できます。 Adobe Experience Platformについて詳しくは、[Experience Platformの概要](https://experienceleague.adobe.com/en/docs/experience-platform/landing/home){target="_blank"}を参照してください。

>[!WARNING]
>
>作成後に宛先を更新することはできません。 設定を変更する必要がある場合は、既存の宛先を削除し、新しい宛先を作成する必要があります。

## 宛先の設定 {#configure-destination}

Adobe Experience Platformを宛先として設定するには、**[!UICONTROL セットアップ]**&#x200B;に移動し、「**[!UICONTROL My destinations]**」タブを選択します。 「**[!UICONTROL Adobe Experience Platform用に設定]**」を選択します。

![Adobe Experience Platformの宛先に対して「設定」オプションが強調表示されたMy destinations ワークスペース。](/help/assets/destinations/adobe-experience-platform/setup-aep.png)

**[!UICONTROL 宛先の作成]** ワークフローが表示されます。

![Adobe Experience Platformの宛先を作成ワークフロー。](/help/assets/destinations/adobe-experience-platform/create-destination.png)

### サンドボックスの設定 {#configure-sandbox}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_audience_expiration"
>title="オーディエンスの有効期限"
>abstract="Adobe Experience Platform でオーディエンスが使用できなくなるまでの期間です。 デフォルトの有効期限は 30 日ですが、1～30 日の任意の値に設定できます。"

まず、オーディエンスデータを送信するサンドボックスを選択する必要があります。

>[!IMPORTANT]
>
>ユーザーがアクセスできるサンドボックスのみを選択できます。 デフォルトでは、すべてのCollaboration ユーザーは&#x200B;**Prod** サンドボックスにアクセスできます。 追加のサンドボックスにアクセスするには、管理者がユーザーに割り当てられた役割に追加のサンドボックスを追加する必要があります。 役割の管理について詳しくは、[役割の管理](../permissions/manage-roles.md) ガイドを参照してください。

**[!UICONTROL サンドボックスの設定]** セクションで、**[!UICONTROL サンドボックス]** ドロップダウンを選択するか、サンドボックス名を入力します。

![宛先を作成ワークフローで強調表示されたサンドボックス ドロップダウン。](/help/assets/destinations/adobe-experience-platform/select-sandbox.png)

または、**[!UICONTROL サンドボックスを参照]**&#x200B;を選択して、使用可能なすべてのサンドボックスと、それらの&#x200B;**[!UICONTROL Type]**、**[!UICONTROL Status]**、**[!UICONTROL Region]**&#x200B;を表示することもできます。 使用するサンドボックスを選択し、**[!UICONTROL 保存]**&#x200B;を選択します。

次に、**[!UICONTROL オーディエンスの有効期限]**&#x200B;を設定します。 デフォルトでは、オーディエンスの有効期限は30日に設定されています。 有効期限は1 ～ 30日の範囲で設定できます。 有効期限が切れると、Adobe Experience Platformでオーディエンスを利用できなくなります。

![宛先の作成ワークフローでハイライト表示されたオーディエンスの有効期限セクション。](/help/assets/destinations/adobe-experience-platform/audience-expiration.png)

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
>abstract="ターゲット名前空間は、一致キーが Adobe Experience Platform でマッピングされる ID 名前空間を指定します。 ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。"

アカウントで有効になっているすべての一致キーは、デフォルトでアクティベーションマッピングに含まれます。 一致キーをターゲット名前空間に直接マッピングしない場合は、「リンクされたキー」オプションを使用して、別の一致キーに置き換えることができます。 リンクされたキーについて詳しくは、以下の[節](#linked-keys)を参照してください。

#### ターゲット名前空間のマッピング {#map-target-namespaces}

各一致キーをターゲット名前空間にマッピングするには、一致キーの横にある&#x200B;**[!UICONTROL ターゲット名前空間]** フィールドを選択します。 「**[!UICONTROL ソースフィールドを選択]**」ダイアログが表示されます。 リストでターゲット名前空間を検索するか、特定の名前空間を検索します。 一致キーに使用するターゲット名前空間を選択し、**[!UICONTROL 選択]**&#x200B;を選択します。

>[!IMPORTANT]
>
>ハッシュ化された一致キーは、ハッシュ化された値をサポートするターゲット名前空間にマッピングする必要があります。 例えば、**[!UICONTROL ハッシュ化された電子メール]**&#x200B;一致キーは、Adobe Experience Platformの&#x200B;**[!UICONTROL 電子メール（SHA256、小文字）]** ID名前空間にマッピングする必要があります。 この名前空間ではハッシュ値がサポートされていないため、**[!UICONTROL ハッシュ化された電子メール]**&#x200B;一致キーを&#x200B;**[!UICONTROL 電子メール]** ID名前空間にマッピングできません。

![選択オプションがハイライト表示されたソースフィールドの選択ダイアログ。](/help/assets/destinations/adobe-experience-platform/select-target-namespace.png)

アクティベーションマッピングに含める照合キーごとに、このプロセスを繰り返します。 一致キーを含めたくない場合は、そのキーを削除するか、「リンクされたキー」オプションを使用して別の一致キーに置き換えることができます。

#### リンクキー {#linked-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_destinations_linked_key"
>title="リンクキー"
>abstract="リンク付けされたキーを使用すると、アクティベーション中に元の一致キーの代わりに別の一致キーを使用するように指定できます。 プロファイルをアクティブ化するには、元の一致キーとリンク付けされた一致キーの両方に値が必要です。"

リンク付けされたキーを使用すると、アクティベーション中に元の一致キーの代わりに別の一致キーを使用するように指定できます。 リンクされたキーの仕組みをよりよく理解するために、次の例を考えてみましょう。

Retailerは、Experience PlatformにアクティベートされているデータをCRM システムに送信したいと考えています。 Retailerでは、オーディエンスをアクティブ化する際に、ハッシュ化されたIPをアカウントの一致キーとして有効にし、マッチ率を高めました。 ただし、retailerのCRM システムは、ID名前空間としてハッシュ化されたIPをサポートしていないため、Experience Platformにオーディエンスをアクティブ化する際には、代わりにCRM ID一致キーを使用する必要があります。 Retailerでは、「リンクされたキー」オプションを使用して、ハッシュ化されたIPではなくCRM IDを使用してExperience Platformにオーディエンスをアクティベートできます。

>[!NOTE]
>
>プロファイルをアクティブ化するには、元の一致キーとリンク付けされた一致キーの両方に値が必要です。 例えば、ハッシュ化されたIDがCRM IDにリンクされている場合、プロファイルをアクティブ化するには、ハッシュ化されたIDとCRM IDの両方の値が必要です。 いずれかの値が見つからない場合、プロファイルはアクティブ化されません。

リンクされたキーを使用するには、代わりに使用する一致キーの横にある「**[!UICONTROL リンクされたキー]**」オプションを切り替えます。 マッピングの作成を求める「**[!UICONTROL リンクされたキー]**」セクションが表示されます。

![&#x200B; リンクされたキーのオプションとセクションが宛先の作成ワークフローで強調表示されます。](/help/assets/destinations/adobe-experience-platform/linked-key.png)

使用する&#x200B;**[!UICONTROL リンクされたキー]**&#x200B;をドロップダウンメニューから選択します。 上記の例に従って、retailerはリンクされたキーとして&#x200B;**[!UICONTROL CRM ID]**&#x200B;を選択します。

![&#x200B; リンクされたキーのドロップダウンが宛先の作成ワークフローで強調表示されます。](/help/assets/destinations/adobe-experience-platform/select-linked-key.png)

次に、リンクされたキーのターゲット名前空間をまだ指定していない場合は、指定します。 「**[!UICONTROL アクティベーションマッピングを作成]**」セクションで一致キーのターゲット名前空間を既に選択している場合、これは自動生成されます。 リンクされたキーのターゲット名前空間をまだ選択していない場合は、今すぐ選択できます。

リンクされたキーの横にある「**[!UICONTROL ターゲット名前空間]**」フィールドを選択します。 「**[!UICONTROL ソースフィールドを選択]**」ダイアログが表示されます。 リストでターゲット名前空間を検索するか、特定の名前空間を検索します。 リンクされたキーに使用するターゲット名前空間を選択し、**[!UICONTROL 選択]**&#x200B;を選択します。

![&#x200B; ソースフィールドを選択ダイアログ。](/help/assets/destinations/adobe-experience-platform/select-linked-key-target-namespace.png)

これで、リンクされたキーが設定されました。

>[!NOTE]
>
>アクティベーションマッピングごとに、1つのリンクされたキーターゲット名前空間のみを使用できます。 例えば、ハッシュ化されたIDをCRM IDにリンクする場合、別のフィールドの「リンクされたキー」オプションを切り替えると、CRM IDにもリンクされます。

すべての一致キーのマッピングが完了したら、設定を確認します。 「**[!UICONTROL プレビュー]**」セクションには、設定の概要が表示されます。

![宛先の作成ワークフローの「プレビュー」セクション。](/help/assets/destinations/adobe-experience-platform/preview.png)

>[!IMPORTANT]
>
>現在、各一致キーは、個別のオーディエンスとしてExperience Platformに対してアクティブ化されます。 例えば、一致キーとして[!UICONTROL &#x200B; ハッシュ化された電子メール &#x200B;]と[!UICONTROL &#x200B; ハッシュ化された電話]を使用している場合、オーディエンスがアクティブ化されると、2つの個別のオーディエンスがAudience Portalに作成されます。

設定に問題がなければ、**[!UICONTROL 宛先を作成]**&#x200B;を選択します。 宛先が正常に作成されたことを示す確認メッセージが表示されます。

## Adobe Experience Platformを宛先として使用する

Experience Platformを宛先として設定したら、プロジェクトを通じて[&#x200B; オーディエンスのプラットフォームへのアクティベーション &#x200B;](../collaborate/activate.md)を開始できます。 現在、アクティベーションプロセスは、共同作業者によって開始されるシングルステップのプロセスです。 例えば、広告主がオーディエンスをアクティベートすると、そのオーディエンスはパブリッシャーの事前設定された宛先（Experience Platform）に送信されます。 パブリッシャーは、オーディエンスを宛先に送信するために追加の手順を実行する必要はありません。 同じことが、ブランドとブランドのコラボレーションのパターンにも当てはまります。

>[!IMPORTANT]
>
>共同作業者がオーディエンスをアクティブ化する&#x200B;*前に、**Experience Platformを宛先*として設定する必要があります**。 宛先が設定されていない場合、オーディエンスは送信され、プロジェクト内の「**[!UICONTROL アクティブ化]**」タブに表示されますが、Experience Platformにはアクティブ化されません。

オーディエンスがアクティブ化されると、Real-Time CDP CollaborationをオリジンとしてExperience Platformの[&#x200B; オーディエンスポータル &#x200B;](#audience-portal)で利用できるようになります。  これらのオーディエンスは、施策や顧客エンゲージメントに活用できます。

### オーディエンスポータル {#audience-portal}

これで、Adobe Experience Platformを宛先として設定したので、アクティベートされたオーディエンスをオーディエンスポータルで表示できます。 オーディエンスポータルは、オーディエンスの表示と管理を可能にするAdobe Experience Platformの中央ハブです。 オーディエンスポータルは、オーディエンスをフィルタリングする際に、Real-Time CDP Collaborationをオリジンとして提供するようになりました。

>[!IMPORTANT]
>
>お客様は、Adobe Experience Platformにアクティベートするオーディエンスに必要なデータ使用ラベルを適用する責任があります。 詳しくは、[&#x200B; データ使用ラベル &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"} ガイドを参照してください。

![&#x200B; フィルターオプションのオリジンとしてReal-Time CDP Collaborationを使用するオーディエンスポータル。](/help/assets/destinations/adobe-experience-platform/audience-portal.png)

オーディエンスポータルについて詳しくは、[&#x200B; オーディエンスポータルの概要](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#manage-audiences){target="_blank"} ガイドを参照してください。
