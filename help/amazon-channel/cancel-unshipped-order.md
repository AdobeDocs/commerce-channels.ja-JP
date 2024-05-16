---
title: 未出荷のAmazon注文のキャンセル
description: Amazonから保留中または一部出荷済（未出荷）の注文をキャンセルする [!DNL Seller Central] アカウント。
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# 未出荷のAmazon注文のキャンセル

Amazonの注文は、 `Unshipped` ステータス。 注文が保留中または一部出荷（未出荷）の場合、注文はユーザーを通じてのみキャンセルできます [!DNL Amazon Seller Central] アカウント。 商品が出荷された場合、返品および交換も貴社で処理する必要があります [!DNL Amazon Seller Central] アカウント。

>[!NOTE]
>
>オーダーのキャンセル以外のタスクの場合：
>
>- 以下がある場合： [注文の読み込み](./order-settings.md) 有効化。注文はで管理されます [[!DNL Commerce] 注文ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- 次の場合 [注文の読み込み](./order-settings.md) 無効になっています。で注文を管理する必要があります [!DNL Amazon Seller Central].

## での注文をキャンセルする `Unshipped` ステータス

1. クリック **[!UICONTROL View Store]** ストアカードに。

1. が含まれる _[!UICONTROL Recent Orders]_「格納」ダッシュボードのセクションで、受注番号をクリックします。

   この _[!UICONTROL Amazon Order Details]_ページが表示されます。

1. クリック **[!UICONTROL Cancel Order]** ヘッダーバーで。

   このオプションは、の注文に対してのみ表示されます `Unshipped` ステータス。

1. の場合 **[!UICONTROL Reason for cancellation]**、オプションを選択します。

1. クリック **[!UICONTROL Confirm]**.

   注文がキャンセルされ、ステータスが「」に更新されます `Canceled` 注文の詳細で。

キャンセル通知がユーザーに送信されます [!DNL Amazon Seller Central] アカウント、および注文に関連付けられた顧客にも通知されます。 対応するのステータス [!DNL Commerce] 注文（存在する場合）の変更先 `Complete`.
