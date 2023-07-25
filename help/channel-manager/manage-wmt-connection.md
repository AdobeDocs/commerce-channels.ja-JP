---
title: ウォルマートマーケットプレイス接続の管理
description: API 資格情報を更新して、[DNL! Commerce] ストア表示と [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] 製品の一覧を作成し、在庫、価格、注文、配送先のデータを同期します。 [!DNL Commerce] そしてウォルマート」
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# 配送業者をマップ

事前準備 [オーダー出荷の処理](process-orders.md#ship-an-order) 対象 [!DNL Walmart Marketplace] 注文、ウォルマートの優先配送業者を、 [!DNL Commerce] これにより、輸送データを [!DNL Walmart] および [!DNL Commerce].

優先通信事業者にマッピングされていない通信事業者は、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* オン [!DNL Walmart].

**前提条件**

レビュー [ウォルマートの要件](walmart-requirements.md) の [!DNL Marketplace Seller account].

## 接続資格情報を更新

1. の [!UICONTROL Listings] セールスチャネルストアのページで、「 」を選択します。 **[!UICONTROL Channel Settings]**.

1. オン **[!UICONTROL Channel Settings]**&#x200B;を選択します。 **[!UICONTROL Walmart Connection]**.

1. 認証情報を変更するには、「 」を選択します。 **[!UICONTROL Change Credentials]**

   ![接続を認証するための Walmart API 認証情報の更新](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Walmart Client ID]** および **[!UICONTROL Walmart Client Secret]**.

1. 選択 **[!UICONTROL Save]** 設定を適用します。
