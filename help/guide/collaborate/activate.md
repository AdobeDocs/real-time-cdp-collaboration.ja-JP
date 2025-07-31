---
title: オーディエンスをアクティベート
description: Adobe Real-Time CDP Collaborationでオーディエンスをアクティブ化する方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 2%

---

# オーディエンスをアクティベート

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL アクティブ化]** ワークスペースは、（接続プロセス中に **&#x200B;**&#x200B;Audience Activation[ ユースケースが有効になっている場合にのみ使用でき ](../connect/establishing-connections.md#connection-settings) す。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

Audience Activation を使用すると、キャンペーンで使用するオーディエンスをアクティブ化できます。 アクティベーションは、オーディエンスアクティベーションの設定 [ 接続で設定 ](/help/guide/connect/establishing-connections.md#configure-connection-settings) に応じて、いずれかの共同作業者が行うことができます。 [ キャンペーンに最適なオーディエンスを見つけた ](./discover.md) 後、オーディエンスをアクティブ化して使用可能にします。 オーディエンスをアクティブ化すると、そのオーディエンスは共同作業者の事前設定済みの宛先（Adobe Experience Platformなど）に送信され、キャンペーンで使用できるようになります。 宛先の設定について詳しくは、[ 宛先の概要 ](../destinations/overview.md) ガイドを参照してください。

## 新しいオーディエンスをアクティブ化 {#activate-new-audiences}

オーディエンスのアクティブ化を開始するには、プロジェクトワークスペースの「**[!UICONTROL アクティブ化]**」タブに移動します。

>[!IMPORTANT]
>
>**前に** オーディエンスをアクティブ化し、共同作業者が宛先を **必須** 設定できます。 オーディエンスをアクティベートすると、共同作業者の設定された宛先に自動的に送信されます。 宛先が設定されていない場合は、オーディエンスをアクティブ化できません。
>
>![ コラボレータに宛先が設定されていない場合の「アクティブ化」ワークスペース ](/help/assets/collaborate/activate/no-destination-configured.png)

追加アイコン（![ 追加」アイコンを選択します。](/help/assets/icons/plus.png)）、または **[!UICONTROL オーディエンスをアクティブ化]** る前のオーディエンスが送信されていない場合はオプション。

![ オーディエンスが追加されていないプロジェクトのアクティブ化ワークスペース。](/help/assets/collaborate/activate/activate-new-audiences.png)

オーディエンスをアクティベートワークフローが開き、共同作業者に送信するオーディエンスを選択できます。 ドロップダウンを使用してオーディエンスを選択するか、特定のオーディエンスを検索します。 選択する前にオーディエンスに関する詳細を表示するには、「**[!UICONTROL オーディエンスを参照]**」を選択します。

![ ドロップダウンオプションと「オーディエンスを参照」オプションがハイライト表示された Audience Activation ワークフロー。](/help/assets/collaborate/activate/audience-activation.png)

**[!UICONTROL オーディエンスを参照]** で、各オーディエンスの **[!UICONTROL ID 数]**、**[!UICONTROL 重複する ID]** および **[!UICONTROL 重複 %]** を確認できます。

![ 使用可能なオーディエンスを表示するオーディエンスを参照ダイアログ ](/help/assets/collaborate/activate/browse-audiences.png)

キャンペーンでアクティブ化するオーディエンスを選択し、「**[!UICONTROL 保存]**」を選択します。 オーディエンスが表示され、選択したオーディエンスの **[!UICONTROL ID 数]**、**[!UICONTROL 重複 ID]** および **[!UICONTROL 重複 %]** を確認できます。

![ 選択したオーディエンスが表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/audience-selected.png)

### 一致キーを編集 {#edit-match-keys}

次に、オーディエンスを選択した範囲内で **[!UICONTROL マッチキーを編集]** を選択して、オーディエンスのマッチキーを編集できます。 これらのオプションは、共同作業者間の接続が最初に設定されたときに、一致キーの選択から継承されます。 選択した一致キーが特定のキャンペーンに適用されない場合は、そのキーを削除できますが、新しい一致キーを追加することはできません。

![ 「一致キーを編集」オプションがハイライト表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/edit-match-keys.png)

**[!UICONTROL マッチキーを編集]** ダイアログが開き、使用しないマッチキーを切り替えることができます。 「**[!UICONTROL 保存]**」を選択して変更を保存します。

>[!NOTE]
>
>1 つ以上の一致キーを選択する必要があります。 現在のリリースでは、使用できる一致キーは **[!UICONTROL ハッシュ化されたメール]** のみなので、この一致キーを削除することはできません。

![ オーディエンスのアクティベーションワークフローの一致キーを編集ダイアログ ](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### オーディエンスの更新頻度を設定 {#set-audience-refresh-frequency}

最後に、更新するオーディエンスに希望する頻度と日付範囲を設定します。 現在のリリースでサポートされている頻度のオプションは **[!UICONTROL 1 回]** のみです。 **[!UICONTROL 1 回]** の頻度は、オーディエンスが 1 回アクティブ化され、更新されないことを意味します。 **[!UICONTROL 日付]** オプションには、現在の日付が自動入力されます。

![ 「頻度」セクションがハイライト表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/audience-frequency.png)

選択が完了したら、「**[!UICONTROL アクティベート]**」を選択してワークフローを完了します。

## ダッシュボードをアクティブ化 {#activate-dashboard}

「**[!UICONTROL アクティブ化]**」タブでは、共同作業者に送信されたすべてのオーディエンスと、共同作業者が宛先に対してアクティブ化されたすべてのオーディエンスを表示できます。

![ 送信済みオーディエンスとアクティブ化されたオーディエンスを表示するアクティブ化ダッシュボードのセクション ](/help/assets/collaborate/activate/activate-dashboard.png)

## 送信済みオーディエンスの表示 {#view-sent-audiences}

**[!UICONTROL 共同作業者に送信されたオーディエンス]** セクションには、送信したすべてのオーディエンスが一覧表示されます。 現在、オーディエンスは、送信後、自動的に共同作業者の設定された宛先に送信されます。 共同作業者の表示では、これらのオーディエンスは「アクティブ化されたオーディエンス **[!UICONTROL セクションに表示さ]** ます。

送信された各オーディエンス内で、次の指標を確認できます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ステータス]** | 送信されたオーディエンスのステータス。 |
| **[!UICONTROL ID 数]** | オーディエンスの ID の数。 |
| **[!UICONTROL 重複する ID]** | 共同作業者のインベントリ全体での、このオーディエンスとプロファイルの総母集団の間で重複している ID の数。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初に送信された日付。 |
| **[!UICONTROL 最後の送信]** | オーディエンスが最後に共同作業者に送信された日付。 |
| **[!UICONTROL 一致キー]** | オーディエンスに使用される一致キーを示します。 |

## アクティブ化されたオーディエンスを表示 {#view-activated-audiences}

「**[!UICONTROL アクティブ化されたオーディエンス]**」セクションでは、宛先に対してアクティブ化されたすべてのオーディエンスを表示できます。

アクティブ化された各オーディエンス内に、次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ステータス]** | アクティブ化されたオーディエンスのステータス。 |
| **[!UICONTROL ID 数]** | コラボレーターがオーディエンスを送信した際に、重複する ID に基づいてアクティブ化された ID の数。 |
| **[!UICONTROL 作成日]** | オーディエンスがアクティブ化された日付。 |
| **[!UICONTROL 前回の更新]** | アクティベーション時に選択した更新スケジュールに基づいて、オーディエンスが最後に更新された日付。 |
| **[!UICONTROL 宛先]** | オーディエンスがアクティブ化された宛先。 |
| **[!UICONTROL 一致キー]** | オーディエンスに使用される一致キーを示します。 |

## 送信済みオーディエンスを削除 {#delete-sent-audiences}

アクティブ化する必要がなくなった送信済みオーディエンスを削除できます。 送信済みオーディエンスを削除すると、そのオーディエンスは「**[!UICONTROL 送信済みオーディエンス]** セクションから削除され、共同作業者の宛先に対してアクティブ化されなくなります。

送信したオーディエンスを削除するには、「**[!UICONTROL 削除]**」アイコン（「![ 削除」アイコン](/help/assets/icons/delete.png)） **[!UICONTROL 送信済みオーディエンス]** セクションのオーディエンスの横に表示されます。

![ 送信済みオーディエンスのセクションの「削除」オプション ](/help/assets/collaborate/activate/delete-sent-audiences.png)

削除を確認する確認ダイアログが表示されます。 「**[!UICONTROL 削除]**」を選択して確定します。

![ 削除の確認ダイアログ ](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## 次の手順 {#next-steps}

オーディエンスをアクティブ化しキャンペーンを実施した後、Adobe イネーブルメントおよびエンジニアリングチームと協力して測定データをアップロードし、対応する [ 測定レポート ](/help/guide/collaborate/measure.md) を確認します。
