---
title: 未発送の注文の取消
description: Amazonを通じて保留中または一部出荷済み（未出荷）の注文をキャンセル [!DNL Seller Central] アカウント
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# 未発送の注文の取消

Amazonの注文は、キャンセルできるのは、 `Unshipped` ステータス。 注文が保留中または一部出荷済（未出荷）の場合、注文はお客様の [!DNL Amazon Seller Central] アカウント 商品が発送済みの場合は、返品や交換もお客様で処理する必要があります [!DNL Amazon Seller Central] アカウント。

>[!NOTE]
>
>オーダーのキャンセル以外のタスクの場合：
>
>- 次の場合： [注文インポート](./order-settings.md) 有効、注文は [[!DNL Commerce] オーダーワークフロー](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.
>- If [注文インポート](./order-settings.md) が無効の場合は、 [!DNL Amazon Seller Central].


## 注文をキャンセル `Unshipped` ステータス

1. クリック **[!UICONTROL View Store]** をストアカードに貼り付けます。

1. 内 _[!UICONTROL Recent Orders]_「 」セクションで、注文番号をクリックします。

   この _[!UICONTROL Amazon Order Details]_ページが表示されます。

1. クリック **[!UICONTROL Cancel Order]** をクリックします。

   このオプションは、 `Unshipped` ステータス。

1. の場合 **[!UICONTROL Reason for cancellation]**、「 」オプションを選択します。

1. クリック **[!UICONTROL Confirm]**.

   オーダーがキャンセルされ、ステータスがに更新されます。 `Canceled` 注文の詳細。

キャンセル通知が [!DNL Amazon Seller Central] アカウント、および注文に関連付けられた顧客にも通知が送信されます。 対応する [!DNL Commerce] 注文（ある場合）、変更 `Complete`.
