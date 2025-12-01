---
title: 最新のReal-Time CDP Collaboration リリースノート
description: Real-Time CDP Collaborationの最新リリースに従ってください
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 8513c648-1cc1-4544-b86d-2ee3193ab60f
source-git-commit: 9e8371c36b58c2b3065e63396be43ebd2c52576f
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 2%

---

# 最新のReal-Time CDP Collaboration リリースノート

{{limited-availability-release-note}}

**最終更新日**:2025 年 12 月。

これらのリリースノートは、Adobe Real-Time CDP Collaborationでリリースされた機能について説明しています。 Collaboration リリースは、継続的な配信モデルに基づいて動作します。このモデルにより、毎月のおおよそのリリースサイクルが可能になります。 これらのリリースノートは頻繁に更新されるので、定期的に確認してください。

## 2025年12月 {#december-2025}

**ヨーロッパ、中東、アフリカ（EMEA））のお客様がReal-Time CDP Collaborationを利用できるようになりました**。 これらの地域のReal-Time CDP PrimeおよびUltimateのお客様は、自動で利用できます。

## 2025年8月 {#august-2025}

**カナダ** のお客様がReal-Time CDP Collaborationを利用できるようになりました。 これらの地域のReal-Time CDP PrimeおよびUltimateのお客様は、自動で利用できます。

