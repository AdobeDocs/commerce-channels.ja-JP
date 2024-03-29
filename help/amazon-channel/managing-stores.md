---
title: '"[!UICONTROL Amazon Stores] 表示»'
description: Amazonストアビューに移動して、各Amazonストアの基本統計をすばやく確認し、管理オプションにアクセスします。
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores] 表示

Amazonセールスチャネルのホームページを表示した場合、 _Amazon Stores_ デフォルトでは、ビューが開きます。

![Amazonストア表示](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

The _[!UICONTROL Amazon Stores]_ビューには、Amazonの各ストアの「ストアカード」と、いくつかの基本的な統計および管理オプションが表示されます。 各カードに表示される概要情報には、各店舗ステータス、作成日、最終更新日、注意が必要なリスト（例：不完全なリスト）、割り当てられた [!DNL Commerce] web サイト。

次を表示する場合： _[!UICONTROL Amazon Store]_各ストアカードでは、次の操作を実行できます。

- ストアを開くには [dashboard](./amazon-store-dashboard.md)をクリックし、 **[!UICONTROL View Store]**.

- ストアのステータスを変更したり、ストアを削除するには、 **[!UICONTROL Action]** 次を選択します。

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]**  — ストアのステータスを次に変更する場合に選択します `Active` または `Inactive`、それぞれ。

     の変更 `Inactive` 保存先 `Active` status は、店舗の現在の店舗設定（一覧設定、価格ルール、上書きなど）を使用して、店舗の一覧と注文アクティビティを有効化します。

     ストアステータスの変更元： `Active` から `Inactive` ステータスはストアのリストと注文アクティビティを中断します。 非アクティブなストアは、すべてのストア設定とリストを保持しますが、ストアがに変更されるまで、価格、数量、注文管理の同期を一時的に停止します。 `Active` ステータス。 この機能を使用すると、Amazonストアを再作成または再統合したり、過去の注文や販売データを失うことなく、地域レベルでストアアクティビティを制御できます。

   - **[!UICONTROL Delete]**  — 不要になったストアを削除するように選択します。

     既存のAmazonストアと、 [!DNL Amazon Seller Central] アカウント。 アカウントを削除すると、Amazonのセールスチャネルからストアが削除され、アカウントの設定、リスト、ログ、およびこのストアに関連するその他の情報もすべて削除されます。 削除後にストアを取得できません。新しいストアを作成する必要があります。

>[!NOTE]
>統合時にストアに割り当てられた Web サイトを変更するには、ストアを削除し、ストア統合時に定義された別の Web サイトを使用してストアを再び追加する必要があります。

| ストアカード | 説明 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 上部セクション | 次を含む： <br>ストアの地域アイコン ( [ストア統合](./store-integration.md).<br> 割り当てられた _[!UICONTROL Magento Website]_：ストアの統合中に定義されます。<br>The_[!UICONTROL Status]_ お客様のストアの オプション： **[!UICONTROL Active]**  — ストアの統合が完了し、Amazonで検証済みで、販売活動に使用できます。 **[!UICONTROL Inactive]**  — ストアの統合が完了しましたが、使用されていないか、セールス活動に使用できません。 条件 `Inactive`に設定しない場合、Amazonの販売は一時停止されています。 条件 `Active`有効化する前に更新するために、売上高と追加の設定が保存されます。<br>The *[!UICONTROL Last Updated]* Amazonストアの設定に対する最新の変更の日付。<br>The *[!UICONTROL Created]* AmazonセールスチャネルにAmazonストアが作成された日付。 |
| 中央のセクション | 過去 30 日間の店舗アクティビティの概要グラフが含まれ、注意が必要なリストに対するおよびアラートが含まれます。 |
| 下部セクション | 「ビューストア」および「アクション」オプションが含まれます。<br>ストアを開くには [dashboard](./amazon-store-dashboard.md)をクリックし、 **[!UICONTROL View Store]**.<br>ストアをアクティベート、アクティベート解除、または削除するには、 **[!UICONTROL Actions]**. |
