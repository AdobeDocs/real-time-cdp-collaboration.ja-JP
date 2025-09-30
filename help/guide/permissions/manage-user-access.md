---
title: 権限によるユーザーアクセスの管理
description: Real-Time CDP Collaboration UI の様々なコンポーネントに対する権限とユーザーのアクセスを管理します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0155f6a6-5e67-4415-af96-1848345842e4
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 1%

---

# 権限によるユーザーアクセスの管理 {#manage-user-access}

{{limited-availability-release-note}}

Experience Cloud [ 権限 ](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/abac/permissions-ui/browse){target="_blank"} インターフェイスを使用して、Adobe Real-Time CDP Collaboration内の個々のコンポーネントに対する権限とユーザーアクセスを管理します。 権限を使用すると、システム管理者と製品管理者は [ 役割 ](./manage-roles.md) を定義して、特定の機能とリソースへのユーザーアクセスを管理できます。

## 権限へのアクセスの設定 {#permissions-access}

権限にアクセスするには、Adobe Experience Platform製品への製品管理者とユーザーの両方のアクセス権が必要です。 製品管理者権限を設定するにはシステム管理者が必要ですが、ユーザー権限はシステム管理者または製品管理者が設定できます。 管理者ロールの詳細については、[ アクセス制御階層 ](./overview.md#hierarchy) ガイドを参照してください。

>[!TIP]
>
>このガイド全体を通して、**管理者** とは、システム管理者と製品管理者の両方 **を指し** います。

### システム管理者：製品管理者アクセスの設定 {#admin-access}

次の手順でユーザーに製品管理者アクセス権を付与し、Experience Platform製品内の管理機能を付与します。

>[!IMPORTANT]
>
>システム管理者はAdobe Admin Consoleなどの特定のExperience Cloud製品に標準でアクセスできます。 ただし、権限を使用するには、自分自身にExperience Platform製品の製品管理者およびユーザーアクセス権を付与する必要があります。 システム管理者として自分自身にアクセス権を付与するには、以下のステップバイステップガイドに従います。

資格情報を使用して [0&rbrace;Adobe Experience Cloud&rbrace; にログインします。 ](https://experience.adobe.com/){target="_blank"}ホームビューは、「**[!UICONTROL クイックアクセス]**」セクションに使用可能な製品のリストと共に表示されます。 「**[!UICONTROL Admin Console]**」を選択します。

![Admin Consoleがハイライト表示されたExperience Cloudのホームビュー ](../../assets/permissions/experience-cloud.png){zoomable="yes"}

[Adobe Admin Console](https://adminconsole.adobe.com/) 概要ダッシュボードが表示されます。 **[!UICONTROL 製品とサービス]** の下にある **[!UICONTROL 製品]** リストから **[!UICONTROL 0&rbrace;Adobe Experience Platform&rbrace; を選択します。]**

![Adobe Experience Platform製品がハイライト表示されたAdmin Consoleの概要ダッシュボード。](../../assets/permissions/admin-console.png){zoomable="yes"}

Adobe Experience Platform ダッシュボードが表示されます。 **[!UICONTROL 管理者]** タブを選択してから、**[!UICONTROL 管理者を追加]** を選択します。

![ 「管理者」タブが選択され、「管理者を追加」がハイライト表示されたAdobe Experience Platform製品ダッシュボード。](../../assets/permissions/add-admin.png){zoomable="yes"}

**[!UICONTROL 製品管理者を追加]** ダイアログが表示されます。 ユーザーのメールアドレスまたはユーザー名を「**[!UICONTROL メールまたはユーザー名]**」テキストフィールドに入力し、ドロップダウンから正しいアカウントを選択します。 「**[!UICONTROL 保存]**」を選択して、ユーザーの製品管理者としての追加を終了します。

![ ユーザー情報が入力され、「保存」オプションが選択された製品管理者を追加ダイアログ ](../../assets/permissions/add-product-administrators.png){zoomable="yes"}

製品管理者権限を持ち、Admin Console内の製品に対してユーザーや他の管理者を追加するなどの管理機能を実行できるようになりました。 次に、権限内の機能にアクセスして実行するには、Experience Platform製品へのユーザーアクセス権が必要になります。

### 管理者：Experience Platformへのユーザーアクセスの設定 {#user-access}

ユーザーに製品管理者アクセス権を付与したら、Experience Platform製品へのユーザーアクセス権を付与する必要があります。 アクセス設定の一部として、ユーザー固有の [ 製品プロファイル ](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html) を割り当てます。

>[!TIP]
>
>前の節の手順を実行している場合は、既にAdobe Experience Platform製品に含まれているため、最初の手順をスキップしてもかまいません。

[Admin Console](https://adminconsole.adobe.com/){target="_blank"} に移動し、&lbrace; 製品 **[!UICONTROL リストから &lbrace;2]**&#x200B;**[!UICONTROL Adobe Experience Platform]** を選択します **&#x200B;**

![Admin Consoleがハイライト表示されたExperience Cloudのホームビュー ](../../assets/permissions/experience-cloud.png){zoomable="yes"}

「**[!UICONTROL ユーザー]**」タブを選択し、「**[!UICONTROL ユーザーを追加]**」を選択します。

![ 「ユーザー」タブが選択され、「ユーザーを追加」がハイライト表示されたAdobe Experience Platform製品ダッシュボード。](../../assets/permissions/add-users.png){zoomable="yes"}

**[!UICONTROL この製品にユーザーを追加]** ダイアログが表示されます。 ユーザーの名前またはメールを「**[!UICONTROL 名前、ユーザーグループまたはメールアドレス]**」テキストフィールドに入力し、ドロップダウンから正しいアカウントを選択します。 次に、「**[!UICONTROL 製品]** 追加」オプションを選択します。

![ ユーザー情報が入力され、「製品の追加」オプションが選択された状態で、この製品にユーザーを追加ダイアログ ](../../assets/permissions/add-users-to-product.png){zoomable="yes"}

**[!UICONTROL 製品プロファイルを選択]** ダイアログが表示されます。 「**[!UICONTROL AEP-Default-All-Users]**」と「**[!UICONTROL Default Production All Access]**」を選択し、「**[!UICONTROL 適用]**」を選択します。

![AEP-Default-All-Users と Default Production All Access のオプションが選択され、「適用」がハイライト表示された製品プロファイルを選択ダイアログ ](../../assets/permissions/select-product-profiles.png){zoomable="yes"}

情報が正しいことを確認し、「**[!UICONTROL 保存]**」を選択します。

![ ユーザー情報と製品プロファイルが表示され、「保存」がハイライト表示された製品にユーザーを追加ダイアログ ](../../assets/permissions/save-selections.png){zoomable="yes"}

これで、製品管理者と製品にExperience Platformへのアクセス権が付与され、権限にアクセスできるようになります。 次に、ユーザーに 2 つの基本的な役割を割り当て、Experience Platform UI へのアクセス権を付与する必要があります。

### 管理者：Experience Platform UI アクセスの設定 {#product-access}

Real-Time CDP Collaborationでは、管理者とエンドユーザーは、オーディエンスや監査ログなど、Experience Platformのデータを操作します。 このデータは、サンドボックスと呼ばれるExperience Platformのインスタンス内に保持されます。 ユーザーがこのデータを確実に操作できるようにするには、ユーザーに [ デフォルトの役割 ](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home#default-roles){target="_blank"} を割り当てる必要があります。

開始するには、[Adobe Experience Cloud](https://experience.adobe.com/) に移動します。 **[!UICONTROL クイックアクセス]** 内に **[!UICONTROL 0&rbrace;Experience Platform&rbrace; と]** 権限 **[!UICONTROL が表示されます。]**

![Experience Platformと権限がハイライト表示されたExperience Cloudのホームビュー ](../../assets/permissions/experience-cloud-products.png){zoomable="yes"}

>[!NOTE]
>
> 製品がにアクセスできるようになるまでに数分かかる場合があります。アクセス権が付与されたことを知らせるメールが届きます。 メールの受信後にAdobe Experience CloudにExperience Platformまたは権限が表示されない場合は、ログアウトしてからアカウントにログインし直してください。

この段階で、**[!UICONTROL 権限]** にアクセスできます。 **[!UICONTROL Experience Platform]** にアクセスしようとすると、次に示すように、有効なサンドボックスがないことを示す警告が表示されます。 これを解決するには、ユーザーにデフォルトの役割を割り当てる必要があります。 開始するには、「**[!UICONTROL 権限]**」を選択します。

![ 警告が表示され、権限がハイライト表示されたExperience Cloudのホームビュー ](../../assets/permissions/experience-cloud-warning.png){zoomable="yes"}

**[!UICONTROL 権限]** ダッシュボードが表示されます。 左側のパネルから **ユーザー** を選択し、ユーザー名を選択します。

![ ユーザーワークスペースが表示され、ユーザーがハイライト表示された権限ダッシュボード。](../../assets/permissions/permissions-user.png){zoomable="yes"}

「**[!UICONTROL 役割]**」タブを選択し、「**[!UICONTROL 役割を追加]**」を選択します。

![ 「ロール」タブが表示され、「ロールを追加」がハイライト表示されたユーザーワークスペース。](../../assets/permissions/user-roles.png){zoomable="yes"}

**[!UICONTROL 役割を追加]** ダイアログが表示されます。 「**[!UICONTROL デフォルトの実稼動環境へのすべてのアクセス]**」と「**[!UICONTROL サンドボックス管理者]**」を選択し、「**[!UICONTROL 保存]**」を選択します。

![ デフォルトの実稼動環境のすべてのアクセスおよびサンドボックス管理者が選択され、「保存」がハイライト表示された役割を追加ダイアログ ](../../assets/permissions/add-roles.png){zoomable="yes"}

これで、Experience Platformと権限にアクセスできるようになりました。 最後の手順で、Real-Time CDP Collaborationへのアクセス権を付与します。

### 管理者：Real-Time CDP Collaboration アクセスの設定 {#RTCDP-collaboration-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_permissions"
>title="ユーザーアクセスの管理ガイド"
>abstract=""

ユーザーにCollaborationへのアクセスを許可するには、roles というアクセス制御の概念を使用します。 役割は、管理者またはユーザーが組織内で [ リソース ](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home#permissions) に対して持つアクセスレベルを定義します。

Collaborationへの個々のアクセスを設定する場合は、共同作業リソースから権限を含むユーザーの役割を割り当てます。 [ 役割の管理 ](./manage-roles.md) ガイドを使用して、次の情報を確認できます。

- [2 つの標準の役割 ](./manage-roles.md#standard-roles) と、それらの役割がCollaborationに付与するアクセスレベル
- Collaboration リソースを使用した [ カスタムの役割 ](./manage-roles.md#specific-access-roles) の作成
- 共同作業リソースに含まれる権限のリスト

>[!NOTE]
>
>さらに、ユーザーは、**[!UICONTROL サンドボックス]** リソースの **[!UICONTROL Prod]** 権限を含む役割に割り当てられている必要があります。 両方の標準ロールにこの権限が含まれています。 ユーザーに標準の役割ではなくカスタムの役割を割り当てる場合は、ユーザーに割り当てられているいずれかの役割にこの権限が含まれていることを確認する必要があります。

ユーザーが必要とするアクセスレベルを含む役割を選択または作成したら、その役割にユーザーを割り当てる必要があります。

#### 役割の割り当て

複数の役割を 1 人のユーザーに割り当てることも、複数のユーザーを 1 つの役割に割り当てることもできます。 最初のケースは、Experience Platformへのアクセス権をユーザーに付与する [ デフォルトのロールの割り当て ](#product-access) を行う際に取り上げました。 次の手順では、選択した役割に直接ユーザーを割り当てます。

**[!UICONTROL 権限]** 左側のパネルから **[!UICONTROL 役割]** を選択し、リストから役割を選択します。

![ 役割ワークスペースが表示され、役割がハイライト表示された権限ダッシュボード。](../../assets/permissions/select-role.png){zoomable="yes"}

役割の詳細ページが表示されます。 「**[!UICONTROL ユーザー]**」タブを選択し、「**[!UICONTROL ユーザーを追加]**」を選択します。

![ 「ユーザー」タブが表示され、「ユーザーを追加」がハイライト表示された役割の詳細ワークスペース。](../../assets/permissions/role-users.png){zoomable="yes"}

**[!UICONTROL ユーザーを追加]** ダイアログが表示されます。 リストからユーザーを選択し、「**[!UICONTROL 保存]**」を選択します。

![ ユーザーが選択し、「保存」オプションがハイライト表示されたユーザーを追加ダイアログ ](../../assets/permissions/add-users-to-role.png){zoomable="yes"}

これで、Experience Cloudの **[!UICONTROL クイックアクセス]** の下に商品としてリストされた **[!UICONTROL RTCDP Collaboration]** が表示されます。

![ 「クイックアクセス」の下で「RTCDP Collaboration」製品がハイライト表示されたExperience Cloud](../../assets/permissions/rtcdp-experience-cloud.png)

## 次の手順

これで、ユーザーはReal-Time CDP Collaborationにアクセスできるので、製品の使用を開始できます。 製品全体の詳細については、[ 概要ガイド ](../home.md) を参照してください。
