---
title: ルールのリスト
description: リストルールを使用して、Amazon Marketplaceリストとして公開されるコマースカタログ製品を決定します。
redirect_from: /sales-channels/asc/ob-listing-rules.html/sales-channels/asc/ob-listing-preview.html/sales-channels/asc/listing-rule-preview.html
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# ルールの一覧

ストアのリストルールは、[ストアダッシュボード](./amazon-store-dashboard.md)でアクセスできます。

リストルールは、Amazonの販売チャネルをAmazonに発行する製品を決定するルールを定義します。 これらのルールには、製品をリストに含めたり除外したりする、シンプルから複雑なルールを作成するための多くのオプションが用意されています。 各ルールは、製品リストの実施要件を設定する条件で構成されます。

リストルールは、[!DNL Commerce]カタログと継続的に同期されます。 リストルールで設定された実施要件を満たす新しい[!DNL Commerce]製品を追加すると、Amazonにリスト用に自動的に処理されます。

- すべての製品をAmazonリストに公開する場合は、リストルールの条件を定義しないでください。

- Amazonに公開するカタログ商品を制限する場合は、リストルールの条件を定義します。 Amazonリストルールの条件を定義する手順は、[買い物かご価格ルール](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}の条件を定義するのと同じロジックに従います。

- リストルールで製品が除外されると、その製品の実施ステータスは`Ineligible`に変わります。 不適格な製品は、Amazonに公開されません。

- 不適格な製品がAmazonに既にリストされ、Amazonリストが[!DNL Commerce]カタログ製品と一致する場合、Amazonリストの数量は`0`に変わり、製品の販売を防ぎます。 Amazonのリストは、[手動で削除](./end-listings-manually.md)できます。

数量と適格性のステータスの変更は、同じ地域で販売する店舗向けに存在する市場でAmazonセラーのSKUを共有するすべてのリストに影響を与えます（[store integration](./store-integration.md)の間の&#x200B;_[!UICONTROL Amazon Marketplace Country]_で定義）。 ただし、1つの地域で共有[!DNL Amazon Seller SKU]を変更しても、別の国での製品のAmazonリストには影響しません。

![ルールの一覧](assets/ob-listing-rules.png)

## リストルールの設定

1. ストアダッシュボードの「**[!UICONTROL Listing Rules]**」をクリックします。

1. Amazonに表示する製品の実施要件に必要な条件を定義します。

[例：条件](./ob-define-condition-example.md)を定義します。

| フィールド | 説明 |
|---|---|
| [!UICONTROL Websites] | 使用可能なオプションは、[!DNL Commerce]設定で設定した[webサイト](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}によって異なります。 Amazonに表示される対象製品のWebサイトを選択します。 各WebサイトにはAmazonの販売チャネルで作成される一意のAmazonストアが必要なので、1つのWebサイトのみ選択できます。 |
| [!UICONTROL Conditions] | Amazon地域内の製品適格性の[!DNL Commerce]属性を定義するために使用します。 [例：条件](./ob-define-condition-example.md)を定義します。 |

## 条件ワークスペース

条件内の太字の領域をクリックすると、様々なオプションを表示できます。

- 選択したWebサイト内のすべての製品が適格な場合は、条件を追加しないでください。
- Amazonのシステムと直接通信する複雑なバックエンドプロセスのセットがあります。 リストしようとしている項目の数と、Amazonのシステムのビジー状態（ブラックフライデーなど）に基づいて、Amazonに項目がリストされるまでに時間がかかる場合があります。

条件について詳しくは、[条件の説明](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}を参照してください。

## ルールのプレビューの一覧表示

リストルールの条件定義を変更する場合は、**[!UICONTROL Preview Changes]**&#x200B;をクリックしてルールの変更を適用し、リストへの影響を確認できます。 リストルールの変更を保存する前に、このリストプレビュー機能のリストを確認してください。

