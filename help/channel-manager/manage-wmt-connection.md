---
title: Walmart Marketplace 連携の管理
description: 'API 資格情報を更新して、[DNL！間の接続を認証します Commerce] store view and the [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] product listings and synchronize inventory, price, order and shipping data between [!DNL Commerce] and the Walmart.'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 配送業者のマップ

オーダーの出荷を [ 処理 ](process-orders.md#ship-an-order) する前に、[!DNL Walmart Marketplace] のオーダーについて、ウォルマートの優先出荷搬送を [!DNL Commerce] で対応する搬送にマップして、[!DNL Walmart] と [!DNL Commerce] の間で出荷データを同期できるようにします。

優先する通信事業者にマッピングしないCommerceの通信事業者には、[!DNL Walmart] で *[!UICONTROL Other Carrier]* というラベルが付けられます。

**前提条件**

[!DNL Marketplace Seller account] の [ ウォルマート要件 ](walmart-requirements.md) を確認します。

## 接続資格情報を更新

1. 営業チャネル ストアの [!UICONTROL Listings] ページで、[**[!UICONTROL Channel Settings]**] を選択します。

1. **[!UICONTROL Channel Settings]** で「**[!UICONTROL Walmart Connection]**」を選択します。

1. 資格情報を変更するには、「**[!UICONTROL Change Credentials]**」を選択します。

   ![Walmart API 認証情報を更新して接続を認証する ](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. **[!UICONTROL Walmart Client ID]** と **[!UICONTROL Walmart Client Secret]** を入力します。

1. 「**[!UICONTROL Save]**」を選択して、設定を適用します。
