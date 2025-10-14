---
title: アクセス制御の概要
description: Adobe Real-Time Customer Data Platform（CDP）Collaborationへのアクセス権を取得する方法を説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: af48f5ea-8258-42a6-a39e-f4a4ca5b4a69
source-git-commit: 608706d00124372ac59209478ab551a3a6ce0226
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 2%

---

# アクセス制御の概要

{{limited-availability-release-note}}

>[!IMPORTANT]
>
> Adobe Real-Time CDP Collaborationへのアクセスを希望するエンドユーザーの場合は、システム管理者または製品管理者に問い合わせて、既存のアクセス権を確認してください。 システム管理者が不明な場合は、Adobeの担当者にお問い合わせください。

Adobe Real-Time CDP Collaborationのアクセス制御は、[Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"} のAdmin Consoleおよび権限を通じて提供されます。 このガイドでは、ユースケースに応じて、自分自身またはチームの他のメンバーにアクセス権を付与する方法を説明します。

## アクセス制御階層 {#hierarchy}

Collaborationへのアクセス制御を設定するには、システム管理者または製品管理者の権限が必要です **す**。 システム管理者には制限がなく、オンボーディングプロセス中にプロビジョニングされます。 一方、製品管理者は、割り当てられたすべての製品の管理機能を提供できます。 製品管理者には、システム管理者から製品と管理アクセス権を付与する必要があります。

これらのガイドでは、システム管理者、製品管理者およびエンドユーザーのアクセスの設定について説明します。 各ロールの主な違いを理解するには、以下の表を参照してください。

| 役割 | 説明 |
| --- | --- | 
| システム管理者 | 組織のスーパーユーザー。 管理者は、Admin Consoleですべての管理タスクを実行でき、他のユーザーに管理機能を委任する権限を持っています。 |
| 製品管理者 | ユーザーに割り当てられた製品と、組織へのユーザーの追加、製品プロファイルへのユーザーの追加または削除、製品への他の製品管理者の追加または削除など、関連するすべての管理機能を管理します。 |
| エンドユーザー | 製品を使用する組織内のユーザー。 |

{style="table-layout:auto"}

管理者の役割について詳しくは、[&#x200B; アドビヘルプセンター &#x200B;](https://helpx.adobe.com/jp/enterprise/using/admin-roles.html) を参照してください。

>[!TIP]
>
>これらのガイドでの **管理者** の使用は、**システム管理者と製品管理者の両方** を指します。

## その他の製品 {#products}

Collaborationへのアクセス権を付与する前に、（ユースケース [&#x200B; に応じて、複数の製品へのアクセス権を付与する必要があ &#x200B;](#use-cases) ます。 アクセス制御ガイドは、進行に応じて複数のユーザーインターフェイスを処理する場合があり、それぞれがアクセス設定プロセス内の特定の目的を果たします。 各製品の使用目的について詳しくは、次の表を参照してください。

| 製品 | 使用 |
| --- | --- |
| [Admin Console](https://adminconsole.adobe.com/) | 管理者はこれを使用して、ユーザーに製品アクセスや管理者アクセスを割り当てます。 |
| [権限](https://experience.adobe.com/) | 管理者はこれを使用して管理者またはエンドユーザーの役割を割り当てます。 |
| [Experience Platform](https://platform.adobe.com/) | 管理者とエンドユーザーには、Experience Platform製品へのアクセス権を付与して、役割に割り当てる必要があります。 |

## どこから始めるか {#use-cases}

これで、ユーザーと管理者の役割および様々なExperience Cloud製品について理解が深まったので、Collaborationへのアクセス権の付与を開始できます。 実行する必要がある手順に影響を与える主な要因は 2 つあります。

- 管理者またはエンドユーザーのアクセス権を割り当てている場合
- ユーザーが既にExperience Platform製品へのアクセス権を持っている場合

以下のチャートを参照して、権限の設定に必要なユーザーと、アクセス制御のユースケースに基づいて開始すべき場所を決定します。 **最初は、ガイドの最後までチュートリアルに従ってください。**

>[!TIP]
>
> スーパーユーザーとは、システム管理者が取得する最高レベルのアクセスを指します。 スーパーユーザーは、すべての管理タスクおよびユーザー機能を実行できます。 システム管理者は、製品の機能を標準で備えていないため、次のチャートに示すように、適切なアクセス権を自分自身に付与する必要があります。

| ユースケース | 必要な役割 | どこから始めるか |
| --- | --- | --- | 
| 既存のExperience Platform製品へのアクセス権を持たないスーパーユーザー。 | システム管理者。 | [&#x200B; 製品管理者アクセスの設定 &#x200B;](./manage-user-access.md#admin-access) |
| 既存のExperience Platform システム管理者 **Experience Platform UI アクセスを持つ** のスーパーユーザー。 | システム管理者。 | [Collaboration アクセスの設定 &#x200B;](./manage-user-access.md#RTCDP-collab-access) |
| Experience Platform UI アクセス権を持たない既存のExperience Platform システム管理者 **のスーパーユーザー** | システム管理者。 | [&#x200B; 製品管理者アクセスの設定 &#x200B;](./manage-user-access.md#admin-access) |
| 新しい製品管理者用の製品管理者権限およびCollaborationアクセス。 | システム管理者。 | [&#x200B; 製品管理者アクセスの設定 &#x200B;](./manage-user-access.md#admin-access) |
| Experience Platform UI アクセスを使用して **既存のExperience Platform製品管理者** Collaborationアクセス。 | システム管理者または製品管理者。 | [Collaboration アクセスの設定 &#x200B;](./manage-user-access.md#RTCDP-collab-access) |
| 既存のExperience Platform製品管理者のCollaboration アクセス **Experience Platform UI アクセスなし**。 | システム管理者または製品管理者。 | [&#x200B; ユーザーアクセスの設定 &#x200B;](./manage-user-access.md#user-access) |
| 新しいエンドユーザーのCollaboration アクセス。 | システム管理者または製品管理者。 | [&#x200B; ユーザーアクセスの設定 &#x200B;](./manage-user-access.md#user-access) |
| Collaborationアクセス権を持つ既存のユーザーがExperience Platformにアクセスする場合。 | システム管理者または製品管理者。 | [Collaboration アクセスの設定 &#x200B;](./manage-user-access.md#RTCDP-collab-access) |

{style="table-layout:auto"}

## 追加の権限

Collaborationへのアクセス権を取得したら、特定の機能に対するExperience Platformの追加権限が必要になる場合があります。

### オーディエンスソーシング {#audience-sourcing}

共同作業者へのオーディエンスの送信を開始する前に、オーディエンスをCollaborationにソース化する必要があります。 現在、オーディエンスの読み込みでサポートされているセルフサービスデータ接続はExperience Platformのみです。 まず、オーディエンスのオンボーディングを管理するユーザーに、次の **[!UICONTROL プロファイル管理]** リソース権限を含む役割を割り当てる必要があります。

| 権限 | 説明 |
| ---- | ---- |
| [!UICONTROL セグメントの表示] | サンドボックス内で使用可能なオーディエンスのリストを表示できるようにします。 |
| [!UICONTROL プロファイルの表示] | コラボレーションフィールドへのマッピングに使用できるフィールドの表示をユーザーに許可します。 |

以下に、上記の権限が追加された役割の例を示します。 役割の作成または割り当てについて詳しくは、[&#x200B; 役割の管理 &#x200B;](./manage-roles.md) ガイドを参照してください。

![Profile Management リソースに追加された「セグメントの表示」権限と「プロファイルの表示」権限を持つ権限のリソースワークスペース。](../../assets/permissions/sample-audience-role.png)

>[!NOTE]
>
>ユーザーは、上記の権限なしでソースされた後、Collaboration内でオーディエンスを操作できます。

## 次の手順

どこから始めるかを決定したら、ユースケースのリンクに従ってアクセスの設定を開始します。 管理者としてのCollaborationへのアクセス設定をこれらのユースケース以外でも行う方法については、[&#x200B; ユーザーアクセスの管理 &#x200B;](manage-user-access.md) ガイドを参照してください。 Collaborationの様々なコンポーネントへのアクセスを設定する際の役割とその役割についての詳細は、[&#x200B; 役割の管理 &#x200B;](manage-roles.md) ガイドを参照してください。
