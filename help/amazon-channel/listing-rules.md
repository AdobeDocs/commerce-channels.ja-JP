---
title: ルールの一覧表示
description: リスティングルールを使用すると、Amazon Marketplace のリストとしてパブリッシュされた Commerce カタログ製品を指定することができます。
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# ルールの一覧表示

ストアのダッシュボードには、ストアのリストルールにアクセスでき [ ](./amazon-store-dashboard.md) ます。

リスティングルールには、Amazon 販売チャンネルが Amazon に公開する製品を決定するためのルールが定義されています。 このルールには、製品一覧に製品を含めたり除外したりするために単純な複雑なルールを作成するためのオプションが数多く用意されています。 各ルールには、製品の一覧表示に関する条件が設定されています。

リストルールは、カタログと継続的に同期され [!DNL Commerce] ます。 [!DNL Commerce]リストルールによって設定された特典要件に適合する新製品を追加すると、Amazon によって製品が自動的に処理されます。

- すべての製品を Amazon リスティングに公開する場合は、リスティングルールについては定義しないでください。

- Amazon にパブリッシュされるカタログ製品の制限を設定するには、リスティングルール条件を定義します。 Amazon の一覧のルールの条件を定義すると、Cart 価格ルールの条件を定義した場合と同じロジックとプロセス、 [ ](https://docs.magento.com/user-guide/marketing/price-rules-cart.html) {target = &quot;_blank&quot;} のようになります。

- 製品を除外する場合は、その製品の適格性状態がに変更され `Ineligible` ます。 非不適合製品は、Amazon に公開されません。

- 対象外の製品が Amazon に既に一覧表示されている場合、Amazon の一覧をカタログ製品と一致させると、 [!DNL Commerce] amazon の一覧の表示が製品販売を防止するために変更され `0` ます。 Amazon リストは手動で削除することができ [ ](./end-listings-manually.md) ます。

数量および適格性の状態の変更は、同じ地域 (ストア統合時に定義されている) の Amazon 売り手 SKU を共有しているすべての番組表に影響し _[!UICONTROL Amazon Marketplace Country]_[ ](./store-integration.md) ます。 ただし、ある領域で共有すると、 [!DNL Amazon Seller SKU] 別の国にある製品の Amazon リストに変更が加えられることはありません。

![ルールの一覧表示](assets/ob-listing-rules.png)

## リスティングルール設定の構成

1. **[!UICONTROL Listing Rules]** Store のダッシュボードのをクリックします。

1. Amazon に記載されている製品の特典に必要な条件を定義します。

[次の例を参照してください。条件を定義 ](./ob-define-condition-example.md) します。

| 名 | つい |
|---|---|
| [!UICONTROL Websites] | 使用できるオプションは、設定 [ で設定されている web サイト ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) {target = &quot;_blank&quot;} によって異なり [!DNL Commerce] ます。 Amazon に記載されている適格な製品については、web サイトを選択してください。 1つの web サイトで選択できるのは、Amazon sales チャンネルで作成された固有の Amazon store が必要なので、1つの web サイトに限られます。 |
| [!UICONTROL Conditions] | [!DNL Commerce]Amazon region 内の製品の適格性の属性を定義するために使用されます。[次の例を参照してください。条件を定義 ](./ob-define-condition-example.md) します。 |

## 条件ワークスペース

条件が太字のすべての領域をクリックすると、様々なオプションが表示されます。

- 選択された web サイト内のすべての製品が適格な条件を追加することはできません。
- Amazon のシステムと直接通信するための、複雑なバックエンドプロセスのセットがあります。 リストされるアイテムの数と、Amazon のシステムの利用率が高い (黒色 (金) など) 場合は、Amazon 上のアイテムが表示されるまでに時間がかかることがあります。

条件について詳しくは、 [ ](https://docs.magento.com/user-guide/marketing/price-rules-cart.html) {target = &quot;_blank&quot;} の条件についてを参照してください。

## リストルールプレビュー

リストされているルールに基づいて条件定義を変更する場合は、をクリックして **[!UICONTROL Preview Changes]** ルールの変更を適用し、出展にどのような影響があるかを確認することができます。 リストルールの変更を保存する前に、このリストプレビュー機能の一覧を確認してください。

Amazon リストがルールと定義された条件と比較されます。 その後、次の内容を確認できます。

- 現在のアカウントに基づいて、どの製品が不適格なステータスに移行するか [!DNL Amazon Seller Central]
- 不適格状態から適格状態に移行する製品
- どの製品が新しい Amazon リストとして、適格製品から Amazon リストに追加されました。 [!DNL Commerce]

リストのプレビューを使用すると、潜在的な Amazon リストをプレビューして、必要に応じて一覧表示規則を調整することができます。

潜在的な Amazon リストは、 _[!UICONTROL Listing Preview]_次の3つのタブのいずれかでページ上に作成されます。

- **[!UICONTROL Ineligible Listings]** -リストに表示されているルールおよび条件に基づいて、表示されている製品が Amazon リストの対象となりません。

   非不適合製品は、Amazon に公開されません。 対象外の製品が Amazon に既に一覧表示されている場合、Amazon の一覧をカタログ製品と一致させると、 [!DNL Commerce] amazon の一覧の表示が製品販売を防止するために変更され `0` ます。 一覧を手動で削除するには、Amazon リスティングの終了を参照してください [ ](./end-listings-manually.md) 。 Amazon の要件を満たしていない製品は、ここには表示されません。 これらの製品は、「無効な出展」タブに一覧表示され [ ](./inactive-listings.md) ます。

- **[!UICONTROL Eligible Listings]** -リストに表示されている製品は、現在のリスティングルールと条件に基づいて、Amazon の一覧が表示されます。また、Amazon の要件にも適合しています。 このリストには、インポートされる既存の Amazon リストが表示されます (リスト表示の設定に設定された **サードパーティリストがある場合** `Import Listing` [ ](./third-party-listing-settings.md) )。

- **[!UICONTROL New Listings]** -製品リストには、 [!DNL Commerce] 現在のリストルールと条件に基づいて、Amazon リストに新しく追加されたカタログ製品が含まれているか、新しい amazon リストが作成され、公開されています。

### リストのプレビューを表示します。

1. **[!UICONTROL Listing Rules]** Store のダッシュボードのをクリックします。

1. リスティングルールを表示または追加 [ ](./listing-rules.md) します。

1. [リストルールの条件 ](./ob-define-condition-example.md) を変更します。

1. をクリックし **[!UICONTROL Preview Changes]** ます。

1. 、、およびタブの一覧を確認して確認し _[!UICONTROL Ineligible Listings]__[!UICONTROL Eligible Listings]_ _[!UICONTROL New Listings]_ます。

1. ご希望の内容と一致している場合は、をクリックし **[!UICONTROL Save and close]** ます。

   一覧が表示されない場合は、目的に合った番組が表示さ **[!UICONTROL Back]** れるまで、ルールや条件をクリックして変更します。

![リストルールプレビュー](assets/amazon-listing-rule-preview.png)

### プレビューレコードの一覧表示

| 名 | つい |
|--- |--- |
| [!UICONTROL Product ID] | カタログ製品が追加されたときに割り当てられる一意の連番 [!DNL Commerce] 。 |
| [!UICONTROL Thumbnail] | メインの製品イメージのサムネールが表示されます。 |
| [!UICONTROL Name] | 「製品グリッド」で管理されている製品の名前 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/products.html) {target = &quot;_blank&quot;}。 |
| [!UICONTROL Type] | 製品グリッドで管理されている製品のタイプ [!DNL Commerce] 。 |
| [!UICONTROL Attribute Set] | 製品グリッドで管理されている、製品のテンプレートとして使用される属性セットの名前 [!DNL Commerce] 。 |
| [!UICONTROL SKU] | 製品グリッドで管理される、製品に割り当てられている固有の在庫保管単位 [!DNL Commerce] です。 |
| [!UICONTROL Visibility] | Products グリッドで管理されている製品が表示される場所を示し [!DNL Commerce] ます。 オプション：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| 現状 | 製品グリッドで管理されている製品の状態を示し [!DNL Commerce] ます。 オプション: `Enabled` / `Disabled` |

![リストプレビューのワークフロー](assets/listing-preview-flowchart.png)
