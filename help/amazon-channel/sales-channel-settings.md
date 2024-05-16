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

いつ [!DNL Amazon Sales Channel] 拡張機能がインストールされ、Amazon セールスチャネルの管理者でデフォルト値が設定されます。 これらの設定は、Amazon ストアの設定で変更できます。 以下の設定が含まれます。

- アクティビティログ履歴をクリアする間隔
- Cron ソースの選択
- ログ同期オプション

## Commerce チャネルの設定を変更する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales Channels]** を選択します **[!UICONTROL Global Settings]**.

1. の場合 **[!UICONTROL Clear Log History]**、次のいずれかのオプションを選択します。

   - `Once Daily` - 1 日に 1 回、ストアのアクティビティ履歴を消去することを選択します。

   - `Once Weekly`  – 毎週 1 回ストアのアクティビティ履歴をクリアすることを選択します。

   - `Once Monthly` - （デフォルト）月に 1 回のストアアクティビティ履歴をクリアすることを選択します。

1. の場合 **[!UICONTROL Background Tasks (CRON) Source]**、を選択 `Magento CRON`.

   このオプションを選択すると、Amazon セールスチャネルで [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) との通信およびデータ同期間隔を決定するための設定 [!DNL Amazon Seller Central].

1. の場合 **[!UICONTROL Enable Debug Logging]**、を選択 `Enabled` トラブルシューティングが必要な場合に追加の同期データを収集します。

   Amazon sales channel logging は、 `{Commerce Root}/var/log/channel_amazon.log` ファイルおよび次で表示できます [開発者モード](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). ログは、次の値のみにする必要があります `Enabled` トラブルシューティング中は、以下を行う必要があります `Disabled` トラブルシューティングが完了したとき。

1. の場合 **[!UICONTROL Read-Only Mode]**&#x200B;を選択 `Enabled` 送信されるすべての状態変更 API リクエストをブロックします。

   この設定では、潜在的な変更は保存されますが、次まで送信されません： [!UICONTROL Read-Only Mode] が無効になっています。 読み取り専用モードを有効にするには、構成キャッシュをクリアする必要があります。 データ転送を再度開始するには、次を選択します `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] は、ステージングや QA などの実稼動インスタンスのコピー用に設計されているので、実稼動インスタンスでは使用しないでください。
   >
   >データベースがインスタンスの新しいコピーに移行されると（設定でストアの URL が変更されたときに検出されます）、 [!UICONTROL Read-Only Mode] が自動的に有効になります。

1. クリック **[!UICONTROL Save Config]**.

![Sales Channelの設定](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
