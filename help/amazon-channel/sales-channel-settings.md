---
title: 販売チャンネル設定
description: ログ、cron ソース、および Amazon 販売チャンネル機能の同期を管理するには、Commerce の設定を更新します。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 販売チャンネル設定

[!DNL Amazon Sales Channel]拡張機能がインストールされている場合は、Amazon sales チャンネルの管理にデフォルト値が設定されます。これらの設定は、Amazon store の設定によって変更されることがあります。 次のような設定があります。

- アクティビティログ履歴を消去する間隔
- Cron ソースの選択
- ログ同期オプション

## Commerce チャネルの設定を変更します。

1. _管理者は_ 、> > を参照して **[!UICONTROL Stores]** _[!UICONTROL Settings]_**[!UICONTROL Configuration]**ください。

1. 左側のパネルで、を展開し、を **[!UICONTROL Sales Channels]** 選択し **[!UICONTROL Global Settings]** ます。

1. **[!UICONTROL Clear Log History]**&#x200B;で、次のいずれかのオプションを選択します。

   - `Once Daily` -ストアの利用状況の履歴を1日に1回削除する場合に選択します。

   - `Once Weekly` -1 週間に1回、ストアの利用状況の履歴を消去する場合に選択します。

   - `Once Monthly` -(デフォルト) 毎月保存するアクティビティの履歴を削除します。

1. について **[!UICONTROL Background Tasks (CRON) Source]** は、を選択 `Magento CRON` します。

   このオプションを使用すると、Amazon 販売チャンネルの Cron 設定を使用して、 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/system/cron.html) の通信およびデータ同期の間隔を指定することができ [!DNL Amazon Seller Central] ます。

1. について **[!UICONTROL Enable Debug Logging]** `Enabled` は、トラブルシューティングが必要なときに、追加の同期データを収集するように選択します。

   Amazon 販売チャンネルのログ出力がファイルに書き込まれ、 `{Commerce Root}/var/log/channel_amazon.log` [ 開発モード ](https://docs.magento.com/user-guide/magento/installation-modes.html) {target = &quot;_blank&quot;} で表示できるようになります。 ログは `Enabled` トラブルシューティングの際にのみ実行し、 `Disabled` トラブルシューティングが完了したら実行する必要があります。

1. をクリックし **[!UICONTROL Save Config]** ます。

![販売チャンネルの設定](assets/config-sales-channel-global-settings.png)
