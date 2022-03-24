---
title: 在庫と価格の更新
description: '"[!DNL Channel Manager] コマースストアと [!DNL Walmart Marketplace] コマース管理者からセールスチャネルの運営を管理できます」'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---


# 在庫と価格の更新

Channel Manager は、公開された製品の在庫と価格を追跡し、Channel Manager と Walmart Marketplace の変更を同期して、製品リストの現在の在庫数と価格を反映します。**

## 在庫の更新

在庫レベルが変更されると、Channel Manager は、Commerce 製品カタログと Walmart Marketplace の間で更新を同期し、Channel Manager と Walmart Marketplace の両方で現在の在庫数を表示します。

在庫の変更が Channel Manager および Walmart Marketplace に表示されるまでに最大 5 分かかる場合があります。

* **製品カタログの在庫数量の更新**- [手動在庫数量変更](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) または注文の返金やキャンセルを行う場合、Channel Manager は、接続された販売チャネルと [!DNL Walmart Marketplace].

* **在庫数を減らして、Walmart Marketplace の注文を反映**-Walmart Marketplace の注文が Channel Manager に同期されると、Channel Manager は Commerce の注文システムに更新を送信します。 コマースは、順序に基づいて在庫数量を調整します。 その後、更新された数量がウォルマート・マーケットプレイスに同期されます。 は、同期操作が完了するまで、チャネルマネージャーと Marketplace に表示される在庫数に多少の違いがある場合があります。

>[!IMPORTANT]
>
> Walmart Marketplace の注文が Channel Manager に同期されると、Commerce から開始された返金およびキャンセルに対してのみ、在庫数量およびその他の注文処理情報が更新されます。 Walmart Marketplace から注文が払い戻されたか、取り消された場合は、Commerce からの変更を処理して、Commerce の在庫数量と注文情報が正確であることを確認します。

## 価格の更新

Commerce で製品価格が変更されると、Channel Manager は Commerce 製品カタログから Walmart Marketplace に更新を同期します。 在庫の変更が表示されるまでに最大 5 分かかる場合があります。

### 公開済み製品の価格を管理

1. 次の [!UICONTROL Admin]を選択します。 **[!UICONTROL Catalog > Products]**.
1. 製品グリッドで、更新する製品を探し、「 」を選択します。 **[!UICONTROL Edit]**.
1. 必要に応じて価格を確認し、更新します。
1. **[!UICONTROL Save]** 変更。

Channel Manager は、チャネルストアに対する価格の更新を同期し、 [!DNL Walmart Marketplace]. この操作には最大 5 分かかる場合があります。

Commerce での製品価格設定の管理について詳しくは、 [価格の管理](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
