---
title: '''[!DNL Amazon Sales Channel] ガイド`'
description: に関する包括的な情報 [!DNL Amazon sales channel] (Adobe CommerceおよびMagento Open Source管理者向け )
seo-title: Adobe Commerce Amazon Sales Channel Guide
seo-description: Describes how to use [!DNL Amazon sales channel] with Adobe Commerce or Magento Open Source.
exl-id: ad3e2353-313b-4c40-800a-b1ef5f0d8235
source-git-commit: 901d856067cd9d236727edc8bde354820791c411
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] ガイド

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 のインストールとオンボーディングに関する詳細情報が含まれます。 [!DNL Amazon sales channel]、およびサービスの設定と管理。 ここでは、コマースのコア設定と機能に関する基本的な知識を前提としています。

[!DNL Amazon sales channel] には、管理者向けの次の 2 つの領域があります。

* 管理者：この領域を使用して、設定 UI とレポートにアクセスします。
* コマンドラインインターフェイスは次のようになります。このツールを使用して、インストールおよびバックエンドの設定タスクを実行します。

このガイドでは、いくつかの基本事項を説明します [!DNL Amazon Seller Central] の設定に必要な要件について説明します。Amazonのセールスチャネルの設定に必要な要件について説明します。 また、オンボーディングと統合プロセス、利用可能なストア、製品、価格、その他のオプション、Amazonセールスチャネルを使用して [!DNL Amazon Marketplace]. 左側のレールを使用して様々な機能をナビゲートし、ドリルダウンして詳細情報と手順にアクセスします。

>[!NOTE]
>
>このガイドでは、Adobe CommerceとMagento Open Sourceの主な機能については説明しません。

| 領域 | 説明 |
|----|----|
| [Amazonセールスチャネルの概要](./overview.md) | Amazonセールスチャネルの基本、主な機能、ベストプラクティスなどの詳細をご覧ください。 |
| [Amazonセールスチャネルのオンボーディング](./amazon-onboarding-home.md) | Amazonストアをすばやく作成し、と統合する [!DNL Amazon Seller Central]. Amazonのセールスチャネルを立ち上げ、導入して、販売を開始します。 |
| [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) | Amazonセールスチャネルのホームページと、使用可能なオプションおよびタスクの詳細をご覧ください。 Amazonストアの概要情報を表示し、ストアの詳細と設定にアクセスします。 |
| [属性の管理](./attributes-view.md) | Amazonセールスチャネルは、 [!DNL Commerce] 製品属性を使用したカタログとAmazon これらの属性の作成、マッピング、管理の詳細について説明します。 |
| [ストア設定を管理](./ob-store-review.md) | ストア設定（リスト設定、注文設定、リストおよび価格設定ルールなど）を表示および変更します。 |
| [リストの管理](./managing-product-listings.md) | Amazon Marketplace を通じて販売する際に、リスト（設定、ルールおよび価格）を更新、追加および管理できます。 ストアおよびリストの設定の作成と変更について詳しく説明します。 |
| [オーダーと達成の管理](./managing-orders.md) | Amazonセールスチャネルは、Amazonを介した注文の達成と出荷をサポートします。 [!DNL Commerce]. を通じて、Amazonを通じて直接充実していく方法を学ぶ [!DNL Commerce]、および注文管理オプション。 |
| [ログとレポートの表示](./amazon-logs-reports.md) | Amazonと [!DNL Commerce]. |

## その他のドキュメント

| ドキュメントリソース | 説明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Merchant ドキュメント](https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html) | Adobe CommerceとMagento Open Sourceの両方に関するマーチャント中心のドキュメント |
| [Adobe Commerce Documentation のサービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | マーチャントがビジネスの主要なコンポーネントを店舗に統合するのに役立つサービスのコレクションをサポートするドキュメントです。 |
| [Commerce on Cloud Infrastructure ガイド](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 管理対象の自動ホスティングされた Cloud プラットフォームにAdobe Commerceをデプロイする手順を説明します。 |
| [Adobe Commerce 2.4 運用ガイド](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Adobe CommerceおよびMagento Open Sourceプラットフォームにデプロイされたプロジェクトを開発、デプロイ、メンテナンスするための概念、プロセス、ツール、ベストプラクティスに関するシステムドキュメントです。 |
| [Adobe Commerce 2.4 開発者向けドキュメント](https://developer.adobe.com/commerce/docs) | Adobe CommerceまたはMagento Open Sourceの構築とカスタマイズに使用する開発者向けドキュメント |

{style="table-layout:auto"}

## サポート

このガイドに記載されていない情報や質問がある場合は、次のリソースを使用してください。

* [ヘルプセンター](https://support.magento.com/hc/en-us)— [!DNL Amazon Sales Channel] — 関連のトラブルシューティング記事。
* [サポートチケット](https://support.magento.com/hc/en-us/articles/360000913794#submit-ticket) — 追加のヘルプを受け取るには、チケットを送信します。
