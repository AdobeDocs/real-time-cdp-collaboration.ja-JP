---
title: 接続の概要
description: Real-Time CDP Collaborationでの接続について説明します。
audience: publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
source-git-commit: 5c08738cdc8e1e208203ee1f9a1cf1891b5b07cb
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# 接続の概要

{{limited-availability-release-note}}

コラボレーターがキャンペーンで連携する前に、連携を確立する必要があります。 この接続を使用すると、オーディエンスのアクティブ化、プロジェクトの作成およびキャンペーンのパフォーマンスに関するレポートの実行を行うことができます。

選択したコラボレーションパターンに基づいて接続が確立されます。 Collaborationは、広告主から媒体社へ、ブランドからブランドへ、広告主から広告プラットフォームという 3 つの主要なコラボレーションパターンをサポートしています。 これらのパターンについて詳しくは、「[ コラボレーションパターン ](/help/guide/overview/collaboration-patterns.md) ガイドを参照してください。

接続を確立する方法については、コラボレーションパターンに対応する以下の節を参照してください。

- [広告主とパブリッシャーの接続](#advertiser-to-publisher-connection)
- [ブランド間の接続](#brand-to-brand-connection)
- [広告主と広告プラットフォームの接続](#advertiser-to-advertising-platform-connection)

## 広告主とパブリッシャーの接続 {#advertiser-to-publisher-connection}

![ 広告主とパブリッシャーの接続プロセスの概要図。](/help/assets/connect/establish-connection/advertiser-publisher-flow.png){zoomable="yes"}

広告主からパブリッシャーへのパターンでは、広告主は **[!UICONTROL パブリッシャーの検出]** ワークスペースを通じて、連携するパブリッシャーを検出し、接続の招待を送信します。 次に、パブリッシャーは招待を確認して受け入れ、広告主が接続設定を提案できるようにします。 パブリッシャーが接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトでの作業を開始できます。

### の概要

広告主とパブリッシャーの間の接続を確立するには、次の手順が必要です。

1. [ パブリッシャーの検出 ](./discover-collaborators.md)：広告主は、共同作業を行う潜在的なパブリッシャーを特定します。
2. [ 招待を送信 ](./establishing-connections.md#send-invite)：広告主は、選択したパブリッシャーに接続招待を送信します。
3. [ 招待を受け入れる ](./establishing-connections.md#accept-invite)：パブリッシャーが招待をレビューし、承認します。
4. [ 接続設定の指定 ](./establishing-connections.md#configure-connection-settings)：広告主は接続設定を指定し、レビュー用にパブリッシャーに送信します。
5. [ 接続設定の確認 ](./establishing-connections.md#review-connection-settings)：パブリッシャーは接続設定を確認し、受け入れるか拒否します。 許可された場合、接続が確立されます。 拒否された場合、公開者は製品外のリビジョンに関するフィードバックを提供できます。 その後、広告主は設定を修正し、レビュー用に再送信できます。

接続設定を受け入れると、接続が確立され、共同作業者は [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) してキャンペーンでの共同作業を開始する準備が整います。

## ブランド間の接続 {#brand-to-brand-connection}

![ ブランド間接続プロセスの概要図。](/help/assets/connect/establish-connection/brand-to-brand-flow.png){zoomable="yes"}

>[!TIP]
>
>**ブランド** という用語は、Collaboration以外の会社またはブランドを参照するために使用されます。 **共同作業者** という用語は、広告主であるか媒体社であるかに関係なく、Collaborationで関連性を形成できる任意のアカウントを指します。

ブランド間パターンでは、商品外でコミュニケーションを取った 2 つのブランドが、「プライベート接続への招待 [ を使用して、Collaborationで直接接続でき ](#private-connection-invite) す。 ブランドは、広告主または公開者のいずれかです。 このパターンは、2 人の広告主や 2 人のパブリッシャーなど、従来の広告主 – パブリッシャーモデルに適合しない可能性のあるブランドで特に役立ちます。

まず、共同作業者がプライベート接続の招待状を別の共同作業者に送信します。 受信者が招待を確認して承諾すると、所有者が接続設定を提案できます。 受信者が接続設定を受け入れると、接続が確立され、両方の共同作業者がプロジェクトでの作業を開始できます。

### の概要

>[!TIP]
>
>接続プロセスについて話し合う際には、**owner** と **recipient** が区別されます。 所有者は、招待を送信して接続を開始する共同作業者であり、受信者は、招待を受信してレビューする共同作業者です。

2 つのブランド間の接続プロセスには、いくつかの手順が必要です。 接続プロセスを開始する前に、次の前提条件を満たす必要があります。

1. 2 つのブランドが製品外でコミュニケーションを取り、潜在的な接続について話し合っています。
1. Collaborationのブランド [ アカウントの作成 ](/help/guide/setup/onboard-account.md) をまだ行っていない場合は、適切なロールタイプ（広告主またはパブリッシャー）を必ず選択します。

前提条件が満たされたら、接続プロセスを開始できます。 次の手順でプロセスの概要を説明します。

1. [ プライベート接続の招待を送信 ](./establishing-connections.md#private-connection-invite):1 人の共同作業者が別の共同作業者にプライベート接続の招待を送信します。
2. [ プライベート接続への招待を受け入れる ](./establishing-connections.md#accept-invite)：受信者がプライベート接続への招待を確認して承諾します。
3. [ 接続設定の指定 ](./establishing-connections.md#configure-connection-settings)：所有者が接続設定を指定し、レビューと承認を受けるために受信者に送信します。
4. [ 接続設定の確認 ](./establishing-connections.md#review-connection-settings)：受信者は接続設定を確認し、受け入れるか拒否します。

接続設定を受け入れると、接続が確立され、共同作業者は [ プロジェクトを作成 ](/help/guide/collaborate/manage-projects.md#create-project) してキャンペーンでの共同作業を開始する準備が整います。

## 広告主と広告プラットフォームの接続 {#advertiser-to-advertising-platform-connection}

広告主と広告プラットフォームの連携プロセスにより、広告主はAmazon Marketing Cloud（AMC）などのサードパーティの広告プラットフォームと連携して、マーケティング機能を強化できます。

### の概要

広告主と広告プラットフォームの間の接続プロセスには、いくつかのステップが含まれます。 接続プロセスが始まる前に、広告プラットフォームのアクティブなアカウントがあり、サービスの使用が承認されていることを確認してください。 接続プロセスの概要を次に示します。

1. [ 広告プラットフォームを見つける ](./discover-collaborators.md)：広告主は、共同作業を行う潜在的な広告プラットフォームを特定します。
2. [ 広告プラットフォームへの接続 ](./advertising-platforms/overview.md#advertising-platforms-overview)：広告主は、接続する広告プラットフォームを選択することで接続プロセスを開始し、プロンプトに従って接続を認証および認証します。
