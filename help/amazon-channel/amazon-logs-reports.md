---
title: Amazon リストのログとストアレポート
description: ログとストアレポートを使用すると、Adobe CommerceまたはMagento Open SourceストアとAmazon Marketplace のリストで何が起きているかを確認できます。
feature: Sales Channels, Logs
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Amazon リストのログとストアレポート

Amazon sales channel 拡張機能には、Amazonのリストや注文に影響を与える変更を確認できる、貴重なログやストアレポートがいくつか含まれています。 これらのレポートを使用すると、ストアで何が起きているかを確認したり、様々なリストのステータスを把握したりできます。

ログまたはストアレポートはレビュー専用の機能なので、これらのアクションは使用できません。

次のログには、 [ストアダッシュボード](./amazon-store-dashboard.md).

- この [変更ログの一覧表示](./listing-changes-log.md) Amazonの販売チャネル設定の反映として、Amazonの販売者アカウントで発生した変更を示します。

- この [通信エラーログ](./communication-errors-log.md) Amazonで報告された通信エラーを表示します。

次のストア固有のレポートには、 [ストアダッシュボード](./amazon-store-dashboard.md).

- この [競争価格分析](./competitive-price-analysis.md) レポートにAmazonが表示される _地価_ （上場価格+出荷価格）に係るもの [Buy Box](./buy-box-competitor-pricing.md) 価格および [競合他社の最低値](./lowest-competitor-pricing.md) 価格。

- この [リストの改善](./listing-improvements.md) レポートには、選択したストアに対してAmazonによって提供された提案リストの改善点がすべて表示されます。

>[!TIP]
>
>トラブルシューティングが必要な場合は、ログファイルで追加情報を確認することもできます。 参照： [販売チャネル管理設定](./sales-channel-settings.md). Amazon sales channel synchronization logging は、 `{Commerce Root}/var/log/channel_amazon.log` ファイルおよび次で表示できます [開発者モード](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
