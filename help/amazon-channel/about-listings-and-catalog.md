---
title: Amazonとコマースカタログについて
description: Amazonセールスチャネルは、Amazonのリストをコマースのバックエンドにインポートし、製品および販売と絶えず同期します。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Amazonと [!DNL Commerce] カタログ

Adobe CommerceまたはMagento Open Sourceバックエンドには、すべての製品と関連する設定および情報（画像、オプション、価格など）と注文および配送設定を含むカタログが含まれています。 お使いの [!DNL Amazon Seller Central] また、アカウントにはカタログと注文の設定が含まれ、 [!DNL Amazon Marketplace].

1 か所で製品カタログと販売をより詳細に管理および確認するために、Amazonの販売チャネルはAmazonの一覧を [!DNL Commerce] バックエンドで製品や販売と継続的に同期し、問題やトレンドを報告します。 複数の [!DNL Amazon Seller Central] アカウントでは、複数のストアフロントに対する単一のインターフェイスを介してすべてのデータを追跡できます。

## 製品属性

Adobe CommerceとMagento Open Sourceは、製品の使用に伴うカタログ同期の管理 [属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} 製品設定とデータを定義します。 Amazonも属性を使用して、オンボーディングを通じてマッピングします。 期間 [事前設定タスク](./amazon-pre-setup-tasks.md) Amazonセールスチャネルの場合、Amazonリストをユーザーに読み込む際に、正しい製品マッピングを確保するために、追加のAmazon属性（必要に応じて）を定義します。 [!DNL Commerce] カタログ。 これらの属性には、UPC、EAN、ISBN、ASIN ([!DNL Amazon Standard Identification Number]) をクリックします。 オンボーディングを通じて、Amazonと [!DNL Commerce] カタログを作成します。 適切なマッピング [!DNL Commerce] Amazon製品を使用すると、製品情報、注文、在庫を継続的に同期できます。

カタログ用にこれらの属性を作成または設定していない場合、 [!DNL Commerce] [製品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} and values to your products before onboarding. When an Amazon attribute is imported, it can be used for search, navigation, price rules, and much more. See [What Do ASIN, UPC, EAN, ISBN, SKU and Other Barcodes Mean?](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

オンボーディング後は、製品属性とAmazonマッピングをいつでも管理および更新できます。

## 製品リスト

Amazonリストは、 [!DNL Amazon Marketplace]、製品の説明、価格、画像など、属性を通じてマッピングされた情報を表示します。 オンボーディング中に、 [!DNL Commerce] 製品はAmazonリストに自動的に公開できます。 また、既存のAmazonリストを [!DNL Commerce] 製品。

リストを作成したとき [!DNL Commerce] 製品の場合は、承認を得るためにAmazonに送信されます。 成功したリストのほとんどは、数時間以内に承認されます。 リストが承認されると、リストは [!DNL Amazon Marketplace] を使用して、顧客による即時の注文。 この [!DNL Amazon Sales Channel] 拡張機能では、Amazonのリストを確認するための一連のタブが提供されます。 問題や必要なデータに応じて、 [!DNL Amazon Seller Central] アカウントを参照してください。

- [アクティブ](./active-listings.md):Marketplace で使用可能な承認済みの製品リストを表示します。

- [リストへの登録準備完了](./ready-to-list.md):リストルール要件を満たし、Amazonに公開する準備ができた製品を一覧表示します。

- [非アクティブ](./inactive-listings.md):特定の理由（ブランディングの問題など）によりブロックされたため、マーケットプレイスで利用できない製品、クローズ済みの製品、信頼が必要な製品などを一覧表示します。

- [不適格](./ineligible-listings.md):リストルールにより、はマーケットプレイスに積極的にリストできない製品 ( `0` 数量または販売日 )。

- [不完全](./incomplete-listings.md):必要な情報が不足している製品をリストします。 別のレビュー用に製品データを更新します。

- [終了](./ended-listings.md):リストに登録できるが、手動でAmazonから削除された製品リストを表示します。 これらの製品はリストし直すことができます。

## データの同期

Adobe CommerceとMagento Open Sourceは、 [!DNL Amazon Seller Central] アカウントおよび [!DNL Commerce] バックエンド。 継続的な更新により、 [!DNL Commerce] 在庫の管理と管理、受注の完了、売上の追跡、および作業のオーバーヘッドと重複の削減を行う。 レポートは、トレンドを追跡し、2 つのシステム間で発生した通信の問題を解決するための最新のデータを取り込みます。

すべての同期は、 [cron ジョブ](https://docs.magento.com/user-guide/system/cron.html){target="_blank"}を更新し、 [事前設定タスク](./amazon-pre-setup-tasks.md).