Amazonのリストは、ルールおよび定義された条件と比較されます。 その後、以下を確認できます。

- 現在の[!DNL Amazon Seller Central]アカウントに基づいて、どの製品が不適格ステータスに移行するか
- 不適格な状態から適格な状態に戻る製品
- どの製品が新しいAmazonリストで、適格な[!DNL Commerce]製品からAmazonリストに追加されるか

リストプレビューを使用すると、潜在的なAmazonリストをプレビューし、リストルールを必要に応じて調整できます。

潜在的なAmazonリストは、次の3つのタブのいずれかの&#x200B;_[!UICONTROL Listing Preview]_ページに表示されます。

- **[!UICONTROL Ineligible Listings]** ：リストされた製品は、現在のリストのルールと条件に基づくAmazonリストには適用されません。

   不適格な製品は、Amazonに公開されません。 不適格な製品がAmazonに既にリストされ、Amazonリストが[!DNL Commerce]カタログ製品と一致する場合、Amazonリストの数量は`0`に変わり、製品の販売を防ぎます。 リストを手動で削除するには、「[Amazonリストの終了](./end-listings-manually.md)」を参照してください。 Amazonの要件を満たさない製品は、ここに記載されていません。 これらの製品は[[非アクティブなリスト]タブ](./inactive-listings.md)に表示されます。

- **[!UICONTROL Eligible Listings]**  — リストされた製品は、現在のリストのルールと条件に基づいてAmazonリストに登録され、Amazonの要件にも従います。このリストには、読み込む既存のAmazonリストが含まれます（[リスト設定](./third-party-listing-settings.md)で`Import Listing`に設定されている「**サードパーティリストを読み込む**」がある場合）。

- **[!UICONTROL New Listings]**  — リストに表示される製品に [!DNL Commerce] は、現在のリストのルールと条件に基づいて新しくAmazonリストに登録できるカタログ製品が含まれ、新しいAmazonリストを作成して公開します。

### リストのプレビューを表示する

1. ストアダッシュボードの「**[!UICONTROL Listing Rules]**」をクリックします。

1. [リストルール](./listing-rules.md)を表示または追加します。

1. [リストルール条件](./ob-define-condition-example.md)を変更します。

1. **[!UICONTROL Preview Changes]**&#x200B;をクリックします。

1. 「_[!UICONTROL Ineligible Listings]_」、「_[!UICONTROL Eligible Listings]_」、「_[!UICONTROL New Listings]_」の各タブでリストを確認し、確認します。

1. リストが期待どおりの場合は、**[!UICONTROL Save and close]**&#x200B;をクリックします。

   リストが期待どおりに表示されない場合は、**[!UICONTROL Back]**&#x200B;をクリックし、リストが期待どおりになるまでルールと条件を変更します。

![ルールのプレビューの一覧表示](assets/amazon-listing-rule-preview.png)

### プレビューレコードのリスト

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Product ID] | [!DNL Commerce]カタログ製品を追加したときに割り当てられる一意の順次番号。 |
| [!UICONTROL Thumbnail] | メイン製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | [!DNL Commerce] [productsグリッド](https://docs.magento.com/user-guide/catalog/products.html){target=&quot;_blank&quot;}で管理される製品の名前。 |
| [!UICONTROL Type] | [!DNL Commerce]製品グリッドで管理される製品のタイプ。 |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。[!DNL Commerce]製品グリッドで管理されます。 |
| [!UICONTROL SKU] | 製品に割り当てられる一意の在庫管理単位。[!DNL Commerce]製品グリッドで管理されます。 |
| [!UICONTROL Visibility] | 製品が表示され、[!DNL Commerce]製品グリッドで管理される場所を示します。 オプション：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| ステータス | [!DNL Commerce]製品グリッドで管理される製品のステータスを示します。 オプション：`Enabled` / `Disabled` |

![リストプレビューワークフロー](assets/listing-preview-flowchart.png)
