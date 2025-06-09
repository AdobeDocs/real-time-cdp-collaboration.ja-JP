---
title: オーディエンスのインポートと管理
description: Adobe Real-Time CDP Collaborationでオーディエンスをインポートおよび管理する方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
source-git-commit: fda414120decc0c76712616ff85b83febede53e9
workflow-type: tm+mt
source-wordcount: '2961'
ht-degree: 18%

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

共同作業者とオーディエンスをアクティブ化し、重複計算を実行する前に、オーディエンスをReal-Time CDP Collaborationに読み込む必要があります。 オーディエンスをインポートするには、以下の節で示すワークフロー手順に従います。

**[!UICONTROL Stetup]** ワークスペース内の「**[!UICONTROL マイオーディエンス]**」タブから、追加アイコン（![ 追加アイコン](/help/assets/icons/plus.png)）または **[!UICONTROL 追加 ] オプションを選択し** から **オーディエンス** を選択します。

![ 「追加」オプションと「オーディエンス」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/add-audiences.png)

### データ接続の選択 {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="マーケティングアクション"
>abstract="<p>マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。<strong>データ共同作業</strong>マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。<strong>データサイエンス</strong>マーケティングアクションは、C9 データ使用ラベルをサポートしています。</p> <p> <ul><li> チェックボックスを<em>有効</em>にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ<strong>ません</strong>。</li><li> チェックボックスを<em>無効</em>にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータが読み込まれます。</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=ja" text="データ使用ラベルの概要"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=ja" text="データ使用ラベルの用語集"

>[!IMPORTANT]
>
>最初のデータ接続を確立し、最初のオーディエンスをインポートしたら、既存のデータ接続から複数のオーディエンスをインポートできます。 追加のオーディエンスを追加する場合は、[ オーディエンスを選択 ](#select-audience) 手順から開始します。これは、他の手順で必要となったすべての情報が既存の接続から読み込まれるからです。

データ接続は、オーディエンスをReal-Time CDP Collaborationに読み込む元のデータのソースです。 現在、サポートされているデータ接続はAdobe Experience Platformのみです。

データ接続に対して設定したスケジュールなどの設定は、このデータ接続から読み込まれたすべてのオーディエンスに適用されます。

>[!TIP]
>
>データ接続を表示および編集できる別のワークフローがあります。 詳細については、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) ガイドを参照してください。

データ接続の追加を開始するには、「**[!UICONTROL 新しいデータ接続を追加]**」を選択し、「**[!UICONTROL 次へ]**」を選択します。

![ 「新しいデータ接続を追加」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-data-connection.png)

#### データソースを選択

次に、データ接続のソースを選択します。 利用可能なソースは次のとおりです。

* **Adobe Experience Platform**:Adobe Experience Platform Real-Time CDPからオーディエンスを取り込む場合は、このオプションを選択します。
* **CSV ファイル** （今後のリリース）：迅速でわかりやすいデータ取り込みを行うために、オーディエンスデータを含んだ CSV ファイルをアップロードします。
* **Amazon Web Services** （今後のリリース）: Amazon S3 ストレージに接続して、S3 バケットから直接オーディエンスデータを読み込みます。
* **Snowflake** （今後のリリース）: Snowflake Data Warehouse を使用して、オーディエンスデータをシームレスに取り込みます。

データソースを選択してから、「**[!UICONTROL 次へ]**」を選択します。

![ 「Adobe Experience Platform」オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-data-connection-source.png)

#### サンドボックスを選択

データソースを選択したら、読み込むオーディエンスを含むサンドボックスを選択する必要があります。 使用可能なサンドボックスのリストからサンドボックスを選択して、「次へ **[!UICONTROL を選択します]**

![ サンドボックスが選択されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-sandbox.png)

#### ガバナンスポリシーと適用アクション {#governance-policy-and-enforcement-actions}

次に、読み込んだデータに対して正しいマーケティングアクションが設定されていることを確認する必要があります。 また、データの共同作業に使用するために、Real-Time CDPからインポートされたデータに対して同意を得る必要があります。

マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。**データ共同作業**&#x200B;マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。**データサイエンス**&#x200B;マーケティングアクションは、C9 データ使用ラベルをサポートしています。

