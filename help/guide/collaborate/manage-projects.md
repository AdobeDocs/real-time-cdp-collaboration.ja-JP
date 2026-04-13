---
title: プロジェクトの作成と管理
description: Adobe Real-Time CDP Collaborationでのプロジェクトの作成および管理方法について説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: ae492846-bc0a-4422-86ca-577bcc1fa60c
source-git-commit: 0cf888e36ffc4730fc8de4d8adccae0e0fc2caa8
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 11%

---

# プロジェクトの作成と管理

{{limited-availability-release-note}}

プロジェクトは、Adobe Real-Time CDP Collaborationのワークフローの中核を成す要素です。 共同作業者とつながった後、プロジェクトを作成してオーディエンスの重複を計算し、キャンペーンに適したオーディエンスを見つけます。

>[!TIP]
>
>通常、プロジェクトは、単一のキャンペーンに関連付ける必要があります。

![現在のすべてのプロジェクトを表示する共同作業ダッシュボード。](/help/assets/collaborate/manage-view-projects/projects-overview-page.png){zoomable="yes"}

フィルターを使用すると、以下に示すように、特定の共同作業者で開始したプロジェクトのみを表示できます。

![1人の共同作業者を含むプロジェクトのフィルター付きビュー。](/help/assets/collaborate/manage-view-projects/filtered-project-view.png){zoomable="yes"}

## プロジェクトを作成 {#create-project}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_create_project_advertisername_amc"
>title="広告主名（Amazon Marketing Cloud）"
>abstract="Amazon Marketing Cloud（AMC）接続の場合、このフィールドは、お使いの Amazon Ads ログインでアクセスできる AMC インスタンスを表します。 広告主名は反映されません。 必要なインスタンスがリストに表示されない場合は、Amazon Marketing Cloud 管理者に連絡してアクセス権をリクエストしてください。"

プロジェクトを作成するには、まず[共同作業者との接続](/help/guide/connect/establishing-connections.md)を確立する必要があります。 接続が確立されたら、その共同作業者と一緒にプロジェクトを作成できます。

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_projects_advertisername"
>title="広告主名"
>abstract="ドロップダウンメニューから広告主名を選択します。 オプションは、システムとの互換性を確保するために、発行者によって接続設定で事前設定されています。"

**[!UICONTROL コラボレーション]**&#x200B;に移動し、**[!UICONTROL マイプロジェクト]**&#x200B;に移動します。 初めてのプロジェクトの場合は、**[!UICONTROL プロジェクトを作成]**&#x200B;を選択できます。 それ以外の場合は、追加アイコン（![追加アイコン。](/help/assets/icons/plus.png)）を選択できます 新しいプロジェクトをいつでも作成できます。

