---
title: Sales Channelの接続先 [!DNL Walmart Marketplace]
description: セールスチャネルを設定し、Walmart Marketplace に接続します。
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 8f07b215c20cc28aa9a6862bcb2b00da30a1ed84
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 接続先 [!DNL Walmart Marketplace]

に Channel Manager をインストールした後、 [!DNL Commerce] 例えば、コマースストアを Walmart Marketplace に接続します。

1. セールスチャネルの作成基準 [製品リスト用のコマースストアの選択](#select-the-commerce-store-for-the-sales-channel).

1. [チャネルの接続先 [!DNL Walmart Marketplace] ウォルマート API 資格情報を追加する](#connect-the-channel-to-walmart-marketplace).

1. [セールスチャネルの設定の完了](#complete-store-setup) そのため、Channel Manger からリスト、在庫、価格、販売を管理できます。

## セールスチャネルを作成

1. チャネルマネージャを開きます。

   - 管理者で、 **[!UICONTROL Marketing** > _チャネル&#x200B;_> **チャネルマネージャ]**.

   - 選択 **[!UICONTROL Connect New Store]**.

      ![コマースストアの接続先 [!DNL Walmart Marketplace] から [!DNL Channel Manager]](assets/connect-commerce-store-to-marketplace.png)


1. ストアと接続の設定：

   - 一意の **[!UICONTROL store name]**.

   - を選択します。 **[!UICONTROL Adobe Commerce site]** 製品リスト用。

   - を追加します。 **[!UICONTROL email address]** ～に関するサービス通知を受け取る [!DNL Channel Manager].

      ![コマースとの接続を設定する [!DNL Walmart Marketplace] から [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)


## チャネルを Walmart Marketplace に接続します。

1. の資格情報を追加します。 [!DNL Walmart Marketplace Adobe Production API key] から [!DNL Walmart Marketplace Seller] アカウント

   - 資格情報をお持ちでない場合は、「 」を選択します。 **[!UICONTROL Get API credentials]** 彼らを [!DNL Walmart Marketplace Developer Portal].

      プロンプトが表示されたら、お住まいの地域（米国およびカナダ）を選択し、ログインします。

      ![[!DNL Walmart Marketplace] アカウントログイン](assets/walmart-marketplace-login-page.png)

   - API キーフォームで、 **[!UICONTROL Client ID]** および **[!UICONTROL Client Secret]** の値 [!UICONTROL Adobe Inc Production API key] を安全な場所に移動します。

      ![[!DNL Walmart Marketplace API key] 設定ページ](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >この [!DNL Adobe Inc] キーが開発者ポータルに表示されない場合は、 **[!UICONTROL Add New Key for a Solution Provider]** 権限を設定し、キーを生成する。 設定の詳細については、 [を生成する [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - 戻る [!DNL Channel Manager] 認証情報を **[!UICONTROL Walmart Connection]** 情報。

      に資格情報を追加する場合 [!DNL Channel Manager]の場合、Adobeはクライアントシークレットを非表示にし、値を安全な Vault に保存します。

1. [!UICONTROL Save] 接続を確立するための設定。

   接続に成功したら、 **[!UICONTROL Channel Manager > Marketplace Stores]**.

   ![[!DNL Walmart Marketplace API key] 設定ページ](assets/manage-connected-stores.png)


### 接続の問題のトラブルシューティング

ウォルマートへの接続に失敗した場合は、 [Walmart Marketplace に関する FAQ](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} を参照してください。

- 次の [!DNL Walmart Developer Portal]に設定し、の実稼動 API キーの正しい資格情報をコピーしたことを確認します。 [!UICONTROL Adobe Inc.]

- WalmartAdobeAPI キーのアクセス設定に正しい権限があることを確認します。 詳しくは、 [ウォルマートの前提条件](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- Walmart API サービスが [ウォルマート API ステータスページ](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}。
