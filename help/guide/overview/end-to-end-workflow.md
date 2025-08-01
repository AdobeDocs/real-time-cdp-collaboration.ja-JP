---
title: エンドツーエンドのワークフロー
description: 共同作業パターンに基づいて、Real-Time CDP Collaborationのエンドツーエンドでの使用ワークフローを理解します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: 8745d6d8da389b552af3da6612bf693230dfb538
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%

---

# エンドツーエンドのワークフロー

{{limited-availability-release-note}}

Adobe Real-Time CDP Collaborationのエンドツーエンドワークフローは、選択した共同作業パターンによって異なります。 このワークフローでは、アカウントの作成とオーディエンスの取得から、接続の形成とプロジェクトの作成に至るまで、共同作業プロジェクトの設定と実行に関する手順の概要を説明します。 このワークフローを理解することは、マーケティング目標を達成するためにプラットフォームの機能を効果的に活用するために不可欠です。

## はじめに

開始する前に、次の主要な概念を十分に理解しておく必要があります。

- **Collaboration パターン**：これらのパターンは、共同作業者の共同作業の方法を定義します。 2 つの異なるパターン、[ 広告主から媒体社へ ](./collaboration-patterns.md#advertiser-to-publisher) と [ ブランドからブランドへ ](./collaboration-patterns.md#brand-to-brand) があります。
- **アカウントロール**：アカウントロールは、プラットフォーム内の機能を決定します。 組織の目標、ブランド、目標に合わせる必要があります。 アカウントの役割には、[ 広告主 ](./roles.md#advertiser) と [ 発行者 ](./roles.md#publisher) の 2 つがあります。
- **ユースケース**：ユースケースでは、Collaborationを活用してマーケティング目標を達成する方法を定義します。 コラボレーションの使用例には、[Discover](./use-cases.md#discover)、[Activate](./use-cases.md#activate)、および [Measure](./use-cases.md#measure) の 3 つがあります。

このガイドでは、3 つのモック共同作業者を使用して、エンドツーエンドのワークフローを説明します。

- **[!UICONTROL Luma]**：アスレチックアパレルブランド。 ターゲットマーケティングキャンペーンを通じて特定のオーディエンスにリーチしたいと考えている広告主です。
- **[!UICONTROL TV Tube]**：デジタルストリーミングプロバイダー。 広告主が使用するオーディエンスデータを提供するパブリッシャーです。
- **[!UICONTROL フィットアパレル]**：別のアスレチックアパレルブランド。 同社は、マーケティング活動を強化するためにオーディエンスデータとインサイトを共有するために共同作業を行う 2 番目の広告主です。

## 広告主からパブリッシャーへのワークフロー {#advertiser-to-publisher-workflow}

スポーツ小売会社の [!UICONTROL Luma] は、ターゲットマーケティングキャンペーンを通じて特定のオーディエンスにリーチするために、デジタルストリーミングプロバイダーの [!UICONTROL TV Tube] との接続を確立したいと考えています。

まず、[!UICONTROL Luma] は広告主の役割を持つ [ アカウントを作成 ](../setup/onboard-account.md) する必要がありますが、[!UICONTROL TV Tube] は発行者の役割を持つアカウントを作成します。

アカウントを確立したら、[!UICONTROL Luma] と [!UICONTROL TV Tube] の両方で [ データ接続とソースオーディエンスの作成 ](../setup/onboard-audiences.md) が必要です。 マーケティングキャンペーンのオーディエンスをアクティブ化するのは [!UICONTROL TV Tube] のみなので、[ 宛先の設定 ](../setup/manage-destinations.md) が必要です。

両方の共同作業者がアカウントを設定すると、プラットフォーム内で [ 接続を作成 ](../connect/establishing-connections.md) する準備が整います。 [!UICONTROL Luma] は、[ パブリッシャーの検出 ](../connect/discover-publishers.md) 機能を使用して [!UICONTROL TV チューブ &#x200B;] を検索し、接続要求を開始します。 [!UICONTROL TV Tube] が接続リクエストを受け入れると、[!UICONTROL Luma] が接続設定を設定して、共同作業の方法を定義します。 [!UICONTROL TV Tube] は、2 つのブランド間に安全なリンクを確立するための接続要求を受け入れます。

接続が確立されると、[!UICONTROL Luma] は [TV Tube](../collaborate/manage-projects.md) との共同作業を開始するために [!UICONTROL &#x200B; プロジェクトを作成 &#x200B;] します。 プロジェクトの設定時に、目標に最適なコラボレーションのユースケース（[ 検出 ](../collaborate/discover.md)、[ アクティブ化 ](../collaborate/activate.md)、[ 測定 ](../collaborate/measure.md) を選択します。

[!UICONTROL Luma] は、[Discover](../collaborate/discover.md) のユースケースを活用して、[!UICONTROL TV Tube] のオーディエンスデータに関するインサイトを得ます。 [!UICONTROL Luma] がターゲットオーディエンスセグメントを識別したら、これらのオーディエンスは [ アクティブ化 ](../collaborate/activate.md) されます。

オーディエンスをアクティブ化した後、[!UICONTROL TV Tube] はターゲットを絞ったマーケティングキャンペーンを実行し、結果を [ 測定 ](../collaborate/measure.md) にアップロードして、キャンペーンの有効性を評価します。

## ブランド間ワークフロー {#brand-to-brand-workflow}

アスレチックアパレルブランドの [!UICONTROL Fit Apparel] は、別のアスレチックアパレルブランドである [!UICONTROL Luma] と連携して、オーディエンスデータとインサイトを共有し、マーケティング活動を強化したいと考えています。

アカウントを確立した後、[!UICONTROL &#x200B; アパレルに適合 &#x200B;] と [!UICONTROL Luma] の両方で [ データ接続とソースオーディエンスの作成 ](../setup/onboard-audiences.md) が必要になります。 [!UICONTROL &#x200B; アパレルに適合 &#x200B;] と [!UICONTROL Luma] の両方がマーケティングキャンペーンのオーディエンスをアクティブ化するので、両方とも [ 宛先を設定 ](../setup/manage-destinations.md) する必要があります。

オーディエンスをソーシングした後は、プラットフォーム内で [!UICONTROL &#x200B; アパレルに適合 &#x200B;] および [!UICONTROL Luma] [ 接続を形成 ](../connect/establishing-connections.md) し、オーディエンスデータを安全に共有します。 これを行うには、[ プライベート接続の招待 ](../connect/establishing-connections.md#private-connection-invite) 機能を利用する必要があります。 [!UICONTROL Luma] は接続コードを [!UICONTROL Fit Apparel] と共有し、そのコードを使用して接続リクエストを開始します。 [!UICONTROL Luma] が接続リクエストを受け入れると、[!UICONTROL Fit Apparel] が接続設定を設定し、共同作業の方法を定義します。 設定の [!UICONTROL &#x200B; アパレルに合わせる &#x200B;] は、両方の共同作業者がマーケティングキャンペーンのオーディエンスをアクティブ化できることを指定します。 接続を完了するために、[!UICONTROL Luma] は、2 つのブランド間に安全なリンクを確立するリクエストを受け入れます。

接続が確立されると、[!UICONTROL &#x200B; アパレルにフィット &#x200B;][ プロジェクトを作成 ](../collaborate/manage-projects.md) して、[!UICONTROL Luma] とのコラボレーションを開始します。 プロジェクトの設定時に、目標に最適なコラボレーションのユースケース（[ 検出 ](../collaborate/discover.md)、[ アクティブ化 ](../collaborate/activate.md)、[ 測定 ](../collaborate/measure.md) を選択します。

[!UICONTROL &#x200B; アパレルにフィット &#x200B;] と [!UICONTROL Luma] の両方が [ 検出 ](../collaborate/discover.md) のユースケースを使用して、お互いのオーディエンスデータに関するインサイトを得ることができます。 貴重なオーディエンスセグメントを特定したら、マーケティングキャンペーン用に選択したオーディエンスを [ アクティブ化 ](../collaborate/activate.md) します。

最後に、キャンペーンを実行した後、両方のブランドが結果にデータをアップロードし [ 測定 ](../collaborate/measure.md)、共同作業の有効性を評価します。
