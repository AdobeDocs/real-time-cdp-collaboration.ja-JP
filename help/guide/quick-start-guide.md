---
title: Real-Time CDP Collaboration クイックスタートガイド
description: 役割と組織の設定、オーディエンスソーシング、アクティベーション、測定など、Real-Time CDP Collaborationで組織をオンボーディングする方法について説明します。 このガイドは、広告主とパブリッシャーが共同作業の設定を行い、共有オーディエンスを安全かつ効率的に使用し始めるのに役立ちます。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 68e5095e-ece5-4f64-9056-10f3b216cf0c
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 0%

---

# Real-Time CDP Collaboration クイックスタートガイド



Real-Time CDP Collaborationの基本を学ぶには、組織を設定し、オーディエンスをソーシングし、プライバシーに焦点を当てたアクティベーションと測定を有効にします。

## 前提条件

開始する前に、次の点を確認してください。

- 有効なReal-Time CDP Collaboration ライセンス。
- [Adobe Experience Platformへのシステム管理者または製品管理者のアクセス ](./permissions/overview.md)。
- [ エンドユーザーにプロビジョニングされたアクセス ](./permissions/manage-user-access.md)。
- [ 組織用に作成され、ユーザーに割り当てられた役割 ](./permissions/manage-roles.md)。
- 組織の名前、ロゴ、バナーなど、ブランディングアセットへのアクセス。
- [ 定義済みの一致キー戦略 ](./setup/onboard-account.md#set-up-match-keys) （現在、サポートされている一致キーはハッシュ化されたメールのみです）。
- （任意）Experience Platform for audience management を使用していない場合は、サポートされているクラウドソース（Amazon S3 またはSnowflake）にアクセスします。

## 手順 1：役割ベースの設定の完了 {#complete-role-based-setup}

>[!NOTE]
>
>この手順は、広告主とパブリッシャーの両方に適用されます。

組織のアクセス権限によって、Collaborationでユーザーが表示および実行できる操作が決まります。 先に進む前に、プラットフォームでの適切なアクセスと表示を確保するために、役割ベースの権限が正しく設定されていることを確認してください。

**リソース：**

- [ユーザーアクセスドキュメント](./permissions/manage-user-access.md)
- [役割設定ドキュメント](./permissions/manage-roles.md)


Admin ConsoleとExperience Platformを使用して、Collaborationの製品アクセスと権限を割り当てる方法については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3452231/?learn=on&enablevpops&captions=jpn)

## 手順 2:Collaboration アカウントの設定 {#set-up-your-account}

>[!NOTE]
>
>この手順は、広告主とパブリッシャーの両方に適用されます。

オーディエンスをソーシングする前に、Collaborationでアカウントを設定する必要があります。 これは、インターフェイスでの表示方法とアクセス権の内容を管理します。

必要なアクセス権がない場合は、手順 1 に戻るか、組織の管理者に問い合わせて、この設定を完了してください。

Collaborationでのアカウントの役割を定義し、ブランディングアセットを提供し、一致キーを設定して、接続全体でオーディエンスを調整します。

>[!NOTE]
>
>セットアップ中に 1 つ以上のアカウント（広告主や公開者など）を作成できます。 ブランディングアセットや連絡先のメールなど、特定のフィールドは、後で **[!UICONTROL 設定]** ワークスペースで更新できます。

- **役割を割り当て** - アカウントが広告主かパブリッシャーかを決定します。 自分の役割によって、Collaborationに含める機能が定義されます。 役割がコラボレーションワークフローに与える影響について詳しくは、[ エンドツーエンドのワークフローガイド ](./end-to-end-workflow.md) を参照してください。
- **ブランディングアセット** - アカウントに以下を追加します。
   - アカウント名（最大 100 文字）
   - 説明（最大 1,000 文字）
   - ロゴ （SVG &lt;20KB、理想的には正方形）

>[!NOTE]
>
>公開者アカウントを作成中に、Collaboration Connections カタログに公開する場合は、Adobe アカウント担当者にお問い合わせください。 発行者アカウントにはカスタムブランドバナー（JPG 2688 x 1536）が必要です。このファイルは、の担当者に直接共有できます。

- **お問い合わせメール** – 接続が確立された後に共同作業者が使用するビジネスメールを指定します。
- **一致キーを設定** - オーディエンスマッチングに使用する識別子を選択します（現在、サポートされている一致キーはハッシュ化されたメールのみです）。

