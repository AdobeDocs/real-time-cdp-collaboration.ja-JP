---
title: パフォーマンスを測定
description: さまざまなチャネルをまたいでキャンペーンのパフォーマンスを測定。 様々なレポートの使用方法と解釈の方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: e06ee94afdd1edbf86430cbe348dc448419b8f4e
workflow-type: tm+mt
source-wordcount: '2612'
ht-degree: 5%

---

# パフォーマンスを測定

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL Measure]** ワークスペースは、接続プロセス [&#128279;](../connect/establishing-connections.md#connection-settings)中に&#x200B;**Measurement** ユースケースが有効になった場合にのみ使用できます。 ユースケースについて詳しくは、[&#x200B; プロジェクトの管理](./manage-projects.md#project-use-cases) ガイドを参照してください。

Adobe Adobe Real-Time CDP Collaborationのレポートでは、さまざまなチャネルをまたいでマーケティング施策のパフォーマンスを測定および分析する方法を解説します。

## 前提条件 {#prerequisites}

Collaborationの測定レポートにアクセスする前に、次の操作を行う必要があります。

* [Measurement **のユースケースが有効になっている共同作業者と](/help/guide/connect/establishing-connections.md)を接続する**
* 共同作業者と少なくとも1つのプロジェクトで共同作業を行います。 [&#x200B; プロジェクトの作成方法](/help/guide/collaborate/manage-projects.md#create-project)について説明します。
* キャンペーンを実行し、キャンペーン [&#128279;](../collaborate/manage-projects.md#manage-campaign-id)に キャンペーン IDが指定されていることを確認します。
   * パブリッシャーの場合は、広告主のキャンペーンにリンクされたキャンペーン IDを入力します。
   * 広告主の場合は、共同作業者（パブリッシャー）にキャンペーン IDの提供を依頼します。 これは、[Measure ワークスペース &#x200B;](#create-measurement-report)でレポートを生成するために必要です。
* [&#x200B; アトリビューションレポート &#x200B;](#create-attribution-report)を[作成する場合は、測定データ &#x200B;](/help/guide/setup/onboard-measurement-data.md)をCollaborationにアップロードします。

## レポートを表示 {#view-reports}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report_campaignID"
>title="キャンペーン ID"
>abstract="キャンペーン ID についての関連情報を UI に追加するためのプレースホルダー。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measurement_create_report"
>title="キャンペーン ID"
>abstract="キャンペーン ID についての関連情報を UI に追加するためのプレースホルダー。"

「測定」タブで使用可能なレポートを表示するには：

1. **[!UICONTROL コラボレーション]** > **[!UICONTROL 自分のプロジェクト]**&#x200B;に移動します。
2. 目的のプロジェクトに対して、**[!UICONTROL ビュー]**&#x200B;を選択します。
3. プロジェクトで、「**[!UICONTROL Measure]**」タブを選択します。

「**[!UICONTROL レポート全体を表示]**」を選択して、利用可能な様々なレポートにアクセスします（詳細は以下を参照）。

![&#x200B; プロジェクトの測定タブにアクセスする方法。](/help/assets/collaborate/measure/measurement.gif)

### 概要ビュー

「測定」タブのページ上部のビューには、次の指標を参照するための高レベルの数値が表示されたキャンペーン概要が表示されます。

**[!UICONTROL インプレッション]**: クリエイティブが表示された合計回数。
**[!UICONTROL ユニーク リーチ]**: クリエイティブを見た個人IDの数。
**[!UICONTROL 合計平均頻度]**: インプレッション数を一意のIDで割った値に達しました。 この図は、すべてのIDがクリエイティブに表示された頻度を示しています。

![&#x200B; キャンペーンの概要ビュー](/help/assets/collaborate/measure/campaign-summary.png)

### 指標の推移 {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="指標の推移"
>abstract="指標の推移ビューを使用すると、キャンペーンの期間中にクリエイティブに表示されたインプレッションの合計数を把握できます。 レポートに表示するディメンションは、最大 2 つまで選択できます。"

指標の推移ビューを使用すると、キャンペーンの期間中にクリエイティブに表示されたインプレッションの合計数を把握できます。 レポートで表示および分析する指標は、最大2つまで選択できます。

![時間表示の指標。](/help/assets/collaborate/measure/metrics-over-time.png)

### 頻度配分 {#frequency-distribution}

周波数分布ビューを使用して、各固有ユーザーに表示されたインプレッション数の内訳を把握します。 このビューは、今後の施策で、オーディエンスの非表示を開始するポイントを決定するのに役立ちます。 例えば、既に3回クリエイティブを見たプロファイルを除外したい場合、

![頻度の分布ビュー。](/help/assets/collaborate/measure/frequency-distribution.gif)

### ディメンション別の指標 {#metric-by-dimension}

プレースメント媒体のコンテキストで、インプレッション、表示可能なインプレッション、ユニークなリーチ、コストなどの様々な指標を分析します。 キャンペーンに最適な結果をもたらしているメディア（モバイルストリーミング、CTV プログラマティックなど）を分析します。

ディメンション別![指標。](/help/assets/collaborate/measure/metric-by-dimension.png)

### 累積リーチカーブ {#cumulative-reach-curve}

キャンペーンが進行し、インプレッション数が増えるにつれて、リーチできたユーザーの数も増えたかどうかを確認します。 キャンペーンで一般的に見られるパターンは、特定の時点を過ぎるとプラトーに達し、同じ人物に何度もクリエイティブが表示されることです。 このビューは、新しいユーザーにリーチしなくなった瞬間に応じて、今後のキャンペーンの長さを調整するのに役立ちます。

![累積リーチカーブ。](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### プレースメント別インプレッション数 {#impressions-by-placement}

クリエイティブのインプレッションを促進するメディアを把握。 これは、今後の施策に広告費をどこに投入すべきかを判断するのに役立ちます。

![&#x200B; プレースメント別インプレッション。](/help/assets/collaborate/measure/impressions-by-placement.png)

### 累積コンバージョン数 {#cumulative-conversions}

このビューでは、表形式で測定するために選択したコンバージョンイベントの詳細な分類を提供します。 テーブルには次のものが含まれます。

* **コンバージョンイベント**：追跡している各コンバージョンイベントの名前。
* **コンバージョン数**：各イベントで発生したコンバージョンの合計数。
* **売上予測**：各コンバージョンイベントに起因する売上予測。

この表を確認して、望ましいアクションを促すキャンペーンの効果を評価します。

![累積コンバージョン数。](/help/assets/collaborate/measure/cumulative-conversions.png)

### 日別のコンバージョン数 {#conversions-by-day}

このグラフは、アトリビューションレポートを作成する際に設定された各イベントについて、コンバージョンの日々の内訳を示しています。 このビューを使用して日々のパターンを明らかにし、コンバージョンの高いアクティビティと低いアクティビティの期間を特定し、キャンペーンのタイムライン全体で様々なコンバージョンイベントがどのように機能するかを比較します。

日別![&#x200B; コンバージョン数。](/help/assets/collaborate/measure/conversions-by-day.gif)

## 測定レポートを作成 {#create-measurement-report}

Collaborationでは、主に2種類の測定レポートを作成できます。

* **キャンペーンの概要**：リーチ、インプレッション、平均頻度、チャネル別の配信などの上位レベルの指標を提供し、キャンペーン全体のパフォーマンスの概要を簡単に説明します。
* **アトリビューション**: キャンペーンの公開がコンバージョンや購入などの下流のアクションをどのように促進するかを測定し、キャンペーンの効果を把握するのに役立ちます。

キャンペーン概要レポートは単独で実行できますが、アトリビューションレポートでは両方のレポートタイプを同時に選択する必要があります。

### キャンペーン概要レポートの作成 {#create-campaign-summary-report}

パブリッシャーと広告主の両方が、**キャンペーン概要** レポートを生成して、キャンペーンのパフォーマンスを評価できます。 これらのレポートを使用して、[reach](#cumulative-reach-curve)、[頻度](#frequency-distribution)、[&#x200B; インプレッション &#x200B;](#impressions-by-placement)などの主要指標に関するインサイトを得て、キャンペーンがどのように配信され、その全体的な影響を把握します。

**キャンペーン概要** レポートを生成するには、**[!UICONTROL コラボレーター]** ワークスペースからプロジェクト ワークスペースに移動します。 「**[!UICONTROL Measure]**」タブから、追加アイコン（![追加アイコン（](/help/assets/icons/plus.png)）を選択します。 **[!UICONTROL Measure]**&#x200B;を選択します。

これが最初のレポートの場合は、**[!UICONTROL レポートを実行]** オプションを選択することもできます。

![&#x200B; レポートの実行オプションと測定オプションを強調表示する「測定」タブ。](/help/assets/collaborate/measure/run-measure-report.png)

**[!UICONTROL 測定レポートを作成]**&#x200B;画面が表示され、**[!UICONTROL 請求の詳細]**、**[!UICONTROL キャンペーンの詳細]**、および&#x200B;**[!UICONTROL レポートの詳細]**&#x200B;のセクションにグループ化された情報と入力フィールドが表示されます。

#### 請求の詳細 {#billing-details}

この節では、測定レポートを生成する際にクレジットがどのように使用されるかを説明します。 クレジットの責任は[接続設定](../connect/establishing-connections.md#credit-split)中に確立されます。 レポートを実行する前に、共同作業者とのクレジット分割設定とレポートの役割を必ず確認して確認してください。

#### キャンペーンの詳細 {#campaign-details}

**[!UICONTROL キャンペーンの詳細]** セクションで、レポートに関連付ける適切な&#x200B;**広告主ID**&#x200B;を選択します。 これらの広告主名またはIDは、[接続設定](../connect/establishing-connections.md#advertiser-names)中に追加されました。 1つの名前のみが設定されている場合は、デフォルトで表示されます。 名前が設定されていない場合、**[!UICONTROL 広告主ID （名前）]** フィールドは無効になり、広告主アカウント名が事前入力されます。

![広告主ID （名前）オプションが無効になっている測定レポートの作成画面。](/help/assets/collaborate/measure/advertiser-id.png)

次に、**[!UICONTROL キャンペーン ID]** ドロップダウンメニューから目的のキャンペーンを選択します。 このメニューには、プロジェクトのパブリッシャーが入力したすべてのキャンペーン IDが一覧表示されます。 必要なキャンペーンが利用できない場合は、レポートを生成する前に[UI](./manage-projects.md#manage-campaign-id)でキャンペーンを追加します。

![Campaign ID ドロップダウンメニューが展開された測定レポートの作成画面。](/help/assets/collaborate/measure/campaign-id.png)

続いて、レポートでカバーする期間を指定します。 **[!UICONTROL レポートの日付範囲]**&#x200B;を選択し、カレンダーを使用して開始日と終了日を選択します。

![&#x200B; レポート日付範囲カレンダーを表示する測定レポートの作成画面。](/help/assets/collaborate/measure/report-date-range.png)

#### レポートの詳細 {#report-details}

**レポート実行日**

「**[!UICONTROL レポートの詳細]**」セクションで、レポートを実行する日付を選択します。 **[!UICONTROL レポート実行日]**&#x200B;を選択し、カレンダーから任意の日付を選択します。

* 今日の日付または過去の日付を選択すると、**キャンペーン概要** レポートがすぐに実行されます。
* 今後の日付を選択した場合、**キャンペーンの概要** レポートはその日に実行される予定です。

![&#x200B; レポート実行日カレンダーを表示する測定レポートの作成画面。](/help/assets/collaborate/measure/report-run-date.png)

**レポートタイプ**

* 広告主の場合は、使用可能なオプションから&#x200B;**[!UICONTROL キャンペーン概要]** レポートタイプを選択できます。 アトリビューションレポートを生成できるのは広告主のみです。
* パブリッシャーの場合、**[!UICONTROL キャンペーン概要]**&#x200B;のレポートタイプは事前に選択されているため、変更できません。 現時点では、アトリビューションレポートを実行することはできません。

![測定レポートの作成画面に、キャンペーン概要オプションが事前選択された変更不可のレポートタイプとして表示されます。](/help/assets/collaborate/measure/cs-report-type.png)

最後に、設定を確認し、**[!UICONTROL 作成]**&#x200B;を選択します。 キャンペーンの概要レポートは、実行日が今日またはそれ以前の場合、または選択した将来の日付の場合にすぐに生成されます。 スケジュール済みレポートは、実行日より前に編集できます。 詳細な手順については、[測定レポートの編集] セクションを参照してください。

利用可能になると、プロジェクトワークスペース内の「**[!UICONTROL Measure]**」タブでいつでもレポートを表示できます。

![測定レポートの作成画面で、情報と「作成」オプションが強調表示されている。](/help/assets/collaborate/measure/cs-review.png)

### アトリビューションレポートを作成 {#create-attribution-report}

広告主は、**アトリビューション** レポートを生成して、キャンペーンの露出が、新規登録や購入などの主要成果にどのように貢献しているかを評価できます。 これらのレポートを活用して、ユーザーとのキャンペーンのインタラクションを把握し、どの顧客接点が最も効果を発揮したのかを特定して、より効果的なマーケティング戦略を策定できます。

>[!IMPORTANT]
>
> アトリビューションレポートを作成する前に、[測定データ &#x200B;](../setup/onboard-measurement-data.md#add-measurement-data)をCollaborationに取り込む必要があります。
>![測定データの要件と無効な測定オプションを含む「測定」タブ。](/help/assets/collaborate/measure/require-measurement-data.png)

**属性** レポートを生成するには、**[!UICONTROL 共同作業者]** ワークスペースからプロジェクト ワークスペースに移動します。 「**[!UICONTROL Measure]**」タブから、追加アイコン（![追加アイコン（](/help/assets/icons/plus.png)）を選択します。 **[!UICONTROL Measure]**&#x200B;を選択します。

これが最初のレポートの場合は、**[!UICONTROL レポートを実行]** オプションを選択することもできます。

![&#x200B; レポートの実行オプションと測定オプションを強調表示する「測定」タブ。](/help/assets/collaborate/measure/run-measure-report-attribution.png)

**[!UICONTROL 測定レポートを作成]**&#x200B;画面が表示され、**[!UICONTROL 請求の詳細]**、**[!UICONTROL キャンペーンの詳細]**、および&#x200B;**[!UICONTROL レポートの詳細]**&#x200B;のセクションにグループ化された情報と入力フィールドが表示されます。

「[&#x200B; キャンペーン概要レポートの作成](#create-campaign-summary-report)」セクションの手順を読み、次の設定を行います。

* [請求の詳細](#billing-details)
* [キャンペーンの詳細](#campaign-details)

#### アトリビューションレポートのレポート詳細 {#report-details-attribution}

**レポート実行日**

>[!IMPORTANT]
>
> アトリビューションレポートの場合、レポート実行日は将来の日付である必要があり、レポート日付範囲の終了日から少なくとも1日後に、定義されたルックバックウィンドウの全期間を加えて発生する必要があります。
> **レポート実行日≥レポート終了日+ ルックバックウィンドウ + 1**
> 
> 例えば、レポートの日付範囲が6月15日に終了し、ルックバックウィンドウが14日の場合、レポート実行日は6月30日以降になります。

「**[!UICONTROL レポートの詳細]**」セクションで、レポートを実行する日付を選択します。 **[!UICONTROL レポート実行日]**&#x200B;を選択し、カレンダーから任意の日付を選択します。

**レポートタイプ**

広告主は、**[!UICONTROL キャンペーンの概要]**&#x200B;に加えて、**[!UICONTROL 属性]**&#x200B;をレポートタイプとして選択できます。 アトリビューションレポートを選択すると、結果には標準のキャンペーンサマリー指標と詳細なアトリビューション分析の両方が含まれ、キャンペーンのパフォーマンスの包括的なビューが提供されます。

![選択したキャンペーンの概要とアトリビューションレポートのタイプの両方を強調表示する測定レポートの作成画面。](/help/assets/collaborate/measure/attribution-report-type.png)

レポートタイプとして「**[!UICONTROL アトリビューション]**」を選択すると、**[!UICONTROL アトリビューション]**&#x200B;設定セクションが表示され、追加の必要な設定が表示されます。

* **日数のルックバックウィンドウ**：各コンバージョンの前にキャンペーンのインプレッションがレポートでどの程度考慮されているかを定義します。 この期間内のインプレッションのみがアトリビューションクレジットの対象となります。
* **コンバージョンイベント**：購入やサインアップなど、測定するコンバージョンアクションを指定します。 これらのイベントは、[測定データを](../setup/onboard-measurement-data.md#add-conversion-event)Collaborationに取り込む際に、事前に設定する必要があります。

最初に、**[!UICONTROL ルックバックウィンドウの値をdays]** フィールドに入力するか、増分/減分オプションで調整します。

![日数のルックバックウィンドウの値を強調表示する測定レポートの作成画面。](/help/assets/collaborate/measure/lookback-window-in-days.png)

次に、使用可能なリストから最大&#x200B;**3**&#x200B;個のコンバージョンイベントを選択します。 特定のイベントの詳細については、**[!UICONTROL i]** アイコンを選択して、その詳細を表示します。

![選択したコンバージョンイベントと購入イベントの情報を強調表示する測定レポートの作成画面。](/help/assets/collaborate/measure/attribution-conversion-events.png)

最後に、設定を確認し、**[!UICONTROL 作成]**&#x200B;を選択してレポートをスケジュールします。 アトリビューションレポートは、指定した実行日に生成されます。 スケジュール済みレポートは、実行日より前に編集できます。 詳細な手順については、[測定レポートの編集] セクションを参照してください。

利用可能になると、プロジェクトワークスペース内の「**[!UICONTROL Measure]**」タブでいつでもレポートを表示できます。

![測定レポートの作成画面で、情報と「作成」オプションが強調表示されている。](/help/assets/collaborate/measure/attribution-review.png)

## 測定レポートを編集 {#edit-measurement-report}

>[!IMPORTANT]
>
>計測レポートの設定を編集できるのは、今後実行がスケジュールされている場合のみです。 既に実行されているレポートの場合、設定を変更することはできません。

測定レポートの設定を更新して、レポートが特定の期間内にキャンペーンの正しい分析を提供し、目的の日付に実行されるようにします。

まず、更新する測定レポートのワークスペースに移動します。 削除アイコンの横にある編集アイコン（![編集アイコン &#x200B;](/help/assets/icons/edit.png)）を選択します。

![編集アイコンがハイライト表示された測定レポート ワークスペース。](/help/assets/collaborate/measure/edit-report.png)

>[!TIP]
>
>「**[!UICONTROL Measure]**」タブで、編集するレポートセクションに移動します。 **[!UICONTROL レポート全体を表示]**&#x200B;の横にある編集アイコン（![編集アイコン &#x200B;](/help/assets/icons/edit.png)）を選択して、設定を更新します。
>![レポートセクション内の編集アイコンを強調表示する「測定」タブ。](/help/assets/collaborate/measure/measure-tab-edit-report.png)

**[!UICONTROL 測定レポートを編集]** ダイアログが表示され、次のセクションにレポートの現在の設定が表示されます。

* [**請求の詳細**](#billing-details)：測定レポートの実行時に、クレジットに関する情報を表示します。 設定は必要ありません。
* [**キャンペーンの詳細**](#campaign-details)：広告主、キャンペーン ID、レポート期間、ユーザーフレンドリーなレポート名の設定を表示します。
* [**レポートの詳細**](#report-details): レポートの種類、レポートの実行日、アトリビューションレポートに特化した設定オプションを表示します。

![請求の詳細、キャンペーンの詳細、レポートの詳細セクションの現在の設定を表示する測定レポートを編集ダイアログ。](/help/assets/collaborate/measure/edit-measurement-report-dialog.png)

### キャンペーンの詳細を編集 {#edit-campaign-details}

**[!UICONTROL 測定レポートを編集]** ダイアログで、**[!UICONTROL 広告主ID （名前）]**&#x200B;および&#x200B;**[!UICONTROL キャンペーン ID]** ドロップダウンメニューを使用して、レポートの広告主とキャンペーン IDを編集します。

![Campaign ID ドロップダウンメニューを強調表示する測定レポートを編集ダイアログが開きます。](/help/assets/collaborate/measure/edit-campaign-id.png)

次に、**[!UICONTROL レポートの日付範囲]**&#x200B;を選択し、カレンダーを使用してレポートの開始日と終了日を変更します。

![&#x200B; レポート日付範囲カレンダーを強調表示する測定レポートを編集ダイアログが開きます。](/help/assets/collaborate/measure/edit-report-date-range.png)

最新の変更をキャプチャするために、更新されたわかりやすいレポート名を入力します。 今後このレポートを認識して見つけるのに役立ちます。

![更新されたフレンドリレポート名を強調表示する測定レポートを編集ダイアログ。](/help/assets/collaborate/measure/edit-friendly-report-name.png)

### レポートの詳細を編集 {#edit-report-details}

別の日付のレポートをスケジュールするには、**[!UICONTROL レポートの詳細]** セクションに移動します。 現在の実行日オプションを選択し、カレンダーを使用して好みの日付を選択します。

![&#x200B; レポート実行日カレンダーを強調表示する測定レポートを編集ダイアログ。](/help/assets/collaborate/measure/edit-report-run-date.png)

広告主は、**[!UICONTROL キャンペーンの概要]**&#x200B;に加えて、**[!UICONTROL 属性]** レポートタイプを選択または削除するオプションがあります。 **[!UICONTROL アトリビューション]**&#x200B;を選択した場合、アトリビューションレポートには、標準のキャンペーンのサマリー指標と詳細なアトリビューションインサイトの両方が含まれます。 **キャンペーンの概要**&#x200B;および&#x200B;**属性**&#x200B;のレポートタイプについて詳しくは、[測定レポートの作成](#create-measurement-report)の節を参照してください。

>[!IMPORTANT]
>
>**発行者**&#x200B;の場合、デフォルトのレポートタイプは&#x200B;**[!UICONTROL キャンペーンの概要]**&#x200B;で、現時点では変更できません。

* レポートタイプとして&#x200B;**[!UICONTROL アトリビューション]**&#x200B;を選択した場合は、**[!UICONTROL アトリビューション]** セクションに必須フィールドを入力する必要があります。 設定手順については、「[属性レポートの詳細](#report-details-attribution)」の節を参照してください。
* レポートの作成時に以前にアトリビューション設定を行った場合は、ルックバックウィンドウ（日数）を編集し、レポートするコンバージョンイベントを選択できます。

日数&#x200B;**で** ルックバックウィンドウを更新するには、数値を入力するか、増減オプションで調整します。 続いて、レポートを作成するコンバージョンイベントを選択します。 利用可能なリストから最大&#x200B;**3**&#x200B;個のコンバージョンを選択できます。

![更新されたコンバージョンイベントを強調表示する測定レポートを編集ダイアログ。](/help/assets/collaborate/measure/edit-conversion-events.png)

完了したら、更新を確認し、**[!UICONTROL 編集]**&#x200B;を選択して変更を適用します。

![編集オプションがハイライト表示された測定レポートの編集ダイアログ。](/help/assets/collaborate/measure/edit-report-confirm.png)

確認ダイアログは、レポートが正常に保存されたことを確認します。

## 測定レポートを削除 {#delete-measurement-report}

Collaborationで測定レポートを削除すると、そのレポートはシステムから完全に削除されます。 このアクションは取り消せません。 これをおこなうには、**[!UICONTROL Measure]** タブで削除するレポートを選択します。

測定レポート ワークスペースで、削除アイコン （![削除アイコン &#x200B;](/help/assets/common/delete.svg)）を選択します。

![削除アイコンがハイライト表示された測定レポート ワークスペース。](/help/assets/collaborate/measure/delete-report.png)

**[!UICONTROL レポートを削除]** ダイアログが表示され、削除の確認を求められます。 「**[!UICONTROL 削除]**」を選択します。

![削除オプションがハイライト表示されたレポートの削除ダイアログ。](/help/assets/collaborate/measure/delete-report-confirm.png)

確認ダイアログは、レポートが正常に削除されたことを確認します。
