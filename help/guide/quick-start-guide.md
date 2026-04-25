---
title: Real-Time CDP Collaboration クイックスタート&セットアップガイド
description: Real-Time CDP Collaboration のセットアップ、役割とアカウントの設定、オーディエンスの取り込み、データのアクティブ化、パートナーとの安全な接続の方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
TQID: https://experienceleague.adobe.com/rhIArZZm0Thkj3E-qiHtVHO6qxpr1vd-Qs4hWt4tf1U
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1417
ht-degree: 2%

---

# Real-Time CDP Collaborationのクイックスタートガイド

{{limited-availability-release-note}}

Real-Time CDP Collaborationの利用を開始するには、組織の設定、オーディエンスのソーシング、プライバシーを重視したアクティベーションと測定の実現が必要です。

## 前提条件

始める前に、次の項目を確認してください。

- アクティブなReal-Time CDP Collaborationライセンス。
- [&#x200B; システム管理者または製品管理者がAdobe Experience Platform](./permissions/overview.md)にアクセスできます。
- [&#x200B; エンドユーザー用にプロビジョニングされたアクセス &#x200B;](./permissions/manage-user-access.md)。
- 組織用に作成され、ユーザーに割り当てられた[役割](./permissions/manage-roles.md)。
- 組織名、ロゴ、バナーなどのブランドアセットにアクセスできます。
- [定義された一致キー戦略](./setup/onboard-account.md#set-up-match-keys)
- （オプション）Experience Platformをオーディエンス管理に使用していない場合は、サポートされているクラウドソース（Amazon S3、Google Cloud Storage、またはSnowflake）へのアクセス権を取得します。

## 手順1：ロールベースの設定の完了 {#complete-role-based-setup}

組織のアクセスロールによって、Collaborationでユーザーが表示および実行できる内容が決まります。 続行する前に、プラットフォームでの適切なアクセスと表示を確保するために、ロールベースの権限が正しく設定されていることを確認してください。

**リソース：**

- [ユーザーアクセスのドキュメント](./permissions/manage-user-access.md)
- [役割の設定ドキュメント](./permissions/manage-roles.md)


Admin ConsoleとExperience Platformを使用して、Collaborationに製品のアクセス権と権限を割り当てる方法について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/3452216/?learn=on&enablevpops)

## 手順2:Collaboration アカウントの設定 {#set-up-your-account}

オーディエンスを取得する前に、Collaborationでアカウントを設定する必要があります。 これにより、インターフェイスでの表示とアクセス権が決まります。

必要なアクセス権がない場合は、手順1に戻るか、組織の管理者に問い合わせてこの設定を完了してください。

Collaborationでのアカウントの役割を定義し、ブランディングアセットを提供し、照合キーを設定して、顧客接点をまたいでオーディエンスを連携します。

>[!NOTE]
>
>設定中に、1つ以上のアカウント（広告主やパブリッシャーなど）を作成できます。 ブランディングアセットや連絡先メールなどの特定のフィールドは、**[!UICONTROL 設定]** ワークスペースで後で更新できます。

- **役割を割り当てる** - アカウントが広告主であるか発行者であるかを判断します。 Collaborationでどの機能を利用するかを決めるのは自身の役割です。 役割が共同作業ワークフローにどのような影響を与えるかについて詳しくは、[役割](./overview/roles.md) ガイドを参照してください。
- **ブランディングアセット** – 以下をアカウントに追加します。
   - アカウント名（最大100文字）
   - 説明（最大1,000文字）
   - ロゴ （SVG &lt;20 KB、理想的には正方形）

>[!NOTE]
>
>パブリッシャーアカウントを作成しており、Collaborationの接続カタログに公開したい場合は、Adobe アカウント担当者にお問い合わせください。 パブリッシャーアカウントには、カスタムブランドバナー（JPG 2688x1536）が必要です。このファイルは、担当者と直接共有できます。

- **メールに連絡** – 接続が確立された後に共同作業者が使用するビジネス メールを提供します。
- **照合キーの設定** - オーディエンスの照合に使用する識別子を選択します。

役割の定義、ブランディングアセットのアップロード、照合キーの設定方法など、初期アカウント設定について詳しくは、[初期アカウント設定](./setup/onboard-account.md#initial-account-setup){target="_blank"} ガイドを参照してください。

アカウントの作成、ブランディング、照合キーの設定など、広告主を設定する手順を動画でご確認ください。

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## 手順3:Source オーディエンス（Experience Platformまたはクラウドソースから） {#source-audiences}

アカウントを作成し、ブランディングキーとマッチキーを設定したら、オーディエンスの調達を開始します。 データストアとビジネスニーズにもとづいて、次のいずれかの調達方法を選択します。

### 選択肢A:Experience PlatformからのSource

[Collaborationを使用して、オーディエンスを含むサンドボックスをリンクします](./setup/onboard-audiences.md)。 このセルフサービス方式を使用して、Experience Platform インスタンス内から既存のオーディエンスセグメントを参照します。

#### オーディエンスの設定

接続で使用するためにオーディエンスを準備、照合、管理する方法を設定します。

- **オーディエンスを選択** *（Experience Platformのみ）* - サポートされているIDを持つオーディエンスセグメントを選択します。
- **一致キーをマッピング** – 設定された一致キーにオーディエンスフィールドを整列させます。
- **変換を適用** – 必要に応じてプレーンテキスト値（電子メールなど）をハッシュ化します。
- **更新スケジュール** – 更新頻度を定義します（毎日など）。
- **同意設定の設定** – 同意モード（オプトイン、オプトアウト、なし）を選択して、接続に含める資格のあるプロファイルを決定します。

>[!NOTE]
>
>オーディエンスを追加または削除し、更新スケジュールをCollaborationで直接更新できます。 一致キーや同意モードなどの他の設定を変更するには、データ接続を削除して再作成する必要があります。

>[!IMPORTANT]
>
>**共同作業者の役割あたりの最大オーディエンス数：**
>
>- **広告主**&#x200B;は、最大25人のオーディエンスを獲得できます。
>- **パブリッシャー**&#x200B;は、最大250人のオーディエンスを取得できます（各オーディエンスのIDは1,000以上）。

>[!IMPORTANT]
>
>**一致するキー要件：**
>
>すべての一致キーは&#x200B;**トリミング**、**小文字にする必要があります**
>ハッシュ化された一致キーは&#x200B;**SHA256-hashed**&#x200B;である必要があります。\
>大文字を使用するハッシュ値を指定すると、Collaborationは自動的に小文字に変換します。\
>ソースに&#x200B;**プレーンテキスト識別子**&#x200B;が含まれている場合は、**[!UICONTROL 変換を適用]** オプションを使用してハッシュを適用します。 このオプションは、Experience Platformからオーディエンスをソーシングする場合にのみ使用でき、クラウドベースのソースではサポートされていません。
>
>詳しくは、ソースおよびオーディエンスの管理ガイドの「[&#x200B; マップフィールド &#x200B;](./setup/onboard-audiences.md#map-fields)」セクションを参照してください。

Collaborationを使用してオーディエンスを調達する方法の詳細については、以下の動画をご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

または、[Collaborationでのオーディエンスのソーシングに関するドキュメント &#x200B;](./setup/onboard-audiences.md#source-and-manage-audiences)を参照してください。

### 選択肢B:Snowflake、Amazon S3、またはGoogle Cloud StorageからのSource

[!DNL Snowflake]、[!DNL Amazon S3]、[!DNL Google Cloud Storage]などのクラウドソースを設定するには、[Audience Specification PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Sourcing_Spec_v1.2.pdf)を使用してオーディエンスデータを準備します

[!DNL Amazon S3]、[!DNL Google Cloud Storage]または[!DNL Snowflake]をセルフサービスのデータソースとして設定できます。 設定手順については、[Amazon S3 ソーシングガイド &#x200B;](./setup/configure-aws-s3-audience-sourcing.md)、[GCS ソーシングガイド &#x200B;](./setup/configure-gcs-audience-sourcing.md)、または[Snowflake ソーシングガイド &#x200B;](./setup/configure-snowflake-audience-sourcing.md)を参照してください。

その他のクラウドサービスプロバイダーについては、Adobeのアカウント担当者にお問い合わせください。

>[!IMPORTANT]
>
>クラウドベースのオーディエンスファイルは、Audience Specification PDFに記載されている必要なスキーマに従う必要があります。 ファイルには、ハッシュ化された識別子（小文字はSHA256）、`segment_name`や`activation_id`などの必須メタデータフィールド、およびCSVやParquetなどのサポートされている形式を使用する必要があります。 Adobeでは、アクティベーション前にデータが正規化されません。 TTLは、オーディエンスのライフスパンに基づいて適用されます。
>
>アップロードされたファイル内のすべてのオーディエンスは、この段階で完全にソース化されます。 [&#x200B; オーディエンスの表示設定](/help/guide/setup/onboard-audiences.md#metadata-visibility)によって、共同作業者がオーディエンスを表示できるかどうかが決まり、Collaboration UIを通じて管理されます。

## 手順4：オーディエンスのアクティベート（Experience Platformまたはクラウドの宛先） {#activate-audiences}

次に、Experience Platform インスタンスまたはクラウドの宛先に対してオーディエンスをアクティブ化します。

### 選択肢A:Experience Platformにアクティベートする

「[Adobe Experience Platformを宛先として設定する](/help/guide/destinations/experience-platform.md) ガイド」で説明されている次の手順を実行します。

- **宛先を作成** - UIを使用して、Experience Platformの宛先（サンドボックスレベル）を設定します。
- **一致するキーをマップ** – 識別子（例：`hashedEmail`）を選択します。
- **TTLを定義** – 有効期限を設定（1 ～ 30日）。
- **オーディエンスポータルで確認** – 共同作業者がオーディエンスを送信したら、オリジン「[!UICONTROL Real-Time CDP Collaboration]」の下のオーディエンスポータルに表示されていることを確認します。

### オプション B: クラウドに対してアクティブ化

クラウドの宛先（例：[!DNL AWS S3]または[!DNL Snowflake]）を設定するには、Adobe アカウント担当者に連絡して設定プロセスを開始してください。 クラウドの宛先に応じて、ファイルパス、資格情報、アカウントロケーターなどのクラウドの宛先の詳細を指定する必要があります。必要な情報が提供されると、Adobeはクラウド宛先設定を行います。

クラウド宛先に送信されたオーディエンスデータは、事前定義されたスキーマに従います。 必須フィールドと書式の詳細については、[Collaboration Audience Activation ガイド &#x200B;](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf)をダウンロードしてください。

## ステップ 5：測定の設定（オプション） {#set-up-measurement}

>[!IMPORTANT]
>
>**[!UICONTROL Measure]** ワークスペースは、接続プロセス [&#128279;](./connect/establishing-connections.md#connection-settings)中に&#x200B;**[!UICONTROL Measurement]** ユースケースが有効になった場合にのみ使用できます。 ユースケースについて詳しくは、[&#x200B; プロジェクトの管理](./collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。

Collaborationは、キャンペーンのリーチ、頻度、効果を分析するための様々なレポートを提供します。 **[!UICONTROL Measure]** ワークスペースはUIで使用できますが、完全なレポート機能を使用するには、バックエンドの有効化が必要になる場合があります。

測定レポートの表示および解釈の方法については、[測定ガイド &#x200B;](./collaborate/measure.md)を参照してください。 アトリビューション、キャンペーンの概要指標、リーチカーブや頻度分布などのダッシュボードについて説明します。

<!-- 
Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."

### Configure measurement workflow

Collaboration supports two measurement workflows:

- **Attribution using Adobe Experience Platform datasets**
- **Campaign summary using only partner-provided data**

Choose the appropriate workflow below based on your campaign measurement goals.

#### Option A: Attribution using Experience Platform datasets

Use this workflow to measure conversion activity using datasets stored in Experience Platform.

1. **Create a measurement data connection**
   - Select the dataset that contains your conversion events.
   - Map identity fields from your dataset to the match keys used in Collaboration.
   - Manage consent and governance settings.
   - Define one or more conversion events to measure.
   - Review and confirm your setup.

2. **Run a measurement report**
   - Go to the **[!UICONTROL Measure]** workspace within the associated project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Attribution]** as the report type.
   - Select the defined conversion event(s).
   - Submit the report. It will run on the specified date and populate within 24 hours.

#### Option B: Campaign summary using partner-provided data

Use this workflow to generate campaign summary insights based on advertiser-supplied identifiers (for example, campaign ID).

1. **Set up the connection**
   - In the connection settings, ensure **[!UICONTROL Measurement]** is selected as a use case.
   - Create a project under the connection with **[!UICONTROL Measurement]** as an activity.

2. **Provide campaign context**
   - Input required campaign identifiers (for example, **Campaign ID**) for the partner to reference.
   - Align with your partner on campaign scope and reporting timeline.

3. **Run a measurement report**
   - Navigate to the **[!UICONTROL Measure]** workspace within the project.
   - Input the report name, date range, and report run date.
   - Select **[!UICONTROL Campaign summary]** as the report type.
   - Submit the report. It will run on the selected date and populate within 24 hours. 
-->

## ステップ 6：共同作業者とつながる {#connect-with-collaborators}

設定が完了したら、招待を送信または受け入れ、承認のためにプロジェクト設定を送信することで、共同作業者とつながる準備が整います。 この接続プロセスには、招待の送信または受信、接続設定（ユースケースやクレジット消費など）の確認と送信、接続の確認が含まれます。

広告主は、左側のナビゲーションメニューの&#x200B;**[!UICONTROL Connect]** ワークスペースを使用して、使用可能なパブリッシャーを参照します。 また、共同作業者は、[&#x200B; プライベート接続招待](./connect/establishing-connections.md#private-connection-invite){target="_blank"}を通じて直接接続できます。

>[!NOTE]
>
>現在のところ、パブリッシャーを閲覧できるのは広告主のみです。 パブリッシャーは、広告主との接続を参照または開始できません。

このフローの概要については、[接続の確立ガイド &#x200B;](./connect/establishing-connections.md){target="_blank"}を参照してください。 共同作業者の参照や接続設定の管理など、接続プロセスの視覚的なチュートリアルについては、[広告主アカウント設定ビデオ &#x200B;](https://experienceleague.adobe.com/ja/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"}をご覧ください。

## 次の手順

これで、最初の設定が完了し、安全なコラボレーション用に組織を設定しました。 次のリソースを確認して、アクティベーション、測定、データガバナンスに関する理解を深めます。

- [&#x200B; オーディエンスのアクティブ化ワークフローのドキュメント &#x200B;](./collaborate/activate.md)
- [測定ユースケース &#x200B;](./collaborate/measure.md)
- [Collaborationのガバナンスのベストプラクティス](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
