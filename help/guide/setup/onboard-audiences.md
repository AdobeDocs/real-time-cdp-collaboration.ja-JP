---
title: Sourceとオーディエンスの管理
description: Adobe Real-Time CDP Collaborationでオーディエンスをソース化および管理する方法を学ぶ
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 425bcb6b8069dfca17838d05b6a91250293c8308
workflow-type: tm+mt
source-wordcount: '3508'
ht-degree: 16%

---

# Sourceとオーディエンスの管理

{{limited-availability-release-note}}

オーディエンスは、様々な属性に基づいてセグメント化された、ユーザーまたは顧客の特定のグループです。 これにより、共同作業者は、ターゲットを絞ったマーケティングとパーソナライズされたエクスペリエンスで連携して、より効果的な広告キャンペーンを行うことができます。 このガイドでは、オーディエンスをReal-Time CDP Collaborationにソース化する方法、オーディエンスダッシュボードを表示する方法、個々のオーディエンスを管理する方法について説明します。

## CollaborationへのSource オーディエンス {#source-audiences}

>[!IMPORTANT]
>
>オーディエンスをソースにするには、2 つのプロファイル管理権限（**[!UICONTROL プロファイルの表示]** および **[!UICONTROL セグメントの表示]** を含む役割にユーザーを割り当てる必要があります。 必要な権限の割り当てについては、権限の [ オーディエンスソーシング ](../permissions/overview.md#audience-sourcing) ガイドを参照してください。

共同作業者とオーディエンスをアクティブ化し、重複計算を実行する前に、オーディエンスをCollaborationにソーシングする必要があります。 オーディエンスをソース化するには、以下の節で示すワークフロー手順に従います。

**[!UICONTROL 設定]** ワークスペース内の **[!UICONTROL マイオーディエンス]** タブで、追加アイコン（![ 追加アイコン](/help/assets/icons/plus.png)）を選択してから、**[!UICONTROL オーディエンス]** を選択します。 初めてのオーディエンスの場合は、「**[!UICONTROL 追加 &#x200B;]」オプションを選択することもでき** す。

![ 「追加」オプションと「オーディエンス」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### データ接続の選択 {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="マーケティングアクション"
>abstract="<p>マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。<strong>データ共同作業</strong>マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。<strong>データサイエンス</strong>マーケティングアクションは、C9 データ使用ラベルをサポートしています。</p> <p> <ul><li> チェックボックスを<em>有効</em>にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ<strong>ません</strong>。</li><li> チェックボックスを<em>無効</em>にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータがソースとされます。</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=ja" text="データ使用ラベルの概要"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=ja" text="データ使用ラベルの用語集"

>[!IMPORTANT]
>
>最初のデータ接続を確立し、最初のオーディエンスをソーシングしたら、既存のデータ接続から複数のオーディエンスをソーシングできます。 追加のオーディエンスを追加する場合は、データ接続が既に確立されているので、[ オーディエンスを選択 ](#select-audiences) の手順から開始します。

データ接続は、オーディエンスのソースとなるデータのソースです。 現在、サポートされているデータ接続はAdobe Experience Platformのみです。

データ接続に対して設定した設定は、このデータ接続をソースとするすべてのオーディエンスに適用されます。

>[!TIP]
>
>データ接続を表示および編集できる別のワークフローがあります。 詳細については、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) ガイドを参照してください。

データ接続の追加を開始するには、「**[!UICONTROL 新しいデータ接続を追加]**」を選択し、「**[!UICONTROL 次へ]**」を選択します。

![ 「新しいデータ接続を追加」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### データソースを選択

次に、データ接続のソースを選択します。 利用可能なソースは次のとおりです。

* **Adobe Experience Platform**:Adobe Experience Platformからオーディエンスを取り込む場合は、このオプションを選択します。
* **CSV ファイル** （今後のリリース）：迅速でわかりやすいデータ取り込みを行うために、オーディエンスデータを含んだ CSV ファイルをアップロードします。
* **Amazon Web Services** （将来リリース）: Amazon S3 ストレージに接続して、S3 バケットから直接オーディエンスデータをソースにします。
* **Snowflake** （今後のリリース）: Snowflake Data Warehouse を使用して、オーディエンスデータをシームレスに取り込みます。
* **Google Cloud Platform** （今後のリリース）: Google クラウドストレージに接続して、GCS バケットから直接オーディエンスデータをソース化します。

データソースを選択してから、「**[!UICONTROL 次へ]**」を選択します。

![ 「Adobe Experience Platform」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### サンドボックスを選択

データソースを選択したら、Collaborationに使用するオーディエンスを含むサンドボックスを選択する必要があります。 使用可能なサンドボックスのリストからサンドボックスを選択して、「次へ **[!UICONTROL を選択します]**

![ サンドボックスが選択されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

#### ガバナンスポリシーと適用アクション {#governance-policy-and-enforcement-actions}

次に、ソースとなるデータに正しいマーケティングアクションが設定されていることを確認する必要があります。 また、データの共同作業に使用するには、Experience Platformをソースとするデータに対して同意を得る必要があります。

マーケティングアクションを使用して、Experience PlatformからCollaborationに取り込むオーディエンスデータを制御します。 **[!UICONTROL データ共同作業]**&#x200B;マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。**[!UICONTROL データサイエンス]**&#x200B;マーケティングアクションは、C9 データ使用ラベルをサポートしています。

詳しくは、[C4、C5 および C9 データ使用ラベル ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"} を参照してください。

* チェックボックスが ***有効*** になっている場合、上記のようにExperience Platformでラベル付けされたデータは除外され、Collaborationに取り込まれます **無効**。
* チェックボックス ***無効*** をオンにした場合、Experience Platformをソースとするデータに関する制限はありません。

データ使用ラベルについて詳しくは、Experience Platform ドキュメントを参照してください。

* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [ データ使用ラベルの用語集 ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference){target="_blank"}

さらに、同意ルールを選択して、Collaborationに取り込まれるデータに適用します。

![ ガバナンスポリシーとエンフォームアクションの節にあるオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}

マーケティングアクションと同意ルールを選択したら、「**[!UICONTROL 次へ]**」を選択して次の手順に進みます。 確認ダイアログが表示され、条件に同意するように求められます。 チェックボックスを選択し、「**[!UICONTROL OK]**」を選択して確定します。

![ チェックボックスと「OK」オプションがハイライト表示されたガバナンスポリシーとエンフォームアクションのダイアログ。](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### 詳細を入力

次に、データ接続の名前と説明を入力します。 この情報は、後でデータ接続を識別するのに役立ちます。

![ 名前と説明を入力するオプションを含んだオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

### フィールドのマッピング {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="ソースフィールド"
>abstract="ソースフィールドは、Experience Platform の実装からの ID 名前空間と属性です。Collaboration で定義したターゲットフィールドにこれらをマッピングできます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="ターゲットフィールド"
>abstract="ターゲットフィールドは、アカウント設定時に選択した一致キーです。デフォルトでは、選択したすべての一致キーを使用できます。"

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
>abstract="Experience Platform のプロファイルクラスの結合スキーマから属性を選択します。このビューには、結合スキーマに存在し、XDM 個人プロファイルクラスに属する属性が表示されます。"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=ja" text="Experience Platform の結合スキーマ"

次に、ソースフィールドを選択して、Collaborationのターゲットフィールドにマッピングします。 使用可能なターゲットフィールドは、アカウント設定時に選択した一致キーに基づきます

>[!IMPORTANT]
>
>現在、データ接続を編集して新しいマップ フィールドを含めることはできません。 データ接続を作成した後に新しい一致キーをアカウントに追加する場合は、新しいデータ接続を作成してマッピングする必要があります。

![ ソースフィールドをターゲットフィールドにマッピングするオプションを使用したオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>複数のソースフィールドを同じターゲットフィールドにマッピングできます。 例えば、Experience Platformの 2 つの異なるフィールドにメールアドレスがある場合、それぞれを 2 つの異なる行として **[!UICONTROL ハッシュ化されたメール]** ターゲットフィールドにマッピングできます。 **[!UICONTROL フィールドを追加]** オプションを使用して、マッピング行を追加します。

>[!BEGINSHADEBOX]

**[!UICONTROL Source フィールド]** は、Experience Platformの id 名前空間および属性です。 これには、[ 標準 ](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#standard){target="_blank"}ID 名前空間と [ カスタム ](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#create-namespaces){target="_blank"} ID 名前空間の両方が含まれます。 また、[ 和集合スキーマ ](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=ja){target="_blank"} に存在し、XDM Individual Profile クラスに属するプロファイル属性も含まれます。

Source フィールドは、Collaborationで定義されたターゲットフィールドにマッピングされます。

**[!UICONTROL ターゲットフィールド]** は、Collaborationでの ID の参照方法を示します。 ターゲットフィールドは、アカウント設定時に選択した一致キーです。デフォルトでは、選択したすべての一致キーを使用できます。

**[!UICONTROL ハッシュ化されていない]** フィールドをハッシュ化されたフィールドにソーシングしている場合は、*変換を適用* オプションを使用します。 Collaborationはハッシュを適用し、フィールドを変換します。 Adobeで使用されるハッシュアルゴリズムは SHA256 です。

>[!ENDSHADEBOX]

マッピングフィールドを開始するには、ターゲットフィールドの横にある空のソースフィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 **[!UICONTROL ID 名前空間]** オプションと **[!UICONTROL プロファイル属性]** オプションの中から選択して、目的のソースフィールドを見つけ、リストからフィールドを選択します。 また、検索オプションを使用して、目的のフィールドを見つけることもできます。

![ メールオプションが表示されたソースフィールドを選択ダイアログ。](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

ハッシュ化されていないフィールドをハッシュ化されたターゲットフィールドにソーシングするには、「**[!UICONTROL 変換を適用]** オプションを使用します。 例えば、2 つ目のメールフィールドを追加するには、「**[!UICONTROL フィールドの追加]**」オプションを選択して新しい行を追加し、ターゲットフィールドで「**[!UICONTROL ハッシュ化されたメール]**」を選択します。 ハッシュ化されていないメールソースフィールドを選択し、「**[!UICONTROL 変換を適用]**」を選択します。

![ メールソースフィールドがターゲットフィールドにマッピングされ、変換の適用がオンになっているオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

引き続き、各ターゲットフィールドにマッピングペアを追加します。 一致キーを使用しない場合は、フィールドの横にある削除（![ 削除アイコン ](/help/assets/icons/delete.png)）アイコンを使用して削除できます。 一致キーが削除されると、接続からオーディエンスをソーシングする際に使用できなくなります。

![ ターゲットフィールドの横にある「削除」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

フィールドのマッピングが完了したら、「**[!UICONTROL 次へ]**」を選択して続行します。

![ マップフィールドが入力され、「次へ」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### スケジュール {#schedule}

次に、オーディエンスへの入力を開始および終了するタイミングをスケジュールします。 オーディエンスは、このスケジュールに従って更新されます。

![ スケジュールオプションが表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>オーディエンスの更新頻度を調整すると、オーディエンスの更新ごとに計算される [Audience Management のクレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities) を管理するのに役立ちます。 高い頻度を選択すると、Audience Discover レポートと Audience Activation で使用できるデータの鮮度に影響を与える可能性があります。

**[!UICONTROL 頻度]** ドロップダウンからオーディエンスの更新の頻度を選択します。

![ 頻度ドロップダウンが開いたオーディエンスを追加スケジュールワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

次に、「**[!UICONTROL 日付範囲]**」を選択します。 開始日は、オーディエンスがプロファイルの入力を開始する日付で、終了日はオーディエンスが更新を停止する日付です。

![ 「日付範囲」オプションが表示されたオーディエンスの追加スケジュールワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>日付範囲の終了日を過ぎると、このデータ接続をソースとするすべてのオーディエンスの更新が停止します。 接続を更新するには、「[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) ガイドに従ってください。

### オーディエンスを選択 {#select-audiences}

オーディエンスソースを選択したら、含める特定のオーディエンスを選択します。 検索およびフィルターオプションを使用して、データ接続から関連するオーディエンスを見つけます。 目的のオーディエンスを選択し、「**[!UICONTROL 次へ]**」を選択します。

![ 使用可能なオーディエンスのリストを含むオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### レビュー

オーディエンスの追加を最終決定する前に、すべての設定を確認してください。 すべての詳細が正しいことを確認してから、「**[!UICONTROL 完了]**」を選択してデータ接続の作成を完了します。

![ すべての選択設定が表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## オーディエンスダッシュボードの表示 {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="ID の欠落"
>abstract="ID 数は、設定されたスケジュールに従って次回データ接続を更新した後に使用できます。最初の更新は通常、データ接続を設定してから 24 時間以内に行われます。継続的な更新は、設定されたスケジュールに従います。"

オーディエンスをソーシングすると、**[!UICONTROL マイオーディエンス]** ワークスペースに、現在Collaborationをソースとしているすべてのオーディエンスが表示されます。

![ ソースとなるすべてのオーディエンスを表示するマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

各オーディエンスには、次の情報の概要が含まれます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ID]** | このオーディエンスに存在する ID の数を示します。 同じプロファイルに 2 つ以上の ID があり、これらの ID がプロジェクトで一致キーとして使用される場合、プロファイルはそのカウントに 2 回表示されます。 |
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 **[!UICONTROL 保留中]** ステータスは、オーディエンスが最近ソースされ、ID がまだ入力されていないことを示します。 ソースオーディエンスは、最初の更新後にプロファイルを入力します。これは、通常、データ接続が設定されてから 24 時間以内に発生します。 |
| **[!UICONTROL ソース]** | オーディエンスのソースを示します。 Collaborationの現在のリリースでは、サポートされているソースはExperience Platformのみです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソースとなるデータ接続。 名前を選択して、データ接続を表示できます。 |
| **[!UICONTROL 接続アクセス]** | オーディエンスがプライベートかパブリックかを定義します。 公開オーディエンスは、重複レポートで検出でき、プロジェクト内でアクティブ化できます。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初にCollaborationをソースにしたタイミングを示します。 |
| **[!UICONTROL 最終更新日]** | Collaborationでオーディエンスが最後に更新された日時を示します。 これは、オーディエンスが最後に更新された日時ではなく、オーディエンスの設定またはメタデータが最後に変更された日時を指します。 |

![ すべてのオーディエンスがソースとなっているマイオーディエンスワークスペース ](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

オーディエンスに対してクイックアクションを実行するには、オーディエンス名の横にある省略記号 **...** を選択します。 次のオプションがあります。

* **[!UICONTROL カテゴリを編集]** を使用すると、オーディエンスに様々なカテゴリタグを追加できます。 詳しくは、以下の [ カテゴリ ](#categories) の節を参照してください。
* **[!UICONTROL 削除]** は、データ接続からオーディエンスを削除します。

![ 省略記号メニューが開き、「カテゴリを編集」オプションと「削除」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}

## 個々のオーディエンスの表示 {#view-individual-audiences}

個々のオーディエンスの情報を表示および更新するには、**[!UICONTROL マイオーディエンス]** ワークスペースからオーディエンスを選択します。 オーディエンスワークスペースには、選択したオーディエンスに関する詳細情報（詳細、ID、カテゴリ、接続アクセス、メタデータの表示設定など）が表示されます。

### オーディエンスの詳細

個々のオーディエンスに対して、次の情報が表示されます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 |
| **[!UICONTROL ソース]** | オーディエンスのソースを示します。 Collaborationの現在のリリースでは、サポートされているソースはExperience Platformのみです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソースとなるデータ接続。 |
| **[!UICONTROL 最終更新日]** | Collaborationでオーディエンスが最後に更新された日時を示します。 これは、オーディエンスが最後に更新された日時ではなく、オーディエンスの設定またはメタデータが最後に変更された日時を指します |
| **[!UICONTROL 最終更新者]** | オーディエンスを最後に更新したユーザーを示します。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初にCollaborationをソースにしたタイミングを示します。 |
| **[!UICONTROL 作成者]** | オーディエンスをCollaborationにソーシングしたユーザーを示します。 |

![ 個々のオーディエンスのワークスペース ](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### ID {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="ID"
>abstract="一致キーで区切られた、このオーディエンスを構成する ID の分類ビュー。"

「**[!UICONTROL ID]**」セクションは、オーディエンスに存在する ID の数を示します。 この節には、オーディエンスの構成を理解するのに役立つ、一致キーによる ID の分類も含まれています。

![ 個々のオーディエンスのワークスペースの ID セクション。](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

一致キーの分類の個々のセクションにマウスポインターを置くと、関連するキーの正確な ID 数が表示されます。

![ 一致キーの分類が表示された、個々のオーディエンスのワークスペースの ID セクション。](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### カテゴリ {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="カテゴリ"
>abstract="整理、フィルタリング、検索を簡単にするために、オーディエンスにタグを付けます。 複数のカテゴリでオーディエンスをタグ付けし、これらのカテゴリタグを使用して、製品の他の領域で目的のオーディエンスをフィルタリングできます。"

オーディエンスの整理、フィルタリングおよび取得を簡単にするために、オーディエンスにタグを付けることができます。 オーディエンスに複数のカテゴリのタグを付けた後、オーディエンスの重複レポートを実行する際に、これらのカテゴリタグを使用して [ 検出 ](/help/guide/collaborate/discover.md) 製品領域で目的のオーディエンスをフィルタリングできます。

カテゴリを追加するには、「**[!UICONTROL カテゴリ]**」セクション内の「**[!UICONTROL 編集]**」オプションを選択します。

![ 個々のオーディエンスのワークスペースのカテゴリセクション。](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

**[!UICONTROL カテゴリ]** ダイアログが表示され、オーディエンスに追加するカテゴリを選択できます。 個々のカテゴリを選択するには、カテゴリ名の横にあるチェックボックスをオンにします。

![ 使用可能なカテゴリが表示されたカテゴリダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png){zoomable="yes"}

#### 接続アクセス {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="接続アクセス"
>abstract="<p>オーディエンスには、パブリック、プライベート、カスタムの 3 つのタイプがあります。</p><p> 共同作業者がいるプロジェクトにおける使用の可用性は、接続アクセス設定に基づいて異なります。</p>"

共同作業者と共にプロジェクトで使用するオーディエンスの可用性は、接続アクセス設定に基づいて異なります。 「**[!UICONTROL 接続アクセス]**」セクションでは、オーディエンスをプライベート、パブリックまたは特定の接続でのみ使用できるかどうかを選択できます。 公開オーディエンスは、接続で使用したり検出したりできます。

オーディエンスの接続アクセスを更新するには、「**[!UICONTROL 接続アクセス]**」セクション内の **[!UICONTROL 編集]** オプションを選択します。

![ 個々のオーディエンスのワークスペースの「接続アクセス」セクション ](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

**[!UICONTROL 接続アクセス]** ダイアログが表示され、使用可能な 3 つの接続アクセスオプションが示されます。

* **[!UICONTROL 非公開オーディエンス]**. これらのオーディエンスは、重複レポートや共同作業者との接続でのアクティブ化には *使用できません*。 共同作業者がオーディエンスを表示または使用することはできませんが、**[!UICONTROL オーディエンスの比較]** セクションの [ すべてのオーディエンス ](/help/guide/collaborate/discover.md#compare-audiences) ビューでは、オーディエンスの母集団が合計母集団に貢献します。 共同作業者と連携してオーディエンスを使用するには、設定をパブリックまたはカスタムに変更します。
* **[!UICONTROL 一般向け]** これらのオーディエンスは、重複レポートや共同作業者との連携でアクティブ化するために使用できます。
* **[!UICONTROL カスタムオーディエンス]**。 これらのオーディエンスは、重複レポートや、指定された接続でのみアクティブ化するために使用できます。 共同作業者がオーディエンスを表示または使用することはできませんが、**[!UICONTROL オーディエンスの比較]** セクションの [ すべてのオーディエンス ](/help/guide/collaborate/discover.md#compare-audiences) ビューでは、オーディエンスの母集団が合計母集団に貢献します。

目的の接続アクセスオプションを選択し、「**[!UICONTROL 保存]**」を選択して変更を適用します。

![ 使用可能なオプションが表示された接続アクセスダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>アクセスステータス（パブリック、プライベート、カスタム）に関係なく、任意のオーディエンスの母集団は、プロジェクト内の **[!UICONTROL オーディエンスを比較]** セクションの **[!UICONTROL すべてのオーディエンス]** 母集団に貢献します。

共同作業者と共にプロジェクトで使用するオーディエンスの可用性は、接続アクセス設定に基づいて異なります。

#### メタデータの表示 {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="メタデータの表示"
>abstract="<p>他の共同作業者が、ユーザーと接続する前またはプロジェクトビュー内で確認できるオーディエンスのメタデータを示します。</p> <p> **ID 数**&#x200B;は、検出タブで重複レポートを表示する際に、共同作業者がオーディエンスの ID 数を表示できるかどうかを制御します。</p><p> **オーディエンス重複％**&#x200B;は、共同編集者が自分のオーディエンスとユーザーのオーディエンス重複割合を検出できるかどうかを制御します。</p><p> **[!UICONTROL オーディエンスインデックス]**&#x200B;は、共同作業者がプロジェクト内のオーディエンスインデックスを表示できるかどうかを制御します。この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。</p> <br> メタデータの表示設定を有効にするには、オーディエンスをパブリックまたはカスタムに設定する必要があります。"

>[!NOTE]
>
>共同作業者がすべてのオーディエンスをプライベートに設定している場合、**[!UICONTROL 検出]** ワークスペースのプロジェクトの **[!UICONTROL 関連オーディエンス]** セクションは空白になります。 詳しくは、[discover](/help/guide/collaborate/discover.md#relevant-audiences) ガイドを参照してください。

メタデータの表示は、他の共同作業者が接続する前や、異なるプロジェクトビュー内でオーディエンスのメタデータを表示することを示します。 オーディエンスのメタデータの表示を更新するには、「**[!UICONTROL メタデータの表示]** セクション内の **[!UICONTROL 編集]** オプションを選択します。

![ 個々のオーディエンスのワークスペースのメタデータ表示セクション ](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

**[!UICONTROL メタデータの表示]** ダイアログが表示され、オーディエンスの表示設定を指定できます。 各オーディエンスに対して設定できるメタデータの表示設定は 2 つあります。

**[!UICONTROL ID 数を表示]**：この設定は、プロジェクト内の [ 「検出」タブで重複レポートを表示 ](/help/guide/collaborate/discover.md#discover-overlaps) する際に、共同作業者がオーディエンスの ID 数を表示できるかどうかを制御します。

**[!UICONTROL オーディエンスの重複を表示 %]**：この設定は、共同作業者がオーディエンスとオーディエンスの間で [ 重複率を検出 ](/help/guide/collaborate/discover.md#compare-audiences) できるかどうかを制御します。

**[!UICONTROL オーディエンスインデックス]**:true に設定すると、共同作業者はプロジェクト内で [ オーディエンスインデックス ](/help/guide/collaborate/discover.md#audience-index-score) を表示できます。 この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。

>[!NOTE]
>
>メタデータの表示設定を有効にするには、オーディエンスをパブリックまたはカスタムに設定する必要があります。

![ 使用可能なオプションが表示されたメタデータの表示ダイアログ ](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## 複数オーディエンスの編集 {#edit-audiences}

オーディエンスダッシュボードから、複数のオーディエンスを一度に編集できます。 そのためには、名前の横にあるボックスを選択して、編集するオーディエンスを選択します。 オーディエンスを選択したら、編集メニューで使用可能なオプションを使用してアクションを実行できます。

![2 つのオーディエンスが選択され、編集メニューがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### メタデータの表示を一括編集 {#bulk-edit-metadata-visibility}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL メタデータの表示を編集]** を選択します。

![ 「メタデータの表示を編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

**[!UICONTROL メタデータの表示]** ダイアログが表示され、選択したオーディエンスの表示設定を指定できます。 デフォルトでは、どのオプションも選択されません。 選択したすべてのオーディエンスに適用するオプションを選択し、「**[!UICONTROL 保存]**」を選択します。

![ 使用可能なオプションが表示されたメタデータの表示ダイアログ ](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### 接続アクセスの一括編集 {#bulk-edit-connection-access}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL 接続アクセスを編集]** を選択します。

![ 「接続アクセスを編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

**[!UICONTROL 接続アクセス]** ダイアログが表示され、選択したオーディエンスのアクセス設定を指定できます。 デフォルトでは、「**[!UICONTROL 非公開オーディエンス]** オプションが選択されています。 選択したすべてのオーディエンスに適用するオプションを選択し、「**[!UICONTROL 保存]**」を選択します。

![ 使用可能なオプションが表示された接続アクセスダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### オーディエンスの名前と説明の一括編集 {#bulk-edit-audience-names-descriptions}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL 名前と説明を編集]** を選択します。

![ 「名前と説明を編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

**[!UICONTROL 名前と説明]** ダイアログが表示され、選択した各オーディエンスの名前と説明を設定できます。 デフォルトでは、各オーディエンスに現在の名前と説明が表示されます。 変更を加え、「**[!UICONTROL 保存]**」を選択します。

![ 使用可能なオプションが表示された名前と説明ダイアログ。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### カテゴリの一括編集 {#bulk-edit-categories}

オーディエンスダッシュボードでオーディエンスを選択し、編集メニューから **[!UICONTROL カテゴリを編集]** を選択します。

![ 「カテゴリを編集」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

**[!UICONTROL カテゴリ]** ダイアログが表示され、選択した各オーディエンスのカテゴリを設定できます。 デフォルトでは、カテゴリは選択されません。 カテゴリを選択するには、まずメイン カテゴリを選択してから、含めるサブカテゴリを選択します。 変更を加え、「**[!UICONTROL 保存]**」を選択します。

![ 使用可能なオプションが表示されたカテゴリダイアログ ](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## 次の手順

オーディエンスをソーシングしたら、[ 接続 ](/help/guide/connect/establishing-connections.md) してプロジェクトで共同作業するパブリッシャーを見つけます。