役割の定義、ブランディングアセットのアップロード、一致キーの設定の方法など、アカウントの初期設定について詳しくは、[ アカウントの初期設定 ](./setup/onboard-account.md#initial-account-setup){target="_blank"} ガイドを参照してください。

アカウントの作成、ブランディング、一致キーの設定など、広告主の設定に関する詳しい手順については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3452264/?learn=on&enablevpops)

## 手順 3:Source オーディエンス（Experience Platformまたはクラウドソースから） {#source-audiences}

アカウントを作成し、ブランディングと一致キーを設定したら、オーディエンスのソーシングを開始する準備が整います。 データストアとビジネスニーズに基づいて、次のいずれかのソーシング方法を選択します。

### オプション A:Experience PlatformのSource

[Collaborationを使用して、オーディエンスを含んだサンドボックスをリンクする ](./setup/onboard-audiences.md) このセルフサービス方式を使用して、Experience Platform インスタンス内から既存のオーディエンスセグメントを参照します。

#### オーディエンスの設定

接続で使用するオーディエンスの準備、マッチ、管理方法を設定します。

- **オーディエンスを選択** *（Experience Platformのみ）* - サポートされる識別子を持つオーディエンスセグメントを選択します。
- **一致キーのマッピング** - オーディエンスフィールドを、設定された一致キーに合わせます。
- **変換を適用** – 必要に応じて、プレーンテキスト値（メールなど）をハッシュ化します。
- **更新のスケジュール設定** – 更新頻度（毎日など）を定義します。
- **同意設定の設定** – 同意モード（オプトイン、オプトアウトまたはなし）を選択して、接続に含める資格のあるプロファイルを決定します。

>[!NOTE]
>
>オーディエンスを追加または削除し、Collaborationで直接更新スケジュールを更新できます。 一致キーや同意モードなど、他の設定を変更するには、データ接続を削除して再作成する必要があります。

>[!IMPORTANT]
>
>**共同作業者の役割ごとの最大オーディエンス数：**
>
>- **広告主** は、最大 25 個のオーディエンスをソースにすることができます。
>- **パブリッシャー** は、最大 250 個のオーディエンス（それぞれが最小 5,000 個の ID を持つ）をソースできます。

>[!IMPORTANT]
>
>**キー要件に一致：**
>
>すべての一致キーは、**トリミング**、**小文字**、および **SHA256 ハッシュ** である必要があります。\
>大文字を使用するハッシュ値を指定すると、Collaborationによって自動的に小文字に変換されます。\
>ソースに **プレーンテキスト識別子** が含まれている場合は、「**[!UICONTROL 変換を適用]**」オプションを使用してハッシュを適用します。 このオプションは、Experience Platformからオーディエンスを取得する場合にのみ使用でき、クラウドベースのソースではサポートされません。
>
>詳しくは、ソースおよびオーディエンス管理ガイドの [ フィールドのマッピング ](./setup/onboard-audiences.md#map-fields) の節を参照してください。

Collaborationを使用してオーディエンスをソース化する方法の完全なチュートリアルを確認するには、以下のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/3452217/?learn=on&enablevpops)

