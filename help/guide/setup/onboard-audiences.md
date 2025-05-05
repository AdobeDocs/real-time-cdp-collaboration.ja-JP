---
title: オーディエンスのインポートと管理
description: Adobe Real-Time CDP Collaborationでオーディエンスをインポートおよび管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: 2c835ce72f09c450aa3467dc72980c9c627a0ab8
workflow-type: tm+mt
source-wordcount: '2666'
ht-degree: 22%

---

# オーディエンスのインポートと管理

{{limited-availability-release-note}}

オーディエンスは、様々な属性に基づいてセグメント化された、ユーザーまたは顧客の特定のグループです。 これにより、広告主とパブリッシャーは、ターゲットを絞ったマーケティングとパーソナライズされたエクスペリエンスで共同作業でき、より効果的な広告キャンペーンを実現できます。

オーディエンスに関連して表示できるすべての関連指標や、オーディエンスをAdobe Real-Time CDP Collaborationに読み込むためのワークフロー手順を理解するための参考として、このページを使用してください。

>[!TIP]
>
>この画面の情報を使用して、オーディエンスに関して必要なすべての情報を取得したり、[ 画面の検出と重なり ](/help/guide/collaborate/discover.md) を使用して、パブリッシャーのインベントリと比較した場合に、様々なキャンペーンタイプに最適なオーディエンスに関するインサイトを取得したりできます。

>[!BEGINSHADEBOX]

このドキュメントページの内容は次のとおりです。

