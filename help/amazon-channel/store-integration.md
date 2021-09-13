---
title: ストア統合
description: オンボーディングプロセスを開始する前に、AmazonSales Channelストアを作成（追加）し、Amazonセラーアカウントに接続する必要があります。
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# ストア統合

Amazon販売チャネルの使用を開始するには、Amazon販売チャネルストアを作成（追加）し、Amazon販売者アカウントに接続する必要があります。 これら2つの手順で、[!DNL Commerce]とAmazonのアカウントを統合して、データの共有、製品の同期などをおこないます。

_ストアに接続するには、アカウントのプライマリログイ [!DNL Amazon Seller Central] ン資格情報（販売者アカウントの作成に使用する電子メールまたは電話）が必要です。_

>[!NOTE]
>
>初回のストア統合後、再度アクセス権を付与してAmazonへのAmazon販売チャネル接続を更新するように毎年求められます。 この認証は、Seller Centralアカウントの&#x200B;**設定** / **ユーザー権限**&#x200B;ページの&#x200B;_Amazon MWS Developer Permissions_&#x200B;セクションの&#x200B;_Current Authorizations_&#x200B;テーブルで更新または取り消しできます。

## Amazonストアの追加

1. _管理_&#x200B;サイドバーで、**マーケティング** / _チャネル_ / **AmazonSales Channel**&#x200B;に移動します。

   最初のAmazonセールスチャネルストアを追加すると、「_事前設定タスク_」モーダルが表示されます。 最初のストアを追加したら、左側のメニューの&#x200B;_Learning and Preparation_&#x200B;の下にある[Amazonのセールスチャネルホーム](./amazon-sales-channel-home.md)ページで、事前設定タスクにアクセスできます。

1. **[!UICONTROL Add Amazon Store]**&#x200B;をクリックします。

   _[!UICONTROL Add Amazon sales channel]_ページが開きます。

   ![Amazon販売チャネルストアの追加](assets/amazon-store-integration.png)

1. **[!UICONTROL Magento Website to use for Amazon Listing]**&#x200B;の場合、このAmazonセールスチャネルストアに接続する[!DNL Commerce] Webサイトを選択します。

   この設定は、[Amazonの注文](./order-settings.md)をインポートする際のデフォルトの[!DNL Commerce]ストアも定義します。

1. **[!UICONTROL Email Address]**&#x200B;の場合は、希望する連絡先の電子メールアドレスを入力します。

1. **[!UICONTROL New Store Name]**&#x200B;には、新しいAmazonセールスチャネルストアを説明する名前を入力します。

   >[!NOTE]
   >
   >この名前は、[!DNL Commerce]参照としてのみ使用され、[Amazon販売チャネルのホーム](./amazon-sales-channel-home.md)ページで店舗を識別します。 チームが簡単に識別できるようにしたい。 例えば、米国の地域で販売しているAmazonのストアには、`Amazon Store USA`という名前を付けることができます。

1. **[!UICONTROL Amazon Marketplace Country]**&#x200B;の場合は、このAmazonセールスチャネルストアで製品を販売する地域/国を選択します。 オプション：

   - 米国
   - カナダ
   - メキシコ
   - 英国

1. _[!UICONTROL Map your Magento attributes to Amazon]_セクションで、次の操作を行います。

   - **[!UICONTROL Product ID on the Amazon market]**&#x200B;の場合は、Amazon属性を選択して、下で選択した[!DNL Commerce]属性にマップします。

      このIDは、[!DNL Commerce]カタログ内の対応する製品を正しく照合するのに役立ちます。

   - **[!UICONTROL Map a Magento attribute]**&#x200B;の場合は、[!DNL Commerce]製品属性を選択して、上で選択したAmazon属性にマッピングします。

      [アトリビュ](./ob-creating-magento-attributes.md) ートシェルプのマッピングにより、Amazonのリストがカタログ内の対応する製品と正しく一致するように [!DNL Commerce] なります。

1. **[!UICONTROL Connect]**&#x200B;をクリックします。

   ダイアログが閉じ、確認メッセージが表示され、[Amazonの販売チャネルホーム](./amazon-sales-channel-home.md)ページに新しいストアが表示されます。

## ストアを[!DNL Amazon Seller Central]に接続します。

1. ストアダッシュボードで、ストアカードの&#x200B;**[!UICONTROL Connect store]**&#x200B;をクリックし、新しいタブで[!DNL Amazon Seller Central]を起動します。

1. [!DNL Amazon Seller Central]アカウントの資格情報を入力し、「**[!UICONTROL Sign in]**」をクリックします。

   この接続を完了するには、プライマリユーザーのログイン資格情報（販売者アカウントの作成に使用する電子メールまたは電話）を使用して[!DNL Amazon Seller Central]アカウントにサインインする必要があります。

1. プロンプトが表示されたら、Amazonから受け取ったコードを入力してAmazon Two-Factor Authorization(2FA)を完了し、「**[!UICONTROL Sign in]**」をクリックします。

1. _[!UICONTROL Amazon Marketplace Web Service]_確認ページで、「[!UICONTROL I understand...]」チェックボックスを選択し、「**[!UICONTROL Next]**」をクリックします。

1. _[!UICONTROL You are almost done]_メッセージで、「**[!UICONTROL Continue]**」をクリックします。

   [!DNL Amazon Seller Central]アカウントにデータにアクセスして共有するためのAmazon販売チャネル権限が付与されています。 Amazonページが閉じ、確認メッセージが表示されます。

   [Amazon販売チャネルホーム](./amazon-sales-channel-home.md)ページが開き、Amazonストアカードが表示されます。

   ストアダッシュボードを表示するには、ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

![Amazonの新しい店舗カード付き販売チャネルホーム](assets/asc-dashboard-after-2fa.png)

これで、新しいAmazonセールスチャネルストアが[!DNL Amazon Seller Central]アカウントに接続されました。

![次のア](assets/btn-next.png) [**イコン「リストルールの作成を続行」**](./ob-create-listing-rule.md)
