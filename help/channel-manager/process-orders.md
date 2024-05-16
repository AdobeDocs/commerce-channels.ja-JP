---
title: 注文を処理
description: 「出荷および取消の指示」 [!DNL Walmart Marketplace] Adobe CommerceとMagento Open Sourceからの注文。
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# 注文を処理

後 [!DNL Walmart Marketplace] 注文が確認され、正常に送信されました [!DNL Channel Manager]を使用します [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) 注文を処理します。

チャネルマネージャーによる更新内容の同期先 [!DNL Walmart Marketplace] 注文ステータスと発送情報の確認元 [!DNL Commerce] で追跡されたデータと一致します [!DNL Walmart Marketplace].

* **注文の出荷** – ウォルマートには、すべての出荷に追跡番号が必要です。 一部の品目が在庫切れの場合は、部分出荷を作成して、現在使用可能な品目を送信できます。 出荷を発行すると、受注の更新は次のように同期化されます。 [!DNL Walmart Marketplace]. 次に、ウォルマートは注文ステータスと配送の詳細を顧客に通知します。

* **注文のキャンセル** – をキャンセルした場合 [!DNL Walmart Marketplace] ご注文、ウォルマートは、お客様に送信される注文キャンセル通知に含まれるキャンセル理由を必要とします。 キャンセルの理由は [!DNL Commerce] 注文支払い情報。 キャンセルを送信すると、在庫更新がに同期されます [!DNL Walmart Marketplace]. 次に、ウォルマートは注文ステータスと配送の詳細を顧客に通知します。

  ストアフロントでは、注文全体をキャンセルする必要があります。 [!DNL Commerce] 部分的なキャンセルは許可されません。

* **払戻要求** – 出荷された注文に対してウォルマート・マーケットプレイスの返品が要求された場合、 [!UICONTROL Status details] 返品へのリンクが含まれます。 返品と返金は、 [戻り値](return-refund-orders.md) ダッシュボード。

Commerceの注文が処理され、 [!DNL Channel Manager] への出荷、部分出荷および取消の更新が正常に同期されます [!DNL Walmart Marketplace]注文の処理が完了しました。 出荷済受注に対する返品要求および払戻は、次の方法で管理されます。 [戻り値](return-refund-orders.md) ダッシュボード。

>[!NOTE]
>
> 注文の更新がに同期されるまでに最大 5 分かかる場合があります [!DNL Walmart Marketplace]. 注文ステータスを確認するには、に戻ります [!DNL Channel Manager] 注文ページ。

## 注文の発送

1. 管理者から、を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. To view [!DNL Walmart Marketplace] 注文、選択 **[!UICONTROL Orders]**.

1. 「受注」テーブルで、次の項目を選択して出荷受注を開きます **[!UICONTROL Commerce Order Number]**.

1. を選択して、注文の全部または一部に対する出荷を作成および送信します。 **[!UICONTROL Ship]**.

   ![のCommerce注文詳細ビュー [!DNL Walmart Marketplace] 順序](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * 配送業者を選択し、次を選択して追跡番号を追加します： **[!UICONTROL Add tracking number]**.

     ![のCommerce注文詳細ビュー [!DNL Walmart Marketplace] 順序](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * 必要に応じて、残りの配送フォームに入力します。 参照： [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html) 詳しい手順については、を参照してください。

1. 出荷を送信した後、 [注文ステータス](manage-orders.md#about-order-status) 。対象： [!DNL Channel Manager] 更新がに送信されたことを確認するには [!DNL Walmart Marketplace].

注文が出荷された後は、全額または一部の払い戻しを処理できます。 [!DNL Channel Manager] から受領した返品要求に基づいて注文に含まれる品目 [!DNL Walmart Marketplace]. 参照： [返品および返金の注文](return-refund-orders.md).

## 注文をキャンセル

1. 管理者から、を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択してストア表示を開きます。

1. To view [!DNL Walmart Marketplace] 注文件数、選択*[!UICONTROL Orders]**。

1. [ 受注 ] テーブルで、 [注文詳細ページ](manage-orders.md#view-order-detail) を選択します。 **[!UICONTROL Commerce Order Number]** キャンセルする注文に対して。

   ![のCommerce注文詳細ビュー[!DNL Walmart Marketplace]順序](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. 注文をキャンセルします。

   * を選択 **キャンセル** 注文詳細メニューから。

   * 日 [!UICONTROL Cancel Order] フォームで、 **[!UICONTROL Cancellation reason]**.

   ![のCommerce注文詳細ビュー [!DNL Walmart Marketplace] 順序](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * を選択 **[!UICONTROL Cancel Order]**.

1. キャンセルを送信した後、 [注文ステータス](manage-orders.md#about-order-status) 。対象： [!DNL Channel Manager] 更新がに送信されたことを確認するには [!DNL Walmart Marketplace].

## 注文エラーの修正

からの注文同期プロセス中にエラーが発生する可能性があります [!DNL Walmart Marketplace]または、出荷、部分出荷および取消の受注更新プロセス中に行います。

出荷、部分出荷または取消更新の同期操作が失敗した場合は、 [!DNL Channel Manager] 注文件数ページに次が表示されます _エラー_ 注文のステータス。 出荷情報と注文キャンセル情報が Walmart Marketplace アカウントに正確に反映されるようにするには、手動で注文を更新します [!DNL Walmart Marketplace] ストア。


