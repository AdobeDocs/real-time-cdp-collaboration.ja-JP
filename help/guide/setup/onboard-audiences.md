---
title: Sourceとオーディエンスの管理
description: Adobe Real-Time CDP Collaborationでのオーディエンスの調達方法と管理方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0a5158fa-73d3-4406-af20-2b6c7be9934e
TQID: https://experienceleague.adobe.com/aGnYCTj23Tth2Hbq1Y-ALmFPVa36vKCYWXVu3-8wf0Q
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 3680
ht-degree: 18%

---

# Sourceとオーディエンスの管理

{{limited-availability-release-note}}

オーディエンスとは、さまざまな属性にもとづいてセグメント化された、特定のユーザーや顧客のグループのことです。 これにより、共同作業者は協力して、より効果的な広告キャンペーンを実現するための、ターゲットマーケティングとパーソナライズされたエクスペリエンスに取り組むことができます。 このガイドでは、Real-Time CDP Collaborationでオーディエンスを取得する方法、オーディエンスダッシュボードを表示する方法、個々のオーディエンスを管理する方法について説明します。

## SourceからCollaborationへのオーディエンス {#source-audiences}

>[!IMPORTANT]
>
>オーディエンスを取得するには、2つのプロファイル管理権限&#x200B;**[!UICONTROL プロファイルの表示]**&#x200B;と&#x200B;**[!UICONTROL セグメントの表示]**&#x200B;を含む役割にユーザーを割り当てる必要があります。 必要な権限の割り当てについて詳しくは、「権限」の「[ オーディエンスソーシング ](../permissions/overview.md#audience-sourcing) ガイド」を参照してください。

共同作業者とのオーディエンスをアクティブ化し、重複の計算を実行する前に、オーディエンスをCollaborationにソースする必要があります。 オーディエンスを取得するには、以下のセクションのワークフロー手順に従います。

**[!UICONTROL セットアップ]** ワークスペース内の&#x200B;**[!UICONTROL マイオーディエンス]** タブから、追加アイコン（![追加アイコン ](/help/assets/icons/plus.png)）を選択します。 **[!UICONTROL Audience]**&#x200B;を選択します。 これが初めてのオーディエンスの場合は、**[!UICONTROL 追加] オプション**&#x200B;を選択することもできます。

![追加オプションとオーディエンスオプションがハイライト表示された自分のオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/add-audiences.png){zoomable="yes"}

### データ接続の選択 {#select-data-connection}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_audience_marketing_actions"
>title="マーケティングアクション"
>abstract="<p>マーケティングアクションを使用して、Experience Platform から Real-Time CDP Collaboration に読み込むオーディエンスデータを制御します。 <strong>データ共同作業</strong>マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。 <strong>データサイエンス</strong>マーケティングアクションは、C9 データ使用ラベルをサポートしています。</p> <p> <ul><li> チェックボックスを<em>有効</em>にすると、Experience Platform で上記のラベルが付いているデータは除外され、Real-Time CDP Collaboration には取り込まれ<strong>ません</strong>。</li><li> チェックボックスを<em>無効</em>にすると、Experience Platform から Real-Time CDP Collaboration にすべてのデータがソースとされます。</li></ul></p>"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=ja" text="データ使用ラベルの概要"
>additional-url="https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=ja" text="データ使用ラベルの用語集"