詳しくは、[C4、C5 および C9 データ使用ラベル ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"} を参照してください。

* チェックボックスを&#x200B;*有効*&#x200B;にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ&#x200B;*ません*。
* チェックボックスを&#x200B;*無効*&#x200B;にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータが読み込まれます。

データ使用ラベルについて詳しくは、Experience Platform ドキュメントを参照してください。

* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [ データ使用ラベルの用語集 ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference){target="_blank"}

さらに、Real-Time CDP Collaborationに読み込むデータに適用する同意ルールを選択する必要があります。

![ ガバナンスポリシーとエンフォームアクションの節にあるオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png)

マーケティングアクションと同意ルールを選択したら、「**[!UICONTROL 次へ]**」を選択して次の手順に進みます。 確認ダイアログが表示され、条件に同意するように求められます。 チェックボックスを選択し、「**[!UICONTROL OK]**」を選択して確定します。

![ チェックボックスと「OK」オプションがハイライト表示されたガバナンスポリシーとエンフォームアクションのダイアログ。](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png)

### 詳細を入力

次に、データ接続の名前と説明を入力します。 この情報は、後でデータ接続を識別するのに役立ちます。

![ 名前と説明を入力するオプションを含んだオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/data-connection-details.png)

### フィールドのマッピング {#map-fields}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_source_fields"
>title="ソースフィールド"
>abstract="ソースフィールドは、Real-Time CDP の既存の実装からの ID 名前空間と属性です。Real-Time CDP 共同作業で定義したターゲットフィールドにこれらをマッピングできます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_mapping_target_fields"
>title="ターゲットフィールド"
>abstract="現在、ハッシュ化されたメールのみがサポートされている一致キーです。"

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

次に、ソースフィールドを選択して、Real-Time CDP Collaborationのターゲットフィールドにマッピングします。

![ ソースフィールドをターゲットフィールドにマッピングするオプションを使用したオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-map-fields.png)

>[!TIP]
>
>複数のソースフィールドを同じターゲットフィールドにマッピングできます。 例えば、Experience Platformの 2 つの異なるフィールドにメールアドレスがある場合、両方のアドレスを 2 つの異なる行として **[!UICONTROL ハッシュ化されたメール]** ターゲットフィールドにマッピングできます。

>[!BEGINSHADEBOX]

**[!UICONTROL Source フィールド]** は、Real-Time CDPの既存の実装から得られる ID 名前空間および属性です。 データの読み込み元のソースに ID が存在する仕組みは次のとおりです。 Source フィールドは、Real-Time CDP Collaborationで定義されたターゲットフィールドにマッピングされます。

**[!UICONTROL ターゲットフィールド]** は、Real-Time CDP Collaborationでの ID の参照方法を示します。 現在、ハッシュ化されたメールのみがサポートされている一致キーです。

ソースから **[!UICONTROL ハッシュ化されていない]** フィールドを読み込む場合は、「*変換を適用* オプションを使用します。 この場合、Real-Time CDP Collaborationはハッシュを適用し、フィールドを変換します。 Adobeが使用するハッシュ法は SHA256 です。

>[!ENDSHADEBOX]

ターゲットフィールドの横にある空のソースフィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 **[!UICONTROL ID 名前空間]** オプションと **[!UICONTROL プロファイル属性]** オプションの中から選択して、目的のソースフィールドを見つけ、リストからソースフィールドを選択します。

![ メールオプションが表示されたソースフィールドを選択ダイアログ。](/help/assets/setup/add-manage-audiences/select-source-field.png)

複数のメールフィールドを処理するには、**[!UICONTROL 変換を適用]** を使用して、ハッシュ化されていないメールソースフィールドをマッピングします。

![ メールソースフィールドがターゲットフィールドにマッピングされ、変換の適用がオンになっているオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/apply-transformation.png)

必要に応じてマッピングペアの追加を続行し、「**[!UICONTROL 次へ]**」を選択します。

### スケジュール {#schedule}

次に、オーディエンスへの入力を開始および終了するタイミングをスケジュールします。 オーディエンスは、このスケジュールに従って更新されます。

![ スケジュールオプションが表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling.png)

>[!IMPORTANT]
>
>オーディエンスの更新頻度を調整すると、オーディエンスの更新ごとに計算される [Audience Management のクレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities) を管理するのに役立ちます。 高い頻度を選択すると、Audience Discover レポートと Audience Activation で使用できるデータの鮮度に影響を与える可能性があります。

**[!UICONTROL 頻度]** ドロップダウンからオーディエンスの更新の頻度を選択します。

![ 頻度ドロップダウンが開いたオーディエンスを追加スケジュールワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png)

次に、「**[!UICONTROL 日付範囲]**」を選択します。 開始日は、オーディエンスがプロファイルの入力を開始する日付で、終了日はオーディエンスが更新を停止する日付です。

![ 「日付範囲」オプションが表示されたオーディエンスの追加スケジュールワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png)

>[!IMPORTANT]
>
>日付範囲の終了日の後、このデータ接続からインポートされたすべてのオーディエンスの更新が停止します。 接続を更新するには、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) に移動して、新しい終了日を設定します。

