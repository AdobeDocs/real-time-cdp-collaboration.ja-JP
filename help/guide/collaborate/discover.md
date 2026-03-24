---
title: 重複の検出とオーディエンスの比較
description: 自分と共同作業者のオーディエンスの重複を見つけます。 キャンペーンで使用する最適なオーディエンスを見つける方法を説明します。
audience: admin, publisher, advertiser
badgelimitedavailability: label="限定提供" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-collaboration.html newtab=true"
exl-id: 38c42ad3-9d01-4d09-b80e-37fb51cbf42b
source-git-commit: 2cd03a98228e1e379396360942227ddbcab8f6ca
workflow-type: tm+mt
source-wordcount: '2120'
ht-degree: 17%

---

# 重複の検出とオーディエンスの比較

{{limited-availability-release-note}}

>[!IMPORTANT]
>
>**[!UICONTROL 検出]** ワークスペースは、**オーディエンス検出** ユースケースが [&#x200B; 接続処理中に &#x200B;](../connect/establishing-connections.md#connection-settings) 有効になっている場合にのみ使用できます。 使用例の詳細については、[&#x200B; プロジェクトの管理 &#x200B;](./manage-projects.md#project-use-cases) ガイドを参照してください。

[&#x200B; プロジェクトの作成 &#x200B;](/help/guide/collaborate/manage-projects.md) 後、オーディエンスを共同作業者と比較できます。 これは、キャンペーンに関連するオーディエンスを特定し、アクティベーション用に共同作業者に送信するオーディエンスを決定するのに役立ちます。

>[!IMPORTANT]
>
>更新または更新されていない [&#x200B; データスケッチ &#x200B;](/help/guide/glossary.md#sketches) は、7 日後に削除されます。 これが発生すると、このページの様々な重複レポートに表示される数値がゼロになり、これらの有効期限切れのオーディエンスに対するオーディエンス共有が使用できなくなります。 データスケッチは、[&#x200B; アクティブな更新スケジュール &#x200B;](/help/guide/setup/onboard-audiences.md#schedule) を使用したオーディエンスに対して自動的に更新されます。

オーディエンスの検出と比較に使用する一致キーは、[&#x200B; 接続プロセス中 &#x200B;](/help/guide/connect/establishing-connections.md#connection-settings) に設定されます。 一致キーは、オーディエンス間の重複の計算に使用され、オンとオフを切り替えることができます。 一致キーを編集するには、「**[!UICONTROL 一致キーを編集]** オプションを選択します。

![&#x200B; オーディエンスインサイトを表示する、「ダイコバー」タブワークスペース。](/help/assets/collaborate/discover/discover-overview.png)

**[!UICONTROL マッチキーを編集]** ダイアログが開き、使用しないマッチキーを切り替えることができます。 「**[!UICONTROL 保存]**」を選択して変更を保存します。

![Discover ワークスペースの一致するキーを編集ダイアログ &#x200B;](/help/assets/collaborate/discover/edit-match-keys.png)

## 前提条件 {#prerequisites}

プロジェクト内で「**[!UICONTROL 検出]**」タブを使用するには、次のものが必要です。

* [&#x200B; ソースとなるオーディエンス &#x200B;](/help/guide/setup/onboard-audiences.md) をアカウントに追加
* [&#x200B; オーディエンス検出 &#x200B;](/help/guide/connect/establishing-connections.md) ユースケースが有効になっている共同作業者で **接続**
* 自分と共同作業者の間で [&#x200B; プロジェクトが作成されました &#x200B;](/help/guide/collaborate/manage-projects.md)

これらの前提条件が満たされたら、自分と共同作業者のオーディエンスの重複を調査し、比較することができます。

>[!NOTE]
>
>この **[!UICONTROL 検出]** ワークスペースは、広告プラットフォームとのコラボレーションには関係ありません。 現在、Amazon Marketing Cloudは、Real-Time CDP Collaborationで唯一の利用可能な広告プラットフォームです。 [!DNL AMC] **[!UICONTROL もっと知る]** ワークスペースについて詳しくは、[Amazon Marketing Cloud](/help/guide/collaborate/advertising-platforms/amc.md) ガイドを参照してください。

## オーディエンスの比較 {#compare-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_compare_audiences"
>title="オーディエンスの比較"
>abstract="ユーザーと共同作業者のオーディエンスの重複を検出します。 ドロップダウンセレクターの設定を調整すると、共同作業者の 1 つ以上のオーディエンスに対する 1 つ以上のオーディエンスの重複を検出できます。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_your_identity_count"
>title="ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づく選択したオーディエンス内の一意の ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_collaborator_identity_count"
>title="共同作業者 ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づく共同作業者のオーディエンス内の一意の ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_count"
>title="重複 ID 数"
>abstract="ユーザーと共同作業者がプロジェクトで合意した一致キーに基づくユーザーと共同作業者のオーディエンスの両方に存在する一意の ID の数。"

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlapping_identities_percentage"
>title="重複 ID の割合"
>abstract="ユーザーと共同作業者の選択したオーディエンスとの間で ID が重複している割合。"

「オーディエンスを比較」セクションを使用して、自社と共同作業者のオーディエンスの重複に関する詳細な情報を取得します。 オーディエンスの選択を変更するには、「**[!UICONTROL オーディエンスを比較]**」セクションの上部にあるドロップダウンセレクターを使用します。 オーディエンスの1つまたは全部と、共同作業者の1つまたは全部のオーディエンスを選択して、比較できます。

![&#x200B; オーディエンスの比較セクションでオーディエンスセレクターがハイライト表示された検索ワークスペース。](/help/assets/collaborate/discover/compare-audiences-selector.png)

「オーディエンスを比較」セクションには、プロジェクトで自分と共同作業者が合意した照合キーに基づく次の指標が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID数]** （自分） | 選択したオーディエンス内の一意のIDの数。 |
| **[!UICONTROL ID数]** （共同作業者） | 共同作業者のオーディエンス内の一意のIDの数。 |
| **[!UICONTROL 重複するID]** | ユーザーと共同作業者の両方のオーディエンスに存在する一意のIDの数。 |
| **[!UICONTROL 重複%]** | ユーザーと共同作業者の選択したオーディエンス間でプロファイルが重複している割合。 |
| **[!UICONTROL オーディエンスインデックス]** | スコアは、基礎となるオーディエンスサイズと重複にもとづいて、あるオーディエンスが別のオーディエンスとどの程度強く関連しているかを示します。 スコアの意味について詳しくは、「[&#x200B; オーディエンスインデックススコア &#x200B;](#audience-index-score)」の節を参照してください。 共同作業者のベースライン（すべてのオーディエンス）と比較する場合、オーディエンスインデックススコアは使用できません。 |
| **[!UICONTROL 一致キーによるIDの分類]** | 各共同作業者の選択オーディエンスに基づいて、プロジェクトで選択された各一致キーに一致するIDの内訳。 |

{style="table-layout:auto"}

>[!NOTE]
>
>重複パーセンテージの数値とオーディエンスインデックススコアは、すべてのオーディエンスが常に利用できるとは限りません。 重複率とオーディエンスインデックススコアの表示は、[&#x200B; メタデータの表示セクション &#x200B;](/help/guide/setup/onboard-audiences.md#metadata-visibility)で共同作業者がオーディエンスに対して選択した設定によって異なります。

共同作業者がオーディエンスインデックスまたは重複率を有効にしていない場合、オーディエンスには利用可能な比較データはありません。

## 関連するオーディエンス {#relevant-audiences}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_relevant_audiences"
>title="関連するオーディエンス"
>abstract="重複パーセンテージに基づき、これらのオーディエンスがキャンペーンに適している可能性があります。<br><br> <b>ID 数</b>は、共同作業者のオーディエンスサイズです。<br><br> <b>重複 ID</b> は、推奨されるオーディエンスとすべてのオーディエンス間の重複を表します。<br><br> <b>重複％</b>は、重複 ID の数を<i>すべて</i>のオーディエンスのサイズで割った値を表します。"

「**[!UICONTROL 見つける]**」タブの&#x200B;**[!UICONTROL 関連オーディエンス]** セクションには、共同作業者のオーディエンスとすべてのオーディエンスの重複率に基づいて、上位5つのオーディエンスの厳選されたリストが表示されます。 これにより、重複の大きいオーディエンスをすばやく特定し、より効果的にキャンペーンをターゲティングできます。 セクションの右上にあるページセレクターを使用して、関連オーディエンスを切り替えます。

![関連オーディエンス セクションがハイライト表示されたワークスペースを見つける。](/help/assets/collaborate/discover/relevant-audiences.png)

>[!NOTE]
>
>共同作業者のオーディエンスの表示は、共同作業者が[接続アクセス セクション &#x200B;](/help/guide/setup/onboard-audiences.md#connection-access)および[&#x200B; メタデータ表示セクション &#x200B;](/help/guide/setup/onboard-audiences.md#metadata-visibility)でオーディエンスに対して選択した設定によって異なります。 共同作業者がすべてのオーディエンスを非公開に設定している場合、このセクションにはオーディエンスは表示されません。

「**[!UICONTROL 関連オーディエンス]**」セクションには、推奨される各オーディエンスに関する次の情報が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID数]** | オーディエンス内の一意のIDの数。 |
| **[!UICONTROL 重複するID]** | 推奨オーディエンスとすべてのオーディエンス間で重複する一意のIDの数。 |
| **[!UICONTROL 重複%]** | 推奨オーディエンスとすべてのオーディエンス間の重複IDの割合。 |
| **[!UICONTROL オーディエンスインデックス]** | スコアは、基礎となるオーディエンスサイズと重複にもとづいて、あるオーディエンスが別のオーディエンスとどの程度強く関連しているかを示します。 スコアの意味について詳しくは、「[&#x200B; オーディエンスインデックススコア &#x200B;](#audience-index-score)」の節を参照してください。 |
| **[!UICONTROL オーディエンスカテゴリ]** | 共同作業者がオーディエンスに割り当てたカテゴリ。 |
| **[!UICONTROL キーの一致]** | 共同作業者がオーディエンス用に選択した照合キー。 |

{style="table-layout:auto"}

共同作業者のオーディエンスに対してオーディエンスインデックススコアが有効になっている場合、関連オーディエンスはオーディエンスインデックススコアに基づいて作成され、オーディエンスインデックスが有効になっていないオーディエンスは含まれません。 オーディエンスインデックススコアに基づく関連オーディエンスがソートされ、最も高いインデックススコアが最初に表示されます。 共同作業者のオーディエンスに対してオーディエンスインデックスが有効になっていない場合、関連オーディエンスは重複率に基づいて表示されます。

## 重複の検出 {#discover-overlaps}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_overlaps_collaborator_audiences"
>title="個々のオーディエンスとの重複の検出"
>abstract="オーディエンスと共同作業者のオーディエンスとの間の重複に関するインサイトを取得します。"

重複を発見して、オーディエンスと共同作業者のオーディエンスの比較に関するインサイトを得ることができます。 デフォルトでは、このセクションでは、すべてのオーディエンスと共同作業者の各オーディエンスを比較します。 セクションの下部にあるページネーション コントロールを使用して、使用可能なオーディエンスを移動します。

![重なりを見つけるセクションがハイライト表示されたワークスペースを見つける。](/help/assets/collaborate/discover/discover-overlaps.png)

>[!NOTE]
>
>共同作業者のオーディエンスの表示は、共同作業者が[接続アクセス セクション &#x200B;](/help/guide/setup/onboard-audiences.md#connection-access)および[&#x200B; メタデータ表示セクション &#x200B;](/help/guide/setup/onboard-audiences.md#metadata-visibility)でオーディエンスに対して選択した設定によって異なります。 共同作業者がすべてのオーディエンスを非公開に設定している場合、このセクションにはオーディエンスは表示されません。

共同作業者がオーディエンスインデックスまたは重複率を有効にしていない場合、オーディエンスは表示されません。

オーディエンスの選択を変更するには、「**[!UICONTROL オーディエンスを変更]**」を選択します。

![&#x200B; オーディエンスの変更オプションが強調表示された検索ワークスペース。](/help/assets/collaborate/discover/change-audience.png)

**[!UICONTROL オーディエンスの変更]** ダイアログが開き、特定のオーディエンスを選択して、共同作業者のオーディエンスと比較できます。 目的のオーディエンスを選択するか、選択範囲をクリアしてすべてのオーディエンスを選択し、**[!UICONTROL 保存]**&#x200B;を選択します。

![見つけるワークスペースのオーディエンスの変更ダイアログ。](/help/assets/collaborate/discover/change-audience-selection.png)

目的のオーディエンスを選択すると、「**[!UICONTROL 重複を見つける]**」セクションに、各オーディエンスに関する次の情報が表示されます。

| 指標 | 説明 |
|---------|----------|
| **[!UICONTROL ID数]** | オーディエンス内の一意のIDの数。 |
| **[!UICONTROL 重複するID]** | 推奨オーディエンスとすべてのオーディエンス間で重複する一意のIDの数。 |
| **[!UICONTROL 重複%]** | 推奨オーディエンスとすべてのオーディエンス間の重複IDの割合。 |
| **[!UICONTROL オーディエンスインデックス]** | スコアは、基礎となるオーディエンスサイズと重複にもとづいて、あるオーディエンスが別のオーディエンスとどの程度強く関連しているかを示します。 スコアの意味について詳しくは、「[&#x200B; オーディエンスインデックススコア &#x200B;](#audience-index-score)」の節を参照してください。 |
| **[!UICONTROL オーディエンスカテゴリ]** | 共同作業者がオーディエンスに割り当てたカテゴリ。 |
| **[!UICONTROL キーの一致]** | 共同作業者がオーディエンス用に選択した照合キー。 |

{style="table-layout:auto"}

## オーディエンスインデックススコア {#audience-index-score}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_discover_audience_index_score"
>title="オーディエンスインデックススコア"
>abstract="オーディエンスインデックススコアは、基になるオーディエンスの数と重複に基づいて、あるオーディエンスと別のオーディエンスの関係の強さを示す微妙な指標です。 生のインデックススコアは関連度バンドに変換され、オーディエンスインデックススコアを非常に低いものから非常に高いものへと分類します。 これにより、オーディエンスと共同作業者のオーディエンスの関係の強さをすばやく評価できます。"

オーディエンスインデックススコアは、基になるオーディエンスの数と重複に基づいて、あるオーディエンスと別のオーディエンスの関係の強さを示す微妙な指標です。 これにより、オーディエンスのインサイトを文脈化し、見込み顧客の開拓やキャンペーンのターゲティングに利用する可能性の高いオーディエンスを特定できます。

索引スコアは、次の式を使用して計算されます。

![索引スコアの計算式。](/help/assets/collaborate/discover/index-score-formula.png)

ある自動車メーカーが、大型CTV パブリッシャーと協力して、新しいSUV モデルの広告キャンペーンを実施したいと考えています。 同社は、現在、誰が類似のモデルを所有しているかに関するデータを有しており、それを活用して見込み客を獲得し、顧客に転換したいと考えています。 自動車メーカーは、CTV パブリッシャーのオーディエンスを調べて、現在のSUV オーナーとほぼ一致する関連性の高いオーディエンスを見つけます。

![自動車広告主とCTV パブリッシャーの視聴者](/help/assets/collaborate/discover/audience-index-score-example.png)

インデックススコアの計算は行われ、キャンペーンの成功の可能性を判断するために使用できます。

| CTV パブリッシャーオーディエンス | 数式 | 索引スコア （i） | 解釈 |
|------------------------|-------------|----------------|----------------|
| ベースライン（すべてのオーディエンス） | （（1.3M / 1.3M） / （50M / 50M）） * 100 | 100 | これは、共同作業者の他のオーディエンスと比較するためのベースラインとして機能します。 |
| ビンジウォッチャー | （（500k / 1.3M） / （20M / 50M）） * 100 | 96 | このオーディエンスをターゲットにすることで、ベースラインと比較してSUV オーナーにリーチする可能性が4%低くなります。 |
| コメディ愛好家 | （（200k / 1.3M） / （6M / 50M）） * 100 | 128 | このオーディエンスをターゲットにすることで、ベースラインと比較してSUV オーナーにリーチする可能性が28%高くなります。 |
| 男性25～34 | （（700k / 1.3M） / （12M / 50M）） * 100 | 224 | このオーディエンスをターゲットにすることで、ベースラインと比較してSUV オーナーにリーチする可能性が124%高くなります。 |
| 技術愛好家 | （（500k / 1.3M） / （8M / 50M）） * 100 | 240 | このオーディエンスをターゲットにすることで、ベースラインと比較してSUV オーナーにリーチする可能性が140%高くなります。 |

{style="table-layout:auto"}

インデックススコアがキャンペーンにどのような影響を与えるかをより詳細に把握するために、スコアとともに関連性バンドが提供されます。

### 関連性バンド {#audience-index-relevance-bands}

様々なオーディエンスやキャンペーンをまたいで簡単に比較できるように、Collaborationはインデックススコアを関連性バンド（非常に低いバンドから非常に高いバンド）に変換します。 これにより、オーディエンスと共同作業者のオーディエンスの関係の強さをすばやく評価できます。

| インデックススコア （i） | Relevance Band | 説明 |
|---------------|----------|-----------|
| i &lt; 60 | 非常に低い | オーディエンスに比べて、ターゲットオーディエンスでは重複がはるかに少ないことから、関係が非常に脆弱であることを示しています。 このオーディエンスを使用しているお客様は、ターゲットオーディエンスに到達する可能性がはるかに低くなります。 |
| 60 &lt; i &lt; 80 | 低 | The overlap is somewhat less prevalent in the target audience compared to your audience, suggesting a weak relationship. このオーディエンスを使用しているお客様は、ターゲットオーディエンスにリーチする可能性が低くなります。 |
| 80 &lt; i &lt; 120 | メディア | 重複は、オーディエンスと同様にターゲットオーディエンスで一般的であり、典型的な関係を示しています。 Customers using this audience have an average likelihood of reaching their target audience. |
| 120 &lt; i &lt; 140 | 高 | オーディエンスに比べてターゲットオーディエンスで重複が多く、強い関係を示しています。 このオーディエンスを使用しているお客様は、ターゲットオーディエンスにリーチする可能性が高くなります。 |
| i > 140 | 非常に高い | 重複は、非常に強い関係を反映して、オーディエンスと比較してターゲットオーディエンスではるかに一般的です。 このオーディエンスを使用しているお客様は、ターゲットオーディエンスにリーチする可能性がはるかに高くなります。 |

{style="table-layout:auto"}

Within the discover overlaps section, the audience index score will display the relevance band alongside the score. スコアは関連性バンドを示すように色分けされ、関係の強さを一目で簡単に識別できます。 非常に関連性の低いバンドはオレンジ色、中程度の関連性のバンドは黒、高と非常に関連性の高いバンドは緑で表示されます。

## 次の手順

After exploring and discovering the desired audiences, it&#39;s time to [activate](/help/guide/collaborate/activate.md) the audiences that should be used in the campaigns.
