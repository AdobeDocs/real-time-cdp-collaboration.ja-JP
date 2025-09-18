---
title: 連携の確立
description: 潜在的な共同作業者を見つけた後、連携を確立し、プロジェクトでの共同作業を開始する方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: 899b6c2a0111ccaebbaf2818772e1d743d6de914
workflow-type: tm+mt
source-wordcount: '3400'
ht-degree: 6%

---

# 連携の確立 {#establishing-connections}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_compare_audiences"
>title="オーディエンスの比較"
>abstract="オーディエンスを、Amazon広告で到達したすべてのコンシューマーと比較します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_relevant_audiences"
>title="関連するオーディエンス"
>abstract="Amazonのインプレッションのみを考慮して、オーディエンスの重複が最も大きいDSP ターゲティングセグメント（これらのセグメントはDSPでのみターゲット設定できます）。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_resolved_ids"
>title="解決された ID"
>abstract="Amazonの ID 解決が、オーディエンスデータを使用して解決できた ID の数です。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlapping_ad_exposed_ids"
>title="重複する公開済み ID"
>abstract="これは、アップロードされたオーディエンスのうち、Amazon Ads 経由で広告にも公開された「解決済み ID」の数を表します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_overlap_percentage"
>title="重複 %"
>abstract="Amazon Ads 経由で広告に公開された「解決済み ID」の割合。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_amc_discover_amazon_breakdown"
>title="Amazon広告商品ごとの分類"
>abstract="Amazon Ads スポンサー商品またはAmazon Ads DSPが到達した「重複広告公開 ID」の分類。"

{{limited-availability-release-note}}

コラボレーターがキャンペーンで連携する前に、連携を確立する必要があります。 この接続を使用すると、オーディエンスのアクティブ化、プロジェクトの作成およびキャンペーンのパフォーマンスに関するレポートの実行を行うことができます。

選択したコラボレーションパターンに基づいて接続が確立されます。 Collaborationは、広告主からパブリッシャーおよびブランドからブランドという 2 つの主要なコラボレーションパターンをサポートしています。 これらのパターンについて詳しくは、「[ 使用例 ](/help/guide/overview/use-cases.md) ガイドを参照してください。

接続を確立する方法については、コラボレーションパターンに対応する以下の節を参照してください。