### オーディエンスを選択 {#select-audience}

オーディエンスソースを選択したら、含める特定のオーディエンスを選択します。 検索およびフィルターオプションを使用して、データソースから関連するオーディエンスを見つけます。 目的のオーディエンスを選択し、「**[!UICONTROL 次へ]**」を選択します。

![ 使用可能なオーディエンスのリストを含むオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-audience.png)

### レビュー

オーディエンスの追加を最終決定する前に、すべての設定を確認してください。 すべての詳細が正しいことを確認してから、「**[!UICONTROL 完了]**」を選択してデータ接続の作成を完了します。

![ すべての選択設定が表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/review-connection.png)

## オーディエンスダッシュボードの表示 {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="ID の欠落"
>abstract="ID 数は、設定されたスケジュールに従って次回データ接続を更新した後に使用できます。最初の更新は通常、データ接続を設定してから 24 時間以内に行われます。継続的な更新は、設定されたスケジュールに従います。 "

オーディエンスをReal-Time CDP Collaborationに読み込むと、**[!UICONTROL マイオーディエンス]** ワークスペースには、組織によってReal-Time CDP Collaborationに現在インポートされているすべてのオーディエンスが表示されます。


各オーディエンスには、次の情報の概要が含まれます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ID]** | このオーディエンスに存在する ID の数を示します。 同じプロファイルに 2 つ以上の ID があり、これらの ID がプロジェクトで一致キーとして使用される場合、プロファイルはそのカウントに 2 回表示されます。 |
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 **[!UICONTROL 保留中]** ステータスは、オーディエンスが最近インポートされ、オーディエンスメンバーがまだ入力していないことを示します。 読み込まれたオーディエンスは、最初の更新後にプロファイルに入力されます。これは、通常、データ接続が設定されてから 24 時間以内に発生します。 |
| **[!UICONTROL ソース]** | オーディエンスのインポート元のソースを示します。 Real-Time CDP Collaborationの現在のリリースでは、サポートされているソースはAdobe Experience Platformのみです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソースとなるデータ接続。 名前を選択して、データ接続を表示できます。 |
| **[!UICONTROL 接続アクセス]** | オーディエンスがプライベートかパブリックかを定義します。 公開オーディエンスは、重複レポートで検出でき、プロジェクト内でアクティブ化できます。 |
| **[!UICONTROL 作成日]** | オーディエンスがReal-Time CDP Collaborationに読み込まれた日時を示します。 |
| **[!UICONTROL 最終更新日]** | オーディエンスのいずれかの側面が更新された最終日時を示します。 |

