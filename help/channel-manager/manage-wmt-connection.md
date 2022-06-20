---
title: ウォルマートマーケットプレイス接続の管理
description: API 資格情報を更新して、[DNL! Commerce] ストア表示と [!DNL Walmart Marketplace]. この接続は、コマース製品リストを接続し、Commerce と Walmart の間で在庫、価格、注文、および出荷データを同期するために必要です。
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 輸送業者をマップ

事前準備 [オーダー出荷の処理](process-orders.md#ship-an-order) 対象 [!DNL Walmart Marketplace] 注文、ウォルマートの優先配送業者を、 [!DNL Commerce] これにより、輸送データを [!DNL Walmart] および [!DNL Commerce].

優先通信事業者にマッピングされていない通信事業者は、次のラベルが付けられます。 *[!UICONTROL Other Carrier]* オン [!DNL Walmart].

**前提条件**

レビュー [ウォルマートの要件](walmart-requirements.md) の [!DNL Marketplace Seller account].

## 接続資格情報を更新

1. の [!UICONTROL Listings] セールスチャネルストアのページで、「 」を選択します。 **[!UICONTROL Channel Settings]**.

1. オン **[!UICONTROL Channel Settings]**&#x200B;を選択します。 **[!UICONTROL Walmart Connection]**.

1. 認証情報を変更するには、「 」を選択します。 **[!UICONTROL Change Credentials]**

   ![接続を認証するための Walmart API 認証情報の更新](assets/update-connection-credentials.png)

1. 次を入力します。 **[!UICONTROL Walmart Client ID]** および **[!UICONTROL Walmart Client Secret]**.

1. 選択 **[!UICONTROL Save]** 設定を適用します。
