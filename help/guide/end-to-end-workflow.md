---
title: エンドツーエンドのワークフロー
description: 広告主またはパブリッシャーとしてReal-Time CDP Collaborationを使用するエンドツーエンドのワークフローを理解する
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 90f9341e-5dd7-4521-a602-edb0263838c5
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# エンドツーエンドのワークフロー

{{limited-availability-release-note}}

Adobe Real-Time Customer Data Platform（CDP）Collaborationを使用すると、広告主やパブリッシャーは、プライバシーを中心とした方法でキャンペーンに関する共同作業を行うことができます。 このページでは、広告主やパブリッシャーとして製品を最大限に活用するワークフローについて説明します。

## 広告主のエンドツーエンドワークフロー {#advertiser}

広告主は、まずReal-Time CDP Collaborationに [ 会社をオンボーディング ](/help/guide/setup/onboard-account.md) します。 [ 設定ページ ](/help/guide/setup/setup-overview.md) を使用して、会社設定を送信して編集し、使用する優先一致キーを追加し、取り込むデータを決定します。 最初のリリースでは、Adobe Experience Platformのみから [ オーディエンスを読み込む ](/help/guide/setup/onboard-audiences.md) ことができます。

![ 広告主を検出、アクティブ化、測定します。](/help/assets/end-to-end-workflow/discover-activate-measure.png)

[ 検出タブを使用して、キャンペーンで使用するパブリッシャーを検索 ](/help/guide/connect/discover-publishers.md) します。 パブリッシャーに問い合わせて、製品外のコラボレーション用語について話し合います。 条件のセットに同意したら、[ 接続の招待を送信 ](/help/guide/connect/establishing-connections.md) し、パブリッシャーと接続するためのコラボレーション設定を提案できます。

パブリッシャーが接続リクエストを受け入れたら、組織と組織の間で重複するオーディエンスを調査する時間です。 キャンペーンのプロジェクトを設定し [ 重複レポートを実行 ](/help/guide/collaborate/discover.md)、コラボレーションのユースケース（ターゲティング、抑制など）に応じて、次の広告キャンペーンに最適なオーディエンスを見つけます。

理想的なオーディエンスを見つけたら、次は [ アクティブ化 ](/help/guide/collaborate/activate.md) します。

コラボレーションループの最後のステップは [ 測定 ](/help/guide/collaborate/measure.md) です。 ビジネス結果を測定したり、把握したりするには、広告ログなどの測定データをアップロードし、プログラムに用意されているレポートを実行して、オーディエンスのパフォーマンスを把握します。

## パブリッシャーのエンドツーエンドワークフロー {#publisher}

パブリッシャーとして、まず [ 会社のオンボーディング ](/help/guide/setup/onboard-account.md) をReal-Time CDP Collaborationに配置します。 [ 設定ページ ](/help/guide/setup/setup-overview.md) を使用して、様々なカンパニー設定を編集します。

読み込むオーディエンスデータと、製品の **[!UICONTROL 接続]** エリアで接続を検討している広告主に対して検出可能および表示可能にするオーディエンスを決定します。

オーディエンスをReal-Time CDP Collaborationに読み込む場合は、オーディエンスにタグ付けおよび分類を行ってください。 Real-Time CDP Collaborationは、オーディエンスの分類については、確立された [IAB 分類 ](https://www.iab.com/guidelines/content-taxonomy/){target="_blank"} に従います。

連携する広告主を決定し、広告主に連絡して製品外の協力条件について話し合います。 条件のセットに同意したら、広告主が正式な接続の招待を延長してあなたと接続するのを待ちます。 通常、キャンペーンでの共同作業を検討している広告主ブランドからの、保留中の接続リクエストも監視する必要があります。 共同作業者の候補によって提案された接続設定を確認し、共同作業を開始する前に同意または修正します。

接続リクエストを承認したら、自分と共同作業者の間で重複するオーディエンスを調査する時間です。 広告主は、キャンペーンのプロジェクトを設定し、オーディエンスの目的（予測、抑制など）に基づいて、オーディエンスとユーザーのオーディエンスの間で重複レポートを実行します。

広告主がキャンペーンのターゲットにすべき理想的なオーディエンスを見つけて、それらを送信したら、それらをアクティブ化してキャンペーンを開始できます。

コラボレーションループの最後のステップは測定です。 キャンペーンの最後の手順として、広告ログなどの測定データをアップロードし、プログラムに表示されるレポートを実行してオーディエンスのパフォーマンスを把握することで、キャンペーンがどのように行われたかを把握します。

## 次の手順

会社の役割に基づいたエンドツーエンドの高いワークフローを理解したら、製品でサポートされている [ サンプルユースケース ](/help/guide/use-cases-benefits.md) をお読みください。
