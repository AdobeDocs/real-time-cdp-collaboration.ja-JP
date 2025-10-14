---
title: 監査ログ
description: Real-Time CDP Collaborationの監査ログ機能を使用して、ユーザーのアクティビティと変更をトラッキングする方法について説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: eed99cfafd5ffad5a468741f7258c162454769b7
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 1%

---

# 監査ログ

{{limited-availability-release-note}}

システムで実行されるアクティビティの透明性と可視性を高めるために、様々なサービスや機能に関するユーザーアクティビティをAdobe Experience Platformの監査ログの形式で監査できます。 これらのログは、Adobe Real-Time CDP Collaborationの問題のトラブルシューティングに役立つ監査証跡を形成し、企業のデータ管理ポリシーおよび規制要件に効果的に準拠するのに役立ちます。

基本的に、監査ログでは、*誰が* 何を *アクションを* いつ *実行したかがわかります*。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーのメール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。

Collaborationの監査ログ機能を使用して、プラットフォーム内のユーザーアクティビティと変更をトラッキングします。 この機能は、Experience Platform監査サービスと統合されており、この機能の UI はExperience Platformにあります。

![&#x200B; 監査ログ機能の大まかな概要画面。](/help/assets/setup/audit-logs/audit-logs-overview.png)

監査ログについて詳しくは、[Experience Platform監査ログのドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"} を参照してください。

## 監査ログへのアクセス

監査ログには、次の 2 つの方法でアクセスできます。以下の節で説明します。 どちらのオプションでも、Collaboration内で実行される様々なアクティビティを記録した監査ログのリストが表示されます。

### Collaboration ユーザーインターフェイスからの監査ログへのアクセス

1. Collaborationの **[!UICONTROL 設定]** ワークスペースにある **[!UICONTROL マイアクティビティ]** タブに移動します。
2. ページ上部のテキスト内でExperience Platform リンクを選択します。

![Collaborationの「マイアクティビティ」タブから監査ログにアクセスします &#x200B;](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)。

### Experience Platform ユーザーインターフェイスで監査ログに直接アクセスします

1. [Experience Platform](https://platform.adobe.com/) に移動し、左側のメニューから **[!UICONTROL 監査]** セクションを選択します。 監査ログを表示できない場合は、組織のシステム管理者に問い合わせて、必要な権限を取得してください。

![Experience Platformから監査ログにアクセスします。](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## 監査ログの表示と使用

監査ログを表示するには：

1. Experience Platformの **[!UICONTROL 監査]** セクションに移動します。
2. [&#x200B; フィルター &#x200B;](#filter-audit-logs) を使用して、条件に基づいてログを絞り込みます。
3. ログエントリを選択して、タイムスタンプ、リクエスト ID、リソースの詳細、アクションステータスなどの詳細情報を表示します。

![&#x200B; 詳細監査ログ &#x200B;](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### 取り込んだアクティビティ

監査ログでは、次のようなユーザーアクティビティに関する詳細情報を取得します。

* **タイムスタンプ**：月/日/年/時 :minuteAM/PM 形式で実行されたアクションの正確な日時。
* **アセット名**：アクションが実行されたリソースの名前。
* **カテゴリ**：アクションが実行されたリソースのタイプ。
* **アクション**：作成や削除など、実行された特定のアクション。
* **ユーザー**：アクションを実行したユーザーのメールアドレス。

これらのログは、Collaboration インスタンス内のすべてのアクティビティの包括的な証跡を作成します。これは、データガバナンスと法令遵守に役立ちます。 詳しくは、[UI での監査ログの管理 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui) を参照してください。

### 監査ログのフィルタリング {#filter-audit-logs}

監査ログ UI には、特定のログを検索するのに役立つフィルターがいくつか用意されています。

* **カテゴリ**:Collaboration インスタンス、Collaboration接続の招待など、アクションが実行されたリソースのタイプ。
* **アクション**：実行されるアクションのタイプ。 使用可能なアクションは、選択したカテゴリによって異なります。 例えば、Collaboration インスタンスのアクションには、作成、更新、削除が含まれます。
* **リクエスト ID**：リクエストの一意の ID。
* **ユーザー**：アクションを実行したユーザーのメールアドレス。
* **ステータス**：アクションのステータス（許可、拒否など）。
* **日付範囲**：ログを表示する日付の範囲。

詳しくは、[&#x200B; 監査ログのフィルタリング &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs) を参照してください。

## メリット

監査ログは、Collaborationを使用する組織にいくつかの利点があります。

* **データガバナンス**：監査ログを使用して、プラットフォーム内のすべてのアクティビティが追跡され、監査可能であることを確認します。
* **規制への準拠**：この機能は、規制要件を満たすためのユーザーアクティビティの証跡を提供します。
* **トラブルシューティング**：監査ログは、ユーザーのアクションの詳細なログを提供することで、問題の特定と解決に役立ちます。

## カテゴリとアクションのリファレンス

次の表に、Real-Time CDP Collaborationのすべてのカテゴリとアクションのリファレンスを示します。

![Real-Time CDP Collaboration監査ログでハイライト表示されている使用可能なカテゴリ。](/help/assets/setup/audit-logs/available-categories.png)

| カテゴリ | アクション | 説明 |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration インスタンス]** | 作成、更新、削除 | アカウントの管理（アカウントの作成、更新、削除など）。 詳細については、[&#x200B; アカウントの設定 &#x200B;](/help/guide/setup/onboard-account.md) ガイドを参照してください。 |
| **[!UICONTROL Collaborationへの招待]** | 作成、更新、削除、承認、拒否 | 招待の作成、更新、削除、承認、却下など、接続の招待を管理します。 詳しくは、[&#x200B; 接続の確立 &#x200B;](/help/guide/connect/establishing-connections.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration接続]** | 作成、更新、削除、承認、却下、承認をリクエスト | 接続の管理（接続の作成、更新、削除、承認、却下、承認のリクエストなど）。 |
| **[!UICONTROL Collaboration データ接続]** | 作成、更新、削除 | データ接続の作成、更新、削除など、オーディエンスをソーシングおよび管理する場所からのデータ接続を管理します。 詳しくは、[&#x200B; データ接続の管理 &#x200B;](/help/guide/setup/manage-data-connection.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration データエンティティ]** | 作成、更新、削除 | データエンティティの作成、更新、削除など、Collaborationのデータエンティティの管理 このコンテキストのデータエンティティはオーディエンスを指します。 詳しくは、[&#x200B; オーディエンスのソーシングと管理 &#x200B;](/help/guide/setup/onboard-audiences.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration プロジェクト]** | 作成、更新、削除 | プロジェクトの作成、更新、削除を含む、Collaboration内のプロジェクトの管理。 詳しくは、[&#x200B; プロジェクトの管理 &#x200B;](/help/guide/collaborate/manage-projects.md) ガイドを参照してください。 |
| **[!UICONTROL Collaboration モジュール]** | 作成、更新、削除 | UI の様々なモジュールを作成、更新、削除するなど、プロジェクト内の様々なモジュールを管理します。 例えば、[&#x200B; オーディエンスをアクティブ化 &#x200B;](/help/guide/collaborate/activate.md) する機能などです。 |

{style="table-layout:auto"}

監査ログ機能を活用すると、Collaboration内のすべてのアクティビティの明確で詳細な記録を保持し、透明性と説明責任を確保できます。
