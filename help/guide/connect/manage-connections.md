---
title: 接続の管理
description: Real-Time CDP Collaborationで接続を管理する方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 50120839-4a20-4ec1-8887-9342bd17c52d
TQID: https://experienceleague.adobe.com/plolWAj37G7hiH7gMYxDwJJDVXAIfMhSQHPRypErbxw
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 1092
ht-degree: 1%

---

# 接続の管理 {#manage-connections}

{{limited-availability-release-note}}

**[!UICONTROL My connections]** ワークスペースは、接続を管理するための一元的な場所を提供します。 **[!UICONTROL 既存の接続]** セクションで既存の接続を表示し、**[!UICONTROL 必要なアクション]** セクションでアクションを必要とする接続を確認できます。

## 接続を表示 {#view-connection}

既存の接続を表示するには、**[!UICONTROL Connect]** ワークスペースに移動します。 パブリッシャーとして、既存の接続が表示されます。 広告主は、**[!UICONTROL My connections]**&#x200B;に移動する必要があります。

![接続を表示オプションが、自分の接続ワークスペースの接続に対して強調表示されます。](/help/assets/connect/manage-connections/view-connection.png){zoomable="yes"}

接続の概要ワークスペースが表示され、接続とそのアクティブなプロジェクトに関する詳細が表示されます。 接続設定を表示するには、**[!UICONTROL 接続設定]**&#x200B;を選択します。

![接続概要ワークスペースでハイライト表示された接続設定オプション。](/help/assets/connect/manage-connections/connection-overview.png){zoomable="yes"}

