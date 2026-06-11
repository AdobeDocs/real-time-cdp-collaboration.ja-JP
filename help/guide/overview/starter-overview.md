---
title: RTCDP Collaboration スターターの概要
description: Adobe Real-Time CDP Collaboration Starterを利用して、Real-Time CDPの完全なライセンスを取得することなく、ライセンスを取得したパートナーとのプライバシー重視のコラボレーションを促進できます。その方法をご確認ください。
audience: publisher, advertiser, invited users to Real-Time CDP Collaboration Starter
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 7ae0bd3d-eee9-48c0-9f18-a56033fee52d
source-git-commit: d0d854f73fa835984e5cff5207ce3e01297c8deb
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 3%

---

# Adobe Real-Time CDP Collaboration [!DNL Starter]の概要

Adobe Real-Time CDP Collaboration [!DNL Starter]を使用して、プライバシー重視のデータプロジェクトでライセンスを取得したパートナーと共同作業を行います。 ご自身のCollaboration ライセンスは必要ありません。

ライセンスを取得したパートナーがAdobe Collaborationにユーザーを招待し、そのクレジットを広告主とパブリッシャー間およびブランドとブランド間の両方のパターンで共同ワークフローに使用します。 これらのパターンとその仕組みについて詳しくは、[ コラボレーションパターン ](./collaboration-patterns.md)および[ エンドツーエンドのワークフロー](./end-to-end-workflow.md)のガイドを参照してください。

招待された[!DNL Starter] ユーザーとして、次の操作を実行できます。

* [!DNL Starter] アカウントでコラボレーションデータをオンボーディングして管理します。
* Sourceを使用して、共同プロジェクトで使用するオーディエンスを管理します。
* 効果的なターゲティングとキャンペーン測定を実施するために、パートナーとのオーディエンスの重複に関するインサイトを得ます。
* オーディエンスをアクティベートし、共同キャンペーンのアクティベーションやエンゲージメントのために、パートナーと共有します。

## 前提条件 {#prerequisites}

Collaboration [!DNL Starter]を使い始めるには、お客様の組織とライセンス済みのパートナーの両方が同じリージョンに存在することを確認してください。 Real-Time CDP Prime、Ultimate、またはCollaboration ライセンスを持つパートナーが招待する必要があります。

招待を開始するには、ライセンスを取得したパートナーに次の情報を提供します。

* 連絡先名
* 連絡先メール
* 会社
* 役割（広告主/発行者）：広告主
* 業界

