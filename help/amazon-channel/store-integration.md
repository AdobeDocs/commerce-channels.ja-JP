---
title: ストアとの統合 [!DNL Amazon Seller Account]
description: オンボーディングプロセスを開始する前に、AmazonSales Channelストアを作成（追加）し、Amazonセラーアカウントに接続する必要があります。
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# ストアとの統合 [!DNL Amazon Seller Account]

Amazonセールスチャネルの使用を開始するには、Amazonセールスチャネルストアを作成（追加）し、 [!DNL Amazon Seller Account]. これら 2 つの手順で、 [!DNL Commerce] およびAmazonアカウントを使用して、データの共有、製品の同期などをおこなうことができます。

_のプライマリログイン資格情報が必要です [!DNL Amazon Seller Central] ストアに接続するためのアカウント（販売者アカウントの作成に使用する電子メールまたは電話）。_

>[!NOTE]
>
>初回のストア統合後、毎年、アクセス権を再度付与してAmazonセールスチャネルとAmazonの接続を更新するよう求めるメッセージが表示されます。 この認証は、 _現在の認証_ 表 _Amazon MWS 開発者権限_ セクション **設定** > **ユーザーの権限** Seller Central アカウントのページ

## Amazonストアを追加

1. の _管理者_ サイドバー、移動 **マーケティング** > _チャネル_ > **AmazonSales Channel**.

   最初のAmazonセールスチャネルストアを追加する場合、 _事前設定タスク_ モーダルが表示されます。 最初のストアを追加した後、事前設定タスクには [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) 下のページ _学習と準備_ をクリックします。

1. クリック **[!UICONTROL Add Amazon Store]**.

   この _[!UICONTROL Add Amazon sales channel]_ページが開きます。

   ![Amazonセールスチャネルストアを追加する](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. の場合 **[!UICONTROL Magento Website to use for Amazon Listing]**&#x200B;を選択し、 [!DNL Commerce] このAmazonセールスチャネルストアに接続する web サイト。

   この設定は、デフォルトの [!DNL Commerce] ～を保存する [Amazon注文のインポート](./order-settings.md).

1. の場合 **[!UICONTROL Email Address]**、希望する連絡先メールアドレスを入力します。

1. の場合 **[!UICONTROL New Store Name]**「 」には、新しいAmazonセールスチャネルストアのわかりやすい名前を入力します。

   >[!NOTE]
   >
   >この名前は、 [!DNL Commerce] を参照し、 [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) ページ。 チームが簡単に識別できるようにしたい。 例えば、米国地域で販売しているAmazonストアの名前を次に示します。 `Amazon Store USA`.

1. の場合 **[!UICONTROL Amazon Marketplace Country]**「 」で、このAmazonセールスチャネルストアが製品を販売する地域または国を選択します。 オプション：

   - 米国
   - カナダ
   - メキシコ
   - 英国

1. 内 _[!UICONTROL Map your Magento attributes to Amazon]_セクションで、以下の操作を実行します。

   - の場合 **[!UICONTROL Product ID on the Amazon market]**&#x200B;にマッピングするAmazon属性を選択します。 [!DNL Commerce] 属性が以下で選択されています。

     この ID は、 [!DNL Commerce] カタログ。

   - の場合 **[!UICONTROL Map a Magento attribute]**、 [!DNL Commerce] 上で選択したAmazon属性にマッピングする製品属性。

     [マッピング属性](./ob-creating-magento-attributes.md) は、Amazonのリストが [!DNL Commerce] カタログ。

1. クリック **[!UICONTROL Connect]**.

   ダイアログが閉じ、新しいストアが [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) ページに確認メッセージが表示されます。

## ストアの接続先 [!DNL Amazon Seller Central]

1. ストアダッシュボードで、 **[!UICONTROL Connect store]** ストアカードで起動 [!DNL Amazon Seller Central] をクリックします。

1. を入力します。 [!DNL Amazon Seller Central] アカウントの資格情報をクリックし、 **[!UICONTROL Sign in]**.

   この接続を完了するには、 [!DNL Amazon Seller Central] プライマリユーザーのログイン資格情報（販売者アカウントの作成に使用する電子メールまたは電話）を使用するアカウント。

1. プロンプトが表示されたら、Amazonから受け取ったコードを入力してAmazon Two-Factor Authorization(2FA) を完了し、 **[!UICONTROL Sign in]**.

1. の _[!UICONTROL Amazon Marketplace Web Service]_確認ページで、「[!UICONTROL I understand...]」チェックボックスをオンにして、**[!UICONTROL Next]**.

1. の _[!UICONTROL You are almost done]_メッセージ、クリック&#x200B;**[!UICONTROL Continue]**.

   Amazonセールスチャネルに対し、データにアクセスして共有する権限を付与しました [!DNL Amazon Seller Central] アカウント Amazonページが閉じ、確認メッセージが表示されます。

   この [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) Amazonストアカードを表示するページが開きます。

   ストアのダッシュボードを表示するには、 **[!UICONTROL View Store]** をストアカードに貼り付けます。

![Amazonセールスチャネルホームに新しいストアカードが付いた](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

新しいAmazonセールスチャネルストアが [!DNL Amazon Seller Central] アカウント

![次のアイコン](assets/btn-next.png) [**リストルールの作成を続行する**](./ob-create-listing-rule.md)
