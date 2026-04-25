---
title: アクセス制御の概要
description: Adobe Real-Time Customer Data Platform（CDP）Collaborationへのアクセス方法について説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
TQID: https://experienceleague.adobe.com/EIm85EKC4-YUePO5CTHQ4hi4KvawwhKXfiQEa7lw-P4
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2:
  - id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 3%

---

# アクセス制御の概要

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Adobe Real-Time CDP Collaborationへのアクセスを希望するエンドユーザーの場合は、システム管理者または製品管理者に連絡して、既存のアクセス権を確認してください。 システム管理者がわからない場合は、Adobe担当者にお問い合わせください。

Adobe Real-Time CDP Collaborationのアクセス制御は、[Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}のAdmin Consoleおよび権限を通じて提供されます。 このガイドでは、ユースケースに応じて、自分自身やチームの他のメンバーにアクセスする方法を説明します。

## アクセス制御階層 {#hierarchy}

Collaborationへのアクセス制御を設定するには、**システム管理者または製品管理者権限を持っている**&#x200B;必要があります。 システム管理者には制限はなく、オンボーディングプロセス中にプロビジョニングされます。 一方、製品管理者は、割り当てられた製品すべてに管理機能を提供することができます。 製品管理者には、システム管理者が製品および管理アクセス権を付与する必要があります。

これらのガイドでは、システム管理者、製品管理者、およびエンドユーザーのアクセス権の設定について説明します。 役割の主な違いを理解するには、次の表を参照してください。

| 役割 | 説明 |
| --- | --- |
| システム管理者 | 組織のスーパーユーザー。 これらのユーザーは、Admin Consoleですべての管理タスクを実行でき、管理機能を他のユーザーに委任する権限を持っています。 |
| 製品管理者 | 割り当てられた製品と、組織へのユーザーの追加、製品プロファイルからのユーザーの追加または削除、製品からの他の製品管理者の追加または削除など、関連するすべての管理機能を管理します。 |
| エンドユーザー | 製品を使用する組織内のユーザー。 |

{style="table-layout:auto"}

管理者の役割について詳しくは、[&#x200B; アドビヘルプセンター](https://helpx.adobe.com/jp/enterprise/using/admin-roles.html)を参照してください。

>[!TIP]
>
>これらのガイドでの&#x200B;**管理者**&#x200B;の使用は、**システム管理者と製品管理者**&#x200B;の両方を参照します。

## 関連製品 {#products}

Collaborationへのアクセス権を付与する前に、[&#x200B; ユースケース &#x200B;](#use-cases)に応じて、複数の商品にアクセスする必要があります。 アクセス制御ガイドは、進行状況に応じて複数のユーザーインターフェイスを介して機能し、アクセス設定プロセス内で特定の目的を果たします。 各製品の用途について詳しくは、次の表を参照してください。

| 製品 | 用途 |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | 管理者は、ユーザーに製品または管理者のアクセス権を割り当てるためにこれを使用します。 |
| [権限](https://experience.adobe.com/) | 管理者は、管理者またはエンドユーザーの役割を割り当てるためにこれを使用します。 |
| [Experience Platform](https://platform.adobe.com/) | 管理者とエンドユーザーにExperience Platform製品へのアクセス権を付与し、ロールに割り当てる必要があります。 |

## どこから始めればよいか {#use-cases}

これで、ユーザーおよび管理者の役割と様々なExperience Cloud製品について理解できたので、Collaborationへのアクセスを開始できます。 必要なステップに影響を与える主な要因は2つあります。

- 管理者またはエンドユーザーのアクセス権を割り当てる場合
- Experience Platform製品に既にアクセスしている場合

アクセス制御のユースケースに基づいて、権限の設定に必要なユーザーと開始場所を決定するには、次のグラフを参照してください。 **必ずチュートリアルを最初から最後まで追ってください。**

>[!TIP]
>
> スーパーユーザーとは、システム管理者が取得できる最高レベルのアクセス権を指します。 スーパーユーザーは、すべての管理タスクとユーザー機能を実行できます。 システム管理者は、すぐに使える製品機能を備えていないため、以下の図に示すように、適切なアクセス権を付与する必要があります。

| ユースケース | 必要な役割 | どこから始めればよいか |
| --- | --- | --- |
| Experience Platformから既存の製品にアクセスできない。 | システム管理者。 | [製品管理者のアクセス権の設定](./manage-user-access.md#admin-access) |
| 既存のExperience Platform システム管理者&#x200B;**と** Experience Platform UI アクセスのスーパーユーザー。 | システム管理者。 | [Collaboration アクセスの設定](./manage-user-access.md#RTCDP-collab-access) |
| 既存のExperience Platform システム管理者&#x200B;**に対するスーパーユーザー（Experience Platform UI アクセスなし）。** | システム管理者。 | [製品管理者のアクセス権の設定](./manage-user-access.md#admin-access) |
| 新しい製品管理者の製品管理者権限とCollaboration アクセス。 | システム管理者。 | [製品管理者のアクセス権の設定](./manage-user-access.md#admin-access) |
| 既存のExperience Platform製品管理者&#x200B;**と** Experience Platform UI アクセスに対するCollaboration アクセス。 | システム管理者または製品管理者。 | [Collaboration アクセスの設定](./manage-user-access.md#RTCDP-collab-access) |
| 既存のExperience Platform製品管理者&#x200B;**に対するCollaboration アクセス （Experience Platform UI アクセスなし）:** | システム管理者または製品管理者。 | [&#x200B; ユーザーアクセスの設定](./manage-user-access.md#user-access) |
| 新しいエンドユーザーのCollaboration アクセス。 | システム管理者または製品管理者。 | [&#x200B; ユーザーアクセスの設定](./manage-user-access.md#user-access) |
| Experience Platform アクセス権を持つ既存ユーザーのCollaboration アクセス。 | システム管理者または製品管理者。 | [Collaboration アクセスの設定](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## 追加の権限

Collaborationにアクセスできたら、特定の機能に対するExperience Platformの権限が必要になる場合があります。

### オーディエンスの取得 {#audience-sourcing}

共同作業者にオーディエンスを送る前に、Collaborationにオーディエンスを送る必要があります。 現在、オーディエンスの読み込みに対応しているセルフサービスのデータ接続はExperience Platformのみです。 開始するには、オーディエンスオンボーディングを管理するユーザーに、次の&#x200B;**[!UICONTROL プロファイル管理]** リソース権限を含む役割を割り当てる必要があります。

| 権限 | 説明 |
| ---- | ---- |
| [!UICONTROL セグメントの表示] | ユーザーがサンドボックスで使用可能なオーディエンスのリストを表示できるようにします。 |
| [!UICONTROL プロファイルの表示] | コラボレーションフィールドへのマッピングに使用できるフィールドを表示できます。 |

Below, you can see an example role with the above permissions added. For more information on creating or assigning roles, refer to the [manage roles](./manage-roles.md) guide.

![The resources workspace in Permissions with the View Segments and View Profiles permissions added to the Profile Management resource.](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>Users are able to work with audiences within Collaboration after they&#39;ve been sourced without any of the above permissions.

## 次の手順

Once you&#39;ve determined where to begin, follow your use case&#39;s link to get started configuring access. If you&#39;re wanting to learn about configuring access to Collaboration as an administrator beyond those use cases, refer to the [manage user access](manage-user-access.md) guide. To learn about roles and their part in configuring access to various components of Collaboration, refer to the [manage roles](manage-roles.md) guide.