招待状を受け取り、承認した後、Collaboration [!DNL Starter]にアクセスするには、Adobeで無償の販売注文を確認し、署名する必要があります。 招待プロセスについて詳しくは、[Collaborationへの共同作業者の招待 [!DNL Starter]](../connect/establishing-connections.md#invite-non-licensed-collaborator) ガイドを参照してください。

## ガードレール {#guardrails}

次の表を参照して、[!DNL Starter] アカウントに適用される主要なガードレールを理解してください。 これには、オーディエンスのソーシング、データ量、更新頻度、オーディエンスの重複、アクティベーション機能に関する制限が含まれます。

| ガードレール | 説明 |
|----------| ------------|
| オーディエンスソース | **[!DNL Amazon S3]**&#x200B;をソースとしてCollaborationにオーディエンスデータを取り込むことができます。 詳細な手順については、[ オーディエンスソーシング用に [!DNL Amazon S3] を設定する方法](../setup/configure-aws-s3-audience-sourcing.md)を参照してください。 |
| オーディエンス | お客様の[!DNL Starter] アカウントには、次の上限が設定されています。<ul><li>[!DNL AWS S3] バケットからソースされた10 オーディエンス</li><li>合計5,000万のID （オーディエンスデータの行数で計算）</li><li>オーディエンスごとに6日ごとに1回の更新</li></ul> |
| オーディエンスの重複とインサイト | オーディエンスの重複やインサイトをオーディエンスをまたいで実行できる頻度に制限はありません。 [重複を発見してオーディエンスを比較](../collaborate/discover.md)する方法について説明します。 |
| Activation | [!DNL Starter] ユーザーは、招待したパートナーにのみオーディエンスをアクティブ化して共有できます。 外部プラットフォームへの宛先の設定は使用できません。 [ オーディエンスのアクティベーション ](../collaborate/activate.md)の詳細をご覧ください。 |

{style="table-layout:auto"}

## はじめに {#getting-started}

[招待に同意し、利用条件](../connect/establishing-connections.md#accept-invitation-sign-terms)に同意したら、資格情報を使用して[Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}にログインします。 Collaborationを使用する前に、適切なアクセス権と役割をアカウントに付与する必要があります。

このワークフローを使用して[!DNL Starter] アカウントを設定し、パートナーとの共同作業を開始します。

### 管理者アクセスの設定 {#setup-admin-access}

まず、**管理者アクセス** ワークスペースを使用して、必要なアクセス権を付与します。 これにより、Experience Platform製品に対する管理者権限とユーザーアクセス権の両方が確保されます。 初期アクセスの設定方法について詳しくは、[管理者アクセス手順](../setup/starter-admin-access.md)を参照してください。

完了すると、[Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} ホームページの&#x200B;**[!UICONTROL クイックアクセス]** セクションに&#x200B;**[!UICONTROL 権限]**、**[!UICONTROL Experience Platform]**、および&#x200B;**[!UICONTROL Real-Time CDP Collaboration]**&#x200B;が表示されます。

![製品管理者がアクセスを設定すると、権限、Experience Platform、Real-Time CDP Collaborationが表示されるAdobe Experience Cloud ワークスペース。](/help/assets/overview/starter/setup-admin-access.png){zoomable="yes"}

アクセス役割と様々なAdobe Experience Cloud製品について詳しくは、[ アクセス制御の概要](../permissions/overview.md)を参照してください。

### 権限の設定 {#configure-permissions}

管理者権限を持っているので、自分や組織内の他のユーザーに役割と権限を割り当てることができます。 この手順は、Real-Time CDP Collaborationにアクセスする前または他のユーザーが使用できるようにする前に必要です。 詳細な手順については、[権限の設定方法](../setup/starter-permission-controls.md)を参照してください。 Collaborationで使用できる様々な役割と権限について詳しくは、[役割の管理](../permissions/manage-roles.md)のドキュメントを参照してください。

役割と権限が割り当てられたら、Collaborationにアクセスできることを確認します。 [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}に移動し、**[!UICONTROL クイックアクセス]** セクション内の&#x200B;**[!UICONTROL Real-Time CDP Collaboration]**&#x200B;を選択します。 これにより、**[!UICONTROL Adobe Real-Time CDP Collaboration]** ワークスペースが開き、Collaboration機能の使用を開始できます。

### 接続の設定 {#set-up-connections}

次に、次のガイドの手順に従って接続を設定し、パートナーとの共同作業を開始します。

* [Collaboration アカウントの設定](../setup/onboard-account.md)
* [招待パートナーとのつながりを確立](../connect/overview.md)
* [新しいプロジェクトを作成し、パートナーとの共同作業を開始する](../collaborate/overview.md)

### クレジット使用について {#understand-credit-usage}

すべてのCollaboration [!DNL Starter] アクティビティでクレジットが使用されます。 ただし、招待ユーザーとして、これらのクレジットを購入または管理する必要はありません。 招待した共同作業者は、アクティビティに関連するすべてのクレジット使用状況をカバーします。 詳しくは、Collaboration [!DNL Starter]](../setup/starter-credit-usage.md)のドキュメントの[ クレジットの使用状況と使用状況を参照してください。

## 次の手順 {#next-steps}

これで、最初の設定が完了し、安全なコラボレーション用に組織を設定しました。 次に、次のリソースを確認して、Collaboration内でのオーディエンスのソーシングと様々なプロジェクトのユースケースについて説明します。

* [Sourceとオーディエンスの管理](../setup/onboard-audiences.md)
* [ プロジェクトの使用例](../collaborate/overview.md#project-use-cases):
   * [重複を見つけてオーディエンスを比較](../collaborate/discover.md)
   * [オーディエンスをアクティベート](../collaborate/activate.md)
   * [施策のパフォーマンスを測定](../collaborate/measure.md)
