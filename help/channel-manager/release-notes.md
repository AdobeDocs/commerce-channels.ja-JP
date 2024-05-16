---
title: '''[!DNL Channel Manager] リリースノート'
description: の最新のリリース情報 [!DNL Channel Manager] Adobe Commerceから
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# [!DNL Channel Manager] リリースノート

これらのリリースノートは、の初回リリースについて説明しています [!DNL Channel Manager] これには以下が含まれます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

参照： [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) リリーススケジュールとサポートについて説明します。

参照： [製品の可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) この拡張機能をサポートしているAdobe Commerceのバージョンを確認するには、

## v2.1.0

*2023 年 10 月 3 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) チャネルマネージャーはと互換性を持つようになりました [Adobe Commerce バージョン 2.4.7 ベータ版](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html) リリース。

## v2.0.0

*2023 年 3 月 20 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg)<!--CHAN-5893--> Channel Manager は、Adobe Commerce バージョン 2.4.6 と互換性を持つようになりました。

## v1.1.0

*2022 年 11 月 23 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg)<!--CHAN-5204--> **返品および返金**—Adobe CommerceおよびMagento Open Sourceチャネル・マネージャ・ストアを通じて出荷された注文に対して、Walmart Marketplace の返品および払い戻し処理を実行できるようになりました。 返品と払い戻しに関する情報と更新は、ウォルマートとAdobe Commerceの間で同期され、現在のデータは両方の [!DNL Commerce] ストアフロントと [!DNL Walmart Marketplace]. 参照： [返品および返金の注文](return-refund-orders.md).

![固定](../assets/fix.svg)<!--CHAN-5661--> を修正 `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` を使用してチャネルマネージャーの注文データを再同期する際に発生したエラー `bin/magento saas:resync --feed orders` コマンド。 このエラーは、Sales Data Exporter モジュールのチャネルマネージャーパッケージ依存関係を更新することで解決されました。この名前は、から変更されました `magento/module-sales-data-exporter` 対象： `magento/module-sales-orders-data-exporter`.

## v1.0.0

*2022 年 1 月 14 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) 一般リリース向けの Channel Manager の初回リリース

