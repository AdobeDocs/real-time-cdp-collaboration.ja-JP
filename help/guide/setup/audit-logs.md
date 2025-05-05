---
title: 監査ログ
description: Real-Time CDP Collaborationの監査ログ機能を使用して、ユーザーのアクティビティと変更をトラッキングする方法について説明します。
audience: admin
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/jp/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 3af1ac47-dc3d-4f19-a6b9-9e4e835977c0
source-git-commit: ff22dde9730fab89481338753b1dc4a0adf1d57e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 1%

---

# 監査ログ

{{limited-availability-release-note}}

システムで実行されるアクティビティの透明性と可視性を高めるために、Adobe Real-Time Customer Data Platform（CDP）の監査ログの形式で、様々なサービスや機能に関するユーザーアクティビティを監査できます。 これらのログは、Real-Time CDP Collaborationの問題のトラブルシューティングに役立つ監査証跡を形成し、企業のデータ管理ポリシーおよび規制要件に効果的に準拠するのに役立ちます。

基本的に、監査ログでは、*誰が* 何を *アクションを* いつ *実行したかがわかります*。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーのメール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。

Real-Time CDP Collaborationの監査ログ機能を使用して、プラットフォーム内のユーザーアクティビティと変更をトラッキングします。 この機能は、Adobe Experience Platform監査サービスと統合されており、この機能の UI はExperience Platformにあります。

![ 監査ログ機能の概要画面 ](/help/assets/setup/audit-logs/audit-logs-overview.png)

監査ログについて詳しくは、[Adobe Experience Platform監査ログのドキュメント ](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview){target="_blank"} を参照してください。

## 監査ログへのアクセス

監査ログには、次の 2 つの方法でアクセスできます。以下の節で説明します。 どちらのオプションでも、Real-Time CDP Collaboration UI 内で実行される様々なアクティビティを記録した監査ログのリストが表示されます

### Real-Time CDP Collaboration ユーザーインターフェイスからの監査ログへのアクセス

1. Real-Time CDP Collaboration UI の **[!UICONTROL マイアクティビティ]** タブに移動します。
2. ページ上部の UI テキストで「Experience Platform」リンクをクリックします。

![Real-Time CDP Collaboration UI からの監査ログへのアクセス ](/help/assets/setup/audit-logs/access-from-collaboration-ui.png)

### Experience Platform ユーザーインターフェイスで監査ログに直接アクセスします

1. Adobe Experience Platform UI に移動し、左側のメニューから **[!UICONTROL 監査]** セクションを選択します。 監査ログを表示できない場合は、組織のシステム管理者に問い合わせて、必要な権限を取得してください。

![Experience Platform UI からの監査ログへのアクセス ](/help/assets/setup/audit-logs/access-from-experience-platform-ui.png)

## 監査ログの表示と使用

監査ログを表示するには：

1. Adobe Experience Platform UI の **[!UICONTROL 監査]** セクションに移動します。
2. フィルターを使用して、条件に基づいてログを絞り込みます。
3. ログエントリを選択して、タイムスタンプ、リクエスト ID、リソースの詳細、アクションステータスなどの詳細情報を表示します。

![ 詳細監査ログ ](/help/assets/setup/audit-logs/filters-and-detailed-view.png)

### 取り込んだアクティビティ

監査ログでは、次のようなユーザーアクティビティに関する詳細情報を取得します。

* **ユーザー ID**：アクションを実行したユーザーの識別子。
* **アクション**：実行されるアクションのタイプ（作成、更新、削除など）。
* **リソース**：変更または作成されたリソース。
* **タイムスタンプ**：アクションが実行された時刻。

