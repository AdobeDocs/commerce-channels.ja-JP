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

[ ストアダッシュボード ](./amazon-store-dashboard.md) で、ストアのリストルールにアクセスできます。

リストルールは、AmazonのセールスチャネルがAmazonに公開する商品を決定するためのルールを定義します。 これらのルールには、製品をリストに含めたりリストから除外したりするための、シンプルなルールから複雑なルールまで、様々なオプションが用意されています。 各ルールは、製品リストの実施要件を設定する条件で構成されます。

リストルールは、[!DNL Commerce] カタログと継続的に同期されます。 リストルールで設定された実施要件を満たす新しい [!DNL Commerce] 製品を追加すると、その製品はAmazonでのリスト用に自動処理されます。

- すべての商品をAmazonのリストに公開する場合は、リストルールの条件を定義しないでください。

- Amazonに公開するカタログ商品を制限する場合は、リストルール条件を定義します。 Amazonのリストルールの条件の定義は、[ 買い物かご価格ルール ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) の条件の定義と同じロジックとプロセスに従います。

- リストルールで製品が除外されると、その製品の実施要件ステータスが `Ineligible` に変更されます。 不適格な製品はAmazonに公開されません。

- 不適格な商品が既にAmazonにリストされていて、Amazonのリストを [!DNL Commerce] カタログの商品と一致させる場合は、商品の売り上げを防ぐために、Amazonのリストの数量が `0` に変わります。 Amazonのリストは、[ 手動で削除 ](./end-listings-manually.md) できます。

数量と実施要件のステータスを変更すると、同じリージョンで販売する店舗に存在するマーケットプレイスの、Amazonの販売者 SKU を共有するすべてのリストに影響します（[ 店舗の統合 ](./store-integration.md) 中に _[!UICONTROL Amazon Marketplace Country]_で定義した通り）。 ただし、ある地域で共有 [!DNL Amazon Seller SKU] を変更しても、別の国での製品のAmazonのリストには影響しません。

![ リストルール ](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## リストルール設定の指定

1. ストアダッシュボードで「**[!UICONTROL Listing Rules]**」をクリックします。

1. Amazonにリストされる商品の実施要件に必要な条件を定義します。

[ 例：条件を定義 ](./ob-define-condition-example.md) を参照してください。

| フィールド | 説明 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | 使用できるオプションは、[!DNL Commerce] 設定で設定した [web サイト ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) によって異なります。 Amazonに一覧表示されている対象の製品の web サイトを選択します。 選択できる web サイトは 1 つだけです。各 web サイトには、Amazon Sales Channel で作成された一意のAmazon ストアが必要です。 |
| [!UICONTROL Conditions] | Amazonリージョン内で製品の実施要件に対する [!DNL Commerce] 属性を定義するために使用します。 [ 例：条件を定義 ](./ob-define-condition-example.md) を参照してください。 |

## 条件ワークスペース

条件内の太字で表示されている領域をクリックして、様々なオプションを表示できます。

- 選択した web サイト内のすべての製品が対象となる場合は、条件を追加しないでください。
- Amazon システムと直接通信するための複雑なバックエンドプロセスのセットがあります。 リストを取得しようとしている商品の数や、Amazonのシステムのビジー状態（ブラックフライデーなど）によっては、Amazonに商品がリストされるまでに時間がかかる場合があります。

条件の詳細については、「[ 条件の説明 ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html)」を参照してください。

## リストルールのプレビュー

リストルールの条件定義を変更する場合は、「**[!UICONTROL Preview Changes]**」をクリックしてルールの変更を適用し、リストへの影響を確認できます。 リストルールの変更を保存する前に、このリストプレビュー機能のリストを確認してください。

Amazonのリストは、ルールや定義済みの条件と比較されます。 その後、以下を確認できます。

- 現在の [!DNL Amazon Seller Central] アカウントに基づいて不適格ステータスに移行する製品
- 不適格な状態から適格なステータスに戻る製品
- Amazonの新しいリストに登録され、適格な [!DNL Commerce] 製品からAmazonのリストに追加される製品

リストのプレビューを使用すると、潜在的なAmazonのリストをプレビューし、リストルールに必要な調整を加えることができます。

潜在的なAmazonのリストは、次の 3 つのタブのいずれかで _[!UICONTROL Listing Preview]_ページに表示されます。

- **[!UICONTROL Ineligible Listings]** – 現在のリストルールおよび条件に基づいて、リストされた製品をAmazonにリストすることはできません。

  不適格な製品はAmazonに公開されません。 不適格な商品が既にAmazonにリストされていて、Amazonのリストを [!DNL Commerce] カタログの商品と一致させる場合は、商品の売り上げを防ぐために、Amazonのリストの数量が `0` に変わります。 リストを手動で削除するには、[Amazon リストの終了 ](./end-listings-manually.md) を参照してください。 Amazonの要件の対象とならない商品は、ここに表示されていません。 これらの製品は、[ 非アクティブなリスト タブ ](./inactive-listings.md) に一覧表示されます。

- **[!UICONTROL Eligible Listings]** – 表示される製品は、現在のリストルールおよび条件に基づいてAmazonへのリスト登録が可能です。また、Amazonの要件にも対応しています。 このリストには、読み込む既存のAmazonの一覧が含まれます（「**サードパーティの一覧を読み込む** が [ 一覧設定 ](./third-party-listing-settings.md) で `Import Listing` に設定されている場合）。

- **[!UICONTROL New Listings]** – 表示される製品には、現在のリストルールおよび条件に基づいて新たにAmazonのリストに登録できる [!DNL Commerce] カタログ製品が含まれます。また、新しいAmazonのリストを作成して公開することもできます。

### リストのプレビューを表示

1. ストアダッシュボードで「**[!UICONTROL Listing Rules]**」をクリックします。

1. [ リストルール ](./listing-rules.md) の表示または追加

1. [ リストルール条件 ](./ob-define-condition-example.md) を変更します。

1. 「**[!UICONTROL Preview Changes]**」をクリックします。

1. _[!UICONTROL Ineligible Listings]_、_[!UICONTROL Eligible Listings]_、_[!UICONTROL New Listings]_のタブでリストを確認して確認します。

1. リストが期待どおりの場合は、「**[!UICONTROL Save and close]**」をクリックします。

   リストが期待どおりに表示されない場合は、「**[!UICONTROL Back]**」をクリックし、リストが期待どおりに表示されるまでルールと条件を変更します。

![ リストルールのプレビュー ](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### プレビューレコードのリスト

| フィールド | 説明 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | カタログ製品を追加したときに割り当てられる一意の [!DNL Commerce] 番です。 |
| [!UICONTROL Thumbnail] | メインの製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | [!DNL Commerce] [ 製品グリッド ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) で管理される製品の名前。 |
| [!UICONTROL Type] | [!DNL Commerce] 製品グリッドで管理される製品のタイプ。 |
| [!UICONTROL Attribute Set] | [!DNL Commerce] 製品グリッドで管理される、製品のテンプレートとして使用される属性セットの名前。 |
| [!UICONTROL SKU] | 商品に割り当てられる一意の在庫管理単位。[!DNL Commerce] 商品グリッドで管理されます。 |
| [!UICONTROL Visibility] | 製品が表示される場所を示し、[!DNL Commerce] 製品グリッドで管理されます。 オプション：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| ステータス | [!DNL Commerce] 製品グリッドで管理される製品の状態を示します。 オプション：`Enabled` / `Disabled` |

![ プレビューワークフローを一覧表示 ](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
