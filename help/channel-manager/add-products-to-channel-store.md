---
title: チャネルマネージャーへの製品の追加
description: 「カタログからチャネルマネージャ  [!DNL Walmart Marketplace]  で設定された販売チャネルに製品を追加して、販売用の製品品揃えを作成します。」
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# [!DNL Channel Manager] への製品の追加

[!DNL Walmart Marketplace] 販売チャネルに製品を追加するには、製品を [!DNL Commerce] 製品カタログから選択して、[!DNL Channel Manager] に読み込みます。
選択する製品の数に応じて、読み込みプロセスに最大 30 分以上かかる場合があります。

## 前提条件

**[カタログ属性のマッピング](map-catalog-attributes.md)** - [!DNL Channel Settings] 設定では、[!DNL Commerce] 製品カタログの少なくとも 1 つの属性を、必要なウォルマート製品識別子（GTIN、ISBN、ISSN、UPC、EAN）の 1 つにマッピングします。

## 要件の一覧表示

製品リスト [!DNL Commerce] は、次の必須属性設定が必要です。

- **[!UICONTROL Connect to Channel Manager]** 属性は有効です

- 必要なウォルマート属性に有効な値を指定します。

   - 必要な [!DNL Walmart Marketplace] 製品識別子（GTIN、ISBN、ISSN、UPC、EAN）のいずれかに一致する 1 つ以上の製品属性。

   - 小数点以下 2 桁まで指定された製品価格（例：`9.99`）

   - 製品の重み付けは、小数点以下 2 桁まで指定できます。例：`1.25`

>[!TIP]
>
>販売チャネルのリストの最適化について詳しくは、[Walmart Marketplace Listing Quality Optimization Guide](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf) を参照してください。

## 製品を追加

1. 接続された販売チャネルストアから、「**製品を追加**」を選択して製品カタログを開きます。

   ![ 販売チャネルストアへの製品の追加 ](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   カタログが新しいタブで開きます。

1. カタログ製品グリッドから、[!DNL Walmart Marketplace] で販売する製品を選択します。

   ![ セールスチャネルストアへの商品の送信 ](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. 選択した項目の **[!UICONTROL Connect to Channel Manager]** 属性を有効にします。

   - 「**[!UICONTROL Actions]**」から、「**[!UICONTROL Update attributes]**」を選択します。

   - **[!UICONTROL Connect to Channel Manager]** 属性までスクロールして、有効にします。

   - 製品属性に、必要な [!DNL Walmart Product IDs] が少なくとも 1 つ含まれていることを確認します。

   - 「**[!UICONTROL Save]**」を選択します。

     確認メッセージが表示されます。

     ![ カタログから販売チャネルへの製品インポートの確認メッセージ ](assets/product-import-from-catalog-confirmation.png){width="400"}

     更新がスケジュールされていることをメッセージが示している場合は、[`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] コマンドを使用して直ちに更新を処理します。

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. 読み込み操作が完了したら、[!DNL Channel Manager] に戻って「**[!UICONTROL Listings]**」を選択し、追加した製品を確認します。

   最初、製品は *ドラフト* ステータスになります。 「**[!UICONTROL Refresh products]**」を選択すると、テーブルを更新できます。

1. チャネルマネージャーに追加された新しい製品を表示するようにビューを更新するには、**[!UICONTROL Draft]** ステータスカードを選択します。

   ![ 接続された販売チャネルにインポートされた製品 ](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


