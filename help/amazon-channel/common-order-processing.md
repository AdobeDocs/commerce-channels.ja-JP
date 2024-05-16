---
title: 一般的なAmazonのオーダー処理タスク
description: 対応するを使用します [!DNL Commerce] Amazon用に作成された注文注文で、での注文アクティビティと処理を管理する [!UICONTROL Commerce] 管理者。
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# 一般的なAmazonのオーダー処理タスク

[Commerceの注文処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) Amazonの注文を管理できます。例えば、購入者への電子メール送信、注文の処理（配送）、クレジットや返金の発行、コメントの追加などを管理できます。 Amazonの注文を管理するには、 [**Amazon注文のインポート**](./order-settings.md) 設定はに設定する必要があります `Enabled` 従って、対応する [!DNL Commerce] 注文は、Amazonの注文を受け取ると作成されます。 Amazonの注文情報はに表示されます *[!UICONTROL Recent Orders]* ストアダッシュボードの「」セクション。

有効な場合、に対応します [!DNL Commerce] Amazon注文に対する注文が作成され、Amazon注文番号がに表示されます _[!UICONTROL Order Number]_列。 対応する場合 [!DNL Commerce] 注文が作成されたら、注文番号をクリックして注文を開きます [Commerceの注文処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) ページ。 他のユーザーと同様に注文を管理できます [[!DNL Commerce] オーダー処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

この [!DNL Commerce] 注文番号がで表示されない _[!UICONTROL Recent Orders]_情報。 Commerce注文番号は、ストアダッシュボードで注文番号をクリックし、で注文を開いた場合にのみ表示されます [Commerceの注文処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). を表示する場合 [!DNL Commerce] 注文すると、Amazonの注文番号が&#x200B;*[!UICONTROL Payment & Shipping Method]*セクション。 また、次のオプションも含まれます&#x200B;*[!UICONTROL View or Cancel Amazon Order]*および&#x200B;*[!UICONTROL View all Amazon Orders]*（注文の出荷ステータスに応じて異なります）。

参照： [未出荷の注文のキャンセル](./cancel-unshipped-order.md).

![Commerce注文でのAmazon注文情報](assets/amazon-order-number-payment-info.png){width="500"}

Amazonの注文を処理する際に、Amazonの販売チャネルは、注文情報を更新し、ユーザーと同期します [!DNL Amazon Seller Central] アカウント。 Cron 設定によって、AmazonとAmazonのセールスチャネル間で注文情報を同期する頻度が決まります。

共通のCommerce [オーダー処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) タスクは次のとおりです。

- [注文アクション](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [オーダー検索](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [注文を処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [オーダーを表示](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [注文を処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [注文およびアカウント情報](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [住所情報](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [お支払いと配送方法](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [並べ替えられた項目を確認](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [貸方/払戻の発行](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [注文のフルフィルメント/発送](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [請求書の作成](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [未出荷の注文のキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文が `Unshipped` ステータス、次のことができます [Amazonの注文のキャンセル](./cancel-unshipped-order.md) 日 [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) ページ。 注文が出荷されている場合は、キャンセルできません。

参照： [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
