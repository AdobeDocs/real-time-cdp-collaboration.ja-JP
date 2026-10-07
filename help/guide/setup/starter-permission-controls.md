---
title: Collaboration [!DNL Starter] オンボーディングの権限コントロールの設定
description: Adobe Experience Cloudの権限を使用して、Adobe Real-Time CDP Collaboration [!DNL Starter]の権限を設定する方法について説明します。
audience: users invited to Real-Time CDP Collaboration [!DNL Starter]
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 4e50b6cc-58f7-4a0c-8b6d-f5aa4f092e9f
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
    internal-label: Real-Time Customer Data Platform
source-git-commit: 5b308de53e76129c8d5f3870ff4646424c2dd69e
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 2%
---
# Collaboration [!DNL Starter] オンボーディングの権限コントロールの設定

Adobe Experience Platform製品への管理者およびユーザーアクセス権を設定したら、Real-Time CDP Collaborationの適切な権限を自分に割り当てる必要があります。 このガイドでは、Experience Cloud権限インターフェイスを使用して適切な役割をアカウントに追加し、Collaboration機能へのユーザーアクセスにアクセスして管理する方法について説明します。

Collaboration リソースに含まれる標準ロールと使用可能な権限について詳しくは、[役割の管理方法ガイド &#x200B;](../permissions/manage-roles.md)を参照してください。

## 前提条件 {#prerequisites}

Adobe Experience Platform製品への&#x200B;**管理者権限**&#x200B;と&#x200B;**ユーザーアクセス**&#x200B;の両方があることを確認してください。 これらのアクセス レベルをまだ設定していない場合は、手順を説明する手順については、[管理者アクセス ガイド &#x200B;](./starter-admin-access.md)を参照してください。

## 権限の設定 {#setup-permissions}

Collaborationに必要な権限を設定するには、次の手順に従います。 まず、資格情報を使用して[Adobe Experience Cloud](https://experience.adobe.com/)にログインします。

### アクセス権限 {#access-permissions}

ログインしたら、**[!UICONTROL クイックアクセス]** セクションに移動し、**[!UICONTROL 権限]**&#x200B;を選択します。 権限ダッシュボードが開き、必要な役割を自分に割り当てることができます。

クイックアクセス セクション内の権限が強調表示された![Experience Cloud ホームページ。](../../assets/setup/starter/access-permissions.png){zoomable="yes"}

### ユーザーの選択 {#select-user}

**[!UICONTROL 権限]** ダッシュボードで、左側のパネルから&#x200B;**[!UICONTROL ユーザー]**&#x200B;を選択します。 次に、「ユーザー」テーブルからアカウントを選択します。

>[!NOTE]
>
> 組織の最初のユーザーがExperience Platformにアクセスする場合は、**Users** テーブルにリストされている唯一のユーザーである可能性があります。 追加のチームメンバーを招待するには、[&#x200B; ユーザーアクセス設定ガイド &#x200B;](../permissions/manage-user-access.md#administrators-configure-user-access-to-experience-platform)の手順に従います。

![権限ダッシュボードには、ユーザーアカウントがハイライト表示されたユーザーテーブルが表示されます。](../../assets/setup/starter/select-user.png){zoomable="yes"}

### 役割の割り当て {#assign-roles}

対応する&#x200B;**[!UICONTROL ユーザー]** ワークスペースで、「**[!UICONTROL 役割]**」タブに移動します。 次に、**[!UICONTROL 役割を追加]**&#x200B;を選択します。

![対応するユーザーワークスペースに「役割」タブが表示され、「役割を追加」オプションが強調表示されます。](../../assets/setup/starter/add-roles.png){zoomable="yes"}

**[!UICONTROL 役割を追加]** ダイアログが表示され、使用可能な役割のテーブルが表示されます。 テーブルの各行は、次の情報を持つ役割を表します。

| **列** | **説明** |
|---------------|--------------------------------------------------------|
| **名前** | 役割の名前。 |
| **説明** | 役割の機能を説明する短い要約。 「読み取り専用」の役割はカスタマイズできません。 |
| **サンドボックス** | 役割がアクセスを提供するサンドボックス （例：`Prod`）を指定します。 |
| **変更** | 役割が最後に更新された日付 |

{style="table-layout:auto"}

特定の役割とその権限について詳しくは、[役割の権限の管理](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/abac/permissions-ui/permissions) ガイドを参照してください。

情報を確認し、アカウントに割り当てる役割を選択します。 完了したら、**[!UICONTROL 保存]**&#x200B;を選択します。

![役割を追加ダイアログに、選択した役割と保存オプションが強調表示されます。](../../assets/setup/starter/add-roles-dialog.png){zoomable="yes"}

確認ダイアログは、新しい役割が正常に追加されたことを確認します。

権限が正しく設定されていることを確認するには、[Experience Cloud](https://experience.adobe.com/) ホームページに戻ります。 **[!UICONTROL クイックアクセス]**&#x200B;内の&#x200B;**[!UICONTROL Real-Time CDP Collaboration]**&#x200B;を選択します。 Collaboration Workspaceにアクセスし、[!DNL Starter] アカウントで利用可能な機能の使用を開始できる必要があります。

## 次の手順 {#next-steps}

権限を設定したら、Collaborationにアクセスする準備が整います。 次に、次のことができます。

* [異なるアクセス レベルを管理するための特定の権限を持つカスタム ロールを作成します](../permissions/manage-roles.md#create-specific-access-roles)。
* [複数のユーザーを権限](../permissions/manage-user-access.md#assign-a-role)の1つの役割に割り当てます。
* [Collaboration アカウントを設定し、招待している共同作業者](../overview/starter-overview.md#set-up-connections)とのつながりを確立します。
* [Collaborationでのクレジットの使用と使用について詳しく見る [!DNL Starter]](./starter-credit-usage.md)。

Real-Time CDP Collaborationとその主な機能について詳しくは、[概要ガイド &#x200B;](../home.md)を参照してください。
