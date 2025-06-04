---
title: オーディエンスを共有
description: 広告キャンペーン用にオーディエンスを共同作業者と共有する方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 0fdf0598-89c9-452d-a2e3-ce868df0b9d2
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 6%

---

# オーディエンスを共有

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL 共有]** ワークスペースを使用できるのは、**オーディエンスの共有とアクティベーション** のユースケースが [ 接続処理中に ](../connect/establishing-connections.md#connection-settings) 有効になっている場合のみです。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

広告主として、オーディエンスをパブリッシャーと共有してキャンペーンを実行できるようにする方法を説明します。 共同作業で **オーディエンスを検出** ユースケースが有効になっている場合は、まず [ 「検出」タブ ](/help/guide/collaborate/discover.md) で重複レポートを実行し、共有するのに最適なオーディエンスを特定します。

## 新しいオーディエンスの共有

オーディエンスの共有を開始するには、プロジェクトワークスペースの「**[!UICONTROL 共有]**」タブに移動します。 キャンペーンのオーディエンスを共有できるのは **広告主組織** のみです。 このタブでは、共有オーディエンスをレビューおよび管理できます。

**プラス記号（+）** を選択するか、以前のオーディエンスが共有されていない場合は **[!UICONTROL オーディエンスを共有]** オプションを選択して、オーディエンス共有プロセスを開始します。

![ オーディエンスが共有されていないデフォルトビュー ](/help/assets/collaborate/share/share-new-audiences.png)

新しいパネルが表示され、共同作業者と共有するオーディエンスを選択できます。

![ 新しいオーディエンスを共有ワークフロー ](/help/assets/collaborate/share/share-audiences-workflow.png)

### 共有するオーディエンスを選択

オーディエンス選択ウィンドウで、検索バーにオーディエンス名を入力することで、共有する特定のオーディエンスを検索できます。 **[!UICONTROL オーディエンスを参照]** を選択し、使用可能な並べ替えオプションを使用して、必要な正確なオーディエンスを見つけます。

![ オーディエンスが選択された状態のオーディエンス参照ビュー ](/help/assets/collaborate/share/browse-audiences-view.png)

### マッチキーの編集とターゲティングオプションの設定

共有するオーディエンスを選択した後、共有アクティビティに対して他の設定オプションを選択できるようになりました。

![[ マッチ キーを編集 ] および [ ターゲット ] または [ セレクターを省略 ] がハイライト表示されている ](/help/assets/collaborate/share/match-keys-and-targeting.png)

**[!UICONTROL 一致キーを編集]** を選択して、オーディエンスの ID に使用する一致キーを示します。 これらのオプションは、共同作業者間の接続が最初に設定されたときに選択した設定から継承されます。 この特定のキャンペーンに適用されない場合は、その時点で選択された一致キーを削除できますが、この時点では新しい一致キーを追加できません。

![ 一致キーを編集 ](/help/assets/collaborate/share/update-match-keys.png)

オーディエンスごとに、キャンペーンでそのオーディエンスのメンバーをターゲットにするか抑制するかを選択します。 抑制されたプロファイルは、特に、発行者によってアクティブ化されたオーディエンスには含まれません。

### オーディエンスの更新頻度と間隔の設定

最後に、オーディエンスの更新に使用する頻度と日付範囲を設定します。 現在サポートされているオーディエンスの更新モードは、**[!UICONTROL 1 回]** と **[!UICONTROL 1 日]** です。

**[!UICONTROL 1 回]** を選択すると、キャンペーンの期間全体でオーディエンスメンバーシップが更新されません。 「**[!UICONTROL 毎日]**」を選択すると、キャンペーンの期間全体を通して、オーディエンスメンバーシップが 1 日に 1 回更新されます。

![ ハイライト表示された「頻度」オプション ](/help/assets/collaborate/share/audience-refresh-frequency.png)

選択が完了したら、「**[!UICONTROL 共有]**」を選択してワークフローを完了します。

>[!SUCCESS]
>
>「**[!UICONTROL 共有]**」タブに、新しいオーディエンス共有アクティビティが表示されるようになりました。 必要に応じて、戻って選択内容を編集できます。

## 現在共有されているオーディエンスを表示

「**[!UICONTROL 共有]**」タブでは、共同作業者間で現在共有されているオーディエンスを、オーディエンス共有アクティビティでグループ化して表示できます。

![ 「共有」タブの概要 ](/help/assets/collaborate/share/share-tab-overview.png)

<!--

The banner at the top of the page shows figures across all audience sharing activities. 

![The hero banner in the sharing tab.](/help/assets/collaborate/share/share-hero-banner.png)


|Metric | Description |
|---------|----------|
| **[!UICONTROL Shared audiences]** | Indicates the number of audiences shared between collaborators in this project, across all audience sharing modules. |
| **[!UICONTROL Estimated addressable reach]** | Indicates the approximate number of profiles that you can reach across all the audiences that are currently shared in the project. [TODO: ADD INFORMATION ABOUT HOW THIS IS CALCULATED] |
| **[!UICONTROL Target identities]** | The number of identities across all audiences shared in this project for which you selected to target the profiles. |
| **[!UICONTROL Suppress identities]** | The number of identities across all audiences shared in this project for which you selected to suppress the profiles and thereby not target them in campaigns. |

-->

各オーディエンス共有アクティビティ内で、各共有オーディエンスに関する情報を取得できます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID 数]** | 最新の ID 数評価ごとに、このオーディエンスに関連付けられたすべての ID にわたるプロファイルの数を示します。 これらの数値は、24 時間ごとに更新されます。 |
| **[!UICONTROL 重複する ID]** | このオーディエンスのメンバー間で重複している ID の数と、共同作業者の在庫全体でのプロファイルの総母集団を示します。 |
| **[!UICONTROL キーの分類に一致]** | オーディエンスで使用される各 ID の ID 数を表示します。 例えば、合計 500,000 人のユーザーという ID 数は、ハッシュ化されたメール ID をキーに切り替えた 400,000 人のユーザーと、モバイル ID をキーに切り替えた 100,000 人のユーザーで構成される場合があります。 ここで説明する例では、同じ人物が、メールおよびモバイル ID ID を使用して、オーディエンスに 2 回存在する場合があります。 |
| **[!UICONTROL 目的]** | **[!UICONTROL 抑制]** または **[!UICONTROL ターゲット]**。 オーディエンスのメンバーをターゲットにするか、キャンペーンから除外するかを示します。 |

