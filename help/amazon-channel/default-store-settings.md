---
title: Amazon一覧用のデフォルトのストア設定
description: デフォルトのコマース設定を変更して、ストアのAmazonSales Channelをカスタマイズします。
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Amazon一覧用のデフォルトのストア設定

ストアに接続し、最初のリストルールを設定したら、Amazonと [!DNL Commerce] 開始します。 ストア設定には、必要に応じてストアをカスタマイズできるものがいくつかあります。 ストアの設定は、ストアでアクセスされます [dashboard](./amazon-store-dashboard.md).

ストア設定には次のものが含まれます。

- [**[!UICONTROL Listing settings]**](./listing-settings.md)  — 商品カタログと [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Amazonの注文の管理方法を制御します。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Amazonに表示する資格のあるカタログ製品を定義します。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) -Amazon定価が適格な上場用にどのように変更されるかを定義します。

- **[!UICONTROL Store reports]** - [競合価格の分析](./competitive-price-analysis.md) および [リストの改善点](./listing-improvements.md).

- **[!UICONTROL Logs]** - [変更のリスト](./listing-changes-log.md) および [通信エラー](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  — でメールとAmazonセールスチャネルのストア名の設定を確認する [!DNL Commerce] 管理者。

## いくつかの重要なデフォルト設定

| 設定 | デフォルト | 説明 | 場所 |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | 対応するを作成 [!DNL Commerce] Amazonから新しい注文を受け取ったときの注文。これにより、注文を [[!DNL Commerce] 購入回数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。 条件 `Disabled`、Amazonはレビュー用に注文情報をインポートしますが、注文は、 [!DNL Amazon Seller Central] アカウント。 | [注文の設定](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Amazonの注文の顧客データは、 [!DNL Commerce] データベース。 読み込まれたAmazonの注文は、ゲストのチェックアウトとして処理されます。 を作成する場合、 [!DNL Commerce] 顧客データベースの場合、この設定を次の値に変更する必要があります： `Build New Customer Account`. | [注文の設定](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] Amazonに自動的に公開してAmazonリストを作成するための (Amazonの適格要件を満たす ) カタログ製品。 製品を手動で確認して公開する場合は、この設定をに変更してください。 `Do Not Automatically List Eligible Products`. 手動公開を待機している製品は、 [_リストへの登録準備完了_](./ready-to-list.md) タブをクリックします。 | [製品リストアクション](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Amazon一覧の基準として使用する価格ソース属性を定義します。 を使用しない場合は、 [!DNL Commerce] `Price` 属性を価格設定ルールの基準価格として使用する場合は、この設定を別の属性に変更する必要があります。 | [上場価格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人は全ての注文をする。 Amazonによる達成を使用する場合、または達成方法の組み合わせを使用する場合は、この設定を変更する必要があります。 | [実行者](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | すべての製品が同じ条件の場合、すべての製品を表すAmazon条件オプションを 1 つ選択できます。 カタログに異なる条件（新規、使用済み、リファース済みなど）の製品が含まれる場合、この設定をに変更する必要があります。 `Assign Condition Using Product Attribute` とマッピング [!DNL Commerce] 条件は、Amazonのリスト条件の属性です。 | [製品リスト条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | なし | Amazonに発行する製品を決定するために使用するルールを定義します。Amazonセールスチャネル これらのルールには、製品をリストに含めたり除外したりする、単純なルールから複雑なルールを作成するための多くのオプションが用意されています。 | [ルールの一覧表示](./listing-rules.md) |
| 価格ルール | なし | 定義済みとは異なるAmazon定価属性を定義 _[!UICONTROL Magento Price Source]_の [上場価格](./listing-price.md). 定価を（上か下に）_[!UICONTROL Magento Price Source]_ を設定し、ルールを作成します。 | [価格ルール](./pricing-products.md) |

詳しくは、 [ストア設定](./ob-store-review.md).
