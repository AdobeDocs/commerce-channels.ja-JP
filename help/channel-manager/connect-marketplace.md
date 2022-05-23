---
title: セールスチャネルの接続先 [!DNL Walmart Marketplace]
description: セールスチャネルを設定し、Walmart Marketplace に接続します。
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
source-git-commit: 7349dd92c2166ff6ae83b705416993e48aa5f954
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# セールスチャネルの接続先 [!DNL Walmart Marketplace]

に Channel Manager をインストールした後、 [!DNL Commerce] 例えば、コマースストアを Walmart Marketplace に接続します。

1. [セールスチャネルを作成](#create-the-sales-channel) 商品リスト用のコマースストアを選択する。

1. [チャネルの接続先 [!DNL Walmart Marketplace] ウォルマート API 資格情報を追加する](#connect-the-channel-to-walmart-marketplace).

1. [セールスチャネルの設定の完了](#complete-store-setup) をクリックして、Walmart Marketplace 製品の品揃えのリスト、在庫、価格、注文を管理します。

## セールスチャネルを作成

1. 管理者から、を開きます。 [!DNL Channel Manager] 選択する **[!UICONTROL Marketing** > _チャネル&#x200B;_> **チャネルマネージャ]**.

1. 内 **[!UICONTROL Marketplaces available to connect]** セクション、選択 **[!UICONTROL Get Started]**.

   ![新しいウォルマートストアをに接続 [!DNL Channel Manager]](assets/channel-manager-home.png)

1. 必要に応じて、Walmart Marketplace Seller アカウントを設定します。

1. ストアと接続の設定：

   - 選択 **[!UICONTROL Add Credentials]**.

   - を選択します。 [!DNL Commerce] マーケットプレイスに接続するためのストア表示。

      ![コマースとの接続を設定する [!DNL Walmart Marketplace] から [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png)

   - 一意の **[!UICONTROL store name]**.

   - を選択します。 **[!UICONTROL Adobe Commerce site]** 製品リスト用。

   - を追加します。 **[!UICONTROL email address]** ～に関するサービス通知を受け取る [!DNL Channel Manager].

1. チャネルの接続先 [!DNL Walmart Marketplace].

   - の資格情報を追加します。 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-prerequisites.md#generate-a-walmart-marketplace-production-api-key) から [!DNL Walmart Marketplace Seller] アカウント

   - 資格情報がない場合は、 [!DNL Walmart Marketplace Developer Portal] 選択する **[!UICONTROL Get API credentials]**.

      開発者ポータルで、お住まいの地域（米国およびカナダ）を選択し、ログインします。

      ![[!DNL Walmart Marketplace] アカウントログイン](assets/walmart-marketplace-login-page.png)

   - API キーフォームで、 **[!UICONTROL Client ID]** および **[!UICONTROL Client Secret]** の値 [!UICONTROL Adobe Inc Production API key] を安全な場所に移動します。

      ![[!DNL Walmart Marketplace API key] 設定ページ](assets/walmart-api-key-management-form.png)

      >[!NOTE]
      >
      >この [!DNL Adobe Inc] キーが開発者ポータルに表示されない場合は、 **[!UICONTROL Add New Key for a Solution Provider]** 権限を設定し、キーを生成する。 設定の詳細については、 [を生成する [!DNL Walmart Marketplace API Key]](walmart-prerequisites.md#generate-a-walmart-marketplace-api-key).

   - 戻る [!DNL Channel Manager] 認証情報を **[!UICONTROL Walmart Connection]** 情報。

      認証情報を追加すると、Adobeはクライアント秘密鍵を非表示にし、その値を安全な Vault に保存します。

1. 選択 **[!UICONTROL Save Store]** 設定を適用し、 [!DNL Walmart marketplace].

1. 接続が成功したら、 [ストア設定を完了](complete-store-setup.md) から **[!UICONTROL Channel Manager]** ストアページ。

![最初のストアを設定](assets/channel-manager-setup-first-store.png)

### 接続の問題のトラブルシューティング

ウォルマートへの接続に失敗した場合は、 [Walmart Marketplace に関する FAQ](https://developer.walmart.com/faq/us/faq-auth/){target=&quot;_blank&quot;} を参照してください。

- 次の [!DNL Walmart Developer Portal]に設定し、の実稼動 API キーの正しい資格情報をコピーしたことを確認します。 [!UICONTROL Adobe Inc.]

- WalmartAdobeAPI キーのアクセス設定に正しい権限があることを確認します。 詳しくは、 [ウォルマートの前提条件](walmart-prerequisites.md##generate-a-walmart-marketplace-api-key).

- を確認します。 [!DNL Walmart API] サービスは [ウォルマート API ステータスページ](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target=&quot;_blank&quot;}。
