---
title: データ接続を管理
description: Real-Time CDP Collaborationでの一致キー、スケジュール、ユースケース、オーディエンスフィルタリングなど、データ接続を管理する方法について説明します
audience: administrator, data engineer
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: d142d3ed-f56a-4150-a885-571728a73ac8
source-git-commit: acaaaa1e1fab981d874210639c16e76e48fc3394
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 4%

---

# データ接続を管理

{{limited-availability-release-note}}

## 概要

Real-Time CDP Collaborationのデータ接続を使用して、様々なソースからオーディエンスを読み込みます。 既存のデータ接続の一致キーを管理し、データの読み込みをスケジュールする方法を説明します。 さらに、様々な属性でオーディエンスをフィルタリングして、より詳細なインサイトを得ることができます。

ここでデータ接続を管理する前に、最初 [ オーディエンスのオンボーディングワークフロー ](./onboard-audiences.md) 中にデータ接続を設定する必要があります。 これにより、正しいデータソースがReal-Time CDP Collaborationで使用できるように接続されます。

## データ接続の表示

>[!IMPORTANT]
>
>データ接続の削除は、現在、Real-Time CDP Collaboration ユーザーインターフェイスではサポートされていません。 データ接続を削除する場合は、Adobe担当者に問い合わせるか、[ カスタマーサポートチケットを作成 ](https://experienceleague.adobe.com/home?lang=en&amp;support-tab=open-ticket#support) してください。

既存のデータ接続を表示するには、**[!UICONTROL 設定]**/**[!UICONTROL マイオーディエンス]** に移動し、「**[!UICONTROL データ接続の管理]**」を選択します。

![ 「データ接続の管理」がハイライト表示されたワークスペースを設定 ](/help/assets/setup/manage-data-connection/manage-data-connection-highlighted.png)

これにより、現在設定されているすべてのデータ接続が表示され、それぞれのオーディエンスの数、データ接続のソースなどに関する情報が表示されます。 **[!UICONTROL データ接続を表示]** を選択して、このデータ接続の一部である一致キー、スケジュール、オーディエンスに関する情報を表示します。

![ 接続がハイライト表示されたデータ接続を管理ワークスペース データ接続を表示。](/help/assets/setup/manage-data-connection/view-data-connection-highlighted.png)

### 一致キー {#match-keys}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_matchkeys"
>title="一致キー"
>abstract="一致キーは、様々なソースのデータの照合方法を決定します。 ユースケースやプライバシーガイドラインに最も関連する一致キーを選択します。"

一致キーは、異なるデータソースのオーディエンス間でメンバーを紐付けするために使用される識別子です。 使用可能な一致キーは次のとおりです。

- **ハッシュ化されたメール**

このデータ接続で使用されている一致キーを編集することはできません。

![ 「キーを一致させる」セクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-match-keys.png)

### スケジュール設定 {#scheduling}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_manage_dataconnections_scheduling"
>title="スケジュール設定"
>abstract="このビューには、データ接続に対して最初に選択したスケジュール オプションが表示されます。"

データ接続に最初に選択したスケジュール オプションは編集できません。 スケジュールオプションについて詳しくは、オーディエンスの読み込みワークフロードキュメントの [ スケジュールセクション ](/help/guide/setup/onboard-audiences.md#schedule) を参照してください。

![ 「スケジュール」セクションがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-scheduling.png)

## オーディエンス管理 {#manage-audiences}

データ接続からオーディエンスのリストを表示する際に、オーディエンスを表示、カテゴリを編集、データ接続から削除するように選択できます。

![ オーディエンスがハイライト表示されたデータ接続ワークスペース。](/help/assets/setup/manage-data-connection/view-data-connection-manage-audiences.png)

## 次の手順

データ接続を管理すると、共同作業者が検出可能にしたオーディエンスとオーディエンスの間で [ 重複を検出 ](/help/guide/collaborate/discover.md) できます。