![&#x200B; プラス記号を選択するか、プロジェクトを作成して新しいプロジェクトを設定します。](/help/assets/collaborate/manage-view-projects/create-project.png){zoomable="yes"}

「**[!UICONTROL プロジェクトを作成]**」ダイアログが表示されます。 ドロップダウンから、プロジェクトを作成する&#x200B;**[!UICONTROL Collaborator]**&#x200B;を選択します。 パブリッシャーで、接続設定中に広告主名を設定した場合は、**[!UICONTROL 広告主名]**&#x200B;を選択できます。

>[!NOTE]
>
> 接続設定で1つの広告主名を設定した場合、デフォルトで表示されます。 広告主名が設定されていない場合、広告主の&#x200B;**[!UICONTROL 名前]**&#x200B;は&#x200B;**[!UICONTROL 広告主名]**&#x200B;として事前に選択されています。

![共同作業者が選択され、広告主名が強調表示されたプロジェクト ダイアログを作成します。](/help/assets/collaborate/manage-view-projects/create-project-advertiser-names.png){zoomable="yes"}

次に、プロジェクトに&#x200B;**[!UICONTROL プロジェクト名]**&#x200B;と&#x200B;**[!UICONTROL 説明]**&#x200B;を追加します。 次に、プロジェクトを表す画像を選択します。 この画像は、プロジェクト概要ページでプロジェクトを区別するのに役立ちます。 完了したら、**[!UICONTROL 作成]**&#x200B;を選択してプロジェクトを作成します。

![新しいプロジェクトを設定するために必要なオプション &#x200B;](/help/assets/collaborate/manage-view-projects/create-project-required-info.png){zoomable="yes"}

接続設定時に選択したユースケースに基づいて、新しいプロジェクト、その詳細、および使用可能なセクションを表示できるようになりました。

![&#x200B; プロジェクト概要ワークスペース。](/help/assets/collaborate/manage-view-projects/project-overview.png){zoomable="yes"}

## キャンペーン IDの管理 {#manage-campaign-id}

**キャンペーン ID**&#x200B;は、プロジェクトを特定のキャンペーンにリンクし、[測定レポート &#x200B;](./measure.md#create-measurement-report)を生成するために必要です。 同じ共同作業者で複数のキャンペーンを実行する場合は、1つのプロジェクトに複数のキャンペーン IDを追加できます。 これらのキャンペーンはすべて、レポートで選択できます。

- **パブリッシャー**: レポートを実行する前に、Collaboration UIでCampaign IDと関連名を入力または更新します。
- **広告主**：必要に応じて、共同作業者（発行者）にキャンペーン IDの追加を依頼します。

キャンペーン IDを追加または更新するには、**[!UICONTROL コラボレーション]** ワークスペースに移動し、関連するプロジェクトカード内の&#x200B;**[!UICONTROL 表示]**&#x200B;を選択します。

![&#x200B; プロジェクトカード内の「表示」オプションを強調表示する共同作業ワークスペース。](/help/assets/collaborate/manage-view-projects/view-project.png){zoomable="yes"}

対応する&#x200B;**[!UICONTROL プロジェクト概要]** ワークスペースが表示され、プロジェクトにリンクされたすべてのキャンペーンが一覧表示された&#x200B;**[!UICONTROL キャンペーン IDと名前]**&#x200B;のセクションが表示されます。 キャンペーンをまだ追加していない場合は、**[!UICONTROL 追加]**&#x200B;を選択します。 既にキャンペーンが存在する場合は、**[!UICONTROL 編集]**&#x200B;を選択して詳細を更新するか、キャンペーンを追加します。

![編集オプションがハイライト表示されたキャンペーン IDと名前セクションを表示するプロジェクト概要ワークスペース。](/help/assets/collaborate/manage-view-projects/edit-campaign-id.png){zoomable="yes"}

**[!UICONTROL キャンペーン IDと名前]** ダイアログで、**[!UICONTROL キャンペーン IDを追加]**&#x200B;を選択して、キャンペーンの詳細を入力できる新しい行を追加します。

![&#x200B; キャンペーン IDを追加オプションを選択した後、空のキャンペーン行を表示するキャンペーン IDと名前ダイアログ。](/help/assets/collaborate/manage-view-projects/add-campaign-row.png){zoomable="yes"}

**[!UICONTROL キャンペーン ID]**&#x200B;と&#x200B;**[!UICONTROL キャンペーン名]**&#x200B;を入力し、**[!UICONTROL 保存]**&#x200B;を選択します。

![新しいキャンペーンの詳細と「保存」オプションがハイライト表示されたキャンペーン IDと名前ダイアログ。](/help/assets/collaborate/manage-view-projects/save-campaign-id.png){zoomable="yes"}

最新のキャンペーンと最近の変更を表示するには、**[!UICONTROL キャンペーン IDと名前]** セクションを確認してください。 新しいキャンペーン IDを使用して、測定レポートを生成できるようになりました。

![更新されたキャンペーン IDと名前のセクションを表示するプロジェクト概要ワークスペース。](/help/assets/collaborate/manage-view-projects/view-updated-campaigns.png){zoomable="yes"}
