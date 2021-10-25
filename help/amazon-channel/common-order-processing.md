---
title: 一般的な注文処理タスク
description: 対応する  [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce]  管理ツールを使用してください。
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# 一般的な注文処理タスク

[[!DNL Commerce] order processing ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank 「}、Amazon の注文を管理できます。この場合、バイヤーへの電子メールの送信、注文 (出荷) の処理、クレジット/払戻の発行、コメントの追加などが含まれます。 Amazon の注文を管理するには、amazon orders に [**取り込む**](./order-settings.md) 設定をに設定する必要があり `Enabled` ます。これは、対応する [!DNL Commerce] 注文が Amazon の注文を受信したときに作成されるようにするためです。 Amazon order 情報は、 *[!UICONTROL Recent Orders]* ストアダッシュボードのセクションに表示されます。

有効にすると、 [!DNL Commerce] amazon の注文に対応する注文が作成され、amazon の注文番号が列に表示され _[!UICONTROL Order Number]_ます。 対応する注文が作成されている場合は [!DNL Commerce] 、注文番号をクリックして、注文を [!DNL Commerce] [ 処理 ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;} ページに表示します。 注文を管理するには、他の [[!DNL Commerce]  注文処理 ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;} のようにします。

この [!DNL Commerce] 情報は、注文番号には表示されません _[!UICONTROL Recent Orders]_。 この [!DNL Commerce] 注文番号が表示されるのは、microsoft store ダッシュボードの注文番号をクリックして、 [[!DNL Commerce]  ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;} の注文を開始した場合のみです。 注文を表示すると [!DNL Commerce] 、Amazon の注文番号がセクションに表示され&#x200B;*[!UICONTROL Payment & Shipping Method]*ます。 また&#x200B;*[!UICONTROL View or Cancel Amazon Order]**[!UICONTROL View all Amazon Orders]*、注文出荷状況に応じて、およびにもオプションが表示されます。

詳しく [ は、未出荷注文 ](./cancel-unshipped-order.md) のキャンセルを参照してください。

![Amazon の注文情報が含まれています](assets/amazon-order-number-payment-info.png)

Amazon の注文を処理する場合、Amazon sales チャンネルによってその注文情報が更新され、アカウントと同期さ [!DNL Amazon Seller Central] れます。 Cron 設定によって、Amazon and Amazon sales チャンネル間の注文情報が同期される頻度を指定します。

一般的な [!DNL Commerce] [ 注文処理 ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;} タスクには、次のタスクが含まれます。

- [注文アクション ](https://docs.magento.com/user-guide/sales/order-actions.html) {target = &quot;_blank&quot;}
- [Search の注文 ](https://docs.magento.com/user-guide/sales/orders-search.html) {target = &quot;_blank&quot;}
- [命令の処理 ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;}
   - [注文の表示 ](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order) {target = &quot;_blank&quot;}
   - [命令の処理 ](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order) {target = &quot;_blank&quot;}
   - [オーダーおよびアカウント情報 ](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information) {target = &quot;_blank&quot;}
   - [Address 情報 ](https://docs.magento.com/user-guide/sales/order-processing.html#address-information) {target = &quot;_blank&quot;}
   - [支払方法 (送料) ](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method) {target = &quot;_blank&quot;}
   - [アイテムの順序を確認 ](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered) {target = &quot;_blank&quot;}
- [貸方/払戻の発行 ](https://docs.magento.com/user-guide/sales/credit-memo-create.html) {target = &quot;_blank&quot;}
- [注文の注文 ](https://docs.magento.com/user-guide/sales/shipments-create.html) {target = &quot;_blank&quot;}
- [請求書の作成 ](https://docs.magento.com/user-guide/sales/invoice-create.html) {target = &quot;_blank&quot;}
- [未出荷注文のキャンセル](./cancel-unshipped-order.md)

>[!NOTE]
>
>注文が状態の場合は `Unshipped` 、ページで Amazon の注文をキャンセルすることができ [ ](./cancel-unshipped-order.md) [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) ます。 注文が出荷されている場合は、取り消すことはできません。

[Commerce オーダーの管理 ](https://docs.magento.com/user-guide/sales/order-management.html) {target = &quot;_blank&quot;} を参照してください。
