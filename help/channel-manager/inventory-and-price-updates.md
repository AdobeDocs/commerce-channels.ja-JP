---
title: 在庫と価格の更新
description: '''[!DNL Channel Manager] コマースストアと [!DNL Walmart Marketplace] コマース管理者からセールスチャネルの運用を管理できます。'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 30495c4e47f15c821206f7b0252b868b4e27d62d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 在庫と価格の更新

[!DNL Channel Manager] では、 [!DNL Commerce] 接続されたセールスチャネルと [!DNL Walmart Marketplace]. 同期により、製品リストは現在の在庫数と価格を反映します。

## 在庫の更新

製品在庫レベルが [!DNL Commerce], [!DNL Channel Manager] セールスチャネルと [!DNL Walmart Marketplace]. 在庫の更新がセールスチャネル全体でと同期されるまで、最大 10 分かかる場合があります。 [!DNL Walmart marketplace].

* **製品カタログの在庫数量の更新**-When [!DNL Commerce] ～による在庫数量の変化 [手動在庫数量変更](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html)、返金、キャンセル [!DNL Channel Manager] 接続されたチャネルと [!DNL Walmart Marketplace].

* **在庫数を減らして反映 [!DNL Walmart Marketplace] 注文件数**-A の後 [!DNL Walmart Marketplace] 同期順 [!DNL Channel Manager], [!DNL Channel Manager] は更新を [!DNL Commerce] 注文システム。 [!DNL Commerce] は、順序に基づいて在庫数量を調整します。 その後、更新された数量がに同期されます。 [!DNL Walmart Marketplace]. 同期操作が完了するまで、販売チャネルの一覧に異なる数量が表示され、 [!DNL Walmart].

>[!IMPORTANT]
>
> 次の後： [!DNL Walmart Marketplace] 同期順 [!DNL Channel Manager]、在庫数量と注文情報は、返金およびキャンセルに対してのみ更新されます。 [!DNL Commerce]. 注文が [!DNL Walmart marketplace]、次の変更を処理： [!DNL Commerce] 正確性を確保する [!DNL Commerce] 在庫数量と注文情報。

## 価格の更新

製品価格が [!DNL Commerce], [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace]. 価格の変更が [!DNL Walmart Marketplace] リスト。

### 公開済み製品の価格を管理

1. 次の [!UICONTROL Admin]を選択します。 **[!UICONTROL Catalog > Products]**.
1. 製品グリッドで、更新する製品を探し、「 」を選択します。 **[!UICONTROL Edit]**.
1. 必要に応じて価格を確認し、更新します。
1. **[!UICONTROL Save]** 変更。

での製品価格設定の管理に関するヘルプ [!DNL Commerce]を参照してください。 [価格の管理](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}。
