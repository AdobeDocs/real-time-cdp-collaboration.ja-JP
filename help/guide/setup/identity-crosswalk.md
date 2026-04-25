---
title: ID クロスウォーク
description: 様々なソースからID クロスウォークを取り込む方法や、ID クロスウォークを管理する方法など、Real-Time CDP CollaborationのID クロスウォークについて説明します
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
hide: true
exl-id: a51f112d-3da7-4482-a24a-6d9f269d28d1
TQID: https://experienceleague.adobe.com/0vUk3-vtaZvCoBmzkbrfMQF1NFaFg2NqsjJIje1sVcg
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 546
ht-degree: 22%

---

# ID クロスウォーク

{{limited-availability-release-note}}

様々なソースからID クロスウォークを取り込む方法や、ID クロスウォークを管理する方法など、Real-Time CDP CollaborationのID クロスウォークについて説明します。

IDのクロスウォークにより、複数のデータセットやプラットフォームをまたいで、顧客IDの安全でプライバシーに準拠したリンクを容易に実現できます。 Real-Time CDP Collaborationでは、ハッシュ化されたIDを利用することで、個人情報（PII）を公開することなく、IDを同期して照合できるようになります。 これにより、顧客の全体像を把握して、より優れたコラボレーションとターゲットを絞ったマーケティング活動を実現できます。

最初の手順として、ID クロスウォークをReal-Time CDP Collaborationに読み込む必要があります。 Real-Time CDP CollaborationにID クロスウォークを読み込むには、以下の節を参照してください。

>[!NOTE]
>
>Real-Time CDP Collaborationのベータ版リリースでは、Real-Time CDPのデータセットからID クロスウォークを読み込むことができます。 その後のリリースでは、さらにオプションが用意されています。

## Real-Time CDP CollaborationへのID クロスウォークの読み込み {#import-crosswalk}

**[!UICONTROL 設定]** > **[!UICONTROL ID クロスウォーク]** タブに移動し、追加アイコン（![追加アイコン &#x200B;](/help/assets/icons/plus.png)）を選択して、**[!UICONTROL ID クロスウォーク]**&#x200B;を選択します

![画面にアクセスしてIDのクロスウォークを追加する方法の記録](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### クロスウォークソースを選択

ID クロスウォークを読み込むソースを選択します。 Real-Time CDP Collaborationの最初のリリースでは、Experience Platformがクロスウォークの読み込みをサポートする唯一のソースです。

>[!TIP]
>
>Experience Platformから読み込むクロスウォークは、Platformでは&#x200B;*データセット*&#x200B;と呼ばれます。

Experience Platformをクロスウォークのソースとして選択したら、ID クロスウォークの読み込み元となる[Experience Platform サンドボックス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/sandbox/home)を選択します。

![&#x200B; クロスウォーク ソースの選択方法の記録](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### クロスウォークを選択

Experience Platformをクロスウォークのソースとして選択すると，

### 詳細を入力

製品に読み込むID クロスウォークの名前と説明を入力します。

### 結合キーの選択 {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="結合キー"
>abstract="結合キーは、異なるデータセット間でレコードを一致させてリンクするために使用される一意の ID です。 これにより、様々なソースからのデータを同じ個人またはエンティティに正確に関連付けることができます。 選択したクロスウォークの任意の列ヘッダーを結合キーとして使用できます。"

結合キーは、異なるデータセット間でレコードを一致させてリンクするために使用される一意の ID です。 これにより、様々なソースからのデータを同じ個人またはエンティティに正確に関連付けることができます。 適切な結合キーを選択することで、データを効果的に結合して紐付けし、キャンペーンの精度と完全性を向上させることができます。

選択したクロスウォークの任意の列ヘッダーを結合キーとして使用できます。

クロスウォーク テーブルの目的の結合キーを選択し、**[!UICONTROL 次]**&#x200B;を選択して次の手順に進みます。

### レビュー

前の画面の選択内容を確認します。 選択内容に満足したら、**[!UICONTROL 次へ]**&#x200B;を選択してワークフローを完了します。

## 次の手順

Real-Time CDPにID クロスウォークを読み込む方法を理解すると、これまでReal-Time CDP Collaborationに追加したすべてのID クロスウォークを表示できます。 また、Real-Time CDP Collaborationにオーディエンスを読み込む際に読み込んだID クロスウォークを使用できるようになりました。
