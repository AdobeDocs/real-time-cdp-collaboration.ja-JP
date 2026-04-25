---
title: 接続の概要
description: Real-Time CDP Collaborationのつながりについて詳しく見る。
audience: publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 419dde94-fee2-4dc1-b25d-cf79b7e57ec0
TQID: https://experienceleague.adobe.com/ZF3bqoR0XRv2G7abRULz1ElRgk5xLCZySHylrqzPqg0
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 0%

---

# 接続の概要

{{limited-availability-release-note}}

共同作業者がキャンペーンで一緒に作業する前に、接続を確立する必要があります。 この連携により、オーディエンスのアクティベーション、プロジェクトの作成、キャンペーンのパフォーマンスに関するレポートの実行が可能になります。

選択したコラボレーションパターンに基づいて、接続が確立されます。 Collaborationは、広告主とパブリッシャー間、ブランドとブランド間、広告主と広告プラットフォームの3つの主要なコラボレーションパターンをサポートしています。 これらのパターンについて詳しくは、[ コラボレーションパターン ](/help/guide/overview/collaboration-patterns.md) ガイドを参照してください。

接続を確立する方法については、コラボレーションパターンに対応する以下の節を参照してください。

- [広告主とパブリッシャーの接続](#advertiser-to-publisher-connection)
- [ブランドとのつながり](#brand-to-brand-connection)
- [広告主と広告プラットフォームの連携](#advertiser-to-advertising-platform-connection)

## 広告主とパブリッシャーの接続 {#advertiser-to-publisher-connection}

![広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

広告主とパブリッシャー間のパターンでは、広告主は&#x200B;**[!UICONTROL Discover publishers]** ワークスペースを通じて使用するパブリッシャーを検出し、接続招待を送信します。 その後、パブリッシャーは招待を確認して受け入れ、広告主が接続設定を提案できるようにします。 パブリッシャーが接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトで共同作業を開始できます。

### 概要

広告主とパブリッシャー間の接続を確立するには、次の手順を実行します。

1. [ パブリッシャーを見つける](./discover-collaborators.md)：広告主は、共同作業を行う潜在的なパブリッシャーを特定します。
2. [招待を送信](./establishing-connections.md#send-invite)：広告主は、選択した発行者に接続招待を送信します。
3. [招待を承認](./establishing-connections.md#accept-invite)：発行者が招待をレビューし、承認します。
4. [接続設定の設定](./establishing-connections.md#configure-connection-settings)：広告主は接続設定を設定し、レビューのためにパブリッシャーに送信します。
5. [接続設定を確認](./establishing-connections.md#review-connection-settings)：発行者は接続設定を確認し、それを承認または拒否します。 受け入れたら、接続が確立されます。 拒否された場合、パブリッシャーは製品外のリビジョンに対するフィードバックを提供できます。 その後、広告主は設定を変更し、レビューのために再送信できます。

接続設定が承認されると、接続が確立され、共同作業者は[ プロジェクトを作成](/help/guide/collaborate/manage-projects.md#create-project)してキャンペーンでの共同作業を開始する準備が整います。

## ブランドとのつながり {#brand-to-brand-connection}

![ ブランド間の接続プロセスの概要ダイアグラム。](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>**brand**&#x200B;という用語は、Collaboration以外の会社またはブランドを表すために使用されます。 **共同作業者**&#x200B;という用語は、広告主であるかパブリッシャーであるかを問わず、Collaborationで接続を形成できる任意のアカウントを指します。

ブランドとブランドのパターンでは、製品外でコミュニケーションを取った2つのブランドが、[ プライベート接続の招待](#private-connection-invite)を使用してCollaborationで直接接続できます。 ブランドには、広告主とパブリッシャーのどちらかが含まれます。 このパターンは、2つの広告主または2つのパブリッシャーなど、従来の広告主 – パブリッシャーのモデルに適合しない可能性があるブランドに特に便利です。

まず、共同作業者が別の共同作業者にプライベート接続招待を送信します。 受信者は招待を確認して受け入れ、所有者が接続設定を提案できるようにします。 受信者が接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトで共同作業を開始できます。

### 概要

>[!TIP]
>
>接続プロセスについて話し合う際に、**所有者**&#x200B;と&#x200B;**受信者**&#x200B;の間で区別が生じます。 所有者は、招待を送信して接続を開始する共同作業者で、受信者は、招待を受信してレビューする共同作業者です。

2つのブランドの接続プロセスには、いくつかのステップがあります。 接続プロセスを開始する前に、いくつかの前提条件を満たす必要があります。

1. 2つのブランドが製品外でコミュニケーションを図り、潜在的なつながりを議論します。
1. Collaborationのブランド [create accounts](/help/guide/setup/onboard-account.md)がまだ存在しない場合は、適切なロールタイプ（広告主またはパブリッシャー）を選択してください。

前提条件が満たされると、接続プロセスを開始できます。 プロセスの概要を以下に示します。

1. [ プライベート接続の招待を送信](./establishing-connections.md#private-connection-invite):1人の共同作業者が別の共同作業者にプライベート接続の招待を送信します。
2. [ プライベート接続の招待を受け入れる](./establishing-connections.md#accept-invite)：受信者はプライベート接続の招待をレビューし、受け入れます。
3. [接続設定の設定](./establishing-connections.md#configure-connection-settings)：所有者は接続設定を設定し、レビューと承認のために受信者に送信します。
4. [接続設定を確認](./establishing-connections.md#review-connection-settings)：受信者は接続設定を確認し、それを承認または拒否します。

接続設定が承認されると、接続が確立され、共同作業者は[ プロジェクトを作成](/help/guide/collaborate/manage-projects.md#create-project)してキャンペーンでの共同作業を開始する準備が整います。

## 広告主と広告プラットフォームの連携 {#advertiser-to-advertising-platform-connection}

広告主と広告プラットフォームの連携プロセスにより、広告主はAmazon Marketing Cloud（AMC）などのサードパーティの広告プラットフォームと連携し、マーケティング能力を向上させることができます。

### 概要

広告主と広告プラットフォームの接続プロセスには、いくつかのステップがあります。 接続プロセスを開始する前に、広告プラットフォームのアクティブなアカウントを持ち、そのサービスの使用が承認されていることを確認します。 接続プロセスの概要を次の手順で説明します。

1. [広告プラットフォームを見つける](./discover-collaborators.md)：広告主は、共同作業を行う潜在的な広告プラットフォームを特定します。
2. [広告プラットフォームに接続](./advertising-platforms/overview.md#advertising-platforms-overview)：広告主は、接続する広告プラットフォームを選択して接続プロセスを開始し、接続を認証して承認するためのプロンプトに従います。