また、このページには、**[!UICONTROL 共有を一時停止]** および **[!UICONTROL オーディエンスを編集]** するためのコントロールもあります。

## オーディエンスの編集 {#edit-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_share_edit_audiences_usecases"
>title="ターゲットまたは抑制のユースケース"
>abstract="<p>オーディエンス内のプロファイルにキャンペーンの広告を表示する場合は、「**ターゲット**」を選択します。</p> <p>オーディエンス内のプロファイルをキャンペーンメッセージから除外する場合は、「**抑制**」を選択します。</p>"

**[!UICONTROL オーディエンスを編集]** を選択すると、オーディエンス共有モジュールで共有するオーディエンスを変更できるほか、オーディエンスの共有方法に関する複数の設定を変更できます。

![ オーディエンスを編集モーダルの表示 ](/help/assets/collaborate/share/edit-audiences-modal.png)

<!--

Search for audiences that you want to add to the sharing module. 

For each audience, you can select whether you'd like to target or suppress those profiles in campaigns. 

To remove an audience from the sharing module, select the trash can icon [TODO: add spectrum icon and folder].

Select how often you would like the audience membership to be refreshed and the date range within which you want the membership of the audience to be refreshed. 

TODO: are there any limitations for frequency in the M1 release?

-->

## 次の手順

パブリッシャーが共有オーディエンスを受け取ったら、デジタル広告キャンペーンで [ アクティブ化 ](/help/guide/collaborate/activate.md) します。