* [Real-Time CDP Collaborationへのオーディエンスの読み込み](#import-audiences)
* [オーディエンスダッシュボードの表示](#view-audiences-dashboard)
* [個々のオーディエンスの表示](#view-individual-audiences)

>[!ENDSHADEBOX]

## Real-Time CDP Collaborationへのオーディエンスの読み込み {#import-audiences}

>[!IMPORTANT]
>
>オーディエンスをインポートするには、プロファイルの表示とセグメントの表示の 2 つのプロファイル管理権限を含む役割にユーザーを割り当てる必要があります。 必要な権限の割り当てについては、[ オーディエンスのインポート ](../permissions/overview.md#audience-importation) ガイドを参照してください。

オーディエンスを共同作業者と共有し、重複計算を実行する前に、オーディエンスをReal-Time CDP Collaborationにインポートする必要があります。 オーディエンスをインポートするには、以下の節で示すワークフロー手順に従います。

![ オーディエンスが組織に追加される前のマイオーディエンス画面 ](/help/assets/setup/add-manage-audiences/org-without-audiences-added.png)

「**[!UICONTROL マイオーディエンス]**」タブで、プラス **+** 記号を選択し、「**オーディエンス**」を選択します。

### データ接続の選択 {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="マーケティングアクション"
>abstract="<p>マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。<strong>データ共同作業</strong>マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。<strong>データサイエンス</strong>マーケティングアクションは、C9 データ使用ラベルをサポートしています。</p> <p> <ul><li> チェックボックスを<em>有効</em>にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ<strong>ません</strong>。</li><li> チェックボックスを<em>無効</em>にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータが読み込まれます。</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=ja" text="データ使用ラベルの概要"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=ja" text="データ使用ラベルの用語集"

>[!IMPORTANT]
>
>最初のデータ接続に接続し、最初のオーディエンスを読み込んだ後、この既存のデータ接続から複数のオーディエンスを読み込むように選択できます。 この場合、他のステップからの前提条件の情報がすべて既存の接続から読み込まれるので、ワークフローによって [ オーディエンスを選択 ](#select-audience) のステップに直接移動します。

データ接続は、オーディエンスをReal-Time CDP Collaborationに読み込む元のデータのソースです。 Real-Time CDP Collaborationの最初のリリースでサポートされているデータ接続はAdobe Experience Platformのみです。

データ接続に対して設定した ID マッピングやスケジュールなどの設定は、このデータ接続から読み込まれたすべてのオーディエンスに適用されます。

>[!TIP]
>
>この手順で追加したすべてのデータ接続を常に表示および編集できる別のワークフローがあります。 詳しくは、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) を参照してください。

![AEP RTCDP、CSV ファイル、Amazon S3 およびSnowflakeのオプションを示すオーディエンスソースを選択画面 ](/help/assets/setup/add-manage-audiences/Step-Select-Audience-Source.png)

#### データソースを選択

この手順では、オーディエンスデータのソースを選択します。 利用可能なソースは次のとおりです。

* **Adobe Experience Platform**:Adobe Experience Platform Real-Time CDPからオーディエンスを取り込む場合は、このオプションを選択します。
* **CSV ファイル** （今後のリリース）：迅速でわかりやすいデータ取り込みを行うために、オーディエンスデータを含んだ CSV ファイルをアップロードします。
* **Amazon Web Services** （今後のリリース）: Amazon S3 ストレージに接続して、S3 バケットから直接オーディエンスデータを読み込みます。
* **Snowflake** （今後のリリース）: Snowflake Data Warehouse を使用して、オーディエンスデータをシームレスに取り込みます。

#### サンドボックスを選択

**Adobe Experience Platform** をデータソースとして選択した後、読み込むオーディエンスを含むサンドボックスを選択する必要があります。

![ オーディエンスをインポートするためのサンドボックスを選択 ](/help/assets/setup/add-manage-audiences/import-audiences-select-sandbox.png)

目的のサンドボックスを選択したら、「**[!UICONTROL 次へ]**」を選択します。

#### ガバナンスポリシーと適用アクション {#governance-policy-and-enforcement-actions}

次に、読み込んだデータに対して正しいマーケティングアクションが設定されていることを確認する必要があります。 また、データの共同作業に使用するために、Real-Time CDPからインポートされたデータに対して同意を得る必要があります。

マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。**データ共同作業**&#x200B;マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。**データサイエンス**&#x200B;マーケティングアクションは、C9 データ使用ラベルをサポートしています。

詳しくは、[C4、C5 および C9 データ使用ラベル ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"} を参照してください。

* チェックボックスを&#x200B;*有効*&#x200B;にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ&#x200B;*ません*。
* チェックボックスを&#x200B;*無効*&#x200B;にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータが読み込まれます。

データ使用ラベルについて詳しくは、Experience Platform ドキュメントを参照してください。

* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [ データ使用ラベルの用語集 ](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference){target="_blank"}

![ データ共同作業に必要なマーケティングアクション ](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

### 詳細を入力

次に、今後このデータ接続を認識できるように、名前と説明を入力します。

<!--

>[!IMPORTANT]
>
>Note a difference in terminology where the sandbox selected from Real-Time CDP is considered a dataset in the UI in Real-Time CDP Collaboration.

-->

### フィールドのマッピング {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="ソースフィールド"
>abstract="ソースフィールドは、Real-Time CDP の既存の実装からの ID 名前空間と属性です。Real-Time CDP 共同作業で定義したターゲットフィールドにこれらをマッピングできます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="ターゲットフィールド"
>abstract="ターゲットフィールドは、会社のオンボーディング時に選択した一致キーに対応しています。 現在、ハッシュ化されたメールのみがサポートされている一致キーです。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_apply_transformation"
>title="変換を適用"
>abstract="ソースから&#x200B;*ハッシュ化されていない*&#x200B;フィールドを読み込む場合は、このオプションを使用して、Real-Time CDP Collaboration でハッシュを適用し、プレーンフィールドをハッシュ化されたフィールドに変換します。"

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

![ ターゲットフィールドにマッピングされたソースフィールドを示すフィールドをマッピング画面。](/help/assets/setup/add-manage-audiences/Step-Map-Fields.png)

フィールドをマッピング ステップでは、データ接続から取り込まれたプロファイルの ID フィールドを組織で選択した一致キーにマッピングする方法を選択できます。

>[!TIP]
>
>複数のソースフィールドを同じターゲットフィールドにマッピングできます。 例えば、Experience Platformの 2 つの異なるフィールドにメールアドレスがある場合、両方のアドレスを 2 つの異なる行として **[!UICONTROL ハッシュ化されたメール]** ターゲットフィールドにマッピングできます。

>[!BEGINSHADEBOX]

**[!UICONTROL Source フィールド]** は、データの読み込み元のソースで ID が参照される方法を示します。

**[!UICONTROL ターゲットフィールド]** は、Real-Time CDP Collaborationでの ID の参照方法を示します。 ここで選択できる値は、会社のオンボーディングワークフローで設定した一致キーに対応します。

ソースから **[!UICONTROL ハッシュ化されていない]** フィールドを読み込む場合は、「*変換を適用* オプションを使用します。 この場合、Real-Time CDP Collaborationはハッシュを適用し、フィールドを変換します。 Adobeが使用するハッシュ法は SHA256 です。

>[!ENDSHADEBOX]

必要な数のマッピングペアを追加し、「**[!UICONTROL 次へ]**」を選択して次の手順に進みます。

<!--

In this step, you can also add any identity crosswalks that you would like to use.

Identity crosswalks will be supported after the beta release.

#### Add identity crosswalk

Use identity crosswalks to connect different identifiers across datasets to enrich your audience data with additional attributes or dimensions. 

TODO add GIF Identity crosswalks screen showing a list of available identity crosswalks with details.

Select **[!UICONTROL Add identity crosswalk]** to see a screen where you can choose from various identity crosswalks that you have previously [imported into Real-Time CDP Collaboration](/help/guide/setup/identity-crosswalk.md#import-crosswalk). Each entry includes details such as the table name, type, description, and creation date.

After selecting the desired crosswalk, use a source field join key to map to the crosswalk table join key. 

>[!NOTE]
>
>After selecting an identity crosswalk, the **[!UICONTROL Add identity crosswalk]** control is greyed out. 

For further reading about identity crosswalks, refer to the [glossary](/help/guide/glossary.md).

-->


<!-- will uncomment this part when Manage use cases part becomes available

### Manage use cases {#manage-use-cases}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_usecases"
>title="Use cases for identities"
>abstract="This control is disabled in the initial release of Real-Time CDP Collaboration"

![Manage use cases screen.](/help/assets/setup/add-manage-audiences/Step-manage-use-cases.png)

For every identity selected in the mapping step, select the use cases that you can use the identity for. Available use cases are: 

* Discover
* Share
* Activate
* Measure

Note that this control is disabled in the initial release of Real-Time CDP Collaboration.

After selecting the desired use cases for each identity, proceed to the next step. 

-->›

### スケジュール {#schedule}

オーディエンスの入力と更新を開始および終了するタイミングをスケジュールします。 オーディエンスメンバーシップは、このスケジュールに従って更新されます。

![ オーディエンスを入力する開始日と終了日を示すスケジュール画面。](/help/assets/setup/add-manage-audiences/Step-Schedule.png)

オーディエンスの更新頻度を選択します。 選択可能なオプションは、1 ～ 6 日間のリフレッシュレートです。

>[!IMPORTANT]
>
>オーディエンスの更新頻度を調整すると、オーディエンスメンバーシップの更新ごとに計算される [Audience Management クレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities) の管理に役立ちます。 この影響は、オーディエンス検出レポートやオーディエンスの共有およびアクティベーションに使用できる、より新しいデータではない可能性があります。

![ オーディエンスメンバーシップを更新するための様々な頻度インターバルを示すスケジュール画面。](/help/assets/setup/add-manage-audiences/Step-Schedule-Set-Frequency.png)

>[!IMPORTANT]
>
>日付範囲の終了日の後、このデータ接続からインポートされたすべてのオーディエンスの更新が停止します。 接続を更新するには、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) に移動して、新しい終了日を設定します。

### オーディエンスを選択 {#select-audience}

オーディエンスソースを選択したら、含める特定のオーディエンスを選択します。 ページの検索およびフィルターオプションを使用して、選択したデータソースから関連するオーディエンスを見つけます。

![ 使用可能なオーディエンスのリストが表示されているオーディエンス選択画面と、それらを選択するチェックボックス。](/help/assets/setup/add-manage-audiences/Step-Select-Audience.png)

### レビュー

オーディエンスの追加を最終決定する前に、すべての設定を確認してください。 すべての詳細が正しいことを確認し、「**[!UICONTROL 完了]**」を選択してプロセスを完了します。

## オーディエンスダッシュボードの表示 {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="ID の欠落"
>abstract="ID 数は、設定されたスケジュールに従って次回データ接続を更新した後に使用できます。 最初の更新は、通常、データ接続が設定されてから 24 時間以内に行われます。 継続的な更新は、設定されたスケジュールに従います。 "

オーディエンスをReal-Time CDP Collaborationに読み込むと、それらに関する情報をダッシュボードビューで取得できます。 **[!UICONTROL マイオーディエンス]** ページのデフォルトビューには、組織によってReal-Time CDP Collaborationに現在インポートされているすべてのオーディエンスが表示されます。

![ 広告主によってインポートされたすべてのオーディエンスを示すオーディエンスの概要ページ ](/help/assets/setup/add-manage-audiences/audiences-overview.png)

各オーディエンスに関する次の関連情報を確認できます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ID]** | このオーディエンスに存在する ID の数を示します。 同じプロファイルに 2 つ以上の ID があり、これらの ID がプロジェクトで一致キーとして使用される場合、プロファイルはそのカウントに 2 回表示されます。 |
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 「保留中」ステータスは、オーディエンスが最近インポートされ、オーディエンスメンバーがまだ入力していないことを示します。 インポートされたオーディエンスは、設定されたスケジュールに従って、次回のデータ接続の更新後にプロファイルを入力します。 最初の更新は、通常、データ接続が設定されてから 24 時間以内に行われます                                         . |
| **[!UICONTROL ソース]** | このオーディエンスのインポート元を示します。 Real-Time CDP Collaborationの現在のリリースでは、サポートされているソースはAdobe Experience Platformのみです。 |
| **[!UICONTROL データ接続]** | このオーディエンスのインポート元に関する詳細なドリルダウン情報。 例えば、Experience Platform ソースからオーディエンスを読み込む場合、組織がアクセスできる個々のサンドボックスがデータ接続と見なされます。 |
| **[!UICONTROL 接続アクセス]** | このオーディエンスがプライベートかパブリックかを定義します。 公開オーディエンスは、重複レポートで検出でき、共同作業者と共有できます。 |
| **[!UICONTROL 作成日]** | このオーディエンスがReal-Time CDP Collaborationにいつ読み込まれたかを示します。 |
| **[!UICONTROL 最終更新日]** | このオーディエンスのいずれかの側面が更新された最終日時を示します。 |

**[!UICONTROL データ接続を管理]** を選択して、設定したすべてのデータ接続を表示および編集します。
省略記号と **[!UICONTROL 削除]** を選択して、オーディエンスを削除します。
省略記号を選択して **[!UICONTROL カテゴリを編集]** オーディエンスに別のカテゴリタグを追加します。 詳しくは、以下の [ カテゴリ ](/#categories) の節を参照してください。
個々のオーディエンスを検査または編集するオーディエンス名を選択します。

## 個々のオーディエンスの表示 {#view-individual-audiences}

オーディエンス表示には、オーディエンスに関する詳細が表示されます。

![ 個々のオーディエンスの表示と検査 ](/help/assets/setup/add-manage-audiences/view-inspect-audience.png)

この画面に表示できる指標を以下に示します。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 |
| **[!UICONTROL ソース]** | このオーディエンスのインポート元を示します。 Real-Time CDP Collaborationの現在のリリースでは、サポートされているソースはAdobe Experience Platformのみです。 |
| **[!UICONTROL データ接続]** | このオーディエンスのインポート元に関する詳細なドリルダウン情報。 例えば、Experience Platform ソースからオーディエンスを読み込む場合、組織がアクセスできる個々のサンドボックスがデータ接続と見なされます。 |
| **[!UICONTROL 最終更新日]** | このオーディエンスのいずれかの側面が更新された最終日時を示します。 |
| **[!UICONTROL 最終更新者]** | このオーディエンスを最後に更新したユーザーを示します。 |
| **[!UICONTROL 作成日]** | このオーディエンスがReal-Time CDP Collaborationにいつ読み込まれたかを示します。 |
| **[!UICONTROL 作成者]** | オーディエンスをReal-Time CDP Collaborationに読み込んだユーザーを示します。 |


ページ上で 2 つの追加のコントロールを使用して、オーディエンスを編集または削除できます。

* **[!UICONTROL 削除]**：インベントリからオーディエンスを削除します
* **[!UICONTROL 編集]**：名前や説明など、オーディエンスメタデータを編集します。

![ 個々のオーディエンスの表示と検査 ](/help/assets/setup/add-manage-audiences/audiences-edit-delete-controls.png)

オーディエンスに関するその他の情報は、次のウィジェットで利用でき、部分的に編集できます。

![ 個々のオーディエンスの表示と検査 ](/help/assets/setup/add-manage-audiences/audiences-further-info-boxes.png)

* [ID](#identities)
* [カテゴリ](#categories)
* [接続アクセス](#connection-access)
* [メタデータの表示](#metadata-visibility)

### ID {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="ID"
>abstract="このオーディエンスを構成する ID の分類ビューと、それぞれの ID を持つプロファイルの合計数を取得します。"

このセクションは、オーディエンスのインポート時に指定した ID のいずれかを持つ、オーディエンスに存在するプロファイルの数を示します。 また、セクションには ID の分類も含まれているので、オーディエンス母集団を最大限に活用している ID を特定できます。

### カテゴリ {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="カテゴリ"
>abstract="整理、フィルタリング、検索を簡単にするために、オーディエンスにタグを付けます。 複数のカテゴリでオーディエンスをタグ付けし、これらのカテゴリタグを使用して、製品の他の領域で目的のオーディエンスをフィルタリングできます。"

オーディエンスの整理、フィルタリングおよび取得を簡単にするために、オーディエンスにタグを付けることができます。 オーディエンスに複数のカテゴリのタグを付けた後、オーディエンスの重複レポートを実行する際に、これらのカテゴリタグを使用して [ 検出 ](/help/guide/collaborate/discover.md) 製品領域で目的のオーディエンスをフィルタリングできます。

### 接続アクセス {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="接続アクセス"
>abstract="<p>オーディエンスには、パブリック、プライベート、カスタムの 3 つのタイプがあります。</p><p> 共同作業者がいるプロジェクトでの使用の可用性は、接続アクセス設定に基づいて異なります。接続アクセスは、常にプライベートからパブリックに変更できますが、オーディエンスを共同作業者と共有すると、その設定を元に戻すことはできません。</p>"

オーディエンスを非公開にするか、接続で使用可能で検出可能にするかを選択します。 次の 3 つのオプションを使用できます。

* **[!UICONTROL 一般向け]** これらのオーディエンスは、重複レポートで使用したり、共同作業者との接続で共有およびアクティブ化するために使用できます。
* **[!UICONTROL 非公開オーディエンス]**. これらのオーディエンスは、重複レポートや共同作業者との接続での共有およびアクティブ化には *使用できません*。 共同作業者が表示または使用することはできませんが、このオーディエンスの母集団は、**[!UICONTROL すべてのオーディエンス]** ビューの [ 検出と重複 ](/help/guide/collaborate/discover.md#compare-audiences) セクションの総母集団に引き続き貢献します。 共同作業者と連携してオーディエンスを使用するには、設定をパブリックまたはカスタムに変更します。
* **[!UICONTROL カスタムオーディエンス]**。 これらのオーディエンスは、重複レポートや、指定された接続での共有およびアクティブ化にのみ使用できます。 すべての共同作業者が表示または使用できるわけではありませんが、このオーディエンスの母集団は、**[!UICONTROL すべてのオーディエンス]** ビューの [ 検出と重複セクション ](/help/guide/collaborate/discover.md) の総母集団に貢献します。

>[!IMPORTANT]
>
>アクセスステータス（パブリック、プライベート、カスタム）に関係なく、任意のオーディエンスの母集団は、オーディエンス検出重複分析ビューの **[!UICONTROL すべてのオーディエンス]** 母集団に貢献します。<br> ![ オーディエンス検出重複分析のシステム生成 **すべてのオーディエンス** オーディエンスには、すべての接続アクセスステータス（パブリック、プライベート、カスタム）を持つオーディエンスが含まれます。](/help/assets/setup/add-manage-audiences/all-audiences-view.png "**オーディエンス検出**&#x200B;重複分析のシステム生成&#x200B;**すべてのオーディエンス**&#x200B;オーディエンスには、すべての接続アクセスステータス（パブリック、プライベート、カスタム）を持つオーディエンスが含まれます。"){width="100" zoomable="yes"}

共同作業者と共にプロジェクトで使用するオーディエンスの可用性は、接続アクセス設定に基づいて異なります。 接続アクセスは、常にプライベートからパブリックに変更できますが、オーディエンスを共同作業者と共有すると、その設定を元に戻すことはできません。

### メタデータの表示 {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="メタデータの表示"
>abstract="<p>他の組織がユーザーの組織に接続する前に、他の組織に表示されるオーディエンスメタデータ情報を示します。 </p> <p> **ID 数**&#x200B;は、検出タブで重複レポートを表示する際に、パートナーがオーディエンスの ID 数を表示できるかどうかを制御します。**オーディエンスの重複％**&#x200B;は、共同編集者が自分のオーディエンスとユーザーのオーディエンスの重複の割合を検出できるかどうかを制御します。"

>[!NOTE]
>
>共同作業者がすべてのオーディエンスをプライベートに設定している場合、オーディエンスインサイトの **[!UICONTROL 関連オーディエンス]** ビューは空白になります。 [詳細情報](/help/guide/collaborate/discover.md#relevant-audiences)。

組織に接続する前に、または異なるプロジェクトビュー内で他の組織に表示されるオーディエンスメタデータ情報を示します。

**[!UICONTROL ID 数を表示]**：この設定は、[ 「検出」タブでの重複レポートの表示 ](/help/guide/collaborate/discover.md#discover-overlaps) の際に、パートナーがオーディエンスの ID 数を表示できるかどうかを制御します。

![ 「ID カウントを表示」オプションの選択を解除して選択した画像を並べて表示 ](/help/assets/setup/add-manage-audiences/show-identity-count.png)

**[!UICONTROL オーディエンスの重複を表示 %]**:true に設定すると、共同作業者は、自分のオーディエンスと自分に属するオーディエンスの間で [ 重複率を検出 ](/help/guide/collaborate/discover.md#compare-audiences) できます。 例えば、以下の録画では、オーディエンス `agora-advertiser-aud3` はこの設定を true に設定しており、共同作業者はそのオーディエンスとの重複率を表示できます。 オーディエンス `agora-advertiser-aud1` では、この設定が false に設定されているので、共同作業者は重複率を表示できません。

![2 つの異なるオーディエンスに対するオーディエンスの重複率。](/help/assets/setup/add-manage-audiences/audience-overlap-percentage.gif)

## 次の手順

オーディエンスをインポートした後、「[ 接続 ](/help/guide/connect/establishing-connections.md)」セクションを使用すると、に接続するパブリッシャーを検出し、プロジェクトでの共同作業を開始できます。
