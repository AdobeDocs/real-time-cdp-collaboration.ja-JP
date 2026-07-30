---
title: オーディエンスをアクティベート
description: Adobe Real-Time CDP Collaborationでオーディエンスをアクティベートする方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
TQID: https://experienceleague.adobe.com/bfPHtcW8Mf6RhIlg5fKcJmPSEKDyAODjbNRJ5D3SMkQ
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 4b38559f30c55f4cb1607d373fb1318416382c32
workflow-type: tm+mt
source-wordcount: 1078
ht-degree: 2%

---

# オーディエンスをアクティベート

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL Activate]** ワークスペースは、接続プロセス [&#128279;](../connect/establishing-connections.md#connection-settings)中に&#x200B;**オーディエンスアクティベーション** ユースケースが有効になった場合にのみ使用できます。 ユースケースについて詳しくは、[&#x200B; プロジェクトの管理](./manage-projects.md#project-use-cases) ガイドを参照してください。

オーディエンスのアクティベーション機能を使用すれば、キャンペーン目的でオーディエンスをアクティベートできます。 ライセンス認証は、接続[&#128279;](/help/guide/connect/establishing-connections.md#configure-connection-settings)で設定されたオーディエンスのライセンス認証設定に応じて、いずれかの共同作業者によって実行できます。 キャンペーンに最適なオーディエンスを[見つけたら](./discover.md)、オーディエンスをアクティブ化して使用できるようにします。 オーディエンスをアクティベートすると、Adobe Experience Platformなど、共同作業者の事前設定済みの宛先に送信され、キャンペーンで使用できるようになります。 宛先の設定について詳しくは、[宛先の概要](../destinations/overview.md) ガイドを参照してください。

アクティベーションがサポートされているワークフローのどこに適合するかの概念的な説明については、[&#x200B; オーディエンスの概要](../setup/audiences-overview.md)を参照してください。

## 新しいオーディエンスを活用 {#activate-new-audiences}

オーディエンスのアクティブ化を開始するには、プロジェクトワークスペースの「**[!UICONTROL アクティブ化]**」タブに移動します。

>[!IMPORTANT]
>
>**オーディエンスをアクティブ化する前**&#x200B;に、共同作業者&#x200B;**は宛先を設定する必要があります。** オーディエンスをアクティベートすると、共同作業者が設定した宛先に自動的に送信されます。 宛先が設定されていない場合、オーディエンスをアクティブ化することはできません。
>
>![共同作業者に宛先が設定されていない場合のアクティブ化ワークスペース。](/help/assets/collaborate/activate/no-destination-configured.png)

追加アイコン（![追加アイコン。](/help/assets/icons/plus.png)）を選択するか、以前のオーディエンスがアクティベーション用に送信されていない場合は、**[!UICONTROL オーディエンスをアクティベート]** オプションを選択します。

![&#x200B; オーディエンスが追加されていないプロジェクトのアクティブ化ワークスペース。](/help/assets/collaborate/activate/activate-new-audiences.png)

オーディエンスをアクティブ化ワークフローが開き、共同作業者に送信するオーディエンスを選択できます。 ドロップダウンを使用してオーディエンスを選択するか、特定のオーディエンスを検索します。 選択する前にオーディエンスに関する詳細を表示するには、**[!UICONTROL オーディエンスを参照]**&#x200B;を選択します

![&#x200B; ドロップダウンと「オーディエンスを参照」オプションがハイライト表示されたオーディエンスのアクティベーションのワークフロー。](/help/assets/collaborate/activate/audience-activation.png)

**[!UICONTROL オーディエンスを参照]**&#x200B;で、各オーディエンスの&#x200B;**[!UICONTROL ID数]**、**[!UICONTROL 重複ID]**&#x200B;および&#x200B;**[!UICONTROL 重複%]**&#x200B;を確認できます。

![利用可能なオーディエンスを表示するオーディエンスを参照ダイアログ。](/help/assets/collaborate/activate/browse-audiences.png)

>[!IMPORTANT]
>
>複数の照合キーを使用するオーディエンスをアクティブ化する場合、1つ（または複数）の照合キーに重複がないか、オーディエンスサイズがないか、しきい値を下回ると、アクティブ化全体が失敗します。 オーディエンスが十分に重複しており、すべてのマッチキーで最低1,000 IDのしきい値を満たしていることを確認してからアクティベートします。

キャンペーンでアクティブ化するオーディエンスを選択し、**[!UICONTROL 保存]**&#x200B;を選択します。 オーディエンスが表示され、選択したオーディエンスの&#x200B;**[!UICONTROL ID数]**、**[!UICONTROL 重複ID]**&#x200B;および&#x200B;**[!UICONTROL 重複%]**&#x200B;が表示されます。

![選択したオーディエンスを含むオーディエンスのアクティブ化ワークフローが表示されます。](/help/assets/collaborate/activate/audience-selected.png)

### 一致キーを編集 {#edit-match-keys}

次に、選択オーディエンス内の&#x200B;**[!UICONTROL 一致キーを編集]**&#x200B;を選択して、オーディエンスの一致キーを編集できます。 これらのオプションは、共同作業者の接続が最初に設定されたときに、一致キーの選択から継承されます。 特定のキャンペーンに適用されない場合は、選択した照合キーを削除できますが、新しい照合キーを追加することはできません。

![一致キーを編集オプションがハイライト表示されたオーディエンスのアクティブ化ワークフロー。](/help/assets/collaborate/activate/edit-match-keys.png)

**[!UICONTROL 一致キーを編集]** ダイアログが開き、使用しない一致キーを切り替えることができます。 **[!UICONTROL 保存]**&#x200B;を選択して、変更を保存します。

>[!NOTE]
>
>少なくとも1つの一致キーを選択する必要があります。

![&#x200B; オーディエンスのアクティブ化ワークフローの一致キーを編集ダイアログ。](/help/assets/collaborate/activate/edit-match-keys-selection.png)

### オーディエンスの更新頻度の設定 {#set-audience-refresh-frequency}

最後に、オーディエンスのアクティベーションに必要な頻度と日付範囲を設定します。 「**[!UICONTROL 頻度]**」ドロップダウンを使用して、オーディエンスを1回アクティブ化するか、定期的なスケジュールで更新するかを選択します。 **[!UICONTROL 1回]**&#x200B;を選択して、オーディエンスを1回だけアクティベートするか、**[!UICONTROL 毎日]**、**[!UICONTROL 2日ごと]**、**[!UICONTROL 3日ごと]**、**[!UICONTROL 4日ごと]**、**[!UICONTROL 5日ごと]**、**[!UICONTROL 6日ごと]**、**[!UICONTROL 2週間ごと]**、**[!UICONTROL 3週間ごと]**、毎月&#x200B;**などの定期的な頻度を選択します。**

![&#x200B; オーディエンス アクティベーション ワークフローの頻度ドロップダウンに、1回、1日、2～6日ごと、2～3週間ごと、毎月など、利用可能なオプションが表示されます。](/help/assets/collaborate/activate/activation-frequency.png)

アクティブ化スケジュールの開始日と終了日を定義するには、**[!UICONTROL 日付範囲]** フィールドを使用します。

選択内容に問題がなければ、**[!UICONTROL アクティブ化]**&#x200B;を選択してワークフローを完了します。

## ダッシュボードを有効化 {#activate-dashboard}

「**[!UICONTROL アクティブ化]**」タブでは、共同作業者に送信されたすべてのオーディエンスと、共同作業者が宛先に対してアクティブ化したすべてのオーディエンスを表示できます。

![送信されたオーディエンスとアクティブ化されたオーディエンスのセクションを表示するアクティブ化ダッシュボード。](/help/assets/collaborate/activate/activate-dashboard.png)

## 送信されたオーディエンスを表示 {#view-sent-audiences}

「**[!UICONTROL 送信済みオーディエンスを]**&#x200B;の共同作業者に送信」セクションには、送信したすべてのオーディエンスが一覧表示されます。 現在、オーディエンスは、共同作業者が設定した宛先に送信した後、自動的に送信されます。 共同作業者のビューでは、これらのオーディエンスが「**[!UICONTROL アクティブ化されたオーディエンス]**」セクションに表示されます。

送信された各オーディエンス内に、次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ステータス]** | 送信されたオーディエンスのステータス。 |
| **[!UICONTROL ID数]** | オーディエンス内のIDの数。 |
| **[!UICONTROL 重複するID]** | このオーディエンスと共同作業者のインベントリ全体のプロファイルの合計母集団との間の重複IDの数。 |
| **[!UICONTROL 作成日]** | オーディエンスが最初に送信された日付。 |
| **[!UICONTROL 最終送信日]** | 1回限りのアクティブ化または定期的なスケジュールから、アクティブ化ワークフローを通じてオーディエンスが共同作業者に最後に利用できるようになった日付。 |
| **[!UICONTROL キーの一致]** | オーディエンスに使用される一致キーを示します。 |

## アクティブなオーディエンスを表示 {#view-activated-audiences}

「**[!UICONTROL アクティブ化されたオーディエンス]**」セクションでは、宛先に対してアクティブ化されたすべてのオーディエンスを表示できます。

アクティブ化された各オーディエンス内に、次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL 名前]** | オーディエンスの名前。 |
| **[!UICONTROL ステータス]** | アクティブ化されたオーディエンスのステータス。 |
| **[!UICONTROL ID数]** | 共同作業者がオーディエンスを送信した際の重複IDに基づいて、アクティブ化されたIDの数。 |
| **[!UICONTROL 作成日]** | オーディエンスがアクティブ化された日付。 |
| **[!UICONTROL 最終更新日]** | アクティブ化中に選択した頻度に基づいて、オーディエンスが最後に更新された日付。 |
| **[!UICONTROL 宛先]** | オーディエンスがアクティベートされた宛先。 |
| **[!UICONTROL キーの一致]** | オーディエンスに使用される一致キーを示します。 |

## 送信したオーディエンスを削除 {#delete-sent-audiences}

アクティブ化しなくなった送信済みオーディエンスを削除できます。 送信済みオーディエンスを削除すると、**[!UICONTROL 送信済みオーディエンス]** セクションから削除され、共同作業者の宛先に対してアクティブ化されなくなります。

送信されたオーディエンスを削除するには、**[!UICONTROL 削除]** アイコン （![削除アイコン :](/help/assets/icons/delete.png)）を選択します 「**[!UICONTROL 送信済みオーディエンス：]**」セクションのオーディエンスの横。

![送信済みオーディエンスのセクションの「削除」オプション。](/help/assets/collaborate/activate/delete-sent-audiences.png)

確認ダイアログが開き、削除の確認を求められます。 「**[!UICONTROL 削除]**」を選択して確定します。

![削除確認ダイアログ。](/help/assets/collaborate/activate/delete-sent-audiences-confirmation.png)

## 次の手順 {#next-steps}

オーディエンスをアクティブ化してキャンペーンを実行したら、Adobeのイネーブルメントおよびエンジニアリングチームと協力して測定データをアップロードし、対応する[測定レポート &#x200B;](/help/guide/collaborate/measure.md)を表示します。
