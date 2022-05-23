---
title: 注文を処理
description: 発送とキャンセルの指示 [!DNL Walmart Marketplace] Adobe CommerceとMagento Open Sourceからの注文
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 注文を処理

Adobe CommerceとMagento Open SourceOrder Management を使用して [!DNL Commerce] 店舗販売、処理 [!DNL Walmart Marketplace] 同様のワークフローを使用してコマースからの注文。

コマースで注文を処理すると、チャネルマネージャーは更新を [!DNL Walmart Marketplace]. この更新により、商品の在庫と注文ステータスが、 [!DNL Walmart Marketplace] お客様に注文状況と配送先情報を送信するようにウォルマートに通知します。

>[!NOTE]
>
> 注文の更新が同期されるまで最大 5 分かかります [!DNL Walmart Marketplace]. オーダーのステータスを確認するには、次の場所に戻ります。 [!DNL Channel Manager] 注文。

## 注文の発送

コマースから注文を出荷する場合、 [[!DNL Commerce Order Management] 出荷ワークフロー](https://docs.magento.com/user-guide/sales/order-ship.html). 注文を送信すると、更新が [!DNL Walmart Marketplace]. その後、Walmart は顧客に注文状況と配送先の詳細を通知します。

**前提条件**

発送の前に、 [チャネル配送設定と通信事業者の設定](map-shipping-carriers.md) 会う [!DNL Walmart Marketplace requirements].

### 出荷を作成して発行

を出荷する際、 [!DNL Walmart Marketplace] 注文 [!DNL Commerce]に値を入力する場合は、トラッキング番号を追加する必要があります。 顧客は、受け取った出荷通知でトラッキング番号を受け取ります。 [!DNL Walmart].

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 開く [!UICONTROL Channel Manager Marketplace Stores] ページ。

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択*[!UICONTROL *Orders]**.

1. 「受注」テーブルで、出荷する受注を選択して開きます。 **コマース注文番号**.

1. 「 」を選択して、注文の全部または一部に対する出荷を作成し、発行します **[!UICONTROL Ship]**.

   - 配送業者を選択し、トラッキング番号を追加するには、 **[!UICONTROL Add tracking number]**.

   - 必要に応じて、残りの配送フォームに入力します。 詳しくは、 [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) を参照してください。

1. 出荷後、 [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager] 更新が次の宛先に送信されたことを確認するには： [!DNL Walmart Marketplace].

## 注文のキャンセル

をキャンセルした場合 [!DNL Walmart Marketplace] 注文、ウォルマートはキャンセル理由を必要とします。 注文キャンセルがウォルマートに更新されると、キャンセル理由が顧客に送信されるキャンセル通知に含まれます。

キャンセルの理由は、 [!DNL Commerce] 注文の支払い情報。

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 開く [!UICONTROL Channel Manager Marketplace Stores] ページ。

1. 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

1. 表示する [!DNL Walmart Marketplace] 注文、選択*[!UICONTROL *Orders]**.

1. 注文テーブルで、 **コマース注文番号** 注文をキャンセルするために。

   ![ウォルマートマーケットプレイス注文のコマース注文の詳細ビュー](assets/order-detail-with-external-order-id.png)

1. オーダーをキャンセルします。

   - 選択 **キャンセル** を選択します。

   - 「オーダーをキャンセル」フォームで、 **キャンセルの理由**.

      ![ウォルマートマーケットプレイス注文のコマース注文の詳細ビュー](assets/order-detail-with-external-order-id.png)

   - 選択 **注文をキャンセル**.

1. 更新がに送信されたことを確認します。 [!DNL Walmart Marketplace] をチェックして [注文ステータス](manage-orders.md#about-order-status) in [!DNL Channel Manager].
