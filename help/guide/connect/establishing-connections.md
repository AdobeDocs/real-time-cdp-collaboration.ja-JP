---
title: 広告主またはパブリッシャーとの接続
description: 潜在的な共同作業者を見つけた後、連携を確立し、プロジェクトでの共同作業を開始する方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3fed93f7-1854-440c-802e-6b47e82918c9
source-git-commit: e0894fb3cb290334e0e95d5c26288705967d9dbe
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 16%

---

# 広告主またはパブリッシャーとの接続

{{limited-availability-release-note}}

Real-Time CDP Collaborationでは、キャンペーンに取り組む企業にとって、共同作業の 2 つの当事者間（通常は広告主とパブリッシャー）をつなぐことが前提条件です。 パブリッシャーと広告主は同様に、接続を設定できます。 接続を開始したパーティは誰でも、後で *接続所有者* になります。

## ワークフローの概要

大まかに言えば、広告主とパブリッシャーの間の接続を確立するために、ワークフローは次のようになります。

1. 広告主 [ パブリッシャーを閲覧して ](/help/guide/connect/discover-publishers.md) 連携したいパブリッシャーを見つけます
2. 広告主が接続招待を送信します。
3. パブリッシャーが招待を受け入れます。
4. 広告主は、一致キーなどを含む接続設定を送信します。 これらの接続設定は、共同作業に関する製品内の用語を表します。
5. パブリッシャーは接続設定を受け入れます。 必要に応じて、パブリッシャーは最初の接続設定を拒否し、広告主に変更した接続設定の送信をリクエストできます。

![ 広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-connection-process.png){zoomable="yes"}

上記の項目が完了したら、共同作業者は [ プロジェクトの作成 ](/help/guide/collaborate/manage-projects.md#create-project) に進み、[ 重複レポートの実行 ](/help/guide/collaborate/discover.md) 広告キャンペーンを開始できます。

>[!IMPORTANT]
>
>2 人の共同作業者の間の接続が確立されると、接続設定は変更できなくなります。

## 招待状を送信 {#send-invite}

接続を設定するには、パブリッシャーの検出画面でパブリッシャーインベントリを参照する際に「**[!UICONTROL 接続]**」を選択します。

![ 接続セレクター ](/help/assets/connect/establish-connection/connect-selection.png){zoomable="yes"}

この時点で、招待は送信されており、接続設定をプレビューできますが、編集することはできません。 保留中の招待は、「**[!UICONTROL マイ接続]**」タブで確認できます。 接続のステータスは **[!UICONTROL 招待状が送信されました]** です。

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
>abstract="このセクションでは、Real-Time CDP 共同作業内の対応するアクティビティに対して支払いを行うユーザーを決定します。現在、オーディエンス共有のユースケースのみが設定可能です。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_audiencesharing"
>title="オーディエンス共有"
>abstract="オーディエンス共有は、一致したデータを共同作業パートナーにアクティブ化するようにリクエストする際にパーティが実行するアクティビティです。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_creditsplit_measurement"
>title="測定"
>abstract="このユースケースでは、Real-Time CDP 共同作業でアクティビティを実行し、キャンペーンパフォーマンスレポートとインサイトを生成できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_legalagreement"
>title="法的契約"
>abstract="2 つのパーティ間にデータ共有契約が存在することを確認します。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_connection_settings_advertisername"
>title="広告主名"
>abstract="発行者が認識している広告主のエイリアスを示します。 "

招待状が送信されると、接続設定をプレビューできます。 接続の設定を完了するには、招待を承諾する必要があります。

![ プレビュー状態の接続設定ビュー ](/help/assets/connect/establish-connection/preview-connection-settings.png){zoomable="yes"}

共同作業者が接続を承認したら、接続の接続設定のセットアップを開始できます。 接続設定は、共同作業の条件（一緒に行うユースケース、プロジェクトで使用する一致キーなど）を定義します。

接続設定を設定して共同作業者と共有するには、[ マイ接続 **[!UICONTROL に移動し]** す。 ステータスが **[!UICONTROL 保留中]** の接続については、「**[!UICONTROL 接続を設定]**」を選択して接続設定を構成できます。

![ 保留中の接続と「接続を設定」オプションがハイライト表示されたマイ接続ビュー ](/help/assets/connect/establish-connection/pending-connection.png){zoomable="yes"}

以下のフィールドを編集し、定義できます。

![ 接続ビューの設定 ](/help/assets/connect/establish-connection/connection-view.png){zoomable="yes"}

+++ユースケース

ユースケースには、使用可能なすべてのユースケースが事前に入力されています。 接続で使用するユースケースを選択するには、「**[!UICONTROL 編集]** を選択し、不要なユースケースはオフにします。 選択したユースケースは、どのビューやオプションを [ プロジェクト内で使用できるか ](../collaborate/manage-projects.md#project-use-cases) に影響します。

![使用例](/help/assets/connect/establish-connection/view-use-cases.png){zoomable="yes"}

+++

+++一致キー

一致キーには、（組織レベルで選択した [ ユーザーが事前入力され ](/help/guide/setup/onboard-organization.md#set-up-match-keys) す。 この接続で使用しない一致キーをオフに切り替えることができますが、組織の設定時に選択されなかった一致キーは追加できません。

![ 一致キー ](/help/assets/connect/establish-connection/match-keys.png)

+++

+++与信分割

「クレジット分割」セクションを使用して、共同作業している 2 つの関係者のうち、アクティビティのコストを負担するのはどれかを決定します。

![ 与信分割 ](/help/assets/connect/establish-connection/edit-billing-ownership.png)

+++

+++協定

この接続を続行する前に、2 者間のデータ共有契約が存在することを確認する必要があります。

![ 法的合意 ](/help/assets/connect/establish-connection/legal-agreement.png)

+++

選択を完了したら、「**[!UICONTROL 送信]**」を選択して、提案された設定をレビュー用に共同作業者に送信します。

共同作業者から提案された接続設定を受け取っている場合は、それらの設定を **[!UICONTROL 承認]** または **[!UICONTROL 拒否]** できます。 接続設定を受け入れる前に、共同作業者との間で法的合意が締結されていることを確認する必要があります。 接続設定を拒否する場合は、製品外の共同作業者に連絡して、接続設定をどのように変更して受け入れるべきかについて話し合ってください。

## 接続の削除 {#delete-connections}

引き続き使用しない、共同作業者との接続を削除できます。 既存の接続を削除するには：

1. **[!UICONTROL 接続]**/**[!UICONTROL マイ接続]** に移動します。
2. 接続カードで **[!UICONTROL 接続を表示]** を選択し、削除する接続にアクセスします。
3. 削除アイコン ![ 削除アイコン ](/help/assets/common/delete.svg) を選択して、接続削除確認ダイアログを表示します。
   ![ ハイライト表示された「接続を削除」アイコン ](/help/assets/connect/establish-connection/delete-icon-highlighted.png){zoomable="yes"}
4. 「**[!UICONTROL 削除]**」を選択して削除を確認します。
   ![ 接続の削除を確認するダイアログ。](/help/assets/connect/establish-connection/delete-connection-dialog.png){zoomable="yes"}

>[!WARNING]
>
>接続が削除されると、コラボレータとの接続は解除され、コラボレーションに含まれる既存のプロジェクトはすべて完全に削除されてリカバリできなくなります。

## 次の手順

共同作業者との接続を確立すると、共同作業者と [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) できるようになります。
