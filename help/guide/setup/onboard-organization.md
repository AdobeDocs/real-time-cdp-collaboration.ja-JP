---
title: 組織のオンボードと管理
description: Real-Time CDP Collaborationで組織の様々な側面をオンボーディングおよび管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 860138b95abc4d6af94bbbf722cf498463570c1b
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 16%

---

# 組織のオンボードと管理

{{limited-availability-release-note}}

組織をReal-Time CDP Collaborationにオンボーディングし、会社の様々な側面を管理する方法について説明します。 ここでは、一致キー、優先 ID およびその他のオプションの設定を含め、組織をAdobe Real-Time CDP Collaborationにオンボーディングする手順の概要を説明します。

![ 組織の設定ワークスペースに現在の設定が表示されます。](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## 組織の初期設定

最初に、組織と組織の詳細を設定する必要があります。 これが最初の組織の場合は、[ アカウントの詳細 ](#set-up-details) の設定からオンボーディングプロセスが直ちに開始されます。

組織を追加するには、左側のパネルで **[!UICONTROL 設定]** に移動し、「追加」アイコン（「![ 追加」アイコン）を選択します。](/help/assets/icons/plus.png)）を選択します。 次に、「**[!UICONTROL アカウント]**」を選択します。

![ アカウントオプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

### 詳細の設定 {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="連絡先メール"
>abstract="チームまたは役割ベースのメール（`collaboration@yourcompany.com` など）を指定してください。個人のメールアドレスは使用しないでください。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="接続コード"
>abstract="接続コードは組織の一意の ID です。 Real-Time CDP Collaboration内の他の組織との接続を確立するために使用されます。"

<!-- Move the above to new section for invite on this page when its created -->

組織のオンボーディングを開始するには、まず組織の詳細を設定する必要があります。 これには、次の情報を追加する必要があります。

* 会社の **[!UICONTROL 組織名]** を追加します。
* 会社について **[!UICONTROL 説明]** を追加します。
* **[!UICONTROL 会社の役割]** を選択します。 **[!UICONTROL 広告主]** と **[!UICONTROL 公開者]** の中から選択できます。 2 つの組織の役割タイプのワークフローの類似点とわずかな違いについて詳しくは、[ エンドツーエンドのワークフロードキュメント ](/help/guide/end-to-end-workflow.md) を参照してください。
* 組織の **[!UICONTROL 業界]** を選択します。 例として、**[!UICONTROL 小売]**、**[!UICONTROL 電気通信]**、または **[!UICONTROL 金融サービス]** があります。
* 組織の **[!UICONTROL 地域]** を選択します。 製品の現在のバージョンでは、**[!UICONTROL 北米]** がプリセットのデフォルトの選択です。
* 組織の **[!UICONTROL 連絡先メール]** を追加します。 チームまたは役割ベースのメールアドレスを指定してください。 個人のメールアドレスは指定しないでください。
* 会社の **[!UICONTROL ロゴ]** をアップロードします。 現在、SVGタイプの画像がサポートされています。
* 会社のヘッダー画像の画像を選択します。

>[!NOTE]
>
>これらの詳細のほとんどは、いつでも編集できますが、初期設定後は **[!UICONTROL 役割]** および **[!UICONTROL 地域]** は編集できません。

![ 詳細セクションが表示された組織ワークスペースの設定。](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

完了したら、「**[!UICONTROL 次へ]** を使用して次のページに進み、組織で使用する目的の一致キーを選択します。

### 一致キーの設定 {#set-up-match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_matchkeys"
>title="一致キー"
>abstract="一致キーは、様々なデータソースのオーディエンス間でメンバーを紐付けるために使用される識別子です。会社で使用できる一致キーを含めます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_peopleIDs"
>title="ファーストパーティ人物 ID"
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
>組織の設定時に選択した一致キーによって、他の組織との接続に使用できる一致キーが決まります。 接続のセットアップ中にマッチ キーを削除できますが、後で新しいマッチ キーを追加することはできません。 組織の設定中に、今後のキャンペーンで使用する予定のすべての一致キーを選択することが重要です。

一致キー（メールアドレス、デバイス ID、顧客 ID など）は、広告主とパブリッシャーが正確でプライバシーを中心としたデータ同期を可能にすることで連携するのに役立ち、より正確なオーディエンスのターゲティングと測定が可能になります。

![Real-Time CDP Collaborationの最初のリリースで使用可能な識別子を示すスライド ](/help/assets/setup/manage-organization/available-identifiers.png)

パブリッシャーおよび広告主オーディエンスのメンバーを紐付けするときに使用する、任意の一致キーを選択します。 会社が使用できる一致キーを含めます。 将来に備えて計画を立て、今後のパブリッシャー/広告主キャンペーンで使用すると予想される一致キーを選択します。 組織の追加の一致キーを選択する必要がある場合は、後の [ 組織を編集 ](#edit-organization) ワークフローでも選択できます。

![ 「キーの一致」セクションが表示された組織ワークスペースの設定 ](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

使用する予定の一致キーを最大 5 つ選択します。 後で接続を設定するときに、不要なマッチ キーを削除することはできますが、新しいマッチ キーを追加することはできません。

Real-Time CDP Collaborationで使用できる一致キーは、次の 3 つのタイプです。

* ファーストパーティ人物 ID
* ファーストパーティデバイス ID
* パートナー ID

Real-Time CDP Collaborationの最初のリリースで使用できる一致キーは次のとおりです。

* ハッシュ化されたメール

準備ができたら、「**[!UICONTROL 完了]**」を選択して、組織設定ワークフローを終了します。

## 組織を編集 {#edit-organization}

組織を最初に設定した後、組織の特定の側面や詳細をいつでも編集できます。 **[!UICONTROL 組織を編集するには、「設定]** ワークスペースの **[!UICONTROL 自分の組織]** セクションで **&#x200B; 編集** を選択します。

![ 「自分の組織」タブと「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

**[!UICONTROL 役割]** および **[!UICONTROL 地域]** を除く、組織の詳細を編集できるようになりました。

![ 組織の詳細を編集ダイアログ ](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

また、組織のオンボーディング時に最初に選択した一致キーを更新することもできます。 **[!UICONTROL 一致キー]** セクションの **[!UICONTROL 編集]** を選択して、必要な一致キーを追加します。

![ 組織の「一致キー」セクション内で「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## 次の手順

組織を設定したら、Real-Time CDP Collaborationに [ オーディエンスを読み込む ](/help/guide/setup/onboard-audiences.md) 準備が整います。
