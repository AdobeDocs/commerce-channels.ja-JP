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

Amazonのセールスチャネルにアクセスする際に、[!DNL Commerce] はストア設定に追加したAmazon API キーを自動的にチェックし、検証します。 検証された場合は、次の手順 [ ストアの統合 ](./store-integration.md) に進むことができます。

Amazon API キーがない、無効または期限切れの場合は、キーを更新する必要があります。 API キーを取得し、それらのキーをAmazon Sales Channel 設定に追加するよう促すメッセージが表示されます。

## 取得し、プロンプトが表示されたらAmazon API キーを追加します

API キーは、Amazonのセールスチャネルにアクセスするたびに検証されます。

1. [!DNL Commerce] Admin にログインします。

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]** に移動します。

   Amazonのセールスチャネルに初めてアクセスする場合、または API キーの更新が必要な場合は、プロセスを進めるように求められます。

   ![Amazon API キープロンプトの取得と追加 ](assets/amazon-api-verification-prompt.png){width="500"}

1. 「**[!UICONTROL Sign in]**」をクリックして、[!DNL Commerce] web アカウントにアクセスします。

   Commerce アカウントページが新しいブラウザータブで開きます。

   - [!DNL Commerce] アカウントにログインしている場合は、_[!UICONTROL My Account]_ページの_[!UICONTROL API Portal]_ セクションが自動的に表示されます。

   - ログインしていない場合は、「_[!UICONTROL API Portal]_」タブが表示される前に、[!DNL Commerce] アカウントのユーザー名とパスワードの入力を求められます。

   - アカウントをお持ちでない場合は、[ アカウントページ  [!DNL Commerce]  にアクセスし ](https://account.magento.com/customer/account/login/){target="_blank"} 登録してください。 このアカウントは、会社またはビジネスの一部である必要があります。

1. 必要に応じて、[!DNL Commerce] アカウントの「_[!UICONTROL API Portal]_」タブで API キーを表示および生成できます。

   API キーを作成するには、`Amazon Sales Channel` のような説明を入力し、「**[!UICONTROL Add New]**」をクリックします。 新しいキーが生成され、入力した名前で表示されます。 「**[!UICONTROL Copy]**」をクリックして、新しいキーをコピーします。

   ![API キーの生成またはコピー ](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. 生成およびコピーされた新しいキーを使用して、ブラウザーの「_[!UICONTROL Amazon Sales Channel]_」タブに戻ります。

1. _[!UICONTROL Welcome to Amazon Sales Channel]_ページで「**[!UICONTROL Add the key]**」をクリックします。

   ブラウザーがAmazon sales channel を終了し、ストア設定ページが [!DNL Commerce] Admin の「_[!UICONTROL Api Keys]_」ページを開きます。 このページは、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_ / **[!UICONTROL Configuration]** に移動し、左側のパネルで「**[!UICONTROL Services]**」を展開して「**[!UICONTROL Magento Services]**」を選択すると、手動で開くことができます。

1. コピーしたキーを **[!UICONTROL Production Api key]** に貼り付けます。

1. 「**[!UICONTROL Save Config]**」をクリックします。 これで、Amazonのセールスチャネルに戻ることができます。

   ![ ストア設定への API キーの追加 ](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]** に移動します。

   Amazonのセールスチャネルトリガー[!DNL Commerce] 再アクセスして、API キーを検証および検証し、続行できるようにします。

   キーをもう一度確認するように求めるプロンプトが表示されたら、この _追加と確認_ の手順を繰り返します。

![ 次へアイコン ](assets/btn-next.png)[**ストア統合を続行**](./store-integration.md)
