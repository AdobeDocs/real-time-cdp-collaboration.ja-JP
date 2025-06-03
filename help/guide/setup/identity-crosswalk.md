---
title: ID クロスウォーク
description: 様々なソースから ID クロスウォークを取り込む方法や ID クロスウォークを管理する方法など、Real-Time CDP Collaborationの ID クロスウォークについてのすべてを説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hidefromtoc: true
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
source-git-commit: dd1386f9371cb40285315d11e07b139d3115e147
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 22%

---

# ID クロスウォーク

{{limited-availability-release-note}}

様々なソースから ID クロスウォークを取り込む方法や、ID クロスウォークを管理する方法など、Real-Time CDP Collaborationの ID クロスウォークについてすべてを説明します。

ID クロスウォークは、複数のデータセットやプラットフォーム間で、顧客 ID の安全でプライバシーに準拠したリンクを容易にします。 Real-Time CDP Collaborationでは、ハッシュ化された識別子を使用することで、個人情報（PII）を公開せずに ID の同期と紐付けを行うことができます。 これにより、顧客の統一されたビューが可能になり、共同作業の質が向上し、ターゲットを絞ったマーケティング活動が可能になります。

<!--
In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 
-->


まず、ID クロスウォークをReal-Time CDP Collaborationに読み込む必要があります。 ID クロスウォークをReal-Time CDP Collaborationに読み込むには、以下の節を参照してください。

>[!NOTE]
>
>Real-Time CDP Collaborationのベータ版リリースでは、Real-Time CDPのデータセットから ID クロスウォークを読み込むことができます。 今後のリリースで、さらに多くのオプションが利用可能になる予定です。

## ID クロスウォークのReal-Time CDP Collaborationへの読み込み {#import-crosswalk}

**[!UICONTROL 設定]**/**[!UICONTROL ID クロスウォーク]** タブに移動し、プラス **+** 記号を選択して **[!UICONTROL ID クロスウォーク]** を選択します。

![ID クロスウォークを追加するための画面へのアクセス方法の記録 ](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### クロスウォークソースを選択

ID クロスウォークを読み込むソースを選択してください。 Real-Time CDP Collaborationの最初のリリースでは、Experience Platformがクロスウォークの読み込みでサポートされている唯一のソースです。

>[!TIP]
>
>Platform から読み込むクロスウォークは、Experience Platformでは *データセット* と呼ばれます。

Experience Platformをクロスウォークのソースとして選択した後、ID クロスウォークを読み込む [&#128279;](https://experienceleague.adobe.com/ja/docs/experience-platform/sandbox/home)0&rbrace;Experience Platform サンドボックス &rbrace; を選択します。

![ 横断歩道等の採択方法の記録 ](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### クロスウォークを選択

Experience Platformをクロスウォークのソースとして選択した後、

### 詳細を入力

製品に読み込む ID クロスウォークの名前と説明を入力します。

### 結合キーの選択 {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="結合キー"
>abstract="結合キーは、異なるデータセット間でレコードを一致させてリンクするために使用される一意の ID です。これにより、様々なソースからのデータを同じ個人またはエンティティに正確に関連付けることができます。選択したクロスウォークの任意の列ヘッダーを結合キーとして使用できます。"

結合キーは、異なるデータセット間でレコードを一致させてリンクするために使用される一意の ID です。これにより、様々なソースからのデータを同じ個人またはエンティティに正確に関連付けることができます。適切な結合キーを選択すると、データを効果的に結合および調整でき、キャンペーンの精度と完全性が向上します。

選択したクロスウォークの任意の列ヘッダーを結合キーとして使用できます。

横断歩道テーブルに必要な結合キーを選択し、[**[!UICONTROL 次へ]**] を選択して次の手順に進みます。

### レビュー

前の画面で選択した内容を確認します。 選択に問題がなければ、「**[!UICONTROL 次へ]**」を選択してワークフローを完了します。

## 次の手順

ID クロスウォークをReal-Time CDPに読み込む方法を理解したら、これまでにReal-Time CDP Collaborationに追加したすべての ID クロスウォークを表示できます。 また、オーディエンスをReal-Time CDP Collaborationに読み込む際に読み込んだ ID クロスウォークを使用できるようになりました。
