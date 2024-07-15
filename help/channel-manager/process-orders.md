---
title: 注文を処理
description: 「Adobe CommerceおよびMagento Open Sourceからの注文の発送  [!DNL Walmart Marketplace]  キャンセルの手順」
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# 注文を処理

[!DNL Walmart Marketplace] 件の注文が確認され、[!DNL Channel Manager] に正常に送信されたら、[Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) を使用して注文を処理します。

チャネルマネージャーは、[!DNL Commerce] からの注文ステータスと配送情報が [!DNL Walmart Marketplace] で追跡されたデータと一致するように、[!DNL Walmart Marketplace] への更新を同期します。

* **受注出荷**- ウォルマートでは、すべての出荷に追跡番号が必要です。 一部の品目が在庫切れの場合は、部分出荷を作成して、現在使用可能な品目を送信できます。 出荷を発行すると、受注更新が [!DNL Walmart Marketplace] に同期されます。 次に、ウォルマートは注文ステータスと配送の詳細を顧客に通知します。

* **注文キャンセル**-[!DNL Walmart Marketplace] 注文をキャンセルする場合、ウォルマートはキャンセル理由を顧客に送信される注文キャンセル通知に含める必要があります。 キャンセル理由は、[!DNL Commerce] 注支払情報にも表示されます。 キャンセルを送信すると、在庫更新が [!DNL Walmart Marketplace] に同期されます。 次に、ウォルマートは注文ステータスと配送の詳細を顧客に通知します。

  ストアフロントでは、注文全体をキャンセルする必要があります。 [!DNL Commerce] では、部分的なキャンセルは許可されていません。

* **払い戻しリクエスト** – 出荷された注文に対して Walmart Marketplace の返品がリクエストされた場合、[!UICONTROL Status details] には返品へのリンクが含まれます。 返品と返金は、[ 返品 ](return-refund-orders.md) ダッシュボードから管理されます。

Commerceのオーダーが処理され、出荷、一部出荷および [!DNL Walmart Marketplace] の取消の更新が正常に同期され [!DNL Channel Manager] と、オーダー処理は完了します。 出荷済受注に対する返品要求および払戻は、「返品 [ ダッシュボードから管理され ](return-refund-orders.md) す。

>[!NOTE]
>
> 注文の更新が [!DNL Walmart Marketplace] に同期されるまで、最大 5 分かかる場合があります。 注文ステータスを確認するには、[!DNL Channel Manager] Orders ページに戻ります。

## 注文の発送

1. 管理者から、**[!UICONTROL Marketing]**/**[!UICONTROL Channel Manager]** を選択します。

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. [!DNL Walmart Marketplace] 注文を表示するには、「**[!UICONTROL Orders]**」を選択します。

1. 「受注」テーブルで、**[!UICONTROL Commerce Order Number]** を選択して出荷対象の受注を開きます。

1. **[!UICONTROL Ship]** を選択して、オーダーの全部または一部に対する出荷を作成して発行します。

   ![[!DNL Walmart Marketplace] 注文のCommerce注文の詳細ビュー ](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * 配送業者を選択し、**[!UICONTROL Add tracking number]** を選択して追跡番号を追加します。

     ![[!DNL Walmart Marketplace] 注文のCommerce注文の詳細ビュー ](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * 必要に応じて、残りの配送フォームに入力します。 手順について詳しくは、[[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) を参照してください。

1. 出荷を送信した後、[ 注文ステータス ](manage-orders.md#about-order-status) を追跡して、更新が [!DNL Walmart Marketplace] に送信されたこ [!DNL Channel Manager] を確認します。

注文が出荷された後、[!DNL Walmart Marketplace] から受け取った返品要求に基づいて、注文に含まれる品目について、[!DNL Channel Manager] からの全額払い戻しまたは一部払い戻しを処理できます。 [ 返品および返金の注文 ](return-refund-orders.md) を参照してください。

## 注文をキャンセル

1. 管理者から、**[!UICONTROL Marketing]**/**[!UICONTROL Channel Manager]** を選択します。

1. 販売チャネルストアの目のアイコンを選択してストア表示を開きます。

1. [!DNL Walmart Marketplace] 注文を表示するには、*[!UICONTROL Orders]**を選択します。

1. 「オーダー」テーブルで、キャンセルするオーダーの **[!UICONTROL Commerce Order Number]** を選択して [ オーダー詳細ページ ](manage-orders.md#view-order-detail) を開きます。

   ![ 注文のCommerce注文詳細ビュ [!DNL Walmart Marketplace]](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. 注文をキャンセルします。

   * 注文詳細メニューから **キャンセル** を選択します。

   * [!UICONTROL Cancel Order] フォームで、**[!UICONTROL Cancellation reason]** を選択します。

   ![[!DNL Walmart Marketplace] 注文のCommerce注文の詳細ビュー ](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * 「**[!UICONTROL Cancel Order]**」を選択します。

1. キャンセルを送信した後、[ 注文ステータス ](manage-orders.md#about-order-status) を追跡して、更新が [!DNL Walmart Marketplace] に送信されたこ [!DNL Channel Manager] を確認します。

## 注文エラーの修正

エラーは、[!DNL Walmart Marketplace] からのオーダー同期処理中、または出荷、部分出荷および取消のオーダー更新処理中に発生する場合があります。

出荷、部分出荷または取消更新の同期操作が失敗した場合は、「受注の [!DNL Channel Manager]」ページに受注の _エラー_ ステータスが表示されます。 出荷情報と注文キャンセル情報が Walmart Marketplace アカウントに正確に反映されるようにするには、[!DNL Walmart Marketplace] 店舗で注文を手動で更新します。


