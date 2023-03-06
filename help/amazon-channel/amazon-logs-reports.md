---
title: ログとストアレポート
description: ログとストアのレポートを使用して、Adobe CommerceまたはMagento Open SourceストアとAmazon Marketplace のリストで発生していることを確認します。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# ログとストアレポート

Amazonセールスチャネル拡張機能には、Amazonの一覧や注文に影響を与えている変更を表示できる、いくつかの有用なログと保存レポートが含まれています。 これらのレポートを使用して、ストアでの出来事を確認し、様々なリストのステータスを理解できます。

レビュー専用の機能なので、ログやストアレポートで使用できるアクションはありません。

次のログは、 [ストアダッシュボード](./amazon-store-dashboard.md).

- この [変更ログのリスト](./listing-changes-log.md) Amazonのセールスアカウントに加えられた変更を、Amazonのセールスチャネル設定を反映したものとして表示します。

- この [通信エラーログ](./communication-errors-log.md) Amazonで報告された通信エラーを表示します。

次のストア固有のレポートは、 [ストアダッシュボード](./amazon-store-dashboard.md).

- この [競合価格の分析](./competitive-price-analysis.md) レポートには、Amazon _上陸価格_ （上場価格+送料） [Buy Box](./buy-box-competitor-pricing.md) 価格と [最も低い競争相手](./lowest-competitor-pricing.md) 価格。

- この [リストの改善点](./listing-improvements.md) レポートには、選択したストアに対してAmazonが提供する推奨リストの改善点がすべて表示されます。

>[!TIP]
>
>トラブルシューティングが必要な場合は、ログファイルで詳細を確認することもできます。 詳しくは、 [セールスチャネル管理者設定](./sales-channel-settings.md). Amazonセールスチャネル同期ログは、 `{Commerce Root}/var/log/channel_amazon.log` ファイルに保存し、 [開発者モード](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}.
