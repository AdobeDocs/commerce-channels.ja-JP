---
title: 注文の管理
description: 注文の設定で注文のインポートを有効にして、コマース管理者からAmazonの注文をより簡単に管理できます。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 注文の管理

Amazonから受け取ったAmazonの注文情報は、[store dashboard](./amazon-store-dashboard.md)の&#x200B;_[!UICONTROL Recent Orders]_セクションまたは_[!UICONTROL Amazon orders]_&#x200B;ページ（_[!UICONTROL All Orders]_ビューとも呼ばれます）で確認できます。

Amazonの注文の管理方法は、[注文設定](./order-settings.md#configure-order-settings)で注文のインポートが有効か無効かによって異なります。

## 注文のインポートを有効にする

[store integration](./store-integration.md)の後、[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)設定はデフォルトで`Enabled`になります。 この設定を使用すると、対応する[!DNL Commerce]注文がAmazonの注文に対して作成され、[[!DNL Commerce] 注文](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}ワークフローで管理できます。

>[!NOTE]
>
>注文のインポート設定に関係なく、[ストア統合](./store-integration.md)の前に[!DNL Amazon Seller Central]アカウントに存在していたAmazonの注文はインポートされません。

インポートされたAmazonの注文は、他の[!DNL Commerce]ストアと同様に、[[!DNL Commerce] Orders](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}ワークフローで管理されます。 *[!UICONTROL Order Number]*&#x200B;列のAmazonの注文番号をクリックして、[[!DNL Commerce] 注文プロセス](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}で注文を開きます。 [Amazon注文](./amazon-orders-all.md)の表示を参照してください。

### 注文のインポート処理

Amazonで注文がおこなわれ、[注文のインポート](./order-settings.md)が有効になると、次の処理が開始されます。

| 変更 | アクション |
|---|---|
| Amazonに註文がある。 | <ul><li>Amazonは注文ステータスを`Pending`に設定します。</li><li>注文情報は[!DNL Commerce]に送信されます。</li><li>[_Amazonの注文_&#x200B;テーブル](./amazon-orders-all.md)に`Pending`ステータスで注文が追加されます。</li></ul> |
| Amazonは注文ステータスを`Unshipped`に変更します。 | <ul><li>ステータスの変更は[!DNL Commerce]に送信されます。</li><li>[_Amazonの注文_&#x200B;テーブル](./amazon-orders-all.md)で、注文ステータスが`Unshipped`に変わります。</li><li>[[!DNL Commerce] ordersワークフロー](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}では、対応する[!DNL Commerce]順序が`Processing`ステータスで作成されます。</li></ul> |
| [[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}では、[!DNL Commerce]の順序が処理され、ステータスが`Shipped`に変わります。 | <ul><li>[_Amazonの注文_&#x200B;テーブル](./amazon-orders-all.md)で、注文ステータスが`Shipped`に変わります。</li><li>次のcronジョブでは、[[!DNL Commerce] orders workflow](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}の順序ステータスが`Complete`に変わります。</li></ul> |

### 注文作成ブロッカー

対応する[!DNL Commerce]の順序が作成されないシナリオがいくつかあります。 [!DNL Commerce] 次のいずれかの問題が発生した場合に受け取った受注に対しては、受注は作成されません。

| シナリオ | 解決策 |
|---|---|
| 項目が[!DNL Commerce]カタログに存在しません。 | [カタログ](./creating-assigning-catalog-products.md) で製品を作 [!DNL Commerce] 成し、製 [品に](./creating-assigning-catalog-products.md) 手動で適合させます。 |
| カタログ内の項目は無効になります。 | [製品ステータス](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;}が有効になっていることを確認します。 |
| 注文した品目は在庫切れです。 | 数量とソースに関しては、[製品オプション](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;}を更新または設定します。 |

注文をインポートできない場合、画面の上部に次のようなシステムメッセージが表示されます。

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題が解決されると、次の同期時に[!DNL Commerce]順序が作成されます。

## 注文のインポートが無効な場合

[!DNL Commerce]でAmazonの注文をインポートおよび管理したくない場合は、[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)設定を`Disabled`に変更できます。 この設定は、Amazonから新しい注文を受け取った場合、対応する[!DNL Commerce]注文は作成されないことを意味します。

無効にすると、Amazonから受け取った注文情報がストアダッシュボードの&#x200B;_[!UICONTROL Recent Orders]_セクションと_[!UICONTROL All Orders]_&#x200B;ビューに表示されます。 この注文情報は表示のみで、[!DNL Amazon Seller Central]で管理する必要があります。 [!DNL Amazon Seller Central]で注文の詳細を開くには、_[!UICONTROL Order Number]_列のAmazon注文番号をクリックします。

[Amazonの注文](./amazon-orders-all.md)の表示、[Amazonの注文の詳細](./amazon-order-details.md)の表示、[一般的な注文処理タスク](./common-order-processing.md)も参照してください。
