---
title: Walmart Marketplace 連携の管理
description: '''API 資格情報を更新して、[DNL！間の接続を認証します Commerce] ストア表示と [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 製品リストと、在庫、価格、注文および配送データの間での同期 [!DNL Commerce] ウォルマートも』'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 配送業者のマップ

お客様の前に [注文の出荷を処理](process-orders.md#ship-an-order) （用） [!DNL Walmart Marketplace] 注文し、ウォルマートの優先配送業者を対応する配送業者にマッピングします [!DNL Commerce] これにより、配送データを次の期間にわたって同期できます。 [!DNL Walmart] および [!DNL Commerce].

優先する通信事業者にマッピングしないCommerce通信事業者には、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* 日付： [!DNL Walmart].

**前提条件**

レビュー [ウォルマートの要件](walmart-requirements.md) の場合 [!DNL Marketplace Seller account].

## 接続資格情報を更新

1. 日 [!UICONTROL Listings] 販売チャネル ストアのページで、次を選択します **[!UICONTROL Channel Settings]**.

1. 日付： **[!UICONTROL Channel Settings]**&#x200B;を選択 **[!UICONTROL Walmart Connection]**.

1. 認証情報を変更するには、以下を選択します。 **[!UICONTROL Change Credentials]**

   ![Walmart API 認証情報を更新して接続を認証する](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. を入力 **[!UICONTROL Walmart Client ID]** および **[!UICONTROL Walmart Client Secret]**.

1. を選択 **[!UICONTROL Save]** をクリックして設定を適用します。
