---
title: 在庫と価格の更新
description: '''[!DNL Channel Manager] コマースストアと [!DNL Walmart Marketplace] コマース管理者からセールスチャネルの運用を管理できます。'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 在庫と価格の更新

[!DNL Channel Manager] チャネルストア内の製品の在庫と価格を追跡します。 在庫または価格が変更されると、更新が両方に同期 [!DNL Channel Manager] および [!DNL Walmart Marketplace] 製品リストに現在の在庫数と価格を反映させる。

## 在庫の更新

在庫レベルが変更されると、Channel Manager は、Commerce と Walmart Marketplace の間で更新を同期し、チャネルマネージャーと Walmart Marketplace の在庫数が正しいことを確認します。

インベントリの更新が Channel Manager とマーケットプレイスをまたいで同期されるまで、最大 10 分かかる場合があります。

* **製品カタログの在庫数量の更新**- [手動在庫数量変更](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html)、返金、またはキャンセルを行うと、Channel Manager は、接続されたチャネルと [!DNL Walmart Marketplace].

* **在庫数を減らして、Walmart Marketplace の注文を反映**-Walmart Marketplace の注文が Channel Manager に同期されると、Channel Manager は Commerce の注文システムに更新を送信します。 コマースは、順序に基づいて在庫数量を調整します。 その後、更新された数量がウォルマート・マーケットプレイスに同期されます。 同期操作が完了するまで、チャネルマネージャーと Marketplace の間で数量の違いが生じる場合があります。

>[!IMPORTANT]
>
> Walmart Marketplace の注文が Channel Manager に同期されると、Commerce から開始された返金およびキャンセルに対してのみ、在庫数量と注文情報が更新されます。 Walmart Marketplace から注文が払い戻されたか取り消された場合は、Commerce からの変更を処理して、Commerce の在庫数量と注文情報の正確性を確保します。

## 価格の更新

コマースで製品価格が変更されると、チャネルマネージャーは、 [!DNL Commerce] 製品カタログ [!DNL Walmart Marketplace]. 市場に価格の変更が表示されるまでに最大 5 分かかる場合があります。

### 公開済み製品の価格を管理

1. 次の [!UICONTROL Admin]を選択します。 **[!UICONTROL Catalog > Products]**.
1. 製品グリッドで、更新する製品を探し、「 」を選択します。 **[!UICONTROL Edit]**.
1. 必要に応じて価格を確認し、更新します。
1. **[!UICONTROL Save]** 変更。

Commerce での製品価格設定の管理について詳しくは、 [価格の管理](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
