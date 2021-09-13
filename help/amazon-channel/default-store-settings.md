---
title: デフォルトのストア設定
description: デフォルトのコマース設定を変更して、ストアのAmazonSales Channelをカスタマイズします。
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# デフォルトのストア設定

ストアに接続し、最初のリストルールを設定したら、Amazonと[!DNL Commerce]の間でデータの同期が開始されます。 ストア設定には、ニーズに合わせてストアをカスタマイズできるものがいくつかあります。 ストアの設定は、ストア[ダッシュボード](./amazon-store-dashboard.md)でアクセスします。

ストア設定には次のものが含まれます。

- [**[!UICONTROL Listing settings]**](./listing-settings.md)  — 製品カタログとのやり取りを制御しま [!DNL Amazon Marketplace]す。

- [**[!UICONTROL Order settings]**](./order-settings.md) - Amazonの注文の管理方法を制御します。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Amazonでリスト表示する資格のあるカタログ製品を定義します。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md)  — 認定リストに対するAmazonの定価の変更方法を定義します。

- **[!UICONTROL Store reports]**  — 競合 [価格分析](./competitive-price-analysis.md) と [上場の改善](./listing-improvements.md)。

- **[!UICONTROL Logs]**  — 変更 [と通信](./listing-changes-log.md) エラー [を表示します](./communication-errors-log.md)。

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  — 管理者で、電子メールおよびAmazonの販売チャネルストア名の設定を確認 [!DNL Commerce] します。

## 重要なデフォルト設定

| 設定 | デフォルト | 説明 | 場所 |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Amazonから新しい注文を受け取ると、対応する[!DNL Commerce]注文が作成され、[[!DNL Commerce] 注文](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}ワークフローで注文を管理できます。 `Disabled`の場合、Amazonはレビュー用に注文情報をインポートしますが、注文は[!DNL Amazon Seller Central]アカウントで管理する必要があります。 | [順序の設定](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Amazonの注文の顧客データは、[!DNL Commerce]データベースにインポートされません。 インポートされたAmazonの注文は、ゲストのチェックアウトとして処理されます。 [!DNL Commerce]顧客データベースを構築する場合は、この設定を`Build New Customer Account`に変更する必要があります。 | [順序の設定](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] (Amazonの適格性要件を満たす)カタログ製品を使用して、Amazonに自動的に公開し、Amazonリストを作成します。製品を手動で確認して公開する場合は、この設定を`Do Not Automatically List Eligible Products`に変更する必要があります。 手動公開を待機している製品が「[_リストへの準備完了_](./ready-to-list.md)」タブに表示されます。 | [製品リストのアクション](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Amazonの一覧表示の基準として使用する価格ソース属性を定義します。 [!DNL Commerce] `Price`属性を価格設定ルールの基準価格として使用しない場合は、この設定を別の属性に変更する必要があります。 | [上場価格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | 商人は注文を全て処理する。 Amazonによるフルフィルメントを使用する場合、またはフルフィルメント方法を組み合わせて使用する場合は、この設定を変更する必要があります。 | [実行者](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | すべての製品が同じ条件の場合、すべての製品を表すAmazon条件オプションを1つ選択できます。 カタログに様々な条件（「新規」、「使用済み」、「再構築済み」など）の製品が含まれる場合は、この設定を`Assign Condition Using Product Attribute`に変更し、[!DNL Commerce]条件属性をAmazonのリスト条件にマッピングする必要があります。 | [製品リスト条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | なし | Amazonに発行する製品を決定するために使用されるルールを定義します。Amazon Sales Channel これらのルールには、製品をリストに含めたり除外したりする、シンプルから複雑なルールを作成するための多くのオプションが用意されています。 | [ルールのリスト](./listing-rules.md) |
| 価格ルール | なし | [Listing Price](./listing-price.md)で定義した&#x200B;_[!UICONTROL Magento Price Source]_とは異なるAmazonの定価属性を定義します。_[!UICONTROL Magento Price Source]_&#x200B;の設定に合わせて定価を調整するには、ルールを作成します。 | [価格ルール](./pricing-products.md) |

詳しくは、[ストア設定](./ob-store-review.md)を参照してください。
