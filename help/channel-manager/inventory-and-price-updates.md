---
title: 在庫と価格の更新
description: 「[!DNL Channel Manager] は、在庫と価格の更新を  [!DNL Commerce]  ストアと  [!DNL Walmart Marketplace]  間で同期するので、 [!DNL Commerce]  管理者」から販売チャネルの運用を管理できます」
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 在庫と価格の更新

[!DNL Channel Manager] は、[!DNL Commerce] 製品カタログ内の製品の在庫と価格を追跡し、接続された販売チャネルと [!DNL Walmart Marketplace] ータの更新を同期します。 同期操作により、製品リストに現在の在庫数と価格が反映されるようになります。


>[!IMPORTANT]
>
>[!DNL Channel Manager] のインストールと設定が完了すると、すべての在庫、価格、注文の更新が自動的に同期されます。 すでに Walmart Marketplace で販売している場合は、製品と注文データを更新するその他の統合を必ず無効にしてください。 次に、ライブマーケットプレイスのストアに接続する前に、[!DNL Commerce] ストアフロントの在庫在庫レベルと価格が正確で、[!DNL Walmart Marketplace] のデータと一致 [!DNL Channel Manager] ていることを確認します。


## インベントリの更新

[!DNL Commerce] で製品インベントリレベルが変更されると、[!DNL Channel Manager] 同期が [!DNL Walmart Marketplace] に更新されます。 在庫の更新がセールスチャネル全体から [!DNL Walmart marketplace] に同期されるまでに、最大 10 分かかる場合があります。

* **製品カタログ内の在庫数の更新** - [ 手動による在庫数の変更 ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html)、払い戻しまたはキャンセルによって在庫数が変 [!DNL Commerce] した場合、[!DNL Channel Manager] は接続されたチャネルと [!DNL Walmart Marketplace] に変更を同期します。

* **在庫数量を減らして [!DNL Walmart Marketplace] 注文を反映** - [!DNL Walmart Marketplace] 注文が [!DNL Channel Manager] に同期された後、[!DNL Channel Manager] は更新を [!DNL Commerce] 注文システムに送信します。 注文 [!DNL Commerce] 基づいて在庫数を調整します。 その後、更新された数量が [!DNL Walmart Marketplace] に同期されます。 同期処理が完了するまで、販売チャネルの一覧と [!DNL Walmart] に異なる数量が表示される場合があります。

>[!IMPORTANT]
>
>[!DNL Walmart Marketplace] 注が [!DNL Channel Manager] に同期された後、在庫数量と注文情報は、[!DNL Commerce] から開始された払戻とキャンセルに対してのみ更新されます。 注文が [!DNL Walmart marketplace] から返金またはキャンセルされた場合は、在庫数量と注文情報の正確性を確保するために、[!DNL Commerce] からの変更 [!DNL Commerce] 処理します。

## 価格アップデート

[!DNL Commerce] で製品価格が変更されると、[!DNL Channel Manager] は更新を [!DNL Walmart Marketplace] に同期します。 価格の変更が [!DNL Walmart Marketplace] リストに表示されるまで、最大 5 分かかる場合があります。

### 接続された製品の価格の管理

1. [!UICONTROL Admin] から「**[!UICONTROL Catalog > Products]**」を選択します。
1. 製品グリッドで、更新する製品を見つけて選択 **[!UICONTROL Edit]** ます。
1. 必要に応じて価格を確認して更新します。
1. 変更を **[!UICONTROL Save]** きます。

[!DNL Commerce] での製品価格設定の管理については、[ 価格の管理 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html) を参照してください。
