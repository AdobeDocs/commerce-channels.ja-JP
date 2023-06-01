---
title: 一般的なAmazonの注文処理タスク
description: 対応する [!DNL Commerce] Amazonの注文で、注文アクティビティと処理を管理するために作成された注文 [!UICONTROL Commerce] 管理者。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 6d221c2c2e9a37a42e9d660aceb3c525fedc511d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# 一般的なAmazonの注文処理タスク

[コマース注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) は、購入者への電子メール送信、注文の完了（発送）、クレジット/返金の発行、コメントの追加など、Amazonの注文を管理できます。 Amazonの注文を管理するには、 [**Amazon注文のインポート**](./order-settings.md) 設定は次のように設定する必要があります： `Enabled` それに対応して [!DNL Commerce] 注文はAmazonの注文を受け取ると作成されます。 Amazonの注文情報は、 *[!UICONTROL Recent Orders]* 」セクションに表示されます。

有効な場合は、対応する [!DNL Commerce] 注文がAmazonの注文に対して作成され、Amazonの注文番号が _[!UICONTROL Order Number]_列。 次に対応する [!DNL Commerce] オーダーが作成されたら、オーダー番号をクリックして、 [コマース注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) ページ。 他の操作と同じように、順序を管理できます [[!DNL Commerce] 注文処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

この [!DNL Commerce] 注文番号が _[!UICONTROL Recent Orders]_情報。 コマースの注文番号は、ストアダッシュボードで注文番号をクリックし、次の場所で注文を開いた場合にのみ表示されます。 [コマース注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). 次を表示する場合： [!DNL Commerce] 注文時に、Amazon注文番号が&#x200B;*[!UICONTROL Payment & Shipping Method]*」セクションに入力します。 また、次のオプションも含まれます。*[!UICONTROL View or Cancel Amazon Order]*および&#x200B;*[!UICONTROL View all Amazon Orders]*（注文発送のステータスに応じて）

詳しくは、 [未発送の注文を取り消す](./cancel-unshipped-order.md).

![コマース注文でのAmazon注文情報](assets/amazon-order-number-payment-info.png){width="500"}

Amazonの注文を処理する際、Amazonのセールスチャネルは注文情報を更新し、 [!DNL Amazon Seller Central] アカウント cron 設定は、注文情報がAmazonとAmazonのセールスチャネルの間で同期される頻度を決定します。

共通コマース [注文処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) タスクには次が含まれます。

- [注文アクション](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [注文検索](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [注文を表示](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [注文およびアカウント情報](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [住所情報](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [支払い方法と発送方法](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [注文された項目のレビュー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [クレジット/返金の発行](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [注文の履行/発送](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [請求書の作成](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [未発送の注文をキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文が `Unshipped` ステータス、 [Amazonの注文を取り消す](./cancel-unshipped-order.md) の [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) ページ。 発送済の注文はキャンセルできません。

詳しくは、 [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
