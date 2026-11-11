---
title: '[!DNL The Trade Desk]からの有料メディアシグナルでプロファイルを充実させる（Alpha）'
description: 有料メディアエンリッチメント属性の書き出し、配信されたCSVの取り込み、オーディエンスの構築とパーソナライゼーションのためのファーストパーティプロファイルの更新方法について説明します。
audience: advertiser
hide: true
badge: Alpha
source-git-commit: d090aff6ea091f60c9b3bbaf2ca72fcf8017d7d1
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 1%
---

# The Trade Desk profile enrichment （Alpha）

生イベントデータストリーム（REDS）インプレッションログデータフィード（[!DNL The Trade Desk]）を使用して、エンリッチメント属性と有料メディアコンテキストをファーストパーティプロファイルに書き出します。

CSV ファイルが[!DNL Amazon S3]書き出し先に到着したら、それを[!DNL Adobe Real-Time CDP]に取り込みます。 このリリースでは、ファイルを書き出しても、プロファイルは自動的に更新されず、エクスペリエンスはアクティブ化されません。 [!DNL Adobe Real-Time CDP]に戻る自動プロファイルエンリッチメントは、後続のリリースの機能になります。

広告露出は、顧客プロファイルにコンテキストを追加します。 エンゲージメント、購入の意図、長期的な興味などは確認しません。

## 強化の準備 {#prepare-for-enrichment}

始める前に、管理者、メディアチーム、データチームと協力して、次のことを確認してください。

* [!DNL Adobe Real-Time CDP Collaboration]へのアクセスと署名済み参加契約書。
* REDS フィードのプロビジョニングを承認するために、[!DNL The Trade Desk]でアクセス レターが完了しました。
* ハッシュ化された電子メールアドレスまたは電話番号を使用する[!DNL Adobe Real-Time CDP Collaboration]で利用できるファーストパーティオーディエンス。 その他の識別子は、このリリースではサポートされていません。
* エンリッチメント出力を受信するように設定された[!DNL Amazon S3]宛先。
* 配信されたファイルを[!DNL Adobe Real-Time CDP]に取り込むプロセスです。

### ソースフィードを承認 {#authorize-source-feed}

[!DNL The Trade Desk]から提供されたアクセスレターに記入して、[!DNL The Trade Desk]がREDS ログをAdobeに直接送信することを許可します。

[!DNL The Trade Desk]がソースフィードをプロビジョニングし、Adobeがアクセスと取り込みを設定します。 プロジェクトを作成する前に、接続がアクティブで、フィードの準備ができていることを確認します。

処理後、エンリッチメント出力ファイルが書き出し先に届きます。

### ダウンストリーム取り込みの準備 {#prepare-downstream-ingestion}

配信後、[!DNL Adobe Real-Time CDP]管理者またはテクニカルサポートチームにファイルの取り込みを依頼します。

## プロジェクトの接続と作成 {#connect-create-projects}

接続ダイアログでアクセスレターを入力し、パートナーIDを保存します。 プロジェクトを作成する前に、AdobeがREDS ログの受信を確認するのを待ちます。 プロジェクトを作成すると、エンリッチメントジョブが開始されます。これには、パートナーIDとログの両方が必要です。

### パートナーとつながる {#connect-partner}

[!DNL The Trade Desk]に接続して、広告主情報を追加します：

1. **[!UICONTROL Connect]**&#x200B;で、**[!UICONTROL 共同作業者を見つける]**&#x200B;を開きます。
1. [!DNL The Trade Desk] を検索します。
   ![共同作業者カタログには、[!DNL The Trade Desk]とその[!UICONTROL 接続] オプションが一覧表示されます。](../../../assets/collaborate/advertising-platforms/discover-collaborators-trade-desk.png){zoomable="yes"}
1. [!DNL The Trade Desk]の&#x200B;**[!UICONTROL Connect]**&#x200B;を選択し、接続ダイアログの指示に従います。
   ![接続ダイアログで、[!DNL The Trade Desk]のREDS認証とパートナーIDの設定について説明します。](../../../assets/collaborate/advertising-platforms/trade-desk-connection-instructions.png){zoomable="yes"}
