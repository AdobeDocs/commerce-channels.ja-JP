---
title: ログとストアレポート
description: ログとストアのレポートを使用して、AdobeのコマースストアまたはMagento Open SourceストアとAmazon Marketplaceのリストで何が起きているかを確認します。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# ログとストアレポート

Amazonの販売チャネル拡張機能には、Amazonのリストや注文に影響を与えている変更を表示できる、いくつかの貴重なログと保存レポートが含まれています。 これらのレポートを使用して、ストアでの出来事を確認したり、様々なリストのステータスを理解したりできます。

レビュー専用の機能なので、ログやストアレポートに対して使用できるアクションはありません。

次のログは、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスできます。

- [変更ログ](./listing-changes-log.md)の一覧には、Amazonの販売チャネル設定を反映して、Amazonの販売者アカウントでおこなわれた変更が表示されます。

- [通信エラーログ](./communication-errors-log.md)には、Amazonで報告された通信エラーが表示されます。

次のストア固有のレポートは、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスできます。

- [Competitive Price Analysis](./competitive-price-analysis.md)レポートは、Amazon _Buy Box](./buy-box-competitor-pricing.md)価格と[競合相手](./lowest-competitor-pricing.md)価格に関して[ランディング価格_（リスト価格と出荷価格）を示します。

- [リストの改善](./listing-improvements.md)レポートには、選択したストアに対してAmazonが提供する推奨リストの改善点がすべて表示されます。

>[!TIP]
>
>トラブルシューティングが必要な場合は、ログファイルで追加情報を確認することもできます。 [販売チャネルの管理設定](./sales-channel-settings.md)を参照してください。 Amazonの販売チャネル同期ログは、`{Commerce Root}/var/log/channel_amazon.log`ファイルに書き込まれ、[開発者モード](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}で表示できます。
