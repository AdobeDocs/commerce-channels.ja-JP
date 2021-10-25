---
title: 未出荷注文のキャンセル
description: Amazon アカウントを使用して、ペンディング状態または一部出荷されている (未出荷) 注文をキャンセル  [!DNL Seller Central]  します。
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# 未出荷注文のキャンセル

Amazon の注文は、ステータスがある場合にのみキャンセルでき `Unshipped` ます。 注文が保留中の場合、または一部が出荷されていない場合は、注文が解約されるのはお客様のアカウントに限られ [!DNL Amazon Seller Central] ます。 品目が出荷されている場合は、返品および為替も、取引先企業で処理する必要があり [!DNL Amazon Seller Central] ます。

>[!NOTE]
>
>注文のキャンセル以外のタスクについては、次の手順に従います。
>
>- 注文のインポートが有効になっている場合は [ ](./order-settings.md) 、注文は、「orders」のワークフローで管理され [[!DNL Commerce]  ](https://docs.magento.com/user-guide/sales/orders.html) ます {target = &quot;_blank&quot;}。
>- [「注文のインポート」 ](./order-settings.md) が無効化されている場合は、で注文を管理する必要があり [!DNL Amazon Seller Central] ます。


## 注文状態のキャンセル `Unshipped`

1. **[!UICONTROL View Store]** Store カードをクリックします。

1. _[!UICONTROL Recent Orders]_ストアダッシュボードのセクションで、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが表示されます。

1. **[!UICONTROL Cancel Order]**&#x200B;ヘッダーバーをクリックします。

   このオプションは、注文状態の場合にのみ表示され `Unshipped` ます。

1. **[!UICONTROL Reason for cancellation]**&#x200B;では、オプションを選択します。

1. をクリックし **[!UICONTROL Confirm]** ます。

   注文がキャンセルされ、ステータスが `Canceled` 注文明細に更新されます。

キャンセル通知がアカウントに送信され、 [!DNL Amazon Seller Central] 注文に関連付けられた顧客にも通知されます。 対応する注文のステータスがある場合は、によって [!DNL Commerce] に変更され `Complete` ます。
