---
title: 'Connect [!DNL Channel Manager] to [!DNL Walmart Marketplace]'
description: 「Commerceストアの表示を  [!DNL Walmart Marketplace]  に接続して、Commerceの商品リスト、在庫、価格、注文を管理するセールスチャネルを作成します。
exl-id: 8c78c582-7b57-4f73-894e-134ba0ba3640
role: Admin, Developer
feature: Sales Channels, Install, Integration
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# [!DNL Channel Manager] の [!DNL Walmart Marketplace] への接続

[!DNL Commerce] インスタンスにチャネルマネージャーをインストールした後、チャネルマネージャーで販売チャネルを作成し、[!DNL Walmart Marketplace] に接続するための資格情報 [!DNL Channel Manager] 設定します。

1. 製品リスト用の [!DNL Commerce] ストアを選択して [ 販売チャネルを作成 ](#create-the-sales-channel) します。

1. [[!UICONTROL Walmart API credentials]](#connect-the-channel-to-walmart-marketplace) を追加して  [!DNL Walmart Marketplace]  チャネルをに接続します。

1. [ 販売チャネルの設定を完了 ](#complete-sales-channel-store-setup) して、[!DNL Walmart Marketplace] 品の品揃えの一覧、在庫、価格、および注文を管理します。

>[!NOTE]
>
>Channel Manager では、Walmart アカウントと [!DNL Commerce] ストアビューの間で 1 対 1 の接続が必要です。 同じストア表示を複数のウォルマート アカウントに接続することはできません。

## 販売チャネルの作成

1. 管理者で、**[!UICONTROL Marketing** > _チャネル _/**チャネルマネージャー]**を選択して [!DNL Channel Manager] を開きます。

1. 「**[!UICONTROL Marketplaces available to connect]**」セクションで、「**[!UICONTROL Get Started]**」を選択します。

   ![ 新しい [!DNL Walmart] ストアの [!DNL Channel Manager]](assets/channel-manager-home.png){width="700" zoomable="yes"} への接続

1. 必要に応じて、[!DNL Walmart Marketplace Seller] アカウントを設定します。

1. ストアと接続を設定します。

   - 「**[!UICONTROL Add Credentials]**」を選択します。

   - Marketplace で販売する製品を提供する [!DNL Commerce] ストア表示を選択します。

     ![[!DNL Channel Manager]](assets/configure-commerce-to-marketplace-connection.png){width="500" zoomable="yes"} から [!DNL Commerce] と [!DNL Walmart Marketplace] 間の接続を設定する

   - 一意の **[!UICONTROL store name]** を入力します。

   - 商品リストおよび注文処理の **[!UICONTROL Adobe [!DNL Commerce] site]** を選択します。

   - [!DNL Channel Manager] に関連する通知を受信するには、**[!UICONTROL email address]** を追加します。

1. チャネルを [!DNL Walmart Marketplace] に接続します。

   - [!DNL Walmart Marketplace Seller] アカウントから [[!DNL Walmart Marketplace Adobe Production API key]](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) の資格情報を追加します。

   - 資格情報がない場合は、「**[!UICONTROL Get API credentials]**」を選択して [!DNL Walmart Marketplace Developer Portal] から取得します。

     開発者ポータルで、お住まいの地域（米国およびカナダ）を選択し、ログインします。

     ![[!DNL Walmart Marketplace] アカウント ログイン ](assets/walmart-marketplace-login-page.png){width="600"}

   - API キーのフォームで、**[!UICONTROL Client ID]** と [!UICONTROL Adobe Inc Production API key] の **[!UICONTROL Client Secret]** の値をコピーして安全な場所に保存します。

     設定ペ ![[!DNL Walmart Marketplace API key] ジ ](assets/walmart-api-key-management-form.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >[!DNL Adobe Inc] キーが開発者ポータルにリストされていない場合は、「**[!UICONTROL Add New Key for a Solution Provider]**」を選択して権限を設定し、キーを生成します。 設定について詳しくは、[ 生成  [!DNL Walmart Marketplace API Key]](walmart-requirements.md#generate-a-walmart-marketplace-api-key) を参照してください。

   - [!DNL Channel Manager] に戻り、**[!UICONTROL Walmart Connection]** 情報に資格情報を追加します。

     資格情報を追加する場合、Adobeはクライアントシークレットを非表示にし、値を安全な Vault に保存します。

1. 「**[!UICONTROL Save Store]**」を選択して設定を適用し、[!DNL Walmart marketplace] に接続します。

1. 正常に接続したら、[ ストアの設定を完了 ](complete-sales-channel-store-setup.md) して、**[!UICONTROL Channel Manager]** ストアページから移動します。

![ 最初のストアを設定 ](assets/channel-manager-setup-first-store.png){width="500" zoomable="yes"}

### 接続の問題のトラブルシューティング

[!DNL Walmart] への接続に失敗した場合、トラブルシューティングのヒントについては、[Walmart Marketplace FAQ](https://developer.walmart.com/faq/us/faq-auth/){target="_blank"} を参照してください。

- [!DNL Walmart Developer Portal] から、[!UICONTROL Adobe Inc.] の実稼動 API キー用の正しい資格情報をコピーしたことを確認します

- [!UICONTROL Walmart Adobe API key] のアクセス設定に適切な権限が設定されていることを確認します。 [[!DNL Walmart Requirements]](walmart-requirements.md##generate-a-walmart-marketplace-api-key) を参照。

- [Walmart API ステータスページ ](https://developer.walmart.com/us/whats-new/new-api-status-information-now-available/){target="_blank"} から [!DNL Walmart API] サービスが使用可能であることを確認します。
