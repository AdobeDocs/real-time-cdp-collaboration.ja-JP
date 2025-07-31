---
title: 広告主またはパブリッシャーとの接続
description: 潜在的な共同作業者を見つけた後、連携を確立し、プロジェクトでの共同作業を開始する方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '1400'
ht-degree: 16%

---

# 広告主またはパブリッシャーとの接続

{{limited-availability-release-note}}

コラボレーターがキャンペーンで連携する前に、連携を確立する必要があります。 この接続を使用すると、オーディエンスのアクティブ化、プロジェクトの作成およびキャンペーンのパフォーマンスに関するレポートの実行を行うことができます。

## ワークフローの概要

広告主とパブリッシャーの間の接続を確立するには、次の手順が必要です。

1. 広告主は [ パブリッシャーを閲覧して ](/help/guide/connect/discover-publishers.md) 連携したいパブリッシャーを検出します。
2. 広告主が接続招待を送信します。
3. パブリッシャーが招待を受け入れます。
4. 広告主は、一致キーなどを含む接続設定を送信します。 これらの接続設定は、共同作業に関する製品内の用語を表します。
5. パブリッシャーは接続設定を受け入れます。 必要に応じて、パブリッシャーは最初の接続設定を拒否し、広告主に変更した接続設定の送信をリクエストできます。

