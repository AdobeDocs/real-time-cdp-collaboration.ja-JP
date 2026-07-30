---
title: オーディエンスの概要
description: Real-Time CDP Collaborationのオーディエンスについて、そのソースを含めて説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f7cd44177d60bfd3d3db384f7b1a250ace4c3633
workflow-type: tm+mt
source-wordcount: 707
ht-degree: 3%

---


# オーディエンスの概要

{{limited-availability-release-note}}

Adobe Real-Time CDP Collaborationでは、オーディエンスは、Collaborationに取り込むユーザーまたは顧客のグループです。 調達後は、オーディエンスを利用して、共同作業者との重複を発見し、オーディエンスを活性化し、キャンペーンのパフォーマンスを測定することができます。 オーディエンスデータの保存場所に応じて、Adobe Experience Platform、クラウドストレージおよび共有システム、ファイルアップロードワークフローなど、さまざまな種類のソースからオーディエンスを取得できます。

## オーディエンスで可能なこと {#audiences-in-collaboration}

オーディエンスがCollaborationにソースされた後、サポートされているコラボレーションワークフローで使用できるようになります。

Collaborationでオーディエンスを使用すると、次のことが可能になります。

* 自社のオーディエンスと共同作業者のオーディエンスの比較
* 重複と機会の特定
* オーディエンスをアクティベート
* 成果と施策のパフォーマンスを測定
* オーディエンスの表示と関連する設定の管理

## Collaborationにオーディエンスを組み込む方法 {#conceptual-diagram}

>[!NOTE]
>
> 次の図は、ソースされたオーディエンスがどのようにCollaborationに適合し、プロジェクトで使用されるかを示す概要を示しています。

```text
Source → Data connection → Audience → Project
                                         │
                          ┌──────────────┼──────────────┐
                          ▼              ▼              ▼
                      Discover       Activate       Measure
                                         │
                                         ▼
                                    Destination
```

## 主要コンセプト {#core-concepts}

次の概念は、オーディエンスのソーシングとコラボレーションワークフローに関する主なオブジェクトについて説明します。

**ソース**\
Adobe Experience Platform、クラウドストレージの場所、ファイルのアップロードなど、オーディエンスデータの送信元のシステムまたは場所。

**データ接続**\
Collaborationがソースからオーディエンスデータにアクセスするために使用する設定済みの接続。 データ接続には、認証、フィールドマッピング、スケジューリングなど、ソース固有の設定の詳細が含まれます。

**オーディエンス**\
Collaborationにソース化され、プロジェクトで使用できるユーザーまたは顧客のグループ。

**接続**\
組織と他の組織との間のコラボレーション関係。

**プロジェクト**\
コラボレーターが、発見、アクティブ化、測定など、サポートされているユースケースでオーディエンスを一緒に使用するワークスペース。

**宛先**\
アクティブなオーディエンスが送信される外部プラットフォームまたはシステム。

**キーの一致**
データセットと共同作業者をまたいでレコードを照合するためにCollaborationが使用する識別子。 マッチキーは、オーディエンスの重複、アクティベーション、測定などのワークフローをサポートします。

## オーディエンスのライフサイクル {#audience-lifecycle}

Collaborationでは、データ接続を通じてオーディエンスを取得し、**[!UICONTROL Setup]**&#x200B;で管理し、サポートされているユースケースのプロジェクトで使用します。

1. **Source audiences**: データ接続を介してCollaborationにオーディエンスデータを取り込みます。
2. **オーディエンスの管理**: オーディエンスの詳細、表示、および関連する設定を確認して管理します。
3. **プロジェクトでオーディエンスを使用**: **Discover**、**Activate**、**Measure**&#x200B;など、サポートされているユースケースでプロジェクトでソース オーディエンスを使用します。

あらゆるユースケースですべてのオーディエンスが使用されているわけではありません。 例えば、オーディエンスはアクティブ化されずに&#x200B;**Discover**&#x200B;にソースを取得して使用したり、宛先に送信せずに&#x200B;**Measure** ワークフローで使用したりできます。

オーディエンスの取得と管理について詳しくは、[Sourceとオーディエンスの管理](./onboard-audiences.md)を参照してください。 データ接続の管理について詳しくは、[&#x200B; データ接続の管理](./manage-data-connection.md)を参照してください。

## オーディエンスの流入元 {#supported-sources}

Collaborationは、複数のオーディエンスソースタイプをサポートしています。 選択したソースによって、セットアップフロー、前提条件、認証要件、データフォーマット、フィールドマッピング、リフレッシュ動作、オーディエンスをCollaborationに取り込むための利用可能な設定オプションが決まります。

* Adobe Experience Platform
* Amazon S3、Google Cloud Storage、Azure Storageを含むクラウドストレージ
* SnowflakeやDatabricks Delta Shareなどのデータ共有サービス
* Adobe Audience Manager
* CSV ファイルのアップロード

サポートされているソースとソース固有の設定手順の一覧については、[&#x200B; ソースの概要](./source-overview.md#available-sources)を参照してください。

## オーディエンスとは {#match-keys}

RTCDP Collaborationのオーディエンスは、一致キーで構成されます。 アカウント設定に応じて、サポートされる照合キーには、**人物ID**、**デバイス ID**、**パートナーID**&#x200B;を含めることができます。 一致キーは、**オーディエンス重複**、**アクティブ化**、**測定**&#x200B;などのワークフローをサポートします。

詳細については、[一致キーの設定](../setup/onboard-account.md#set-up-match-keys)および[&#x200B; データ接続の管理](../setup/manage-data-connection.md#match-keys)を参照してください

## プロジェクトでのオーディエンスの使用 {#audiences-in-projects}

プロジェクトは、他の組織と共同作業するためのコンテキストを提供します。 プロジェクト内では、サポートされているコラボレーションのユースケースに対してオーディエンスを使用できます。

* **もっと知る**: オーディエンスを比較し、重複インサイトをレビューします。 [&#x200B; オーディエンス重複の検出](../collaborate/discover.md)を参照してください。
* **アクティブ化**：選択したオーディエンスをキャンペーンで使用するためにアクティブ化します。 アクティベーションは、プロジェクトワークスペースの「[!UICONTROL &#x200B; アクティベート &#x200B;]」タブから開始され、接続で設定された宛先にオーディエンスを送信します。 [&#x200B; オーディエンスのアクティベーション &#x200B;](../collaborate/activate.md)を参照してください。
* **測定**: プロジェクトに関連付けられているキャンペーン配信とコンバージョンレポートを確認します。 [&#x200B; パフォーマンスの測定](../collaborate/measure.md)を参照してください。

プロジェクトの作成と管理について詳しくは、[&#x200B; プロジェクトの作成と管理](../collaborate/manage-projects.md)を参照してください。 宛先の設定について詳しくは、[宛先の概要](../destinations/overview.md)を参照してください。

## 次の手順 {#next-steps}

* [利用可能なオーディエンスソースを確認する](./source-overview.md)
* [Sourceとオーディエンスの管理](./onboard-audiences.md)
* [プロジェクトの作成と管理](../collaborate/manage-projects.md)
* [オーディエンス重複の発見](../collaborate/discover.md)
* [オーディエンスをアクティベート](../collaborate/activate.md)
* [パフォーマンスを測定](../collaborate/measure.md)
* [宛先の概要](../destinations/overview.md)
