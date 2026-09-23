---
title: 「拡張」で拡張オーディエンスを作成する
description: Adobe Real-Time CDP Collaborationで共同作業者のオーディエンス母集団を使用して、シードオーディエンスから拡張オーディエンスを作成する方法を説明します。
source-git-commit: d2585628407acf10ad8388231259c77991a9a0b0
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%
---
# （Beta） Expandでの拡張オーディエンスの作成

プロジェクト内の「**[!UICONTROL 拡張]**」タブを使用して、いずれかのオーディエンスから拡張オーディエンスを作成します。 Collaborationでは、共同作業者のオーディエンスデータを利用して、シードオーディエンスに類似するプロファイルを検索します。これにより、共同作業者の元となるオーディエンスデータを公開することなく、新しい見込み客にリーチすることができます。 作成された拡張オーディエンスは、共同作業者に送信され、アクティベーションされます。

## 前提条件 {#prerequisites}

「**[!UICONTROL 展開]**」タブを使用する前に、次の操作を行う必要があります。

* シードオーディエンスとして使用する[ ソース ](/help/guide/setup/onboard-audiences.md)の少なくとも1人のオーディエンス
* [共同作業者と接続](/help/guide/connect/establishing-connections.md)
* [その共同作業者と共にプロジェクト ](/help/guide/collaborate/manage-projects.md)を作成しました
* 拡張オーディエンスを受信している場合は、アクティブなオーディエンスを受信するように[宛先](/help/guide/destinations/overview.md)が設定されています

## さらに詳しく {#expand-overview}

**[!UICONTROL コラボレーション]** > **[!UICONTROL マイプロジェクト]**&#x200B;に移動し、プロジェクトを開いて、**[!UICONTROL 展開]** タブを選択します。

**[!UICONTROL 拡張]** ページには、この共同作業者のために作成された拡張オーディエンスと、新しいオーディエンスを作成するオプションが表示されます。

![拡張オーディエンス テーブルを表示する「拡張」タブ。名前、ステータス、モデル サイズ、オーディエンスのリーチ、最終更新列が表示されます。](/help/assets/collaborate/expand/expand-overview.png){zoomable="yes"}

**[!UICONTROL 拡張オーディエンス]** テーブルには、プロジェクトで作成されたすべての拡張オーディエンスが一覧表示されます。

