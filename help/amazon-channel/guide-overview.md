---
title: '[!DNL Amazon Sales Channel] ガイド'
description: インストールやオンボーディングなど、Adobe Commerce管理者とMagento Open Source管理者の  [!DNL Amazon sales channel]  に関する包括的な情報を提供します。
seo-title: Adobe Commerce Amazon Sales Channel Guide
seo-description: Describes how to use [!DNL Amazon sales channel] with Adobe Commerce or Magento Open Source.
role: Leader, Admin, User
level: Intermediate
recommendations: noCatalog
exl-id: ad3e2353-313b-4c40-800a-b1ef5f0d8235
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] ガイド

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 [!DNL Amazon sales channel] のインストールとオンボーディング、およびサービスの設定と管理に関する詳細な情報が含まれています。 ここでは、Commerceのコア設定と機能に関する基本的な知識を前提としています。

[!DNL Amazon sales channel] には、管理者向けの領域が 2 つあります。

* 管理者：この領域を使用して、設定 UI およびレポートにアクセスします。
* コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

このガイドでは、Amazonのセールスチャネルを設定するための基本的な [!DNL Amazon Seller Central] 要や要件について説明します。 また、オンボーディングと統合のプロセス、利用可能な店舗、商品、価格、その他のオプションに関する詳細、Amazon sales channel を使用して [!DNL Amazon Marketplace] でのリストと売上を管理する方法についても説明します。 左側のパネルを使用して様々な機能間を移動し、ドリルダウンして詳細情報および手順にアクセスします。

>[!NOTE]
>
>このガイドでは、Adobe CommerceとMagento Open Sourceのコア機能については説明しません。

| 領域 | 説明 |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Amazon販売チャネルの概要 ](./overview.md) | Amazon セールスチャネルの基本、主な機能、ベストプラクティスなどについて説明します。 |
| [ オンボードAmazonセールスチャネル ](./amazon-onboarding-home.md) | Amazon ストアをすばやく作成して、[!DNL Amazon Seller Central] と統合します。 Amazonのセールスチャネルを立ち上げて、販売を開始します。 |
| [Amazon販売チャネルホーム ](./amazon-sales-channel-home.md) | Amazon Sales Channel のホームページと使用可能なオプションおよびタスクについて詳しく説明します。 Amazon ストアの概要情報を表示し、ストアの詳細と設定にアクセスします。 |
| [ 属性の管理 ](./attributes-view.md) | Amazon販売チャネルは、製品属性を使用して [!DNL Commerce] カタログとAmazon間で製品をマッピングします。 これらの属性の作成、マッピング、管理について説明します。 |
| [ ストア設定の管理 ](./ob-store-review.md) | リスト設定、注文設定、リストおよび価格設定ルールなど、ストア設定を表示および変更します。 |
| [ リストの管理 ](./managing-product-listings.md) | Amazon Marketplace を通じて販売する際に、リスト（設定、ルール、価格）を更新、追加、管理できます。 ストアおよびリスト設定の作成と変更の詳細を説明します。 |
| [ 注文とフルフィルメントの管理 ](./managing-orders.md) | Amazon sales channel は、Amazonと [!DNL Commerce] を通じて、注文のフルフィルメントと出荷をサポートしています。 Amazonを通じたフルフィルメント、[!DNL Commerce] を通じた直接のフルフィルメント、および注文管理のオプションについて詳しく説明します。 |
| [ ログとレポートの表示 ](./amazon-logs-reports.md) | トラッキングされるエラーと、Amazonと [!DNL Commerce] の間のやり取りについて説明します。 |

## 追加ドキュメント

| ドキュメントリソース | 説明 |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Adobe Commerce 2.4 マーチャントドキュメント ](https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html) | Adobe CommerceとMagento Open Sourceの両方に関するマーチャント向けドキュメント |
| [Adobe Commerce向けサービスのドキュメント ](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | マーチャントがビジネスの主要なコンポーネントをストアと統合するのに役立つ、サービスのコレクションをサポートするドキュメント。 |
| [ クラウドインフラストラクチャー上のCommerceガイド ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 管理された自動ホスティングクラウドプラットフォームにAdobe Commerceをデプロイするためのステップバイステップの手順。 |
| [Adobe Commerce 2.4 運用ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Adobe CommerceおよびMagento Open Sourceプラットフォームにデプロイされたプロジェクトを開発、デプロイ、管理するためのコンセプト、プロセス、ツールおよびベストプラクティスに関するシステムドキュメント。 |
| [Adobe Commerce 2.4 開発者向けドキュメント ](https://developer.adobe.com/commerce/docs) | Adobe CommerceまたはMagento Open Sourceの構築とカスタマイズに使用される、開発者向けドキュメント |

{style="table-layout:auto"}

## サポート

情報が必要な場合や、このガイドで扱われていない質問がある場合は、次のリソースを使用してください。

* [ ヘルプセンター ](https://support.magento.com/hc/en-us) - [!DNL Amazon Sales Channel] に関連するトラブルシューティング記事を参照してください。
* [ サポートチケット ](https://support.magento.com/hc/en-us/articles/360000913794#submit-ticket) - チケットを送信すると、追加のヘルプを受けることができます。
