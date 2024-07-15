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

ストアが接続され、最初のリストルールを設定すると、Amazonと [!DNL Commerce] の間のデータの同期が開始されます。 必要に応じてストアをカスタマイズできるストア設定には、いくつかのタイプがあります。 ストアの設定は、ストア [ ダッシュボード ](./amazon-store-dashboard.md) でアクセスできます。

ストアの設定は次のとおりです。

- [**[!UICONTROL Listing settings]**](./listing-settings.md) – 製品カタログと [!DNL Amazon Marketplace] とのやり取りを制御します。

- [**[!UICONTROL Order settings]**](./order-settings.md) - Amazon注文の管理方法を制御します。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Amazonにリストできる適格なカタログ商品を定義します。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) – 限定提供リストでAmazonの定価を変更する方法を定義します。

- **[!UICONTROL Store reports]** - [ 競争価格分析 ](./competitive-price-analysis.md) および [ リストの改善 ](./listing-improvements.md)。

- **[!UICONTROL Logs]** - [ 変更のリスト ](./listing-changes-log.md) および [ 通信エラー ](./communication-errors-log.md)。

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - [!DNL Commerce] Admin でメールおよびAmazonのセールスチャネルストアの名前設定を確認します。

## 重要なデフォルト設定

| 設定 | デフォルト | 説明 | 場所 |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | Amazonから新しい注文を受け取ると、対応する [!DNL Commerce] しい注文を作成し、注文を [[!DNL Commerce]  注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフローで管理できるようにします。 `Disabled` の場合、Amazonの注文はレビュー用に注文情報をインポートしますが、注文は [!DNL Amazon Seller Central] アカウントで管理する必要があります。 | [ 順序設定 ](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Amazon注文の顧客データは、[!DNL Commerce] データベースに読み込まれません。 インポートされたAmazon注文は、ゲストチェックアウトとして処理されます。 [!DNL Commerce] 顧客データベースを構築する場合、この設定を `Build New Customer Account` に変更する必要があります。 | [ 順序設定 ](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | （Amazonの実施要件を満たす）カタログ製品を [!DNL Commerce] 開して、Amazonに自動的に公開し、Amazon リストを作成します。 製品を手動でレビューおよび公開する場合、この設定を `Do Not Automatically List Eligible Products` に変更する必要があります。 手動公開を待機している製品は、「[_リストへの準備完了_](./ready-to-list.md) タブに表示されます。 | [ 製品リストのアクション ](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Amazon リストのベースとして使用される価格ソース属性を定義します。 価格設定ルールの基準となる基本価格として [!DNL Commerce] `Price` 属性を使用しない場合は、この設定を別の属性に変更する必要があります。 | [ 上場価格 ](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人は注文を全て履行する。 Amazonによるフルフィルメントを使用する場合、または複数のフルフィルメント方法を使用する場合、この設定を変更する必要があります。 | [ フルフィルメント ](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | すべての商品が同じ条件の場合は、Amazonの条件オプションの 1 つを選択して、すべての商品を表すことができます。 カタログに、異なる条件（新規、使用済み、再生済みなど）の商品が含まれている場合は、この設定を `Assign Condition Using Product Attribute` に変更し、[!DNL Commerce] の条件属性をAmazonのリスト条件にマッピングする必要があります。 | [ 商品リストの状態 ](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | なし | Amazonの販売チャネルがAmazonに公開する商品を決定するために使用するルールを定義します。 これらのルールには、製品をリストに含めたりリストから除外したりするための、シンプルなルールから複雑なルールまで、様々なオプションが用意されています。 | [ 上場準則 ](./listing-rules.md) |
| 価格ルール | なし | [ 上場価格 ](./listing-price.md) で定義した _[!UICONTROL Magento Price Source]_とは異なるAmazon上場価格属性を定義します。_[!UICONTROL Magento Price Source]_ の設定に照らしてリスト価格を（上下に）調整するには、ルールを作成します。 | [ 価格決定ルール ](./pricing-products.md) |

詳しくは、[ ストア設定 ](./ob-store-review.md) を参照してください。