>[!IMPORTANT]
>
>最初のデータ接続を確立し、最初のオーディエンスをソーシングしたら、既存のデータ接続から複数のオーディエンスをソーシングできます。 追加オーディエンスを追加する場合は、データ接続が既に確立されているため、[ オーディエンスの選択](#select-audiences)の手順から開始します。

データ接続は、オーディエンスをCollaborationに取り込むソースです。 サポートされているソースには、Adobe Experience Platform、CSV ファイルのアップロード、[!DNL Amazon S3]、[!DNL Snowflake]および[!DNL Google Cloud Storage]があり、それぞれ独自のワークフローを使用します。

以下のセクションでは、**Adobe Experience Platform**&#x200B;を選択し、Experience Platform固有の手順（サンドボックス、ガバナンス、同意）を完了する方法について説明します。 CSV、[!DNL Amazon S3]、[!DNL Snowflake]または[!DNL Google Cloud Storage]を選択した場合は、そのオプションの[ データソースを選択](#select-data-source)の下にリンクされているガイドを使用します。

Experience Platform データ接続に対して設定した設定は、その接続からソースされたすべてのオーディエンスに適用されます。

>[!TIP]
>
>データ接続を表示および編集できる別のワークフローがあります。 詳細については、[ データ接続の管理](/help/guide/setup/manage-data-connection.md) ガイドを参照してください。

データ接続の追加を開始するには、**[!UICONTROL 新しいデータ接続を追加]**&#x200B;を選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![新しいデータ接続を追加オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

#### データソースを選択

次に、データ接続のソースを選択します。 利用可能なソースは次のとおりです。

* **Adobe Experience Platform**: Adobe Experience Platformからオーディエンスを取り込むには、このオプションを選択します。
* **CSV ファイル**: オーディエンスデータを含むCSV ファイルをアップロードして、すばやく簡単にデータを取り込みます。 開始するには、「[ オーディエンスソーシング用CSV ファイルのアップロード ](./upload-csv-audience-sourcing.md)」ガイドを参照してください。
* **Amazon Web Services**: Amazon S3 ストレージに接続して、S3 バケットから直接オーディエンスデータを取得します。 詳しい手順については、「[ オーディエンスソーシング用にAWS S3を設定](./configure-aws-s3-audience-sourcing.md) ガイド」を参照してください。
* **Snowflake**: Snowflake データウェアハウスを使用して、オーディエンスデータをシームレスに取り込みます。 オーディエンスのソーシング ](./configure-snowflake-audience-sourcing.md)については、[設定 [!DNL Snowflake]  ガイドを参照してください。
* **Google Cloud Storage**:GCS バケットに接続してソースオーディエンスデータを取得します。 詳しい手順については、[ オーディエンスソーシング用GCSの設定](./configure-gcs-audience-sourcing.md) ガイドを参照してください。

データソースを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![Adobe Experience Platform オプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-data-connection-source.png){zoomable="yes"}

#### サンドボックスを選択

データソースを選択したら、Collaborationに使用するオーディエンスを含むサンドボックスを選択する必要があります。 使用可能なサンドボックスのリストからサンドボックスを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します

![ サンドボックスを選択したオーディエンスの追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-sandbox.png){zoomable="yes"}

#### ガバナンスポリシーと適用アクション {#governance-policy-and-enforcement-actions}

次に、ソースとなるデータに対して適切なマーケティング施策を設定する必要があります。 また、データコラボレーションに使用するために、Experience Platformから取得したデータに対して同意を得る必要もあります。

マーケティングアクションを使用して、Experience PlatformからCollaborationに取り込むオーディエンスデータを制御します。 **[!UICONTROL データ共同作業]**&#x200B;マーケティングアクションは、C4、C5、C9 データ使用ラベルをサポートしています。 **[!UICONTROL データサイエンス]**&#x200B;マーケティングアクションは、C9 データ使用ラベルをサポートしています。

[C4、C5、およびC9 データ使用ラベル ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference#contract){target="_blank"}の詳細をご確認ください。

* チェックボックスが&#x200B;***enabled***&#x200B;の場合、上記のようにExperience Platformでラベル付けされたデータは除外され、**not**&#x200B;がCollaborationに取り込まれます。
* チェックボックス ***disabled***&#x200B;を使用すると、Experience Platformから取得したデータに制限はありません。

データ使用ラベルの詳細については、Experience Platformのドキュメントを参照してください。

* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
* [データ使用ラベルの用語集](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference){target="_blank"}

さらに、Collaborationに取り込むデータに適用する同意ルールを選択します。

![ ガバナンスポリシーと履行アクションのセクションにある「オーディエンスを追加」ワークスペース。](/help/assets/setup/add-manage-audiences/data-collaboration-consent.png){zoomable="yes"}

マーケティング活動と同意ルールを選択したら、**[!UICONTROL 次]**&#x200B;を選択して次の手順に進みます。 条件に同意するよう求める確認ダイアログが表示されます。 チェックボックスを選択し、**[!UICONTROL OK]**&#x200B;を選択して確認します。

![ チェックボックスと「OK」オプションがハイライト表示されたガバナンスポリシーと履行アクションのダイアログ。](/help/assets/setup/add-manage-audiences/data-collaboration-consent-confirmation.png){zoomable="yes"}

### 詳細を入力

次に、データ接続の名前と説明を入力します。 この情報は、後でデータ接続を特定するのに役立ちます。

![名前と説明を指定するオプションを含むオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/data-connection-details.png){zoomable="yes"}

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

次に、ソースフィールドを選択して、Collaborationのターゲットフィールドにマッピングします。 使用可能なターゲットフィールドは、アカウントの設定中に選択した照合キーに基づきます。

>[!IMPORTANT]
>
>現在、新しいマップフィールドを含めるようにデータ接続を編集することはできません。 データ接続を作成した後に新しい照合キーをアカウントに追加する場合は、新しいデータ接続を作成してマッピングする必要があります。

![ ソースフィールドをターゲットフィールドにマッピングするオプションを備えたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/add-map-fields.png){zoomable="yes"}

>[!TIP]
>
>複数のソースフィールドを同じターゲットフィールドにマッピングできます。 例えば、Experience Platformの2つの別々のフィールドに電子メールアドレスがある場合、それぞれに&#x200B;**[!UICONTROL ハッシュ化された電子メール]**&#x200B;のターゲットフィールドを2つの別々の行としてマッピングできます。 「**[!UICONTROL フィールドを追加]**」オプションを使用して、マッピング行を追加します。

>[!BEGINSHADEBOX]

**[!UICONTROL Source フィールド]**&#x200B;は、Experience PlatformのID名前空間と属性です。 これには、[標準](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html?lang=ja#standard){target="_blank"}と[ カスタム ](https://experienceleague.adobe.com/docs/experience-platform/identity/features/namespaces.html#create-namespaces){target="_blank"}の両方のID名前空間が含まれます。 また、[union スキーマ ](https://experienceleague.adobe.com/docs/experience-platform/profile/union-schemas/union-schema.html?lang=ja){target="_blank"}に存在し、XDM Individual Profile クラスに属するプロファイル属性も含まれます。

Source フィールドは、Collaborationで定義されたターゲットフィールドにマッピングされます。

**[!UICONTROL ターゲットフィールド]**&#x200B;は、CollaborationでのIDの参照方法を示します。 ターゲットフィールドは、アカウント設定時に選択した一致キーです。 デフォルトでは、選択したすべての一致キーを使用できます。

ハッシュ化されたフィールドに&#x200B;*非ハッシュ化された* フィールドをソーシングする場合は、**[!UICONTROL 変換を適用]** オプションを使用します。 Collaborationがハッシュ化を適用し、フィールドを変換します。 Adobeで使用されるハッシュアルゴリズムはSHA256です。

>[!ENDSHADEBOX]

フィールドのマッピングを開始するには、ターゲットフィールドの横にある空のソースフィールドを選択します。 **[!UICONTROL ソースフィールドを選択]** ダイアログが表示されます。 **[!UICONTROL ID名前空間]**&#x200B;と&#x200B;**[!UICONTROL プロファイル属性]**&#x200B;のオプションを選択して、目的のソースフィールドを見つけ、リストからフィールドを選択します。 検索オプションを使用して、目的のフィールドを見つけることもできます。

![電子メールオプションが表示された「ソースフィールドを選択」ダイアログ。](/help/assets/setup/add-manage-audiences/select-source-field.png){zoomable="yes"}

ハッシュ化されていないフィールドをハッシュ化されたターゲットフィールドにソーシングするには、**[!UICONTROL 変換を適用]** オプションを使用します。 例えば、2番目の電子メールフィールドを追加するには、**[!UICONTROL フィールドを追加]** オプションを選択して新しい行を追加し、ターゲットフィールドに&#x200B;**[!UICONTROL ハッシュ化された電子メール]**&#x200B;を選択します。 ハッシュ化されていないメールソースフィールドを選択し、**[!UICONTROL 変換を適用]**&#x200B;を選択します。

![電子メールソースフィールドがターゲットフィールドにマッピングされ、変換の適用が1つに対してオンに切り替えられたオーディエンスの追加ワークスペース。](/help/assets/setup/add-manage-audiences/apply-transformation.png){zoomable="yes"}

各ターゲットフィールドのマッピングペアを引き続き追加します。 一致キーを使用しない場合は、フィールドの横にある削除（![削除アイコン ](/help/assets/icons/delete.png)）アイコンを使用して削除できます。 一致するキーが削除されると、接続からオーディエンスを取得する際に使用できなくなります。

![ ターゲットフィールドの横に「削除」オプションが表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/remove-target-field.png){zoomable="yes"}

フィールドのマッピングが完了したら、**[!UICONTROL 次へ]**&#x200B;を選択して続行します。

![ マップフィールドが入力され、次のオプションがハイライト表示されたオーディエンスを追加ワークスペース。](/help/assets/setup/add-manage-audiences/confirm-field-mapping.png){zoomable="yes"}

### スケジュール {#schedule}

次に、オーディエンスの入力を開始および終了するタイミングをスケジュールします。 このスケジュールに従ってオーディエンスが更新されます。

![ スケジュール設定オプションが表示されたオーディエンスの追加ワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling.png){zoomable="yes"}

>[!IMPORTANT]
>
>オーディエンスの更新頻度を調整すると、オーディエンスの更新ごとに計算される[ オーディエンス管理クレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities)を管理するのに役立ちます。 より高い頻度を選択すると、オーディエンス発見レポートやオーディエンスのアクティベーションで利用できるデータの鮮度に影響を与える可能性があります。

**[!UICONTROL 頻度]** ドロップダウンから、オーディエンスの更新の頻度を選択します。

![頻度ドロップダウンが開いたオーディエンスの追加スケジュール ワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png){zoomable="yes"}

次に、**[!UICONTROL 日付範囲]**&#x200B;を選択します。 開始日は、オーディエンスがプロファイルの入力を開始する日で、終了日はオーディエンスの更新を停止する日です。

![日付範囲オプションが表示されたオーディエンスの追加スケジュール ワークスペース。](/help/assets/setup/add-manage-audiences/audience-scheduling-date-range.png){zoomable="yes"}

>[!IMPORTANT]
>
>日付範囲の終了日の後、このデータ接続からソースされたすべてのオーディエンスが更新を停止します。 接続を更新するには、[ データ接続の管理](/help/guide/setup/manage-data-connection.md) ガイドに従ってください。

### オーディエンスを選択 {#select-audiences}

オーディエンスソースを選択したら、含める特定のオーディエンスを選択します。 検索およびフィルターオプションを使用して、データ接続から関連オーディエンスを見つけます。 目的のオーディエンスを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![使用可能なオーディエンスのリストを含むオーディエンスの追加ワークスペース。](/help/assets/setup/add-manage-audiences/select-audience.png){zoomable="yes"}

### レビュー

オーディエンスの追加を確定する前に、すべての設定と設定を確認します。 すべての詳細が正しいことを確認してから、**[!UICONTROL 完了]**&#x200B;を選択して、データ接続の作成を完了します。

![すべての選択設定が表示されたオーディエンスの追加ワークスペース。](/help/assets/setup/add-manage-audiences/review-connection.png){zoomable="yes"}

## オーディエンスダッシュボードの表示 {#view-audiences-dashboard}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_missing_identities"
>title="ID の欠落"
>abstract="ID 数は、設定されたスケジュールに従って次回データ接続を更新した後に使用できます。 最初の更新は通常、データ接続を設定してから 24 時間以内に行われます。 継続的な更新は、設定されたスケジュールに従います。"

オーディエンスのソーシング後、**[!UICONTROL マイオーディエンス]** ワークスペースには、現在Collaborationにソーシングされているすべてのオーディエンスが表示されます。

![ マイオーディエンスワークスペースに、ソースされたすべてのオーディエンスが表示されます。](/help/assets/setup/add-manage-audiences/audiences-workspace.png)

各オーディエンスには、次の情報の概要が含まれます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ID]** | このオーディエンスに存在するIDの数を示します。 同じプロファイルに2つ以上のIDがあり、これらのIDがプロジェクトで一致キーとして使用されている場合、プロファイルはカウントに2回表示されます。 |
| **[!UICONTROL ステータス]** | オーディエンスがアクティブで、プロジェクトで使用できるかどうかを示します。 **[!UICONTROL 保留中]**&#x200B;のステータスは、オーディエンスが最近取得されたばかりで、IDがまだ入力されていないことを示します。 ソース側のオーディエンスは、初回更新後にプロファイルが入力されます。通常、データ接続の設定から24時間以内に行われます。 |
| **[!UICONTROL ソース]** | オーディエンスのソース元を示します。 現在のリリースのCollaborationでは、Experience Platformが唯一のサポート対象ソースです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソース元のデータ接続。 名前を選択して、データ接続を表示できます。 |
| **[!UICONTROL 接続アクセス]** | オーディエンスがプライベートかパブリックかを定義します。 公開オーディエンスは、重複レポートで見つけ出し、プロジェクト内でアクティブ化できます。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初にCollaborationに送信された日付を示します。 |
| **[!UICONTROL 最終更新日]** | Collaborationでオーディエンスが更新された最後の日時を示します。 これは、オーディエンスが最後に更新された時期ではなく、オーディエンスの設定やメタデータが最後に変更された時期を指します。 |

![ マイオーディエンスワークスペースに、ソースされたすべてのオーディエンスが表示されます。](/help/assets/setup/add-manage-audiences/audiences-workspace.png){zoomable="yes"}

オーディエンスに対してクイックアクションを実行するには、オーディエンス名の横にある省略記号&#x200B;**...**&#x200B;を選択します。 次のオプションがあります。

* **[!UICONTROL カテゴリを編集]**&#x200B;すると、異なるカテゴリタグをオーディエンスに追加できます。 詳しくは、以下の「[ カテゴリ ](#categories)」の節を参照してください。
* **[!UICONTROL 削除]**&#x200B;は、データ接続からオーディエンスを削除します。

![省略記号メニューが表示されているマイオーディエンスワークスペースが開き、「カテゴリを編集」および「削除」オプションがハイライト表示されている](/help/assets/setup/add-manage-audiences/audiences-ellipsis-menu.png){zoomable="yes"}。

## 個々のオーディエンスを表示 {#view-individual-audiences}

個々のオーディエンスの情報を表示および更新するには、**[!UICONTROL マイオーディエンス]** ワークスペースからオーディエンスを選択します。 オーディエンスワークスペースには、選択したオーディエンスの詳細（詳細、ID、カテゴリー、接続アクセス、メタデータの表示設定など）が表示されます。

### オーディエンスの詳細

個々のオーディエンスに対して、次の情報が表示されます。

| 項目 | 説明 |
|----------|---------|
| **[!UICONTROL ステータス]** | オーディエンスがアクティブで、プロジェクトで使用できるかどうかを示します。 |
| **[!UICONTROL ソース]** | オーディエンスのソース元を示します。 現在のリリースのCollaborationでは、Experience Platformが唯一のサポート対象ソースです。 |
| **[!UICONTROL データ接続]** | オーディエンスのソース元のデータ接続。 |
| **[!UICONTROL 最終更新日]** | Collaborationでオーディエンスが更新された最後の日時を示します。 これは、オーディエンスが最後に更新された時期ではなく、オーディエンスの設定またはメタデータが最後に変更された時期を指します |
| **[!UICONTROL 最終更新者]** | オーディエンスを最後に更新したユーザーを示します。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初にCollaborationに送信された日付を示します。 |
| **[!UICONTROL 作成者]** | オーディエンスをCollaborationにソースしたユーザーを示します。 |

![個々のオーディエンスのワークスペース。](/help/assets/setup/add-manage-audiences/audience-details.png){zoomable="yes"}

#### ID {#identities}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_identities"
>title="ID"
>abstract="一致キーで区切られた、このオーディエンスを構成する ID の分類ビュー。"

「**[!UICONTROL ID]**」セクションは、オーディエンスに存在するIDの数を示します。 このセクションには、オーディエンスの構成を理解するのに役立つ、一致キーによるIDの分類も含まれています。

![個々のオーディエンスのワークスペースの「ID」セクション。](/help/assets/setup/add-manage-audiences/audience-details-identities.png){zoomable="yes"}

一致キーの分類の個々のセクションにカーソルを合わせると、関連するキーの正確なID数が表示されます。

![一致キーの分類が表示されている個々のオーディエンスのワークスペースの「ID」セクション。](/help/assets/setup/add-manage-audiences/audience-details-identities.png)

#### カテゴリ {#categories}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_categories"
>title="カテゴリ"
>abstract="整理、フィルタリング、検索を簡単にするために、オーディエンスにタグを付けます。 複数のカテゴリでオーディエンスをタグ付けし、これらのカテゴリタグを使用して、製品の他の領域で目的のオーディエンスをフィルタリングできます。"

オーディエンスの整理、フィルタリング、検索を容易におこなうために、オーディエンスにタグを付けることができます。 オーディエンスに複数のカテゴリを付けてタグ付けし、これらのカテゴリ タグを使用して、オーディエンス重複レポートを実行する際に、[discover](/help/guide/collaborate/discover.md)製品エリアで目的のオーディエンスをフィルタリングできます。

カテゴリを追加するには、**[!UICONTROL カテゴリ]** セクション内の&#x200B;**[!UICONTROL 編集]** オプションを選択します。

![個々のオーディエンスのワークスペースの「カテゴリ」セクション。](/help/assets/setup/add-manage-audiences/audience-details-categories.png){zoomable="yes"}

「**[!UICONTROL カテゴリー]**」ダイアログが表示され、オーディエンスに追加するカテゴリーを選択できます。 個々のカテゴリを選択するには、カテゴリ名の横にあるチェックボックスを選択します。


#### 接続アクセス {#connection-access}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_connection_access"
>title="接続アクセス"
>abstract="<p>オーディエンスには、パブリック、プライベート、カスタムの 3 つのタイプがあります。</p><p> 共同作業者がいるプロジェクトにおける使用の可用性は、接続アクセス設定に基づいて異なります。</p>"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_access"
>title="詳細情報"
>abstract=""

コラボレーターを含むプロジェクトでのオーディエンスの使用の可用性は、接続アクセス設定によって異なります。 「**[!UICONTROL 接続アクセス]**」セクションでは、オーディエンスをプライベートにするか、パブリックにするか、特定の接続でのみ使用するかを選択できます。 公開オーディエンスは、接続で利用でき、検索できます。

オーディエンスの接続アクセスを更新するには、**[!UICONTROL 接続アクセス]** セクション内の&#x200B;**[!UICONTROL 編集]** オプションを選択します。

![個々のオーディエンスのワークスペースの接続アクセス セクション。](/help/assets/setup/add-manage-audiences/audience-details-connection-access.png){zoomable="yes"}

**[!UICONTROL 接続アクセス]** ダイアログが表示され、使用可能な3つの接続アクセス オプションが表示されます。

* **[!UICONTROL プライベートオーディエンス]**。 これらのオーディエンスは、*not*&#x200B;です。重複レポートで使用したり、共同作業者との接続でアクティブ化したりできます。 共同作業者がオーディエンスを表示または使用することはできませんが、オーディエンスの母集団は、[ オーディエンスの比較セクション ](/help/guide/collaborate/discover.md#compare-audiences)の&#x200B;**[!UICONTROL すべてのオーディエンス]** ビューの合計母集団に引き続き貢献します。 設定をパブリックまたはカスタムに変更して、共同作業者との接続でオーディエンスを使用します。
* **[!UICONTROL 公開オーディエンス]**。 これらのオーディエンスは、重複レポートで使用したり、共同作業者との接続でアクティブ化したりできます。
* **[!UICONTROL カスタムオーディエンス]**。 これらのオーディエンスは、重複レポートで使用したり、指定した接続でのみアクティブ化したりできます。 共同作業者がオーディエンスを表示または使用することはできませんが、オーディエンスの母集団は、[ オーディエンスの比較セクション ](/help/guide/collaborate/discover.md#compare-audiences)の&#x200B;**[!UICONTROL すべてのオーディエンス]** ビューの合計母集団に引き続き貢献します。

目的の接続アクセス オプションを選択し、**[!UICONTROL 保存]**&#x200B;を選択して変更を適用します。

![使用可能なオプションが表示された接続アクセス ダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png){zoomable="yes"}

>[!IMPORTANT]
>
>アクセス状態（パブリック、プライベート、またはカスタム）に関係なく、任意のオーディエンスの母集団は、プロジェクト内の&#x200B;**[!UICONTROL オーディエンスの比較]** セクションの&#x200B;**[!UICONTROL すべてのオーディエンス]**&#x200B;母集団に貢献します。

コラボレーターを含むプロジェクトで使用できるオーディエンスの可用性は、接続アクセス設定によって異なります。

#### メタデータの表示 {#metadata-visibility}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_view_audience_metadata_visibility"
>title="メタデータの表示"
>abstract="<p>他の共同作業者が、ユーザーと接続する前またはプロジェクトビュー内で確認できるオーディエンスのメタデータを示します。</p> <p> **ID 数**&#x200B;は、「検出」タブで重複レポートを表示する際に、共同作業者がオーディエンスの ID 数を表示できるかどうかを制御します。</p><p> **オーディエンス重複％**&#x200B;は、共同編集者が自分のオーディエンスとユーザーのオーディエンス重複割合を検出できるかどうかを制御します。</p><p> **[!UICONTROL オーディエンスインデックス]**&#x200B;は、共同作業者がプロジェクト内のオーディエンスインデックスを表示できるかどうかを制御します。 この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。</p> <br> メタデータの表示設定を有効にするには、オーディエンスをパブリックまたはカスタムに設定する必要があります。"

>[!NOTE]
>
>共同作業者がすべてのオーディエンスを非公開に設定している場合、**[!UICONTROL もっと知る]** ワークスペースのプロジェクトの&#x200B;**[!UICONTROL 関連オーディエンス]** セクションは空白になります。 詳しくは、[discover](/help/guide/collaborate/discover.md#relevant-audiences) ガイドを参照してください。

メタデータの可視性とは、オーディエンスのメタデータが、他の共同作業者に公開される前や、異なるプロジェクトビュー内で表示されることを示します。 オーディエンスのメタデータの表示を更新するには、**[!UICONTROL メタデータの表示]** セクション内の&#x200B;**[!UICONTROL 編集]** オプションを選択します。

![個々のオーディエンスのワークスペースのメタデータ表示セクション。](/help/assets/setup/add-manage-audiences/audience-details-metadata-visibility.png){zoomable="yes"}

**[!UICONTROL メタデータの表示]** ダイアログが表示され、オーディエンスの表示設定を設定できます。 各オーディエンスに対して設定できるメタデータの表示設定は2つあります。

**[!UICONTROL ID数を表示]**：この設定は、プロジェクト内の「検出」タブ ](/help/guide/collaborate/discover.md#discover-overlaps)で[重複レポートを表示する際に、共同作業者がオーディエンスのID数を表示できるかどうかを制御します。

**[!UICONTROL オーディエンスの重複を表示%]**：この設定は、共同作業者がオーディエンスとオーディエンス間の重複パーセンテージ ](/help/guide/collaborate/discover.md#compare-audiences)を[見つけることができるかどうかを制御します。

**[!UICONTROL オーディエンスインデックス]**:trueに設定すると、共同作業者はプロジェクト内の[ オーディエンスインデックス ](/help/guide/collaborate/discover.md#audience-index-score)を表示できます。 この機能は、3 つ以上のアクティブオーディエンスがある場合にのみ使用できます。

>[!NOTE]
>
>メタデータの表示設定を有効にするには、オーディエンスをパブリックまたはカスタムに設定する必要があります。

![使用可能なオプションが表示されたメタデータの表示ダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png){zoomable="yes"}

## 複数のオーディエンスを編集 {#edit-audiences}

オーディエンスダッシュボードでは、複数のオーディエンスを一度に編集できます。 編集するオーディエンスを選択するには、オーディエンス名の横にあるボックスを選択します。 オーディエンスを選択したら、編集メニューのオプションを使用してアクションを実行できます。

![2つのオーディエンスが選択され、編集メニューがハイライト表示されたマイオーディエンスワークスペース。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit.png)

### Bulk edit metadata visibility {#bulk-edit-metadata-visibility}

With your audiences selected in the audience dashboard, select **[!UICONTROL Edit metadata visibility]** from the edit menu.

![The My audiences workspace with the Edit metadata visibility option highlighted.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-metadata.png)

The **[!UICONTROL Metadata visibility]** dialog appears, allowing you to configure the visibility settings for the selected audiences. By default, none of options will be selected. Choose the options you want to apply to all selected audiences, and then select **[!UICONTROL Save]**.

![使用可能なオプションが表示されたメタデータの表示ダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-metadata-dialog.png)

### Bulk edit connection access {#bulk-edit-connection-access}

With your audiences selected in the audience dashboard, select **[!UICONTROL Edit connection access]** from the edit menu.

![The My audiences workspace with the Edit connection access option highlighted.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-connection-access.png)

The **[!UICONTROL Connection access]** dialog appears, allowing you to configure the access settings for the selected audiences. By default, the **[!UICONTROL Private audience]** option will be selected. Choose the options you want to apply to all selected audiences, and then select **[!UICONTROL Save]**.

![使用可能なオプションが表示された接続アクセス ダイアログ。](/help/assets/setup/add-manage-audiences/audience-details-connection-access-dialog.png)

### Bulk edit audience names and descriptions {#bulk-edit-audience-names-descriptions}

With your audiences selected in the audience dashboard, select **[!UICONTROL Edit name and description]** from the edit menu.

![The My audiences workspace with the Edit name and description option highlighted.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description.png)

The **[!UICONTROL Name and description]** dialog appears, allowing you to configure the name and description for each selected audience. By default, the current names and descriptions will be displayed for each audience. Make your changes and then select **[!UICONTROL Save]**.

![The Name and description dialog with the available options displayed.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-name-description-dialog.png)

### Bulk edit categories {#bulk-edit-categories}

With your audiences selected in the audience dashboard, select **[!UICONTROL Edit categories]** from the edit menu.

![The My audiences workspace with the Edit categories option highlighted.](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories.png)

The **[!UICONTROL Categories]** dialog appears, allowing you to configure the categories for each selected audience. デフォルトでは、カテゴリは選択されません。 カテゴリを選択するには、まずメインカテゴリを選択し、次に含めるサブカテゴリを選択します。 変更を加え、**[!UICONTROL 保存]**&#x200B;を選択します。

![使用可能なオプションが表示されたカテゴリ ダイアログ。](/help/assets/setup/add-manage-audiences/audiences-bulk-edit-categories-dialog.png)

## 次の手順

オーディエンスをソーシングした後、プロジェクトで共同作業を行う[connect](/help/guide/connect/establishing-connections.md)の共同作業者を見つけます。
