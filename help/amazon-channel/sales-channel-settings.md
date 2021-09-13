---
title: Sales Channel設定
description: Amazonの販売チャネル機能のログ、クロンソース、同期を管理するには、コマース設定を更新します。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Sales Channel設定

[!DNL Amazon Sales Channel]拡張機能をインストールすると、Amazonの販売チャネルの管理者にデフォルト値が設定されます。 これらの設定は、Amazonストアの設定で変更できます。 次の設定が含まれます。

- アクティビティログ履歴をクリアする間隔
- Cronソースの選択
- ログ同期オプション

## コマースチャネル設定の変更

1. _管理_&#x200B;サイドバーで、**[!UICONTROL Stores]** / _[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで&#x200B;**[!UICONTROL Sales Channels]**&#x200B;を展開し、「**[!UICONTROL Global Settings]**」を選択します。

1. **[!UICONTROL Clear Log History]**&#x200B;の場合は、次のオプションを選択します。

   - `Once Daily`  — ストアアクティビティの履歴を1日に1回クリアするように選択します。

   - `Once Weekly`  — 週に1回ストアアクティビティ履歴をクリアするように選択します。

   - `Once Monthly` - （デフォルト）ストアアクティビティ履歴を毎月1回クリアするように選択します。

1. **[!UICONTROL Background Tasks (CRON) Source]**&#x200B;の場合は、`Magento CRON`を選択します。

   このオプションを使用すると、Amazonの販売チャネルで[!DNL Commerce] [Cron](https://docs.magento.com/user-guide/system/cron.html)設定を使用して、[!DNL Amazon Seller Central]との通信とデータ同期の間隔を決定できます。

1. **[!UICONTROL Enable Debug Logging]**&#x200B;の場合は、`Enabled`を選択して、トラブルシューティングが必要な場合に追加の同期データを収集します。

   Amazonの販売チャネルのログは`{Commerce Root}/var/log/channel_amazon.log`ファイルに書き込まれ、[開発者モード](https://docs.magento.com/user-guide/magento/installation-modes.html){:target=&quot;_blank&quot;}で表示できます。 ログは、トラブルシューティング中に`Enabled`のみにし、トラブルシューティングが完了したら`Disabled`にする必要があります。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

![Sales Channel設定](assets/config-sales-channel-global-settings.png)
