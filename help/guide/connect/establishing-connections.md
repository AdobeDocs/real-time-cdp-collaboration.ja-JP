---
title: 共同作業者との関係の確立
description: 潜在的な共同作業者を見つけた後、つながりを確立し、プロジェクトでの共同作業を開始する方法を学びます。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
TQID: https://experienceleague.adobe.com/N9tz3RPzEWdG-SEplHk5Vt6L3g2NkV03JO7PlGllPMk
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: fb824ee8d84cb8dc125da82a4afd6f50e3ce80cf
workflow-type: tm+mt
source-wordcount: 3420
ht-degree: 9%

---

# 共同作業者との関係の確立 {#establishing-connections}

{{limited-availability-release-note}}

共同作業者がキャンペーンで一緒に作業する前に、接続を確立する必要があります。 この連携により、オーディエンスのアクティベーション、プロジェクトの作成、キャンペーンのパフォーマンスに関するレポートの実行が可能になります。

Collaborationでは、次の招待メソッドをサポートしています。

- [&#x200B; パブリック接続の招待](#discover-collaborators): **[!UICONTROL 共同作業者を見つける]** ワークスペースを介してライセンスを取得した別の顧客と接続します。
- [&#x200B; プライベート接続招待](#private-connection-invite)：接続コードを使用して、ライセンスを取得した別の顧客と直接接続します。
- [Starter invite](#invite-non-licensed-collaborator): ライセンスを持たない組織に接続します。
- [認証](/help/guide/connect/overview.md#advertiser-to-advertising-platform-connection): サポートされているサードパーティの広告プラットフォームに接続します。

選択したコラボレーションパターンに基づいて、接続が確立されます。 Collaborationでは、広告主とパブリッシャー間およびブランドとブランド間の2つの主要なコラボレーションパターンをサポートしています。 これらのパターンについて詳しくは、[&#x200B; ユースケース &#x200B;](/help/guide/overview/use-cases.md) ガイドを参照してください。

接続を確立する方法については、コラボレーションパターンに対応する以下の節を参照してください。

- [広告主とパブリッシャーの接続](#advertiser-to-publisher-connection)
- [ブランドとのつながり](#brand-to-brand-connection)

## 広告主とパブリッシャーの接続 {#advertiser-to-publisher-connection}

![広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

広告主とパブリッシャー間のパターンでは、広告主は&#x200B;**[!UICONTROL 共同作業者を見つける]** ワークスペースを通じて使用するパブリッシャーを見つけ、接続招待を送信します。 その後、パブリッシャーは招待を確認して受け入れ、広告主が接続設定を提案できるようにします。 パブリッシャーが接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトで共同作業を開始できます。

### 概要

広告主とパブリッシャー間の接続を確立するには、次の手順を実行します。

1. [Discover publishers](#discover-collaborators)：広告主は、協力する可能性のある共同作業者を特定します。
1. [招待を送信](#send-invite)：広告主は、選択した発行者に接続招待を送信します。
1. [招待を承認](#accept-invite)：発行者が招待をレビューし、承認します。
1. [接続設定の設定](#configure-connection-settings)：広告主は接続設定を設定し、レビューのためにパブリッシャーに送信します。
1. [接続設定を確認](#establish-connection)：発行者は接続設定を確認し、それを承認または拒否します。 受け入れたら、接続が確立されます。 拒否された場合、パブリッシャーは製品外のリビジョンに対するフィードバックを提供できます。 その後、広告主は設定を変更し、レビューのために再送信できます。

接続設定が承認されると、接続が確立され、共同作業者は[&#x200B; プロジェクトを作成](/help/guide/collaborate/manage-projects.md#create-project)してキャンペーンでの共同作業を開始する準備が整います。

## ブランドとのつながり {#brand-to-brand-connection}

![&#x200B; ブランド間の接続プロセスの概要ダイアグラム。](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}


## 接続 {#connect}

**[!UICONTROL Connect]** ワークスペースでは、共同作業者との接続を管理したり、接続招待を送信したり、広告主がパブリッシャーディレクトリを参照したりできます。 ワークスペースは、次の2つのメインタブに分かれています。

### 共同作業者を見つける {#discover-collaborators}

>[!IMPORTANT]
>
>広告主のみが、**[!UICONTROL 共同作業者を見つける]** ワークスペースを使用してパブリッシャーを発見できます。 共同作業者の役割に関係なく共同作業者とつながる方法については、[&#x200B; ブランド間の接続](#brand-to-brand-connection)の節を参照してください。

パブリッシャーを見つけるには、「**[!UICONTROL Connect]**」タブの「**[!UICONTROL 共同作業者を見つける]**」ワークスペースに移動します。 ここでは、ワークスペースの下部にあるページネーション コントロールを使用して、使用可能なパブリッシャーのリストを参照できます。 **[!UICONTROL 共同作業者を見つける]** ワークスペースについて詳しくは、[共同作業者を見つける](/help/guide/connect/discover-collaborators.md) ガイドを参照してください。

![使用可能な発行者のリストを表示する「共同作業者を検索」ワークスペース。](/help/assets/connect/establish-connection/discover-collaborators.png){zoomable="yes"}

### 招待状を送信 {#send-invite}

>[!IMPORTANT]
>
>この節では、広告主が&#x200B;**[!UICONTROL 共同作業者を見つける]** ワークスペースを介してメディア企業に接続招待を送信するプロセスについて説明します。 役割に関係なくブランド間の接続を形成する方法については、[&#x200B; ブランド間の接続](#brand-to-brand-connection) セクションを参照するか、[&#x200B; プライベート接続の招待](#private-connection-invite) セクションにアクセスしてください。

共同作業を行うパブリッシャーを特定したら、パブリッシャーカードの&#x200B;**[!UICONTROL Connect]** オプションを選択します。 このアクションにより、接続プロセスが開始されます。

![共同作業者を検索ワークスペースの特定のパブリッシャーでハイライト表示された接続オプション。](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

ダイアログが表示され、パブリッシャーに接続招待を送信するよう求められます。 「**[!UICONTROL 招待を送信]**」を選択して続行します。

![送信招待ボタンがハイライト表示された送信接続招待ダイアログ。](/help/assets/connect/establish-connection/send-connection-invite-dialog.png){zoomable="yes"}

>[!NOTE]
>
>製品外でコミュニケーションしたパブリッシャーと接続したい場合は、プライベート接続の招待オプションを利用できます。 詳しくは、「[&#x200B; プライベート接続への招待](#private-connection-invite)」の節を参照してください。

保留中の招待は、**[!UICONTROL 必要なアクション]** セクションの&#x200B;**[!UICONTROL 自分の接続]** タブに表示されます。 接続ステータスは&#x200B;**[!UICONTROL 招待状が送信されました]**&#x200B;と表示されます。 **[!UICONTROL 接続のプレビュー]**&#x200B;を選択して接続設定をプレビューできますが、パブリッシャーが招待を受け入れるまで編集することはできません。

![保留中の接続は、「アクションが必要」セクションの「自分の接続」ワークスペースに表示されます。](/help/assets/connect/establish-connection/preview-connection.png){zoomable="yes"}

### プライベート接続の招待 {#private-connection-invite}

プライベート接続の招待を使用すると、**[!UICONTROL Connect コード]**&#x200B;を使用して、製品外でコミュニケーションを行った共同作業者と接続できます。 プライベート接続を確立するには、製品外で接続する共同作業者から&#x200B;**[!UICONTROL 接続コード]**&#x200B;を取得する必要があります。 次に、このコードを使用して、**[!UICONTROL Connect]** ワークスペースの共同作業者にプライベート接続招待を送信できます。

#### 接続コード {#connect-code}

プライベート接続の招待を送信する前に、目的の共同作業者が一意の&#x200B;**[!UICONTROL 接続コード]**&#x200B;を提供する必要があります。 **[!UICONTROL Connect コード]**&#x200B;を検索してコピーするには、**[!UICONTROL セットアップ]** ワークスペース内の&#x200B;**[!UICONTROL マイアカウント]** タブに移動します。 **[!UICONTROL 接続コード]**&#x200B;は、アカウントの詳細に表示されます。

![接続コードがハイライト表示された設定ワークスペース内の「自分のアカウント」タブ。](/help/assets/connect/establish-connection/connect-code.png){zoomable="yes"}

コード **[!UICONTROL 接続]**&#x200B;の横にあるコピーアイコン（![&#x200B; コピーアイコン &#x200B;](/help/assets/icons/copy.png)）を選択して、クリップボードにコピーします。 その後、このコードを製品外の共同作業者と共有できます。

![&#x200B; コピーアイコンがハイライト表示された接続コード。](/help/assets/connect/establish-connection/copy-connect-code.png){zoomable="yes"}

##### 接続コードの更新 {#refresh-connect-code}

**[!UICONTROL Connect コード]**&#x200B;はいつでも更新できます。 コードを更新すると、共同作業者と共有できる新しい一意のコードが生成されます。 これは、セキュリティ上の理由から以前のコードを無効にする場合に便利です。 古いコードを使用して確立された接続は引き続きアクティブですが、新しい共同作業者は新しいコードを使用して接続する必要があります。

>[!IMPORTANT]
>
>保留中の招待中に&#x200B;**[!UICONTROL 接続コード]**&#x200B;を更新すると、招待が承認されない可能性があります。 コードを更新した場合、共同作業者は新しいコードを使用してプライベート接続招待を再送信する必要がある場合があります。

**[!UICONTROL Connect コード]**&#x200B;を更新するには、**[!UICONTROL Connect コード]**&#x200B;の横にある更新アイコン（![更新アイコン &#x200B;](/help/assets/icons/refresh.png)）を選択します。

![更新アイコンがハイライト表示された接続コード。](/help/assets/connect/establish-connection/refresh-connect-code.png){zoomable="yes"}

>[!IMPORTANT]
>
>**[!UICONTROL 接続コード]**&#x200B;機能が導入される前に作成されたアカウントには、生成された接続コードはなく、接続フィールドには&#x200B;**[!UICONTROL 使用できません]**&#x200B;と表示されます。 更新オプションを使用して、新しい接続コードを生成します。

#### プライベート接続の招待を送信 {#send-private-connection-invite}

共同作業者から&#x200B;**[!UICONTROL Connect コード]**&#x200B;を取得したら、プライベート接続の招待を送信できます。 これを行うには、**[!UICONTROL Connect]** ワークスペースに移動し、右上隅にあるプラスアイコン（![&#x200B; プラスアイコン &#x200B;](/help/assets/icons/plus.png)）を選択します。

次に、**[!UICONTROL 招待コードで接続]**&#x200B;を選択します。

![接続ワークスペースでプラス アイコンが強調表示されます。](/help/assets/connect/establish-connection/private-connection-invite.png){zoomable="yes"}

**[!UICONTROL Connect]** ダイアログが表示され、接続する共同作業者の&#x200B;**[!UICONTROL Connect コード]**&#x200B;を入力するよう求められます。 コードをテキストフィールドに貼り付け、**[!UICONTROL 続行]**&#x200B;を選択して続行します。

![接続コード フィールドが入力され、続行オプションがハイライト表示された接続ダイアログ。](/help/assets/connect/establish-connection/private-connection-invite-connect.png){zoomable="yes"}

次に、**[!UICONTROL Connect]** ダイアログに、コードが関連付けられている共同作業者が表示され、正しい共同作業者に接続していることを確認できます。 共同作業者が正しい場合は、**[!UICONTROL Connect]**&#x200B;を選択して、プライベート接続の招待を送信します。

![共同作業者の詳細が表示され、接続オプションが強調表示された接続ダイアログ。](/help/assets/connect/establish-connection/private-connection-invite-connect-confirm.png){zoomable="yes"}

### 招待状を承認 {#accept-invite}

>[!TIP]
>
>接続プロセスについて話し合う際に、**所有者**&#x200B;と&#x200B;**受信者**&#x200B;の間で区別が生じます。 所有者は、招待を送信して接続を開始する共同作業者で、受信者は、招待を受信してレビューする共同作業者です。

所有者が接続設定を設定する前に、受信者が接続招待を受け入れる必要があります。 これを行うには、**[!UICONTROL Connect]** ワークスペースに移動し、**[!UICONTROL 必要なアクション]** セクションで保留中の接続を見つけます。 接続ステータスは、**[!UICONTROL 招待を受信しました]**&#x200B;と表示されます。 招待を承諾するには、**[!UICONTROL 承諾]**&#x200B;を選択します。

![保留中の接続は、「同意」オプションが強調表示された状態で、ワークスペースを接続するアクションが必要なセクションに表示されます。](/help/assets/connect/establish-connection/accept-connection.png){zoomable="yes"}

招待を受け入れるよう促すダイアログが表示されます。 「**[!UICONTROL 招待を承諾]**」を選択して続行します。

![招待を承認オプションがハイライト表示された接続招待を承認ダイアログ。](/help/assets/connect/establish-connection/accept-connection-invite.png){zoomable="yes"}

接続のステータスが&#x200B;**[!UICONTROL 保留中]**&#x200B;に変更されます。 所有者は、接続設定を設定できるようになりました。

### 接続設定の設定 {#configure-connection-settings}

接続設定は、2人の共同作業者の条件を定義します。 これらの設定には、ユースケース、照合キー、クレジットの分割、法的契約書などが含まれます。 広告主と連携する共同作業者は、プロジェクトの作成時に使用する接続設定に広告主名を追加することもできます。

受信者が招待を受け入れた後、所有者は接続設定を設定できます。 これを行うには、**[!UICONTROL My connections]**&#x200B;に移動し、**[!UICONTROL Action required]** セクションで保留中の接続を見つけます。 **[!UICONTROL 接続を設定]**&#x200B;を選択して、接続設定を構成します。

![&#x200B; アクションが必要なセクションで「接続を設定」オプションがハイライト表示された接続ワークスペース。](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

接続設定ワークスペースが表示され、接続の様々な設定を行うことができます。

![接続設定ワークスペース。](/help/assets/connect/establish-connection/connection-set-up.png){zoomable="yes"}

#### 接続設定 {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="ユースケース"
>abstract="ユースケースには、すべてのオプションが事前入力されています。 接続設定を送信する前に、ユースケースを編集できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="一致キー"
>abstract="一致キーには、自身と共同作業者がアカウントレベルで選択した、共通の一致キーが事前入力されています。 この接続で使用しない一致キーは、オフに切り替えることができます。"
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
>abstract="アクティビティを実行して、キャンペーンのパフォーマンスレポートとインサイトを生成します。 クレジットは、すべてのキャンペーンのキャンペーンレポートの行数とレポートの頻度（毎日、3 日ごと、または週ごと）に基づいて消費されます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="広告主名"
>abstract="<p>オプションの設定。 発行者が認識している広告主の名前と ID を示します。</p><p>ここに追加する広告主名は、プロジェクトを作成ステップで事前入力されます。</p><ul><li>発行者が複数の名前を設定している場合は、リストから 1 つ選択します。</li><li>1 つの名前のみを設定する場合は、自動的に事前選択されます。</li><li>名前が設定されていない場合、このフィールドには、Collaboration の広告主アカウント名が事前入力されます。</li></ul>"
>additional-url="https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="プロジェクトの作成"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Audience Activation"
>abstract="Audience Activation を使用すると、Audience Activation を開始できる共同作業者を選択できます。"

次の接続設定を設定できます。

##### Audience Activation {#audience-activation}

>[!IMPORTANT]
>
>**[!UICONTROL オーディエンスアクティベーション]**&#x200B;機能が導入される前に作成された接続では、オーディエンスアクティベーション設定が自動的に接続所有者に設定されます。 両方の共同作業者がオーディエンスをアクティブ化できるようにするには、[現在の接続を削除し](#delete-connections)更新された設定で新しい接続を作成する必要があります。

オーディエンスアクティベーションを使用すると、接続内でオーディエンスをアクティベートできる共同作業者を選択できます。 オーディエンスアクティベーションは、**[!UICONTROL オーディエンスアクティベーション]**&#x200B;のユースケースが選択されている場合にのみオプションになります。 接続プロセス中にユースケースを削除することを選択した場合、オーディエンスアクティベーション設定は接続設定から削除されます。 オーディエンスのアクティベーションについて詳しくは、[activate](/help/guide/collaborate/activate.md) ガイドを参照してください。

オーディエンスのアクティブ化を設定するには、「**[!UICONTROL オーディエンスのアクティブ化]**」セクションで「**[!UICONTROL セットアップ]**」を選択します。 ドロップダウンメニューを使用して、オーディエンスをアクティベートできる共同作業者を指定します。 1人の共同作業者を選択するか、両方の共同作業者がオーディエンスをアクティブ化できるようにします。

![接続設定ワークスペースのオプションを含むオーディエンスアクティベーションダイアログ。](/help/assets/connect/establish-connection/audience-activation.png){zoomable="yes"}

完了したら、**[!UICONTROL 保存]**&#x200B;を選択して変更を保存します。

![接続設定ワークスペースの「保存」オプションを使用したオーディエンスのアクティブ化ダイアログ。](/help/assets/connect/establish-connection/audience-activation-confirm.png){zoomable="yes"}

##### ユースケース {#use-cases}

ユースケースには、使用可能なすべてのオプションが自動的に入力されます。 選択したユースケースによって、プロジェクト内で使用できるビューとオプションが決まります。 詳しくは、[&#x200B; プロジェクトのユースケース &#x200B;](/help/guide/collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。

ユースケースをカスタマイズするには、「**[!UICONTROL ユースケース]**」セクションで「**[!UICONTROL 編集]**」を選択し、共同作業者とのプロジェクトに含めたくない場合はオフにします。 完了したら、**[!UICONTROL 保存]**&#x200B;を選択して変更を保存します。

![接続設定ワークスペースのユースケース設定。](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

##### 一致キー {#match-keys}

>[!IMPORTANT]
>
>複数の照合キーを使用するオーディエンスをアクティブ化する場合、1つ（または複数）の照合キーに重複がないか、オーディエンスサイズがないか、しきい値を下回ると、アクティブ化全体が失敗します。 オーディエンスが十分に重複しており、すべてのマッチキーで最低1,000 IDのしきい値を満たしていることを確認してからアクティベートします。

[&#x200B; アカウントの設定](/help/guide/setup/onboard-account.md#set-up-match-keys)中に、あなたと共同作業者が選択した共通の照合キーが照合キーに自動的に入力されます。 自分と共同作業者が選択した&#x200B;**と**&#x200B;の両方に共通する一致するキーのみが表示されます。

![一致キーのセクションがハイライト表示された接続設定ワークスペースで、共通の一致キーが表示されます。](/help/assets/connect/establish-connection/auto-populated-match-keys.png){zoomable="yes"}

接続所有者が接続設定を設定している場合、アカウント一致キーを[編集して](../setup/onboard-account.md#edit-match-keys)追加の一致キーを含めることができます。 アカウント設定でさらに一致するキーを切り替えた後、それらの一致するキーは、共同作業者が選択している場合は、接続設定で切り替え可能になります。 接続プロセスが開始された後に追加された照合キーは自動的に入力されないため、手動でオンに切り替える必要があります。

照合キーをカスタマイズするには、**[!UICONTROL 照合キー]** セクションの&#x200B;**[!UICONTROL 編集]**&#x200B;を選択し、この接続で使用しない照合キーをすべてオフにします。 完了したら、**[!UICONTROL 保存]**&#x200B;を選択して変更を保存します。

![一致キーのセクション ダイアログが開き、一致キーがオフになっている接続設定ワークスペースが表示されます。](/help/assets/connect/establish-connection/additional-match-key-selected.png){zoomable="yes"}

>[!IMPORTANT]
>
>共同作業者が接続設定を受け入れると、一致キーがロックされ、変更できません。

##### クレジット分割 {#credit-split}

「クレジットの分割」セクションを使用して、2つの共同作業当事者のうち、活動のコストをカバーする当事者を決定します。 クレジット分割オプションは、接続で選択したユースケースによって決まります。 **[!UICONTROL Measurement]**&#x200B;のユースケースでは、コストをカバーするには1つの関係者が必要ですが、**[!UICONTROL Activation - Matching]**&#x200B;のユースケースでは、各関係者が独自のコストをカバーするように追加オプションが提供されます。 コストの内訳について詳しくは、[&#x200B; クレジットアクティビティタイプ &#x200B;](/help/guide/setup/my-activity.md#types-of-activities) ガイドを参照してください。

>[!NOTE]
>
>オーディエンス – エグレスは、オーディエンスを受信する共同作業者によって常にカバーされるため、選択は必要ありません。

クレジット分割を設定するには、「**[!UICONTROL クレジット分割]**」セクションの「**[!UICONTROL 編集]**」を選択します。 その後、各ユースケースに適切なオプションを選択できます。 完了したら、**[!UICONTROL 保存]**&#x200B;を選択して変更を保存します。

![接続設定ワークスペースのオプションを含むクレジット分割ダイアログ。](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}

##### 広告主名 {#advertiser-names}

>[!NOTE]
>
>このオプションは、接続を開始するユーザーに応じて、接続設定の設定または接続設定のレビュー中に表示される場合があります。

広告主との接続を形成するパブリッシャーの場合は、接続設定に広告主名を追加することを選択できます。 これにより、システムで広告主が認識される複数の名前を追加できます。 これは、広告主が複数の地域で事業を展開している場合や、異なるコンテクストで名称が異なる場合に特に役立ちます。 その後、プロジェクトを作成する際に、接続設定で設定した名前のリストから適切な広告主名を選択できます。

![接続設定ワークスペースの広告主名。](/help/assets/connect/establish-connection/advertiser-names.png){zoomable="yes"}

広告主名を追加するには、「**[!UICONTROL 広告主名]**」セクションで「**[!UICONTROL 編集]**」を選択します。 次に、広告主がシステム内で認識されている&#x200B;**[!UICONTROL 広告主ID]**&#x200B;と、Collaboration内でそのIDに関連付ける&#x200B;**[!UICONTROL 広告主名]**&#x200B;を入力できます。 **[!UICONTROL 追加]** オプションを選択して、複数の広告主名を追加できます。

![接続設定ワークスペースのオプションを含む広告主名ダイアログ。](/help/assets/connect/establish-connection/advertiser-names-dialog.png){zoomable="yes"}

完了したら、**[!UICONTROL 保存]**&#x200B;を選択して変更を保存します。

プロジェクトを作成する際には、接続中に設定された次の設定に基づいて広告主名が事前入力されます。

1. **広告主名セットなし**：広告主名が追加されない場合、Collaborationはデフォルトで広告主名を広告主名として使用します。
2. **1つの広告主名セット**:1つの広告主名が追加された場合、Collaborationはその名前を自動的にプロジェクトの広告主名として使用します。
3. **複数の広告主名セット**：複数の広告主名が追加された場合、プロジェクトの作成時に、指定された名前のいずれかを選択できます。

>[!NOTE]
>
> 接続設定を送信すると、広告主名を追加または編集できなくなります。

![広告主名セクションが入力された接続設定ワークスペース。](/help/assets/connect/establish-connection/add-advertiser-names.png)

選択した後、**[!UICONTROL 送信]**&#x200B;を選択して、レビュー用に提案された設定を受信者に送信します。

### 接続設定を確認 {#review-connection-settings}

次に、受信者は所有者が提案した接続設定を確認する必要があります。 受信者は、**[!UICONTROL Connect]** ワークスペースの「**[!UICONTROL 自分の接続]**」タブに移動して、これを行うことができます。 接続は、**[!UICONTROL アクションが必要]** セクションに表示されます。 **[!UICONTROL 接続設定を確認]**&#x200B;を選択して、提案された接続設定を確認します。

![接続設定を確認オプションがハイライト表示された自分の接続ワークスペース。](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

共同作業者が提案した設定を確認します。 接続設定を承認または拒否できます。 接続設定を拒否する場合は、製品外で行う変更について共同作業者に連絡する必要があります。 共同作業者の連絡先情報は、接続設定ワークスペースの&#x200B;**[!UICONTROL 連絡先]** セクションに表示されます。 その後、所有者は接続設定を変更し、レビュー用に再送信できます。

![同意と拒否オプションがハイライト表示された接続設定ワークスペース。](/help/assets/connect/establish-connection/accept-connection-settings.png){zoomable="yes"}

さらに、広告主と接続するパブリッシャーの場合は、接続設定に広告主名を追加できるようになりました。 このプロセスについて詳しくは、[接続設定](#connection-settings)の節を参照してください。

>[!NOTE]
>
> 接続設定を受け入れると、広告主名を追加または編集できなくなります。

次に、**[!UICONTROL 同意]**&#x200B;を選択して接続を続行します。 接続ステータスが&#x200B;**[!UICONTROL アクティブ]**&#x200B;に変更され、プロジェクトの共同作業を開始できるようになります。

## ライセンスのない共同作業者を招待（スターター） {#invite-non-licensed-collaborator}

ライセンスのないパートナーをReal-Time CDP Collaboration [!DNL Starter]に招待するには、次の手順に従います。 Collaboration [!DNL Starter]の詳細とプロセスの手順ごとの概要については、[[!DNL Starter] 概要ドキュメント &#x200B;](../overview/starter-overview.md)を参照してください。

招待プロセスを開始する前に、共同作業者から次の情報を収集します。

| フィールド | 説明 |
|-------|-------------|
| 会社 | 共同作業者の会社名。 |
| 名前 | 招待しているユーザーのフルネーム。 |
| 電子メールアドレス | 共同作業者がReal-Time CDP Collaboration [!DNL Starter]へのアクセスに使用する電子メールアドレス。 |
| タイトル | メインコンタクトの役職名。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>別の共同作業者を招待することで、その活動を通じて発生した料金に対して責任を負うことを認めます。 Collaboration Starter[&#128279;](../setup/starter-credit-usage.md)での クレジットの使用状況と使用状況について詳しく見る

### 招待状を送信 {#send-invitation}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_starter_invite_collaborator"
>title="共同作業者を招待"
>abstract="パートナー組織を Collaboration Starter に招待するには、このフォームに入力します。 招待者には招待メールが届きます。登録を完了するには、指定されたメールアドレスを使用する必要があります。"
>additional-url="https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/overview/starter-overview" text="詳しくは、Collaboration Starter を参照してください"

ユーザーインターフェイスを使用して、パートナー組織をCollaboration [!DNL Starter]に直接参加するように招待します。

開始するには、**[!UICONTROL Connect]** ワークスペースに移動し、右上隅にあるプラスアイコン（![&#x200B; プラスアイコン &#x200B;](/help/assets/icons/plus.png)）を選択します。 次に、**[!UICONTROL 共同作業者を招待]**&#x200B;を選択します。

![&#x200B; プラスアイコンと「共同作業者を招待」オプションがハイライト表示された接続ワークスペース。](/help/assets/connect/establish-connection/invite-collaborator/invite-collaborator.png){zoomable="yes"}

**[!UICONTROL 共同作業者を招待]** ダイアログが表示され、招待された共同作業者の情報を入力するよう求められます。 [!UICONTROL 会社名]、[!UICONTROL 名]、[!UICONTROL 姓]、[!UICONTROL 電子メール &#x200B;]の必須フィールドに入力します。

>[!IMPORTANT]
>
>招待状は&#x200B;**指定された電子メールアドレスに関連付けられています**。 招待されたユーザーが招待に同意して製品にアクセスするには、その正確な電子メールを使用する必要があるため、電子メールアドレスが正確であることを確認します。

次に、ドロップダウンを使用して、パートナーに適した役割を選択します。 Collaborationで使用可能なロールの種類について詳しくは、[&#x200B; アカウントのロールに関するドキュメント &#x200B;](../overview/roles.md)を参照してください。

![役割ドロップダウンがハイライト表示された「共同作業者を招待」ダイアログ。](/help/assets/connect/establish-connection/invite-collaborator/role-dropdown.png){zoomable="yes"}

完了したら、情報を確認し、**[!UICONTROL 招待を送信]**&#x200B;を選択します。

![招待オプションがハイライト表示された「共同作業者を招待」ダイアログ。](/help/assets/connect/establish-connection/invite-collaborator/send-invite.png){zoomable="yes"}

招待がパートナー組織に正常に送信されたことを確認する確認ダイアログが表示されます。

![確認ダイアログで、招待が正常に送信されたことを確認します。](/help/assets/connect/establish-connection/invite-collaborator/invite-sent-confirmation.png){zoomable="yes"}

### 招待に同意して条件に署名 {#accept-invitation-sign-terms}

招待状を送信すると、パートナー組織に、Adobe Real-Time Collaborationの利用条件を確認して同意するための手順が記載されたメールが届きます。 また、同意する前にCollaborationの機能を確認することもできます。

![Collaboration Starterへの招待メール。](/help/assets/connect/establish-connection/invite-collaborator/invitation-email.png){zoomable="yes"}

パートナー組織が利用条件に同意すると、AdobeはアカウントのReal-Time CDP Collaboration [!DNL Starter]のプロビジョニングを開始します。

### プロビジョニングの確認 {#provisioning-confirmation}

プロビジョニングプロセスが完了すると、招待された組織にウェルカムメールが送信され、Collaboration [!DNL Starter]を使用する準備ができていることを確認します。 このメールでは、次の方法について説明します。

- [管理者とユーザーアクセス権の設定](../setup/starter-admin-access.md)
- [Collaborationにアクセスする権限を設定する](../setup/starter-permission-controls.md)

![招待された組織に、必要なアクセスと権限を設定する手順が記載されたウェルカムメールが送信されました。](/help/assets/connect/establish-connection/invite-collaborator/welcome-email.png){zoomable="yes" width="700"}

パートナーがCollaborationにアクセスできるようになると、自分と招待された組織の両方が[接続を確立](#connect)し、[接続設定を設定](#configure-connection-settings)して、プロジェクトでの共同作業を開始できます。

## 次の手順

共同作業者との接続を確立すると、共同作業者と共同作業者は[&#x200B; プロジェクトを作成できるようになりました](/help/guide/collaborate/manage-projects.md#create-project)。
