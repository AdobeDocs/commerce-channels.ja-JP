---
title: Amazon注文の管理
description: 注文設定で注文の読み込みを有効にして、Commerce管理者からAmazonの注文をより簡単に管理できます。
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Amazon注文の管理

Amazonから受け取ったAmazonの注文情報は、[ ストアダッシュボード ](./amazon-store-dashboard.md) の _[!UICONTROL Recent Orders]_セクション、または_[!UICONTROL Amazon orders]_ ページ（_[!UICONTROL All Orders]_ビューとも呼ばれます）で表示できます。

Amazonの注文の管理方法は、「Order Settings[ で注文の読み込みが有効になっているか無効になっているかによって異なり ](./order-settings.md#configure-order-settings) す。

## 注文の読み込みが有効な場合

[ ストア統合 ](./store-integration.md) 後、[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定はデフォルトで `Enabled` 定されます。 この設定を使用すると、Amazonの注文に対応する [!DNL Commerce] 注文が作成され、[[!DNL Commerce]  注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフローで管理できます。

>[!NOTE]
>
>注文の読み込み設定に関係なく、[ ストア統合 ](./store-integration.md) の前に [!DNL Amazon Seller Central] アカウントに存在していたAmazonの注文は読み込まれません。

読み込まれたAmazonの注文は、他の [!DNL Commerce] ストアと同様に、[[!DNL Commerce]  注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフローで管理されます。 *[!UICONTROL Order Number]* 列のAmazon注文番号をクリックして、[[!DNL Commerce]  注文プロセス ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions) で注文を開きます。 [Amazon注文の表示 ](./amazon-orders-all.md) を参照してください。

### 注文のインポートプロセス

Amazonに注文し、[ 注文の読み込み ](./order-settings.md) が有効になると、次のプロセスが開始されます。

| 変更 | アクション |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amazonで注文が行われます。 | <ul><li>Amazonは、注文ステータスを `Pending` に設定します。</li><li>注文情報が [!DNL Commerce] に送信されます。</li><li>注文が [_Amazon注文_ テーブル ](./amazon-orders-all.md) に追加され、ステータスが「`Pending`」になります。</li></ul> |
| Amazonが注文ステータスを `Unshipped` に変更します。 | <ul><li>ステータスの変更が [!DNL Commerce] に送信されます。</li><li>[_Amazon orders_ テーブル ](./amazon-orders-all.md) では、注文ステータスが `Unshipped` に変わります。</li><li>[[!DNL Commerce]  注文ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) では、対応する [!DNL Commerce] 注文が `Processing` ステータスで作成されます。</li></ul> |
| [[!DNL Commerce]  注文ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) では、[!DNL Commerce] 注文が処理され、ステータスが `Shipped` に変わります。 | <ul><li>[_Amazon orders_ テーブル ](./amazon-orders-all.md) では、注文ステータスが `Shipped` に変わります。</li><li>次の cron ジョブで、[[!DNL Commerce]  注文ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) の注文ステータスが `Complete` に変わります。</li></ul> |

### オーダー作成ブロッカー

対応する [!DNL Commerce] の順序を作成できないシナリオがいくつかあります。 次のいずれかの問題が発生した場合、受け取った注文に対して [!DNL Commerce] の注文は作成されません。

| シナリオ | 解決策 |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!DNL Commerce] カタログにアイテムが存在しません。 | [!DNL Commerce] カタログ内で [ 製品を作成 ](./creating-assigning-catalog-products.md) し、その製品を [ 手動で一致 ](./creating-assigning-catalog-products.md) させます。 |
| カタログ内の項目が無効になっています。 | [ 製品ステータス ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) が有効になっていることを確認します。 |
| 注文した商品は在庫切れです。 | 数量およびソースの [ 製品オプション ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) を更新または設定します。 |

注文をインポートできない場合は、次のようなシステムメッセージが画面の上部に表示されます。

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題が解決すると、次回の同期で [!DNL Commerce] 注書が作成されます。

## 注文の読み込みが無効の場合

Amazonの注文を [!DNL Commerce] に読み込んで管理しない場合は、[**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定を `Disabled` に変更できます。 この設定では、Amazonから新しい注文を受け取っても、対応す [!DNL Commerce] 注文が作成されません。

無効にすると、Amazonから受け取った注文情報が、ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションと_[!UICONTROL All Orders]_ 表示に表示されます。 この注文情報は表示のみなので、これらの注文を [!DNL Amazon Seller Central] で管理する必要があります。 注文の詳細を [!DNL Amazon Seller Central] で開くには、_[!UICONTROL Order Number]_列のAmazon注文番号をクリックします。

[Amazon注文の表示 ](./amazon-orders-all.md)、[Amazon注文の詳細の表示 ](./amazon-order-details.md)、および [ 一般的な注文処理タスク ](./common-order-processing.md) も参照してください。