1. 接続がアクティブになったら、**[!UICONTROL 接続設定]**&#x200B;を開きます。 **[!UICONTROL 広告主情報]**&#x200B;で、**[!UICONTROL 編集]**&#x200B;を選択して既存の情報を更新するか、**[!UICONTROL 追加]**&#x200B;して新しい情報を入力します。
   ![&#x200B; アクティブな接続設定には、[!UICONTROL 広告主情報]と[!UICONTROL 編集] コントロールが表示されます。](../../../assets/collaborate/advertising-platforms/trade-desk-connection-settings.png){zoomable="yes"}
1. **[!UICONTROL パートナーID]**&#x200B;と&#x200B;**[!UICONTROL パートナー名]**&#x200B;にパートナーIDとパートナー名を入力し、**[!UICONTROL 保存]**&#x200B;を選択します。 **[!UICONTROL シート ID]**&#x200B;の下にある[!DNL The Trade Desk] アカウントでパートナーIDを検索します。
   ![広告主情報ダイアログには、必要なパートナーIDとパートナー名のフィールドと[!UICONTROL 保存] コントロールがあります。](../../../assets/collaborate/advertising-platforms/trade-desk-advertiser-partner-info-dialog.png){zoomable="yes"}

接続がアクティブになり、広告主情報を保存したら、AdobeがREDS ログを受信したことを確認します。 そしてプロジェクトを作成します。

### プロジェクトの作成 {#create-project}

接続のプロジェクトを作成します。

1. **[!UICONTROL コラボレーション]**&#x200B;で、**[!UICONTROL マイプロジェクト]**&#x200B;を選択します。
1. **[!UICONTROL プロジェクトを作成]**&#x200B;または追加アイコン（![&#x200B; プロジェクトを追加。](/help/assets/icons/plus.png)）を選択します。
1. **[!UICONTROL プロジェクトを作成]**&#x200B;で、**[!UICONTROL 共同作業者]**&#x200B;から[!DNL The Trade Desk]を選択します。
   ![[!UICONTROL &#x200B; プロジェクトの作成] フォームには、[!DNL The Trade Desk]が一覧表示され、プロジェクト名、説明、画像のフィールドが含まれています。](../../../assets/collaborate/advertising-platforms/trade-desk-create-project.png){zoomable="yes"}
1. **[!UICONTROL プロジェクト名]**&#x200B;と&#x200B;**[!UICONTROL 説明]**&#x200B;を入力し、プロジェクトを識別する画像を選択します。
1. 「**[!UICONTROL 作成]**」を選択します。

一般的なプロジェクト管理については、[&#x200B; プロジェクトの作成と管理ガイド &#x200B;](/help/guide/collaborate/manage-projects.md)を参照してください。

## 属性の選択と書き出し {#select-export-attributes}

プロジェクトからエンリッチメント属性を書き出します。

<!-- TODO: Replace the destination screenshot with one showing the [!UICONTROL Export Attributes] action. -->

1. プロジェクトを開き、**[!UICONTROL エンリッチ]**&#x200B;を選択します。
1. 各属性のカバレッジ値を確認して、シグナルの可用性を把握します。
1. エンリッチメントに使用する属性を選択します。
   ![[!UICONTROL Enrich] ページは、選択可能な信号をカテゴリ別にグループ化し、カバレッジ値を表示します。](../../../assets/collaborate/advertising-platforms/enrich-attribute-selection.png){zoomable="yes"}
1. エンリッチメント出力用に設定された[!DNL Amazon S3]書き出し先を選択します。 宛先を設定するには、[&#x200B; クラウドストレージの宛先の設定と管理](/help/guide/destinations/manage-destinations.md)を参照してください。
   <!-- ![The [!UICONTROL Choose a destination] screen lists a destination and the [!UICONTROL Export Attributes] action.](../../../assets/collaborate/advertising-platforms/enrich-choose-destination.png){zoomable="yes"} -->
1. 選択した属性と宛先を確認し、**[!UICONTROL 属性の書き出し]**&#x200B;を選択します。
   <!-- ![The destination screen confirms that enrichment has started.](../../../assets/collaborate/advertising-platforms/enrich-request-confirmation.png){zoomable="yes"} -->

宛先が正しく設定されている場合、書き出しの送信が配信を開始します。 [!DNL Adobe Real-Time CDP Collaboration]以外で正常にファイルを配信したことを確認します。

Adobeでは、プロジェクトを作成してから週単位でエンリッチメント属性を処理します。 各実行では、利用可能な[!DNL The Trade Desk] データの過去90日間が使用されます。 各エクスポートには、最新の完了済み実行から選択した属性が含まれます。 更新された属性を書き出すには、後で実行が完了した後で、別の書き出しをリクエストします。

### 利用可能なエンリッチメントシグナル {#available-signals}

4つのカテゴリーにまたがる18のシグナルから選択できます。 カスタムエンリッチメント式はサポートされていません。

| カテゴリ | シグナル | 説明 |
| --- | --- | --- |
| コア | [!UICONTROL 最終公開日] | IDが最後に広告に公開された日付。 |
| コア | [!UICONTROL 露光量] | 未加工のインプレッション数ではなく、露出 – 頻度カテゴリ。 |
| コア | [!UICONTROL 見込み顧客とリターゲティング &#x200B;] | 見込み顧客の獲得またはリマーケティングとしての露出の分類。 |
| コア | [!UICONTROL 製品カテゴリが表示されました] | 広告で宣伝される製品に対する推定カテゴリ。 |
| コア | [!UICONTROL 主要な在庫チャネル &#x200B;] | 広告露出に関連する主な在庫チャネル。 |
| コア | [!UICONTROL 主要なデバイスの種類] | 広告露出に関連する主なデバイスタイプ。 |
| 地域 | [!UICONTROL 市区町村] | 広告のコンテキストから得られた市区町村の情報で、位置情報は確認されていません。 |
| 地域 | [!UICONTROL 地域/都道府県] | 広告のコンテキストから地域または州の情報を収集します。 |
| 地域 | [!UICONTROL DMA] | 広告のコンテキストから得られた指定市場地域（DMA）情報。 |
| コネクテッドテレビ（CTV） | [!UICONTROL CTV公開] | コネクテッド TV デバイスでの広告露出。 |
| コネクテッドテレビ（CTV） | [!UICONTROL &#x200B; ライブストリームビューアー] | 視聴やエンゲージメントのプルーフではなく、ライブストリームの広告在庫の露出。 |
| コネクテッドテレビ（CTV） | [!UICONTROL PMP / プレミアム露出] | プライベートマーケットプレイス（PMP）またはプライベート契約の露出。独立して確認されたプレミアム在庫はありません。 |
| コンテンツの親和性 | [!UICONTROL &#x200B; コネクテッド TV / ストリーミング &#x200B;] | ストリーミングコンテンツに関連する広告露出。 |
| コンテンツの親和性 | [!UICONTROL &#x200B; ゲーマー] | ゲームコンテンツ、サイト、アプリに関連する広告露出。 |
| コンテンツの親和性 | [!UICONTROL &#x200B; スポーツファン &#x200B;] | スポーツコンテンツ、サイト、アプリに関連する広告露出。 |
| コンテンツの親和性 | [!UICONTROL &#x200B; ニュースフォロワー] | ニュースコンテンツ、サイト、アプリに関連する広告露出。 |
| コンテンツの親和性 | [!UICONTROL 音楽愛好家] | 音楽コンテンツ、サイト、アプリに関連する広告露出。 |
| コンテンツの親和性 | [!UICONTROL &#x200B; コンテンツのジャンル &#x200B;] | 広告露出に関連するコンテンツジャンル。 |

ジオグラフィックシグナルは、検証済みの住宅や現在地ではなく、広告のコンテキストを表します。 コンテンツに対する親和性のシグナルは、個人の興味や好みを確認するものではありません。 ソース情報が使用できない場合、一部の属性に値が含まれていないことがあります。

### 属性のカバー範囲 {#attribute-coverage}

カバレッジは、処理されたレコードに属性値が含まれる頻度を表します。 「**[!UICONTROL CTV exposed]**」などの「はい/いいえ」シグナルの場合、カバレッジは真の値を持つレコードをカウントします。 カバレッジは、IDの一致率や、属性を受け取るファーストパーティプロファイルの割合を示すものではありません。

IDの照合、ソースシグナルの可用性、取り込みは、プロファイルの更新に影響します。 カバレッジでは、書き出しの完了やプロファイルの更新は確認されません。

### ワークフローの範囲 {#workflow-scope}

キュレートされたカタログを使用して、[!DNL The Trade Desk]からのデータを拡充します。 生のログを書き出したり、カスタム属性式を作成したりすることはできません。 その他のデマンドサイドプラットフォーム（DSP）とサプライサイドプラットフォーム（SSP）の統合はサポートされていません。

このワークフローは、エンリッチメント機会の発見、オーディエンス重複の分析、アトリビューションと増分測定はサポートしていません。

## 結果の取り込みと検証 {#ingest-validate-results}

配信後、[!DNL Adobe Real-Time CDP]管理者またはテクニカルサポートチームにファイルの取り込みを依頼します。

### 出力ファイル {#output-file}

書き出しは、設定した[!DNL Amazon S3]宛先にCSV ファイルを配信します。

<!-- 
TODO: replace this placeholder with the engineering-confirmed output specification:
* Required hashing and normalization for each identifier, including whether email requires SHA-256 after trimming and lowercasing.
* Exact CSV headers, the file naming pattern, and the delivery bucket and path.
* Each identifier column in the delivered file and the identity namespace to map that column to during ingestion.
Do not treat example formats or supported input match keys as confirmed output requirements.
-->

プロファイルの更新とは別に、書き出しを確認します。

1. CSV ファイルが目的の[!DNL Amazon S3]場所に到着したことを確認します。
1. ファイルに必要な識別子と選択した属性が含まれていることを確認します。
1. ターゲットサンドボックスとデータセットの確認されたIDとスキーママッピングを使用して、ファイルを取り込みます。
1. 取り込み結果を確認し、期待されるプロファイルのサンプルにエンリッチメント属性が含まれていることを確認します。

ファイルを書き出しても、取り込みがプロファイルを更新したことを確認できません。 各後の書き出しを個別に取り込んで、プロファイルを更新します。

## エンリッチメントのトラブルシューティング {#troubleshoot-enrichment}

ソースデータ、書き出し、取り込みの問題をトラブルシューティングするには、次のチェックを使用します。

| 問題 | 確認すべきこと |
| --- | --- |
| 接続または&#x200B;**[!UICONTROL Enrich]**&#x200B;は利用できません | 管理者に接続とプロジェクトへのアクセスを確認してもらいます。 ソースフィードの設定が完了したことを確認します。 |
| 書き出し先がありません | 宛先が設定され、エンリッチメント出力に使用できることを管理者に確認してもらいます。 |
| 属性の範囲が限られています | メディアチームと共にソースデータの可用性を確認します。 カバレッジをプロファイルの一致率として解釈しないでください。 |
| 書き出しが要求されましたが、ファイルがありません | 目的の宛先をデータチームと確認する。 リクエスト送信で配信が確認されません。 |
| 配信されたファイルはプロファイルを更新していません | 取り込み結果を確認し、IDとスキーママッピングを確認します。 書き出しと取り込みは個別の操作です。 |
| 書き出しをリクエストすることはできません | 少なくとも1つの属性と宛先を選択してください。 書き出しが既に処理中の場合は、書き出しが完了するまで待ってから、別の書き出しをリクエストします。 |
| カバー率は高いものの、属性を受け取るプロファイルはほとんどありません | カバレッジはID マッチ率ではありません。 ソースフィードの準備ができており、オーディエンスがサポートされている一致キーを使用し、取り込み中にID マッピングが正しいことを確認します。 |
| プロジェクトの作成後に属性や適用範囲が表示されない | プロジェクトの設定は、作成時に固定されます。 Adobeがその時点で[!DNL The Trade Desk]からREDS ログを受信していない場合、プロジェクトは後でそれらを使用できません。 Adobeがログの受信を確認したら、新しいプロジェクトを作成します。 |
| プロファイルには属性がありますが、オーディエンスやエクスペリエンスはそれらを反映しません | オーディエンスの評価、ID、同意、エクスペリエンスのターゲティングルールを確認します。 |

## 次の手順 {#next-steps}

属性を取り込んで検証した後、エンリッチメントシグナルとファーストパーティデータを組み合わせることで、[!DNL Adobe Real-Time CDP]でオーディエンスを構築します。 詳しくは、[Audience Builder ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/segmentation/ui/audience-builder){target="_blank"}を参照してください。

宛先、パーソナライゼーション、またはカスタマージャーニーに対してオーディエンスをアクティブ化するには、[&#x200B; オーディエンスアクティベーションガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/destinations/ui/activate/activation-overview){target="_blank"}を参照してください。
