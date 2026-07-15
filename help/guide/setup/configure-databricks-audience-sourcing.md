---
title: オーディエンスソーシング用に [!DNL Databricks Delta Share] を設定
description: Real-Time CDP Collaborationでオーディエンス ソーシング用に [!DNL Databricks Delta Share] を設定および接続する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 876b7d2996d3027f81159252f714c2305d6d23b4
workflow-type: tm+mt
source-wordcount: '2816'
ht-degree: 1%

---


# オーディエンスソーシング用に[!DNL Databricks Delta Share]を設定

このガイドでは、ユーザーインターフェイスを使用して[!DNL Databricks Delta Share]をAdobe Real-Time CDP Collaborationに接続し、ファーストパーティオーディエンスを調達する方法を説明します。

[!DNL Databricks Delta Share]を接続すると、CollaborationはUnity カタログ共有からオーディエンスデータを直接読み取ります。 ソーシング完了後は、コラボレーションプロジェクトでオーディエンスをアクティベーションおよび重複分析に使用できます。

このガイドでは、前提条件の準備方法、[!DNL Delta Share]の接続方法、ソーステーブルの指定方法、ID フィールドのマッピング方法、オーディエンスのソーシングが正常に開始されたことを確認する方法について説明します。

[!DNL Databricks]から取得したオーディエンスは、Adobe Experience Platformやその他のサポートされているクラウドソースから取得したオーディエンスと同じガバナンスとデータ処理ルールに従います。

その他の利用可能なソーシング方法には、[Experience Platform](./onboard-audiences.md)、[Amazon S3](./configure-aws-s3-audience-sourcing.md)、[Google Cloud Storage](./configure-gcs-audience-sourcing.md)、[Snowflake](./configure-snowflake-audience-sourcing.md)、[Azure storage](./configure-azure-storage-audience-sourcing.md)、および[CSV ファイルのアップロード ](./upload-csv-audience-sourcing.md)があります。 Collaborationで使用可能なすべてのソースについて詳しくは、[ ソースの概要](./source-overview.md)を参照してください。

## 前提条件 {#prerequisites}

設定ワークフローを開始する前に、このセクションの前提条件を完了してください。 前提条件が見つからない場合は、設定が失敗したり、オーディエンスがソーシング後に表示されなかったりする一般的な理由です。 このガイドに従う前に、[ アカウントのオンボーディングと設定](./onboard-account.md)を完了してください。

このガイドの一部のタスクでは、[!DNL Databricks]管理者の支援が必要です。 組織の[!DNL Databricks]を管理しない場合は、開始する前に適切な管理者と協力してください。

### [!DNL Databricks Delta Share] アクセス {#databricks-delta-share-access}

続行する前に、次の点を[!DNL Databricks]管理者に確認してください。

* お客様の組織は、ネイティブ DatabricksからDatabricksへの共有（Unity Catalog）を使用して、Adobeの[!DNL Databricks] アカウントに[!DNL Delta Share]を公開しました。 Collaborationでは、このワークフローのUIでのベアラートークンまたはOIDC資格情報の入力はサポートされていません。
* AdobeのUnity カタログメタストアに登録されているプロバイダー名、共有名、オーディエンステーブルを含むスキーマを理解しています。
* Collaboration アカウントとリージョンに対して、[!DNL Databricks Delta Share]件のオーディエンスのソーシングを利用できます。 お住まいの地域でDatabricksのソーシングがまだ利用できない場合は、Adobeのアカウント担当者にお問い合わせください。