これらのログは、Real-Time CDP Collaboration インスタンス内のすべてのアクティビティの包括的な証跡を作成します。これは、データガバナンスと法令遵守に役立ちます。 詳しくは、[UI での監査ログの管理 ](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#managing-audit-logs-in-the-ui) を参照してください。

### 監査ログのフィルタリング

監査ログ UI には、特定のログを検索するのに役立つフィルターがいくつか用意されています。

* **カテゴリ**：リソースタイプを指します（例：コラボレーションインスタンス、接続、プロジェクト）。
* **アクション**：実行されるアクションのタイプ（例：作成、削除、更新）。
* **リクエスト ID**：リクエストの一意の ID。
* **ユーザーメール**：アクションを実行したユーザーのメールアドレス。
* **ステータス**：アクションのステータス（例：許可、拒否）。
* **日付範囲**：ログを表示する日付の範囲。

詳しくは、[ 監査ログのフィルタリング ](https://experienceleague.adobe.com/ja/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview#filter-audit-logs) を参照してください。

### 使用例

オーディエンスの管理、コネクション招待の拡張、プロジェクトの作成など、Experience Platform UI 内のアクションを実行すると、監査ログがReal-Time CDP Collaboration監査 UI に生成および表示されます。 例えば、プロジェクトの一部を作成または更新する操作は、次のように取り込まれます。

![ プロジェクトの一部を作成および更新する際に生成される監査ログの例 ](/help/assets/setup/audit-logs/create-project-audits.png)

## メリット

監査ログを使用する利点の一部を理解します。

* **データガバナンス**：監査ログを使用して、プラットフォーム内のすべてのアクティビティが追跡され、監査可能であることを確認します。
* **規制への準拠**：この機能は、規制要件を満たすためのユーザーアクティビティの証跡を提供します。
* **トラブルシューティング**：監査ログは、ユーザーのアクションの詳細なログを提供することで、問題の特定と解決に役立ちます。

## カテゴリとアクションのリファレンス

次の表に、Real-Time CDP Collaborationのすべてのカテゴリとアクションのリファレンスを示します。

![Real-Time CDP Collaboration監査ログでハイライト表示されている使用可能なカテゴリ。](/help/assets/setup/audit-logs/available-categories.png)

| カテゴリ | アクション | 説明 |
|-------------------------------|------------------------------------------|-------------|
| **[!UICONTROL Collaboration インスタンス]** | 作成、更新、削除 | 組織アカウントの管理（組織の作成、更新、削除など）。 詳しくは、[ 組織の設定 ](/help/guide/setup/onboard-organization.md) を参照してください。 |
| **[!UICONTROL Collaborationへの招待]** | 作成、更新、削除、承認、拒否 | 招待の作成、更新、削除、承認、却下など、接続の招待を管理します。 詳しくは、[ 接続招待 ](/help/guide/connect/establishing-connections.md) を参照してください。 |
| **[!UICONTROL Collaboration接続]** | 作成、更新、削除、承認、却下、承認をリクエスト | 接続の作成、更新、削除、承認、却下、承認のリクエストなど、コラボレーション接続を管理します。 |
| **[!UICONTROL Collaboration データ接続]** | 作成、更新、削除 | データ接続の作成、更新、削除など、オーディエンスをインポートおよび管理するための共同作業のためのデータ接続の管理。 詳しくは、[ データ接続の管理 ](/help/guide/setup/manage-data-connection.md) を参照してください。 |
| **[!UICONTROL Collaboration データエンティティ]** | 作成、更新、削除 | データ エンティティの作成、更新、削除を含む、共同作業のためのデータ エンティティを管理します。 このコンテキストのデータエンティティはオーディエンスを指します。 詳しくは、[ オーディエンスのインポートと管理 ](/help/guide/setup/onboard-audiences.md) を参照してください。 |
| **[!UICONTROL Collaboration プロジェクト]** | 作成、更新、削除 | プロジェクトの作成、更新、削除を含め、コラボレーション内のプロジェクトを管理します。 詳しくは、[ プロジェクトの管理 ](/help/guide/collaborate/manage-projects.md) を参照してください。 |
| **[!UICONTROL Collaboration モジュール]** | 作成、更新、削除 | UI での様々なモジュールの作成、更新、削除を含め、共同作業プロジェクト内の様々なモジュールを管理します。 例えば、[ オーディエンスを共有 ](/help/guide/collaborate/share.md) する機能などです。 |

{style="table-layout:auto"}

監査ログ機能を活用すると、Real-Time CDP Collaboration インスタンス内のすべてのアクティビティの明確で詳細な記録を保持し、透明性と説明責任を確保できます。