- [広告主とパブリッシャーの接続](#advertiser-to-publisher-connection)
- [ブランド間の接続](#brand-to-brand-connection)

## 広告主とパブリッシャーの接続 {#advertiser-to-publisher-connection}

![ 広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

広告主からパブリッシャーへのパターンでは、広告主は **[!UICONTROL パブリッシャーの検出]** ワークスペースを通じて、連携するパブリッシャーを検出し、接続の招待を送信します。 次に、パブリッシャーは招待を確認して受け入れ、広告主が接続設定を提案できるようにします。 パブリッシャーが接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトでの作業を開始できます。

### の概要

広告主とパブリッシャーの間の接続を確立するには、次の手順が必要です。

1. [ パブリッシャーの検出 ](#discover-publishers)：広告主は、共同作業を行う潜在的なパブリッシャーを特定します。
1. [ 招待を送信 ](#send-invite)：広告主は、選択したパブリッシャーに接続招待を送信します。
1. [ 招待を受け入れる ](#accept-invite)：パブリッシャーが招待をレビューし、承認します。
1. [ 接続設定の指定 ](#configure-connection-settings)：広告主は接続設定を指定し、レビュー用にパブリッシャーに送信します。
1. [ 接続設定の確認 ](#establish-connection)：パブリッシャーは接続設定を確認し、受け入れるか拒否します。 許可された場合、接続が確立されます。 拒否された場合、公開者は製品外のリビジョンに関するフィードバックを提供できます。 その後、広告主は設定を修正し、レビュー用に再送信できます。

接続設定を受け入れると、接続が確立され、共同作業者は [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) してキャンペーンでの共同作業を開始する準備が整います。

## ブランド間の接続 {#brand-to-brand-connection}

![ ブランド間接続プロセスの概要図。](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>**ブランド** という用語は、Collaboration以外の会社またはブランドを参照するために使用されます。 **共同作業者** という用語は、広告主であるか媒体社であるかに関係なく、Collaborationで関連性を形成できる任意のアカウントを指します。

ブランド間パターンでは、商品外でコミュニケーションを取った 2 つのブランドが、「プライベート接続への招待 [ を使用して、Collaborationで直接接続でき ](#private-connection-invite) す。 ブランドは、広告主または公開者のいずれかです。 このパターンは、2 人の広告主や 2 人のパブリッシャーなど、従来の広告主 – パブリッシャーモデルに適合しない可能性のあるブランドで特に役立ちます。

まず、共同作業者がプライベート接続の招待状を別の共同作業者に送信します。 受信者が招待を確認して承諾すると、所有者が接続設定を提案できます。 受信者が接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトでの作業を開始できます。

### の概要

>[!TIP]
>
>接続プロセスについて話し合う際には、**owner** と **recipient** が区別されます。 所有者は、招待を送信して接続を開始する共同作業者であり、受信者は、招待を受信してレビューする共同作業者です。

2 つのブランド間の接続プロセスには、いくつかの手順が必要です。 接続プロセスを開始する前に、次の前提条件を満たす必要があります。

1. 2 つのブランドが製品外でコミュニケーションを取り、潜在的な接続について話し合っています。
1. Collaborationのブランド [ アカウントの作成 ](/help/guide/setup/onboard-account.md) をまだ行っていない場合は、適切なロールタイプ（広告主またはパブリッシャー）を必ず選択します。

   前提条件が満たされたら、接続プロセスを開始できます。 次の手順でプロセスの概要を説明します。

1. [ プライベート接続の招待を送信 ](#send-private-connection-invite):1 人の共同作業者が別の共同作業者にプライベート接続の招待を送信します。
1. [ プライベート接続への招待を受け入れる ](#accept-private-connection-invite)：受信者がプライベート接続への招待を確認して承諾します。
1. [ 接続設定の指定 ](#configure-connection-settings)：所有者が接続設定を指定し、レビューと承認を受けるために受信者に送信します。
1. [ 接続設定の確認 ](#establish-connection)：受信者は接続設定を確認し、受け入れるか拒否します。

接続設定を受け入れると、接続が確立され、共同作業者は [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) してキャンペーンでの共同作業を開始する準備が整います。

## 接続 {#connect}

**[!UICONTROL 接続]** ワークスペースでは、共同作業者との接続を管理したり、接続招待状を送信したり、広告主が発行者ディレクトリを参照したりできます。 ワークスペースは、次の 2 つのメインタブに分かれています。

### パブリッシャーを検出 {#discover-publishers}

>[!IMPORTANT]
>
>**[!UICONTROL パブリッシャーの検出]** ワークスペースを使用してパブリッシャーを検出できるのは広告主のみです。 役割に関係なく共同作業者と接続する方法については、[ ブランド間接続 ](#brand-to-brand-connection) の節を参照してください。

パブリッシャーを検出するには、「**[!UICONTROL 接続]**」タブの **[!UICONTROL パブリッシャーを検出]** ワークスペースに移動します。 ここでは、ワークスペースの下部にあるページネーションコントロールを使用して、使用可能な公開者のリストを参照できます。 **[!UICONTROL Discover パブリッシャー]** ワークスペースについて詳しくは、[Discover パブリッシャー ](/help/guide/connect/discover-publishers.md) ガイドを参照してください。

![ 使用可能なパブリッシャーのリストを表示する Discover パブリッシャーワークスペース。](/help/assets/connect/establish-connection/discover-publishers.png){zoomable="yes"}

### 招待状を送信 {#send-invite}

>[!IMPORTANT]
>
>ここでは、広告主が **[!UICONTROL Discover パブリッシャー]** ワークスペースを通じて接続招待をパブリッシャーに送信するプロセスについて説明します。 ブランドの役割に関係なく、ブランド間の接続を形成する方法については、[ ブランド間接続 ](#brand-to-brand-connection) の節を参照するか、[ プライベート接続の招待 ](#private-connection-invite) の節を参照してください。

共同作業するパブリッシャーを特定したら、パブリッシャーカードの **[!UICONTROL 接続]** オプションを選択します。 接続プロセスを開始します。

![Discover パブリッシャーワークスペースで特定のパブリッシャーでハイライト表示された「接続」オプション。](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

接続招待をパブリッシャーに送信するよう促すダイアログが表示されます。 「**[!UICONTROL 招待を送信]**」を選択して続行します。

![ 「招待を送信」ボタンがハイライト表示された接続の招待を送信ダイアログ ](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>製品外とやり取りしたパブリッシャーと接続する場合は、プライベート接続の招待オプションを利用できます。 詳しくは、[ プライベート接続の招待 ](#private-connection-invite) の節を参照してください。

保留中の招待は、[**[!UICONTROL 必要な操作]**] セクションの [**[!UICONTROL マイ接続]**] タブに表示されます。 接続ステータスは **[!UICONTROL 招待状が送信されました]** と表示されます。 **[!UICONTROL 接続のプレビュー]** を選択すると、接続設定をプレビューできますが、パブリッシャーが招待を受け入れるまで編集できません。

![ 保留中の接続は、[ マイ接続 ] ワークスペースの [ 操作が必要 ] セクションに表示されます。](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}

### プライベート接続への招待 {#private-connection-invite}

プライベート接続の招待を使用すると、**[!UICONTROL Connect コード]** を使用して、製品外と通信した共同作業者と接続できます。 プライベート接続を形成するには、製品外で接続する共同作業者から **[!UICONTROL Connect コード]** を取得する必要があります。 その後、このコードを使用して、**[!UICONTROL 接続]** ワークスペースの共同作業者にプライベート接続の招待を送信できます。

#### 接続コード {#connect-code}

プライベート接続の招待状を送信する前に、目的の共同作業者が一意の **[!UICONTROL Connect コード]** を提供する必要があります。 **[!UICONTROL Connect コード]** を探してコピーするには、「設定 **[!UICONTROL ワークスペース内の]** マイアカウント **[!UICONTROL タブに移動し]** す。 **[!UICONTROL Connect コード]** がアカウントの詳細内に表示されます。

![ 接続コードがハイライト表示された設定ワークスペース内の「マイアカウント」タブ。](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

![ コードを接続 ](/help/assets/icons/copy.png) の横にあるコピーアイコン（**[!UICONTROL コピーアイコン]**）を選択して、クリップボードにコピーします。 このコードを製品外の共同作業者と共有できます。

![ 「コピー」アイコンがハイライト表示された「コードを接続」 ](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### 接続コードの更新 {#refresh-connect-code}

**[!UICONTROL Connect コード]** はいつでも更新できます。 コードを更新すると、共同作業者と共有できる新しい一意のコードが生成されます。 これは、セキュリティ上の理由から以前のコードを無効にする場合に便利です。 古いコードを使用して確立された接続は引き続きアクティブですが、新しい共同作業者は、新しいコードを使用して接続する必要があります。

>[!IMPORTANT]
>
>保留中の招待中に **[!UICONTROL 接続コード]** を更新すると、招待が受け入れられない可能性があります。 コードを更新すると、共同作業者は、新しいコードを使用してプライベート接続の招待を再送信する必要がある場合があります。

**[!UICONTROL Connect コード]** を更新するには、![Connect コード ](/help/assets/icons/refresh.png) の横にある更新アイコン（**[!UICONTROL 更新アイコン]**）を選択します。

![ 更新アイコンがハイライト表示された接続コード。](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>**[!UICONTROL 接続コード]** 機能が導入される前に作成されたアカウントには、生成された接続コードがなく、接続フィールドには **[!UICONTROL 使用不可]** と表示されます。 「更新」オプションを使用して、新しい接続コードを生成します。

#### プライベート接続への招待の送信 {#send-private-connection-invite}

共同作業者から **[!UICONTROL 接続コード]** を取得したら、プライベート接続の招待を送信できます。 これを行うには、**[!UICONTROL 接続]** ワークスペースに移動し、右上隅のプラスアイコン（![ プラスアイコン ](/help/assets/icons/plus.png)）を選択します。

![ 接続ワークスペースでハイライト表示されたプラスアイコン。](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

**[!UICONTROL 接続]** ダイアログが表示され、接続する共同作業者の **[!UICONTROL 接続コード]** を入力するように求められます。 コードをテキストフィールドに貼り付け、「**[!UICONTROL 続行]** を選択して続行します。

![ 「接続コード」フィールドが入力され、「続行」オプションがハイライト表示された接続ダイアログ ](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

**[!UICONTROL 接続]** ダイアログに、コードが関連付けられている共同作業者が表示され、正しい共同作業者で接続していることを確認できます。 共同作業者が正しい場合は、[**[!UICONTROL 接続]**] を選択して、プライベート接続の招待を送信します。

![ 共同作業者の詳細が表示され、「接続」オプションがハイライト表示された接続ダイアログ ](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### 招待状を承認 {#accept-invite}

>[!TIP]
>
>接続プロセスについて話し合う際には、**owner** と **recipient** が区別されます。 所有者は、招待を送信して接続を開始する共同作業者であり、受信者は、招待を受信してレビューする共同作業者です。

所有者が接続設定を指定する前に、受信者は接続への招待を受け入れる必要があります。 これを行うには、「**[!UICONTROL 接続]**」ワークスペースに移動し、「**[!UICONTROL アクションが必要]**」セクションで保留中の接続を見つけます。 接続ステータスは **[!UICONTROL 招待状を受信]** と表示されます。 「**[!UICONTROL 同意する]**」を選択して、招待を承認します。

![ 保留中の接続は、「同意」オプションがハイライト表示された「接続」ワークスペースの「アクションが必要」セクションに表示されます。](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

招待を受け入れるよう促すダイアログが表示されます。 **[!UICONTROL 招待を受け入れる]** を選択して続行します。

![ 「招待を承認」オプションがハイライト表示された接続の招待を承認ダイアログ ](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

接続のステータスが「**[!UICONTROL 保留中]** に変わります。 これで、所有者が接続設定を指定できるようになります。

### 接続設定の指定 {#configure-connection-settings}

接続設定は、2 人の共同作業者の間の用語を定義します。 これらの設定には、ユースケース、一致キー、クレジット分割、法的契約が含まれます。 広告主と接続する共同作業者は、接続設定に広告主名を追加することもできます。この設定は、プロジェクトを作成する際に使用されます。

受信者が招待を受け入れると、所有者が接続設定を指定できます。 これを行うには、**[!UICONTROL マイ接続]** に移動し、**[!UICONTROL 必要なアクション]** セクションで保留中の接続を見つけます。 **[!UICONTROL 接続を設定]** を選択して、接続設定を指定します。

![ 「必要なアクション」セクションで「接続を設定」オプションがハイライト表示された接続ワークスペース。](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

接続設定ワークスペースが表示され、接続の様々な設定を指定できます。

![ 接続設定ワークスペース ](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

#### 接続設定 {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="ユースケース"
>abstract="ユースケースには、すべてのオプションが事前入力されています。接続設定を送信する前に、ユースケースを編集できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="一致キー"
>abstract="一致キーには、自分と共同作業者がアカウントレベルで選択した共通の一致キーが事前入力されます。 この接続で使用しない一致キーは、オフに切り替えることができます。"
>additional-url="https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/setup/onboard-account#set-up-match-keys" text="アカウント一致キー"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit"
>title="クレジット分割"
>abstract="このセクションでは、Collaboration 内の対応するアクティビティに対して支払いを行うユーザーを決定します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="オーディエンス共有"
>abstract="Audience Activation のクレジットは、アクティベーションのために準備された一致する ID の数に基づいて消費されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="測定"
>abstract="アクティビティを実行して、キャンペーンのパフォーマンスレポートとインサイトを生成します。クレジットは、すべてのキャンペーンのキャンペーンレポートの行数とレポートの頻度（毎日、3 日ごと、または週ごと）に基づいて消費されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="広告主名"
>abstract="<p>オプションの設定。発行者が認識している広告主の名前と ID を示します。</p><p>ここに追加する広告主名は、プロジェクトを作成ステップで事前入力されます。</p><ul><li>発行者が複数の名前を設定している場合は、リストから 1 つ選択します。</li><li>1 つの名前のみを設定する場合は、自動的に事前選択されます。</li><li>名前が設定されていない場合、このフィールドには、Collaboration の広告主アカウント名が事前入力されます。</li></ul>"
>additional-url="https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="プロジェクトの作成"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Audience Activation"
>abstract="Audience Activation を使用すると、Audience Activation を開始できる共同作業者を選択できます。"

次の接続設定を指定できます。

##### Audience Activation {#audience-activation}

>[!IMPORTANT]
>
>**[!UICONTROL Audience Activation]** 機能が導入される前に作成した接続では、自動的に接続所有者に対する Audience Activation 設定が設定されます。 両方の共同作業者がオーディエンスをアクティブ化できるようにする場合は、[ 現在の接続を削除 ](#delete-connections) し、更新された設定で新しい接続を作成する必要があります。

Audience Activation を使用すると、接続内でオーディエンスをアクティブ化できる共同作業者を選択できます。 Audience Activation は、「**[!UICONTROL Audience Activation]** のユースケースが選択されている場合にのみ、オプションになります。 接続プロセスの実行中にユースケースを削除することを選択した場合、Audience Activation 設定は接続設定から削除されます。 Audience Activation について詳しくは、[ アクティベート ](/help/guide/collaborate/activate.md) ガイドを参照してください。

Audience Activation を設定するには、「**[!UICONTROL Audience Activation]** セクションの **[!UICONTROL 設定]** を選択します。 ドロップダウンメニューを使用して、オーディエンスをアクティブ化できる共同作業者を指定します。 1 人の共同作業者を選択することも、両方の共同作業者がオーディエンスをアクティブ化できるようにすることもできます。

![ 接続設定ワークスペースのオプションを含む Audience Activation ダイアログ。](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

完了したら、「**[!UICONTROL 保存]** を選択して変更を保存します。

![ 接続設定ワークスペースに「保存」オプションが表示された Audience Activation ダイアログ ](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

##### ユースケース {#use-cases}

ユースケースには、使用可能なすべてのオプションが自動的に入力されます。 選択したユースケースによって、プロジェクト内で使用できるビューやオプションが決まります。 詳しくは、[ プロジェクトのユースケース ](/help/guide/collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。

ユースケースをカスタマイズするには、「**[!UICONTROL ユースケース]**」セクションで **[!UICONTROL 編集]** を選択し、共同作業者とのプロジェクトに含めたくないプロジェクトをオフにします。 完了したら、「**[!UICONTROL 保存]** を選択して変更を保存します。

![ 接続設定ワークスペースのユースケース設定 ](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

##### 一致キー {#match-keys}

>[!IMPORTANT]
>
>複数の一致キーが使用されているオーディエンスをアクティブ化する場合、1 つ（または複数）の一致キーの重複がない、オーディエンス数がない、またはしきい値を下回る場合、アクティベーション全体が失敗します。 オーディエンスに十分な重複があり、アクティブ化する前にすべての一致キーで 1000 個の ID の最小しきい値を満たしていることを確認します。

一致キーは、ユーザーと共同作業者が [ アカウントの設定 ](/help/guide/setup/onboard-account.md#set-up-match-keys) 時に選択した共通の一致キーで自動的に入力されます。 自分と共同作業者の両方が選択した **および** 共通している一致するキーのみが表示されます。

![ 共通の一致キーを示す「キーを一致」セクションがハイライト表示された接続設定ワークスペース。](/help/assets/connect/establish-connection/auto-populated-match-keys.png){zoomable="yes"}

接続所有者が接続設定を設定する際に、追加の一致キーを含めるために [ アカウント一致キーを編集 ](../setup/onboard-account.md#edit-match-keys) できます。 アカウント設定で一致キーをさらに切り替えると、共同作業者も選択している場合、それらの一致キーを接続設定でオンに切り替えることができます。 接続プロセスを開始した後に追加された一致キーは自動的には入力されず、手動で切り替える必要があります。

一致キーをカスタマイズするには、「**[!UICONTROL 一致キー]**」セクションで **[!UICONTROL 編集]** を選択し、この接続で使用しない一致キーをオフに切り替えます。 完了したら、「**[!UICONTROL 保存]** を選択して変更を保存します。

![ キーの一致セクション ダイアログが開き、キーの一致がオフに切り替えられた接続設定ワークスペース ](/help/assets/connect/establish-connection/additional-match-key-selected.png){zoomable="yes"}

>[!IMPORTANT]
>
>共同作業者が接続設定を承認すると、一致キーはロックされ、変更できなくなります。

##### クレジット分割 {#credit-split}

「クレジット分割」セクションを使用して、共同作業している 2 つの関係者のうち、アクティビティのコストを負担するのはどれかを決定します。 クレジット分割オプションは、接続に対して選択したユースケースによって決定されます。 **[!UICONTROL 測定]** のユースケースではコストをカバーするために一方のパーティが必要ですが、**[!UICONTROL アクティベーション – マッチング]** のユースケースでは、追加のオプションとして各パーティに独自のコストをカバーさせることができます。 コストの内訳について詳しくは、[ クレジットアクティビティタイプ ](/help/guide/setup/my-activity.md#types-of-activities) ガイドを参照してください。

>[!NOTE]
>
>オーディエンス – 出力は、常にオーディエンスを受け取る共同作業者によってカバーされるので、選択は必要ありません。

与信分割を設定するには、「**[!UICONTROL 与信分割]** セクションで **[!UICONTROL 編集]** を選択します。 その後、ユースケースごとに適切なオプションを選択できます。 完了したら、「**[!UICONTROL 保存]** を選択して変更を保存します。

![ 接続設定ワークスペースにオプションが表示されたクレジット分割ダイアログ ](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

##### 広告主名 {#advertiser-names}

>[!NOTE]
>
>このオプションは、接続を開始したユーザーに応じて、接続設定の設定中や接続設定の確認中に表示される場合があります。

広告主との接続を形成するパブリッシャーの場合は、接続設定で広告主名を追加することを選択できます。 これにより、システム内で広告主が自分に知られている複数の名前を追加できます。 これは、広告主が複数の地域に存在する場合や、様々なコンテキストで異なる名前で知られている場合に特に便利です。 後でプロジェクトを作成する際に、接続設定で設定された名前のリストから適切な広告主名を選択できます。

![ 接続設定ワークスペースの広告主名。](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

広告主名を追加するには、「**[!UICONTROL 広告主名]** セクションの **[!UICONTROL 編集]** を選択します。 その後、システム内で広告主が認識できる **[!UICONTROL 広告主 ID]** と、Collaboration内でその ID に関連付ける **[!UICONTROL 広告主名]** を入力できます。 「**[!UICONTROL 追加]** オプションを選択して、複数の広告主名を追加できます。

![ 接続設定ワークスペースにオプションが表示された広告主名ダイアログ ](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

完了したら、「**[!UICONTROL 保存]** を選択して変更を保存します。

プロジェクトを作成する際には、接続時に設定された以下の設定に基づいて広告主名が事前入力されます    :

1. **広告主名を設定しない**：広告主名を追加しない場合、Collaborationではデフォルトで広告主名が使用されます。
2. **1 つの広告主名セット**:1 つの広告主名が追加された場合、Collaborationはその名前をプロジェクトの広告主名として自動的に使用します。
3. **複数の広告主名を設定**：複数の広告主名を追加した場合、ユーザーまたは共同作業者は、プロジェクトの作成時に、指定された名前のいずれかを選択できます。

>[!NOTE]
>
> 接続設定を送信すると、広告主名を追加または編集できなくなります。

![ 「広告主名」セクションに値が入力された接続設定ワークスペース ](/help/assets/connect/establish-connection/add-advertiser-names.png)

選択が完了したら、「**[!UICONTROL 送信]**」を選択して、提案された設定をレビュー用に受信者に送信します。

### 接続設定を確認 {#review-connection-settings}

次に、受信者は、所有者によって提案された接続設定を確認する必要があります。 受信者は、「接続 **[!UICONTROL ワークスペースの]** マイ接続 **[!UICONTROL タブに移動することでこれを実行でき]** す。 「**[!UICONTROL 必要なアクション]**」セクションに接続が表示されます。 **[!UICONTROL 接続設定を確認]**」を選択して、提案された接続設定を確認します。

![ 「接続設定を確認」オプションがハイライト表示されたマイ接続ワークスペース。](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

共同作業者が提案した設定を確認します。 接続設定は、承認または拒否できます。 接続設定を拒否する場合は、製品外で行う変更について共同作業者と連絡を取る必要があります。 共同作業者の連絡先情報は、接続設定ワークスペースの **[!UICONTROL 連絡先]** セクションに表示されます。 その後、所有者は接続設定を変更し、レビュー用に再送信できます。

![ 「確定」および「却下」オプションがハイライト表示された接続設定ワークスペース ](/help/assets/connect/establish-connection/accept-connection-settings.png){zoomable="yes"}

さらに、広告主と接続するパブリッシャーの場合、接続設定に広告主名を追加できるようになりました。 このプロセスについて詳しくは、[ 接続設定 ](#connection-settings) の節を参照してください。

>[!NOTE]
>
> 接続設定を承認すると、広告主名を追加または編集できなくなります。

次に、「**[!UICONTROL 同意する]** を選択して、接続を続行します。 接続ステータスが **[!UICONTROL アクティブ]** に変わり、プロジェクトの共同作業を開始できるようになります。

## 接続の削除 {#delete-connections}

引き続き使用しない、共同作業者との接続を削除できます。 既存の接続を削除するには、**[!UICONTROL 接続]** に移動します。 パブリッシャーには、既存の接続が表示されます。 広告主の場合は、「マイ連携 **[!UICONTROL に移動する必要があ]** ます。

削除する接続カードで「**[!UICONTROL 接続を表示]**」を選択します。

![ マイ接続ビューでハイライト表示された「接続を表示」オプション ](/help/assets/connect/establish-connection/delete-view-connection.png){zoomable="yes"}

接続ワークスペースで削除アイコン ![ 削除アイコン ](/help/assets/common/delete.svg) を選択して、接続を削除します。

![ 接続ワークスペースでハイライト表示された削除アイコン。](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

接続の削除を確認する確認ダイアログが表示されます。 「**[!UICONTROL 削除]**」を選択して、削除を確定します。

![ 接続を削除するための確認ダイアログ。](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>接続が削除されると、コラボレーション内の既存のプロジェクトはすべて完全に削除され、復元できなくなります。 接続要求は保留状態のままになりますが、接続とその設定はアクティブではなくなります。 共同作業者と再度接続する場合は、接続を再確立する必要があります。

## 次の手順

共同作業者との接続を確立すると、共同作業者と [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) できるようになります。
