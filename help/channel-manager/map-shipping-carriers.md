---
title: 輸送業者をマップ
description: 一致する属性をマッピング [DNL! コマース ] 製品を既存の製品に [!DNL Walmart Marketplace] リストと同期，データ間 [!DNL Channel Manager] および [!DNL Walmart].
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# 輸送業者をマップ

事前準備 [オーダー出荷の処理](process-orders.md#ship-an-order) 対象 [!DNL Walmart Marketplace] 注文、ウォルマートの優先配送業者を、 [!DNL Commerce] これにより、輸送データを [!DNL Walmart] および [!DNL Commerce].

優先通信事業者にマッピングされていない通信事業者は、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* オン [!DNL Walmart].

**前提条件**

輸送業者をマッピングする前に、次のタスクを実行します。

1. 以下を確認します。 [通信事業者の方法と配送に関するベストプラクティス](https://sellerhelp.walmart.com/s/guide?article=000009473) 対象 [!DNL Walmart Marketplace].

1. を確認します。 [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) および [[!UICONTROL Shipping Settings]](https://docs.magento.com/user-guide/configuration/sales/shipping-settings.html) 設定 [!DNL Commerce] を保存して、次の設定を最適化しました。 [!DNL Walmart Marketplace sales].

## 輸送業者をマップ

1. 次の **[!UICONTROL Listings]** または **[!UICONTROL Orders]** ページ、選択 **[!UICONTROL Channel Settings]**.

1. オン **[!UICONTROL Channel Settings]**&#x200B;を選択します。 **[!UICONTROL Shipping Carriers]**.

   ![輸送業者をマップ](assets/map-shipping-carriers.png)

1. 各 [!DNL Walmart] リストに表示された優先キャリア、 [!DNL Commerce] 通信事業者が使用可能な場合は、ドロップダウンから通信事業者名を選択します。

1. 選択 **[!UICONTROL Save]** 設定を適用します。
