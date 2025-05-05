---
title: 組織のオンボードと管理
description: Real-Time CDP Collaborationで組織の様々な側面をオンボーディングおよび管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 0de6ab9af8152975f8e0b0f75b1ee0116ed73584
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 14%

---

# 組織のオンボードと管理

{{limited-availability-release-note}}

組織をReal-Time CDP Collaborationにオンボーディングし、会社の様々な側面を管理する方法について説明します。 ここでは、一致キー、優先 ID およびその他のオプションの設定を含め、組織をAdobe Real-Time CDP Collaborationにオンボーディングする手順の概要を説明します。

![ 設定ページ ](/help/assets/setup/manage-organization/my-organization.png){zoomable="yes"}

## 組織の初期設定

最初に、組織と組織の詳細を設定する必要があります。 左側のレールで **[!UICONTROL 設定]** に移動し、右上隅の **+** 記号を選択して **[!UICONTROL アカウント]** を選択します。

>[!TIP]
>
>使用する初期アカウントを設定した後、同じワークフローを使用して、同じ組織内に追加のアカウントを設定できます。

![ アカウントを選択してReal-Time CDP Collaborationに新しい組織を追加する ](/help/assets/setup/manage-organization/add-new-account.png){zoomable="yes"}

組織を設定するワークフローには、次の 2 つのページが含まれます。

* [詳細を設定](#set-up-details)
* [ マッチキーの設定 ](#set-up-match-keys)

>[!IMPORTANT]
>
>組織レベルで選択した *一致キー* は、広告主とパブリッシャーの共同作業により、[ プロジェクトレベル ](/help/guide/collaborate/manage-projects.md) に流れ落ちます。 その後、プロジェクトレベルで一致するキーを削除できますが、この画面で組織レベルで選択されていないキーを追加 *追加することはできません*。

### 詳細を設定 {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="連絡先メール"
>abstract="チームまたは役割ベースの電子メール （`collaboration@yourcompany.com` など）を指定してください。 個人または個人のメールアドレスは使用しないでください。"

![ 組織を設定するための詳細とユースケースの手順 ](/help/assets/setup/manage-organization/add-organization-details.png){zoomable="yes"}

1. 会社の **[!UICONTROL 組織名]** を追加します。
2. 会社について **[!UICONTROL 説明]** を追加します。
3. **[!UICONTROL 会社の役割]** を選択します。 **[!UICONTROL 広告主]** と **[!UICONTROL 公開者]** の中から選択できます。 2 つの組織の役割タイプのワークフローの類似点とわずかな違いについて詳しくは、[ エンドツーエンドのワークフロードキュメント ](/help/guide/end-to-end-workflow.md) を参照してください。
4. 組織の **[!UICONTROL 業界]** を選択します。 例として、**[!UICONTROL 小売]**、**[!UICONTROL 電気通信]**、または **[!UICONTROL 金融サービス]** があります。
5. 組織の **[!UICONTROL 地域]** を選択します。 製品の現在のバージョンでは、**[!UICONTROL 北米]** がプリセットのデフォルトの選択です。
6. 組織の **[!UICONTROL 連絡先メール]** を追加します。 チームまたは役割ベースのメールアドレスを指定してください。 個人のメールアドレスは指定しないでください。
7. <span class="preview"> パブリッシャーのみ </span>：パブリッシャー組織を設定する場合、パブリッシャーカタログの広告主によって検出可能であることを読み、確認する必要があります。
   ![ 発行者固有のオプトインメッセージ。](/help/assets/setup/manage-organization/publisher-specific-optin-message.png){zoomable="yes"}
8. 会社の **[!UICONTROL ロゴ]** をアップロードします。 現在、SVGタイプの画像がサポートされています。
9. 会社のヘッダー画像の画像を選択します。

選択内容に問題がなければ、「**[!UICONTROL 次へ]**」を使用して次のページに進み、組織で使用する必要のある一致キーを選択します。

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

一致キー（メールアドレス、デバイス ID、顧客 ID など）は、広告主とパブリッシャーが正確でプライバシーを中心としたデータ同期を可能にすることで連携するのに役立ち、より正確なオーディエンスのターゲティングと測定が可能になります。

![Real-Time CDP Collaborationの最初のリリースで使用可能な識別子を示すスライド ](/help/assets/setup/manage-organization/available-identifiers.png)

パブリッシャーおよび広告主オーディエンスのメンバーを紐付けするときに使用する、任意の一致キーを選択します。 会社が使用できる一致キーを含めます。 将来に備えて計画を立て、今後のパブリッシャー/広告主キャンペーンで使用すると予想される一致キーを選択します。 組織の追加の一致キーを選択する必要がある場合は、後の [ 組織を編集 ](#edit-organization) ワークフローでも選択できます。

![ キーの一致の選択ステップ ](/help/assets/setup/manage-organization/add-organization-match-keys.png){zoomable="yes"}

使用する予定の一致キーを最大 5 つ選択します。 後で接続を設定するときに、不要なマッチ キーを削除することはできますが、新しいマッチ キーを追加することはできません。

Real-Time CDP Collaborationで使用できる一致キーは、次の 3 つのタイプです。

* ファーストパーティ人物 ID
* ファーストパーティデバイス ID
* パートナー ID

Real-Time CDP Collaborationの最初のリリースで使用できる一致キーは次のとおりです。

* ハッシュ化されたメール

<!--

not available in the Limited GA release

* Hashed phone
* IPv4

-->

準備ができたら、「**[!UICONTROL 完了]**」を選択して、組織設定ワークフローを終了します。

## 組織を編集 {#edit-organization}

組織を最初に設定した後、組織の特定の側面や詳細をいつでも編集できます。 **[!UICONTROL 組織を編集するには、「自分の組織]** ビューで **[!UICONTROL 編集]** を選択します。

![ ハイライト表示された「組織の編集」コントロール ](/help/assets/setup/manage-organization/edit-organization.png){zoomable="yes"}

この時点で、組織名、説明、ロゴおよび組織プロファイル画像を更新できます。

![ 組織の編集可能オプション。](/help/assets/setup/manage-organization/editable-options.png){zoomable="yes"}

また、組織にオンボーディングする際に最初に選択した一致キーを更新したり、一致キーに対応する ID の最小しきい値を更新して、オーディエンスの重複やその他の製品領域で表示および使用できるようにすることもできます。 **[!UICONTROL 一致キー]** タブで **[!UICONTROL 編集]** を選択し、目的の一致キーを追加するか、ID しきい値を更新します。

![ 一致キーを編集 ](/help/assets/setup/manage-organization/edit-match-keys.png){zoomable="yes"}

## 次の手順

組織を設定したら、Real-Time CDP Collaborationに [ オーディエンスを読み込む ](/help/guide/setup/onboard-audiences.md) 準備が整います。