接続設定ワークスペースが表示され、ユーザーと共同作業者の間の接続の詳細が表示されます。 ここでは、接続プロセス中に選択したすべての設定、接続の現在のステータス、接続所有者、共同作業者の連絡先情報を表示できます。 特定の接続設定について詳しくは、[接続設定](/help/guide/connect/establishing-connections.md#connection-settings) ガイドを参照してください。

![接続の詳細を表示する接続設定ワークスペース。](/help/assets/connect/manage-connections/connection-settings.png){zoomable="yes"}

## 接続を削除 {#delete-connection}

共同作業者との関係を削除して、作業を続行しないようにすることができます。 接続を削除するには、削除する接続に移動し、接続ワークスペースで削除アイコン ![削除アイコン ](/help/assets/common/delete.svg)を選択します。

![接続ワークスペースで削除アイコンが強調表示されます。](/help/assets/connect/establish-connection/delete-option.png){zoomable="yes"}

接続の削除を確認する確認ダイアログが表示されます。 「**[!UICONTROL 削除]**」を選択して、削除を確認します。

![接続を削除するための確認ダイアログ。](/help/assets/connect/establish-connection/delete-confirmation-dialog.png){zoomable="yes"}

>[!WARNING]
>
>接続が削除されると、コラボレーション内の既存のすべてのプロジェクトが完全に削除され、復元できなくなります。 接続リクエストは、**[!UICONTROL My connections]**&#x200B;内の&#x200B;**[!UICONTROL Action required]** セクション内の保留状態のままですが、接続とその設定はアクティブではなくなります。 共同作業者と再び接続するには、接続を再確立する必要があります。

## 接続を編集 {#edit-connection}

コラボレーション接続の所有者は、接続が確立された後、共同作業者との接続設定を編集できます。 実行できる操作は、次のとおりです。

* ユースケースを追加
* 一致キーを追加します。 今後、一致するキーの削除がサポートされます。
* オーディエンスアクティベーション権限の更新
* クレジット分割設定の更新

>[!IMPORTANT]
>
>ユースケースまたは一致キーを接続に追加すると、削除できません。

>[!TIP]
>
>**所有者**&#x200B;は、招待を&#x200B;**受信者**&#x200B;に送信して接続を開始する共同作業者です。 詳しくは、[共同作業者との接続の確立に関するドキュメント ](./establishing-connections.md)を参照してください。

接続設定を編集するには、接続設定ワークスペースに移動します。 3点アイコン （![3点アイコン。](/help/assets/icons/more.png)）を選択します 使用可能なアクションを表示するには、**[!UICONTROL 編集]**&#x200B;を選択します。

![編集オプションがハイライト表示された接続設定ワークスペース。](/help/assets/connect/manage-connections/edit-connection.png){zoomable="yes"}

ダイアログが表示され、共同作業者のレビュー用に設定の変更を編集して送信するよう求められます。 **[!UICONTROL 編集]**&#x200B;を選択します。

![編集オプションがハイライト表示された接続設定を編集ダイアログ。](/help/assets/connect/manage-connections/edit-connection-settings-dialog.png){zoomable="yes"}

### オーディエンスのアクティベーションの編集 {#edit-audience-activation}

オーディエンスアクティベーション設定は、接続内のどの共同作業者が宛先に対してオーディエンスをアクティベートできるかを決定します。 これらの設定を変更するには、**[!UICONTROL オーディエンスアクティベーション]** セクション内の&#x200B;**[!UICONTROL 編集]**&#x200B;を選択します。

![ オーディエンスのアクティブ化セクションと「編集」オプションを表示する接続設定の編集画面。](/help/assets/connect/manage-connections/edit-audience-activation.png){zoomable="yes"}

**[!UICONTROL オーディエンスアクティベーション]** ダイアログで、ドロップダウンメニューを使用してオーディエンスアクティベーション権限を更新します。 1人の共同作業者を選択するか、両方の共同作業者がオーディエンスをアクティブ化できるようにします。

![ オーディエンスのアクティベーション権限を更新するためのドロップダウンメニューが表示されるオーディエンスのアクティベーションダイアログが拡張されました。](/help/assets/connect/manage-connections/audience-activation-dropdown-menu.png){zoomable="yes"}

完了したら、**[!UICONTROL 保存]**&#x200B;を選択します。

![新しいオーディエンスアクティベーション権限と「保存」オプションが表示されたオーディエンスアクティベーションダイアログ。](/help/assets/connect/manage-connections/audience-activation-dialog.png){zoomable="yes"}

### ユースケースを追加 {#add-use-cases}

Collaborationでは、「見つける」、「アクティベート」、「測定」などのユースケースにより、共同作業者と一緒に使用できるプロジェクトセクションと機能を決定します。 今後のプロジェクト用に、既存の接続に追加のユースケースを追加できます。 詳しくは、[ コラボレーションのユースケース ](../overview/use-cases.md)を参照してください。

新しいユースケースを追加するには、「**[!UICONTROL ユースケース]**」セクションの「**[!UICONTROL 編集]**」を選択します。

![ ユースケース セクションと「編集」オプションがハイライト表示された接続設定編集画面。](/help/assets/connect/manage-connections/edit-use-cases.png){zoomable="yes"}

**[!UICONTROL ユースケース]** ダイアログで、追加する新しいユースケースを切り替え、次に&#x200B;**[!UICONTROL 保存]**&#x200B;します。

![保存オプションがハイライト表示されているユースケースダイアログ。](/help/assets/connect/manage-connections/use-cases-dialog.png){zoomable="yes"}

>[!NOTE]
>
>「オーディエンスアクティベーション」や「測定」など、新しいユースケース ](#add-use-cases)を[追加すると、接続設定編集画面が更新され、**[!UICONTROL オーディエンスアクティベーション]**&#x200B;と&#x200B;**[!UICONTROL クレジット分割]** セクションが含まれます。 これらの新しいユースケースに適切な設定を行う必要があります。 詳しくは、[ オーディエンスアクティベーション ](../connect/establishing-connections.md#audience-activation)および[ クレジット分割](../connect/establishing-connections.md#credit-split) ガイドを参照してください。
>
>![新しいユースケースが追加された後、オーディエンスのアクティブ化とクレジット分割のセクションを表示する接続設定編集画面](/help/assets/connect/manage-connections/setup-audience-activation-credit-split.png){zoomable="yes"}

### 一致キーを追加 {#add-match-keys}

接続には、アカウントで設定され、共同作業者も選択した一致キーのみが使用できます。 [新しい一致キーをアカウントに追加し](../setup/onboard-account.md#edit-match-keys)、共同作業者も同じキーを選択したら、既存の接続内でそれらを有効にできます。

接続設定の編集画面で、**[!UICONTROL キーの照合]** セクション内の&#x200B;**[!UICONTROL 編集]**&#x200B;を選択します。

![ キーの一致セクションと編集オプションを強調表示する接続設定の編集画面。](/help/assets/connect/manage-connections/edit-connection-match-keys.png){zoomable="yes"}

**[!UICONTROL 一致キー]** ダイアログが表示され、接続に設定された既存の一致キーが表示されます。 追加する照合キーを選択し、その後&#x200B;**[!UICONTROL 保存]**&#x200B;します。

![選択した新しい一致キーと保存オプションを表示する一致キーのダイアログ。](/help/assets/connect/manage-connections/connection-match-keys-dialog.png){zoomable="yes"}

### クレジット分割を編集 {#edit-credit-split}

クレジット分割設定では、接続の各ユースケースに関連するコストを担当する共同作業者を指定します。 これらの設定を更新するには、**[!UICONTROL クレジット分割]** セクションの&#x200B;**[!UICONTROL 編集]**&#x200B;を選択します。

![ クレジット分割セクションと「編集」オプションがハイライト表示された接続設定画面。](/help/assets/connect/manage-connections/edit-credit-split.png){zoomable="yes"}

**[!UICONTROL クレジット分割]** ダイアログで、[!UICONTROL Activation-Matching]および[!UICONTROL Measurement]の優先設定を選択します。 次に、**[!UICONTROL 保存]**&#x200B;を選択して確認します。

![ クレジットの分割ダイアログに、クレジットの分割の設定と保存オプションが表示されます。](/help/assets/connect/manage-connections/credit-split-dialog.png){zoomable="yes"}

### 変更のレビューと送信 {#review-and-submit-changes}

接続設定の編集が完了したら、**[!UICONTROL 変更を送信]**&#x200B;を確認して選択します。 接続設定の更新は、共同作業者にレビュー用に送信されます。

![更新内容と「変更を送信」オプションを表示する接続設定の編集画面。](/help/assets/connect/manage-connections/review-and-submit-changes.png){zoomable="yes"}

#### 接続設定をドラフトとして保存

接続設定の変更をドラフトとして保存し、いつでも接続設定の更新を完了するために戻ることができます。

変更をドラフトとして保存するには、**[!UICONTROL 変更を送信]**&#x200B;の横にある&#x200B;**[!UICONTROL キャンセル]**&#x200B;を選択します。 次に、**[!UICONTROL 未送信の変更]** ダイアログで、**[!UICONTROL 後で続行]**&#x200B;を選択して確認します。

![接続設定の編集画面。](/help/assets/connect/manage-connections/unsubmitted-changes-dialog.png){zoomable="yes"}

変更はドラフトとして保存されます。 接続設定ワークスペースに、未送信の変更があることを示す通知が表示されます。 さらに更新するには、**[!UICONTROL 編集を続行]**&#x200B;を選択します。

![接続設定ワークスペースの通知で、レビューと送信が保留中の未送信の変更が表示されています。](/help/assets/connect/manage-connections/continue-editing-connection.png){zoomable="yes"}
