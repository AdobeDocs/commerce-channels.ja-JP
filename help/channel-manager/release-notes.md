---
title: '[!DNL Channel Manager] リリースノート'
description: Adobe Commerceからのの最新  [!DNL Channel Manager]  リリース情報です。
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# [!DNL Channel Manager] リリースノート

このリリースノートは、[!DNL Channel Manager] の初期リリースを説明するもので、次のものが含まれます。

![ 新機能 ](../assets/new.svg) 新機能
![ 修正された問題 ](../assets/fix.svg) 修正および改善
![ 既知の問題 ](../assets/bug.svg)

リリーススケジュールとサポートについては、[ 今後のリリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) を参照してください。

この拡張機能をサポートするAdobe Commerceのバージョンについては、[ 製品の可用性 ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) を参照してください。

## v2.1.0

*2023 年 10 月 3 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) Channel Manager は、[Adobe Commerce バージョン 2.4.7 ベータ版 ](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html) リリースと互換性を持つようになりました。

## v2.0.0

*2023 年 3 月 20 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)<!--CHAN-5893--> Channel Manager は、Adobe Commerce バージョン 2.4.6 と互換性を持つようになりました。

## v1.1.0

*2022 年 11 月 23 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg)<!--CHAN-5204--> **返品と払い戻し** - Adobe CommerceおよびMagento Open Sourceチャネル・マネージャ・ストアを介して出荷された受注に対して、Walmart Marketplace の返品と払い戻し処理を処理できるようになりました。 返品と払い戻しに関する情報と更新は、ウォルマートとAdobe Commerceの間で同期されるため、現在のデータは [!DNL Commerce] ストアフロントと [!DNL Walmart Marketplace] の両方で利用できます。 [ 返品および返金の注文 ](return-refund-orders.md) を参照してください。

![ 修正 ](../assets/fix.svg)<!--CHAN-5661--> `bin/magento saas:resync --feed orders` コマンドを使用してチャネルマネージャーの注文データを再同期する際に発生していた `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` エラーを修正しました。 このエラーは、Sales Data Exporter モジュールのチャネルマネージャーパッケージ依存関係を更新することで解決されました。この名前は、`magento/module-sales-data-exporter` から `magento/module-sales-orders-data-exporter` に変更されました。

## v1.0.0

*2022 年 1 月 14 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) 一般リリース向けの Channel Manager の初期リリース

