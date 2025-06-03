---
title: オーディエンスをアクティベート
description: パブリッシャーとして、共同作業者と共有するオーディエンスをキャンペーンでアクティブ化する方法を説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: fd82fcbf-ab39-48e0-9438-0a9046693431
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 3%

---

# オーディエンスをアクティベート

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL アクティベート]** ワークスペースは、パブリッシャーで、**オーディエンスの共有とアクティベート** ユースケースが [ 接続プロセス中に ](../connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[ プロジェクトの管理 ](./manage-projects.md#project-use-cases) ガイドを参照してください。

パブリッシャーとしてAdobe Real-Time CDP Collaborationを使用してオーディエンスをアクティブ化する方法を見つける 現在、Amazon S3 の場所に対してオーディエンスをアクティブ化できます。 追加のアクティベーションチャネルが予定されています。

キャンペーンのオーディエンスをアクティブ化できるのは、**パブリッシャー組織** のみです。 広告主組織は、これらのオーディエンスをプロジェクトでアクティブ化するパブリッシャーと [ オーディエンスを共有 ](/help/guide/collaborate/share.md) できます。 詳しくは、広告主およびパブリッシャー向けの [ エンドツーエンドのワークフロー ](/help/guide/end-to-end-workflow.md) を参照してください。

## 前提条件 {#prerequisites}

Real-Time CDP Collaborationを使用するパブリッシャーの場合、最初にAdobe イネーブルメントおよびエンジニアリングチームと協力して、目的のAmazon S3 の場所への接続を設定する必要があります。 これを設定すると、Real-Time CDP CollaborationからAmazon S3 の場所にオーディエンスをアクティブ化（または書き出し）できるようになります。 このワークフローを開始する場合は、Adobe担当者にお問い合わせください。

さらに、接続で **オーディエンスの共有とアクティベーション** ユースケースが有効になっている必要があります。

## アクティブ化動作 {#activation-behavior}

広告主接続がアクティベーション用にオーディエンスを共有すると、このオーディエンスは直ちに **[!UICONTROL アクティブ化]** ビューに表示されます。 オーディエンスは、広告主がオーディエンス共有画面で設定した間隔で、指定した場所に書き出されます。

![Amazon S3 の宛先に対するワークフローのアクティブ化 ](/help/assets/collaborate/activate/activate-to-amazon-s3.png)

## 次の手順 {#next-steps}

データをアクティブ化しキャンペーンを実施した後、Adobeのイネーブルメントおよびエンジニアリングチームと協力して、測定データをアップロードし、対応する [ 測定レポート ](/help/guide/collaborate/measure.md) を確認します。
