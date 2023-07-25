---
title: 注文を処理
description: '''出荷とキャンセルの指示 [!DNL Walmart Marketplace] Adobe Commerce及びMagento Open Sourceの命令」'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 注文を処理

後 [!DNL Walmart Marketplace] 注文が確認され、正常に次に送信されました： [!DNL Channel Manager]、 [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) をクリックして注文を処理します。

チャネルマネージャーは次の更新を同期します： [!DNL Walmart Marketplace] 注文ステータスと配送先情報を確実に [!DNL Commerce] は、 [!DNL Walmart Marketplace].

* **注文出荷** — ウォルマートは、すべての出荷の追跡番号を必要とします。 一部の品目が在庫切れの場合は、一部の出荷を作成して、現在使用可能な品目を送信できます。 出荷を発行した後、注文の更新は次の項目と同期されます： [!DNL Walmart Marketplace]. その後、Walmart は顧客に注文状況と配送先の詳細を通知します。

* **注文のキャンセル**- [!DNL Walmart Marketplace] 注文、ウォルマートは、お客様に送信された注文キャンセル通知に含まれるキャンセル理由を必要とします。 キャンセルの理由は、 [!DNL Commerce] 注文の支払い情報。 キャンセルを送信すると、在庫の更新内容が [!DNL Walmart Marketplace]. その後、Walmart は顧客に注文状況と配送先の詳細を通知します。

  ストアフロントでは、注文全体をキャンセルする必要があります。 [!DNL Commerce] では部分的なキャンセルは許可されません。

* **返金要求** — ウォルマート・マーケットプレイスの返品が発送済みの注文に対して要求された場合、 [!UICONTROL Status details] リターンへのリンクが含まれます。 返金と返金は、 [戻り値](return-refund-orders.md) ダッシュボード。

コマース注文が処理され、 [!DNL Channel Manager] 出荷、出荷の一部、および取り消しの更新を [!DNL Walmart Marketplace]に設定されている場合、注文処理は完了です。 発送注文の返品要求と返金は、 [戻り値](return-refund-orders.md) ダッシュボード。

>[!NOTE]
>
> 注文の更新が同期されるまで最大 5 分かかる場合があります [!DNL Walmart Marketplace]. オーダーのステータスを確認するには、 [!DNL Channel Manager] 注文ページ。

## 注文の発送

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択 **[!UICONTROL Orders]**.

1. 「受注」テーブルで、出荷する受注を選択して開きます。 **[!UICONTROL Commerce Order Number]**.

1. 「 」を選択して、注文の全部または一部に対する出荷を作成し、発行します **[!UICONTROL Ship]**.

   ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * 配送業者を選択し、次を選択してトラッキング番号を追加します： **[!UICONTROL Add tracking number]**.

     ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * 必要に応じて、残りの配送フォームに入力します。 詳しくは、 [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) を参照してください。

1. 出荷後、 [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager] 更新が次の宛先に送信されたことを確認するには： [!DNL Walmart Marketplace].

注文の出荷後、からの完全な返金または一部の返金を処理できます。 [!DNL Channel Manager] から受け取った返品リクエストに基づいて注文に含まれる項目の [!DNL Walmart Marketplace]. 詳しくは、 [返品・返金の注文](return-refund-orders.md).

## 注文のキャンセル

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択*[!UICONTROL Orders]**.

1. 「オーダー」テーブルで、 [注文の詳細ページ](manage-orders.md#view-order-detail) 選択 **[!UICONTROL Commerce Order Number]** 注文をキャンセルするために。

   ![のコマース注文の詳細ビュー[!DNL Walmart Marketplace]注文](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. オーダーをキャンセルします。

   * 選択 **キャンセル** を選択します。

   * の [!UICONTROL Cancel Order] フォームで、 **[!UICONTROL Cancellation reason]**.

   ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * 選択 **[!UICONTROL Cancel Order]**.

1. キャンセルを送信した後、 [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager] 更新が次の宛先に送信されたことを確認するには： [!DNL Walmart Marketplace].

## 注文エラーを修正

次の注文の同期プロセス中にエラーが発生する可能性があります： [!DNL Walmart Marketplace]または、出荷、一部出荷および取消のオーダー更新プロセス中。

出荷、出荷の一部、または取り消しの更新の同期操作が失敗した場合、 [!DNL Channel Manager] 注文ページには、 _エラー_ オーダーのステータス。 出荷情報と注文キャンセル情報が Walmart Marketplace アカウントに正確に反映されるようにするには、 [!DNL Walmart Marketplace] ストア。


