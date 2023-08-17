---
title: Amazon セールスチャネル - [!UICONTROL Listing Rules]
description: リストルールを使用して、Amazon Marketplace リストとして公開する Commerce カタログ製品を決定します。
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

ストアのリストルールには、 [ストアダッシュボード](./amazon-store-dashboard.md).

リストルールは、AmazonセールスチャネルがAmazonに公開する製品を決定するルールを定義します。 これらのルールには、製品をリストに含めたり除外したりする、単純なルールから複雑なルールを作成するための多くのオプションが用意されています。 各ルールは、製品リストの実施要件を設定する条件で構成されます。

リストルールは、 [!DNL Commerce] カタログ。 新しい [!DNL Commerce] リストルールで設定された適格要件を満たす製品は、Amazonで自動的に処理されてリストに表示されます。

- すべての製品をAmazonリストに公開する場合は、リストルールの条件を定義しないでください。

- Amazonに公開するカタログ商品を制限する場合は、リストルールの条件を定義します。 Amazonリストルールの条件の定義は、 [買い物かごの価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- リストルールで製品が除外される場合、その製品の適格性ステータスは「 `Ineligible`. 不適格な製品はAmazonに公開されません。

- 不適格な製品が既にAmazonにリストされていて、Amazonリストが [!DNL Commerce] カタログ製品、Amazonリストの数量の変更 `0` 製品の販売を防ぐ。 Amazonのリストは、 [手動で削除](./end-listings-manually.md).

数量と適格性のステータスの変更は、同じ地域で販売する店舗に存在する市場で、Amazonのセラー SKU を共有するすべてのリストに影響します ( _[!UICONTROL Amazon Marketplace Country]_期間 [ストア統合](./store-integration.md)) をクリックします。 ただし、共有された [!DNL Amazon Seller SKU] ある地域では、別の国での製品のAmazonリストには影響しません。

![リストルール](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## リストルールの設定

1. クリック **[!UICONTROL Listing Rules]** を選択します。

1. Amazonに表示される製品の適格要件に関する必要な条件を定義します。

詳しくは、 [例：条件の定義](./ob-define-condition-example.md).

| フィールド | 説明 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | 使用可能なオプションは、 [web サイト](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定が完了したら、 [!DNL Commerce] 設定。 Amazonに表示される対象製品の Web サイトを選択します。 各 Web サイトにはAmazonセールスチャネルで作成する一意のAmazonストアが必要なので、選択できる Web サイトは 1 つだけです。 |
| [!UICONTROL Conditions] | を定義するために使用されます。 [!DNL Commerce] Amazon地域での製品適格要件の属性。 詳しくは、 [例：条件の定義](./ob-define-condition-example.md). |

## 条件ワークスペース

条件内の太字の領域をクリックすると、様々なオプションを表示できます。

- 選択した Web サイト内のすべての製品が適格な場合は、条件を追加しないでください。
- Amazonのシステムと直接通信する複雑なバックエンドプロセスのセットがあります。 リストしようとしている項目の数と、Amazonのシステムのビジー状態（ブラックフライデーなど）に基づいて、Amazonに項目がリストされるまでに時間がかかる場合があります。

条件について詳しくは、 [条件の説明](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## リストルールのプレビュー

リストルールの条件定義を変更する場合は、 **[!UICONTROL Preview Changes]** ルールの変更を適用し、リストへの影響を確認するには、次の手順に従います。 リストルールの変更を保存する前に、このリストプレビュー機能のリストを確認してください。

Amazonのリストは、ルールおよび定義された条件と比較されます。 その後、以下を確認できます。

- 現在の状況に基づいて、どの製品が不適格ステータスに移行するか [!DNL Amazon Seller Central] アカウント
- 不適格な状態から適格な状態に戻す製品
- 対象となる製品から、新しいAmazonリストであり、Amazonリストに追加される製品 [!DNL Commerce] 製品

リストのプレビューを使用すると、潜在的なAmazonリストをプレビューし、リストルールに必要な調整をおこなうことができます。

使用可能なAmazonのリストは、 _[!UICONTROL Listing Preview]_次の 3 つのタブのいずれかで、

- **[!UICONTROL Ineligible Listings]**  — リストされた製品は、現在のリストルールおよび条件に基づくAmazonリストに登録する資格がありません。

  不適格な製品はAmazonに公開されません。 不適格な製品が既にAmazonにリストされていて、Amazonリストが [!DNL Commerce] カタログ製品、Amazonリストの数量の変更 `0` 製品の販売を防ぐ。 リストを手動で削除するには、 [Amazonリストの終了](./end-listings-manually.md). Amazonの要件を満たさない製品は、ここに記載されていません。 これらの製品は、 [非アクティブなリストタブ](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]**  — リストされた製品は、現在のリストルールおよび条件に基づくAmazonリストへの登録に使用でき、Amazon要件にも基づく適格です。 このリストには、読み込む既存のAmazonリストが含まれます ( **サードパーティリストの読み込み** に設定 `Import Listing` in [リスト設定](./third-party-listing-settings.md)) をクリックします。

- **[!UICONTROL New Listings]**  — リストに表示される製品には、 [!DNL Commerce] 現在のリストルールおよび条件に基づいて新しくAmazonリストに登録できる商品をカタログ化し、新しいAmazonリストを作成して公開します。

### リストのプレビューを表示

1. クリック **[!UICONTROL Listing Rules]** を選択します。

1. を表示または追加します。 [リストルール](./listing-rules.md).

1. を変更します。 [ルール条件のリスト](./ob-define-condition-example.md).

1. クリック **[!UICONTROL Preview Changes]**.

1. リストを確認し、 _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_、および _[!UICONTROL New Listings]_タブ。

1. お使いのリストが期待どおりの内容の場合は、 **[!UICONTROL Save and close]**.

   リストが期待どおりに表示されない場合は、[ ] をクリックします。 **[!UICONTROL Back]** リストが期待どおりになるまで、ルールと条件を変更します。

![リストルールのプレビュー](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### プレビューレコードのリスト

| フィールド | 説明 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | に割り当てられる一意の順番 [!DNL Commerce] カタログ製品を追加する際に使用します。 |
| [!UICONTROL Thumbnail] | メイン製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | で管理される製品の名前。 [!DNL Commerce] [製品グリッド](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | で管理される製品のタイプ [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。 [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL SKU] | 製品に割り当てられ、で管理される一意の在庫管理単位 [!DNL Commerce] 製品グリッド。 |
| [!UICONTROL Visibility] | 製品が表示され、で管理される場所を示します。 [!DNL Commerce] 製品グリッド。 オプション：<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| ステータス | 製品のステータスを示します。 [!DNL Commerce] 製品グリッド。 オプション： `Enabled` / `Disabled` |

![リストのプレビューワークフロー](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
