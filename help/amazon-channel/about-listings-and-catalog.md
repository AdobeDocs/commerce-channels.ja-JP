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

Adobe CommerceまたはMagento Open Sourceのバックエンドには、すべての商品と関連する設定および情報（画像、オプション、価格など）を含むカタログ、および注文と配送の設定が含まれます。 [!DNL Amazon Seller Central] アカウントにはカタログと注文の設定もあり、[!DNL Amazon Marketplace] を通じてお客様の販売を厳密に追跡します。

1 つの場所で商品カタログと売上をより適切に管理およびレビューするために、Amazon sales channel では、Amazonのリストを [!DNL Commerce] バックエンドに読み込み、商品と売上を継続的に同期し、問題とトレンドをレポートします。 複数の [!DNL Amazon Seller Central] アカウントとの統合をサポートし、単一のインターフェイスを介してすべてのデータを追跡し、複数のストアフロントに対応します。

## 製品属性

Adobe CommerceとMagento Open Sourceは、製品 [ 属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) を使用してカタログ同期を管理し、製品の設定とデータを定義します。 Amazonは属性も使用して、オンボーディングを通じてマッピングされます。 Amazon セールスチャネルの [ 事前設定タスク ](./amazon-pre-setup-tasks.md) 中に、（必要に応じて）追加のAmazon属性を定義して、Amazonのリストを [!DNL Commerce] カタログに読み込む際に製品マッピングが正しくなるようにします。 これらの属性には、UPC、EAN、ISBN、および ASIN （[!DNL Amazon Standard Identification Number]）が含まれます。 オンボーディングを通じて、製品は属性を使用してAmazonと [!DNL Commerce] カタログを同期します。 [!DNL Commerce] とAmazonの商品を適切にマッピングすることで、商品の情報、注文および在庫を継続的に同期させることができます。

これらの属性をカタログ用に作成または設定していない場合は、オンボーディングの前に製品に [!DNL Commerce] [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) と値を追加する必要があります。 Amazon属性を読み込むと、検索、ナビゲーション、価格ルールなどに使用できます。 [ASIN、UPC、EAN、ISBN、SKU およびその他のバーコードとは ](https://sellerskills.com/multi-channel-operations/what-asin-upc-ean-isbn-sku-and-other-barcodes-mean/#what-is-isbn-number){target="_blank"} を参照してください。

オンボーディング後は、製品属性とAmazon マッピングをいつでも管理および更新できます。

## 製品リスト

Amazonのリストは、ア [!DNL Amazon Marketplace] ットを通じて販売する各商品の商品ページであり、属性を通じてマッピングされた商品の説明、価格、画像などを表示します。 オンボーディング中に、[!DNL Commerce] の商品をAmazon リストに自動的に公開できるように設定できます。 また、既存のAmazonのリストを [!DNL Commerce] の商品にマッピングして読み込むこともできます。

商品のリストを作成すると、そ [!DNL Commerce] 商品はAmazonに送信されて承認を受けます。 ほとんどの成功したリストは数時間以内に承認されます。 リストが承認されると、顧客からの即時の注文の [!DNL Amazon Marketplace] に表示されます。 [!DNL Amazon Sales Channel] 拡張機能には、Amazonのリストを確認するための一連のタブが用意されています。 問題や必要なデータに応じて、これらのリストに関する特定の詳細について、[!DNL Amazon Seller Central] アカウントを確認する必要があります。

- [ アクティブ ](./active-listings.md)：マーケットプレイスで利用可能な、承認済み製品リストを一覧表示します。

- [ リストへの準備完了 ](./ready-to-list.md)：リストルールの要件を満たし、Amazonへの公開準備が整った製品をリストします。

- [ 非アクティブ ](./inactive-listings.md)：特定の理由（ブランディングの問題など）でブロックされている、クローズされている、信頼が必要であるなどの理由で、マーケットプレイスで利用できない製品のリストを表示します。

- [ 不適格 ](./ineligible-listings.md)：リストルールにより、マーケットプレイスにアクティブにリストできない製品（数量や販売日など） `0` リストします。

- [ 未完了 ](./incomplete-listings.md)：必要な情報が欠落している製品がリストされます。 別のレビュー用に製品データを更新します。

- [ 終了 ](./ended-listings.md)：リスト対象の商品リストをリストしますが、Amazonから手動で削除します。 これらの製品は再リストに登録できます。

## データの同期

Adobe CommerceとMagento Open Sourceは、[!DNL Amazon Seller Central] アカウントと [!DNL Commerce] バックエンドの間で製品データと注文データをやり取りします。 継続的な更新により、在庫の管理と維持、注文のフルフィルメント、販売の追跡、オーバーヘッドの削減と作業の重複を [!DNL Commerce] う単一のソースが提供されます。 レポートでは、トレンドの追跡と 2 つのシステム間で発生する通信の問題の解決に役立つ最新のデータを取得します。

すべての同期は [Cron ジョブ ](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) によって管理され、[ 事前設定タスク ](./amazon-pre-setup-tasks.md) で 5 分ごとに更新されるように設定されます。
