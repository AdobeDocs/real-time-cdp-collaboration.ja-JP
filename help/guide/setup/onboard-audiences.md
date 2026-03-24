---
title: Source and manage audiences
description: Learn how to source and manage audiences in Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: d554ce3921211bc0d726b88f410410cdccc1a937
workflow-type: tm+mt
source-wordcount: '3631'
ht-degree: 18%

---

# Source and manage audiences

{{limited-availability-release-note}}

Audiences are specific groups of users or customers segmented based on various attributes. These enable collaborators to work together on targeted marketing and personalized experiences for more effective advertising campaigns. This guide covers how to source audiences into Real-Time CDP Collaboration, view the audiences dashboard, and manage individual audiences.

## Source audiences into Collaboration {#source-audiences}

>[!IMPORTANT]
>
>**&#x200B;**&#x200B;**&#x200B;**&#x200B;[&#128279;](../permissions/overview.md#audience-sourcing)

Before you can activate audiences with collaborators and run overlap calculations, the audiences need to be sourced into Collaboration. To source audiences, follow the workflow steps in the section below.

**&#x200B;**&#x200B;**&#x200B;**![](/help/assets/icons/plus.png)**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### データ接続の選択 {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="マーケティングアクション"
>abstract="<p>マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。 <strong>データ共同作業</strong>マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。 <strong>データサイエンス</strong>マーケティングアクションは、C9 データ使用ラベルをサポートしています。</p> <p> <ul><li> チェックボックスを<em>有効</em>にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ<strong>ません</strong>。</li><li> チェックボックスを<em>無効</em>にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータがソースとされます。</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=ja" text="データ使用ラベルの概要"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=ja" text="データ使用ラベルの用語集"

