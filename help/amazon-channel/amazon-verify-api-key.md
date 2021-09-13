---
title: Amazon APIキーの追加または検証
description: コマース設定では、検証済みのAmazon APIキーを使用して、ストアをAmazonセラーアカウントと統合できます。
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Amazon APIキーの追加または検証

Amazonの販売チャネルにアクセスする場合、[!DNL Commerce]はストア設定に追加したAmazon APIキーを自動的に確認し、検証します。 検証済みの場合は、次の手順([Store Integration](./store-integration.md))に進むことができます。

Amazon APIキーが見つからない、無効な、または期限切れの場合は、キーを更新する必要があります。 APIキーを取得し、Amazon Sales Channel設定に追加するよう求めるメッセージが表示されます。

## プロンプトに従ってAmazon APIキーを取得し、追加します。

APIキーは、Amazon Salesチャネルにアクセスするたびに検証されます。

1. [!DNL Commerce]管理にログインします。

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**&#x200B;に移動します。

   Amazonの販売チャネルに初めてアクセスする場合、またはAPIキーを更新する必要がある場合は、プロセスを実行するよう求めるプロンプトが表示されます。

   ![Amazon APIキープロンプトの取得と追加](assets/amazon-api-verification-prompt.png)

1. **[!UICONTROL Sign in]**&#x200B;をクリックして、[!DNL Commerce] Webアカウントにアクセスします。

   新しいブラウザータブでコマースアカウントページが開きます。

   - [!DNL Commerce]アカウントにログインすると、_[!UICONTROL My Account]_ページの_[!UICONTROL API Portal]_&#x200B;セクションが自動的に表示されます。

   - ログインしていない場合は、「_[!UICONTROL API Portal]_」タブを表示する前に、[!DNL Commerce]アカウントのユーザー名とパスワードを入力するよう求められます。

   - アカウントがない場合は、[ [!DNL Commerce] アカウントページ](https://account.magento.com/customer/account/login/){target=&quot;_blank&quot;}にアクセスし、登録します。 このアカウントは、会社またはビジネスの一部にする必要があります。

1. 必要に応じて、[!DNL Commerce]アカウントの「_[!UICONTROL API Portal]_」タブでAPIキーを表示および生成できます。

   APIキーを作成するには、`Amazon Sales Channel`のような説明を入力し、**[!UICONTROL Add New]**&#x200B;をクリックします。 新しいキーが生成され、入力した名前で表示されます。 **[!UICONTROL Copy]**&#x200B;をクリックして、新しいキーをコピーします。

   ![APIキーの生成またはコピー](assets/amazon-add-api-key.png)

1. 新しいキーが生成され、コピーされた状態で、ブラウザーの「_[!UICONTROL Amazon Sales Channel]_」タブに戻ります。

1. _[!UICONTROL Welcome to Amazon Sales Channel]_ページで、「**[!UICONTROL Add the key]**」をクリックします。

   ブラウザーがAmazonの販売チャネルを終了し、ストア設定ページで[!DNL Commerce]管理者の&#x200B;_[!UICONTROL Api Keys]_ページが開きます。**[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**&#x200B;に移動し、左側のパネルで&#x200B;**[!UICONTROL Services]**&#x200B;を展開して、「**[!UICONTROL Magento Services]**」を選択すると、このページを手動で開くことができます。

1. コピーしたキーを&#x200B;**[!UICONTROL Production Api key]**&#x200B;に貼り付けます。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。 これで、Amazonの販売チャネルに戻ることができます。

   ![ストア設定へのAPIキーの追加](assets/config-magento-services-api-screen.png)

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**&#x200B;に移動します。

   Amazon販売チャネルトリガー[!DNL Commerce]への再アクセスAPIキーの確認と検証を行い、続行できます。

   キーの検証を再度求められた場合は、_Add and Verify_&#x200B;プロセスを繰り返します。

![次の](assets/btn-next.png) [**アイコン「統合を保存を続行」**](./store-integration.md)
