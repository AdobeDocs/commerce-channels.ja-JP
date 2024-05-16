---
title: チャネルマネージャーへの製品の追加
description: '''製品品揃えを作成します [!DNL Walmart Marketplace] カタログの製品をチャネルマネージャーで設定された販売チャネルに追加して販売を行う。'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# 製品の追加先 [!DNL Channel Manager]

に商品を追加するには [!DNL Walmart Marketplace] 販売チャネル、から選択 [!DNL Commerce] 製品カタログとを読み込みます [!DNL Channel Manager].
選択する製品の数に応じて、読み込みプロセスに最大 30 分以上かかる場合があります。

## 前提条件

**[カタログ属性のマッピング](map-catalog-attributes.md)** – の場合 [!DNL Channel Settings] 設定する。少なくとも 1 つの属性をからマッピングします [!DNL Commerce] 製品カタログ：GTIN、ISBN、ISSN、UPC、EAN。

## 要件の一覧表示

[!DNL Commerce] 製品リストには、次の必須属性設定が必要です。

- **[!UICONTROL Connect to Channel Manager]** 属性は有効です

- 必要なウォルマート属性に有効な値を指定します。

   - 必須フィールドのいずれかに一致する製品属性が 1 つ以上 [!DNL Walmart Marketplace] 製品識別子（GTIN、ISBN、ISSN、UPC、EAN）

   - 製品価格は小数点以下 2 桁まで指定されます。例： `9.99`

   - 製品の重み付けは、小数点以下 2 桁まで指定できます。例： `1.25`

>[!TIP]
>
>販売チャネルの一覧を最適化する方法の詳細については、 [Walmart Marketplace リスト品質最適化ガイド](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## 製品を追加

1. 接続されているセールス・チャネル・ストアから、 **製品を追加** 製品カタログを開きます。

   ![販売チャネル ストアに製品を追加する](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   カタログが新しいタブで開きます。

1. カタログの製品グリッドから、販売する製品を選択します [!DNL Walmart Marketplace].

   ![販売チャネル ストアに商品を送信します](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. を有効にする **[!UICONTROL Connect to Channel Manager]** 選択した項目の属性。

   - 送信元 **[!UICONTROL Actions]**&#x200B;を選択 **[!UICONTROL Update attributes]**.

   - スクロール先： **[!UICONTROL Connect to Channel Manager]** 属性を設定して有効にします。

   - 製品属性に、必要な属性が少なくとも 1 つ含まれていることを確認します [!DNL Walmart Product IDs].

   - を選択 **[!UICONTROL Save]**.

     確認メッセージが表示されます。

     ![カタログから販売チャネルへの商品インポートの確認メッセージ](assets/product-import-from-catalog-confirmation.png){width="400"}

     更新がスケジュールされていることをメッセージが示している場合は、 [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] 更新を直ちに処理するコマンド。

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. 読み込み操作が完了したら、に戻って、追加した製品を確認します。 [!DNL Channel Manager] および選択 **[!UICONTROL Listings]**.

   最初、製品は次の場所にあります。 *ドラフト* ステータス。 を選択 **[!UICONTROL Refresh products]** をクリックしてテーブルを更新します。

1. チャネルマネージャーに追加された新製品を表示するようにビューを更新するには、 **[!UICONTROL Draft]** ステータスカード。

   ![接続された販売チャネルに読み込まれた製品](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


