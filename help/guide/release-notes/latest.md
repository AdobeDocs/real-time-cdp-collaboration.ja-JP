---
title: 最新のReal-Time CDP Collaboration リリースノート
description: Real-Time CDP Collaborationの最新リリースに従う
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
TQID: https://experienceleague.adobe.com/re4oFblCLiZpspWIS7D4EEYNh36EDhULEOd2-ccXH28
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: ec15512bc5c6579ade907fc238cfe5394862dc7e
workflow-type: tm+mt
source-wordcount: 1968
ht-degree: 3%

---

# 最新のReal-Time CDP Collaboration リリースノート

{{limited-availability-release-note}}

**最終更新**: 2026年7月。

このリリースノートでは、Adobe Real-Time CDP Collaborationでリリースされた機能について説明します。 Collaboration リリースは継続的な配信モデルで動作します。これにより、ほぼ毎月のリリース頻度を把握できます。 これらのリリースノートは頻繁に更新されるので、定期的に確認してください。

## 2026年7月 {#july-2026}

Real-Time CDP Collaborationでは、追加のセルフサービスのオーディエンスソーシングオプションをサポートするようになりました。

**新機能または更新された機能**

| 機能 | 説明 |
| ------- | ----------- |
| [!DNL Databricks Delta Share]およびAdobe Audience Managerからのセルフサービスのオーディエンスのソーシング | [!DNL Databricks Delta Share]から直接1st パーティオーディエンスを取得したり、適格なAdobe Audience Manager セグメントをCollaborationに取り込んだりできるようになりました。 設定の手順については、次のガイドを参照してください。 <ul><li>オーディエンスソーシング用[設定 [!DNL Databricks Delta Share] ](../setup/configure-databricks-audience-sourcing.md)</li><li>[ オーディエンスソーシング用にAdobe Audience Managerを設定](../setup/configure-aam-audience-sourcing.md)</li></ul> |

{style="table-layout:auto"}

## 2026年4月 {#april-2026}

Real-Time CDP Collaborationで新機能が利用可能になりました。 これには、パートナーの招待に関するCollaboration [!DNL Starter]や、[!DNL Snowflake]および[!DNL Google Cloud Storage]からのオーディエンスソーシングの拡張、一致キーとしての[!DNL Demdex ID (ECID)]のサポート、代理店およびデータパートナーという2つの新しい共同作業者の役割が含まれます。

**新機能または更新された機能**

