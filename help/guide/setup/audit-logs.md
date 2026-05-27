---
title: 監査ログ
description: Real-Time CDP Collaborationの監査ログ機能を使用して、ユーザーのアクティビティと変更を追跡する方法を説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
TQID: https://experienceleague.adobe.com/zb09-bUpxJ2VPDknETHeayMuLpNRCaQ2VTnV9QnTRgE
product_v2:
  - id: fdddec33-c9cb-4459-b8b6-2664395a6f10
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 3ce7e66b31332836fd6cc6137c94622436505cc9
workflow-type: tm+mt
source-wordcount: 950
ht-degree: 4%

---

# 監査ログ

{{limited-availability-release-note}}

システムで実行されるアクティビティの透明性と可視性を高めるために、Adobe Experience Platformで様々なサービスや機能のユーザーアクティビティを監査ログの形式で監査できます。 これらのログは、Adobe Real-Time CDP Collaborationの問題のトラブルシューティングに役立つ監査証跡を形成し、企業のデータスチュワードシップポリシーや規制要件に効果的に準拠するのに役立ちます。

基本的な意味では、監査ログは&#x200B;*who*&#x200B;が&#x200B;*what* アクションを実行し、*when*&#x200B;を実行したことを示します。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーの電子メール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。

Collaborationの監査ログ機能を使用して、プラットフォーム内のユーザーのアクティビティと変更を追跡できます。 この機能はExperience Platform監査サービスと統合されており、この機能のUIはExperience Platformにあります。

![監査ログ機能の概要画面。](/help/assets/setup/audit-logs/audit-logs-overview.png)

監査ログの詳細については、[Experience Platform監査ログのドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"}を参照してください。

## 監査ログへのアクセス

次の節で説明するように、監査ログには2つの方法でアクセスできます。 どちらのオプションも、Collaboration内で実行されたさまざまなアクティビティをキャプチャする監査ログのリストを表示します。

### Collaboration ユーザーインターフェイスから監査ログにアクセスする

1. Collaborationの&#x200B;**[!UICONTROL Setup]** ワークスペースの&#x200B;**[!UICONTROL My Activity]** タブに移動します。
2. ページ上部のテキストで「Experience Platform」リンクを選択します。

![Collaborationの「マイアクティビティ」タブから監査ログにアクセスします。](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Experience Platformのユーザーインターフェイスから監査ログに直接アクセスできます

1. [Experience Platform](https://platform.adobe.com/)に移動し、左側のメニューから&#x200B;**[!UICONTROL 監査]** セクションを選択します。 監査ログを表示できない場合は、組織のシステム管理者に連絡して、必要な権限を取得してください。

![Experience Platformから監査ログにアクセスします。](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## 監査ログの表示と使用

監査ログを表示するには：

1. Experience Platformの&#x200B;**[!UICONTROL 監査]** セクションに移動します。
2. 条件に基づいてログを絞り込むには、[&#x200B; フィルター](#filter-audit-logs)を使用します。
3. ログエントリを選択して、タイムスタンプ、リクエスト ID、リソースの詳細、アクションステータスなどの詳細情報を表示します。

![詳細な監査ログ &#x200B;](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### キャプチャしたアクティビティ

監査ログには、次のようなユーザーアクティビティに関する詳細情報が記録されます。

* **タイムスタンプ**：月/日/年の時間:minute午前/午後の形式で実行されたアクションの正確な日時。
* **アセット名**: アクションが実行されたリソースの名前。
* **カテゴリ**: アクションが実行されたリソースのタイプ。
* **アクション**：作成や削除など、実行された特定のアクション。
* **ユーザー**: アクションを実行したユーザーの電子メールアドレス。

これらのログにより、Collaborationインスタンス内のあらゆるアクティビティを包括的に追跡でき、データガバナンスや規制遵守に役立ちます。 UI[&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui)での監査ログの管理について詳しく説明します。

### 監査ログのフィルタリング {#filter-audit-logs}

監査ログ UIには、特定のログの検索に役立つフィルターがいくつか用意されています。

* **カテゴリ**: アクションが実行されたリソースの種類（Collaboration インスタンスまたはCollaboration Connection Inviteなど）。
* **アクション**：実行されたアクションのタイプ。 使用可能なアクションは、選択したカテゴリによって異なります。 たとえば、Collaboration インスタンスのアクションには、作成、更新、削除などがあります。
* **要求ID**：要求の一意のID。
* **ユーザー**: アクションを実行したユーザーの電子メールアドレス。
* **ステータス**：許可または拒否など、アクションのステータス。
* **日付範囲**: ログを表示する日付の範囲。

詳しくは、[監査ログのフィルタリング &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs)を参照してください。

## メリット

監査ログは、Collaborationを利用する企業にとって、次のような利点をもたらします。

* **データガバナンス**：監査ログを使用して、プラットフォーム内のすべてのアクティビティが追跡および監査可能であることを確認します。
* **規制遵守**：この機能は、規制要件を満たすためにユーザーアクティビティのトレイルを提供します。
* **トラブルシューティング**：監査ログは、ユーザーのアクションの詳細なログを提供することで、問題の特定と解決に役立ちます。

## カテゴリとアクションの参照

次の表に、Real-Time CDP Collaborationのすべてのカテゴリとアクションの一覧を示します。

![使用可能なカテゴリがReal-Time CDP Collaboration監査ログで強調表示されます。](/help/assets/setup/audit-logs/available-categories.png)

| カテゴリ | アクション | 説明 |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration インスタンス]** | 作成、更新、削除 | アカウントの作成、更新、削除などのアカウント管理。 詳しくは、[&#x200B; アカウントの設定](/help/guide/setup/onboard-account.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration Connection Invite]** | 作成、更新、削除、承認、却下 | 招待の作成、更新、削除、承認、拒否など、接続への招待を管理します。 詳しくは、[接続の確立](/help/guide/connect/establishing-connections.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration Connection]** | 作成、更新、削除、承認、却下、承認のリクエスト | 接続の作成、更新、削除、承認、拒否、承認の要求など、接続を管理します。 |
| **[!UICONTROL Collaboration Data Connection]** | 作成、更新、削除 | データ接続の作成、更新、削除など、オーディエンスをソースおよび管理する場所からのデータ接続を管理します。 詳しくは、[&#x200B; データ接続の管理](/help/guide/setup/manage-data-connection.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration データエンティティ]** | 作成、更新、削除 | データエンティティの作成、更新、削除など、Collaborationのデータエンティティを管理します。 この文脈でのデータエンティティはオーディエンスを指します。 詳しくは、[&#x200B; オーディエンスの取得と管理](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration プロジェクト]** | 作成、更新、削除 | プロジェクトの作成、更新、削除など、Collaboration内のプロジェクトを管理します。 詳しくは、[&#x200B; プロジェクトの管理](/help/guide/collaborate/manage-projects.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration Module]** | 作成、更新、削除 | UIでの様々なモジュールの作成、更新、削除など、プロジェクト内の様々なモジュールを管理します。 例えば、オーディエンスを[&#x200B; アクティブ化](/help/guide/collaborate/activate.md)する機能があります。 |

{style="table-layout:auto"}

監査ログ機能を活用することで、Collaboration内のあらゆるアクティビティを明確かつ詳細に記録し、透明性と説明責任を確保できます。
