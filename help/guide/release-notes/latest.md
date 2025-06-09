---
title: 最新のReal-Time CDP Collaboration リリースノート
description: Real-Time CDP Collaborationの最新リリースに従ってください
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 92e347e3258817a983d8eaed9cf2b962b3443cbc
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 3%

---

# 最新のReal-Time CDP Collaboration リリースノート

{{limited-availability-release-note}}

**最終更新日**:2025 年 4 月。

これらのリリースノートは、Real-Time Customer Data Platform Collaborationでリリースされた機能について説明しています。 Real-Time CDP Collaboration リリースは、継続的な配信モデルに基づいて動作します。このモデルにより、毎月のおおよそのリリースサイクルが可能になります。 これらのリリースノートは頻繁に更新されるので、定期的に確認してください。

## 2025年5月 {#may-2025}

* Real-Time CDP Collaborationは、**オーストラリア** および **ニュージーランド** のお客様が利用できるようになりました。 これらの地域のReal-Time CDP PrimeおよびUltimateのお客様は、自動で利用できます。
* Real-Time CDP Collaborationは、「設定」セクションの「自分の宛先」タブから [ セルフサービスの宛先 ](../setup/manage-destinations.md) を提供するようになりました。 宛先を使用すると、広告ネットワークやデータ管理プラットフォームなどのサードパーティプラットフォームでオーディエンスをアクティブ化して、様々なチャネルをまたいで顧客にリーチできます。 現在、Adobe Experience Platformの宛先のみがサポートされています。 別の宛先の設定に興味がある場合は、Adobe担当者にお問い合わせください。 宛先について詳しくは、[ 宛先の概要 ](../destinations/overview.md) ガイドを参照してください。

   * 宛先では、[Adobe Experience Platform オーディエンスポータル ](https://experienceleague.adobe.com/ja/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences.) でReal-Time CDP Collaboration オーディエンスを表示することもできます。

* Real-Time CDP Collaborationの既存のデータ接続のオーディエンスの更新頻度を編集できるようになりました。 現在、オーディエンスを毎日または 2～6 日ごとに更新するように選択できます。 オーディエンスの更新頻度を編集する方法について詳しくは、[ データ接続の管理 ](../setup/manage-data-connection.md#scheduling) ガイドを参照してください。
* コラボレーター間のクレジット分割が、接続内で選択された各ユースケースに対して設定されるようになりました。 ユースケースごとに異なるクレジット消費ルールを設定して、クレジットの使用方法をより詳細に制御できます。 クレジット分割機能について詳しくは、[ 接続設定 ](../connect/establishing-connections.md#connection-settings) ガイドを参照してください。 クレジットの消費方法について詳しくは、[ クレジットアクティビティタイプ ](../setup/my-activity.md#types-of-activities) ガイドを参照してください。<br> ![ クレジット分割機能を示す接続設定画面 ](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* パブリッシャーは、広告主から接続設定を受け入れる前に広告主名と ID を設定できるようになりました。 パブリッシャーは、内部システムに合った名前と ID を設定できます。これは、広告主の名前と ID とは異なる場合があります。 広告主名と ID の追加について詳しくは、[ 接続設定 ](../connect/establishing-connections.md#connection-settings.md) ガイドを参照してください。<br> ![ 広告主名と ID を設定しているパブリッシャーを示す接続設定画面 ](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## 2025年4月 {#april-2025}

* 新しい **[!UICONTROL 処理済みの入力]** 列がクレジット消費アクティビティテーブルに追加されました。 この列には、各アクティビティで処理された入力（ID や行など）の合計数が表示されます。 [ 詳細情報 ](/help/guide/setup/my-activity.md#inputs-processed). <br> ![ マイアクティビティビューでハイライト表示された処理済み列の入力。](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* 新しい連絡先メールオプションがアカウントの作成に追加されました。 これは、パートナーの共同作業者が接続プロセス中に必要に応じて連絡するのに役立ちます。 [詳細情報](../setup/onboard-organization.md)。

## 2025年3月 {#march-2025}

* Real-Time CDP Collaborationに [ オーディエンスを読み込む ](/help/guide/setup/onboard-audiences.md) 際に、オーディエンスの更新頻度を **1 ～ 6 日ごと** に設定して、[Audience Management クレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities) をより適切に管理できるようになりました。 [ 詳細情報 ](/help/guide/setup/onboard-audiences.md#schedule). <br> ![ オーディエンスメンバーシップを更新するための様々な頻度インターバルを示すスケジュール画面。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png " オーディエンスメンバーシップを更新するための様々な頻度インターバルを示すスケジュール画面。"){width="250" align="center" zoomable="yes"}
* コラボレータとの接続を確立する際に、事前定義された **ユースケース** から選択できるようになりました。 選択したユースケースによって、使用可能になるプロジェクトセクションと製品機能が決まります。 [詳細情報](/help/guide/collaborate/manage-projects.md#project-use-cases)。
   * *キャンペーン測定* は、「**測定** プロジェクトセクションを有効にします。
   * *オーディエンス検出* により、**検出** プロジェクトセクションが有効になります。
   * *Audience Activation* で **アクティベート** プロジェクトセクションを有効にする <br>
* 共同作業を希望しない共同作業者との接続を削除できるようになりました。 [詳細情報](/help/guide/connect/establishing-connections.md#delete-connections)。


## 2025 年 2 月 – 米国のお客様向けの一般公開 {#february-2025-ga}

Real-Time CDP Collaborationは、広告主やパブリッシャーがサードパーティ cookie を使用せずに高価値オーディエンスを検出、アクティブ化および測定できるようにすることを目的に構築されたもので、米国で一般公開されるようになりました。

### 基本を学ぶ

1. **アクセス設定**：システム管理者は、ユーザーのアクセス権限を設定します。 [詳細情報](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access)。
2. **データソースの接続**:Real-Time CDP Collaborationで使用するオーディエンスをインポートします。 [詳細情報](/help/guide/setup/onboard-audiences.md)。
3. **パートナーとのつながりを確立**：信頼できるブランドやパブリッシャーとの共同作業を開始します。 [詳細情報](/help/guide/connect/establishing-connections.md)。
4. **検出とアクティブ化**：貴重なオーディエンスセグメントを特定し、キャンペーンでアクティブ化するプロジェクトを作成します。 [詳細情報](/help/guide/collaborate/manage-projects.md)。

### 対象

* Real-Time CDP Collaborationは現在、米国のお客様のみが利用できます。
* Real-Time CDP PrimeおよびUltimateのお客様が自動的に使用できます

詳しくは、以下を参照してください。

* [Real-Time CDP Collaborationの概要](/help/guide/home.md)
* [エンドツーエンドのワークフロー](/help/guide/end-to-end-workflow.md)
* [権限の概要](/help/guide/permissions/overview.md)
