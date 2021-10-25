---
title: レポートの記録と保存
description: 「ログ」および「保存」レポートを使用して、Adobe Commerce または Magento Open Source store および Amazon Marketplace の一覧で発生したことを確認します。
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# レポートの記録と保存

Amazon 販売チャンネルの拡張機能には、いくつかの重要なログが含まれています。また、レポートには、Amazon の一覧や注文に影響する変更を表示することができます。 これらのレポートを使用して、ストアで発生した内容を確認したり、様々な一覧状態を把握することができます。

ログまたは格納レポートはレビューのみの機能なので、操作を実行することはできません。

次のログには、ストアのダッシュボードからアクセスでき [ ](./amazon-store-dashboard.md) ます。

- 出展変更ログには、amazon [ ](./listing-changes-log.md) 販売チャンネル設定に反映された Amazon 売り手アカウントで発生した変更が表示されます。

- [通信エラーログには、 ](./communication-errors-log.md) Amazon に関する報告された通信エラーが記録されています。

ストアのダッシュボードからは、ストアに関する次のレポートにアクセスでき [ ](./amazon-store-dashboard.md) ます。

- [「競合製品に関する価格分析」レポートは、 ](./competitive-price-analysis.md) __ [ 購入ボックス ](./buy-box-competitor-pricing.md) 価格および競合企業の最低価格に基づいて、Amazon の支持価格 (出展価格と送料) が表示されることを示して [ ](./lowest-competitor-pricing.md) います。

- リストに記載された改善レポートには、 [ ](./listing-improvements.md) 選択したストアに対して Amazon によって提供される一覧の改善がすべて表示されます。

>[!TIP]
>
>トラブルシューティングが必要な場合は、ログファイルに追加情報があるかどうかを確認することもできます。 [販売チャンネル管理の設定 ](./sales-channel-settings.md) を参照してください。Amazon 販売チャンネルの同期ログがファイルに書き込まれ、 `{Commerce Root}/var/log/channel_amazon.log` [ 開発モードで表示でき ](https://docs.magento.com/user-guide/magento/installation-modes.html) ます {target = &quot;_blank&quot;}。