![ 読み込まれたすべてのオーディエンスを表示するマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

オーディエンスに対してクイックアクションを実行するには、オーディエンス名の横にある省略記号 **...** を選択します。 次のオプションがあります。

* **[!UICONTROL カテゴリを編集]** を使用すると、オーディエンスに様々なカテゴリタグを追加できます。 詳しくは、以下の [ カテゴリ ](#categories) の節を参照してください。
* **[!UICONTROL 削除]** は、データ接続からオーディエンスを削除します。

![ 省略記号メニューが開き、「カテゴリを編集」オプションと「削除」オプションがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png)

## 個々のオーディエンスの表示 {#view-individual-audiences}

個々のオーディエンスの詳細を表示し設定を編集するには、**[!UICONTROL マイオーディエンス]** ワークスペースからオーディエンスを選択します。 オーディエンスワークスペースには、選択したオーディエンスに関する詳細情報（詳細、ID、カテゴリ、接続アクセス、メタデータの表示設定など）が表示されます。

### オーディエンスの詳細

個々のオーディエンスに対して、次の情報が表示されます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ステータス]** | オーディエンスがアクティブであり、プロジェクトで使用できるかどうかを示します。 |
| **[!UICONTROL ソース]** | オーディエンスのインポート元のソースを示します。 Real-Time CDP Collaborationの現在のリリースでは、サポートされているソースはAdobe Experience Platformのみです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソースとなるデータ接続。 |
| **[!UICONTROL 最終更新日]** | オーディエンスが最後に更新された日時を示します。 |
| **[!UICONTROL 最終更新者]** | オーディエンスを最後に更新したユーザーを示します。 |
| **[!UICONTROL 作成日]** | オーディエンスがReal-Time CDP Collaborationに読み込まれた日時を示します。 |
| **[!UICONTROL 作成者]** | オーディエンスをReal-Time CDP Collaborationに読み込んだユーザーを示します。 |

![ 個々のオーディエンスのワークスペース ](/help/assets/setup/add-manage-audiences/audience-details.png)

さらに、オーディエンスワークスペースでは次のコントロールを使用できます。

* **[!UICONTROL 削除]**：データ接続からオーディエンスを削除します。
* **[!UICONTROL 編集]**：オーディエンスの名前または説明を編集します。

![ 「編集と削除」オプションがハイライト表示された個々のオーディエンスのワークスペース。](/help/assets/setup/add-manage-audiences/audience-details-edit-delete.png)

次に、オーディエンスのワークスペース内の次のセクションを更新できます。

* [ID](#identities)
* [カテゴリ](#categories)
* [接続アクセス](#connection-access)
* [メタデータの表示](#metadata-visibility)

### ID {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="ID"
>abstract="このオーディエンスを構成する ID の分類ビュー、および各 ID を持つプロファイルの合計数。"

「**[!UICONTROL ID]**」セクションには、オーディエンスのインポート時に選択した ID のいずれかでオーディエンスに存在するプロファイルの数が示されます。 また、セクションには ID の分類も含まれているので、オーディエンス母集団を最大限に活用している ID を特定できます。

![ 個々のオーディエンスのワークスペースの ID セクション。](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

### カテゴリ {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="カテゴリ"
>abstract="整理、フィルタリング、検索を簡単にするために、オーディエンスにタグを付けます。 複数のカテゴリでオーディエンスをタグ付けし、これらのカテゴリタグを使用して、製品の他の領域で目的のオーディエンスをフィルタリングできます。"

オーディエンスの整理、フィルタリングおよび取得を簡単にするために、オーディエンスにタグを付けることができます。 オーディエンスに複数のカテゴリのタグを付けた後、オーディエンスの重複レポートを実行する際に、これらのカテゴリタグを使用して [ 検出 ](/help/guide/collaborate/discover.md) 製品領域で目的のオーディエンスをフィルタリングできます。

カテゴリを追加するには、「**[!UICONTROL カテゴリ]**」セクション内の「**[!UICONTROL 編集]**」オプションを選択します。

![ 個々のオーディエンスのワークスペースのカテゴリセクション。](/help/assets/setup/add-manage-audiences/audience-details-categories.png)

**[!UICONTROL カテゴリ]** ダイアログが表示され、オーディエンスに追加するカテゴリを選択できます。 個々のカテゴリを選択するには、カテゴリ名の横にあるチェックボックスをオンにします。

![ 使用可能なカテゴリが表示されたカテゴリダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-categories-select.png)

### 接続アクセス {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="接続アクセス"
>abstract="<p>オーディエンスには、パブリック、プライベート、カスタムの 3 つのタイプがあります。</p><p> 共同作業者がいるプロジェクトでの使用の可用性は、接続アクセス設定に基づいて異なります。接続アクセスは、常にプライベートからパブリックに変更できますが、共同作業者とオーディエンスをアクティブ化した後で設定を元に戻すことはできません。</p>"

共同作業者と共にプロジェクトで使用するオーディエンスの可用性は、接続アクセス設定に基づいて異なります。 「**[!UICONTROL 接続アクセス]**」セクションでは、オーディエンスをプライベートにするか、接続で使用可能で検出可能にするかを選択できます。

オーディエンスの接続アクセスを更新するには、「**[!UICONTROL 接続アクセス]**」セクション内の **[!UICONTROL 編集]** オプションを選択します。

![ 個々のオーディエンスのワークスペースの「接続アクセス」セクション ](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png)

**[!UICONTROL 接続アクセス]** ダイアログが表示され、使用可能な 3 つの接続アクセスオプションが示されます。

* **[!UICONTROL 非公開オーディエンス]**. これらのオーディエンスは、重複レポートや共同作業者との接続でのアクティブ化には *使用できません*。 共同作業者がオーディエンスを表示または使用することはできませんが、**[!UICONTROL オーディエンスの比較 [ セクションの]** すべてのオーディエンス ](/help/guide/collaborate/discover.md#compare-audiences) ビューでは、オーディエンスの母集団が合計母集団に貢献します。 共同作業者と連携してオーディエンスを使用するには、設定をパブリックまたはカスタムに変更します。
* **[!UICONTROL 一般向け]** これらのオーディエンスは、重複レポートや共同作業者との連携でアクティブ化するために使用できます。
* **[!UICONTROL カスタムオーディエンス]**。 これらのオーディエンスは、重複レポートや、指定された接続でのみアクティブ化するために使用できます。 共同作業者がオーディエンスを表示または使用することはできませんが、**[!UICONTROL オーディエンスの比較 [ セクションの]** すべてのオーディエンス ](/help/guide/collaborate/discover.md#compare-audiences) ビューでは、オーディエンスの母集団が合計母集団に貢献します。

目的の接続アクセスオプションを選択し、「**[!UICONTROL 保存]**」を選択して変更を適用します。

![ 使用可能なオプションが表示された接続アクセスダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

>[!IMPORTANT]
>
>アクセスステータス（パブリック、プライベート、カスタム）に関係なく、任意のオーディエンスの母集団は、プロジェクト内の **[!UICONTROL オーディエンスを比較]** セクションの **[!UICONTROL すべてのオーディエンス]** 母集団に貢献します。<br>

共同作業者と共にプロジェクトで使用するオーディエンスの可用性は、接続アクセス設定に基づいて異なります。 接続アクセスは、いつでもプライベートからパブリックに変更できますが、オーディエンスがアクティブ化された後にその設定を元に戻すことはできません。

### メタデータの表示 {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="メタデータの表示"
>abstract="<p>組織に接続する前に、他の組織に表示するオーディエンスのメタデータを示します。 </p> <p> **ID 数**&#x200B;は、検出タブで重複レポートを表示する際に、パートナーがオーディエンスの ID 数を表示できるかどうかを制御します。**オーディエンスの重複％**&#x200B;は、共同編集者が自分のオーディエンスとユーザーのオーディエンスの重複の割合を検出できるかどうかを制御します。"

>[!NOTE]
>
>共同作業者がすべてのオーディエンスをプライベートに設定している場合、**[!UICONTROL 検出]** ワークスペースのプロジェクトの **[!UICONTROL 関連オーディエンス]** セクションは空白になります。 詳しくは、[discover](/help/guide/collaborate/discover.md#relevant-audiences) を参照してください。 ガイド。

メタデータの表示は、オーディエンスが組織に接続する前、または様々なプロジェクトビュー内で他の組織にオーディエンスのメタデータを表示することを示します。 オーディエンスのメタデータの表示を更新するには、「**[!UICONTROL メタデータの表示]** セクション内の **[!UICONTROL 編集]** オプションを選択します。

![ 個々のオーディエンスのワークスペースのメタデータ表示セクション ](/help/assets/setup/add-manage-audiences/audience-details-metadata.png)

**[!UICONTROL メタデータの表示]** ダイアログが表示され、オーディエンスの表示設定を指定できます。 各オーディエンスに対して設定できるメタデータの表示設定は 2 つあります。

**[!UICONTROL ID 数を表示]**：この設定は、プロジェクト内の [ 「検出」タブで重複レポートを表示 ](/help/guide/collaborate/discover.md#discover-overlaps) する際に、共同作業者がオーディエンスの ID 数を表示できるかどうかを制御します。

**[!UICONTROL オーディエンスの重複を表示 %]**:true に設定すると、共同作業者は、オーディエンスとオーディエンスの間で [ 重複率を検出 ](/help/guide/collaborate/discover.md#compare-audiences) できます。

![ 使用可能なオプションが表示されたメタデータの表示ダイアログ ](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

## 次の手順

オーディエンスをインポートしたら、パブリッシャーを見つけて [ 接続 ](/help/guide/connect/establishing-connections.md) し、プロジェクトとの共同作業を開始します。
