---
title: Configure and manage your account
description: Learn how to configure and manage various aspects of your account in Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: be7078b16d8126a80cced0a3a8328b465b6ec245
workflow-type: tm+mt
source-wordcount: '1393'
ht-degree: 13%

---

# Configure and manage your account

{{limited-availability-release-note}}

Learn how to set up your account in Real-Time CDP Collaboration to prepare for connections with other collaborators. This guide covers the initial setup of your account, including adding account details, selecting match keys, and managing your account&#39;s settings.

![](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## Set up your account {#set-up-account}

[](#set-up-details)

****![](/help/assets/icons/plus.png)****

![](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### 詳細の設定 {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="連絡先メール"
>abstract="チームまたは役割ベースのメール（**collaboration@yourcompany.com** など）を指定してください。 個人のメールアドレスは使用しないでください。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="接続コード"
>abstract="接続コードは、アカウントの一意の ID です。 これを使用すると、Real-Time CDP Collaboration で他の共同作業者との接続を確立できます。"

To begin configuring your account, you must first set up the account details. This requires you to add the following information:

* ****
* ****
* ************[](/help/guide/overview/roles.md)
* ****************
* ****
* ****
* ****
* Select an image for your account header picture.

>[!NOTE]
>
>********

![](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### 一致キーの設定 {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="一致キー"
>abstract="一致キーは、様々なデータソースからのオーディエンスプロファイルを紐付けるために使用される識別子です。 ブランドで使用できる一致キーを含めます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_setup_match_keys"
>title="一致キー"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ファーストパーティ人物 ID"
>abstract="ハッシュ化されたメールアドレス、ハッシュ化された電話番号、CRM ID などのファーストパーティ人物 ID は、個々のプロファイルに直接接続されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ファーストパーティデバイス ID"
>abstract="ECID や IP アドレスなどのファーストパーティデバイス ID はデバイスに直接接続され、複数の個人間で共有される場合があります。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="サポートされるパートナー ID"
>abstract="パートナー ID は、オーディエンスの紐付けのために外部パートナーによって提供される識別子です。 パートナー ID は、個々のプロファイルに直接接続されません。"

![](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>[](../connect/establishing-connections.md#connection-settings)****

[](./onboard-audiences.md#map-fields)

[](#edit-account)

#### サポートされている一致キー {#supported-match-keys}

Collaboration supports three types of match keys: first-party people IDs, first-party device IDs, and partner IDs. All match keys must meet the following requirements:

* ********
* ****
* If you provide hashed values that use uppercase characters, Collaboration automatically converts them to lowercase.
* ********[](./manage-data-connection.md#match-keys)

##### ファーストパーティ人物 ID

First-party people IDs are directly connected to an individual profile. Currently supported IDs are:

* ****
* ****
* ****
* ****
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ファーストパーティデバイス ID

First-party device IDs are identifiers connected to a specific device. Currently supported IDs are:

* ****
* ****
* ****

##### パートナー ID

パートナー ID は、オーディエンスの紐付けのために外部パートナーによって提供される識別子です。 

* ****

>[!NOTE]
>
>[!DNL AdFixus]****

******************

![](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

****

![](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## Edit account {#edit-account}

After setting up your account, you can edit the details and match keys at anytime.

### 詳細を編集 {#edit-details}

****

************

![](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

****

![](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### 一致キーを編集 {#edit-match-keys}

You can also update the match keys that you initially selected when creating your account. These match keys will determine the match keys available to future connections.

********

![](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

************

>[!IMPORTANT]
>
>[](../glossary.md#sketches)[](./manage-data-connection.md#scheduling)
>
>At this time, match keys cannot be removed once added to your account.

![](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

A success dialog confirms that your account&#39;s match keys are updated successfully.

![](/help/assets/setup/manage-account/match-key-updated-successfully.png){zoomable="yes"}

## 次の手順

[](/help/guide/setup/onboard-audiences.md)
