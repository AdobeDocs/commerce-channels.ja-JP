---
title: チャネルマネージャに製品を追加
description: '''次の製品の品揃えを作成： [!DNL Walmart Marketplace] 「チャネルマネージャーで設定したセールスチャネルにカタログから製品を追加する販売」'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 製品の追加先 [!DNL Channel Manager]

製品を [!DNL Walmart Marketplace] セールスチャネルで、次から選択します。 [!DNL Commerce] 製品カタログと読み込み先 [!DNL Channel Manager].
読み込み処理は、選択した製品の数に応じて、最大 30 分以上かかる場合があります。

## 前提条件

**[カタログ属性をマッピング](map-catalog-attributes.md)**— [!DNL Channel Settings] 設定、少なくとも 1 つの属性を [!DNL Commerce] 必要な Walmart Product Identifier—-GTIN, ISBN, ISSN, UPC, EAN のいずれかに製品カタログを追加します。

## リストの要件

[!DNL Commerce] 製品リストには、次の必須属性設定が必要です。

- **[!UICONTROL Connect to Channel Manager]** 属性が有効になっている

- 必要な Walmart 属性に有効な値を指定します。

   - 必要な製品属性の 1 つに一致する製品属性が少なくとも 1 つあります [!DNL Walmart Marketplace] 製品識別子 —GTIN、ISBN、ISSN、UPC、EAN。

   - 小数第 2 位までに指定された製品価格（例： ） `9.99`

   - 小数第 2 位までに指定された商品の重み付け（例： ） `1.25`

>[!TIP]
>
>セールスチャネルの最適化について詳しくは、 [Walmart Marketplace リスト品質最適化ガイド](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## 製品を追加

1. 接続されたセールスチャネルストアから、 **製品を追加** をクリックして、製品カタログを開きます。

   ![セールスチャネルストアに製品を追加](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   カタログが新しいタブで開きます。

1. カタログ製品グリッドから、販売する製品を選択します。 [!DNL Walmart Marketplace].

   ![製品をセールスチャネルストアに送信](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. を有効にします。 **[!UICONTROL Connect to Channel Manager]** 属性を設定します。

   - 送信者 **[!UICONTROL Actions]**&#x200B;を選択します。 **[!UICONTROL Update attributes]**.

   - をスクロールします。 **[!UICONTROL Connect to Channel Manager]** 属性を設定し、有効にします。

   - 製品属性に、必要な [!DNL Walmart Product IDs].

   - 選択 **[!UICONTROL Save]**.

     確認メッセージが表示されます。

     ![カタログから販売チャネルへの製品インポートの確認メッセージ](assets/product-import-from-catalog-confirmation.png){width="400"}

     更新がスケジュールされたことを示すメッセージが表示された場合は、 [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] コマンドを使用して、更新を直ちに処理できます。

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. 読み込み操作が完了したら、に戻って、追加した製品を確認します。 [!DNL Channel Manager] および選択 **[!UICONTROL Listings]**.

   最初は、製品は *ドラフト* ステータス。 選択 **[!UICONTROL Refresh products]** をクリックして、テーブルを更新します。

1. チャネルマネージャーに追加された新しい製品を表示するには、 **[!UICONTROL Draft]** ステータスカード。

   ![接続済みセールスチャネルにインポートされた製品](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


