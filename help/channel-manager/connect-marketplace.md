---
title: '接続 [!DNL Channel Manager] 対象： [!DNL Walmart Marketplace]'
description: 「Commerce ストア表示をに接続する [!DNL Walmart Marketplace] Commerceの商品リスト、在庫、価格、注文を管理する営業チャネルを作成するには、Walmart Marketplace の売上について説明します。
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 接続 [!DNL Channel Manager] 対象： [!DNL Walmart Marketplace]

チャネルマネージャーのインストール後 [!DNL Commerce] インスタンスとして、チャネルマネージャーで販売チャネルを作成し、接続するための資格情報を設定します [!DNL Channel Manager] 対象： [!DNL Walmart Marketplace].

1. [販売チャネルの作成](#create-the-sales-channel) を選択します。 [!DNL Commerce] 製品リストのストア。

1. [チャネルの接続先 [!DNL Walmart Marketplace] を追加 [!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace).

1. [販売チャネル設定の完了](#complete-sales-channel-store-setup) リスト、在庫、価格設定および受注を管理する手順は、次のとおりです [!DNL Walmart Marketplace] 製品の品揃え。

>[!NOTE]
>
>Channel Manager では、Walmart アカウントとの間で 1 対 1 の接続が必要です。 [!DNL Commerce] ストア表示。 同じストア表示を複数のウォルマート アカウントに接続することはできません。

## 販売チャネルの作成

1. 管理者から、を開きます。 [!DNL Channel Manager] 選択による **[!UICONTROL Marketing** > _チャネル&#x200B;_> **チャネルマネージャー]**.

1. が含まれる **[!UICONTROL Marketplaces available to connect]** セクションで選択 **[!UICONTROL Get Started]**.

   ![新規を接続 [!DNL Walmart] に保存 [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"}

1. 必要に応じて、 [!DNL Walmart Marketplace Seller] アカウント。

1. ストアと接続を設定します。

   - を選択 **[!UICONTROL Add Credentials]**.

   - 「」を選択します [!DNL Commerce] マーケットプレイスで販売する製品を提供するストア表示。

     ![間の接続の設定 [!DNL Commerce] および [!DNL Walmart Marketplace] から [!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"}

   - 一意のを入力 **[!UICONTROL store name]**.

   - 「」を選択します **[!UICONTROL Adobe [!DNL Commerce] site]** 商品リストおよび注文処理の場合。

   - に関連する通知を受信するには [!DNL Channel Manager]、を追加 **[!UICONTROL email address]**.

1. チャネルの接続先 [!DNL Walmart Marketplace].

   - の資格情報を追加します。 [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) から [!DNL Walmart Marketplace Seller] アカウント。

   - 資格情報がない場合は、から取得します。 [!DNL Walmart Marketplace Developer Portal] 選択による **[!UICONTROL Get API credentials]**.

     開発者ポータルで、お住まいの地域（米国およびカナダ）を選択し、ログインします。

     ![[!DNL Walmart Marketplace] アカウントのログイン](assets/walmart-marketplace-login-page.png){width="600"}

   - API キーのフォームで、 **[!UICONTROL Client ID]** および **[!UICONTROL Client Secret]** の値 [!UICONTROL Adobe Inc Production API key] 安全な場所に移動します。

     ![[!DNL Walmart Marketplace API key] 設定ページ](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >次の場合 [!DNL Adobe Inc] キーが開発者ポータルに一覧表示されていません。次を選択してください： **[!UICONTROL Add New Key for a Solution Provider]** 権限を設定し、キーを生成します。 設定について詳しくは、を参照してください [を生成 [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key).

   - に戻る [!DNL Channel Manager] に資格情報を追加する **[!UICONTROL Walmart Connection]** 情報。

     資格情報を追加する場合、Adobeはクライアントシークレットを非表示にし、値を安全な Vault に保存します。

1. を選択 **[!UICONTROL Save Store]** 設定を適用してに接続するには [!DNL Walmart marketplace].

1. 正常に接続すると、 [ストアの設定の完了](complete-sales-channel-store-setup.md) から **[!UICONTROL Channel Manager]** ストアページ。

![最初のストアを設定](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### 接続の問題のトラブルシューティング

への接続の場合 [!DNL Walmart] 失敗します。を参照してください [Walmart Marketplace FAQ](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} トラブルシューティングのヒント

- から [!DNL Walmart Developer Portal]に対して、実稼動 API キーの正しい資格情報をコピーしたことを確認します。 [!UICONTROL Adobe Inc.]

- のアクセス設定を確認します。 [!UICONTROL Walmart Adobe API key] には適切な権限があります。 参照： [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key).

- を確認します [!DNL Walmart API] サービスは、次から使用できます [ウォルマート API ステータスページ](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"}.
