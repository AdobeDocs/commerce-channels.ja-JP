---
title: 未出荷の注文の取消
description: Amazon [!DNL Seller Central] アカウントを通じて、保留中または一部出荷済み（未出荷）の注文をキャンセルします。
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# 未出荷の注文のキャンセル

Amazonの注文は、ステータスが`Unshipped`の場合にのみキャンセルできます。 注文が保留中または一部出荷済み（未出荷）の場合、注文は[!DNL Amazon Seller Central]アカウントを通じてのみキャンセルできます。 商品が発送済みの場合は、返品や交換も[!DNL Amazon Seller Central]アカウントで処理する必要があります。

>[!NOTE]
>
>オーダーのキャンセル以外のタスクの場合：
>
>- [注文のインポート](./order-settings.md)を有効にしている場合、注文は[[!DNL Commerce] 注文ワークフロー](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}で管理されます。
>- [注文のインポート](./order-settings.md)が無効な場合は、[!DNL Amazon Seller Central]で注文を管理する必要があります。


## `Unshipped`状態の注文をキャンセル

1. ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

1. ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションで、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが表示されます。

1. ヘッダーバーの&#x200B;**[!UICONTROL Cancel Order]**&#x200B;をクリックします。

   このオプションは、`Unshipped`ステータスの注文に対してのみ表示されます。

1. **[!UICONTROL Reason for cancellation]**&#x200B;の場合は、オプションを選択します。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

   オーダーがキャンセルされ、ステータスがオーダーの詳細で`Canceled`に更新されます。

キャンセル通知が[!DNL Amazon Seller Central]アカウントに送信され、注文に関連付けられた顧客にも通知が届きます。 対応する[!DNL Commerce]の順序のステータス（ある場合）は`Complete`に変わります。