![ 広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

上記の項目が完了したら、共同作業者は [ プロジェクトの作成 ](/help/guide/collaborate/manage-projects.md#create-project) に進み、[ 重複レポートの実行 ](/help/guide/collaborate/discover.md) 広告キャンペーンを開始できます。

>[!IMPORTANT]
>
>2 人の共同作業者の間の接続が確立されると、接続設定は変更できません。

## 招待状を送信 {#send-invite}

接続を設定するには、「**[!UICONTROL パブリッシャーを検出]** ワークスペースでパブリッシャーインベントリを参照する際に **[!UICONTROL 接続]** を選択します。

![ 特定のパブリッシャーで「接続」オプションがハイライト表示された接続ダッシュボード。](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

招待状を送信すると、接続設定をプレビューできます（編集はできません）。 保留中の招待を表示は、「**[!UICONTROL マイ接続]** タブに表示されます。 接続ステータスは **[!UICONTROL 招待状が送信されました]** と表示されます。

![ 公開者に送信された保留中の招待状がマイ接続ビューに表示されます。](/help/assets/connect/establish-connection/pending-invite-sent.png){zoomable="yes"}

共同作業者が招待を受け入れると、接続設定を構成し、それらを共同作業者に送信して、確認して同意できます。

## 接続設定 {#connection-settings}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_usecases"
>title="ユースケース"
>abstract="ユースケースには、すべてのオプションが事前入力されています。接続設定を送信する前に、ユースケースを編集できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_matchkeys"
>title="一致キー"
>abstract="一致キーには、組織レベルで選択したキーが事前入力されています。この接続で使用しない一致キーは、オフに切り替えることができます。"

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
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="法的契約"
>abstract="2 つのパーティ間にデータ共有契約が存在することを確認します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="広告主名"
>abstract="<p>オプションの設定。発行者が認識している広告主の名前と ID を示します。</p><p>ここに追加する広告主名は、プロジェクトを作成ステップで事前入力されます。</p><ul><li>発行者が複数の名前を設定している場合は、リストから 1 つ選択します。</li><li>1 つの名前のみを設定する場合は、自動的に事前選択されます。</li><li>名前が設定されていない場合、このフィールドには、Collaboration の広告主アカウント名が事前入力されます。</li></ul>"
>additional-url="https://experienceleague.adobe.com/ja/docs/real-time-cdp-collaboration/using/collaborate/manage-projects#create-project" text="プロジェクトの作成"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_audience_activation"
>title="Audience Activation"
>abstract="Audience Activation を使用すると、Audience Activation を開始できる共同作業者を選択できます。"

<!-- Move and update the above popover when bidirectional is active. -->

招待状が送信されると、接続設定をプレビューできます。 接続の設定を完了するには、招待を承諾する必要があります。

![ プレビュー状態の接続設定ビュー ](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

<!-- The sections below will be updated in B2B and have not been addressed yet. -->

### 広告主接続設定 {#advertiser-connection-settings}

共同作業者が接続を受け入れたら、接続設定を設定します。 これらの設定は、作業のユースケース、プロジェクトの一致キー、その他の設定など、共同作業に関する用語を定義します。

開始するには、「マイ接続 **[!UICONTROL に移動し]** す。 ステータスが **[!UICONTROL 保留中]** の接続については、「**[!UICONTROL 接続を設定]**」を選択して接続設定を構成できます。

![ 保留中の接続と「接続を設定」オプションがハイライト表示されたマイ接続ワークスペース ](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

以下のフィールドを編集し、定義できます。

![ 入力する前の接続設定ワークスペース。](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++ユースケース

ユースケースには、使用可能なすべてのオプションが事前入力されています。 これらをカスタマイズするには、「**[!UICONTROL ユースケース]**」セクションで **[!UICONTROL 編集]** を選択し、不要な場合はオフにします。 選択したユースケースによって、（プロジェクト内で使用可能な [ ビューとオプションが決 ](../collaborate/manage-projects.md#project-use-cases) ります。

![ 接続設定ワークスペースのユースケース設定 ](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++一致キー

一致キーには、（組織の設定 [ 時に選択したキーが事前に入力されて ](/help/guide/setup/onboard-account.md#set-up-match-keys) ます。 使用しない一致キーはオフにできますが、組織の設定時に選択されなかった一致キーは追加できません。

![ 接続設定ワークスペースの「キーを一致」設定 ](/help/assets/connect/establish-connection/match-keys.png){zoomable="yes"}

+++

+++与信分割

「クレジット分割」セクションを使用して、共同作業している 2 つの関係者のうち、アクティビティのコストを負担するのはどれかを決定します。 クレジット分割オプションは、接続に対して選択したユースケースによって決定されます。 **[!UICONTROL 測定]** のユースケースではコストをカバーするために一方のパーティが必要ですが、**[!UICONTROL アクティベーション – マッチング]** のユースケースでは、追加のオプションとして各パーティに独自のコストをカバーさせることができます。 コストの内訳について詳しくは、[ クレジットアクティビティタイプ ](/help/guide/setup/my-activity.md#types-of-activities) ガイドを参照してください。

>[!NOTE]
>
>オーディエンス – 出力は、常にオーディエンスを受け取る共同作業者によってカバーされるので、選択は必要ありません。

![ 接続ワークスペースにオプションが表示されたクレジット分割ダイアログ ](/help/assets/connect/establish-connection/credit-split.png){zoomable="yes"}
+++

+++協定

この接続を続行する前に、2 者間のデータ共有契約が存在することを確認する必要があります。

![ 法的契約セクションがハイライト表示され、接続ワークスペースで確認されています。](/help/assets/connect/establish-connection/legal-agreement.png){zoomable="yes"}

+++

選択が完了したら、「**[!UICONTROL 送信]**」を選択して、提案された設定をレビュー用に共同作業者に送信します。

### Publisher 接続設定 {#publisher-connection-settings}

パブリッシャーは、接続設定を確認し、設定を承認または拒否する必要があります。 接続設定を確認するには、**[!UICONTROL マイ接続]** に移動し、接続カードで **[!UICONTROL 接続設定を確認]** を選択します。

![ マイ接続ビューでハイライト表示された「接続設定を確認」オプション ](/help/assets/connect/establish-connection/review-connection-settings.png){zoomable="yes"}

共同作業者が提案した設定を確認します。 接続設定を受け入れる前に、自分と共同作業者の間に法的合意が締結されていることを確認する必要があります。 さらに、システム内で広告主が知られている任意の広告主名を追加できます。

![ 共同作業者から提案された設定と、「広告主名」セクションおよび「契約書」セクションがハイライト表示された接続設定ワークスペース。](/help/assets/connect/establish-connection/publisher-connection-settings.png){zoomable="yes"}

+++広告主名

接続設定に取り組むパブリッシャーとして、システム内で広告主が知られている広告主名を追加することを選択できます。 パブリッシャーは、複数の地域に所属する広告主がいる場合など、複数の広告主名を接続に追加できます。 プロセスの後半で、共同作業を行う [ プロジェクトを作成する ](/help/guide/collaborate/manage-projects.md#create-project) 際に、自分または共同作業者が、プロジェクトに関連付ける広告主名を選択できるようになります。

![ 接続設定ワークスペースの広告主名ダイアログ ](/help/assets/connect/establish-connection/add-advertiser-names-modal.png)

プロジェクト作成時の広告主名の選択の仕組みを次に示します。

1. **広告主名を設定しない**：広告主名を追加しない場合、Real-Time CDP Collaborationではデフォルトで広告主名が使用されます。
2. **1 つの広告主名セット**:1 つの広告主名が追加された場合、Real-Time CDP Collaborationはその名前をプロジェクトの広告主名として自動的に使用します。
3. **複数の広告主名を設定**：複数の広告主名を追加した場合、ユーザーまたは共同作業者は、プロジェクトの作成時に、指定された名前のいずれかを選択できます。

![ 「広告主名」セクションに値が入力された接続設定ワークスペース ](/help/assets/connect/establish-connection/advertiser-names.png)

+++

>[!NOTE]
>
> 接続設定を承認すると、広告主名を追加または編集できなくなります。

提案された接続設定に問題がない場合は、「**[!UICONTROL 確定]**」を選択して接続を確立します。 接続設定の変更を要求する場合は、「**[!UICONTROL 拒否]**」を選択します。 その後、共同作業者は接続設定を修正し、レビュー用に再送信できます。

<!-- The end of the sections needing updates still. -->

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
>接続が削除されると、コラボレータとの接続は解除され、コラボレーションに含まれる既存のプロジェクトはすべて完全に削除されてリカバリできなくなります。

## 次の手順

共同作業者との接続を確立すると、共同作業者と [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) できるようになります。
