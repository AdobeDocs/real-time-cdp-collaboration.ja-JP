---
title: クラウドストレージの宛先の設定と管理
description: Real-Time CDP Collaborationでクラウドストレージの宛先を設定、表示、削除する方法について説明します。
audience: admin, publisher
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
product_v2: id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 60124235569ca9b17b3bb1cef502d57d39e82e1f
workflow-type: tm+mt
source-wordcount: 885
ht-degree: 1%

---

# クラウドストレージの宛先の設定と管理

このガイドを使用して、**[!UICONTROL アクティベーション]** ワークスペースからクラウドストレージの宛先を設定、表示、削除します。 **[!UICONTROL カタログ]** タブを使用して宛先を設定し、**[!UICONTROL 宛先]** タブを使用して宛先を管理し、**[!UICONTROL アクティブ化されたオーディエンス]** タブを使用して、宛先に対してアクティブ化されたオーディエンスを確認します。

宛先を設定すると、オーディエンスをアクティブ化すると、宛先を使用できるようになります。 サポートされている宛先の完全なリストについては、[使用可能な宛先](./overview.md#available-destinations)の表を参照してください。

>[!NOTE]
>
> このガイドでは、**[!DNL Amazon S3]**&#x200B;宛先を例として使用します。 ガイド付きの設定ワークフローは、サポートされているクラウドストレージの宛先タイプ間で共有されますが、認証方法、必須フィールド、コネクタ機能は異なる場合があります。 宛先を設定する前に、対応するAdobe Experience Platformの宛先ドキュメントにリンクされている[cloud storage destination requirements](./cloud-storage-destination-requirements.md)を確認してください。
>
> Adobe Experience Platformには、Real-Time CDP Collaborationの個別の設定ワークフローがあります。 設定するには、[Adobe Experience Platformを宛先として設定](./experience-platform.md)を参照してください。

## 前提条件 {#prerequisites}

宛先を設定する前に、次のことを確認してください。

* **[!UICONTROL アクティベーション]** ワークスペースにアクセスできます。
* クラウドストレージプロバイダーに必要な接続情報があります。
* アカウントを作成する必要がある場合は、必要な資格情報または権限があります。
* クラウドストレージの宛先](./cloud-storage-destination-requirements.md)の[要件を確認しました。

## 宛先の設定 {#configure-destination}

宛先を設定する場合、クラウドストレージアカウントをReal-Time CDP Collaborationに接続し、オーディエンスデータの書き出し方法を定義します。

**[!UICONTROL アクティベーション]** > **[!UICONTROL カタログ]**&#x200B;に移動します。

「**[!UICONTROL カタログ]**」タブには、使用可能な宛先プロバイダーが表示されます。 各宛先はカードとして表示されます。 宛先に応じて、そのカードは追加情報を表示するために設定されたアカウントとアクションを表示できます。

![宛先プロバイダーカードを表示する「カタログ」タブ。](/help/assets/destinations/manage-destinations/destination-provider-catalog.png)

設定する宛先プロバイダーを探し、**[!UICONTROL セットアップ]**&#x200B;を選択します。

宛先設定のガイド付き設定が開き、**[!UICONTROL 認証]**、**[!UICONTROL 宛先の作成]**、**[!UICONTROL フィールドのマッピング]**、**[!UICONTROL レビュー]**&#x200B;の4つの手順をガイドします。

### 認証 {#authenticate}

**[!UICONTROL 認証]**&#x200B;手順により、Real-Time CDP Collaborationと宛先アカウントとの間の接続が確立されます。

既存のアカウントが使用可能な場合は、アカウントセレクターから選択します。 アカウントを作成するには、**[!UICONTROL 新しいアカウント]**&#x200B;を選択します。

認証方法を選択し、必要なアカウント情報を入力します。 使用可能な認証方法とフィールドは、選択した宛先プロバイダーによって異なります。 コネクタ固有の要件については、[ クラウドストレージの宛先の要件](./cloud-storage-destination-requirements.md)を参照してください。

「**[!UICONTROL Amazon S3]**&#x200B;に接続」を選択します。 他の宛先プロバイダーの場合は、対応するプロバイダー名がボタンに表示されます。

アカウントが正常に検証されたら、**[!UICONTROL 次へ]**&#x200B;を選択します。

![ アカウントの選択と新しいアカウントの作成を表示する認証手順。](/help/assets/destinations/manage-destinations/authenticate-destination-account.png)

### 宛先を作成 {#create-destination}

**[!UICONTROL 宛先の作成]**&#x200B;手順では、オーディエンス書き出しファイルの配信場所と配信方法を定義します。

宛先名を入力し、必要なストレージと書き出しの設定を完了します。 使用可能なフィールドは、選択した宛先プロバイダーによって異なります。 定義とコネクタ固有の要件については、[ クラウドストレージの宛先の要件](./cloud-storage-destination-requirements.md)からリンクされている宛先ドキュメントを参照してください。

すべての必須フィールドを完了したら、**[!UICONTROL 次へ]**&#x200B;を選択します。 ガイド付きの設定は、フィールドマッピングの手順に進みます。

![宛先設定フィールドを表示する宛先作成手順。](/help/assets/destinations/manage-destinations/configure-new-destination.png)

### フィールドのマッピング {#map-fields}

**[!UICONTROL フィールドのマッピング]**&#x200B;手順では、オーディエンス一致キーを宛先で想定されるID フィールドにマッピングする方法を定義します。

Real-Time CDPの標準的な宛先ワークフローとは異なり、Real-Time CDP Collaborationは、宛先の作成時にこれらのマッピングを設定します。 オーディエンス一致キーがソースフィールドとして表示されます。 各ソースフィールドを対応するターゲット IDにマッピングして、書き出されたIDを宛先が認識し、それらを目的のユーザーに関連付けられるようにします。

「**[!UICONTROL フィールドを追加]**」を選択して別の一致キーマッピングを追加するか、削除アイコンを選択してマッピングを削除します。 必要なすべてのマッピングを確認して設定します。

マッピングが完了したら、**[!UICONTROL 次へ]**&#x200B;を選択します。 ガイド付きの設定は、レビューステップに進みます。

![ アクティブ化一致キーマッピング設定を表示するフィールドのマップ手順。](/help/assets/destinations/manage-destinations/map-destination-fields.png)

### レビュー {#review-destination}

**[!UICONTROL Review]**&#x200B;手順では、宛先設定を作成する前に、概要を作成します。

宛先設定を確認します。 変更するには、鉛筆アイコン ![鉛筆アイコンを選択します。](../../assets/icons/edit.png) 設定を更新します。

設定が正しい場合は、**[!UICONTROL 完了]**&#x200B;を選択します。 宛先が作成され、オーディエンスのアクティベーションに利用できるようになります。

![完了前に宛先設定の概要を表示するレビュー手順。](/help/assets/destinations/manage-destinations/review-destination-configuration.png)

## 設定済みの宛先の表示 {#view-configured-destinations}

宛先を設定すると、宛先インベントリに表示されます。 インベントリから、そのステータスとアクティベートされたオーディエンスを確認できます。

**[!UICONTROL アクティベーション]** > **[!UICONTROL 宛先]**&#x200B;に移動します。 「**[!UICONTROL 宛先]**」タブには、設定された宛先のテーブルが表示されます。

![設定済みの宛先を表示する「宛先」タブ。](/help/assets/destinations/manage-destinations/configured-destinations-list.png)

## 宛先の削除 {#delete-destination}

オーディエンスのアクティブ化に必要なくなった宛先を削除します。 宛先を削除すると、宛先インベントリから削除され、将来的にオーディエンスがアクティブ化されるのを防ぐことができます。

>[!IMPORTANT]
>
>宛先を削除しても、以前に書き出されたオーディエンスデータは削除されません。 以前に書き出したデータを宛先データストアから直接削除します。

**[!UICONTROL アクティベーション]** > **[!UICONTROL 宛先]**&#x200B;に移動します。

削除する宛先を見つけ、**[!UICONTROL アクション]**&#x200B;列の省略記号アイコンを選択し、**[!UICONTROL 削除]**&#x200B;を選択します。

![省略記号アイコンと削除アクションがハイライト表示されたアクティベーションワークスペースの「宛先」タブ。](/help/assets/destinations/manage-destinations/delete-configured-destination.png)

確認ダイアログが表示されます。 削除される宛先を確認し、**[!UICONTROL 削除]**&#x200B;を選択して確認します。

宛先は宛先インベントリから削除され、オーディエンスのアクティブ化に使用できなくなります。

## 次の手順 {#next-steps}

宛先を設定したら、プロジェクト内で[ オーディエンスのアクティブ化](../collaborate/activate.md)を開始できます。
