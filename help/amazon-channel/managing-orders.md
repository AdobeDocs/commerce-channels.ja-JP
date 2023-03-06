---
title: 注文の管理
description: 注文設定で注文のインポートを有効にして、コマース管理者からAmazonの注文をより簡単に管理できます。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 注文の管理

Amazonから受け取ったAmazonの注文情報は、 _[!UICONTROL Recent Orders]_セクション [ストアダッシュボード](./amazon-store-dashboard.md) または_[!UICONTROL Amazon orders]_ ページ ( _[!UICONTROL All Orders]_表示 )。

Amazonの注文の管理方法は、 [注文の設定](./order-settings.md#configure-order-settings).

## 注文のインポートを有効にした状態

後 [ストア統合](./store-integration.md)、 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定： `Enabled` デフォルトでは。 この設定では、 [!DNL Commerce] 注文はAmazon注文に対して作成され、 [[!DNL Commerce] 注文](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} ワークフロー。

>[!NOTE]
>
>注文のインポート設定に関係なく、Amazonの注文は [!DNL Amazon Seller Central] アカウントを [ストア統合](./store-integration.md) は読み込まれません。

インポートされたAmazonの注文は、 [[!DNL Commerce] 注文](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} workflow, just like your other [!DNL Commerce] stores. Click the Amazon order number in the *[!UICONTROL Order Number]* column to open the order in the [[!DNL Commerce] order process](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target="_blank"}. 詳しくは、 [Amazon注文の表示](./amazon-orders-all.md).

### 注文のインポートプロセス

Amazonで注文がおこなわれ、 [注文インポート](./order-settings.md) を有効にすると、次の処理が開始されます。

| 変更 | アクション |
|---|---|
| Amazonで注文がある。 | <ul><li>Amazonは、注文ステータスをに設定します。 `Pending`.</li><li>注文情報は次の宛先に送信されます： [!DNL Commerce].</li><li>注文が [_Amazon注文_ 表](./amazon-orders-all.md) と `Pending` ステータス。</li></ul> |
| Amazonが注文ステータスを `Unshipped`. | <ul><li>ステータスの変更は、次の宛先に送信されます： [!DNL Commerce].</li><li>内 [_Amazon注文_ 表](./amazon-orders-all.md)注文ステータスが `Unshipped`.</li><li>内 [[!DNL Commerce] オーダーワークフロー](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}、 [!DNL Commerce] 注文が `Processing` ステータス。</li></ul> |
| In [[!DNL Commerce] オーダーワークフロー](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}、 [!DNL Commerce] 注文が処理され、ステータスが `Shipped`. | <ul><li>内 [_Amazon注文_ 表](./amazon-orders-all.md)注文ステータスが `Shipped`.</li><li>次の cron ジョブでは、注文ステータスが `Complete` 内 [[!DNL Commerce] オーダーワークフロー](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.</li></ul> |

### 注文作成ブロッカー

いくつかのシナリオで、対応する [!DNL Commerce] 注文。 [!DNL Commerce] 次のいずれかの問題が発生した場合に受け取った注文に対しては、オーダーは作成されません。

| シナリオ | 解決策 |
|---|---|
| 項目が [!DNL Commerce] カタログ。 | [製品の作成](./creating-assigning-catalog-products.md) の [!DNL Commerce] カタログと [手動一致](./creating-assigning-catalog-products.md) 製品に送られます。 |
| カタログの項目は無効です。 | 必ず [製品ステータス](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} が有効になっている。 |
| 注文した項目は在庫切れです。 | の更新または設定 [製品オプション](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){target="_blank"} 数量とソースに関する |

注文がインポートできない場合、画面の上部に次のようなシステムメッセージが表示されます。

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題が解決されると、 [!DNL Commerce] 注文は次の同期時に作成されます。

## 注文のインポートが無効な場合

Amazonの注文を [!DNL Commerce]に値を入力する場合、 [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定 `Disabled`. この設定は、Amazonから新しい注文を受け取った場合、 [!DNL Commerce] オーダーが作成されません。

無効にすると、Amazonから受け取った注文情報が _[!UICONTROL Recent Orders]_ストアダッシュボードの「 」セクションと_[!UICONTROL All Orders]_ 表示 この注文情報は表示のみで、 [!DNL Amazon Seller Central]. で注文の詳細を開くには、以下を実行します。 [!DNL Amazon Seller Central]をクリックし、 _[!UICONTROL Order Number]_列。

関連トピック [Amazon注文の表示](./amazon-orders-all.md), [Amazon注文の詳細を表示](./amazon-order-details.md)、および [一般的な注文処理タスク](./common-order-processing.md).
