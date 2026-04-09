---
title: 測定データの追加と管理
description: Adobe Real-Time CDP Collaborationに測定データを追加する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 739d31b9-3f00-477d-b6be-995c7767c6ca
source-git-commit: 42bbd17878701cfaf2cba170a9471cf5c7285796
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 5%

---

# 測定データの追加と管理 {#add-and-manage-measurement-data}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_onboard_measurement_data"
>title="詳細情報"
>abstract=""

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_target_fields"
>title="ターゲットフィールド"
>abstract="測定ターゲットフィールドのプレースホルダー。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_data_source_fields"
>title="ソースフィールド"
>abstract="測定ソースフィールドのプレースホルダー。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_source_fields"
>title="ソースフィールドのマッピング"
>abstract="ソースフィールドの測定マッピング用プレースホルダー。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_measurement_mapping_target_fields"
>title="ターゲットフィールドのマッピング"
>abstract="ターゲットフィールドの測定マッピング用プレースホルダー。"

{{limited-availability-release-note}}

このドキュメントでは、Adobe Real-Time CDP Collaborationにキャンペーン測定データを追加する手順の概要を説明します。 パブリッシャーは、Adobeチームと協力して、キャンペーン測定データをアップロードできます。 そのデータがアップロードされ、処理されると、パブリッシャーと広告主の両方が広範な[&#x200B; キャンペーン測定レポート &#x200B;](/help/guide/collaborate/measure.md)を表示できるようになります。

## 測定データを追加 {#add-measurement-data}

広告主は、コンバージョンイベントを含む測定データをCollaborationにアップロードして、キャンペーン測定レポートで使用できます。 コンバージョンデータには、通常、ユーザーID （ハッシュ化された電子メールやデバイス IDなど）、コンバージョンイベントのタイムスタンプ、購入やサインアップなどの特定のコンバージョンイベントの詳細などのフィールドが含まれます。

測定データを取得するには、**[!UICONTROL セットアップ]** ワークスペース内の&#x200B;**[!UICONTROL My measurement data]** タブに移動します。 追加アイコン（![追加アイコン。](/help/assets/icons/plus.png)）を選択します **[!UICONTROL 測定データ]**&#x200B;を選択します。

これが最初の測定データである場合は、**[!UICONTROL 追加]** オプションを選択することもできます。

![追加オプションと測定データ オプションがハイライト表示された測定データ タブ。](../../assets/setup/add-manage-measurement-data/add-measurement-data.png){zoomable="yes"}

**[!UICONTROL 測定データを追加]**&#x200B;画面が表示され、ソース測定データへの手順の概要が表示されます。 「**[!UICONTROL オンボーディングの開始]**」を選択します。

![測定データを追加する画面で、測定データを取得するための手順の概要と、オンボーディングを開始するオプションが強調表示されている](../../assets/setup/add-manage-measurement-data/add-measurement-data-screen.png){zoomable="yes"}。

### データ接続と詳細 {#data-connection-and-details}

この手順では、データ接続を設定し、測定データの詳細を指定する必要があります。

#### 測定データタイプを選択 {#select-measurement-data-type}

測定データタイプは、キャンペーン測定に取り込むイベントの種類を定義します。 現在、コンバージョンデータがサポートされているタイプです。

測定データタイプとして&#x200B;**[!UICONTROL コンバージョンデータ]**&#x200B;を選択し、次に&#x200B;**[!UICONTROL 次]**&#x200B;を選択します。

![測定データの種類と次のオプションを強調するデータ接続と詳細の手順](../../assets/setup/add-manage-measurement-data/select-measurement-data-type.png){zoomable="yes"}

#### データ接続の選択 {#select-data-connection}

データ接続とは、Collaborationに測定データを取り込むソースのことです。 最初のデータ接続を確立し、最初の測定データを取得したら、同じデータ接続を使用して追加の測定データを取得し続けることができます。

データ接続を追加するには、**[!UICONTROL 新しいデータ接続を追加]**&#x200B;を選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![新しいデータ接続の追加オプションと次のオプションを強調表示するデータ接続と詳細の手順。](../../assets/setup/add-manage-measurement-data/select-measurement-data-connection.png){zoomable="yes"}

#### データソースを選択 {#select-data-source}

次に、データ接続のソースを選択します。 現時点では、Adobe Experience Platformが唯一サポートされているデータソースです。

データソースを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![Adobe Experience Platform オプションと次のオプションを強調表示するデータ接続と詳細の手順。](../../assets/setup/add-manage-measurement-data/select-measurement-data-source.png){zoomable="yes"}

#### サンドボックスを選択 {#select-sandbox}

Collaboration Campaignの測定レポートに使用する測定データが含まれているサンドボックスを選択します。 使用可能なサンドボックスのリストからサンドボックスを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![製品サンドボックスと次のオプションを強調表示するデータ接続と詳細の手順。](../../assets/setup/add-manage-measurement-data/select-sandbox.png){zoomable="yes"}

#### 測定データセットの選択 {#select-measurement-dataset}

選択したサンドボックス内のデータセットのリストが表示されます。 測定データとしてデータセットを選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。 検索オプションを使用して、目的のデータセットをフィルタリングして検索できます。

![検索オプション、例イベント データ データセット、次のオプションを強調表示するデータ接続と詳細の手順](../../assets/setup/add-manage-measurement-data/select-measurement-dataset.png){zoomable="yes"}

#### 名前と詳細を入力 {#provide-name-and-details}

次に、データ接続の名前と説明を入力します。 この情報は、後でデータ接続を特定するのに役立ちます。

![名前と説明を指定するオプションを含むデータ接続と詳細ステップ。](../../assets/setup/add-manage-measurement-data/data-connection-name-details.png){zoomable="yes"}

### マッピング {#mapping}

次のステップでは、測定データのフィールドを、Collaborationで使用される対応するターゲットフィールドにマッピングします。 また、結合キーをマッピングしてリアルタイム顧客プロファイルの属性をイベントデータセットに追加し、これらの属性を使用して測定レポートを分類することもできます。

#### イベントデータの拡充 {#enrich-event-data}

イベントデータを拡充するには、**[!UICONTROL Source フィールド結合キー]** オプションを選択します。

![Source フィールド結合キーオプションがハイライト表示されたマッピング画面。](../../assets/setup/add-manage-measurement-data/select-source-field-join-key.png){zoomable="yes"}

**[!UICONTROL Source フィールド結合キー]** ダイアログで、ソースフィールドを選択し、次に&#x200B;**[!UICONTROL 選択]**&#x200B;します。

![Source フィールドと次のオプションを強調表示するSource フィールド結合キーダイアログ。](../../assets/setup/add-manage-measurement-data/source-field-join-key-dialog.png){zoomable="yes"}

次に、**[!UICONTROL プロファイル結合キー]** オプションを選択します。 **[!UICONTROL プロファイル結合キー]** ダイアログで、リストからプロファイルフィールドを選択します。 「検索」オプションを使用して、目的のフィールドを検索できます。 次に、**[!UICONTROL 選択]**&#x200B;を選択して確認します。

![検索キー、選択したプロファイルフィールド、次のオプションを強調表示するプロファイル結合キーダイアログ。](../../assets/setup/add-manage-measurement-data/profile-join-key-dialog.png){zoomable="yes"}

#### マッピングフィールド {#mapping-fields}

測定データからCollaborationのターゲットフィールドへのソースフィールドのマッピングを開始するには、**[!UICONTROL マッピング]**&#x200B;画面で空のソースフィールドを選択します。

![空のソースフィールドがハイライト表示されたマッピング画面。](../../assets/setup/add-manage-measurement-data/mapping-screen.png){zoomable="yes"}

**[!UICONTROL ソースフィールドを選択]** ダイアログが表示され、**[!UICONTROL ID名前空間]**&#x200B;や&#x200B;**[!UICONTROL イベントスキーマ]**&#x200B;などのオプションにグループ化された、利用可能なソースフィールドのリストが表示されます。 検索オプションを使用して、リストからソースフィールドをフィルタリングして検索できます。

必要なソースフィールドを選択し、続いて&#x200B;**[!UICONTROL 選択]**&#x200B;します。

![電子メールソースフィールドと選択オプションを強調表示するソースフィールドを選択ダイアログ。](../../assets/setup/add-manage-measurement-data/select-source-field-dialog.png){zoomable="yes"}

次に、ドロップダウンメニューを使用して、選択したソースフィールドを適切なターゲットフィールドにマッピングします。 使用可能なすべてのターゲットフィールドは、共同作業者アカウント用に設定された[一致キーです](./onboard-account.md#set-up-match-keys)。

![選択したソースフィールドとマッピングするために使用可能なすべてのターゲットフィールドを表示するドロップダウンメニュー。](../../assets/setup/add-manage-measurement-data/select-target-field-dropdown.png){zoomable="yes"}

必要に応じて、マッピング行を追加または削除できます。 ハッシュ化されていないソースフィールドをハッシュ化されたターゲットフィールドにマッピングする必要がある場合（例えば、プレーンテキストメールを[!UICONTROL &#x200B; ハッシュ化されたメール &#x200B;]にマッピングする場合）、**[!UICONTROL 変換を適用]** オプションを使用して、必要なハッシュ化を適用します。

完了したら、エンリッチメントが有効になっている場合は、マッピングされたフィールドと結合キーを確認します。 次に、**[!UICONTROL 次へ]**&#x200B;を選択します。

![&#x200B; マッピングされたフィールド、結合キー（エンリッチメントが有効になっている場合）、強調表示された「次へ」オプションを表示するマッピング画面。](../../assets/setup/add-manage-measurement-data/review-mapping.png){zoomable="yes"}

### 同意を管理 {#manage-consent}

先に進む前に、Collaborationでのデータ使用がReal-Time CDP データガバナンスポリシーに準拠していることを確認する必要があります。 同意の要件や適用されるカスタム同意ポリシーに従って、あらゆるデータを事前にフィルタリングする必要があるため、追加の処理は必要ありません。

確認を確認するには、**[!UICONTROL 次へ]**&#x200B;を選択してください。

![次のオプションがハイライト表示された確認を必要とする同意管理画面。](../../assets/setup/add-manage-measurement-data/manage-consent.png){zoomable="yes"}

マッピング手順[&#128279;](#enrich-event-data)中にプロファイルのエンリッチメントを有効にする場合は、事前定義されたオプションのリストから同意ポリシーを設定できます。 これには以下が含まれます。

* **マーケティングアクション**：これらのマーケティングアクションを使用して、Experience PlatformからCollaborationに取り込むオーディエンスデータを制御します。
* **同意ルール**: Collaborationに送信するデータに適用する同意ルールを選択します。
* **オーディエンス**: オーディエンスフィルターを使用して、同意のためにオーディエンスプロファイルを含めたり除外したりします。


>[!NOTE]
>
>**[!UICONTROL Data Collaboration]**&#x200B;はC4、C5、C9のデータ使用ラベルをサポートしていますが、**[!UICONTROL Data Science]**&#x200B;はC9のみをサポートしています。 データ使用ラベルの詳細については、Experience Platformのドキュメントを参照してください。
>
>* [データ使用ラベルの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/overview){target="_blank"}
>* [用語集](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/labels/reference){target="_blank"}

必要な設定を選択し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![&#x200B; プロファイルのエンリッチメントが有効になっている場合、同意設定オプションが表示され、次のオプションがハイライト表示される同意管理画面](../../assets/setup/add-manage-measurement-data/manage-consent-configuration-options.png){zoomable="yes"}

続行する前に、**[!UICONTROL ガバナンスポリシーと実行アクション]** ダイアログで条件を確認して同意する必要があります。 チェックボックスを選択し、その後に&#x200B;**[!UICONTROL OK]**&#x200B;を選択します。

![&#x200B; チェックボックスと「OK」オプションが強調表示されたガバナンスポリシーと実行アクションのダイアログ。](../../assets/setup/add-manage-measurement-data/governance-policy-enforcement-actions-dialog.png){zoomable="yes"}

#### オーディエンスフィルター {#audience-filter}

同意のために特定のオーディエンスプロファイルを含めるか除外するには、**[!UICONTROL オーディエンスフィルター]** ドロップダウンメニューを使用します。 このフィルターを選択すると、UIが更新され、**[!UICONTROL オーディエンスを参照]** オプションが表示されます。 「**[!UICONTROL オーディエンスを参照]**」を選択します。

![同意管理画面に、オーディエンスフィルターを選択した後の「オーディエンスを参照」オプションが表示されている。](../../assets/setup/add-manage-measurement-data/browse-audiences.png){zoomable="yes"}

「**[!UICONTROL オーディエンスを選択]**」ダイアログが表示されます。 リストからオーディエンスを選択し、次に&#x200B;**[!UICONTROL 選択]**&#x200B;します。

![選択したオーディエンスと選択オプションを強調表示するオーディエンスの選択ダイアログ。](../../assets/setup/add-manage-measurement-data/select-audiences-dialog.png){zoomable="yes"}

選択したオーディエンスが表示され、必要に応じて削除するオプションが表示されます。 同意設定を確認し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![同意用に選択したオーディエンスと「次へ」オプションがハイライト表示された同意管理画面。](../../assets/setup/add-manage-measurement-data/audience-for-consent.png){zoomable="yes"}

### コンバージョンイベントを追加 {#add-conversion-event}

続いて、サイト訪問、登録、購入完了など、キャンペーンが与える影響を測定するためのコンバージョンイベントを定義します。 測定には、最大&#x200B;**3**&#x200B;個の個別のコンバージョンイベントを指定できます。

コンバージョンイベントの名前を入力し、ドロップダウンメニューを使用してコンバージョンタイプを選択します。

![&#x200B; コンバージョンタイプのドロップダウンメニューが表示されたコンバージョンイベントの追加画面が展開されました。](../../assets/setup/add-manage-measurement-data/conversion-type-dropdown.png){zoomable="yes"}

この時点で値を割り当てたくない場合は、コンバージョンの値を入力するか、空のままにすることができます。

![&#x200B; コンバージョン値オプションを強調表示するコンバージョンイベントの追加画面。](../../assets/setup/add-manage-measurement-data/conversion-value.png){zoomable="yes"}

次に、イベントデータセット内のどの行が同じ基になるコンバージョンイベントに属しているかを示すために、複製キーを指定する必要があります（例えば、サインアッププロセス中に同じタイムスタンプ）。 これにより、測定レポートで同じコンバージョンを複数回カウントするのを防ぐことができます。 これを行うには、**[!UICONTROL 複製キー]**&#x200B;を選択します。 **[!UICONTROL 複製キー]** ダイアログで、キーを検索して選択し、続いて&#x200B;**[!UICONTROL 選択]**&#x200B;します。

![選択したキーと選択オプションを表示する複製キーダイアログ。](../../assets/setup/add-manage-measurement-data/duplication-key-dialog.png){zoomable="yes"}

複製キーを指定した後、変換用のイベントデータセットの関連行のみを含めるように、最大&#x200B;**5**&#x200B;件の条件を追加できます。 これらの条件の全部または一部を適用することを選択します。

「**[!UICONTROL 条件を追加]**」を選択し、条件オプションを選択します。

![条件を追加オプションを選択した後、条件オプションを強調表示するコンバージョンイベントの追加画面。](../../assets/setup/add-manage-measurement-data/add-condition.png){zoomable="yes"}

**[!UICONTROL ソースフィールドを選択]** ダイアログで、条件ルールのソースフィールドを検索して選択し、次に&#x200B;**[!UICONTROL Select]**&#x200B;を選択します。

![&#x200B; イベントタイプフィールドと選択オプションを強調表示するソースフィールドを選択ダイアログ。](../../assets/setup/add-manage-measurement-data/select-condition-field.png){zoomable="yes"}

ドロップダウンメニューを使用してロジック演算子を選択し、設定ルールの値を入力します。

![&#x200B; ロジック演算子のドロップダウンと「値」オプションを強調表示するコンバージョンイベントの追加画面。](../../assets/setup/add-manage-measurement-data/logic-operator-dropdown.png){zoomable="yes"}

別のコンバージョンイベントを追加するには、**[!UICONTROL コンバージョンを追加]**&#x200B;を選択します。 合計&#x200B;**3**&#x200B;個のコンバージョンイベントを含めることができます。 完了したら、コンバージョン設定を確認し、**[!UICONTROL 次へ]**&#x200B;を選択します。

![&#x200B; コンバージョンイベント設定と「次へ」オプションがハイライト表示されたコンバージョンイベント追加画面。](../../assets/setup/add-manage-measurement-data/add-conversion-event.png){zoomable="yes"}

### レビュー {#review}

**[!UICONTROL レビュー]**&#x200B;画面が表示され、測定データ設定の概要が表示されます。 すべての情報が正しいことを確認します。 セクションを変更する必要がある場合は、**[!UICONTROL 編集]** オプションを使用します。

最後に、**[!UICONTROL 完了]**&#x200B;を選択して、測定データの追加を完了します。

![測定データ設定の概要と「完了」オプションがハイライト表示されたレビュー画面。](../../assets/setup/add-manage-measurement-data/review-measurement-data.png){zoomable="yes"}

確認ダイアログは、測定データが正常に作成されたことを確認します。 測定データから設定された新しいコンバージョンイベントは、**[!UICONTROL My measurement data]** ワークスペースで確認できます。

![測定データから設定されたコンバージョンイベントのリストを表示している測定データワークスペース。](../../assets/setup/add-manage-measurement-data/conversion-event-list.png){zoomable="yes"}

グリッドビューまたはテーブルビューで、行アイテムまたはイベントカード内の&#x200B;**[!UICONTROL コンバージョンを表示]** オプションを選択すると、特定のコンバージョンイベントの概要が表示されます。 イベントのステータス、ソース、データ接続名が表示され、次の詳細パネルが表示されます。

* **[!UICONTROL コンバージョンの詳細]**：コンバージョンに関する重要な情報を表示します。その情報には、種類、一意のイベントの識別に使用される複製キー、割り当てられたコンバージョン値（指定されている場合）が含まれます。
* **[!UICONTROL 条件]**：このコンバージョンイベントに適用された条件ルールを表示します。

![&#x200B; コンバージョンイベントの詳細を表示する概要画面。](../../assets/setup/add-manage-measurement-data/conversion-event-overview.png){zoomable="yes"}

## 次の手順 {#next-steps}

Collaborationでの測定データのソーシングが完了しました。 広告主は、アトリビューションレポートを作成して、キャンペーンがどのようにコンバージョンを促進しているかを調査し、全体的な影響を測定できるようになりました。 パブリッシャーの場合は、キャンペーンのアトリビューションレポートを共同作業者に生成するように依頼します。 詳細な手順については、[&#x200B; アトリビューションレポートの作成](../collaborate/measure.md#create-attribution-report) ガイドを参照してください。
