---
title: 「[!DNLChannel Manager] リリースノート」
description: 「 [!DNL Channel Manager] Adobe Commerceから」
source-git-commit: 501a76a126f090805f95e64078ec2c73de003aa4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!DNL Channel Manager] リリースノート

以下のリリースノートでは、 [!DNL Channel Manager] およびを含めます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題


## v1.1.0

![新規](../assets/new.svg)<!--CHAN-5204--> **返品と返金**—Adobe CommerceとMagento Open Source・チャネル・マネージャーのストアを通じて出荷された注文に対して、Walmart Marketplace が返品と返金の処理を行えるようになりました。 返品と返金に関する情報と更新は、現在のデータが [!DNL Commerce] ストアフロントと [!DNL Walmart Marketplace]. 詳しくは、 [返品・返金の注文](return-refund-orders.md).

![固定](../assets/fix.svg)<!--CHAN-5661--> 修正された `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` チャネルマネージャの再同期で、 `bin/magento saas:resync --feed orders` コマンドを使用します。 エラーは、セールスデータエクスポータモジュールのチャネルマネージャパッケージの依存関係を更新することで解決されました。この依存関係は、から名前が変更されました。 `magento/module-sales-data-exporter` から `magento/module-sales-orders-data-exporter`.

## v1.0.0

初期リリース。次の Commerce バージョンとの互換性。

* オープンソース (CE):2.4.x
* Adobe Commerce(EE):2.4.x
* Adobe Commerce for Cloud (ECE):2.4.x
* 安定性：安定