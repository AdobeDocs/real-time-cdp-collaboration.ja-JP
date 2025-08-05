---
title: アカウントの設定と管理
description: Real-Time CDP Collaborationでアカウントの様々な側面を設定および管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 18%

---

# アカウントの設定と管理

{{limited-availability-release-note}}

他の共同作業者との連携に備えて、Real-Time CDP Collaborationでアカウントを設定する方法を説明します。 このガイドでは、アカウントの詳細の追加、一致キーの選択、アカウントの設定の管理など、アカウントの初期設定について説明します。

![ 設定済みのアカウントが表示されている設定ワークスペース ](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## アカウントの設定 {#set-up-account}

初めてCollaborationにアクセスすると、アカウントを設定するよう求められます。 これは、アカウントの詳細と一致キーを設定できる 1 回限りのプロセスです。 組織の最初のアカウントの場合は、[ アカウントの詳細 ](#set-up-details) の設定からオンボーディングプロセスが直ちに開始されます。

組織を追加するには、左側のパネルで **[!UICONTROL 設定]** に移動し、「追加」アイコン（「![ 追加」アイコン）を選択します。](/help/assets/icons/plus.png)）を選択します。 次に、「**[!UICONTROL アカウント]**」を選択します。

![ 「マイアカウント」タブと「アカウント」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### 詳細の設定 {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="連絡先メール"
>abstract="チームまたは役割ベースのメール（**collaboration@yourcompany.com** など）を指定してください。個人のメールアドレスは使用しないでください。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="接続コード"
>abstract="接続コードは、アカウントの一意の ID です。これを使用すると、Real-Time CDP Collaboration で他の共同作業者との接続を確立できます。"

アカウントの設定を開始するには、まずアカウントの詳細を設定する必要があります。 これには、次の情報を追加する必要があります。

* ブランドを明確に表す **[!UICONTROL アカウント名]** を追加します。
* ブランドについて **[!UICONTROL 説明]** を追加します。 これはオプションですが、他の共同作業者がブランドをより深く理解するのに役立ちます。
* **[!UICONTROL 役割]** を選択します。 **[!UICONTROL 広告主]** と **[!UICONTROL 公開者]** の中から選択できます。 2 つのアカウントロールタイプのワークフローの類似点とわずかな違いについては、[roles](/help/guide/overview/roles.md) ガイドを参照してください。
<!-- The above will need to be updated when I update things for B2B -->
* アカウントの **[!UICONTROL 業界]** を選択します。 例として、**[!UICONTROL 小売]**、**[!UICONTROL 電気通信]**、または **[!UICONTROL 金融サービス]** があります。
* **[!UICONTROL 地域]** は、Adobe Experience Cloud アカウントに基づいて自動的に設定されます。 これはいつでも変更できません。
* アカウントに **[!UICONTROL 連絡先メール]** を追加します。 チームまたは役割ベースのメールアドレスを指定してください。 個人のメールアドレスは指定しないでください。
* アカウントに **[!UICONTROL ロゴ]** をアップロードします。 現在、SVGタイプの画像がサポートされています。 これはオプションですが、ロゴをアップロードすると、Collaboration インターフェイスでブランドを視覚的に表すのに役立ちます
* アカウントのヘッダー画像の画像を選択します。

>[!NOTE]
>
>これらの詳細のほとんどは、いつでも編集できますが、初期設定後は **[!UICONTROL 役割]** を編集できません。 完了したら、「**[!UICONTROL 次へ]** を使用して次のページに進み、組織で使用する目的の一致キーを選択します。

![ 「詳細」セクションが表示され、「次へ」オプションがハイライト表示されたアカウントの設定ワークスペース。](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

### 一致キーの設定 {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="一致キー"
>abstract="一致キーは、様々なデータソースのオーディエンス間でメンバーを紐付けるために使用される識別子です。ブランドで使用できる一致キーを含めます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ファーストパーティユーザー ID"
>abstract="ハッシュ化されたメールアドレスや電話番号などのファーストパーティ人物 ID は、個々のプロファイルに直接接続されます。現在サポートされている ID は、ハッシュ化されたメールと電話番号です。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_deviceIDs"
>title="ファーストパーティデバイス ID"
>abstract="ECID や IP アドレスなどのファーストパーティデバイス ID はデバイスに直接接続され、複数の個人間で共有される場合があります。現在サポートされているファーストパーティデバイス ID は IPv4 のみです。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="サポートされるパートナー ID"
>abstract="プロファイルに関連付けられたパートナー ID により、特定のプロファイルへのリーチが拡張されます。"

>[!IMPORTANT]
>
>アカウントの設定時に選択した一致キーによって、他の共同作業者と作成する接続で使用できる一致キーが決まります。 接続の設定中に一致キーを削除できますが、新しい一致キーを追加することはできません。 アカウントの設定中に、今後のキャンペーンで使用する予定の **すべて** 一致キーを選択することが重要です。

一致キー（メールアドレス、デバイス ID、顧客 ID など）は、コラボレーターが正確でプライバシーを中心としたデータ同期を可能にすることで連携するのに役立ち、より正確なオーディエンスターゲティングと測定が可能になります。

![Collaborationの最初のリリースで使用可能な識別子を示すスライド ](/help/assets/setup/manage-account/available-identifiers.png)

<!-- Eventually replace this image above to match branding better. -->

オーディエンスプロファイルを紐付ける際に使用する一致キーを選択します。 使用できる一致キーを含めます。 将来のキャンペーンを計画し、将来のキャンペーンで使用すると予想される一致キーを選択します。 後でアカウントに追加の一致キーを選択する必要がある場合は、[ アカウントを編集 ](#edit-account) ワークフローで選択できます。

使用する予定の一致キーを最大 5 つ選択します。 後で接続を設定するときに、不要なマッチ キーを削除することはできますが、新しいマッチ キーを追加することはできません。

使用できる一致キーには 3 つのタイプがあります。

* ファーストパーティユーザー ID
* ファーストパーティデバイス ID
* パートナー ID

>[!IMPORTANT]
>
>現在、サポートされている一致キーはハッシュ化されたメールのみです。

準備ができたら、「**[!UICONTROL 完了]**」を選択して、組織設定ワークフローを終了します。

![ 「キーの一致」セクションが表示された組織ワークスペースの設定 ](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## アカウントを編集 {#edit-account}

アカウントを設定した後、いつでもアカウントの特定の側面や詳細を編集します。 **[!UICONTROL アカウントを編集するには、「設定]** ワークスペースの **[!UICONTROL マイアカウント]** セクションで ** 編集** を選択します。

![ 「マイアカウント」タブと「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

**[!UICONTROL 役割]** を除くアカウントの詳細を編集できるようになりました。 リージョンは、Adobe Experience Cloud アカウントに基づいて自動的に設定され、いつでも変更できないことに注意してください。

![ アカウントの詳細を編集ダイアログ。](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

また、組織のオンボーディング時に最初に選択した一致キーを更新することもできます。 **[!UICONTROL 一致キー]** セクションの **[!UICONTROL 編集]** を選択して、必要な一致キーを追加します。

![ アカウントの「一致キー」セクション内で「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

## 次の手順

アカウントを設定したら、Real-Time CDP Collaborationに [ オーディエンスをソース ](/help/guide/setup/onboard-audiences.md) する準備が整います。
