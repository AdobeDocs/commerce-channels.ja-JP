---
title: 販売チャネルの設定
description: Amazon sales channel 機能のログ、cron ソース、同期を管理するには、Commerce設定を更新します。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# 販売チャネルの設定

[!DNL Amazon Sales Channel] 拡張機能がインストールされると、管理者のAmazon Sales Channel にデフォルト値が設定されます。 これらの設定は、Amazon ストアの設定で変更できます。 以下の設定が含まれます。

- アクティビティログ履歴をクリアする間隔
- Cron ソースの選択
- ログ同期オプション

## Commerce チャネルの設定を変更する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales Channels]**」を展開し、「**[!UICONTROL Global Settings]**」を選択します。

1. **[!UICONTROL Clear Log History]** の場合は、次のいずれかのオプションを選択します。

   - `Once Daily` - 1 日に 1 回のストアアクティビティ履歴をクリアすることを選択します。

   - `Once Weekly` – 毎週 1 回のストアアクティビティ履歴をクリアすることを選択します。

   - `Once Monthly` - （デフォルト）月に 1 回のストアアクティビティ履歴をクリアすることを選択します。

1. **[!UICONTROL Background Tasks (CRON) Source]** の場合は、「`Magento CRON`」を選択します。

   このオプションを使用すると、Amazonのセールスチャネルで [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 設定を使用して、[!DNL Amazon Seller Central] との通信およびデータ同期間隔を決定できます。

1. **[!UICONTROL Enable Debug Logging]** しくは、トラブルシューティングが必要な場合に追加の同期データを収集する `Enabled` を選択します。

   Amazon sales channel のログは、`{Commerce Root}/var/log/channel_amazon.log` ファイルに書き込まれ、[developer mode](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes) で表示できます。 ログは、トラブルシューティング中にのみ `Enabled` 示し、トラブルシューティングが完了したら `Disabled` 示する必要があります。

1. **[!UICONTROL Read-Only Mode]** の場合、`Enabled` を選択して、送信されるすべての状態変更 API リクエストをブロックします。

   この設定では、変更が保存されますが、無効になるまで送信さ [!UICONTROL Read-Only Mode] ません。 読み取り専用モードを有効にするには、構成キャッシュをクリアする必要があります。 データ転送を再度開始するには、「`Disabled`」を選択します。

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] は、ステージングや QA などの実稼動インスタンスのコピー用に設計されているので、実稼動インスタンスでは使用しないでください。
   >
   >データベースがインスタンスの新しいコピーに移行されると（設定でストアの URL が変更されたときに検出）、[!UICONTROL Read-Only Mode] が自動的に有効になります。

1. 「**[!UICONTROL Save Config]**」をクリックします。

![Sales Channel設定 ](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
