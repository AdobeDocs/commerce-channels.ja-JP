---
title: 配送業者のマップ
description: '一致する属性をマッピング [DNL! Commerce] 既存の製品へ [!DNL Walmart Marketplace] リストと間のデータの同期 [!DNL Channel Manager] および [!DNL Walmart].'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 配送業者のマップ

お客様の前に [注文の出荷を処理](process-orders.md#ship-an-order) （用） [!DNL Walmart Marketplace] 注文し、ウォルマートの優先配送業者を対応する配送業者にマッピングします [!DNL Commerce] これにより、配送データを次の期間にわたって同期できます。 [!DNL Walmart] および [!DNL Commerce].

優先する通信事業者にマッピングしないCommerce通信事業者には、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* 日付： [!DNL Walmart].

**前提条件**

出荷搬送をマッピングする前に、次のタスクを実行します。

1. をレビュー [オンタイム配信の配送方法と配送のベストプラクティス](https://sellerhelp.walmart.com/s/guide?article=000009473) （用） [!DNL Walmart Marketplace].

1. を確認 [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) および [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) での設定 [!DNL Commerce] を保存して、の設定が最適化されていることを確認します。 [!DNL Walmart Marketplace sales].

## 配送業者のマッピング

1. から **[!UICONTROL Listings]** または **[!UICONTROL Orders]** ページ、選択 **[!UICONTROL Channel Settings]**.

1. 日付： **[!UICONTROL Channel Settings]**&#x200B;を選択 **[!UICONTROL Shipping Carriers]**.

   ![配送業者のマッピング](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. それぞれに対して [!DNL Walmart] 優先する通信事業者の一覧から、 [!DNL Commerce] 通信事業者が使用可能な場合は、ドロップダウンから通信事業者名を選択します。

1. を選択 **[!UICONTROL Save]** をクリックして設定を適用します。

