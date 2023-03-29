---
title: '''[!DNL Channel Manager] リリースノート`'
description: の最新のリリース情報 [!DNL Channel Manager] Adobe Commerceから
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: d3acde7aa297ba33dffa7854aa7578985ad12c9b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Channel Manager] リリースノート

以下のリリースノートでは、 [!DNL Channel Manager] およびを含めます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題


## v2.0.0

*2023 年 3 月 21 日*

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![新規](../assets/new.svg)<!--CHAN-5893--> Channel Manager は、Adobe Commerceバージョン 2.4.6 と互換性があります。

## v1.1.0

*2022 年 11 月 24 日*

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![新規](../assets/new.svg)<!--CHAN-5204--> **返品と返金**—Adobe CommerceとMagento Open Source・チャネル・マネージャーのストアを通じて出荷された注文に対して、Walmart Marketplace が返品と返金の処理を行えるようになりました。 返品と返金に関する情報と更新は、現在のデータが [!DNL Commerce] ストアフロントと [!DNL Walmart Marketplace]. 詳しくは、 [返品・返金の注文](return-refund-orders.md).

![固定](../assets/fix.svg)<!--CHAN-5661--> 修正された `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` チャネルマネージャの再同期で、 `bin/magento saas:resync --feed orders` コマンドを使用します。 エラーは、セールスデータエクスポータモジュールのチャネルマネージャパッケージの依存関係を更新することで解決されました。この依存関係は、から名前が変更されました。 `magento/module-sales-data-exporter` から `magento/module-sales-orders-data-exporter`.

## v1.0.0

*2022 年 1 月 15 日*

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![新規](../assets/new.svg) 一般公開のための Channel Manager の初期リリース