| 機能 | 説明 |
| ------- | ----------- |
| Real-Time CDP Collaboration [!DNL Starter] | Collaboration ライセンスを持たないパートナーを招待して、Collaboration [!DNL Starter]を通じて共同作業を行うことができます。 招待されたパートナーは、オーディエンスを獲得し、重複を発見して、共有された接続でオーディエンスをアクティブ化できます。 開始するには、[Collaboration [!DNL Starter] 概要](../overview/starter-overview.md)を参照してください。 |
| [!DNL Snowflake]および[!DNL Google Cloud Storage]からのセルフサービスオーディエンスのソーシング | [!DNL Snowflake Secure Data Share]または[!DNL Google Cloud Storage] バケットから直接Collaborationに1st パーティオーディエンスを取得できるようになりました。 設定の手順については、次のガイドを参照してください。 <ul><li>オーディエンスソーシング用[設定 [!DNL Snowflake] ](../setup/configure-snowflake-audience-sourcing.md) </li><li> オーディエンスソーシング用[設定 [!DNL Google Cloud Storage] ](../setup/configure-gcs-audience-sourcing.md) </li></ul> |
| [!DNL Demdex ID]一致キー | [!DNL Demdex ID] （ECID）は、プラットフォーム間で匿名のCookie ベースのIDを照合するための照合キーとしてサポートされるようになりました。 認証されたユーザーデータに依存することなく、オーディエンスの重複精度を向上できます。 詳しくは、[ サポートされている一致キー](../setup/onboard-account.md#supported-match-keys)を参照してください。 |
| 新しい共同作業者の役割 | Collaborationでは、**代理店**&#x200B;および&#x200B;**データパートナー**&#x200B;を含む、2つの共同作業者ロールが追加でサポートされるようになりました。 これらの役割は、さまざまな組織がプラットフォーム内で参加し、連携する方法を拡大します。 詳細情報： <ul><li>[共同作業者アカウントの役割](../overview/roles.md)</li><li>[Collaboration パターン ](../overview/collaboration-patterns.md)</li><li>[ エンドツーエンドのワークフロー](../overview/end-to-end-workflow.md)</li></ul> |

{style="table-layout:auto"}

## 2026 年 3 月 {#march-2026}

Real-Time CDP Collaborationでキャンペーン測定レポートを生成し、測定データを管理できるようになりました。

**新機能または更新された機能**

| 機能 | 説明 |
| ------- | ----------- |
| 測定の一般提供 | 測定レポートがCollaborationで一般公開されました。 マーケティングキャンペーンに関連付けられたキャンペーン IDをパブリッシャーとして入力し、コンバージョンデータを広告主として取得して、キャンペーン全体の結果に対して&#x200B;**キャンペーン概要**、キャンペーン効果インサイトに対して&#x200B;**アトリビューション**&#x200B;の2種類のレポートを生成できるようになりました。 最初に、次のガイドを参照してください。 <ul><li>[ キャンペーン IDの入力](../collaborate/manage-projects.md#manage-campaign-id)</li><li>[Source コンバージョンデータ ](../setup/onboard-measurement-data.md)</li><li>[測定レポートの作成と表示](../collaborate/measure.md)</li></ul> |
| 測定ライフサイクル管理 | Collaborationは測定管理にも対応しています。<ul><li> 広告主は、測定データの接続と関連するコンバージョンイベントの両方を編集または削除して、正確で最新のキャンペーン分析を確保できるようになりました。 詳細については、[測定データ接続の管理](../setup/manage-measurement-data-connection.md)および[ コンバージョンイベントの管理](../setup/onboard-measurement-data.md#edit-measurement-data)を参照してください。</li><li>また、任意のコラボレーションプロジェクトの「**[!UICONTROL Measure]**」タブから、スケジュールされた測定レポートを直接編集または削除することもできます。 これはすべてのユーザーが利用できます。 詳しくは、[測定レポートの管理ガイド ](../collaborate/measure.md)を参照してください。</li></ul> |

{style="table-layout:auto"}

## 2026年2月 {#february-2026}

Real-Time CDP Collaborationでは、既存の接続設定とデータ接続設定をインターフェイスで直接編集できるようになりました。

**新しい機能または更新された機能**

| 機能 | 説明 |
| ------- | ----------- |
| 接続設定を編集 | 接続の所有者は、接続が確立された後、ユースケース、照合キー、アクティベーション権限、クレジット分割を更新できるようになりました。 ステップバイステップの手順については、[接続を編集](../connect/manage-connections.md#edit-connection)を参照してください。 |
| データ接続の編集 | Collaboration内で直接、既存のデータ接続の照合キーとスケジュール設定を更新できます。 詳細な手順については、[ データ接続の編集](../setup/manage-data-connection.md#edit-data-connection)を参照してください。 |

## 2026年1月 {#january-2026}

Real-Time CDP Collaborationでは、オーディエンスのソーシングの新しい方法として、CSV ファイルのアップロードがサポートされるようになりました。また、オーディエンスのマッチングと測定を強化するための新しいモバイルマッチキー（IDFAおよびGAID）もサポートされるようになりました。

**新機能または更新された機能**

| 機能 | 説明 |
| ------- | ----------- |
| オーディエンスソーシング用のCSV アップロード | UIから直接、CSV ファイルをソースオーディエンスにCollaborationにアップロードします。 短期的なコラボレーションプロジェクトに最適な1st パーティデータのオンボーディング。 詳しくは、「[ オーディエンスのソーシングガイド用にCSV ファイルをアップロードする](../setup/upload-csv-audience-sourcing.md)」を参照してください。 |
| モバイルマッチキーサポート | Collaborationは、オーディエンスのマッチングと測定のために、IDFAやGAIDなどのモバイルマッチキーをサポートするようになりました。 これらの照合キーは、アカウントの設定中に選択され、新しい接続の接続設定を設定する際や下流のコラボレーションワークフローで使用できます。 詳しくは、[一致キー設定ガイド ](../setup/onboard-account.md#set-up-match-keys)を参照してください。 |

{style="table-layout:auto"}

## 2025年12月 {#december-2025}

Real-Time CDP Collaborationは、**ヨーロッパ、中東、アフリカ（EMEA）**&#x200B;のお客様が利用できるようになりました。 Real-Time CDP PrimeおよびUltimateのお客様は、これらのリージョンで自動的に利用できます。

## 2025年8月 {#august-2025}

Real-Time CDP Collaborationは、**カナダ**&#x200B;のお客様が利用できるようになりました。 Real-Time CDP PrimeおよびUltimateのお客様は、これらのリージョンで自動的に利用できます。

* Collaborationでは、次の[一致キー](../setup/onboard-account.md#supported-match-keys)がサポートされるようになりました。
  * ハッシュ化されたメール
  * ハッシュ化された電話番号
  * CRM ID
  * ロイヤルティ ID
  * ハッシュ化された IPv4
  * AdFixus ID
* Collaboration全体で複数のマッチキーが使用できるようになりました。これにより、オーディエンスサイズを拡大し、マッチ率を向上させることができます。 オーディエンスのソーシング、接続の確立、オーディエンスのアクティブ化を行う場合は、複数の照合キーを使用できます。 複数の一致キーの使用について詳しくは、[一致キーの設定](../setup/onboard-account.md)および[ オーディエンスのソーシング ](../setup/onboard-audiences.md#map-fields)のガイドを参照してください。

>[!IMPORTANT]
>
>複数の照合キーを使用するオーディエンスをアクティブ化する場合、1つ（または複数）の照合キーに重複がないか、オーディエンスサイズがないか、しきい値を下回ると、アクティブ化全体が失敗します。 オーディエンスが十分に重複しており、すべてのマッチキーで最低1,000 IDのしきい値を満たしていることを確認してからアクティベートします。

* Adobe Experience Platformの宛先で、複数の一致キーを使用したオーディエンスのアクティブ化がサポートされるようになりました。 さらに、宛先のマッピングを設定する際にリンクされたキーを使用して、アクティベーション中に送信される照合キーを指定できるようになりました。 詳しくは、[Experience Platform destination](../destinations/experience-platform.md#linked-keys) ガイドを参照してください。
* 共同作業者は、一度に複数のオーディエンスを編集できるようになりました。 一括編集ツールを使用して、複数のオーディエンスのオーディエンスのメタデータ、接続アクセス、名前、説明、カテゴリを編集できるようになりました。 オーディエンスの編集について詳しくは、[ オーディエンスの管理](../setup/onboard-audiences.md#edit-audiences) ガイドを参照してください。

## 2025年7月 {#july-2025}

Adobe Real-Time CDP Collaborationは、ブランド間のコラボレーションをサポートするようになりました。 共同作業者は、広告主かパブリッシャーかに関係なく、接続を形成できるようになりました。 これにより、より柔軟なコラボレーション機会が可能になり、互いのデータとインサイトを活用できるようになります。 ブランド間の共同作業と広告主とパブリッシャー間の共同作業の違いについて詳しくは、[共同作業パターン ](../overview/collaboration-patterns.md) ガイドを参照してください。

* 共同作業者は、[ プライベート接続の招待](../connect/establishing-connections.md#private-connection-invites)を使用して互いに接続できるようになりました。 アカウントの一意の接続コードを共同作業者と共有すると、共同作業者がそれを使用して直接接続できます。 これは、ブランド間のコラボレーションの主な機能であり、共同作業者は、**[!UICONTROL 共同作業者を見つける]** ディレクトリを探索する広告主の枠を超えてつながりを確立できます。
* [ セルフサービスの宛先](../destinations/overview.md)が、広告主とパブリッシャーの両方で利用できるようになりました。
* オーディエンスのアクティブ化は、アカウントの役割[に関係なく、接続の両方の共同作業者に対して利用できるようになりました。 ](../overview/roles.md)オーディエンスのアクティブ化の設定は、[接続の確立中](../connect/establishing-connections.md#configure-connection-settings)に設定され、どの共同作業者がオーディエンスをアクティブ化できるかを指定できます。 オーディエンスのアクティベーションについて詳しくは、[ オーディエンスのアクティベーション ](../collaborate/activate.md) ガイドを参照してください。
* ブランド間のコラボレーションをサポートするために、**[!UICONTROL Activate]**&#x200B;のユースケースが再構成されました。 プロジェクト内の「**[!UICONTROL アクティブ化]**」タブに、共同作業者に送信されたオーディエンスと、共同作業者によって宛先にアクティブ化されたオーディエンスが表示されるようになりました。 詳しくは、[ オーディエンスのアクティベーション ](../collaborate/activate.md) ガイドを参照してください。<br> ![ オーディエンスが送信済みおよびオーディエンスがアクティブ化されたセクションを含むアクティブ化ダッシュボード。](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* オーディエンスインデックススコアが、プロジェクトの「**[!UICONTROL もっと知る]**」タブで利用できるようになりました。 オーディエンスインデックススコアは、オーディエンスが共同作業者のオーディエンスにどの程度合致しているのかを示す指標です。 このスコアは、基礎となるオーディエンスサイズと重複にもとづいて計算されます。 オーディエンスインデックススコアについて詳しくは、[ オーディエンスインデックススコア ](../collaborate/discover.md#audience-index-score) ガイドを参照してください。

## 2025年5月 {#may-2025}

* Real-Time CDP Collaborationは、**オーストラリア**&#x200B;および&#x200B;**ニュージーランド**&#x200B;のお客様が利用できるようになりました。 Real-Time CDP PrimeおよびUltimateのお客様は、これらのリージョンで自動的に利用できます。
* Real-Time CDP Collaborationでは、**[!UICONTROL セットアップ]** セクションの「**[!UICONTROL 自分の宛先]**」タブを通じて[ セルフサービスの宛先](../destinations/overview.md)を提供するようになりました。 配信先を使用すると、広告ネットワークやデータ管理プラットフォームなどのサードパーティプラットフォームでオーディエンスをアクティブ化し、様々なチャネルで顧客にリーチできます。 現在、サポートされているのはAdobe Experience Platformの宛先のみです。 別の目的地の設定をご希望の場合は、Adobe担当者にお問い合わせください。 宛先について詳しくは、[宛先の概要](../destinations/overview.md) ガイドを参照してください。
  * 宛先では、[Collaboration オーディエンスポータル ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences)でAdobe Experience Platform オーディエンスを表示するためのサポートも追加されています。
* Collaborationの既存のデータ接続のオーディエンス更新頻度を編集できるようになりました。 現在は、毎日、または2～6日ごとにオーディエンスを更新することができます。 オーディエンスの更新頻度を編集する方法について詳しくは、[ データ接続の管理](../setup/manage-data-connection.md#scheduling) ガイドを参照してください。
* 共同作業者のクレジット分割は、接続内で選択した各ユースケースに対して設定されるようになりました。 ユースケースごとに異なるクレジット消費ルールを設定することで、クレジットの使用方法をより適切に制御できます。 クレジット分割機能について詳しくは、[接続設定](../connect/establishing-connections.md#connection-settings) ガイドを参照してください。 クレジットの利用方法について詳しくは、[ クレジットアクティビティタイプ ](../setup/my-activity.md#types-of-activities) ガイドを参照してください。<br> ![ クレジット分割機能を表示する接続設定画面。](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* パブリッシャーは、広告主から接続設定を受け入れる前に、広告主の名前とIDを設定できるようになりました。 パブリッシャーは、社内システムに沿った名前やIDを設定でき、広告主の名前やIDとは異なる場合があります。 広告主名とIDの追加について詳しくは、[接続設定](../connect/establishing-connections.md#connection-settings.md) ガイドを参照してください。<br> ![広告主名とIDを設定するパブリッシャーを表示する接続設定画面。](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## 2025年4月 {#april-2025}

* 新しい&#x200B;**[!UICONTROL 処理済み入力]**&#x200B;列がクレジット消費アクティビティテーブルに追加されました。 この列には、各アクティビティで処理された入力の合計数（IDや行など）が表示されます。 [詳細を読む](/help/guide/setup/my-activity.md#inputs-processed)。<br> ![処理済み列がマイアクティビティビューで強調表示されます。](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* アカウント作成に新しい連絡先メールオプションが追加されました。 これにより、パートナーの共同作業者が接続プロセス中に必要に応じて連絡を取ることができます。 [詳細情報](../setup/onboard-account.md)。

## 2025年3月 {#march-2025}

* [ オーディエンス ](/help/guide/setup/onboard-audiences.md)をCollaborationにソーシングする際に、オーディエンスの更新頻度を&#x200B;**1日ごとに**&#x200B;に設定し、[Audience Managementのクレジットアクティビティ ](/help/guide/setup/my-activity.md#types-of-activities)をより適切に管理できるようになりました。 詳しくは、[ オーディエンスの管理](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences) ガイドを参照してください。<br> ![ オーディエンスメンバーシップを更新するための異なる頻度の間隔を表示するスケジュール画面。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png " オーディエンスメンバーシップを更新するための異なる頻度の間隔を表示するスケジュール画面。"){width="250" align="center" zoomable="yes"}
* 共同作業者との接続を確立する際に、定義済みの&#x200B;**ユースケース**&#x200B;から選択できるようになりました。 選択したユースケースによって、使用可能になるプロジェクトセクションと製品機能が決まります。 詳しくは、[ プロジェクトの管理](/help/guide/collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。
  * *Measurement*&#x200B;は、**Measure** プロジェクトセクションを有効にします。
  * *オーディエンスの発見*&#x200B;により、**発見** プロジェクトセクションが有効になります。
  * *オーディエンスアクティベーション*&#x200B;により、**アクティベート** プロジェクトセクション <br>が有効になります
* 共同作業者との接続を削除できるようになりました。共同作業者との接続は削除できません。 接続を削除する方法については、[接続の削除](/help/guide/connect/establishing-connections.md#delete-connections) ガイドを参照してください。

## 2025年2月 {#february-2025}

Adobe Real-Time CDP Collaborationは、広告主とパブリッシャーが、サードパーティ Cookieを使用せずに有望なオーディエンスを発見、活性化、測定できるようにすることを目的として構築され、現在、米国で一般公開されています。

### 基本を学ぶ

1. **アクセス設定**: システム管理者がユーザーのアクセス権限を設定します。 アクセス権限の設定について詳しくは、[ ユーザーアクセスの管理](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access) ガイドを参照してください。
2. **データソースを接続**: Collaborationで使用するSource オーディエンス。 オーディエンスのソーシングを開始するには、[ オーディエンスのソースと管理](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。
3. **接続の確立**：信頼できる広告主またはパブリッシャーとの共同作業を開始します。 接続の形成について詳しくは、[接続の確立](/help/guide/connect/establishing-connections.md) ガイドを参照してください。
4. **発見とアクティブ化**: キャンペーンでアクティブ化する価値あるオーディエンスを特定するプロジェクトを作成します。 プロジェクトの作成について詳しくは、[ プロジェクトの管理](/help/guide/collaborate/manage-projects.md) ガイドを参照してください。

### 対象

* Adobe Real-Time CDP Collaborationは現在、米国のお客様のみが利用できます。
* Adobe Real-Time CDP PrimeおよびUltimateのお客様は自動的に利用できます

詳しくは、以下を参照してください。

* [Collaborationの概要](/help/guide/home.md)
* [エンドツーエンドのワークフロー](/help/guide/overview/end-to-end-workflow.md)
* [権限の概要](/help/guide/permissions/overview.md)
