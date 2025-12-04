---
title: 権限を使用した役割の管理
description: Real-Time CDP Collaboration UI 内の様々なコンポーネントへのアクセスを提供する、使用可能なすべてのロールリソースを理解します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 59cf5bf2-421b-4ebc-beab-30eafb098649
source-git-commit: 1f825bb4a81dbf65c43ddadcfd444923a37a906e
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# 役割の管理 {#manage-roles}

{{limited-availability-release-note}}

Adobe Real-Time CDP Collaboration UI の様々なコンポーネントへのユーザーアクセスを管理するには、[ 管理者 ](./manage-user-access.md#system-admin-gain-access) が役割を定義して割り当てることができます。 役割は、管理者またはユーザーが組織内で [ リソース ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#permissions){target="_blank"} に持つアクセスを定義します。 このガイドでは、Real-Time CDP Collaborationで提供される標準のロールに関する情報と、カスタムロールに割り当てることができる個々の権限に関する情報を提供します。

ロールの管理を開始するには、管理者がExperience Platform製品にアクセスできる必要があります。 管理者アクセス権またはExperience Platformへのアクセス権の取得について詳しくは、[ ユーザーアクセスの管理 ](./manage-user-access.md#manage-user-access-through-permissions) ガイドを参照してください。

## 標準役割 {#standard-roles}

2 つの標準的な役割が用意されており、それらの役割が 2 つの一般的なアクセス制御ユースケースに役立ちます。 これらは「読み取り専用」の役割で、カスタマイズできません。

| 役割名 | 役割の説明 | 権限 |
| --- | --- | --- |
| Collaboration Managers | これは、15 の権限がすべて含まれる all-access 権限です。 これにより、ユーザーはすべてのデータの読み取り、作成および編集が可能になります。 また、Experience Platformの **[!UICONTROL Prod]** サンドボックスにアクセスして、オーディエンスをReal-Time CDP Collaborationにインポートすることもできます。 | 以下の表からすべて。 |
| Collaboration ビューア | これは、読み取り専用アクセス権限です。 ユーザーは、データ、アクティビティ、接続などを読み取り、検出できます。 また、Experience Platformの **[!UICONTROL Prod]** サンドボックスにアクセスして、オーディエンスをReal-Time CDP Collaborationにインポートすることもできます。 | すべての読み取り権限（以下の表を参照） |

{style="table-layout:auto"}

## 特定のアクセス役割の作成 {#specific-access-roles}

追加の役割を作成して、様々なユーザーに様々なレベルのアクセスを提供する必要が生じる場合があります。 役割を作成する際は、**[!UICONTROL 共同作業]** リソース内で特定の権限を選択することで、様々なアクセスレベルを管理できます。 役割の作成および管理方法については、[roles](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/roles#create-new-role){target="_blank"} ガイドを参照してください。

>[!NOTE]
> Collaborationにアクセスするには、Adobe Experience Platformの **[!UICONTROL Prod]** サンドボックスへのアクセス権が必要です。 このサンドボックスへのアクセス権をユーザーに付与するには、「サンドボックス **[!UICONTROL リソースの]** Prod **[!UICONTROL 権限を含む役割にユーザーを割り当てる必要が]** ります。

Collaborations リソース内で使用可能な権限のリストを以下に示します。

| 権限の概要 | 説明 |
| --- | --- |
| Collaboration インスタンスの管理 | 組織のコラボレーション インスタンスを表示、作成、更新、および削除します。 他の組織のコラボレーション インスタンスを検出します。 |
| Collaboration インスタンスの読み取り | 組織のコラボレーションインスタンスを読み取り、他の組織のコラボレーションインスタンスを検出します。 |
| 接続招待の管理 | 組織が開始した接続招待を表示、作成および削除します。 他の組織によって開始された接続招待を承認または拒否します。 |
| 接続招待を読み取る | 接続の招待を表示します。 |
| Collaboration接続の管理 | 共同作業者は、設定の表示、作成、更新のほか、接続の送信および削除を行うことができます。 |
| Collaboration連携の読み取り | 接続を表示します。 |
| オーディエンスデータの管理 | オーディエンスのオンボーディングと検出。 パブリック、プライベートおよびカスタムオーディエンスを更新し、オーディエンスインベントリメタデータ設定を管理します。 |
| オーディエンスデータの読み取り | オーディエンスの読み取り、検出。 |
| 測定データの管理 | 測定データのオンボーディング、更新、削除 |
| 測定データの読み取り | 測定データの読み取り。 |
| プロジェクトの管理 | 検出、アクティブ化、測定のいずれかのアクティビティについて、プロジェクトを表示、作成、更新、削除します。 |
| プロジェクトの読み取り | 検出、アクティブ化、測定の各アクティビティのプロジェクトを表示します。 |
| ユーザーアクティビティを読み取り | ユーザーアクティビティを読み取る。 |
| ユーザーアクティビティの書き出し | ユーザーアクティビティを書き出します。 |
| Collaborationの与信監視を読む | 組織レベルおよびインスタンスレベルでのクレジットの監視。 |

{style="table-layout:auto"}

## 次の手順

Collaborationへのアクセスを定義する役割を作成したら、管理者とユーザーに [ 役割を割り当て ](./manage-user-access.md#assign-a-role) 必要があります。 役割の管理の概要については、[ 役割の権限の管理 ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions) ガイドを参照してください。
