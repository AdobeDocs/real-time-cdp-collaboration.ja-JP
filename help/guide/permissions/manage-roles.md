---
title: 権限による役割の管理
description: Real-Time CDP Collaboration UI内の様々なコンポーネントにアクセスできる、利用可能なすべてのロールリソースについて説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
TQID: https://experienceleague.adobe.com/dB7nEQtEGG8PvCSE7eDDelH-ml2EhKOQ8ovvGXG1Ejg
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
feature_v2: id: ba929a52-9339-4154-9487-317dc875a3c7
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 623
ht-degree: 1%

---

# 役割の管理 {#manage-roles}

{{limited-availability-release-note}}

Adobe Real-Time CDP Collaboration UIの様々なコンポーネントへのユーザーアクセスを管理するには、[管理者](./manage-user-access.md#system-admin-gain-access)が役割を定義して割り当てることができます。 役割は、組織内の管理者またはユーザーが[ リソース ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target="_blank"}に対して持つアクセス権を定義します。 このガイドでは、Real-Time CDP Collaborationで提供される標準の役割に関する情報と、カスタムロールに割り当てることができる個々の権限について説明します。

ロールの管理を開始するには、管理者がExperience Platform製品にアクセスする必要があります。 管理アクセスの取得またはExperience Platformへのアクセスの取得について詳しくは、[ ユーザーアクセスの管理](./manage-user-access.md#manage-user-access-through-permissions) ガイドを参照してください。

## 標準ロール {#standard-roles}

2つの一般的なアクセス制御ユースケースに対応する、2つの標準ロールが用意されています。 これらは「読み取り専用」の役割であり、カスタマイズできません。

| 役割名 | 役割の説明 | 権限 |
| --- | --- | --- |
| Collaboration Manager | これは15個の権限すべてを含むオールアクセス権限です。 これにより、ユーザーはすべてのデータを読み取り、作成、編集できます。 また、Experience Platformの&#x200B;**[!UICONTROL Prod]** サンドボックスへのアクセスも提供され、Real-Time CDP Collaborationにオーディエンスを読み込むことができます。 | 全て下の表から。 |
| Collaboration Viewers | これは読み取り専用のアクセス権限です。 利用者は、データ、アクティビティ、接続などを読み取り、発見することができます。 また、Experience Platformの&#x200B;**[!UICONTROL Prod]** サンドボックスへのアクセスも提供され、Real-Time CDP Collaborationにオーディエンスを読み込むことができます。 | 以下の表のすべての読み取り権限。 |

{style="table-layout:auto"}

## 特定のアクセスロールの作成 {#specific-access-roles}

さまざまなユーザーにさまざまなレベルのアクセスを提供するために、追加の役割を作成する必要があります。 役割を作成する場合、**[!UICONTROL コラボレーション]** リソース内で特定の権限を選択して、異なるアクセスレベルを管理できます。 役割を作成および管理する方法については、[役割](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"} ガイドを参照してください。

>[!NOTE]
> Collaborationにアクセスするには、Adobe Experience Platformの&#x200B;**[!UICONTROL Prod]** サンドボックスにアクセスする必要があります。 ユーザーにこのサンドボックスへのアクセス権を付与するには、**[!UICONTROL サンドボックス]** リソースの&#x200B;**[!UICONTROL Prod]**&#x200B;権限を含む役割に割り当てる必要があります。

以下に、コラボレーションリソース内で使用可能な権限のリストを示します。

| 高レベルの権限 | 説明 |
| --- | --- |
| Collaboration インスタンスの管理 | 組織のコラボレーションインスタンスを表示、作成、更新、削除します。 その他の組織のコラボレーションインスタンスの詳細。 |
| Collaboration インスタンスの読み取り | 組織のコラボレーションインスタンスを読み、他の組織のコラボレーションインスタンスを見つけます。 |
| 接続の招待を管理 | 組織によって開始された接続招待を表示、作成、削除します。 他の組織によって開始された接続の招待を受け入れたり拒否したりします。 |
| 接続の招待の読み取り | 接続の招待を表示します。 |
| Collaboration接続の管理 | 共同作業者は、設定の表示、作成、更新、および送信と削除を行うことができます。 |
| Collaborationとの連携の詳細 | 接続を表示します。 |
| オーディエンスデータの管理 | オーディエンスのオンボーディングと発見。 パブリック、プライベート、カスタムのオーディエンスを更新し、オーディエンスインベントリのメタデータ設定を管理できます。 |
| オーディエンスデータの読み込み | オーディエンスの読み取りと発見： |
| 測定データの管理 | 測定データのオンボーディング、更新、削除： |
| 測定データの読み取り | 測定データの読み取り： |
| プロジェクトの管理 | 検出、アクティブ化、測定アクティビティのプロジェクトを表示、作成、更新、削除できます。 |
| プロジェクトを読む | 検出、アクティブ化、測定アクティビティのいずれかのプロジェクトを表示します。 |
| ユーザーアクティビティの読み取り | ユーザーアクティビティの読み取り： |
| ユーザーアクティビティの書き出し | ユーザーアクティビティの書き出し： |
| Collaborationのクレジットモニタリング機能の詳細 | 組織およびインスタンスレベルでの信用調査。 |

{style="table-layout:auto"}

## 次の手順

Collaborationへのアクセスを定義する役割を作成したら、管理者とユーザーに役割](./manage-user-access.md#assign-a-role)を[割り当てる必要があります。 役割の管理の詳細については、「[役割の権限の管理](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) ガイド」を参照してください。