または、[Collaborationでのオーディエンスのソーシング ](https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/setup/onboard-audiences#import-audiences) のドキュメントを参照してください。

### オプション B:SnowflakeのSourceまたはAmazon S3

クラウドソース（[!DNL AWS S3] や [!DNL Snowflake] など）を設定するには、次の [ オーディエンス仕様PDF](../assets/quick-start/RTCDP_Collaboration_Audience_Onboarding_Spec_v1.0.pdf) を使用してオーディエンスデータを準備します。 設定が完了したら、または質問がある場合は、Adobe アカウント担当者に連絡して設定を完了してください。 この方法はセルフサービスではないので、Adobeのサポートが必要です。

>[!IMPORTANT]
>
>クラウドベースのオーディエンスファイルは、オーディエンス仕様PDFで説明されている必要なスキーマに従う必要があります。 ファイルには、ハッシュ化された識別子（小文字の SHA256）、必須のメタデータフィールド（`segment_name` や `activation_id` など）を含め、CSV や Parquet などのサポートされている形式を使用する必要があります。 Adobeは、アクティブ化の前にデータを正規化しません。 TTL は、オーディエンスの存続期間に基づいて適用されます。
>
>アップロードされたファイル内のすべてのオーディエンスは、この段階で完全にソース化されます。 [ オーディエンス表示設定 ](/help/guide/setup/onboard-audiences.md#metadata-visibility) は、共同作業者がオーディエンスを表示できるかどうかを決定し、Collaboration UI を使用して管理されます。

## 手順 4：オーディエンスをアクティブ化（Experience Platformまたはクラウドの宛先に対して） {#activate-audiences}

>[!NOTE]
>
>この手順は、広告主とパブリッシャーの両方に適用されます。

次に、Experience Platform インスタンスまたはクラウドの宛先に対してオーディエンスをアクティブ化します。

### オプション A:Experience Platformに対してアクティブ化

[Adobe Experience Platformを宛先として設定 ](/help/guide/destinations/experience-platform.md) ガイドで説明されている次の手順を実行します。

- **宛先の作成** - UI を使用して、Experience Platformの宛先（サンドボックスレベル）を設定します。
- **一致キーをマッピング** – 識別子を選択します（例：`hashedEmail`）。
- **TTL の定義** – 有効期限（1～30 日）を設定します。
- **Audience Portal での検証** – 共同作業者がオーディエンスを送信したら、そのオーディエンスが接触チャネル「[!UICONTROL Real-Time CDP Collaboration]」の下の Audience Portal に表示されることを確認します。

### オプション B：クラウドに対してアクティブ化

クラウドの宛先（[!DNL AWS S3] や [!DNL Snowflake] など）を設定するには、Adobe アカウント担当者に連絡して設定プロセスを開始します。 クラウドの宛先に応じて、ファイルパス、資格情報、アカウントロケーターなど、クラウドの宛先の詳細を指定する必要があります。 必要な情報が入力されると、Adobeによってクラウドの宛先の設定が行われます。

クラウドの宛先に送信されるオーディエンスデータは、事前に定義されたスキーマに従います。 必須フィールドと形式について詳しくは、[Collaboration Audience Activation ガイド ](../assets/quick-start/RTCDP_Collaboration_Audience_Activation_Spec_v1.0.pdf) をダウンロードしてください。

## 手順 5：測定の設定（オプション） {#set-up-measurement}

>[!AVAILABILITY]
>
>この機能は **ベータ版** で、限定提供プログラムのお客様のみが利用できます。 アクセス権をリクエストするには、Adobe担当者にお問い合わせください。

>[!IMPORTANT]
>
>**[!UICONTROL 測定]** ワークスペースは、**[!UICONTROL 測定]** ユースケースが [ 接続プロセス中に ](./connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[ プロジェクトの管理 ](./collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。

Collaborationには、キャンペーンのリーチ、頻度および効果を分析するための様々なレポートが用意されています。 **[!UICONTROL 測定]** ワークスペースは UI で使用できますが、完全なレポート機能ではバックエンドの有効化が必要になる場合があります。

測定レポートの表示および解釈方法については、[ 測定ガイド ](./collaborate/measure.md) を参照してください。 アトリビューション、キャンペーンの概要指標、ダッシュボード（リーチカーブや頻度分布など）について説明します。

<!-- Commenting out the below information as this workflow is not yet in Beta but will be imminently. A guided measurement configuration workflow will be available in a future release."
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
   - Submit the report. It will run on the selected date and populate within 24 hours. -->

## 手順 6：共同作業者と接続する {#connect-with-collaborators}

設定が完了したので、組織は招待を送信または受け入れ、承認のためにプロジェクト設定を送信することで、共同作業者と接続する準備が整いました。 この接続プロセスには、招待状の送信または受信、接続設定（ユースケースやクレジット消費など）の確認と送信、接続の確認が含まれます。

広告主は、左側のナビゲーションメニューの **[!UICONTROL 接続]** ワークスペースを使用して、使用可能な公開者を参照します。

>[!NOTE]
>
>現在、パブリッシャーを参照できるのは広告主のみです。 パブリッシャーは、広告主との接続を参照または開始できません。

このフローの概要については、[ 広告主またはパブリッシャーとの接続ガイド ](./connect/establishing-connections.md){target="_blank"} を参照してください。 共同作業者の参照や接続設定の管理など、接続プロセスの視覚的な手順については、[ 広告主アカウントの設定ビデオ ](https://experienceleague.adobe.com/ja/docs/platform-learn/tutorials/collaboration/connect-with-publishers){target="_blank"} をご覧ください。

## 次の手順

これで、初期設定が完了し、共同作業を保護するために組織が設定されました。 次に、アクティベーション、測定、データガバナンスに関する理解を深めるために、次のリソースを探索します。

- [Audience Activation ワークフロードキュメント ](./collaborate/activate.md)
- [ 測定の使用例 ](./collaborate/measure.md)
- [Collaboration ガバナンスのベストプラクティス](./setup/onboard-audiences.md#governance-policy-and-enforcement-actions)
