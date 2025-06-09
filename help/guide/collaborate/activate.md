---
title: オーディエンスをアクティベート
description: Adobe Real-Time CDP Collaborationでオーディエンスをアクティブ化する方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: f19aff1b7d10a446dd209721e7a6fdf537c9d63e
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# オーディエンスをアクティベート

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL アクティブ化]** ワークスペースは、（接続プロセス中に [**Audience Activation** ユースケースが有効になっている場合にのみ使用でき ](../connect/establishing-connections.md#connection-settings) す。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

Audience Activation を使用すると、キャンペーンでオーディエンスをアクティブ化できます。 この活動プロセスは、広告主とパブリッシャーの共同作業です。 [ キャンペーンに最適なオーディエンスを見つける ](./discover.md) 後、オーディエンスはターゲットオーディエンスをアクティブ化できます。 アクティブ化されたオーディエンスは、キャンペーンで使用するために、パブリッシャーの事前設定済み宛先（Adobe Experience Platformなど）に送信されます。 宛先の設定について詳しくは、[ 宛先の概要 ](../destinations/overview.md) ガイドを参照してください。

>[!IMPORTANT]
>
>現在、広告主がオーディエンスをアクティブ化すると、その後、組織に対して設定された宛先に対して自動的にアクティブ化されます。 パブリッシャーは **必ず** 宛先を設定 *事前* 広告主はオーディエンスをアクティブ化します。 宛先が設定されていない場合、オーディエンスはパブリッシャーに送信されますが、どのキャンペーンでもアクティブ化できません。

## 新しいオーディエンスをアクティブ化

オーディエンスのアクティブ化を開始するには、プロジェクトワークスペースの「**[!UICONTROL アクティブ化]**」タブに移動します。

追加アイコン（![ 追加」アイコンを選択します。](/help/assets/icons/plus.png)）、または **[!UICONTROL オーディエンスをアクティブ化]** る前のオーディエンスが送信されていない場合はオプション。

![ オーディエンスが追加されていないプロジェクトのアクティブ化ワークスペース。](/help/assets/collaborate/activate/activate-new-audiences.png)

オーディエンスをアクティベートワークフローが開き、共同作業者に送信するオーディエンスを選択できます。 ドロップダウンを使用してオーディエンスを選択するか、特定のオーディエンスを検索します。 選択する前にオーディエンスに関する詳細を表示するには、「**[!UICONTROL オーディエンスを参照]**」を選択します。

![ ドロップダウンオプションと「オーディエンスを参照」オプションがハイライト表示された Audience Activation ワークフロー。](/help/assets/collaborate/activate/audience-activation.png)

**[!UICONTROL オーディエンスを参照]** で、各オーディエンスの **[!UICONTROL ID 数]**、**[!UICONTROL 重複する ID]** および **[!UICONTROL 重複 %]** を確認できます。

![ 使用可能なオーディエンスを表示するオーディエンスを参照ダイアログ ](/help/assets/collaborate/activate/browse-audiences.png)

キャンペーンでアクティブ化するオーディエンスを選択し、「**[!UICONTROL 保存]**」を選択します。 オーディエンスが表示され、選択したオーディエンスの **[!UICONTROL ID 数]**、**[!UICONTROL 重複 ID]** および **[!UICONTROL 重複 %]** を確認できます。

![ 選択したオーディエンスが表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/audience-selected.png)

### 一致キーを編集

次に、オーディエンスを選択した範囲内で **[!UICONTROL マッチキーを編集]** を選択して、オーディエンスのマッチキーを編集できます。 これらのオプションは、共同作業者間の接続が最初に設定されたときに、一致キーの選択から継承されます。 選択した一致キーが特定のキャンペーンに適用されない場合は、そのキーを削除できますが、新しい一致キーを追加することはできません。

![ 「一致キーを編集」オプションがハイライト表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/edit-match-keys.png)

**[!UICONTROL マッチキーを編集]** ダイアログが開き、使用しないマッチキーを切り替えることができます。 「**[!UICONTROL 保存]**」を選択して変更を保存します。

>[!NOTE]
>
>1 つ以上の一致キーを選択する必要があります。 現在のリリースでは、使用できる一致キーは **[!UICONTROL ハッシュ化されたメール]** のみなので、この一致キーを削除することはできません。

![ オーディエンスのアクティベーションワークフローの一致キーを編集ダイアログ ](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### オーディエンスの更新頻度と間隔の設定

最後に、更新するオーディエンスに希望する頻度と日付範囲を設定します。 現在のリリースでサポートされている頻度のオプションは **[!UICONTROL 1 回]** のみです。 **[!UICONTROL 1 回]** の頻度は、オーディエンスが 1 回アクティブ化され、更新されないことを意味します。 **[!UICONTROL 日付]** オプションには、現在の日付が自動入力されます。

![ 「頻度」セクションがハイライト表示された Audience Activation ワークフロー ](/help/assets/collaborate/activate/audience-frequency.png)

選択が完了したら、「**[!UICONTROL アクティベート]**」を選択してワークフローを完了します。 オーディエンスがアクティベートされ、「**[!UICONTROL アクティベート]** タブで表示できるようになりました。 また、共同作業者の **[!UICONTROL アクティブ化]** タブでも使用できるようになり、キャンペーンで使用できるようになります。

オーディエンスの名前編集アイコン（![ 鉛筆アイコン](/help/assets/icons/edit.png)）を選択するか、**[!UICONTROL 非アクティブ化]** を選択してオーディエンスを非アクティブ化します。

![ アクティブ化されたオーディエンスが表示され、「編集」オプションと「非アクティブ化」オプションがハイライト表示された「アクティブ化」タブ。](/help/assets/collaborate/activate/edit-activate-audience.png)

## アクティブ化されたオーディエンスを表示

「**[!UICONTROL アクティブ化]**」タブでは、パブリッシャーと広告主の両方が、現在アクティブ化されているオーディエンスを表示できます。 現在、オーディエンスは、広告主がアクティブ化すると自動的にパブリッシャーの設定済み宛先に送信されます。

![ 「アクティブ化」タブの概要。アクティブ化されたオーディエンスが表示されます。](/help/assets/collaborate/activate/activate-overview.png)

アクティブ化された各オーディエンス内に、次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL アクティブ化された ID]** | オーディエンス内のアクティブ化された ID の数を示します。 |
| **[!UICONTROL 重複する ID]** | このオーディエンスと、共同作業者の在庫全体でのプロファイルの総母集団との間で重複する ID の数を示します。 |
| **[!UICONTROL キーの分類に一致]** | オーディエンスで使用される各 ID の ID 数を表示します。 例えば、合計 500,000 人のユーザーという ID 数は、ハッシュ化されたメール ID をキーに切り替えた 400,000 人のユーザーと、モバイル ID をキーに切り替えた 100,000 人のユーザーで構成される場合があります。 ここで説明する例では、同じ人物が、メールおよびモバイル ID ID を使用して、オーディエンスに 2 回存在する場合があります。 |

## 次の手順 {#next-steps}

データをアクティブ化しキャンペーンを実施した後、Adobeのイネーブルメントおよびエンジニアリングチームと協力して、測定データをアップロードし、対応する [ 測定レポート ](/help/guide/collaborate/measure.md) を確認します。
