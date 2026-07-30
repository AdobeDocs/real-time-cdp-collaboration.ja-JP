---
title: エンドツーエンドのワークフロー
description: 共同作業パターンに基づいて、Real-Time CDP Collaborationを使用するエンドツーエンドのワークフローを把握します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
TQID: https://experienceleague.adobe.com/9edtg5tMbnB3BrdLrDkcHQ-AjBNOqMFGojAja3NCwCs
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 4dba099a1bf484d9e2dfa71d5ad21a1ac076d794
workflow-type: tm+mt
source-wordcount: 1738
ht-degree: 0%

---

# エンドツーエンドのワークフロー

{{limited-availability-release-note}}

Adobe Real-Time CDP Collaborationでは、選択した共同作業パターンによって、エンドツーエンドのワークフローが異なります。 このワークフローでは、アカウントの作成、オーディエンスのソーシング、接続の形成、プロジェクトの作成など、コラボレーションプロジェクトの設定と実行に関する手順の概要を説明します。 このワークフローを理解することは、マーケティング目標を達成するためにプラットフォームの機能を効果的に活用するために不可欠です。

## はじめに

まず、次の重要な概念をしっかりと理解していることを確認してください。

- **Collaboration パターン**：これらのパターンは、共同作業者の共同作業の方法を定義します。 5つの異なるパターンがあります。
  - [広告主とパブリッシャー](./collaboration-patterns.md#advertiser-to-publisher)
  - [ブランド間](./collaboration-patterns.md#brand-to-brand)
  - [広告主とデータのパートナー](./collaboration-patterns.md#advertiser-to-data-partner)
  - [agency-to-publisher](./collaboration-patterns.md#agency-to-publisher)
  - [広告主と代理店のプラットフォーム](./collaboration-patterns.md#advertiser-to-agency-platform)
- **アカウントの役割**: アカウントの役割によって、プラットフォーム内での機能が決まります。 作成するコンテンツは、組織の目標、ブランド、目的に合わせる必要があります。 アカウントには、[広告主](./roles.md#advertiser)、[発行者](./roles.md#publisher)、[代理店](./roles.md#agency)、[&#x200B; データパートナー](./roles.md#data-partner)の4つの役割があります。
- **ユースケース**：ユースケースは、Collaborationを活用してマーケティング目標を達成する方法を定義します。 コラボレーションの使用例は3つあります：[Discover](./use-cases.md#discover)、[Activate](./use-cases.md#activate)、[Measure](./use-cases.md#measure)。

このガイドでは、3人のモックコラボレーターがエンドツーエンドのワークフローを説明します。

- **[!UICONTROL Luma]**：スポーツ衣料ブランド。 ターゲットマーケティング施策を通じて特定のオーディエンスにリーチしたい広告主です。
- **[!UICONTROL TV Tube]**: デジタルストリーミングプロバイダー。 広告主が使用するオーディエンスデータを提供するパブリッシャーです。
- **[!UICONTROL フィットアパレル]**：別のスポーツ衣料ブランド。 マーケティング活動を強化するために、オーディエンスデータとインサイトを共有するために連携したいと考えている、2番目の広告主です。
- **[!UICONTROL Agency99]**: メディアエージェンシー。 同社は、ワークスペース内で複数の顧客アカウントを管理し、パブリッシャーや広告主とつながっています。
- **[!UICONTROL DataM8]**：サードパーティのデータプロバイダー。 広告主が利用するためのオーディエンスデータを提供します。
- **[!UICONTROL Holdco]**：社内の代理店チームがクライアントキャンペーンを管理するために使用する、マーケティングおよび広告サービスプラットフォームを保有する代理店。

## 広告主とパブリッシャーのワークフロー {#advertiser-to-publisher-workflow}

スポーツ小売企業の[!UICONTROL Luma]は、デジタルストリーミングプロバイダーの[!UICONTROL TV Tube]とつながり、ターゲットマーケティングキャンペーンを通じて特定のオーディエンスにリーチしたいと考えています。

開始するには、[!UICONTROL Luma]が[広告主の役割でアカウント &#x200B;](../setup/onboard-account.md)を作成し、[!UICONTROL TV Tube]がパブリッシャーの役割でアカウントを作成する必要があります。

アカウントを設定した後、[!UICONTROL Luma]と[!UICONTROL TV Tube]の両方が[&#x200B; データ接続とソースオーディエンスを作成する必要があります](../setup/onboard-audiences.md)。 マーケティングキャンペーン用にオーディエンスをアクティブ化するのは[!UICONTROL TV Tube]のみなので、[宛先を設定](../destinations/manage-destinations.md)する必要があります。

両方の共同作業者がアカウントを設定したら、プラットフォーム内で[接続を形成する](../connect/establishing-connections.md)準備が整います。 [!UICONTROL Luma]は、[共同作業者の検索](../connect/discover-collaborators.md)機能を使用して[!UICONTROL TV Tube]を検索し、接続リクエストを開始します。 [!UICONTROL TV Tube]が接続要求を受け入れた後、[!UICONTROL Luma]は接続設定を設定して、共同作業の方法を定義します。 [!UICONTROL TV Tube]は、2つのブランド間の安全なリンクを確立するための接続要求を受け入れました。

接続が確立されると、[!UICONTROL Luma] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成し、[!UICONTROL TV Tube]との共同作業を開始します。 プロジェクトのセットアップ中に、目的に最適なコラボレーションユースケースを選択します：[見つける](../collaborate/discover.md)、[&#x200B; アクティブ化](../collaborate/activate.md)、[測定](../collaborate/measure.md)。

[!UICONTROL Luma]は、[Discover](../collaborate/discover.md)のユースケースを活用して、[!UICONTROL TV Tube]のオーディエンスデータに関するインサイトを得ます。 [!UICONTROL Luma]がターゲットオーディエンスセグメントを特定すると、これらのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)します。

オーディエンスをアクティベートした後、[!UICONTROL TV Tube]がターゲットマーケティング施策を実行し、データを[Measure](../collaborate/measure.md)にアップロードして、施策の効果を評価します。

## ブランド間ワークフロー {#brand-to-brand-workflow}

アスレティックアパレルブランドの[!UICONTROL Fit Apparel]は、別のアスレティックアパレルブランドの[!UICONTROL Luma]と協力して、オーディエンスデータとインサイトを共有し、マーケティング活動を強化したいと考えています。

アカウントを設定した後、[!UICONTROL Fit Apparel]と[!UICONTROL Luma]の両方が[&#x200B; データ接続とソースオーディエンスを作成する必要があります](../setup/onboard-audiences.md)。 [!UICONTROL Fit Apparel]と[!UICONTROL Luma]の両方がマーケティングキャンペーンのオーディエンスをアクティブ化するため、両方で[宛先を設定](../destinations/manage-destinations.md)する必要があります。

オーディエンスをソーシングした後、[!UICONTROL Fit Apparel]と[!UICONTROL Luma] [は、プラットフォーム内で接続](../connect/establishing-connections.md)を形成して、オーディエンスデータを安全に共有します。 そのためには、[&#x200B; プライベート接続の招待](../connect/establishing-connections.md#private-connection-invite)機能を利用する必要があります。 [!UICONTROL Luma]は接続コードを[!UICONTROL Fit Apparel]と共有し、その後、接続コードを使用して接続要求を開始します。 [!UICONTROL Luma]が接続要求を受け入れた後、[!UICONTROL Fit Apparel]は接続設定を設定して、共同作業の方法を定義します。 設定では、[!UICONTROL Fit Apparel]は、両方の共同作業者がマーケティングキャンペーン用にオーディエンスをアクティブ化できることを指定します。 接続を完了するために、[!UICONTROL Luma]は2つのブランド間の安全なリンクを確立するリクエストを受け入れます。

接続が確立されると、[!UICONTROL Fit Apparel] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成して、[!UICONTROL Luma]との共同作業を開始します。 プロジェクトのセットアップ中に、目的に最適なコラボレーションユースケースを選択します：[見つける](../collaborate/discover.md)、[&#x200B; アクティブ化](../collaborate/activate.md)、[測定](../collaborate/measure.md)。

[!UICONTROL Fit Apparel]と[!UICONTROL Luma]は、両方とも[Discover](../collaborate/discover.md)のユースケースを使用して、お互いのオーディエンスデータに関するインサイトを得ることができます。 価値のあるオーディエンスセグメントを特定し、マーケティングキャンペーン用に選択したオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)します。

最後に、両方のブランドがキャンペーンを実行した後、データを[Measure](../collaborate/measure.md)にアップロードし、結果を確認して、共同作業の効果を評価します。

## 広告主と広告プラットフォームのワークフロー {#advertiser-to-advertising-platform-workflow}

[!DNL AMC]のID解決とターゲティングツールを活用してマーケティング機能を向上させるために、[!DNL Amazon Marketing Cloud] （[!DNL AMC]）と連携したいと考えているスポーツ用小売り企業[!UICONTROL Luma]です。 Lumaは既にアクティブな[!DNL Amazon Advertising] アカウントを持っており、[!DNL AMC]の使用が承認されています。

開始するには、[!UICONTROL Luma]が広告主の役割を持つアカウント [&#128279;](../setup/onboard-account.md)を作成する必要があります。 アカウントを確立した後、[!UICONTROL Luma]は[&#x200B; データ接続とソースオーディエンス &#x200B;](../setup/onboard-audiences.md)を作成する必要があります。 [!UICONTROL Luma]はマーケティングキャンペーン用にオーディエンスをアクティブ化するので、[宛先を設定](../destinations/manage-destinations.md)する必要があります。

[!UICONTROL Luma]がアカウントを設定したら、プラットフォーム内で[!DNL AMC]との接続[&#128279;](../connect/establishing-connections.md)を形成する準備が整います。 [!UICONTROL Luma]は、[共同作業者を見つける](../connect/discover-collaborators.md)機能を使用して、[!UICONTROL Amazon Marketing Cloud]および[接続リクエストを開始](../connect/advertising-platforms/amc.md)します。 [!DNL Amazon] サインインページを介して接続を認証および承認した後、[!DNL AMC]との接続が確立されます。

接続が確立されると、[!UICONTROL Luma] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成して[!DNL AMC]との共同作業を開始します。 ユースケースなどの接続設定は、広告プラットフォームに応じて事前に設定されています。 [!DNL AMC]の場合、使用可能な使用例は[Discover](../collaborate/advertising-platforms/amc.md#discover)です。

[!UICONTROL Luma]は、[Discover](../collaborate/advertising-platforms/amc.md#discover)の使用例を活用して、[!DNL AMC]からインサイトとオーディエンスデータを取得します。 これらのインサイトを使用することで、[!UICONTROL Luma]はマーケティング戦略を最適化し、キャンペーンの効果を向上させることができます。

## 広告主とデータ間のパートナーのワークフロー {#advertiser-to-data-partner-workflow}

スポーツ用小売メーカーの[!UICONTROL Luma]は、顧客プロファイルを充実させ、オーディエンスのターゲティングを改善するために、サードパーティデータプロバイダーの[!UICONTROL DataM8]と協力したいと考えています。

開始するには、[!UICONTROL Luma]が[広告主の役割でアカウント &#x200B;](../setup/onboard-account.md)を作成し、[!UICONTROL DataM8]がデータパートナーの役割でアカウントを作成する必要があります。

アカウントを確立した後、[!UICONTROL Luma]と[!UICONTROL DataM8]の両方が[&#x200B; データ接続とソースオーディエンスを作成する必要があります](../setup/onboard-audiences.md)。 両方の共同作業者は、マーケティングキャンペーンのオーディエンスをアクティブ化できるため、それぞれ[宛先を設定](../destinations/manage-destinations.md)する必要があります。

両方の共同作業者がアカウントを設定したら、プラットフォーム内で[接続を形成する](../connect/establishing-connections.md)準備が整います。 [!UICONTROL Luma]は、[共同作業者の検索](../collaborate/discover.md)機能を使用して[!UICONTROL DataM8]を検索し、接続要求を開始します。 [!UICONTROL DataM8]が接続要求を受け入れた後、[!UICONTROL Luma]は接続設定を設定して、共同作業の方法を定義します。 [!UICONTROL DataM8]は、2人の共同作業者の間に安全なリンクを確立するための接続要求を受け入れました。

接続が確立されると、[!UICONTROL Luma] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成し、[!UICONTROL DataM8]との共同作業を開始します。 プロジェクトのセットアップ中に、目的に最適なコラボレーションユースケースを選択します：[見つける](../collaborate/discover.md)、[&#x200B; アクティブ化](../collaborate/activate.md)、[測定](../collaborate/measure.md)。

[!UICONTROL Luma]は、[Discover](../collaborate/discover.md)の使用例を活用して、[!UICONTROL DataM8]のオーディエンスデータに関するインサイトを得ます。 [!UICONTROL Luma]がターゲットオーディエンスセグメントを特定すると、これらのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)します。

[!UICONTROL DataM8]は、そのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)して[!UICONTROL Luma]にすることもできます。 [!UICONTROL Luma]は、これらの機能を使用して、顧客プロファイルにサードパーティの属性を追加し、オーディエンス構成を分析します。 強化されたデータをCDPで直接利用できるようにすることで、[!UICONTROL Luma]は、管理された環境外にデータを移動することなく、より正確なオーディエンスを構築し、有料メディアの宛先にアクティベートすることができます。

## 代理店とパブリッシャー間のワークフロー {#agency-to-publisher-workflow}

メディア代理店である[!UICONTROL Agency99]は、デジタルストリーミングプロバイダーである[!UICONTROL TV Tube]と協力して、ターゲットマーケティングキャンペーンを通じて特定のオーディエンスにリーチしたいと考えています。

開始するには、[!UICONTROL Agency99]が[&#x200B; エージェンシーの役割でアカウント &#x200B;](../setup/onboard-account.md)を作成し、[!UICONTROL TV Tube]がパブリッシャーの役割でアカウントを作成する必要があります。

アカウントを設定した後、[!UICONTROL Agency99]と[!UICONTROL TV Tube]の両方が[&#x200B; データ接続とソースオーディエンスを作成する必要があります](../setup/onboard-audiences.md)。 [!UICONTROL Agency99]は、ワークスペース内でクライアント サブアカウントとソース クライアント データを設定します。 マーケティングキャンペーン用にオーディエンスをアクティブ化するのは[!UICONTROL TV Tube]のみなので、[宛先を設定](../destinations/manage-destinations.md)する必要があります。

両方の共同作業者がアカウントを設定したら、プラットフォーム内で[接続を形成する](../connect/establishing-connections.md)準備が整います。 [!UICONTROL Agency99]は、[共同作業者の検索](../collaborate/discover.md)機能を使用して[!UICONTROL TV Tube]を検索し、接続要求を開始します。 [!UICONTROL Agency99]は、[!UICONTROL TV Tube]と共同作業を行う1人または複数のクライアントに対してこれを行います。 [!UICONTROL TV Tube]が接続要求を受け入れた後、[!UICONTROL Agency99]は接続設定を設定して、各コラボレーション方法を定義します。 [!UICONTROL TV Tube]は、2つのブランド間の安全なリンクを確立するための接続要求を受け入れました。

接続が確立されると、[!UICONTROL Agency99] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成し、各クライアントサブアカウントで[!UICONTROL TV Tube]との共同作業を開始します。 プロジェクトのセットアップ中に、目的に最適なコラボレーションユースケースを選択します：[見つける](../collaborate/discover.md)、[&#x200B; アクティブ化](../collaborate/activate.md)、[測定](../collaborate/measure.md)。

[!UICONTROL Agency99]は、[Discover](../collaborate/discover.md)の使用例を活用して、[!UICONTROL TV Tube]の視聴者データに関するインサイトを得ます。 [!UICONTROL Agency99]がターゲットオーディエンスセグメントを特定すると、これらのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)します。

オーディエンスをアクティベートした後、[!UICONTROL TV Tube]がターゲットマーケティング施策を実行し、データを[measure](../collaborate/measure.md)にアップロードして、施策の効果を評価します。

## 広告主と代理店のプラットフォームのワークフロー {#advertiser-to-agency-platform-workflow}

スポーツ用小売メーカーの[!UICONTROL Luma]は、代理店プラットフォームの[!UICONTROL Holdco]と協力してデータを共有し、有料メディアのインサイトを受け取りたいと考えています。

開始するには、[!UICONTROL Luma]が[広告主の役割でアカウント &#x200B;](../setup/onboard-account.md)を作成し、[!UICONTROL Holdco]が代理店の役割でアカウントを作成する必要があります。 

アカウントを確立した後、[!UICONTROL Luma]と[!UICONTROL Holdco]の両方が[&#x200B; データ接続とソースオーディエンスを作成する必要があります](../setup/onboard-audiences.md)。 両方の共同作業者は、マーケティングキャンペーンのオーディエンスをアクティブ化できるため、それぞれ[宛先を設定](../destinations/manage-destinations.md)する必要があります。 

両方の共同作業者がアカウントを設定したら、プラットフォーム内で[接続を形成する](../connect/establishing-connections.md)準備が整います。 [!UICONTROL Luma]は、[共同作業者の検索](../collaborate/discover.md)機能を使用して、[!UICONTROL Holdco]を検索し、接続要求を開始します。 [!UICONTROL Holdco]が接続要求を受け入れた後、[!UICONTROL Luma]は接続設定を設定して、共同作業の方法を定義します。

[!UICONTROL Holdco]は、2人の共同作業者の間に安全なリンクを確立するための接続要求を受け入れました。

接続が確立されると、[!UICONTROL Luma] [はプロジェクト &#x200B;](../collaborate/manage-projects.md)を作成して、[!UICONTROL Holdco]との共同作業を開始します。 プロジェクトのセットアップ中に、目的に最適なコラボレーションユースケースを選択します：[見つける](../collaborate/discover.md)、[&#x200B; アクティブ化](../collaborate/activate.md)、[測定](../collaborate/measure.md)。

[!UICONTROL Luma]は、[Discover](../collaborate/discover.md)の使用例を活用して、[!UICONTROL Holdco]のオーディエンスデータに関するインサイトを得ます。 [!UICONTROL Luma]がターゲットオーディエンスセグメントを特定すると、これらのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)します。

[!UICONTROL Holdco]は、そのオーディエンスを[&#x200B; アクティブ化](../collaborate/activate.md)して[!UICONTROL Luma]にすることもできます。 [!UICONTROL Luma]は、これらの機能を使用して、インサイト、CDP プロファイルの追加、オウンドメディアオーケストレーションのために、代理店が実行するキャンペーンから有料メディアインサイトを受け取ります。
