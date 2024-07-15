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

次のログには、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスできます。

- [ 変更のリスト表示ログ ](./listing-changes-log.md) には、Amazonの販売チャネル設定の反映として、Amazonの販売者アカウントで発生した変更が表示されます。

- [ 通信エラーログ ](./communication-errors-log.md) には、Amazonで報告された通信エラーが表示されます。

次のストア固有のレポートは、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスできます。

- [ 競合価格分析 ](./competitive-price-analysis.md) レポートは、Amazonの _荷揚げ価格_ （上場価格に出荷価格を加えた価格）を [Buy Box](./buy-box-competitor-pricing.md) 価格および [ 最低競合製品 ](./lowest-competitor-pricing.md) 価格と比較して示します。

- [ リストの改善 ](./listing-improvements.md) レポートには、選択したストアに対してAmazonが提供する、すべての推奨リストの改善が表示されます。

>[!TIP]
>
>トラブルシューティングが必要な場合は、ログファイルで追加情報を確認することもできます。 [ 販売チャネル管理設定 ](./sales-channel-settings.md) を参照してください。 Amazon sales channel synchronization logging は `{Commerce Root}/var/log/channel_amazon.log` ファイルに書き込まれ、[developer mode](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes) で表示できます。
