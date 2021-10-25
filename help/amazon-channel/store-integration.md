---
title: ストア統合
description: オンボードプロセスを開始する前に、Amazon 販売チャンネルストアを作成 (追加) し、Amazon 売り手アカウントに関連付ける必要があります。
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# ストア統合

Amazon 販売チャンネルを初めて使用するには、Amazon sales channel ストアを作成して追加し、Amazon 売り手アカウントに関連付ける必要があります。 この2つの手順では、と Amazon のアカウントを統合して、 [!DNL Commerce] データの共有、製品の同期などを行います。

_[!DNL Amazon Seller Central]ストアを接続するには、アカウント (販売者アカウントを作成するために使用される電子メールまたは電話) のプライマリログイン資格情報を必要とします。_

>[!NOTE]
>
>最初のストア統合が完了すると、その後、アクセスを許可することで、amazon に対する Amazon 販売チャンネルの接続を更新するよう求めるメッセージが毎年表示されます。 この承認は、「 __ > の設定」を参照して __ **** **ください。「ユーザー権限の設定」** ページの「現在の承認」にある「開発者アクセス権」セクションにある「現在の承認」によって、更新または失効を行うことができます

## Amazon store の追加

1. _管理_ サイドバーで、 **販促** > _チャンネル_ > **Amazon Sales Channel に移動** します。

   最初の Amazon sales channel store を追加すると、 _事前設定タスクの_ モーダルが表示されます。 最初のストアが追加されると、左側に表示される [ ](./amazon-sales-channel-home.md) 「学習と準備」の「Amazon sales channel」ホームページで、事前に設定したタスクにアクセスでき __ ます。

1. をクリックし **[!UICONTROL Add Amazon Store]** ます。

   _[!UICONTROL Add Amazon sales channel]_ページが開きます。

   ![Amazon sales チャンネルストアを追加します。](assets/amazon-store-integration.png)

1. について **[!UICONTROL Magento Website to use for Amazon Listing]** は、 [!DNL Commerce] この Amazon 販売チャンネルストア用に接続する web サイトを選択します。

   この設定によって、 [!DNL Commerce] Amazon の注文を取り込むためのデフォルトのストアも定義さ [ ](./order-settings.md) れます。

1. **[!UICONTROL Email Address]**「」には、連絡先電子メールアドレスを入力します。

1. **[!UICONTROL New Store Name]**「」に、新しい Amazon 販売チャンネルストアの内容を示す名前を入力します。

   >[!NOTE]
   >
   >この名前はリファレンスとしてのみ使用され、 [!DNL Commerce] Amazon 販売チャンネルのホームページでストアを識別し [ ](./amazon-sales-channel-home.md) ます。 チームが容易に識別できるようにする必要があります。 例えば、米国地域に販売される Amazon store には、という名前が付けら `Amazon Store USA` れています。

1. **[!UICONTROL Amazon Marketplace Country]**「」で、この Amazon 販売店のチャネルストアが製品を販売する地域/国を選択します。オプション：

   - 米国
   - カナダ
   - メキシコ
   - 英国

1. セクションで _[!UICONTROL Map your Magento attributes to Amazon]_、次の操作を行います。

   - **[!UICONTROL Product ID on the Amazon market]**&#x200B;で、次に選択した属性にマップするために Amazon 属性を選択 [!DNL Commerce] します。

      この ID を使用して、カタログ内の対応する製品を正確に一致させることができ [!DNL Commerce] ます。

   - については **[!UICONTROL Map a Magento attribute]** 、 [!DNL Commerce] 上で選択した Amazon 属性にマップする製品属性を選択します。

      [属性のマッピング ](./ob-creating-magento-attributes.md) を行うと、Amazon リストが、カタログ内の対応する製品と完全に一致することを確認でき [!DNL Commerce] ます。

1. をクリックし **[!UICONTROL Connect]** ます。

   ダイアログが閉じ、新しいストアが [ Amazon 販売チャンネルのホームページに ](./amazon-sales-channel-home.md) 確認メッセージと共に表示されます。

## ストアの接続 [!DNL Amazon Seller Central]

1. Store のダッシュボードで、「 **[!UICONTROL Connect store]** store」カードをクリックして [!DNL Amazon Seller Central] 新しいタブで起動します。

1. アカウントの [!DNL Amazon Seller Central] 資格情報を入力し、をクリックし **[!UICONTROL Sign in]** ます。

   この接続を完了するには、 [!DNL Amazon Seller Central] プライマリユーザー (販売者アカウントを作成するために使用された電子メールまたは電話) に対するログイン資格情報を使用してアカウントにサインインする必要があります。

1. 確認メッセージが表示されたら、Amazon から取得されたコードを入力してクリックし、Amazon Two Multi-factor Authorization (2FA) を完了し **[!UICONTROL Sign in]** ます。

1. _[!UICONTROL Amazon Marketplace Web Service]_確認ページで「」チェックボックスを選択し、を [!UICONTROL I understand...] クリックし&#x200B;**[!UICONTROL Next]**ます。

1. メッセージの _[!UICONTROL You are almost done]_をクリックし&#x200B;**[!UICONTROL Continue]**ます。

   アカウントを使用したデータへのアクセスと共有を行うために、Amazon sales チャンネルが許可されてい [!DNL Amazon Seller Central] ます。 Amazon ページが閉じ、確認メッセージが表示されます。

   Amazon [ 販売チャンネルのホーム ](./amazon-sales-channel-home.md) ページに、amazon store カードが表示されます。

   ストアのダッシュボードを表示するには、「store」カードをクリックし **[!UICONTROL View Store]** ます。

![新しいストアカードを使用した Amazon セールスチャネルホーム](assets/asc-dashboard-after-2fa.png)

新しい Amazon 販売チャンネルストアがアカウントに接続されました [!DNL Amazon Seller Central] 。

![次 ](assets/btn-next.png) [**のアイコン一覧ルールの作成を続行します。**](./ob-create-listing-rule.md)
