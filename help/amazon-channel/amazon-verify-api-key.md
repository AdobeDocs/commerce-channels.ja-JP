---
title: Amazon API キーを追加または確認
description: Commerce設定で、検証済みのAmazon API キーを使用すると、ストアをAmazonの販売者アカウントに統合できます。
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Amazon API キーを追加または確認

Amazon Sales Channel にアクセスする場合、 [!DNL Commerce] ストア設定に追加したAmazon API キーを自動的にチェックし検証します。 検証済みの場合は、次の手順に進むことができます。 [ストアの統合](./store-integration.md).

Amazon API キーがない、無効または期限切れの場合は、キーを更新する必要があります。 API キーを取得し、それらのキーをAmazon Sales Channel 設定に追加するよう促すメッセージが表示されます。

## 取得し、プロンプトが表示されたらAmazon API キーを追加します

API キーは、Amazonのセールスチャネルにアクセスするたびに検証されます。

1. にログインします [!DNL Commerce] 管理者。

1. 日 _[!UICONTROL Admin]_サイドバー、に移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Amazonのセールスチャネルに初めてアクセスする場合、または API キーの更新が必要な場合は、プロセスを進めるように求められます。

   ![Amazon API キープロンプトを取得して追加します](assets/amazon-api-verification-prompt.png){width="500"}

1. クリック **[!UICONTROL Sign in]** にアクセスする [!DNL Commerce] web アカウント。

   Commerce アカウントページが新しいブラウザータブで開きます。

   - にログインしている場合 [!DNL Commerce] アカウント、 _[!UICONTROL API Portal]_の節_[!UICONTROL My Account]_ ページは自動的に表示されます。

   - ログインしていない場合は、を入力するよう求められます [!DNL Commerce] 次の前のアカウントのユーザー名とパスワード _[!UICONTROL API Portal]_タブが表示されます。

   - アカウントをお持ちでない場合は、 [この [!DNL Commerce] アカウントページ](https://account.magento.com/customer/account/login/){target="_blank"} と登録。 このアカウントは、会社またはビジネスの一部である必要があります。

1. 必要に応じて、API キーを表示および生成できます _[!UICONTROL API Portal]_タブ [!DNL Commerce] アカウント。

   API キーを作成するには、のような説明を入力します。 `Amazon Sales Channel` をクリックして、 **[!UICONTROL Add New]**. 新しいキーが生成され、入力した名前で表示されます。 クリック **[!UICONTROL Copy]** 新しいキーをコピーします。

   ![API キーの生成またはコピー](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. 生成およびコピーされた新しいキーを使用して、に戻ります。 _[!UICONTROL Amazon Sales Channel]_ブラウザーで tab キーを押します。

1. 日 _[!UICONTROL Welcome to Amazon Sales Channel]_ページ、クリック&#x200B;**[!UICONTROL Add the key]**.

   ブラウザーがAmazon sales channel を終了し、「store configuration」ページが開きます。 _[!UICONTROL Api Keys]_内のページ [!DNL Commerce] 管理者。 に移動したときに、このページを手動で開くことができます。**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**、を展開 **[!UICONTROL Services]** 左パネルで、を選択します。 **[!UICONTROL Magento Services]**.

1. コピーしたキーを貼り付けます **[!UICONTROL Production Api key]**.

1. クリック **[!UICONTROL Save Config]**. これで、Amazonのセールスチャネルに戻ることができます。

   ![ストア設定への API キーの追加](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. 日 _[!UICONTROL Admin]_サイドバー、に移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Amazonのセールスチャネルトリガーへの再アクセス [!DNL Commerce] api キーを検証および検証し、続行できるようにします。

   キーをもう一度確認するように求めるメッセージが表示された場合は、この手順を繰り返します _追加と検証_ プロセス。

![次へアイコン](assets/btn-next.png) [**ストア統合の続行**](./store-integration.md)
