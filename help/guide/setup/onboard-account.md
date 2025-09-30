---
title: アカウントの設定と管理
description: Real-Time CDP Collaborationでアカウントの様々な側面を設定および管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: 0dead396657c97cec47ddd64c8ec3c349f541a8f
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 14%

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
>abstract="一致キーは、様々なデータソースからのオーディエンスプロファイルを紐付けるために使用される識別子です。ブランドで使用できる一致キーを含めます。"

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
>abstract="ECID や IP アドレスなどのファーストパーティデバイス ID はデバイスに直接接続され、複数の個人間で共有される場合があります。現在サポートされているファーストパーティデバイス ID は IPv4 のみです。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_organization_onboarding_partnerIDs"
>title="サポートされるパートナー ID"
>abstract="パートナー ID は、オーディエンスの紐付けのために外部パートナーによって提供される識別子です。パートナー ID は、個々のプロファイルに直接接続されません。"

![ サポートされる一致キー。](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>アカウントの設定時に選択した一致キーによって、接続内で使用可能な一致キーが決まります。 接続の設定中に [ 不要な一致キーを削除 ](../connect/establishing-connections.md#connection-settings) できますが、接続が確立された後に一致キーを追加することはできません。 アカウントの設定中に、今後のキャンペーンで使用する予定の **すべて** 一致キーを選択することが重要です。

一致キーは、正確でプライバシーを中心としたデータ同期を可能にし、より正確なオーディエンスのターゲティングと測定を可能にすることで、共同作業者が連携するのに役立ちます。 アカウント設定時に選択した一致キーによって、今後の接続で使用できる一致キーが決まります。 また、オーディエンスをソーシングする際に、データ接続からCollaborationのターゲットフィールドに [ マッピング ](./onboard-audiences.md#map-fields) するために使用されます。

オーディエンスプロファイルを紐付ける際に使用する一致キーを選択します。 将来に備えて計画を立て、連携できる一致キーを含め、将来のキャンペーンで使用を予測します。 後でアカウントに追加の一致キーを選択する必要がある場合は、[ アカウントを編集 ](#edit-account) ワークフローで選択できます。 ただし、初期セットアップの後に追加されたマッチ キーは、既存の接続では使用できません。

#### サポートされている一致キー {#supported-match-keys}

Collaborationでは、ファーストパーティの人物 ID、ファーストパーティのデバイス ID、パートナー ID の 3 種類の一致キーをサポートしています。 すべての一致キーは、次の要件を満たす必要があります。

* 一致キーは、**トリム**、**小文字** である必要があります
* ハッシュ化された一致キーは、**SHA256 ハッシュ化** されている必要があります。
* 大文字を使用するハッシュ値を指定すると、Collaborationによって自動的に小文字に変換されます。
* ソースに **プレーンテキスト識別子** が含まれている場合は、**[!UICONTROL データ接続の設定]** 中に [ 変換を適用 ](./manage-data-connection.md#match-keys) オプションを使用してハッシュを適用します。 このオプションは、Experience Platformからオーディエンスを取得する場合にのみ使用でき、クラウドベースのソースではサポートされません。

##### ファーストパーティ人物 ID

ファーストパーティの人物 ID は個人プロファイルに直接接続されます。 現在サポートされている ID は次のとおりです。

* **[!UICONTROL ハッシュ化されたメール]**
* **[!UICONTROL ハッシュ化された電話]**
* **[!UICONTROL CRM ID]**
* **[!UICONTROL ロイヤルティ ID]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ファーストパーティデバイス ID

ファーストパーティデバイス ID は、特定のデバイスに接続される識別子です。 現在サポートされている ID は次のとおりです。

* **[!UICONTROL ハッシュ化された IPv4]**：ハッシュ化された IPv4 アドレス

##### パートナー ID

パートナー ID は、オーディエンスの紐付けのために外部パートナーによって提供される識別子です。現在サポートされている ID は次のとおりです。

* **[!UICONTROL Adfixus ID]**

>[!NOTE]
>
>Adobeと [!DNL Adfixus] の統合により、各アカウントの一意の [!UICONTROL Adfixus ID] が、共通のAdobeでエンコードされた形式にマップされます。 これらのマッピングは、共同作業者間の重複を識別するために使用されます。 **[!UICONTROL 付加 ID]** を使用してオーディエンスをアクティブ化する場合、元の ID が使用されます。 Adobeでエンコードされた形式は、Collaborationから移動されません。

**[!UICONTROL Adfixus ID]** を選択する場合、**[!UICONTROL アカウント資格情報]** セクションで、外部パートナーから対応する ID を指定する必要があります。 このオプションは、*Adfixus ID* を切り替える **[!UICONTROL after]** でのみ使用できます。 Adfixus ID を **[!UICONTROL アカウント ID]** フィールドに入力します。値が正確かどうか再確認してください。

![Adfixus ID が切り替えられ、「アカウント資格情報」セクションがハイライト表示されたキーを一致ダイアログ ](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

必要な一致キーをすべて選択したら、「**[!UICONTROL 完了]**」を選択して、アカウント設定ワークフローを終了します。

![ 一致するキーのセクションが表示されたアカウントを設定ワークスペース。](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## アカウントを編集 {#edit-account}

アカウントの設定後、いつでも詳細を編集してキーを照合できます。

### 詳細を編集 {#edit-details}

アカウントの詳細の大部分は、**[!UICONTROL 役割]** を除き、いつでも編集できます。 このリージョンは、Adobe Experience Cloud アカウントに基づいて自動的に設定され、変更できません。

アカウントを編集するには、**[!UICONTROL 設定]** ワークスペースの **[!UICONTROL マイアカウント]** セクションで **[!UICONTROL 編集]** を選択します。

![ 「マイアカウント」タブと「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

アカウントの詳細を編集できるようになりました。 変更するフィールドがあれば更新し、「**[!UICONTROL 保存]**」を選択して変更を確定します。

![ アカウントの詳細を編集ダイアログ。](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### 一致キーを編集 {#edit-match-keys}

>[!IMPORTANT]
>
>一致キーを編集しても、既存の接続には影響しません。 接続が確立されると、接続設定時に選択した一致キーが固定されます。 アカウントの設定中に、今後のキャンペーンで使用する予定の **すべて** 一致キーを選択することが重要です。

また、アカウントの作成時に最初に選択した一致キーを更新することもできます。 これらの一致キーは、今後の接続で使用できる一致キーを決定します。

**[!UICONTROL 一致キー]** セクションの **[!UICONTROL 編集]** を選択します。

![ アカウントの「一致キー」セクション内で「編集」オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

**[!UICONTROL キーを一致]** ダイアログが表示されます。 任意の一致キーのオン/オフを切り替えるか、**[!UICONTROL Adfixus ID]** の [!UICONTROL &#x200B; アカウント ID] を更新してから、「**[!UICONTROL 保存]**」を選択して変更を確定します。

>[!IMPORTANT]
>
>[!UICONTROL Adfixus ID] を変更しても、マッチ キーを使用して既存のデータ接続の [ データ スケッチ ](../glossary.md#sketches) 更新がトリガーされることはありません。 データをスケッチすると、[!UICONTROL &#x200B; データ接続スケジュール &#x200B;] 設定に従って次回オーディエンスを更新するまで、[Adfixus ID](./manage-data-connection.md#scheduling) に対する変更は反映されません。 次回の更新の前に変更が必要な場合は、データ接続を削除して再作成できます。

![ 「保存」オプションがハイライト表示されたキーを一致させるダイアログ ](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

## 次の手順

アカウントを設定したら、Real-Time CDP Collaborationに [ オーディエンスをソース ](/help/guide/setup/onboard-audiences.md) する準備が整います。