>[!IMPORTANT]
>
>[&#128279;](#select-audiences)

A data connection is the source of data from where you are sourcing audiences. Currently, the only supported data connection is Adobe Experience Platform.

Any settings that you configure for your data connection are applied to all the audiences sourced from this data connection.

>[!TIP]
>
>[&#128279;](/help/guide/setup/manage-data-connection.md)

**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### データソースを選択

Next, you&#39;ll choose the source for your data connection. The available sources include:

* **&#x200B;**
* **&#x200B;**&#x200B;[&#128279;](./upload-csv-audience-sourcing.md)
* **&#x200B;**&#x200B;[&#128279;](./configure-aws-s3-audience-sourcing.md)
* **&#x200B;**
* **&#x200B;**

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### サンドボックスを選択

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

#### ガバナンスポリシーと適用アクション {#governance-policy-and-enforcement-actions}

Next, you must make sure that the correct marketing actions are set on the sourced data. You are also required to provide consent for data sourced from Experience Platform to be used for data collaboration.

**[!UICONTROL データ共同作業]**&#x200B;マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。 **[!UICONTROL データサイエンス]**&#x200B;マーケティングアクションは、C9 データ使用ラベルをサポートしています。

[&#128279;](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}

* **&#x200B;**&#x200B;**&#x200B;**&#x200B;**
* **&#x200B;**&#x200B;**

Read more about data usage labels in the Experience Platform documentation:

* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [データ使用ラベルの用語集](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference){target="_blank"}

Additionally, you&#39;ll want to select your consent rules to apply to data being sourced into Collaboration.

![](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}

**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### 詳細を入力

Next, provide a name and a description for your data connection. This information will help you identify the data connection later on.

![](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

### フィールドのマッピング {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="ソースフィールド"
>abstract="ソースフィールドは、Experience Platform の実装からの ID 名前空間と属性です。 Collaboration で定義したターゲットフィールドにこれらをマッピングできます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="ターゲットフィールド"
>abstract="ターゲットフィールドは、アカウント設定時に選択した一致キーです。 デフォルトでは、選択したすべての一致キーを使用できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="変換を適用"
>abstract="*ハッシュ化されていない*&#x200B;フィールドをソースする場合は、このオプションを使用して、Collaboration でハッシュを適用し、プレーンフィールドをハッシュ化されたフィールドに変換します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_identity_namespaces"
>title="ID 名前空間"
>abstract="Experience Platform 組織で使用可能な標準およびカスタムの ID 名前空間から ID 名前空間を選択します。"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#standard" text="Experience Platform の標準および ID 名前空間"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_profile_attributes"
>title="プロファイル属性"
>abstract="Experience Platform のプロファイルクラスの結合スキーマから属性を選択します。 このビューには、結合スキーマに存在し、XDM 個人プロファイルクラスに属する属性が表示されます。"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=ja" text="Experience Platform の結合スキーマ"

Next you&#39;ll select source fields to map to target fields in Collaboration. Available target fields will be based on the match keys you selected during account setup.

>[!IMPORTANT]
>
>Currently, you cannot edit data connections to include new map fields. If you add new match keys to your account after your data connection has been created, you will need to create a new data connection to map to them.

![](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>**&#x200B;**&#x200B;**&#x200B;**

>[!BEGINSHADEBOX]

**&#x200B;**&#x200B;[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#standard){target="_blank"}[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#create-namespaces){target="_blank"}[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=ja){target="_blank"}

Source fields get mapped to the target fields defined in Collaboration.

**&#x200B;**&#x200B;ターゲットフィールドは、アカウント設定時に選択した一致キーです。 デフォルトでは、選択したすべての一致キーを使用できます。

**&#x200B;**&#x200B;**

>[!ENDSHADEBOX]

**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

![](/help/assets/icons/delete.png)

![](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### スケジュール {#schedule}

Next, schedule when to start and end populating the audiences. The audience will be refreshed according to this schedule.

![](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>[&#128279;](/help/guide/setup/my-activity.md#types-of-activities)

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>[&#128279;](/help/guide/setup/manage-data-connection.md)

### オーディエンスを選択 {#select-audiences}

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### レビュー

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## オーディエンスダッシュボードの表示 {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="ID の欠落"
>abstract="ID 数は、設定されたスケジュールに従って次回データ接続を更新した後に使用できます。 最初の更新は通常、データ接続を設定してから 24 時間以内に行われます。 継続的な更新は、設定されたスケジュールに従います。"

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

Each audience contains an overview of the following information:

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL 名前]** | The name of the audience. |
| **&#x200B;**&#x200B;| Indicates the number of identities present in this audience. Note that if the same profile has two or more identities, and these identities are used as match keys in the project, then the profile will appear twice in the count. |
| **[!UICONTROL ステータス]** | **&#x200B;**&#x200B;|
| **[!UICONTROL ソース]** | Indicates where the audience was sourced from. In the current release of Collaboration, Experience Platform is the only supported source. |
| **&#x200B;**&#x200B;| The data connection the audience is sourced from. You can select the name to view the data connection. |
| **&#x200B;**&#x200B;| Defines whether the audience is private or public. Public audiences are discoverable in overlap reports and can be activated within a project. |
| **[!UICONTROL 作成日]** | Indicates when the audience was initially sourced into Collaboration. |
| **[!UICONTROL 最終更新日]** | Indicates the last date and time when the audience was updated in Collaboration. This does not refer to when the audience was last refreshed, but rather when the audience&#39;s configuration or metadata was last changed. |

![](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

**&#x200B;**&#x200B;次のオプションがあります。

* **&#x200B;**&#x200B;[&#128279;](#categories)
* **&#x200B;**

![](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}

## View individual audiences {#view-individual-audiences}

**&#x200B;**

### オーディエンスの詳細

The following information is displayed for each individual audience:

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ステータス]** | Indicates if the audience is active and can be used in projects. |
| **[!UICONTROL ソース]** | Indicates where the audience was sourced from. In the current release of Collaboration, Experience Platform is the only supported source. |
| **&#x200B;**&#x200B;| The data connection the audience is sourced from. |
| **[!UICONTROL 最終更新日]** | Indicates the last date and time when the audience was updated in Collaboration. This does not refer to when the audience was last refreshed, but rather when the audience&#39;s configuration or metadata was last changed |
| **[!UICONTROL 最終更新者]** | Indicates the user who last updated the audience. |
| **[!UICONTROL 作成日]** | Indicates when the audience was initially sourced into Collaboration. |
| **[!UICONTROL 作成者]** | Indicates the user who sourced the audience into Collaboration. |

![](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### ID {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="ID"
>abstract="一致キーで区切られた、このオーディエンスを構成する ID の分類ビュー。"

**&#x200B;**&#x200B;The section also contains an identity breakdown of identities by match key to help you understand the composition of the audience.

![The Identities section of an individual audience&#39;s workspace.](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

Hovering over the individual sections of the match key breakdown will provide an accurate identity count for the relevant key.

![The Identities section of an individual audience&#39;s workspace with a match key&#39;s breakdown displayed.](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### カテゴリ {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="カテゴリ"
>abstract="整理、フィルタリング、検索を簡単にするために、オーディエンスにタグを付けます。 複数のカテゴリでオーディエンスをタグ付けし、これらのカテゴリタグを使用して、製品の他の領域で目的のオーディエンスをフィルタリングできます。"

For easy audience organization, filtering, and retrieval, you can tag your audiences. You can tag an audience with multiple categories and then you can use these category tags to filter your desired audiences in the [discover](/help/guide/collaborate/discover.md) product area, when running audience overlap reports.

To add categories, select the **[!UICONTROL Edit]** option within the **[!UICONTROL Categories]** section.

![The Categories section of an individual audience&#39;s workspace.](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

The **[!UICONTROL Categories]** dialog will appear, allowing you to select the categories you want to add to the audience. To select an individual category, select the checkbox next to the category name.


#### 接続アクセス {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="接続アクセス"
>abstract="<p>オーディエンスには、パブリック、プライベート、カスタムの 3 つのタイプがあります。</p><p> 共同作業者がいるプロジェクトにおける使用の可用性は、接続アクセス設定に基づいて異なります。</p>"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_access"
>title="詳細情報"
>abstract=""

An audience&#39;s availability for use in projects with collaborators differs based on the connection access setting. In the **[!UICONTROL Connection access]** section, you can select if the audience should be private, public, or only available for specific connections. Public audiences are usable and discoverable in connections.

To update the audience&#39;s connection access, select the **[!UICONTROL Edit]** option within the **[!UICONTROL Connection access]** section.

![The Connection access section of an individual audience&#39;s workspace.](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

The **[!UICONTROL Connection access]** dialog appears, with three available connection access options:

* **[!UICONTROL Private audience]**. These audiences are *not* available for use in overlap reports or for activation in connections with any collaborators. While the audiences are not available for collaborators to view or use, the population of the audiences still contributes to the total population in the **[!UICONTROL All audiences]** view in the [compare audiences section](/help/guide/collaborate/discover.md#compare-audiences). Change the setting to public or custom to use the audiences in connections with collaborators.
* **[!UICONTROL Public audience]**. These audiences are available for use in overlap reports and for activation in connections with any collaborators.
* **[!UICONTROL Custom audience]**. These audiences are available for use in overlap reports and for activation in specified connections only. While the audiences are not available for collaborators to view or use, the population of the audiences still contributes to the total population in the **[!UICONTROL All audiences]** view in the [compare audiences section](/help/guide/collaborate/discover.md#compare-audiences).

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>**&#x200B;**&#x200B;**&#x200B;**

Audience availability for use in projects with collaborators differs based on the connection access setting.

#### メタデータの表示 {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="メタデータの表示"
>abstract="<p>他の共同作業者が、ユーザーと接続する前またはプロジェクトビュー内で確認できるオーディエンスのメタデータを示します。</p> <p> **ID 数**&#x200B;は、「検出」タブで重複レポートを表示する際に、共同作業者がオーディエンスの ID 数を表示できるかどうかを制御します。</p><p> **オーディエンス重複％**&#x200B;は、共同編集者が自分のオーディエンスとユーザーのオーディエンス重複割合を検出できるかどうかを制御します。</p><p> **[!UICONTROL オーディエンスインデックス]**&#x200B;は、共同作業者がプロジェクト内のオーディエンスインデックスを表示できるかどうかを制御します。 この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。</p> <br> メタデータの表示設定を有効にするには、オーディエンスをパブリックまたはカスタムに設定する必要があります。"

>[!NOTE]
>
>**&#x200B;**&#x200B;**&#x200B;**&#x200B;[&#128279;](/help/guide/collaborate/discover.md#relevant-audiences)

**&#x200B;**&#x200B;**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

**&#x200B;**

**&#x200B;**&#x200B;[&#128279;](/help/guide/collaborate/discover.md#discover-overlaps)

**&#x200B;**&#x200B;[&#128279;](/help/guide/collaborate/discover.md#compare-audiences)

**&#x200B;**&#x200B;[&#128279;](/help/guide/collaborate/discover.md#audience-index-score)この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。

>[!NOTE]
>
>For the metadata visibility settings to take effect, the audience must be set to public or custom.

![](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## Edit multiple audiences {#edit-audiences}

From the audience dashboard, you can edit multiple audiences at once. To do this, select the audiences you want to edit by selecting the boxes next to their names. Once you&#39;ve selected the audiences, you can perform actions using the options available in the edit menu.

![](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Bulk edit metadata visibility {#bulk-edit-metadata-visibility}

**&#x200B;**

![](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

**&#x200B;**&#x200B;デフォルトでは、どのオプションも選択されません。 選択したすべてのオーディエンスに適用するオプションを選択し、「**[!UICONTROL 保存]**」を選択します。

![The Metadata visibility dialog with the available options displayed.](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### 接続アクセスの一括編集 {#bulk-edit-connection-access}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL 接続アクセスを編集]** を選択します。

![&#x200B; 「接続アクセスを編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

**[!UICONTROL 接続アクセス]** ダイアログが表示され、選択したオーディエンスのアクセス設定を指定できます。 デフォルトでは、「**[!UICONTROL 非公開オーディエンス]** オプションが選択されています。 選択したすべてのオーディエンスに適用するオプションを選択し、「**[!UICONTROL 保存]**」を選択します。

![&#x200B; 使用可能なオプションが表示された接続アクセスダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### オーディエンスの名前と説明の一括編集 {#bulk-edit-audience-names-descriptions}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL 名前と説明を編集]** を選択します。

![&#x200B; 「名前と説明を編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

**[!UICONTROL 名前と説明]** ダイアログが表示され、選択した各オーディエンスの名前と説明を設定できます。 デフォルトでは、各オーディエンスに現在の名前と説明が表示されます。 Make your changes and then select **[!UICONTROL Save]**.

![&#x200B; 使用可能なオプションが表示された名前と説明ダイアログ。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### カテゴリの一括編集 {#bulk-edit-categories}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL カテゴリを編集]** を選択します。

![&#x200B; 「カテゴリを編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

**[!UICONTROL カテゴリ]** ダイアログが表示され、選択した各オーディエンスのカテゴリを設定できます。 デフォルトでは、カテゴリは選択されません。 カテゴリを選択するには、まずメイン カテゴリを選択してから、含めるサブカテゴリを選択します。 Make your changes and then select **[!UICONTROL Save]**.

![&#x200B; 使用可能なオプションが表示されたカテゴリダイアログ &#x200B;](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## 次の手順

オーディエンスをソーシングしたら、[&#x200B; 接続 &#x200B;](/help/guide/connect/establishing-connections.md) してプロジェクトで共同作業する共同作業者を見つけます。
