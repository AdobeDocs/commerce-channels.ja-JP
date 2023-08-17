---
title: '接続 [!DNL Channel Manager] から [!DNL Walmart Marketplace]'
description: コマースストア表示の接続先 [!DNL Walmart Marketplace] Walmart Marketplace の販売に関するコマース製品リスト、在庫、価格、注文を管理するセールスチャネルを作成する。」
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# 接続 [!DNL Channel Manager] から [!DNL Walmart Marketplace]

に Channel Manager をインストールした後、 [!DNL Commerce] 例えば、チャネルマネージャーでセールスチャネルを作成し、接続するための資格情報を設定します [!DNL Channel Manager] から [!DNL Walmart Marketplace].

1. [セールスチャネルを作成する](#create-the-sales-channel) 選択して [!DNL Commerce] 製品リスト用のストア。

1. [チャネルの接続先 [!DNL Walmart Marketplace] 追加する [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [セールスチャネルの設定の完了](#complete-sales-channel-store-setup) のリスト、在庫、価格、注文を管理する [!DNL Walmart Marketplace] 製品の品揃え。

>[!NOTE]
>
>Channel Manager では、Walmart アカウントと [!DNL Commerce] ストア表示。 同じストア表示を複数のウォルマートアカウントに接続することはできません。

## セールスチャネルを作成する

1. 管理者から、を開きます。 [!DNL Channel Manager] 選択する **[!UICONTROL Marketing** > _チャネル&#x200B;_> **チャネルマネージャ]**.

1. Adobe Analytics の **[!UICONTROL Marketplaces available to connect]** セクション、選択 **[!UICONTROL Get Started]**.

   ![新規接続 [!DNL Walmart] 保存先 [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. 必要に応じて、 [!DNL Walmart Marketplace Seller] アカウント。

1. ストアと接続の設定：

   - 選択 **[!UICONTROL Add Credentials]**.

   - を選択します。 [!DNL Commerce] マーケットプレイスで販売する製品を提供するストア表示。

     ![次の間の接続を設定 [!DNL Commerce] および [!DNL Walmart Marketplace] から [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - 一意の **[!UICONTROL store name]**.

   - を選択します。 **[!UICONTROL Adobe [!DNL Commerce] site]** 製品のリストと注文の処理。

   - 次に関連する通知を受け取るには： [!DNL Channel Manager]、を追加します。 **[!UICONTROL email address]**.

1. チャネルの接続先 [!DNL Walmart Marketplace].

   - の資格情報を追加します。 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) から [!DNL Walmart Marketplace Seller] アカウント。

   - 資格情報がない場合は、 [!DNL Walmart Marketplace Developer Portal] 選択する **[!UICONTROL Get API credentials]**.

     開発者ポータルで、お住まいの地域（米国およびカナダ）を選択し、ログインします。

     ![[!DNL Walmart Marketplace] アカウントログイン](assets/walmart-marketplace-login-page.png){width="600"}

   - API キーフォームで、 **[!UICONTROL Client ID]** および **[!UICONTROL Client Secret]** の値 [!UICONTROL Adobe Inc Production API key] を安全な場所に移動します。

     ![[!DNL Walmart Marketplace API key] 設定ページ](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >次の場合、 [!DNL Adobe Inc] キーが開発者ポータルに表示されない場合は、「 **[!UICONTROL Add New Key for a Solution Provider]** 権限を設定し、キーを生成する。 設定の詳細については、 [を生成する [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - 戻る [!DNL Channel Manager] に資格情報を追加するには、以下を実行します。 **[!UICONTROL Walmart Connection]** 情報。

     認証情報を追加すると、Adobeはクライアント秘密鍵を非表示にし、その値を安全な Vault に保存します。

1. 選択 **[!UICONTROL Save Store]** 設定を適用し、 [!DNL Walmart marketplace].

1. 接続が成功したら、 [ストア設定を完了](complete-sales-channel-store-setup.md) から **[!UICONTROL Channel Manager]** ストアページ。

![最初のストアを設定](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### 接続の問題のトラブルシューティング

接続先が [!DNL Walmart] 失敗 ( [Walmart Marketplace に関する FAQ](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} トラブルシューティングのヒント。

- 次から： [!DNL Walmart Developer Portal]に設定し、の実稼動 API キーの正しい資格情報をコピーしたことを確認します。 [!UICONTROL Adobe Inc.]

- のアクセス設定を確認します。 [!UICONTROL Walmart Adobe API key] には正しい権限があります。 詳しくは、 [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- を確認します。 [!DNL Walmart API] サービスは、 [ウォルマート API ステータスページ](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
