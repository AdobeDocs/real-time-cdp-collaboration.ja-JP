---
title: アカウントの設定と管理
description: Real-Time CDP Collaborationでアカウントのさまざまな側面を設定および管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: a95e932a-9681-48f2-bf34-6fe5a50597d7
source-git-commit: be7078b16d8126a80cced0a3a8328b465b6ec245
workflow-type: tm+mt
source-wordcount: '1393'
ht-degree: 13%

---

# アカウントの設定と管理

{{limited-availability-release-note}}

Real-Time CDP Collaborationでアカウントを設定して、他の共同作業者とのつながりに備える方法について説明します。 このガイドでは、アカウントの詳細の追加、照合キーの選択、アカウントの設定の管理など、アカウントの初期設定について説明します。

![設定されたアカウントを表示する設定ワークスペース。](/help/assets/setup/manage-account/my-account.png){zoomable="yes"}

## アカウントの設定 {#set-up-account}

最初にCollaborationにアクセスすると、アカウントの設定を求めるメッセージが表示されます。 これは、アカウントの詳細を設定し、キーを照合するための1回限りのプロセスです。 これが組織の最初のアカウントの場合は、すぐにオンボーディングプロセスを介して、[&#x200B; アカウントの詳細](#set-up-details)の設定を開始します。

組織を追加するには、左側のパネルの&#x200B;**[!UICONTROL 設定]**&#x200B;に移動し、追加アイコン（![追加アイコン &#x200B;](/help/assets/icons/plus.png)）を選択します。 右上隅にあります。 次に、**[!UICONTROL アカウント]**&#x200B;を選択します。

![&#x200B; マイアカウントタブとアカウントオプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/add-new-account.png){zoomable="yes"}

### 詳細の設定 {#set-up-details}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_contact_email"
>title="連絡先メール"
>abstract="チームまたは役割ベースのメール（**collaboration@yourcompany.com** など）を指定してください。 個人のメールアドレスは使用しないでください。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_setup_connect_code"
>title="接続コード"
>abstract="接続コードは、アカウントの一意の ID です。 これを使用すると、Real-Time CDP Collaboration で他の共同作業者との接続を確立できます。"

アカウントの設定を開始するには、最初にアカウントの詳細を設定する必要があります。 これには、次の情報を追加する必要があります。

* ブランドを明確に表す&#x200B;**[!UICONTROL アカウント名]**&#x200B;を追加します。
* ブランドに関する&#x200B;**[!UICONTROL 説明]**&#x200B;を追加します。 これはオプションですが、他の共同作業者がブランドをより深く理解するのに役立ちます。
* **[!UICONTROL 役割]**&#x200B;を選択します。 **[!UICONTROL 広告主]**&#x200B;と&#x200B;**[!UICONTROL 発行者]**&#x200B;の間を選択できます。 [roles](/help/guide/overview/roles.md) ガイドを読んで、2つのアカウントの役割タイプ間の類似点とワークフローのわずかな違いを確認してください。
* アカウントの&#x200B;**[!UICONTROL Industry]**&#x200B;を選択します。 例としては、**[!UICONTROL 小売]**、**[!UICONTROL 通信]**、**[!UICONTROL 金融サービス]**&#x200B;などがあります。
* **[!UICONTROL 地域]**&#x200B;は、Adobe Experience Cloud アカウントに基づいて自動的に設定されます。 この設定はいつでも変更できません。
* アカウントの&#x200B;**[!UICONTROL お問い合わせメール]**&#x200B;を追加します。 これは、チームまたは役割ベースのメールアドレスである必要があります。 個人のメールアドレスは提供しないでください。
* アカウントの&#x200B;**[!UICONTROL ロゴ]**&#x200B;をアップロードします。 現在、SVG型の画像がサポートされています。 これはオプションですが、ロゴをアップロードすると、Collaboration インターフェイスでブランドを視覚的に表現するのに役立ちます
* アカウントヘッダー画像の画像を選択します。

>[!NOTE]
>
>これらの詳細のほとんどは、いつでも編集できますが、最初のセットアップ後に&#x200B;**[!UICONTROL 役割]**&#x200B;を編集することはできません。 完了したら、**[!UICONTROL 次の]**&#x200B;を使用して次のページに進み、組織で使用する照合キーを選択します。

![詳細セクションが表示され、次のオプションがハイライト表示されたアカウント設定ワークスペース。](/help/assets/setup/manage-account/add-account-details.png){zoomable="yes"}

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

![一致キーをサポートしています。](/help/assets/setup/manage-account/match-keys.png){zoomable="yes"}

>[!IMPORTANT]
>
>アカウントの設定中に選択した照合キーによって、接続内で使用可能な照合キーが決まります。 接続設定中に[不要な一致キー](../connect/establishing-connections.md#connection-settings)を削除できますが、接続が確立された後に一致キーを追加することはできません。 アカウントの設定中に、今後のキャンペーンで使用する予定の&#x200B;**all**&#x200B;一致キーを選択することが重要です。

マッチキーは、正確でプライバシーを重視したデータ同期を可能にすることで、共同作業者が協力して作業するのに役立ち、より正確なオーディエンスのターゲティングと測定が可能になります。 アカウントの設定中に選択した照合キーによって、今後の接続で使用できる照合キーが決まります。 また、オーディエンスのソーシング時に、データ接続からCollaborationのターゲットフィールドに[&#x200B; フィールド &#x200B;](./onboard-audiences.md#map-fields)をマッピングするためにも使用されます。

オーディエンスプロファイルを紐付ける際に使用する一致キーを選択します。 将来の計画を立て、今後のキャンペーンで使用できる照合キーを含めます。 後でアカウントに追加の一致キーを選択する必要がある場合は、[&#x200B; アカウントを編集](#edit-account) ワークフローで選択できます。 ただし、初期設定後に追加された一致キーは、既存の接続では使用できません。

#### サポートされている一致キー {#supported-match-keys}

Collaborationでは、ファーストパーティの人物ID、ファーストパーティデバイス ID、パートナーIDの3種類の照合キーをサポートしています。 すべての一致キーは、次の要件を満たす必要があります。

* 一致するキーは&#x200B;**trimmed**、**小文字**&#x200B;である必要があります
* ハッシュ化された一致キーは&#x200B;**SHA256-hashed**&#x200B;である必要があります。
* 大文字を使用するハッシュ値を指定すると、Collaborationは自動的に小文字に変換します。
* ソースに&#x200B;**プレーンテキスト識別子**&#x200B;が含まれている場合は、[&#x200B; データ接続のセットアップ &#x200B;](./manage-data-connection.md#match-keys)中に&#x200B;**[!UICONTROL 変換を適用]** オプションを使用してハッシュを適用します。 このオプションは、Experience Platformからオーディエンスをソーシングする場合にのみ使用でき、クラウドベースのソースではサポートされていません。

##### ファーストパーティ人物 ID

ファーストパーティの人物IDは、個々のプロファイルに直接接続されます。 現在サポートされているIDは次のとおりです。

* **[!UICONTROL ハッシュ化されたメール]**
* **[!UICONTROL ハッシュ化された電話]**
* **[!UICONTROL CRM ID]**
* **[!UICONTROL ロイヤルティ ID]**
<!-- * **[!UICONTROL Custom ID]**: Custom identifiers -->

##### ファーストパーティデバイス ID

ファーストパーティデバイス IDは、特定のデバイスに接続された識別子です。 現在サポートされているIDは次のとおりです。

* **[!UICONTROL ハッシュ IPv4]**: ハッシュ IPv4 アドレス
* **[!UICONTROL IDFA]**: Apple iOS デバイスで使用される広告主向け識別子（IDFA）
* **[!UICONTROL GAID]**: Android デバイスで使用されているGoogle Advertiser ID

##### パートナー ID

パートナー ID は、オーディエンスの紐付けのために外部パートナーによって提供される識別子です。 現在サポートされているIDは次のとおりです。

* **[!UICONTROL AdFixus ID]**

>[!NOTE]
>
>Adobeと[!DNL AdFixus]の統合により、各アカウントの一意の[!UICONTROL AdFixus ID]が、Adobeでエンコードされた共通のフォーマットにマッピングされます。 これらのマッピングは、共同作業者の重複を識別するために使用されます。 **[!UICONTROL AdFixus ID]**&#x200B;を使用してオーディエンスをアクティブ化する場合、元のIDが使用されます。 Adobeでエンコードされたフォーマットは、Collaborationから離れることはありません。

**[!UICONTROL AdFixus ID]**&#x200B;を選択する場合、**[!UICONTROL アカウント資格情報]** セクションで、外部パートナーから対応するIDを指定する必要があります。 このオプションは、**[!UICONTROL AdFixus ID]**&#x200B;で&#x200B;*切り替え後*&#x200B;にのみ使用できます。 AdFixus IDを&#x200B;**[!UICONTROL アカウント ID]** フィールドに入力し、値が正確かどうかを再確認してください。

![AdFixus IDを含むキーマッチダイアログがオンになり、アカウント資格情報セクションが強調表示されます。](/help/assets/setup/manage-account/adfixus-settings.png){zoomable="yes"}

必要なすべての一致キーを選択したら、**[!UICONTROL 完了]**&#x200B;を選択して、アカウント設定ワークフローを完了します。

![一致するキーを含むアカウント ワークスペースの設定セクションが表示されます。](/help/assets/setup/manage-account/add-account-match-keys.png){zoomable="yes"}

## アカウントを編集 {#edit-account}

アカウントを設定したら、いつでも詳細を編集してキーを照合できます。

### 詳細を編集 {#edit-details}

**[!UICONTROL 役割]**&#x200B;を除き、いつでもアカウントの詳細情報を編集できます。 リージョンはAdobe Experience Cloud アカウントに基づいて自動的に設定され、変更することはできません。

アカウントを編集するには、**[!UICONTROL セットアップ]** ワークスペースの&#x200B;**[!UICONTROL マイアカウント]** セクションで&#x200B;**[!UICONTROL 編集]**&#x200B;を選択します。

![&#x200B; マイアカウント タブと編集オプションがハイライト表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-account.png){zoomable="yes"}

アカウントの詳細を編集できるようになりました。 変更するフィールドを更新し、**[!UICONTROL 保存]**&#x200B;を選択して変更を確認します。

![&#x200B; アカウントの詳細を編集ダイアログ。](/help/assets/setup/manage-account/editable-options.png){zoomable="yes"}

### 一致キーを編集 {#edit-match-keys}

また、アカウントの作成時に最初に選択した照合キーを更新することもできます。 これらの照合キーによって、今後の接続で使用できる照合キーが決まります。

「**[!UICONTROL キーの一致]**」セクションで「**[!UICONTROL 編集]**」を選択します。

![&#x200B; アカウントの「キーの一致」セクション内で「編集」オプションが強調表示された設定ワークスペース。](/help/assets/setup/manage-account/edit-match-keys.png){zoomable="yes"}

「**[!UICONTROL 一致キー]**」ダイアログが表示されます。 任意の一致キーを切り替えるか、[!UICONTROL AdFixus ID]の&#x200B;**[!UICONTROL アカウント ID]**&#x200B;を更新し、**[!UICONTROL 保存]**&#x200B;を選択して変更を確認します。

>[!IMPORTANT]
>
>[!UICONTROL AdFixus ID]を変更しても、一致キーを使用した既存のデータ接続の[&#x200B; データスケッチ &#x200B;](../glossary.md#sketches)の更新はトリガーされません。 データがスケッチされると、[&#x200B; データ接続スケジュール &#x200B;](./manage-data-connection.md#scheduling)の設定に従って次のオーディエンスが更新されるまで、[!UICONTROL AdFixus ID]に対する変更は反映されません。 次の更新の前に変更が必要な場合は、データ接続を削除して再作成できます。
>
>現時点では、アカウントに追加した照合キーは削除できません。

![保存オプションがハイライト表示されたキーの一致ダイアログ。](/help/assets/setup/manage-account/match-key-dialog.png){zoomable="yes"}

成功ダイアログは、アカウントの照合キーが正常に更新されたことを確認します。

![&#x200B; アカウントの照合キーが正常に更新されたことを確認する成功ダイアログが表示されます。](/help/assets/setup/manage-account/match-key-updated-successfully.png){zoomable="yes"}

## 次の手順

アカウントを設定したら、[&#x200B; ソースオーディエンス &#x200B;](/help/guide/setup/onboard-audiences.md)をReal-Time CDP Collaborationに登録できます。