| 列 | 説明 |
|---|---|
| **[!UICONTROL 名前]** | 拡張オーディエンスの名前。 編集するまで、シードオーディエンス名がデフォルトになります。 |
| **[!UICONTROL ステータス]** | 拡張オーディエンスの現在のステータス。 詳しくは、[拡張オーディエンスのステータス ](#expansion-audience-status)を参照してください。 |
| **[!UICONTROL モデルサイズ]** | 生成された拡張オーディエンスのサイズ。 モデルの処理が完了するまで使用できません。 |
| **[!UICONTROL オーディエンスリーチ]** | 拡張オーディエンスに使用されるオーディエンスリーチ設定。 |
| **[!UICONTROL 最終更新日]** | 拡張オーディエンスが最後に更新された日時。 |

{style="table-layout:auto"}

### 拡張オーディエンスステータス {#expansion-audience-status}

拡張オーディエンスは、次のステータスで移動します。

| ステータス | 説明 |
|---|---|
| **[!UICONTROL 処理中]** | 拡張モデルは、まだ拡張オーディエンスを生成中です。 |
| **[!UICONTROL ドラフト]** | モデルが終了し、拡張オーディエンスをレビューして共同作業者に送信する準備が整いました。 |
| **[!UICONTROL アクティブ]** | 拡張オーディエンスを共同作業者に送信しました。 |

{style="table-layout:auto"}

>[!NOTE]
>
>ステータスはリアルタイムで更新されません。 「**[!UICONTROL 展開]**」タブを再度開くか更新して、最新のステータスを確認します。

## 拡張オーディエンスの作成 {#create-expansion-audience}

新しい拡張オーディエンスを作成するには、追加アイコン（![追加アイコン。](/help/assets/icons/plus.png)）を選択します **[!UICONTROL 拡張]** ページで、「**[!UICONTROL 拡張オーディエンスを作成]**」を選択します。


**[!UICONTROL 拡張オーディエンスの生成]** ダイアログが表示されます。 拡張オーディエンスを生成するには、すべてのフィールドを完了します。

![ シードオーディエンス、オーディエンスのリーチ、一致キー、シードオーディエンスメンバーのフィールドを含むオーディエンス拡張を生成ダイアログ。](/help/assets/collaborate/expand/generate-expansion-audience-dialog.png){zoomable="yes"}

### シードオーディエンスを選択 {#select-seed-audience}

「**[!UICONTROL シードオーディエンスを選択]**」ドロップダウンから、独自のオーディエンスのいずれかを選択します。 Collaborationでは、このオーディエンスを、共同作業者の母集団の類似プロファイルを見つけるためのベースとして使用します。

![ オーディエンス拡張を生成ダイアログのシードオーディエンス フィールド。](/help/assets/collaborate/expand/select-seed-audience.png){zoomable="yes"}

### 一致キーを選択 {#select-match-key}

拡張オーディエンスに1つの一致キーを有効にします。 1つ以上を有効にすることはできません。

| ユーザー ID | デバイス ID |
|---|---|
| **[!UICONTROL ハッシュ化されたメール]** | **[!UICONTROL ハッシュ化されたIPv4]** |
| **[!UICONTROL ハッシュ化された電話]** | **[!UICONTROL GAID]** |
| **[!UICONTROL ロイヤルティ ID]** | **[!UICONTROL IDFA]** |
| **[!UICONTROL CRM ID]** | **[!UICONTROL Demdex ID]** |

{style="table-layout:auto"}

>[!NOTE]
>
>シードオーディエンスに特定の一致キーが含まれていない場合、そのオプションは無効に表示され、選択できません。

![使用可能な一致キーオプションを含むオーディエンス拡張を生成ダイアログの「一致キー」セクション。](/help/assets/collaborate/expand/select-match-key.png){zoomable="yes"}

### オーディエンスのリーチの選択 {#select-audience-reach}

「**[!UICONTROL オーディエンスリーチ]**」ドロップダウンを使用して、シードオーディエンスとの類似性とリーチ全体のバランスを取ります。 シードオーディエンスに対する類似性と全体的なリーチの中間の接点として、**[!UICONTROL バランス]**&#x200B;を選択します。

![ バランスオプションとその下の説明テキストを選択したオーディエンス拡張を生成ダイアログの「オーディエンスへのリーチ」フィールド。](/help/assets/collaborate/expand/select-audience-reach.png){zoomable="yes"}

### シードオーディエンスを含める、または除外する {#include-exclude-seed-audience}

「**[!UICONTROL シードオーディエンス]**」ラジオボタンを使用して、元のシードオーディエンスを最終的な拡張オーディエンスに含めるか、最終的な拡張オーディエンスから除外するかを選択します。

![はい/いいえラジオボタンを含むオーディエンス拡張を生成ダイアログの「シードオーディエンスメンバー」フィールド。](/help/assets/collaborate/expand/include-exclude-seed-audience.png){zoomable="yes"}

### 拡張オーディエンスの生成 {#generate-expansion-audience}

すべてのフィールドが完了したら、**[!UICONTROL 拡張オーディエンスの生成]**&#x200B;を選択します。 確認メッセージは、Collaborationが拡張オーディエンスを作成中であり、**[!UICONTROL 拡張]** ページでその進行状況を追跡できることを確認します。

## 拡張オーディエンスのレビューと送信 {#review-send-expansion-audience}

拡張オーディエンスのステータスが&#x200B;**[!UICONTROL ドラフト]**&#x200B;に更新されたら、**[!UICONTROL 拡張オーディエンス]** テーブルからその名前を選択して開きます。

![拡張オーディエンス オーディエンス オーディエンスのメタデータ、モデルサイズ、シードオーディエンスサイズ、送信ボタンを示す詳細ページ。](/help/assets/collaborate/expand/expansion-audience-detail.png){zoomable="yes"}

このビューでは、次の操作を実行できます。

* 拡張オーディエンス名の編集
* 作成日時を表示
* シードオーディエンスサイズと生成された拡張オーディエンスサイズを比較します
* オーディエンスの生成に使用された一致キーを確認します

準備ができたら、**[!UICONTROL パートナーに送信]**&#x200B;を選択して、拡張オーディエンスを共同作業者に送信します。 オーディエンスは、送信するまで&#x200B;**[!UICONTROL ドラフト]** ステータスのままになり、次に&#x200B;**[!UICONTROL アクティブ]**&#x200B;に更新されます。

>[!NOTE]
>
>共同作業者が宛先を設定していない場合、**[!UICONTROL パートナーに送信]**&#x200B;は使用できません。 メッセージは、共同作業者が最初に宛先を設定する必要があることを説明します。

>[!IMPORTANT]
>
>拡張オーディエンスは、共同作業者に送信されない場合、生成されてから7日後に有効期限が切れます。

## 拡張オーディエンスの受信とアクティブ化 {#receive-activate-expansion-audience}

拡張オーディエンスを送信する場合、Collaborationは、接続に設定されたアクティブ化設定に従って、そのオーディエンスを共同作業者に配信します。

* **自動アクティブ化**&#x200B;が有効になっている場合、Collaborationは拡張オーディエンスを共同作業者が設定した宛先に自動的にアクティブ化し、[ アクティブ化タブ ](./activate.md#activated-audiences)に表示されます。
<!-- Beta release: automatic activation is the only available activation setting. Uncomment the manual activation guidance below when manual activation is introduced with the GA release. -->
<!-- * If **manual activation** is enabled, the expansion audience appears in your collaborator's [Received audiences](./activate.md#received-audiences) section of the **[!UICONTROL Activate]** tab, and your collaborator must manually activate it. -->

## 次の手順

拡張オーディエンスを送信したら、[もっと知るタブ ](./discover.md)を使用して他のオーディエンスと比較するか、[ タブをアクティブ化](./activate.md)を使用してアクティブ化を追跡します。
