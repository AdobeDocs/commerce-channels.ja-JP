---
title: 在庫と価格の更新
description: '[!DNL Channel Manager] 間で在庫と価格の更新を同期します [!DNL Commerce] 格納と [!DNL Walmart Marketplace] そのため、から販売チャネルの運用を管理できます。 [!DNL Commerce] 管理者'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 在庫と価格の更新

[!DNL Channel Manager] で製品の在庫と価格をトラッキングします。 [!DNL Commerce] 製品カタログを作成し、接続された販売チャネルに対して更新を同期 [!DNL Walmart Marketplace]. 同期操作により、製品リストに現在の在庫数と価格が反映されるようになります。


>[!IMPORTANT]
>
>後 [!DNL Channel Manager] はインストールおよび設定され、すべての在庫、価格、注文の更新は自動的に同期されます。 すでに Walmart Marketplace で販売している場合は、製品と注文データを更新するその他の統合を必ず無効にしてください。 次に、で在庫在庫レベルと価格を確認します [!DNL Commerce] ストアフロントは正確で、のデータと一致します [!DNL Walmart Marketplace] 接続する前に [!DNL Channel Manager] ライブマーケットプレイスのストアに移動します。


## インベントリの更新

で製品在庫レベルが変更された場合 [!DNL Commerce], [!DNL Channel Manager] 更新をに同期します [!DNL Walmart Marketplace]. 在庫更新がセールスチャネル全体から次のチャネルに同期されるまでに、最大 10 分かかる場合があります [!DNL Walmart marketplace].

* **製品カタログの在庫数量のアップデート** – 条件 [!DNL Commerce] 次の理由で在庫数が変更されました [手動在庫数量の変更](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html)、払戻しまたは取消 [!DNL Channel Manager] 接続されたチャネルに変更を同期し、 [!DNL Walmart Marketplace].

* **反映する在庫数を減らす [!DNL Walmart Marketplace] 注文件数** – 後 [!DNL Walmart Marketplace] 同期を次の順序にする [!DNL Channel Manager], [!DNL Channel Manager] 更新内容をに送信します [!DNL Commerce] 注文システム。 [!DNL Commerce] 注文に基づいて在庫数を調整します。 その後、更新された数量がに同期されます。 [!DNL Walmart Marketplace]. 同期処理が完了するまで、販売チャネルの一覧および一覧には異なる数量が表示される場合があります。 [!DNL Walmart].

>[!IMPORTANT]
>
>後 [!DNL Walmart Marketplace] 同期を次の順序にする [!DNL Channel Manager]、在庫数量および受注情報は、払戻および取消が開始された場合にのみ更新されます。 [!DNL Commerce]. 注文が返金またはキャンセルされた場合 [!DNL Walmart marketplace]、からの変更を処理 [!DNL Commerce] ～の精度を確保する [!DNL Commerce] 在庫数量およびオーダー情報。

## 価格アップデート

製品価格が変更されたとき [!DNL Commerce], [!DNL Channel Manager] 更新内容をに同期します [!DNL Walmart Marketplace]. 価格の変更がに表示されるまでに最大 5 分かかる場合があります。 [!DNL Walmart Marketplace] リスト。

### 接続された製品の価格の管理

1. から [!UICONTROL Admin]を選択 **[!UICONTROL Catalog > Products]**.
1. 製品グリッドで、更新する製品を見つけて選択します。 **[!UICONTROL Edit]**.
1. 必要に応じて価格を確認して更新します。
1. **[!UICONTROL Save]** 変更。

での製品価格設定の管理に関するヘルプ [!DNL Commerce]を参照してください [価格の管理](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
