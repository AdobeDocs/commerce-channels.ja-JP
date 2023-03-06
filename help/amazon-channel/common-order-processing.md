---
title: 一般的な注文処理タスク
description: 対応する [!DNL Commerce] Amazonの注文で、注文アクティビティと処理を管理するために作成された注文 [!UICONTROL Commerce] 管理者。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# 一般的な注文処理タスク

[[!DNL Commerce] 注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} は、購入者への電子メール送信、注文の完了（発送）、クレジット/返金の発行、コメントの追加など、Amazonの注文を管理できます。 Amazonの注文を管理するには、 [**Amazon注文のインポート**](./order-settings.md) 設定は次のように設定する必要があります： `Enabled` それに対応して [!DNL Commerce] 注文はAmazonの注文を受け取ると作成されます。 Amazonの注文情報は、 *[!UICONTROL Recent Orders]* 」セクションに表示されます。

有効な場合は、対応する [!DNL Commerce] 注文がAmazonの注文に対して作成され、Amazonの注文番号が _[!UICONTROL Order Number]_列。 次に対応する [!DNL Commerce] オーダーが作成されたら、オーダー番号をクリックして、 [!DNL Commerce] [注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} page. You can manage the order as you do your other [[!DNL Commerce] order processing](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

この [!DNL Commerce] 注文番号が _[!UICONTROL Recent Orders]_情報。 この [!DNL Commerce] 注文番号は、ストアダッシュボードで注文番号をクリックし、 [[!DNL Commerce] 注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}. 次を表示する場合： [!DNL Commerce] 注文時に、Amazon注文番号が&#x200B;*[!UICONTROL Payment & Shipping Method]*」セクションに入力します。 また、次のオプションも含まれます。*[!UICONTROL View or Cancel Amazon Order]*および&#x200B;*[!UICONTROL View all Amazon Orders]*（注文発送のステータスに応じて）

詳しくは、 [未発送の注文を取り消す](./cancel-unshipped-order.md).

![コマース注文でのAmazon注文情報](assets/amazon-order-number-payment-info.png)

Amazonの注文を処理する際、Amazonのセールスチャネルは注文情報を更新し、 [!DNL Amazon Seller Central] アカウント cron 設定は、注文情報がAmazonとAmazonのセールスチャネルの間で同期される頻度を決定します。

共通 [!DNL Commerce] [注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"} タスクには次が含まれます。

- [注文アクション](https://docs.magento.com/user-guide/sales/order-actions.html){target="_blank"}
- [注文検索](https://docs.magento.com/user-guide/sales/orders-search.html){target="_blank"}
- [注文の処理](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}
   - [注文を表示](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target="_blank"}
   - [注文の処理](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target="_blank"}
   - [注文およびアカウント情報](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target="_blank"}
   - [住所情報](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target="_blank"}
   - [支払い方法と発送方法](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target="_blank"}
   - [注文された項目のレビュー](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target="_blank"}
- [クレジット/返金の発行](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target="_blank"}
- [注文の履行/発送](https://docs.magento.com/user-guide/sales/shipments-create.html){target="_blank"}
- [請求書の作成](https://docs.magento.com/user-guide/sales/invoice-create.html){target="_blank"}
- [未発送の注文をキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文が `Unshipped` ステータス、 [Amazonの注文を取り消す](./cancel-unshipped-order.md) の [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) ページ。 発送済の注文はキャンセルできません。

詳しくは、 [Commerce Order Management](https://docs.magento.com/user-guide/sales/order-management.html){target="_blank"}.
