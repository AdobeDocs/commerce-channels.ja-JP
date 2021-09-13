---
title: Amazonとコマースカタログについて
description: Amazonの販売チャネルは、Amazonのリストをコマースバックエンドに読み込み、製品および販売と絶えず同期します。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Amazonと[!DNL Commerce]カタログについて

AdobeコマースまたはMagento Open Sourceバックエンドには、すべての製品と関連する設定および情報（画像、オプション、価格など）と注文および配送設定を含むカタログが含まれます。 [!DNL Amazon Seller Central]アカウントにはカタログと注文の設定も含まれ、[!DNL Amazon Marketplace]を通じて厳密に販売状況を追跡します。

1か所で製品カタログと販売をより適切に管理および確認するために、Amazonの販売チャネルはAmazonのリストを[!DNL Commerce]バックエンドに読み込み、製品と販売と継続的に同期し、問題と傾向を報告します。 複数の[!DNL Amazon Seller Central]アカウントとの統合をサポートし、複数のストアフロントの単一のインターフェイスを介してすべてのデータを追跡します。

## 製品属性

AdobeコマースおよびMagento Open Sourceは、製品[属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}を使用してカタログの同期を管理し、製品の設定とデータを定義します。 Amazonも属性を使用して、オンボーディングを通じてマッピングします。 Amazonの販売チャネルの[事前設定タスク](./amazon-pre-setup-tasks.md)の間に、Amazonリストを[!DNL Commerce]カタログに読み込む際に、適切な製品マッピングを確保するために、追加のAmazon属性を（必要に応じて）定義します。 これらの属性には、UPC、EAN、ISBN、ASIN([!DNL Amazon Standard Identification Number])が含まれます。 オンボーディングを通じて、製品は属性を使用してAmazonと[!DNL Commerce]カタログ間で同期します。 [!DNL Commerce]製品とAmazon製品を適切にマッピングすると、製品情報、注文、在庫を継続的に同期できます。

カタログ用にこれらの属性を作成または設定していない場合は、オンボーディングする前に、[!DNL Commerce] [product属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}と値を製品に追加する必要があります。 Amazon属性を読み込むと、検索、ナビゲーション、価格ルールなどに使用できます。 これらの属性について詳しくは、[Amazonを参照してください。UPC、EAN、ISBN、ASINとは何ですか。](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target=&quot;_blank&quot;}

オンボーディング後、製品属性とAmazonマッピングをいつでも管理および更新できます。

## 製品リスト

Amazonのリストは、[!DNL Amazon Marketplace]を通じて販売するすべての製品の製品ページで、製品の説明、価格、画像など、属性を通じてマッピングされた製品を表示します。 オンボーディング中に、[!DNL Commerce]製品をAmazonのリストに自動的に公開するように設定できます。 また、既存のAmazonのリストを[!DNL Commerce]製品にマッピングして、インポートすることもできます。

[!DNL Commerce]製品のリストを作成すると、承認を得るためにAmazonに送信されます。 成功したリストのほとんどは、数時間以内に承認されます。 リストが承認されると、顧客の直ちの注文に対して[!DNL Amazon Marketplace]に表示されます。 [!DNL Amazon Sales Channel]拡張機能は、Amazonのリストを確認するための一連のタブを提供します。 問題や必要なデータに応じて、[!DNL Amazon Seller Central]アカウントを確認し、これらのリストの詳細を確認する必要があります。

- [アクティブ](./active-listings.md):マーケットプレイスで使用できる承認済みの製品リストを表示します。

- [リストへの準備完了](./ready-to-list.md):リストのルール要件を満たし、Amazonに公開する準備ができた製品をリストします。

- [非アクティブ](./inactive-listings.md):特定の理由（ブランディングの問題など）でブロックされ、閉じられ、信頼が必要なため、Marketplaceで利用できない製品のリストを表示します。

- [不適格](./ineligible-listings.md):リストルールにより、は、市場に積極的にリストできない製品(数量や販売日な `0` ど)をリストします。

- [不完全](./incomplete-listings.md):必要な情報が不足している製品をリストします。別のレビュー用に製品データを更新します。

- [終了](./ended-listings.md):リストに登録できるが、Amazonから手動で削除された製品リストを表示します。これらの製品を再リストできます。

## データの同期

AdobeコマースとMagento Open Sourceは、[!DNL Amazon Seller Central]アカウントと[!DNL Commerce]バックエンドの間で製品と注文データをやり取りします。 継続的な更新は、[!DNL Commerce]を通じて1つのソースを提供し、インベントリの管理と管理、注文の処理、販売の追跡、および作業のオーバーヘッドと重複の削減を実現します。 レポートは、トレンドを追跡し、2つのシステム間で発生した通信の問題を解決するための最新のデータを取り込みます。

すべての同期は、[cronジョブ](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}によって管理され、[プリセットアップタスク](./amazon-pre-setup-tasks.md)で5分ごとに更新するように設定されます。
