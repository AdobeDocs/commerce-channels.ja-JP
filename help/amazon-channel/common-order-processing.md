---
title: 一般的なAmazonのオーダー処理タスク
description: Amazon注文に対して作成された対応する注文を使用して  [!DNL Commerce] [!UICONTROL Commerce] Admin で注文アクティビティと処理を管理します。
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 一般的なAmazonのオーダー処理タスク

[Commerce注文処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) は、購入者への電子メール送信、注文の処理（配送）、クレジット/返金の発行、コメントの追加など、Amazonの注文を管理できます。 Amazonの注文を管理するには、「Amazon注文を読み込み [****](./order-settings.md) 設定を `Enabled` に設定し、Amazonの注文を受け取ったときに対応する [!DNL Commerce] 注文が作成されるようにする必要があります。 Amazonの注文情報は、ストアダッシュボードの「*[!UICONTROL Recent Orders]*」セクションに表示されます。

有効にすると、対応する [!DNL Commerce] 注文がAmazon注文に対して作成され、Amazon注文番号が _[!UICONTROL Order Number]_列に表示されます。 対応する [!DNL Commerce] 注文が作成されている場合は、注文番号をクリックして、[Commerce注文処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) ページで注文を開きます。 他の [[!DNL Commerce]  注文処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) と同様に、注文を管理できます。

_[!UICONTROL Recent Orders]_の情報では、[!DNL Commerce] 注番号は表示されません。 Commerceの注文番号は、ストアダッシュボードで注文番号をクリックし、[Commerceの注文処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) で注文を開いた場合にのみ表示されます。 [!DNL Commerce] 注を表示すると、「*[!UICONTROL Payment & Shipping Method]*」セクションにAmazon注文番号が表示されます。 また、注文の出荷ステータスに応じて、*[!UICONTROL View or Cancel Amazon Order]*と&#x200B;*[!UICONTROL View all Amazon Orders]*のオプションも含まれます。

[ 未出荷の受注の取消 ](./cancel-unshipped-order.md) を参照してください。

![Amazonオーダー情報（Commerceオーダー内） ](assets/amazon-order-number-payment-info.png){width="500"}

Amazonの注文を処理すると、Amazonのセールスチャネルが更新し、注文情報を [!DNL Amazon Seller Central] アカウントと同期します。 Cron 設定によって、AmazonとAmazonのセールスチャネル間で注文情報を同期する頻度が決まります。

一般的なCommerce[ 注文処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) タスクは次のとおりです。

- [ 注文操作 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [ オーダー検索 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [ 注文の処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [ 注文を表示 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [ 注文の処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [ 注文及び口座情報 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [ 住所情報 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [ お支払いおよび配送方法 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [ 並べ替えられた項目を確認 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [ 信用の供与等 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [ 注文のフルフィルメント/発送 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [ 請求書の作成 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [未出荷の注文のキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文のステータスが `Unshipped` の場合は、[[!UICONTROL Amazon Order Details]](./amazon-order-details.md) のページで [Amazonの注文をキャンセル ](./cancel-unshipped-order.md) できます。 注文が出荷されている場合は、キャンセルできません。

[Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations) を参照してください。
