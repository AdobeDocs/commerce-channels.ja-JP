---
title: 注文を処理
description: 発送とキャンセルの指示 [!DNL Walmart Marketplace] Adobe CommerceとMagento Open Sourceからの注文
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: f1c37111df2f566b9673946bb9b2b282506f990c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 注文を処理

後 [!DNL Walmart Marketplace] 注文が確認され、正常に次に送信されました： [!DNL Channel Manager]、 [Commerce Order Management](https://docs.magento.com/user-guide/sales/orders-workspace.html) をクリックして注文を処理します。

チャネルマネージャーは次の更新を同期します： [!DNL Walmart Marketplace] を使用して、Commerce からの注文ステータスと配送先情報が、 [!DNL Walmart Marketplace].

* **注文出荷** — ウォルマートは、すべての出荷の追跡番号を必要とします。 一部の品目が在庫切れの場合は、一部の出荷を作成して、現在使用可能な品目を送信できます。 出荷を発行した後、注文の更新は次の項目と同期されます： [!DNL Walmart Marketplace]. その後、Walmart は顧客に注文状況と配送先の詳細を通知します。

* **注文のキャンセル**- [!DNL Walmart Marketplace] 注文、ウォルマートは、お客様に送信された注文キャンセル通知に含まれるキャンセル理由を必要とします。 キャンセルの理由は、 [!DNL Commerce] 注文の支払い情報。

>[!NOTE]
>
> 注文の更新を同期するには、最大 5 分かかります。 [!DNL Walmart Marketplace]. オーダーのステータスを確認するには、 [!DNL Channel Manager] 注文ページ。

## 注文の発送

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択*[!UICONTROL *Orders]**.

1. 「受注」テーブルで、出荷する受注を選択して開きます。 **コマース注文番号**.

1. 「 」を選択して、注文の全部または一部に対する出荷を作成し、発行します **[!UICONTROL Ship]**.

   ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-detail-with-external-order-id.png)

   * 配送業者を選択し、次を選択してトラッキング番号を追加します： **[!UICONTROL Add tracking number]**.

      ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-shipment-add-tracking-number.png)


   * 必要に応じて、残りの配送フォームに入力します。 詳しくは、 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) を参照してください。

1. 出荷後、 [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager] 更新が次の宛先に送信されたことを確認するには： [!DNL Walmart Marketplace].

## 注文のキャンセル

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択*[!UICONTROL *Orders]**.

1. 注文テーブルで、 **コマース注文番号** 注文をキャンセルするために。

   ![のコマース注文の詳細ビュー[!DNL Walmart Marketplace]注文](assets/order-detail-with-external-order-id.png)

1. オーダーをキャンセルします。

   * 選択 **キャンセル** を選択します。

   * の [!UICONTROL Cancel Order] フォームで、 **キャンセルの理由**.
   ![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/cancel-order-reason-selector.png)

   * 選択 **注文をキャンセル**.


1. キャンセルを送信した後、 [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager] 更新が次の宛先に送信されたことを確認するには： [!DNL Walmart Marketplace].