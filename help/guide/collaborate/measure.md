---
title: パフォーマンスの測定
description: 様々なチャネルでのキャンペーンのパフォーマンスを測定します。 様々なレポートの使用方法と解釈方法について説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: c92b263e-1f96-49f1-841a-ef2e97a4cb9a
source-git-commit: a7215d453021be578a32ce1af4d659845c3b8493
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 19%

---

# パフォーマンスの測定

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL 測定]** ワークスペースは、**測定** ユースケースが [&#x200B; 接続処理中に &#x200B;](../connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[&#x200B; プロジェクトの管理 &#x200B;](./manage-projects.md#project-use-cases) ガイドを参照してください。

Adobe Real-Time CDP Collaborationで使用可能なレポートについて説明し、様々なチャネルをまたいでマーケティングキャンペーンのパフォーマンスを測定および分析する方法を説明します。

## 前提条件

Collaborationの測定レポートにアクセスする前に、次の操作を完了しています。

* [&#x200B; 測定 &#x200B;](/help/guide/connect/establishing-connections.md) ユースケースを有効にして **プロジェクト** の共同作業を開始した共同作業者と [&#x200B; 連携 &#x200B;](/help/guide/collaborate/manage-projects.md)
* キャンペーンを実行し [&#x200B; アップロードされた測定データ &#x200B;](/help/guide/setup/onboard-measurement-data.md) をCollaborationに送信します。

<!--

## Create a report {#create-report}

Hidden until functionality is live. At that point, move the contextualhelp from below into this section. 

The syntax rtcdp_collaboration_measurement_create_report is currently implemented in the UI. However, a preference would be to imlement the other contextualhelp ID from below instead, since that explicitly includes campaignID in the syntax. Need to sync up with UI team. More details in CORE-116991.

-->

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

1. **[!UICONTROL 共同作業]**/**[!UICONTROL マイプロジェクト]** に移動します。
2. 目的のプロジェクトで「**[!UICONTROL 表示]**」を選択します。
3. プロジェクトで、「**[!UICONTROL 測定]**」タブを選択します。

**[!UICONTROL 完全なレポートを表示]** を選択すると、使用可能な様々なレポートにアクセスできます。詳しくは、以下を参照してください。

![&#x200B; プロジェクトの「測定」タブへのアクセス方法 &#x200B;](/help/assets/collaborate/measure/measurement.gif)

### 概要ビュー

測定タブのページの上部ビューには、キャンペーンの概要と、参照可能な大まかな数値が表示されます。

**[!UICONTROL インプレッション数]**：クリエイティブが表示された合計回数。
**[!UICONTROL ユニークリーチ]**：クリエイティブを閲覧した個人 ID の数。
**[!UICONTROL 合計平均頻度]**：インプレッション数を、到達したユニーク ID で割った値です。 この図は、すべての ID がクリエイティブに表示された頻度を示しています。

![&#x200B; キャンペーンの概要ビュー &#x200B;](/help/assets/collaborate/measure/campaign-summary.png)

### 指標の推移 {#metrics-over-time}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_measure_metricsovertime"
>title="指標の推移"
>abstract="指標の推移ビューを使用すると、キャンペーンの期間中にクリエイティブに表示されたインプレッションの合計数を把握できます。レポートに表示するディメンションは、最大 2 つまで選択できます。"

指標の推移ビューを使用すると、キャンペーンの期間中にクリエイティブに表示されたインプレッションの合計数を把握できます。レポートに表示して分析する指標は、最大 2 つまで選択できます。

![&#x200B; 指標の推移ビュー &#x200B;](/help/assets/collaborate/measure/metrics-over-time.png)

### 頻度配分 {#frequency-distribution}

頻度分布ビューを使用して、一意の各ユーザーに表示されたインプレッション数の分類を理解します。 このビューは、今後のキャンペーンでオーディエンスを抑制する時期を決定するのに役立ちます。 例えば、既に 1 つのクリエイティブを 3 回表示しているプロファイルを抑制できます。

![&#x200B; 頻度分布ビュー &#x200B;](/help/assets/collaborate/measure/frequency-distribution.gif)

### ディメンション別の指標 {#metric-by-dimension}

インプレッション数、ビューアブルインプレッション数、ユニークリーチ、コストなど、プレースメント媒体のコンテキストの様々な指標を分析します。 キャンペーンに最適な結果をもたらすメディア（モバイルストリーミング、プログラムによる CTV など）を分析します。

![&#x200B; ディメンション別指標。](/help/assets/collaborate/measure/metric-by-dimension.png)

### 累積リーチカーブ {#cumulative-reach-curve}

キャンペーンが進行し、インプレッション数が増えたので、リーチできるユーザー数も増えたかどうかを把握します。 ある一定の時点を過ぎると、同じ人物に何度も繰り返しクリエイティビティが表示される高原に到達するのがキャンペーンの一般的なパターンです。 このビューを使用すると、新しいユーザーにリーチされなくなった瞬間に応じて、今後のキャンペーンの期間を調整できます。

![&#x200B; 累積リーチカーブ &#x200B;](/help/assets/collaborate/measure/cumulative-reach-curve.png)

### プレースメント別インプレッション数 {#impressions-by-placement}

クリエイティブのインプレッションを促進しているメディアを理解します。 これは、今後のキャンペーンで広告費用をどこに投資するかを決定するのに役立ちます。

![&#x200B; プレースメントによるインプレッション数 &#x200B;](/help/assets/collaborate/measure/impressions-by-placement.png)
