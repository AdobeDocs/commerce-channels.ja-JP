---
title: Amazon API キーの追加または検証
description: コマース設定では、検証済みのAmazon API キーを使用して、ストアをAmazonセラーアカウントと統合できます。
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Amazon API キーの追加または検証

Amazonセールスチャネルにアクセスする場合、 [!DNL Commerce] は、ストア設定に追加したAmazon API キーを自動的に確認して検証します。 検証された場合は、次の手順に進むことができます。 [ストア統合](./store-integration.md).

Amazon API キーが見つからない、無効な、または期限切れの場合は、キーを更新する必要があります。 API キーを取得し、それらのキーをAmazon Sales Channel 設定に追加するよう求めるメッセージが表示されます。

## プロンプトに従ってAmazon API キーを取得し、追加します

API キーは、Amazonセールスチャネルにアクセスするたびに検証されます。

1. にログインします。 [!DNL Commerce] 管理者。

1. の _[!UICONTROL Admin]_サイドバー、移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Amazonセールスチャネルに初めてアクセスする場合、または API キーで更新が必要な場合は、プロセスを完了するよう求めるメッセージが表示されます。

   ![Amazon API キープロンプトの取得と追加](assets/amazon-api-verification-prompt.png){width="500"}

1. クリック **[!UICONTROL Sign in]** をクリックし、 [!DNL Commerce] Web アカウント。

   新しいブラウザータブにコマースアカウントページが開きます。

   - 次にログインした場合、 [!DNL Commerce] アカウント、 _[!UICONTROL API Portal]_セクション_[!UICONTROL My Account]_ ページが自動的に表示されます。

   - ログインしていない場合は、 [!DNL Commerce] アカウントのユーザー名とパスワード（前） _[!UICONTROL API Portal]_」タブが表示されます。

   - アカウントがない場合は、 [の [!DNL Commerce] アカウントページ](https://account.magento.com/customer/account/login/){target="_blank"} と登録。 このアカウントは、会社またはビジネスに含まれる必要があります。

1. 必要に応じて、 _[!UICONTROL API Portal]_」タブをクリックします。 [!DNL Commerce] アカウント

   API キーを作成するには、 `Amazon Sales Channel` をクリックし、 **[!UICONTROL Add New]**. 新しいキーが生成され、入力した名前で表示されます。 クリック **[!UICONTROL Copy]** をクリックして、新しいキーをコピーします。

   ![API キーを生成またはコピーする](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. 新しいキーが生成され、コピーされた状態で、に戻ります。 _[!UICONTROL Amazon Sales Channel]_」タブをクリックします。

1. の _[!UICONTROL Welcome to Amazon Sales Channel]_ページ、クリック&#x200B;**[!UICONTROL Add the key]**.

   ブラウザーがAmazonセールスチャネルを終了し、ストア設定ページで _[!UICONTROL Api Keys]_ページの [!DNL Commerce] 管理者。 このページは、**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**、展開 **[!UICONTROL Services]** を選択し、 **[!UICONTROL Magento Services]**.

1. コピーしたキーをに貼り付けます。 **[!UICONTROL Production Api key]**.

1. クリック **[!UICONTROL Save Config]**. これで、Amazonセールスチャネルに戻ることができます。

   ![ストア設定への API キーの追加](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. の _[!UICONTROL Admin]_サイドバー、移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Amazonセールスチャネルトリガーへの再アクセス [!DNL Commerce] API キーを確認および検証し、続行できるようにします。

   キーの確認を再度求められた場合は、この操作を繰り返します。 _追加と検証_ プロセス。

![次のアイコン](assets/btn-next.png) [**ストア統合を続行**](./store-integration.md)
