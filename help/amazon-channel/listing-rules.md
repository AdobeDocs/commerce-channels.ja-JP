---
title: Amazon販売チャネル - [!UICONTROL Listing Rules]
description: リストルールを使用して、Amazon Marketplace のリストとして公開されるCommerce カタログ商品を決定します。
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

でストアのリストルールにアクセスできます。 [ストアダッシュボード](./amazon-store-dashboard.md).

リストルールは、AmazonのセールスチャネルがAmazonに公開する商品を決定するためのルールを定義します。 これらのルールには、製品をリストに含めたりリストから除外したりするための、シンプルなルールから複雑なルールまで、様々なオプションが用意されています。 各ルールは、製品リストの実施要件を設定する条件で構成されます。

リストルールは常にユーザーと同期されます [!DNL Commerce] カタログ。 新規追加の場合 [!DNL Commerce] リストルールで設定された実施要件を満たす商品は、Amazonでのリスト用に自動処理されます。

- すべての商品をAmazonのリストに公開する場合は、リストルールの条件を定義しないでください。

- Amazonに公開するカタログ商品を制限する場合は、リストルール条件を定義します。 Amazon リストルールの条件の定義は、の条件の定義と同じロジックとプロセスに従います [買い物かご価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- リストルールで 1 つの製品が除外されている場合、その製品の実施要件ステータスは「」に変更されます。 `Ineligible`. 不適格な製品はAmazonに公開されません。

- 不適格な製品がAmazonに既にリストされていて、Amazonのリストをのリストと一致させる場合 [!DNL Commerce] カタログ商品、Amazonリストの数量が「」に変わります `0` 商品の販売を防止する。 Amazonのリストには、次のものがあります [手動で削除](./end-listings-manually.md).

数量と実施要件ステータスを変更すると、同じリージョンで販売する店舗に存在するマーケットプレイスの、Amazonの販売者 SKU を共有するすべてのリストに影響します（で定義） _[!UICONTROL Amazon Marketplace Country]_次の期間 [ストアの統合](./store-integration.md)）に設定します。 ただし、共有に対する変更 [!DNL Amazon Seller SKU] ある地域では、別の国での製品のAmazonのリストに影響しません。

![リストルール](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## リストルール設定の指定

1. クリック **[!UICONTROL Listing Rules]** ストアダッシュボードで、次の操作を行います。

1. Amazonにリストされる商品の実施要件に必要な条件を定義します。

参照： [例：条件の定義](./ob-define-condition-example.md).

| フィールド | 説明 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | 使用できるオプションは、 [web サイト](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) をに設定しました [!DNL Commerce] 設定。 Amazonに一覧表示されている対象の製品の web サイトを選択します。 選択できる web サイトは 1 つだけです。各 web サイトには、Amazon Sales Channel で作成された一意のAmazon ストアが必要です。 |
| [!UICONTROL Conditions] | を定義するために使用します [!DNL Commerce] Amazon リージョン内の製品実施要件の属性。 参照： [例：条件の定義](./ob-define-condition-example.md). |

## 条件ワークスペース

条件内の太字で表示されている領域をクリックして、様々なオプションを表示できます。

- 選択した web サイト内のすべての製品が対象となる場合は、条件を追加しないでください。
- Amazon システムと直接通信するための複雑なバックエンドプロセスのセットがあります。 リストを取得しようとしている商品の数や、Amazonのシステムのビジー状態（ブラックフライデーなど）によっては、Amazonに商品がリストされるまでに時間がかかる場合があります。

条件の詳細については、を参照してください。 [条件の説明](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## リストルールのプレビュー

リストルールの条件定義を変更する場合は、 **[!UICONTROL Preview Changes]** ルールの変更を適用し、リストがどのように影響を受けるかを表示します。 リストルールの変更を保存する前に、このリストプレビュー機能のリストを確認してください。

Amazonのリストは、ルールや定義済みの条件と比較されます。 その後、以下を確認できます。

- 現在のステータスに基づいて不適格ステータスに移行する製品 [!DNL Amazon Seller Central] アカウント
- 不適格な状態から適格なステータスに戻る製品
- Amazonの新しいリストに登録され、適格な商品からAmazonのリストに追加される商品 [!DNL Commerce] 製品

リストのプレビューを使用すると、潜在的なAmazonのリストをプレビューし、リストルールに必要な調整を加えることができます。

潜在的なAmazonのリストは、に入力されます _[!UICONTROL Listing Preview]_次の 3 つのタブのいずれかのページ：

- **[!UICONTROL Ineligible Listings]**  – 現在のリストルールおよび条件に基づいて、リストされた製品をAmazonにリストすることはできません。

  不適格な製品はAmazonに公開されません。 不適格な製品がAmazonに既にリストされていて、Amazonのリストをのリストと一致させる場合 [!DNL Commerce] カタログ商品、Amazonリストの数量が「」に変わります `0` 商品の販売を防止する。 リストを手動で削除するには、を参照してください [Amazon リストの終了](./end-listings-manually.md). Amazonの要件の対象とならない商品は、ここに表示されていません。 その製品は [非アクティブな一覧タブ](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]**  – 表示される製品は、現在のリストルールおよび条件に基づいてAmazonへのリスト登録が可能です。また、Amazonの要件にも対応しています。 このリストには、読み込む既存のAmazonのリストが含まれます（次がある場合） **サードパーティの一覧のインポート** をに設定 `Import Listing` 。対象： [リスト設定](./third-party-listing-settings.md)）に設定します。

- **[!UICONTROL New Listings]**  – 次の製品がリストされます [!DNL Commerce] 現在のリストルールと条件に基づいて新しくAmazon リストに登録できる製品をカタログ化し、新しいAmazon リストを作成して公開します。

### リストのプレビューを表示

1. クリック **[!UICONTROL Listing Rules]** ストアダッシュボードで、次の操作を行います。

1. の表示または追加 [リストルール](./listing-rules.md).

1. を変更 [リストルール条件](./ob-define-condition-example.md).

1. クリック **[!UICONTROL Preview Changes]**.

1. のリストを確認します。 _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_、および _[!UICONTROL New Listings]_タブ。

1. リストが期待どおりの場合は、 **[!UICONTROL Save and close]**.

   リストが期待どおりに表示されない場合は、 **[!UICONTROL Back]** リストが期待に合うまで、ルールと条件を変更します。

![リストルールのプレビュー](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### プレビューレコードのリスト

| フィールド | 説明 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | に割り当てられる一意の連続番号 [!DNL Commerce] カタログ製品（追加時）。 |
| [!UICONTROL Thumbnail] | メインの製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | で管理される製品の名前 [!DNL Commerce] [製品グリッド](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | で管理される製品のタイプ [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL Attribute Set] | で管理される、製品のテンプレートとして使用される属性セットの名前 [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL SKU] | で管理される、製品に割り当てられている一意の最小在庫管理単位 [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL Visibility] | 製品の表示場所を示し、で管理されます [!DNL Commerce] 製品グリッド。 オプション：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| ステータス | で管理される、製品のステータスを示します [!DNL Commerce] 製品グリッド。 オプション： `Enabled` / `Disabled` |

![プレビューワークフローを一覧表示](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
