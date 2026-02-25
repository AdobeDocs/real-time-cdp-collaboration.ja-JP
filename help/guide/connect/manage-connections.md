---
title: 接続の管理
description: Real-Time CDP Collaborationでの接続の管理方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
source-git-commit: 46d2596bd0ccdc5da32067493968945c61f8acc4
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 1%

---

# 接続の管理 {#manage-connections}

{{limited-availability-release-note}}

**[!UICONTROL マイ接続]** ワークスペースは、接続を一元的に管理するための場所となります。 「**[!UICONTROL 既存の接続]**」セクションでは既存の接続を確認でき、「**[!UICONTROL 必要なアクション]**」セクションではアクションが必要な接続を確認できます。

## 接続を表示 {#view-connection}

既存の接続を表示するには、**[!UICONTROL 接続]** ワークスペースに移動します。 パブリッシャーには、既存の接続が表示されます。 広告主の場合は、「マイ連携 **[!UICONTROL に移動する必要があ]** ます。

![&#x200B; マイ接続ワークスペースの接続でハイライト表示された「接続を表示」オプション &#x200B;](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

接続の概要ワークスペースが表示され、接続とそのアクティブなプロジェクトに関する詳細が表示されます。 **[!UICONTROL 接続設定]** を選択して、接続設定を表示します。

![&#x200B; 接続の概要ワークスペースでハイライト表示された「接続設定」オプション &#x200B;](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

接続設定ワークスペースが表示され、ユーザーと共同作業者の間の接続の詳細が表示されます。 ここでは、接続プロセス中に選択したすべての設定、接続の現在のステータス、接続所有者、共同作業者の連絡先情報を表示できます。 特定の接続設定について詳しくは、[&#x200B; 接続設定 &#x200B;](/help/guide/connect/establishing-connections.md#connection-settings) ガイドを参照してください。

![&#x200B; 接続の詳細が表示されている接続設定ワークスペース。](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## 接続を削除 {#delete-connection}

引き続き使用しない、共同作業者との接続を削除できます。 接続を削除するには、削除する接続に移動し、接続ワークスペースで削除アイコン ![&#x200B; 削除アイコン &#x200B;](/help/assets/common/delete.svg) を選択します。

![&#x200B; 接続ワークスペースでハイライト表示された削除アイコン。](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

接続の削除を確認する確認ダイアログが表示されます。 「**[!UICONTROL 削除]**」を選択して、削除を確定します。

![&#x200B; 接続を削除するための確認ダイアログ。](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>接続が削除されると、コラボレーション内の既存のプロジェクトはすべて完全に削除され、復元できなくなります。 接続リクエストは、「マイ接続 **[!UICONTROL 内の「]** アクションが必要 **[!UICONTROL 」セクション内で保留状態のままになりますが、接続とその設定はアクティブ]** なくなります。 共同作業者と再度接続する場合は、接続を再確立する必要があります。

## 接続を編集 {#edit-connection}

コラボレーション接続の所有者は、接続が確立された後に、コラボレータとの接続設定を編集できます。 実行できる操作は、次のとおりです。

* ユースケースを追加
* 一致キーを追加します。 一致キーの削除は今後サポートされる予定です。
* Audience Activation 権限の更新
* 与信分割設定の更新

>[!IMPORTANT]
>
>ユースケースまたは一致キーを接続に追加すると、削除できなくなります。

>[!TIP]
>
>**所有者** は、招待を **受信者** に送信して接続を開始する共同作業者です。 詳しくは、[&#x200B; 共同作業者との接続の確立 &#x200B;](./establishing-connections.md) ドキュメントを参照してください。

接続設定を編集するには、接続設定ワークスペースに移動します。 3 つのドット アイコン（![3 つのドット アイコン](/help/assets/icons/more.png)）を選択して使用可能なアクションを表示し、**[!UICONTROL 編集]** を選択します。

![&#x200B; 「編集」オプションがハイライト表示された接続設定ワークスペース。](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

共同作業者レビュー用の設定変更を編集して送信するように促すダイアログが表示されます。 「**[!UICONTROL 編集]**」を選択します。

![&#x200B; 「編集」オプションがハイライト表示された接続設定を編集ダイアログ &#x200B;](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### Audience Activation を編集 {#edit-audience-activation}

Audience Activation 設定は、宛先に対してオーディエンスをアクティブ化できる接続内の共同作業者を決定します。 これらの設定を変更するには、「**[!UICONTROL オーディエンスのアクティベーション]** セクション内の **[!UICONTROL 編集]** を選択します。

![Audience Activation セクションと「編集」オプションを表示する接続設定を編集画面。](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

**[!UICONTROL Audience Activation]** ダイアログで、ドロップダウンメニューを使用して、Audience Activation 権限を更新します。 1 人の共同作業者を選択することも、両方の共同作業者がオーディエンスをアクティブ化できるようにすることもできます。

![Audience Activation ダイアログのハイライト表示のドロップダウンメニューが展開され、Audience Activation 権限を更新できるようになりました。](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

終了したら、「**[!UICONTROL 保存]**」を選択します。

![&#x200B; 新しい Audience Activation 権限と「保存」オプションを表示する Audience Activation ダイアログ &#x200B;](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### ユースケースを追加 {#add-use-cases}

Collaborationでは、検出、アクティブ化、測定などのユースケースによって、共同作業者と使用できるプロジェクトセクションおよび機能が決まります。 今後のプロジェクトで、既存の接続にユースケースを追加できます。 詳しくは、[&#x200B; 共同作業のユースケース &#x200B;](../overview/use-cases.md) を参照してください。

**[!UICONTROL 新しいユースケースを追加するには、「ユースケース]** セクションの **[!UICONTROL 編集]** を選択します。

![&#x200B; 「ユースケース」セクションと「編集」オプションがハイライト表示された接続設定編集画面 &#x200B;](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

**[!UICONTROL ユースケース]** ダイアログで、追加する新しいユースケースをオンに切り替え、次に **[!UICONTROL 保存]** をクリックします。

![&#x200B; 「保存」オプションがハイライト表示されているユースケースダイアログ &#x200B;](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>「Audience Activation[&#x200B; や「測定」など、「新しいユースケースを追加 &#x200B;](#add-use-cases) する場合、接続設定を編集画面が更新され、「Audience Activation **&#x200B;**&#x200B;セクションと **[!UICONTROL クレジット分割]** セクションが含まれます。 これらの新しいユースケースに適切な設定を行う必要があります。 詳しくは、[Audience Activation](../connect/establishing-connections.md#audience-activation) および [&#x200B; クレジット分割 &#x200B;](../connect/establishing-connections.md#credit-split) ガイドを参照してください。
>
>![&#x200B; 新しいユースケースが追加された後、Audience Activation およびクレジット分割のセクションが表示された接続設定編集画面。](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### 一致キーを追加 {#add-match-keys}

アカウントで設定され、共同作業者によって選択された一致キーのみが接続に使用できます。 [&#x200B; アカウントに新しい一致キーを追加 &#x200B;](../setup/onboard-account.md#edit-match-keys) し、共同作業者も同じキーを選択したら、既存の接続内でそれらを有効にすることができます。

接続設定を編集画面の **[!UICONTROL キーの一致]** セクション内の **[!UICONTROL 編集]** を選択します。

![&#x200B; 「キーを一致させる」セクションと「編集」オプションがハイライト表示された接続設定編集画面 &#x200B;](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

**[!UICONTROL 一致キー]** ダイアログが表示され、接続用に設定された既存の一致キーが表示されます。 追加する一致キーを選択し、続けて **[!UICONTROL 保存]** を選択します。

![&#x200B; 選択した新しいマッチ キーと [ 保存 ] オプションが表示されている [ マッチ キー ] ダイアログ ボックス &#x200B;](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### クレジット分割を編集 {#edit-credit-split}

クレジット分割設定では、接続内の各ユースケースに関連付けられたコストを担当する共同作業者を指定します。 これらの設定を更新するには、「**[!UICONTROL クレジット分割]** セクションの **[!UICONTROL 編集]** を選択します。

![&#x200B; 「クレジット分割」セクションと「編集」オプションがハイライト表示された接続設定編集画面 &#x200B;](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

**[!UICONTROL クレジット分割]** ダイアログで、[!UICONTROL &#x200B; アクティベーションの照合 &#x200B;] および [!UICONTROL &#x200B; 測定 &#x200B;] の優先設定を選択します。 次に、「**[!UICONTROL 保存]**」を選択して確定します。

![&#x200B; 与信分割設定と「保存」オプションを表示する与信分割ダイアログ &#x200B;](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### 変更を確認して送信 {#review-and-submit-changes}

接続設定の編集が完了したら、「変更を送信 **[!UICONTROL を確認して選択]** ます。 接続設定の更新は共同作業者に送信され、レビューされます。

![&#x200B; 更新プログラムと「変更を送信」オプションを表示する接続設定を編集画面 &#x200B;](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### 接続設定の変更をドラフトとして保存

接続設定の変更をドラフトとして保存し、いつでも接続設定の更新を完了するために戻ることができます。

変更をドラフトとして保存するには、「**[!UICONTROL 変更を送信]** の横にある「**[!UICONTROL キャンセル]** を選択します。 次に、「**[!UICONTROL 未送信の変更]** ダイアログで、「**[!UICONTROL 後で続行]**」を選択して確定します。

![&#x200B; 接続設定を編集画面 &#x200B;](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

変更内容がドラフトとして保存されました。 接続設定ワークスペースには、未送信の変更があることを示す通知が表示されます。 さらに更新するには、「**[!UICONTROL 編集を続行]**」を選択します。

![&#x200B; レビューおよび送信待ちの未送信の変更があることを示す、接続設定ワークスペースの通知。](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
