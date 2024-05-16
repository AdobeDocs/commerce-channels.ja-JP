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

Amazonから受け取ったAmazonの注文情報は、 _[!UICONTROL Recent Orders]_の節 [ストアダッシュボード](./amazon-store-dashboard.md) または_[!UICONTROL Amazon orders]_ ページ（ _[!UICONTROL All Orders]_表示）。

Amazon注文の管理方法は、で注文の読み込みが有効になっているか無効になっているかによって異なります。 [オーダー設定](./order-settings.md#configure-order-settings).

## 注文の読み込みが有効な場合

後 [ストアの統合](./store-integration.md), [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) 設定はです `Enabled` デフォルトでは。 この設定では、に対応します [!DNL Commerce] 注文はAmazon注文用に作成され、 [[!DNL Commerce] 注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。

>[!NOTE]
>
>注文の読み込み設定に関係なく、に存在したAmazon注文 [!DNL Amazon Seller Central] の前のアカウント [ストアの統合](./store-integration.md) は読み込まれません。

インポートされたAmazonの注文は、で管理されます。 [[!DNL Commerce] 注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) 他のワークフローと同様に、 [!DNL Commerce] ストア。 のAmazon注文番号をクリックします *[!UICONTROL Order Number]* の順序を開く列 [[!DNL Commerce] 注文プロセス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). 参照： [Amazonの注文を表示](./amazon-orders-all.md).

### 注文のインポートプロセス

Amazonで注文した場合 [注文の読み込み](./order-settings.md) を有効にすると、次のプロセスが開始されます。

| 変更 | アクション |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amazonで注文が行われます。 | <ul><li>Amazonが注文ステータスを次のように設定 `Pending`.</li><li>オーダー情報の送信先 [!DNL Commerce].</li><li>注文の追加先： [_Amazonの注文_ テーブル](./amazon-orders-all.md) （を使用） `Pending` ステータス。</li></ul> |
| Amazonが注文ステータスを「」に変更します。 `Unshipped`. | <ul><li>ステータスの変更はに送信されます [!DNL Commerce].</li><li>が含まれる [_Amazonの注文_ テーブル](./amazon-orders-all.md)注文のステータスが「」に変わります。 `Unshipped`.</li><li>が含まれる [[!DNL Commerce] 注文ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html)、対応する [!DNL Commerce] オーダーは `Processing` ステータス。</li></ul> |
| 対象： [[!DNL Commerce] 注文ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), [!DNL Commerce] 注文が処理され、ステータスが「」に変わります `Shipped`. | <ul><li>が含まれる [_Amazonの注文_ テーブル](./amazon-orders-all.md)注文のステータスが「」に変わります。 `Shipped`.</li><li>次の cron ジョブで、注文ステータスが「」に変わります。 `Complete` が含まれる [[!DNL Commerce] 注文ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### オーダー作成ブロッカー

対応するを作成できないシナリオがいくつかあります [!DNL Commerce] オーダー。 [!DNL Commerce] 次のいずれかの問題が発生した場合、受注は作成されません。

| シナリオ | 解決策 |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 項目がに存在しません [!DNL Commerce] カタログ。 | [商品の作成](./creating-assigning-catalog-products.md) が含まれる [!DNL Commerce] カタログと [手動で一致](./creating-assigning-catalog-products.md) 製品に追加されます。 |
| カタログ内の項目が無効になっています。 | 次のことを確認します [製品ステータス](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) が有効になっています。 |
| 注文した商品は在庫切れです。 | を更新または設定 [製品オプション](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) （数量およびソース）。 |

注文をインポートできない場合は、次のようなシステムメッセージが画面の上部に表示されます。

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題が解決すると、次のようになります [!DNL Commerce] 注文は次回の同期時に作成されます。

## 注文の読み込みが無効の場合

でAmazonの注文を読み込んで管理しない場合 [!DNL Commerce]を変更できます [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) をに設定しています `Disabled`. この設定は、新しい注文がAmazonから届いたら、次に対応することを意味します [!DNL Commerce] 注文は作成されません。

無効にすると、Amazonから受信した注文情報がに表示されます _[!UICONTROL Recent Orders]_ストアダッシュボードのセクションと_[!UICONTROL All Orders]_ 表示。 この注文情報は表示のみです。これらの注文は [!DNL Amazon Seller Central]. で注文の詳細を開くには [!DNL Amazon Seller Central]で、Amazonの注文番号をクリックします _[!UICONTROL Order Number]_列。

関連トピック [Amazonの注文を表示](./amazon-orders-all.md), [Amazon注文の詳細を表示](./amazon-order-details.md)、および [一般的なオーダー処理タスク](./common-order-processing.md).
