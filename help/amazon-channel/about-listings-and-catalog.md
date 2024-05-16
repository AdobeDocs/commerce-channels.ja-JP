---
title: AmazonとCommerce カタログ
description: Amazonの営業チャネルは、AmazonのリストをCommerce バックエンドに読み込み、商品や売上と継続的に同期します。
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services, Merchandising, Catalog Management
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Amazonと [!DNL Commerce] カタログ

Adobe CommerceまたはMagento Open Sourceのバックエンドには、すべての商品と関連する設定および情報（画像、オプション、価格など）を含むカタログ、および注文と配送の設定が含まれます。 あなたの [!DNL Amazon Seller Central] アカウントにはカタログと注文の設定もあり、 [!DNL Amazon Marketplace].

1 つの場所で商品カタログと売上高をより適切に管理およびレビューするために、Amazon販売チャネルはAmazonのリストをのサイトに読み込みます [!DNL Commerce] バックエンドは、製品や売上と継続的に同期し、問題やトレンドを報告します。 複数のとの統合をサポートします [!DNL Amazon Seller Central] 複数のストアフロント向けの単一のインターフェイスを通じてすべてのデータを追跡する、アカウント。

## 製品属性

Adobe CommerceとMagento Open Sourceは、製品を使用してカタログ同期を管理します [属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) 製品の設定とデータを定義します。 Amazonは属性も使用して、オンボーディングを通じてマッピングされます。 次の期間 [事前設定タスク](./amazon-pre-setup-tasks.md) Amazon セールスチャネルの場合、Amazonのリストをのチャネルに読み込む際に、製品が正しくマッピングされるように、（必要に応じて）追加のAmazon属性を定義します [!DNL Commerce] カタログ。 これらの属性には、UPC、EAN、ISBN および ASIN （[!DNL Amazon Standard Identification Number]）に設定します。 オンボーディングを通じて、製品はAmazonとの間で同期されます [!DNL Commerce] 属性を使用したカタログ。 の適切なマッピング [!DNL Commerce] とAmazonの製品は、商品情報、注文および在庫の継続的な同期を確保します。

これらの属性をカタログ用に作成または設定していない場合は、を追加する必要があります。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) およびオンボーディング前の製品への値。 Amazon属性を読み込むと、検索、ナビゲーション、価格ルールなどに使用できます。 参照： [ASIN、UPC、EAN、ISBN、SKU およびその他のバーコードは何を意味しますか？](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"}

オンボーディング後は、製品属性とAmazon マッピングをいつでも管理および更新できます。

## 製品リスト

Amazon リストは、を通じて販売するすべての商品の商品ページです [!DNL Amazon Marketplace]属性を通じてマッピングされた製品の説明、価格、画像などを表示します。 オンボーディング中に、 [!DNL Commerce] 商品は、Amazonのリストに自動的に公開できます。 また、既存のAmazon リストを読み込むには、それらをにマッピングします。 [!DNL Commerce] 製品。

リストの作成時 [!DNL Commerce] 商品がAmazonに送信され、承認が得られます。 ほとんどの成功したリストは数時間以内に承認されます。 リストが承認されると、に表示されます [!DNL Amazon Marketplace] 顧客からの即時オーダーの場合。 この [!DNL Amazon Sales Channel] extension には、Amazonのリストを確認するための一連のタブが用意されています。 問題や必要なデータに応じて、 [!DNL Amazon Seller Central] これらのリストに関する特定の詳細を説明します。

- [アクティブ](./active-listings.md):Marketplace で利用できる承認済み製品リストを表示します。

- [リストへの準備完了](./ready-to-list.md)：リストルールの要件を満たし、Amazonへの公開準備が整った製品をリストします。

- [Inactive](./inactive-listings.md)：特定の理由（ブランディングの問題など）でブロックされている、クローズされている、信頼が必要であるなどの理由で、マーケットプレイスで利用できない製品のリストを表示します。

- [不適格](./ineligible-listings.md)：リストルールにより、は、Marketplace に積極的にリストできない製品（など）をリストします `0` 数量または販売日）。

- [未完了](./incomplete-listings.md)：必要な情報が欠落している製品のリスト。 別のレビュー用に製品データを更新します。

- [終了](./ended-listings.md)：リストに適格な製品リストをリストしますが、Amazonから手動で削除されました。 これらの製品は再リストに登録できます。

## データの同期

Adobe CommerceとMagento Open Sourceは、製品間で製品と注文のデータをやり取りします [!DNL Amazon Seller Central] アカウントと [!DNL Commerce] バックエンド。 継続的なアップデートにより、以下を通じて単一のソースが提供されます。 [!DNL Commerce] 在庫の管理と保守、オーダーの履行、販売の追跡、オーバーヘッドの削減および作業の重複の削減を行います。 レポートでは、トレンドの追跡と 2 つのシステム間で発生する通信の問題の解決に役立つ最新のデータを取得します。

すべての同期はによって管理されます [cron ジョブ](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)、で 5 分ごとに更新するように設定します [事前設定タスク](./amazon-pre-setup-tasks.md).
