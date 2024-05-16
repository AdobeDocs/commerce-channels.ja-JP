---
title: とのストアの統合 [!DNL Amazon Seller Account]
description: オンボーディングプロセスを開始する前に、Amazon Sales Channelストアを作成（追加）し、Amazon販売者アカウントに接続する必要があります。
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# とのストアの統合 [!DNL Amazon Seller Account]

Amazonのセールスチャネルの使用を開始するには、Amazonのセールスチャネルストアを作成（追加）し、 [!DNL Amazon Seller Account]. これら 2 つの手順により、 [!DNL Commerce] とAmazon アカウントを使用すると、データの共有や商品の同期などを行うことができます。

_のプライマリログイン資格情報が必要です [!DNL Amazon Seller Central] アカウント（販売者アカウントの作成に使用するメールまたは電話）：ストアに接続します。_

>[!NOTE]
>
>初めてストアに統合した後、アクセス権を再度付与してAmazonへのAmazon Sales Channel 接続を更新するよう、毎年プロンプトが表示されます。 で、この認証を更新または取り消すことができます _現在の承認_ のテーブル _Amazon MWS 開発者権限_ の節 **設定** > **ユーザー権限** 販売者中央アカウントのページ。

## Amazon ストアを追加する

1. 日 _Admin_ サイドバー、に移動 **Marketing** > _チャネル_ > **AmazonSales Channel**.

   最初のAmazon販売チャネルストアを追加する場合、 _事前設定タスク_ モーダルが表示されます。 最初のストアが追加されたら、で事前設定タスクにアクセスできます。 [Amazon販売チャネルホーム](./amazon-sales-channel-home.md) ページの下 _学習と準備_ 左側のメニューの

1. クリック **[!UICONTROL Add Amazon Store]**.

   この _[!UICONTROL Add Amazon sales channel]_ページが開きます。

   ![Amazon販売チャネルストアを追加します。](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. の場合 **[!UICONTROL Magento Website to use for Amazon Listing]**&#x200B;を選択してください [!DNL Commerce] このAmazon セールスチャネルストアに接続するための web サイトです。

   この設定は、デフォルトも定義します [!DNL Commerce] 保管する [Amazon注文の読み込み](./order-settings.md).

1. の場合 **[!UICONTROL Email Address]**：希望する連絡先メールアドレスを入力します。

1. の場合 **[!UICONTROL New Store Name]**&#x200B;を入力し、新しいAmazonセールスチャネルストアのわかりやすい名前を入力します。

   >[!NOTE]
   >
   >この名前は [!DNL Commerce] のみを参照し、のストアを識別します。 [Amazon販売チャネルホーム](./amazon-sales-channel-home.md) ページ。 チームが簡単に識別できるものにしたい。 例えば、米国で販売されているAmazon ストアの名前は次のようになります `Amazon Store USA`.

1. の場合 **[!UICONTROL Amazon Marketplace Country]**&#x200B;を選択し、このAmazon sales channel store が商品を販売する地域/国を選択します。 オプション：

   - 米国
   - カナダ
   - メキシコ
   - 英国

1. が含まれる _[!UICONTROL Map your Magento attributes to Amazon]_セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Product ID on the Amazon market]**&#x200B;を選択し、にマッピングするAmazon属性を選択します [!DNL Commerce] 以下で属性を選択しました。

     この ID は、の対応する製品を正しく照合するのに役立ちます [!DNL Commerce] カタログ。

   - の場合 **[!UICONTROL Map a Magento attribute]**、を選択します [!DNL Commerce] 上記で選択したAmazon属性にマッピングする製品属性。

     [属性のマッピング](./ob-creating-magento-attributes.md) Amazonのリストがユーザーの製品と正しく一致することを確認できます [!DNL Commerce] カタログ。

1. クリック **[!UICONTROL Connect]**.

   ダイアログが閉じ、新しいストアがに表示されます [Amazon販売チャネルホーム](./amazon-sales-channel-home.md) 確認メッセージが表示されたページ。

## ストアの接続先 [!DNL Amazon Seller Central]

1. ストアダッシュボードで、 **[!UICONTROL Connect store]** 開始するストアカード [!DNL Amazon Seller Central] 新しいタブで上書きできます。

1. を入力 [!DNL Amazon Seller Central] アカウント資格情報を入力し、 **[!UICONTROL Sign in]**.

   この接続を完了するには、にサインインする必要があります [!DNL Amazon Seller Central] プライマリユーザーのログイン資格情報を使用するアカウント（販売者アカウントの作成に使用するメールまたは電話）。

1. プロンプトが表示されたら、Amazonから受け取るコードを入力してAmazon 2 要素認証（2FA）を行い、をクリックします。 **[!UICONTROL Sign in]**.

1. 日 _[!UICONTROL Amazon Marketplace Web Service]_確認ページで、「[!UICONTROL I understand...]」チェックボックスをオンにして、**[!UICONTROL Next]**.

1. 日 _[!UICONTROL You are almost done]_メッセージ、クリック&#x200B;**[!UICONTROL Continue]**.

   Amazon セールスチャネルに対して、データへのアクセスおよびとのデータ共有を許可しました [!DNL Amazon Seller Central] アカウント。 Amazonページが閉じ、確認メッセージが表示されます。

   この [Amazon販売チャネルホーム](./amazon-sales-channel-home.md) Amazonのストアカードを示すページが開きます。

   ストアダッシュボードを表示するには、をクリックします **[!UICONTROL View Store]** ストアカードに。

![新しい店舗カードを使用したAmazon販売チャネルホーム](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

これで、新しいAmazon セールスチャネルストアがに接続されました [!DNL Amazon Seller Central] アカウント。

![次へアイコン](assets/btn-next.png) [**リストルールの作成を続行**](./ob-create-listing-rule.md)
