---
title: 一般的な注文処理タスク
description: 対応する [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] 管理者を使用します。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# 一般的な注文処理タスク

[[!DNL Commerce] 注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}は、購入者への電子メール送信、注文（発送）の完了、クレジット/返金の発行、コメントの追加など、Amazonの注文を管理できます。Amazonの注文を管理するには、Amazonの注文を受け取ったときに対応する[!DNL Commerce]注文が作成されるように、「[**Amazonの注文をインポート**](./order-settings.md)」設定を`Enabled`に設定する必要があります。 Amazonの注文情報は、ストアダッシュボードの&#x200B;*[!UICONTROL Recent Orders]*&#x200B;セクションに表示されます。

有効にすると、対応する[!DNL Commerce]注文がAmazonの注文に対して作成され、Amazonの注文番号が&#x200B;_[!UICONTROL Order Number]_列に表示されます。 対応する[!DNL Commerce]の順序が作成された場合は、順序番号をクリックして、[!DNL Commerce] [順序処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}ページで順序を開きます。 他の[[!DNL Commerce] 注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}と同じように、順序を管理できます。

[!DNL Commerce]の注文番号は&#x200B;_[!UICONTROL Recent Orders]_情報と共に表示されません。 [!DNL Commerce]の注文番号は、ストアダッシュボードで注文番号をクリックし、[[!DNL Commerce] 注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}で注文を開いた場合にのみ表示されます。 [!DNL Commerce]順序を表示すると、*[!UICONTROL Payment & Shipping Method]*セクションにAmazonの注文番号が表示されます。 また、注文発送状況に応じて、*[!UICONTROL View or Cancel Amazon Order]*と&#x200B;*[!UICONTROL View all Amazon Orders]*のオプションも含まれます。

[未出荷の注文のキャンセル](./cancel-unshipped-order.md)を参照してください。

![Amazon Commerce注文の注文情報](assets/amazon-order-number-payment-info.png)

Amazonの注文を処理する際、Amazonの販売チャネルは注文情報を更新し、[!DNL Amazon Seller Central]アカウントと同期します。 Cron設定は、注文情報がAmazonとAmazonの販売チャネルの間で同期される頻度を決定します。

一般的な[!DNL Commerce] [注文処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}タスクは次のとおりです。

- [アクションの並べ替え](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [注文の検索](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [注文の処理](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [注文の表示](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [注文の処理](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [注文およびアカウント情報](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [アドレス情報](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [支払いおよび配送方法](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [順序付けされた項目を確認します](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [クレジット/返金の発行](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [注文{target=&quot;_blank&quot;](https://docs.magento.com/user-guide/sales/shipments-create.html)}を実行/発送中
- [請求書の作成](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [未出荷の注文のキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文が`Unshipped`ステータスの場合は、[[!UICONTROL Amazon Order Details]](./amazon-order-details.md)ページでAmazonの注文](./cancel-unshipped-order.md)を[キャンセルできます。 発送済の注文はキャンセルできません。

[Commerce Order Management](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}を参照してください。