* Collaborationで、次の [&#x200B; 一致キー &#x200B;](../setup/onboard-account.md#supported-match-keys) がサポートされるようになりました。
   * ハッシュ化されたメール
   * ハッシュ化された電話番号
   * CRM ID
   * ロイヤルティ ID
   * ハッシュ化された IPv4
   * AdFixus ID
* Collaboration全体で複数の一致キーを使用できるようになり、オーディエンスサイズを大きくして一致率を向上させることができます。 オーディエンスのソーシング、接続の確立、オーディエンスのアクティブ化の際には、複数の一致キーを使用できます。 複数の一致キーの使用について詳しくは、[&#x200B; 一致キーの設定 &#x200B;](../setup/onboard-account.md) および [&#x200B; ソーシングオーディエンス &#x200B;](../setup/onboard-audiences.md#map-fields) ガイドを参照してください。

>[!IMPORTANT]
>
>複数の一致キーが使用されているオーディエンスをアクティブ化する場合、1 つ（または複数）の一致キーの重複がない、オーディエンス数がない、またはしきい値を下回る場合、アクティベーション全体が失敗します。 オーディエンスに十分な重複があり、アクティブ化する前にすべての一致キーで 1000 個の ID の最小しきい値を満たしていることを確認します。

* Adobe Experience Platformの宛先では、複数の一致キーを持つオーディエンスのアクティブ化をサポートするようになりました。 さらに、宛先のマッピングを設定する際にリンクされたキーを使用して、アクティベーション中に送信される一致キーを指定できるようになりました。 詳しくは、[Experience Platformの宛先 &#x200B;](../destinations/experience-platform.md#linked-keys) ガイドを参照してください。
* 共同作業者は、複数のオーディエンスを一度に編集できるようになりました。 一括編集ツールを使用して、複数のオーディエンスのオーディエンスメタデータ、接続アクセス、名前、説明およびカテゴリを編集できるようになりました。 オーディエンスの編集について詳しくは、[&#x200B; オーディエンスの管理 &#x200B;](../setup/onboard-audiences.md#edit-audiences) ガイドを参照してください。

## 2025年7月 {#july-2025}

Real-time CDP Collaborationで、ブランド間のコラボレーションがサポートされるようになりました。 共同作業者は、広告主であるか公開者であるかに関係なく、接続を形成できるようになりました。 これにより、より柔軟なコラボレーションの機会が可能になり、ブランドは互いのデータとインサイトを活用できます。 ブランド間のコラボレーションと、広告主とパブリッシャーのコラボレーションの違いについて詳しくは、[&#x200B; コラボレーションパターン &#x200B;](../overview/collaboration-patterns.md) ガイドを参照してください。

* コラボレーターは、[&#x200B; プライベート接続の招待 &#x200B;](../connect/establishing-connections.md#private-connection-invites) を使用して相互に接続できるようになりました。 アカウントの一意の接続コードを共同作業者と共有すると、共同作業者はそのコードを使用してユーザーと直接接続できます。 これは、ブランド間のコラボレーションの中核となる機能であり、コラボレーターは、広告主が **[!UICONTROL コラボレーターを見つける]** ディレクトリを探索する以外にも、つながりを確立できます。
* [&#x200B; セルフサービスの宛先 &#x200B;](../setup/manage-destinations.md) が、広告主とパブリッシャーの両方が利用できるようになりました。
* Audience Activation が、接続の両方の共同作業者に対して、その [&#x200B; アカウントの役割 &#x200B;](../overview/roles.md) に関係なく、使用できるようになりました。 Audience Activation 設定は、[&#x200B; 接続の確立 &#x200B;](../connect/establishing-connections.md#configure-connection-settings) 中に設定され、オーディエンスをアクティブ化できる共同作業者を指定できます。 Audience Activation について詳しくは、[&#x200B; オーディエンスのアクティブ化 &#x200B;](../collaborate/activate.md) ガイドを参照してください。
* **[!UICONTROL アクティブ化]** のユースケースが、ブランド間のコラボレーションをサポートするように再構成されました。 プロジェクト内の **[!UICONTROL アクティブ化]** タブに、共同作業者に送信されたオーディエンスと、共同作業者が宛先に対してアクティブ化したオーディエンスが表示されるようになりました。 詳しくは、[&#x200B; オーディエンスのアクティブ化 &#x200B;](../collaborate/activate.md) ガイドを参照してください。<br> ![&#x200B; 「送信先のオーディエンス」セクションと「アクティブ化されたオーディエンス」セクションのアクティブ化ダッシュボード。](/help/assets/release-notes/2025/activate-dashboard.png){zoomable="yes"}
* オーディエンスインデックススコアがプロジェクトの **[!UICONTROL 検出]** タブで使用できるようになりました。 オーディエンスインデックススコアは、オーディエンスが共同作業者のオーディエンスにどの程度適合しているかを測定する指標です。 このスコアは、基になるオーディエンスの数と重複に基づいて計算されます。 オーディエンスインデックススコアについて詳しくは、[&#x200B; オーディエンスインデックススコア &#x200B;](../collaborate/discover.md#audience-index-score) ガイドを参照してください。

## 2025年5月 {#may-2025}

* Real-Time CDP Collaborationは、**オーストラリア** および **ニュージーランド** のお客様が利用できるようになりました。 これらの地域のReal-Time CDP PrimeおよびUltimateのお客様は、自動で利用できます。
* Real-Time CDP Collaborationは、「設定 [&#x200B; セクションの「](../setup/manage-destinations.md)**[!UICONTROL 宛先]** タブを使用して **[!UICONTROL セルフサービスの宛先]** を提供するようになりました。 宛先を使用すると、広告ネットワークやデータ管理プラットフォームなどのサードパーティプラットフォームでオーディエンスをアクティブ化して、様々なチャネルをまたいで顧客にリーチできます。 現在、Adobe Experience Platformの宛先のみがサポートされています。 別の宛先の設定に興味がある場合は、Adobe担当者にお問い合わせください。 宛先について詳しくは、[&#x200B; 宛先の概要 &#x200B;](../destinations/overview.md) ガイドを参照してください。
   * 宛先では、[Adobe Experience Platform オーディエンスポータル &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences) でCollaboration オーディエンスを表示することもできます。
* Collaborationの既存のデータ接続のオーディエンスの更新頻度を編集できるようになりました。 現在、オーディエンスを毎日または 2～6 日ごとに更新するように選択できます。 オーディエンスの更新頻度を編集する方法について詳しくは、[&#x200B; データ接続の管理 &#x200B;](../setup/manage-data-connection.md#scheduling) ガイドを参照してください。
* コラボレーター間のクレジット分割が、接続内で選択された各ユースケースに対して設定されるようになりました。 ユースケースごとに異なるクレジット消費ルールを設定して、クレジットの使用方法をより詳細に制御できます。 クレジット分割機能について詳しくは、[&#x200B; 接続設定 &#x200B;](../connect/establishing-connections.md#connection-settings) ガイドを参照してください。 クレジットの消費方法について詳しくは、[&#x200B; クレジットアクティビティタイプ &#x200B;](../setup/my-activity.md#types-of-activities) ガイドを参照してください。<br> ![&#x200B; クレジット分割機能を示す接続設定画面 &#x200B;](/help/assets/release-notes/2025/credit-split.png){zoomable="yes"}
* パブリッシャーは、広告主から接続設定を受け入れる前に広告主名と ID を設定できるようになりました。 パブリッシャーは、内部システムに合った名前と ID を設定できます。これは、広告主の名前と ID とは異なる場合があります。 広告主名と ID の追加について詳しくは、[&#x200B; 接続設定 &#x200B;](../connect/establishing-connections.md#connection-settings.md) ガイドを参照してください。<br> ![&#x200B; 広告主名と ID を設定しているパブリッシャーを示す接続設定画面 &#x200B;](/help/assets/release-notes/2025/add-advertiser-names-modal.png){zoomable="yes"}

## 2025年4月 {#april-2025}

* 新しい **[!UICONTROL 処理済みの入力]** 列がクレジット消費アクティビティテーブルに追加されました。 この列には、各アクティビティで処理された入力（ID や行など）の合計数が表示されます。 [&#x200B; 詳細情報 &#x200B;](/help/guide/setup/my-activity.md#inputs-processed). <br> ![&#x200B; マイアクティビティビューでハイライト表示された処理済み列の入力。](/help/assets/release-notes/2025/inputs-processed-column.png){zoomable="yes"}
* 新しい連絡先メールオプションがアカウントの作成に追加されました。 これは、パートナーの共同作業者が接続プロセス中に必要に応じて連絡するのに役立ちます。 [詳細情報](../setup/onboard-account.md)

## 2025年3月 {#march-2025}

* Collaborationに [&#x200B; オーディエンスをソーシング &#x200B;](/help/guide/setup/onboard-audiences.md) する際に、オーディエンスの更新頻度を **1 ～ 6 日ごと** に設定して、[Audience Management クレジットアクティビティ &#x200B;](/help/guide/setup/my-activity.md#types-of-activities) をより適切に管理できるようになりました。 詳しくは、[&#x200B; オーディエンスの管理 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/segmentation/ui/audience-portal.md#manage-audiences) ガイドを参照してください。<br> ![&#x200B; オーディエンスメンバーシップを更新するための様々な頻度インターバルを示すスケジュール画面。](/help/assets/setup/add-manage-audiences/audience-scheduling-frequency.png " オーディエンスメンバーシップを更新するための様々な頻度インターバルを示すスケジュール画面。"){width="250" align="center" zoomable="yes"}
* コラボレータとの接続を確立する際に、事前定義された **ユースケース** から選択できるようになりました。 選択したユースケースによって、使用可能になるプロジェクトセクションと製品機能が決まります。 詳しくは、「[&#x200B; プロジェクトの管理 &#x200B;](/help/guide/collaborate/manage-projects.md#project-use-cases) ガイドを参照してください。
   * *測定* は、**測定** プロジェクトセクションを有効にします。
   * *オーディエンス検出* により、**検出** プロジェクトセクションが有効になります。
   * *Audience Activation* で **アクティベート** プロジェクトセクションを有効にする <br>
* 共同作業を希望しない共同作業者との接続を削除できるようになりました。 接続を削除する方法については、「[&#x200B; 接続の削除 &#x200B;](/help/guide/connect/establishing-connections.md#delete-connections) ガイドを参照してください。

## 2025年2月 {#february-2025}

Adobe Real-Time CDP Collaborationは、広告主やパブリッシャーがサードパーティ cookie を使用せずに高価値オーディエンスを検出、アクティブ化および測定できるようにすることを目的に構築されたもので、米国で一般公開されるようになりました。

### 基本を学ぶ

1. **アクセス設定**：システム管理者は、ユーザーのアクセス権限を設定します。 アクセス権限の設定について詳しくは、[&#x200B; ユーザーアクセスの管理 &#x200B;](/help/guide/permissions/manage-user-access.md#RTCDP-collaboration-access) ガイドを参照してください。
2. **データソースの接続**:Collaborationで使用するSource オーディエンス。 オーディエンスのソーシングを開始するには、[&#x200B; オーディエンスのソースおよび管理 &#x200B;](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。
3. **接続の確立**：信頼できる広告主やパブリッシャーとの共同作業を開始します。 接続の作成について詳しくは、[&#x200B; 接続の確立 &#x200B;](/help/guide/connect/establishing-connections.md) ガイドを参照してください。
4. **検出とアクティブ化**：キャンペーンでアクティブ化する価値のあるオーディエンスを特定するプロジェクトを作成します。 プロジェクトの作成について詳しくは、[&#x200B; プロジェクトの管理 &#x200B;](/help/guide/collaborate/manage-projects.md) ガイドを参照してください。

### 対象

* Adobe Real-Time CDP Collaborationは現在、米国のお客様のみが利用できます。
* Adobe Real-Time CDP PrimeおよびUltimateのお客様が自動的に使用できます

詳しくは、以下を参照してください。

* [Collaborationの概要](/help/guide/home.md)
* [エンドツーエンドのワークフロー](/help/guide/overview/end-to-end-workflow.md)
* [権限の概要](/help/guide/permissions/overview.md)
