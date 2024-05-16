---
title: Amazon リストのデフォルトのストア設定
description: Commerceのデフォルト設定を変更して、ストアに合わせてAmazonSales Channelをカスタマイズします。
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Amazon リストのデフォルトのストア設定

ストアが接続され、最初のリストルールを設定した後、Amazonとの間のデータの同期 [!DNL Commerce] 開始。 必要に応じてストアをカスタマイズできるストア設定には、いくつかのタイプがあります。 ストア設定はストアでアクセスできます [dashboard](./amazon-store-dashboard.md).

ストアの設定は次のとおりです。

- [**[!UICONTROL Listing settings]**](./listing-settings.md)  – 製品カタログとの相互作用を制御する [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Amazon注文の管理方法を制御します。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Amazonにリストできるカタログ商品を定義します。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md)  – 適格な上場に対するAmazonの定価の変更方法を定義します。

- **[!UICONTROL Store reports]** - [競争価格分析](./competitive-price-analysis.md) および [リストの改善](./listing-improvements.md).

- **[!UICONTROL Logs]** - [リストの変更](./listing-changes-log.md) および [通信エラー](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  – のメールおよびAmazon販売チャネルストアの名前設定を確認します [!DNL Commerce] 管理者。

## 重要なデフォルト設定

| 設定 | デフォルト | 説明 | 場所 |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | 対応するを作成 [!DNL Commerce] Amazonから新しい注文を受け取った場合の注文。注文を [[!DNL Commerce] 注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。 条件 `Disabled`、Amazon注文は、レビュー用に注文情報をインポートしますが、注文は [!DNL Amazon Seller Central] アカウント。 | [オーダー設定](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Amazon注文の顧客データは、に読み込まれません [!DNL Commerce] データベース。 インポートされたAmazon注文は、ゲストチェックアウトとして処理されます。 を作成する場合 [!DNL Commerce] 顧客データベース。この設定をに変更する必要があります。 `Build New Customer Account`. | [オーダー設定](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] （Amazonの実施要件を満たす）カタログ製品をAmazonに自動公開し、Amazon リストを作成する。 製品を手動でレビューおよび公開する場合、この設定をに変更する必要があります。 `Do Not Automatically List Eligible Products`. 手動公開を待機中の製品が以下に表示される： [_リストへの準備完了_](./ready-to-list.md) タブ。 | [製品リストのアクション](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Amazon リストのベースとして使用される価格ソース属性を定義します。 を使用しない場合 [!DNL Commerce] `Price` 属性：価格設定ルールの基準となる基準価格として、この設定を別の属性に変更する必要があります。 | [上場価格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人は注文を全て履行する。 Amazonによるフルフィルメントを使用する場合、または複数のフルフィルメント方法を使用する場合、この設定を変更する必要があります。 | [履行者](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | すべての商品が同じ条件の場合は、Amazonの条件オプションの 1 つを選択して、すべての商品を表すことができます。 カタログに異なる条件（新規、使用中、再生済みなど）の製品が含まれる場合は、この設定を次のように変更する必要があります。 `Assign Condition Using Product Attribute` およびマッピング [!DNL Commerce] Amazon リスト条件に対する条件属性。 | [商品リストの条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | なし | Amazonの販売チャネルがAmazonに公開する商品を決定するために使用するルールを定義します。 これらのルールには、製品をリストに含めたりリストから除外したりするための、シンプルなルールから複雑なルールまで、様々なオプションが用意されています。 | [リストルール](./listing-rules.md) |
| 価格ルール | なし | Amazonのリスト価格属性を、定義されたものと異なるように定義します _[!UICONTROL Magento Price Source]_が含まれる [上場価格](./listing-price.md). リスト価格をユーザーに対して（上下に）調整するには_[!UICONTROL Magento Price Source]_ 設定、ルールの作成。 | [価格ルール](./pricing-products.md) |

詳しくは、を参照してください [ストアの設定](./ob-store-review.md).