共有をAdobeに公開する手順については、このガイドの「[Delta ShareをAdobeに公開する](#publish-delta-share)」セクションを参照してください。

### オーディエンスデータの準備 {#prepare-audience-data}

オーディエンステーブルを構成して、Collaborationがオーディエンスを発見し、IDを正しくマッピングできるようにします。

* **メンバーシップテーブル （必須）:** プロファイルとオーディエンスのペアごとに1行を含む、共有スキーマ内のテーブル。 このテーブルには、`AUDIENCE_ID`にマッピング可能な列と、少なくとも1つのサポートされている一致キー列が含まれている必要があります。 Collaborationでは、このテーブルをソースデータのプレビューとフィールドマッピングに使用します。
* **メタデータテーブル （オプション）:** オーディエンスのカタログを個別に管理する場合（オーディエンス ID、名前、カウント、または類似のメタデータを持つオーディエンスごとに1行）、このテーブルを指定すると、Collaborationがメンバーシップテーブルのみから異なるオーディエンス IDを推測するのではなく、オーディエンス定義を読み取ることができます。
* **サポートされている照合キー：** `HASHED_EMAIL_SHA_256`、`HASHED_PHONE_SHA_256`、`HASHED_IPV4_SHA_256`、`CRM_ID`、`LOYALTY_ID`、`ADFIXUS_ID`およびその他の照合キーが、お使いのCollaboration アカウントに対して有効になっています。
* **ハッシュ化要件：**&#x200B;一致するキー値はすべて、[!DNL Databricks]に保存する前に、トリミング、小文字、およびSHA256 ハッシュ化する必要があります。 Collaborationでは、取り込み前にデータをハッシュ化または正規化しません。
* **列の一貫性：** メンバーシップテーブルは、Collaborationが有効な一致キーにマッピングできる安定した列名を公開する必要があります。

メンバーシップテーブルに存在するすべての照合キーも、Collaboration アカウントに対して有効にする必要があります。 一致キーを追加または有効にするには、[一致キーの設定](./onboard-account.md#set-up-match-keys)を参照してください。

### 開始する前に必要な値 {#required-values}

設定ウィザードを開始する前に、次の値を準備しておく必要があります。


| 値 | 説明 |
| ----- | ----------- |
| プロバイダー名 | AdobeがUnity Catalogで[!DNL Delta Share]にアクセスするために使用するプロバイダーID。 [!DNL Databricks]管理者またはAdobe オンボーディング担当者がこの値を提供できます。 この値は、[!DNL Databricks] ワークスペース URLと同じではありません。 |
| 共有名 | Adobeに公開された[!DNL Delta Share]の名前。 |
| スキーマ | オーディエンステーブルを含む共有内のスキーマ。 |
| メンバーシップテーブル | オーディエンスメンバーシップ行（オーディエンスのプロファイルごとに1行）を保持するスキーマ内のテーブル名。 |
| メタデータテーブル （オプション） | メタデータ駆動型オーディエンスカタログを使用する場合、オーディエンスをリストするスキーマ内のテーブル名（オーディエンスごとに1行）。 |

{style="table-layout:auto"}

## [!DNL Databricks]接続の設定 {#configure-databricks-connection}

設定ワークフローは、**[!UICONTROL セットアップ]** ワークスペース内のマルチステップ ウィザードです。 各ステップを順番に進めていきます。

### 新しいデータ接続を追加 {#add-data-connection}

**[!UICONTROL セットアップ]** ワークスペース内の&#x200B;**[!UICONTROL マイオーディエンス]** タブから、追加アイコン（![追加アイコン ](/help/assets/icons/plus.png)）を選択します。 **[!UICONTROL Audience]**&#x200B;を選択します。

これが初めてのオーディエンスの場合は、**[!UICONTROL 追加]** オプションを選択することもできます。

![追加アイコンと「オーディエンスを追加」オプションが表示された設定ワークスペースの「マイオーディエンス」タブ。](../../assets/setup/add-manage-audiences/add-audiences.png)

オーディエンスを追加ワークフローが表示されます。 「**[!UICONTROL 新しいデータ接続を追加]**」を選択し、「**[!UICONTROL 次へ]**」を選択します。

![新しいデータ接続を追加オプションがハイライト表示されたオーディエンスを追加ワークスペース。](../../assets/setup/add-manage-audiences/add-data-connection.png){zoomable="yes"}

### データソースとして [!DNL Databricks Delta Share] を選択 {#select-databricks-delta-share}

データソース選択画面には、使用可能なすべての接続タイプが一覧表示されます。 「**[!UICONTROL Databricks Delta Share]**」を選択し、「**[!UICONTROL 次へ]**」を選択します。

![Databricks Delta Shareが選択され、次にハイライト表示されたデータソース選択画面を表示するオーディエンスの追加ワークフロー。](../../assets/setup/databricks-audience-sourcing/databricks-data-source-selection.png)

### [!DNL Delta Share]を接続 {#connect-delta-share}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_sharing_databricks"
>title="Experience League"
>abstract="オーディエンスソーシング用に共有を設定する手順については、[!DNL Databricks Delta Share] ソーシングガイドを参照してください"

Collaborationによる[!DNL Delta Share]へのアクセスを許可するために必要な詳細を入力してください。 プロバイダー、共有、スキーマ、テーブルの詳細を[!DNL Databricks Delta Share]から入力します。 必要なメンバーシップテーブルは、共有スキーマで使用できる必要があります。 メタデータテーブルを使用する場合は、同じ共有スキーマでも使用できる必要があります。
必要な情報を入力したら、**[!UICONTROL Connect]**&#x200B;を選択します。

Collaborationは、共有を検証し、Adobeのワークスペースにマウントします。 この手順は最大1分かかる場合があります。 接続が確立されると、進行状況インジケーターが表示されます。

| フィールド | 説明 |
| --- | --- |
| **[!UICONTROL プロバイダー名]** | Adobeが共有を利用するために使用するUnity カタログプロバイダー名。 開始する前に必要な[値](#required-values)を参照してください。 |
| **[!UICONTROL 共有名]** | Adobeに公開された[!DNL Delta Share]の名前。 |
| **[!UICONTROL スキーマ]** | オーディエンステーブルを含む共有内のスキーマ。 |
| **[!UICONTROL データテーブル]** | オーディエンスメンバーシップ行（オーディエンスのプロファイルごとに1行）を保持するスキーマ内のテーブル名。 |
| **[!UICONTROL メタデータテーブル]** | オーディエンスを一覧表示するテーブル（オーディエンスごとに1行）。 |


![Databricks connect-share フォームに、プロバイダー名、共有名、スキーマ、データテーブル、メタデータテーブルのフィールドおよび使用可能な「次へ」ボタンが表示されているオーディエンスを追加ワークフロー。](../../assets/setup/databricks-audience-sourcing/databricks-connect-share-successful.png)

共有が見つからないか、スキーマがまだ表示されていない場合は、エラーメッセージが表示されます。 [!DNL Databricks]管理者で値を確認して、もう一度試してください。

### 同意とデータ使用の確認 {#confirm-consent}

続ける前に、Collaborationに送信するオーディエンスデータに法律で必要なオプトアウトを適用していることを確認してください。 データがこの要件を満たしているかどうかわからない場合は、続行する前に、[ ガバナンスポリシーと施行アクション ](./onboard-audiences.md#governance-policy-and-enforcement-actions) ガイドを確認してください。 確認チェックボックスを選択し、**[!UICONTROL OK]**&#x200B;を選択して続行します。

![続行する前に確認が必要な同意オプトアウト確認ダイアログ。](../../assets/setup/aws-audience-sourcing/consent-optout-acknowledgment.png)

### 接続の詳細を提供 {#provide-connection-details}

このデータ接続の名前とオプションの説明を入力します。 指定した名前は、**[!UICONTROL My data connections]** タブに表示され、複数のデータ接続を管理する場合にこのソースを区別するのに役立ちます。

* **[!UICONTROL データ接続名]** （必須）
* **[!UICONTROL データ接続の説明]** （オプション）

「**[!UICONTROL 次へ]**」をクリックして続行します。

![ データ接続名とデータ接続の説明のフィールドを表示する「詳細を提供」ステップにオーディエンスワークフローを追加し、右上隅に「次へ」が表示されます。](../../assets/setup/databricks-audience-sourcing/databricks-connection-details.png)

### ID フィールドのマッピング {#map-identity-fields}

**[!UICONTROL マッピング]**&#x200B;画面には、Collaborationがメンバーシップテーブルのソース列をターゲット ID フィールドにマッピングする方法が表示されます。 Collaborationでは、列の名前とアカウントで有効になっている照合キーに基づいて、フィールドが自動的にマッピングされます。

>[!TIP]
>
>「**[!UICONTROL ソースデータをプレビュー]**」を選択してメンバーシップテーブルのサンプルを表形式で確認し、「**[!UICONTROL 閉じる]**」を選択してマッピング画面に戻ります。

![AUDIENCE_IDおよびHASHED_EMAIL_SHA_256などの列と、右下隅の「閉じる」ボタンを含むオーディエンスデータのサンプルテーブルを表示する「Databricks データプレビュー」ダイアログ。](../../assets/setup/databricks-audience-sourcing/databricks-source-data-preview.png)

表示されるマッピングが、メンバーシップテーブルの列を反映していることを確認します。 「**[!UICONTROL 次へ]**」をクリックして続行します。

![ ターゲット ID フィールドにマッピングされたソースフィールドを表示する「フィールドをマップ」ステップにオーディエンスワークフローを追加し、「ソースデータをプレビュー」オプションを表示して、右上隅に「次へ」ボタンを表示します。](../../assets/setup/databricks-audience-sourcing/databricks-field-mapping.png)

### スケジュール更新頻度と日付範囲 {#schedule-refresh}

**[!UICONTROL スケジュール]** ビューが表示されます。 ドロップダウンメニューを使用して、1日から6日の間の更新頻度を選択し、アクティブな日付範囲を設定します。 カレンダーアイコンを使用して、開始日と終了日を指定します。

>[!IMPORTANT]
>
>Collaboration クレジットを効果的に管理するには、更新の頻度を、基礎となるデータ更新の更新頻度と一致するか、それを超えるように設定します。

![更新頻度オプションと日付範囲の設定を含むスケジュール設定画面。](../../assets/setup/databricks-audience-sourcing/databricks-schedule-refresh-frequency.png)

### 接続を確認して完了 {#review-and-complete}

接続を作成する前に、設定の概要を確認します。 概要画面には、次のセクションが表示されます。

* **[!UICONTROL データ接続]**：設定した接続名、プロバイダー名、共有名、スキーマ。
* **[!UICONTROL マッピング]**: ソース ID フィールドとターゲット ID フィールドのマッピング。
* **[!UICONTROL スケジュール]**：更新頻度とアクティブな日付範囲。

![設定された値を持つ共有接続、詳細、およびマッピング セクションの概要と、右上隅に表示される「完了」ボタンを表示する「レビュー」ステップでオーディエンスワークフローを追加します。](../../assets/setup/databricks-audience-sourcing/databricks-review.png)

すべてのセクションが正しいことを確認し、**[!UICONTROL 完了]**&#x200B;を選択します。

確認ダイアログが表示され、Collaborationがデータ接続を作成し、オーディエンスのソーシングが進行中であることを示します。

## ソース別オーディエンスの確認 {#review-sourced-audiences}

コンフィギュレーションウィザードが完了すると、Collaborationは[!DNL Databricks] テーブルからオーディエンスのソーシングを非同期で開始します。 **[!UICONTROL セットアップ ] / [!UICONTROL  マイオーディエンス]**&#x200B;に移動して、進行状況を監視します。 必要な時間は、データのサイズによって異なります。

### オーディエンスのソーシングの進捗状況の監視 {#monitor-sourcing-progress}

Collaborationがオーディエンスデータを取得している間、**[!UICONTROL My audiences]** ワークスペースの上部にあるバナーは、ソーシングが進行中であることを示します。 個々のオーディエンスは、各オーディエンスのソーシング完了後にのみリストに表示されます。

「My audiences」タブの![ ワークスペースを設定すると、「Audience sourcing in progress」バナーが表示され、オーディエンスがDatabricks データ接続からソースされていることを示します。オーディエンスのリストは以下に表示されます。](../../assets/setup/databricks-audience-sourcing/databricks-audience-sourcing-in-progress-banner.png)

>[!TIP]
>
>オーディエンスのソーシング時間は、メンバーシップテーブルのサイズと、オーディエンスの発見にメタデータテーブルを使用するかどうかによって異なります。 大きなデータセットが&#x200B;**[!UICONTROL マイオーディエンス]** ワークスペースに表示されるまでに時間がかかる場合があります。

### ソースされたオーディエンスの詳細の表示 {#view-audience-details}

ソーシングが完了すると、[!DNL Databricks]個のオーディエンスが、他の接続からソーシングされたオーディエンスと共に&#x200B;**[!UICONTROL 個のマイオーディエンス]** タブに表示されます。 特定のオーディエンスの詳細ビューを開くには、行項目を選択するか、**[!UICONTROL オーディエンスを表示]**&#x200B;します。

![設定ワークスペースの「マイオーディエンス」タブに、Databricks Delta Shareから取得したものなど、選択可能なチェックボックスと行アクションが使用可能なオーディエンスのテーブルが表示されている。](../../assets/setup/databricks-audience-sourcing/databricks-my-audiences-row-actions.png)

詳細ビューには、オーディエンスのステータス、ソースおよびデータ接続名が、次のパネルとともに表示されます。

* **[!UICONTROL ID]**: データが利用可能になると、オーディエンスのID数と内訳の合計が表示されます。
* **[!UICONTROL カテゴリ]**: オーディエンスの整理またはフィルタリングに適用されたタグ。
* **[!UICONTROL 接続アクセス]**: オーディエンスがプライベート、パブリック、または特定の共同作業者と共有されているかどうか。
* **[!UICONTROL メタデータの可視化]**：共同作業者が表示できるID数、重複率、インデックスなどのオーディエンス情報。

![個々のオーディエンスの詳細ビューで、ステータス：アクティブ、ソースシステム、データ接続名が上部に表示され、以下の4つのパネルが表示されます。ID、カテゴリ、接続アクセス、メタデータの表示。](../../assets/setup/databricks-audience-sourcing/databricks-audience-detail-view.png)

コラボレーションプロジェクトでオーディエンスを使用する前に、これらの設定を確認してください。 カテゴリ、接続アクセス、またはメタデータの表示を更新するには、[個々のオーディエンスの表示と管理](./onboard-audiences.md#view-individual-audiences)を参照してください。

### オーディエンス設定の編集 {#edit-audience-settings}

詳細ビューを開かずに、**[!UICONTROL 自分のオーディエンス]**&#x200B;のリストビューからオーディエンスメタデータを直接編集できます。 オーディエンスのチェックボックスを選択してアクションツールバーを表示し、アクションを選択します。**[!UICONTROL メタデータ表示を編集]**、**[!UICONTROL 接続アクセスを編集]**、**[!UICONTROL 名前と説明を編集]**、**[!UICONTROL カテゴリを編集]**、または&#x200B;**[!UICONTROL 削除]**。

![別のシステムから取得したオーディエンスが表示され、1行がチェックボックスを使用して選択されたマイオーディエンスリストビューには、編集および削除オプションを備えた下部のツールバーが表示されます。](../../assets/setup/databricks-audience-sourcing/databricks-edit-audience-settings.png)

### [!DNL Databricks] データ接続の表示 {#view-databricks-connection}

一致キーを含む接続自体を確認するには、**[!UICONTROL 設定]** > **[!UICONTROL データ接続]**&#x200B;に移動します。 新しい[!DNL Databricks]接続がそこで使用できます。 オーディエンスソースは&#x200B;**[!UICONTROL Databricks Delta Share]**&#x200B;として表示されます。

![ ソーシングステータス情報を含む[!DNL Databricks Delta Share] データ接続を示す「My data connections」タブ。](../../assets/setup/databricks-audience-sourcing/databricks-my-data-connections-tab.png)

## 既知の制限事項 {#known-limitations}

[!DNL Databricks Delta Share] オーディエンスソーシングを設定して使用する場合は、次の制約に注意してください。

* **ネイティブ共有のみ：** UIでは、ネイティブ DatabricksからDatabricksへの[!DNL Delta Sharing]のみがサポートされます。 Bearer-tokenおよびOIDC認証フローは、設定ウィザードでは使用できません。
* **ウィザードテーブルブラウザーがありません：** テーブル名を手動で入力する必要があります。 Collaborationでは、テーブルをプレビューする際にテーブル名が検証されます。共有されているすべてのテーブルが自動的に一覧表示されるわけではありません。
* **メタデータテーブルの行制限：** オーディエンスの検出にメタデータテーブルを使用すると、Collaborationはそのテーブルから最大100,000個のオーディエンス行をインポートします。 カタログがこの制限を超える場合は、Adobe サポートにお問い合わせください。
* **一致キーの制約：** データ接続で一致キーが有効になると、削除できません。 既存の接続に一致するキーを追加することはできますが、無効にしたり削除したりすることはできません。 アクティブな一致キーを変更するには、[ データ接続](./manage-data-connection.md#delete-data-connection)を削除して新しい接続を作成する必要があります。
* **メンバーシップテーブルが必要：** オーディエンスの検出にメタデータテーブルを使用する場合でも、メンバーシップテーブルを指定する必要があります。 Collaborationは、取り込み中にメンバーシップテーブルからID行を読み取ります。

## トラブルシューティング {#troubleshooting}

この節では、設定中または設定後に発生する問題を解決する場合に使用します。 共有接続中にエラーが発生した場合は、プロバイダー名、共有名、スキーマを[!DNL Databricks]管理者と確認してください。

**共有接続が失敗するか、タイムアウトします**

* [!DNL Delta Share]がAdobeの[!DNL Databricks] アカウントに公開され、プロバイダー名、共有名、スキーマが正しいことを確認します。
* 共有にスキーマが表示されていることを確認します。 新たに公開された共有は、反映に時間がかかる場合があります。
* 数分後に接続が失敗する場合は、設定を再起動して再試行するか、Adobe カスタマーサポートに連絡して、プロバイダー名、共有名、スキーマ、および関連するエラーの詳細を指定します。 機密情報は含めないでください。

**テーブルのプレビューに失敗しました**

* テーブル名が正しくスペルされ、指定したスキーマに存在することを確認します。
* テーブルがAdobeに公開された[!DNL Delta Share]に含まれていることを確認します。
* メタデータ駆動型の検出の場合は、続行する前に、メンバーシップテーブルとメタデータテーブルの両方をプレビューします。

**フィールドマッピング検証ブロックの進行状況**

* メンバーシップ テーブルに&#x200B;**`AUDIENCE_ID`**&#x200B;にマッピング可能な列が含まれていることを確認してください。
* 少なくとも2つのID フィールド（ソースとターゲット）が完全にマッピングされていることを確認します。
* **[!UICONTROL ソースデータのプレビュー]**&#x200B;を使用して、有効な照合キーに一致する列名を確認します。

**オーディエンスが表示されていないか、ソーシングに予想以上の時間がかかっています**

* データ量に合わせてソーシング時間を拡大： 大規模なメンバーシップテーブルの処理時間が延長されています。
* オーディエンスが24時間以内に表示されない場合は、**[!UICONTROL データ接続]** タブで、接続のエラーインジケーターを確認してください。
* メンバーシップ テーブルの構造とフィールド マッピングが、[ オーディエンス データの準備](#prepare-audience-data)の要件に一致することを確認します。
* 問題が解決しない場合は、Adobe カスタマーサポートにお問い合わせいただき、データ接続名とテーブルの詳細を入力してください。

**最初に成功した後、データ接続に失敗したステータスが表示される**

* 接続を作成してから、[!DNL Delta Share]とテーブルが[!DNL Databricks]で削除または名前が変更されていないことを確認してください。
* Adobeの共有へのアクセス権が取り消されていないことを確認します。
* 問題が解決しない場合は、Adobe カスタマーサポートにお問い合わせください。

## [!DNL Delta Share]をAdobeに公開 {#publish-delta-share}

[!DNL Databricks] Unity カタログ [!DNL Delta Sharing]を使用すると、データをコピーすることなく、他の[!DNL Databricks] アカウントと安全にテーブルを共有できます。 Collaborationがオーディエンスデータを読み取れるようにするには、[!DNL Databricks]管理者が[!DNL Delta Share]をAdobeの[!DNL Databricks]のコンシューマーアカウントに公開する必要があります。

### 公開前に {#before-you-publish}

Adobeの担当者またはオンボーディング担当者に問い合わせると、次の情報を入手できます。

* Adobeがお客様の地域でシェアを受け取る準備ができていることを確認します。
* プロバイダー名Adobeは、Unity Catalogのメタストアで組織を共有プロバイダーとして識別するために使用します。

[!DNL Databricks] ワークスペースで次の準備を行います。

* Collaborationのスキーマとテーブルを含む[!DNL Delta Share]が読み取られます。
* プロファイルとオーディエンスのペアごとに1行、および&#x200B;**`AUDIENCE_ID`**&#x200B;と照合キーの列を含むメンバーシップテーブル。
* メタデータ駆動型オーディエンス検出を使用する場合は、オプションのメタデータテーブル。

### 共有を公開 {#publish}

組織の[!DNL Databricks Delta Sharing]手順に従って、Adobeのコンシューマーアカウントに共有へのアクセス権を付与します。 正確な手順は、[!DNL Databricks]のデプロイメントとガバナンス モデルによって異なります。 一般：

1. Unity Catalogで、オーディエンススキーマとテーブルを含む共有を作成または特定します。
2. 共有にスキーマ（または個々のテーブル）を追加します。
3. ネイティブのDatabricks間の共有を使用して、Adobeの[!DNL Databricks] コンシューマーアカウントに共有を付与します。
4. Adobeの連絡先に確認し、共有がコンシューマサイドに表示されていることを確認し、Collaboration設定ウィザードのプロバイダー名と共有名をメモします。
5. [!DNL Delta Sharing]の[!DNL Databricks]製品ドキュメントについては、[Databricks Delta Sharing ドキュメント ](https://docs.databricks.com/aws/en/delta-sharing)を参照してください。

### Collaborationの[!DNL Databricks]の詳細を収集 {#collect-databricks-details}

共有を公開したら、Collaboration設定ワークフローで使用可能なプロバイダー名、共有名、スキーマおよびテーブル名があることを確認します。

Collaboration Configuration Wizardを起動する前に、以下の詳細を収集します。

| フィールド | 説明 | 例 |
| ------| ----------- | ------- |
| プロバイダー名 | AdobeのUnity カタログメタストアのプロバイダー識別子（Adobe オンボーディングから） | `your_org_provider` |
| 共有名 | 公開済み[!DNL Delta Share]の名前 | `audience_share_prod` |
| スキーマ | スキーマ | `collaboration_audiences` |
| メンバーシップテーブル | profile-audience メンバーシップ行を含むテーブル | `audience_members` |
| メタデータテーブル （オプション） | オーディエンスを一覧表示する表（オーディエンスごとに1行） | `audience_catalog` |

{style="table-layout:auto"}

## 次の手順 {#next-steps}

[!DNL Databricks Delta Share]をCollaborationのデータソースとして設定しました。 ソーシングが完了すると、オーディエンスは&#x200B;**[!UICONTROL マイオーディエンス]** ワークスペースで使用できるようになり、コラボレーションプロジェクトで使用できるようになります。

ここから、次の操作を実行できます。

* [コラボレーションプロジェクトの作成と管理](../collaborate/manage-projects.md)
* [プロジェクト内でオーディエンスを活用](../collaborate/activate.md)
* [重複を確認し、パフォーマンスを測定する](../collaborate/measure.md)
* [オーディエンス設定と可視性の管理](./onboard-audiences.md#view-individual-audiences)
* [データ接続の表示と管理](./manage-data-connection.md)

その他のオーディエンスのソーシング方法については、次を参照してください。

* [オーディエンスのソーシング用に [!DNL Google Cloud Storage] を設定](./configure-gcs-audience-sourcing.md)
* [オーディエンスのソーシング用に [!DNL Amazon S3] を設定](./configure-aws-s3-audience-sourcing.md)
* [オーディエンスのソーシング用に [!DNL Snowflake] を設定](./configure-snowflake-audience-sourcing.md)
* [Experience PlatformのSource オーディエンス](./onboard-audiences.md)
* [オーディエンスのソーシング用にCSV ファイルをアップロード](./upload-csv-audience-sourcing.md)
