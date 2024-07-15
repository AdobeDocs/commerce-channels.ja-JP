---
title: 未出荷のAmazon注文のキャンセル
description: Amazon アカウントを通じて、保留中または一部出荷済（未出荷）の注文  [!DNL Seller Central]  キャンセルします。
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# 未出荷のAmazon注文のキャンセル

Amazonの注文は、`Unshipped` ステータスの場合にのみキャンセルできます。 注文が保留中または一部出荷済（未出荷）の場合、注文は [!DNL Amazon Seller Central] アカウントを通じてのみキャンセルできます。 商品が発送された場合、返品と交換は [!DNL Amazon Seller Central] アカウントでも処理する必要があります。

>[!NOTE]
>
>オーダーのキャンセル以外のタスクの場合：
>
>- [ 注文のインポート ](./order-settings.md) を有効にしている場合、注文は [[!DNL Commerce]  注文ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) で管理されます。
>- [ 注文の読み込み ](./order-settings.md) が無効になっている場合は、[!DNL Amazon Seller Central] で注文を管理する必要があります。

## 注文ステータスのキャンセ `Unshipped`

1. ストアカードの **[!UICONTROL View Store]** をクリックします。

1. ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションで、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが表示されます。

1. ヘッダーバーの「**[!UICONTROL Cancel Order]**」をクリックします。

   このオプションは、`Unshipped` ステータスの注文に対してのみ表示されます。

1. **[!UICONTROL Reason for cancellation]** の場合は、オプションを選択します。

1. 「**[!UICONTROL Confirm]**」をクリックします。

   注文がキャンセルされ、ステータスが注文の詳細の `Canceled` に更新されます。

キャンセル通知が [!DNL Amazon Seller Central] アカウントに送信され、注文に関連付けられたお客様にも通知が送信されます。 対応する [!DNL Commerce] 注文がある場合は、そのステータスが `Complete` に変わります。
