---
title: セールスチャネル設定
description: Amazonセールスチャネル機能のログ、クローンソース、同期を管理するには、Commerce 設定を更新します。
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# セールスチャネル設定

次の場合に [!DNL Amazon Sales Channel] 拡張機能がインストールされている場合、デフォルト値は「 Amazonの管理」セールスチャネルに設定されます。 これらの設定は、Amazonストアの設定で変更できます。 以下の設定が含まれます。

- アクティビティログ履歴をクリアする間隔
- Cron ソースの選択
- ログ同期オプション

## コマースチャネル設定の変更

1. の _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales Channels]** を選択します。 **[!UICONTROL Global Settings]**.

1. の場合 **[!UICONTROL Clear Log History]**、オプションを選択します。

   - `Once Daily`  — 毎日 1 回ストアアクティビティの履歴をクリアするように選択します。

   - `Once Weekly`  — 毎週 1 回ストアアクティビティ履歴をクリアするように選択します。

   - `Once Monthly` - （デフォルト）毎月 1 回、ストアアクティビティ履歴をクリアするように選択します。

1. の場合 **[!UICONTROL Background Tasks (CRON) Source]**&#x200B;選択 `Magento CRON`.

   このオプションを使用すると、Amazonのセールスチャネルで [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 通信間隔とデータ同期間隔を [!DNL Amazon Seller Central].

1. の場合 **[!UICONTROL Enable Debug Logging]**&#x200B;選択 `Enabled` トラブルシューティングが必要な場合に、追加の同期データを収集する。

   Amazonセールスチャネルのログは、 `{Commerce Root}/var/log/channel_amazon.log` ファイルに保存し、 [開発者モード](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). ログは次の場合にのみ実行します `Enabled` トラブルシューティング中に、 `Disabled` トラブルシューティングが完了したら、

1. の場合 **[!UICONTROL Read-Only Mode]**&#x200B;を選択します。 `Enabled` をクリックして、送信状態が変化するすべての API リクエストをブロックします。

   この設定を使用すると、潜在的な変更は保存されますが、送信されなくなります。 [!UICONTROL Read-Only Mode] は無効です。 読み取り専用モードを有効にするには、設定キャッシュをクリアする必要があります。 データ転送を再度開始するには、 `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] は、ステージングや QA など、実稼動インスタンスのコピー用に設計されており、実稼動インスタンスでは使用しないでください。
   >
   >データベースがインスタンスの新しいコピーに移行された場合（ストアの URL が設定内で変更された場合に検出されます）、 [!UICONTROL Read-Only Mode] は自動的に有効になります。

1. クリック **[!UICONTROL Save Config]**.

![Sales Channel設定](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
