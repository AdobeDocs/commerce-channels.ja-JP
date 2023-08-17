---
title: 配送業者をマップ
description: '''一致する属性をマッピング [DNL! コマース ] 製品を既存の製品に [!DNL Walmart Marketplace] のリストと同期，データを [!DNL Channel Manager] および [!DNL Walmart].`'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 配送業者をマップ

事前準備 [オーダー出荷の処理](process-orders.md#ship-an-order) 対象： [!DNL Walmart Marketplace] 注文、ウォルマートの優先配送業者を、 [!DNL Commerce] これにより、配送先のデータを次の間で同期させることができます。 [!DNL Walmart] および [!DNL Commerce].

優先通信事業者にマッピングされていない通信事業者は、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* オン [!DNL Walmart].

**前提条件**

輸送業者をマッピングする前に、次のタスクを実行します。

1. 以下を確認します。 [通信事業者の方法と配送に関するベストプラクティス](https://sellerhelp.walmart.com/s/guide?article=000009473) 対象： [!DNL Walmart Marketplace].

1. を確認します。 [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) および [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) の設定 [!DNL Commerce] を保存して、次の設定を最適化しました。 [!DNL Walmart Marketplace sales].

## 配送業者をマップ

1. 次から： **[!UICONTROL Listings]** または **[!UICONTROL Orders]** ページ、選択 **[!UICONTROL Channel Settings]**.

1. オン **[!UICONTROL Channel Settings]**&#x200B;を選択します。 **[!UICONTROL Shipping Carriers]**.

   ![配送業者をマップ](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. 次ごとに [!DNL Walmart] リストに表示された優先通信事業者、 [!DNL Commerce] 通信事業者が使用可能な場合は、ドロップダウンから通信事業者名を選択します。

1. 選択 **[!UICONTROL Save]** をクリックして設定を適用します。

