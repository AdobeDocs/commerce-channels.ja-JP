---
title: Amazon ストアダッシュボード
description: Amazon ストアダッシュボードを使用して、Commerce管理者からAmazon ストアのアクティビティを表示します。
feature: Sales Channels, Orders, Storefront
exl-id: b86220c6-8350-474e-8faa-988a9a575ac4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Amazon ストアダッシュボード

が含まれる _[!UICONTROL Amazon Stores]_Amazon sales channel のホームページで、**[!UICONTROL View Store]**ストアカードでストアダッシュボードを開きます。

ストアダッシュボードは、各Amazon ストアのアクティビティを表示する主な場所です。 と [!DNL Amazon Seller] 追加および統合されたストアは、ストアデータビューを通じて注文と販売の追跡を行います。 ダッシュボードでは、売上高の表示、トレンドの追跡、リストの販売データのレビューを行うことができます。 リストと売上は、アクティブ、非アクティブ、進行中など、リストタイプ別にさらにグループ化され、追跡されます。

にアクセスすることもできます [ストアの設定](./ob-store-review.md), [リストの管理](./managing-product-listings.md)をクリックし、販売データと最近の注文情報を表示します。

![Amazon ストアダッシュボード](assets/amazon-store-dashboard.png){width="600" zoomable="yes"}

ストアダッシュボードのヘッダーには、ストアカードに表示されるのと同じ基本的なストア情報が表示されます。

- _[!UICONTROL Store Name]_
- _[!UICONTROL Magento Website]_
- _[!UICONTROL Status]_
- _[!UICONTROL Created]_
- _[!UICONTROL Last Updated]_

ストアダッシュボードには、ストアデータと、設定または詳細情報へのリンクも含まれます。

- [**[!UICONTROL Store Settings]**](./ob-store-review.md) - ストアの設定とレポートにアクセスします。

   - [**[!UICONTROL Listing settings]**](./listing-settings.md)  – 製品カタログとの相互作用を制御する [!DNL Amazon Marketplace].

   - [**[!UICONTROL Order settings]**](./order-settings.md) - Amazon注文の管理方法を制御します。

   - [**[!UICONTROL Listing rules]**](./listing-rules.md) - Amazonにリストできるカタログ商品を定義します。

   - [**[!UICONTROL Pricing rules]**](./pricing-products.md)  – 適格な上場に対するAmazonの定価の変更方法を定義します。

   - [**[!UICONTROL Store reports]**](./amazon-logs-reports.md) - [競争価格分析](./competitive-price-analysis.md) および [リストの改善](./listing-improvements.md).

   - [**[!UICONTROL Logs]**](./amazon-logs-reports.md) - [リストの変更](./listing-changes-log.md) および [通信エラー](./communication-errors-log.md).

   - [**[!UICONTROL Store integration settings]**](./store-integration-settings.md)  – のメールおよびAmazon販売チャネルストアの名前設定を確認します [!DNL Commerce] 管理者。

- **[!UICONTROL Store Listings]**  – 過去 7 日間または 30 日間の店舗販売のグラフィカル表現と、生涯販売データを表示します。

  このセクションには、のリスト数も表示されます [アクティブな一覧](./active-listings.md), [非アクティブな一覧](./inactive-listings.md)、処理中のリストおよび対応するリンク _[!UICONTROL Product Listings]_ページ。 次をクリックすることもできます&#x200B;**[!UICONTROL Manage Listings]**を開きます_[!UICONTROL Product Listings]_ ページ。 参照： [Amazon リストの管理](./managing-product-listings.md).

- **[!UICONTROL Recent Orders]**  – 最新のAmazon注文に関する情報を表示します。 表示される情報は、Amazonから受信した情報に基づいています。 このテーブルはで更新されません [!DNL Commerce] 注文情報（の場合も） [注文の読み込み](./order-settings.md) が有効になっています。 すべてのAmazon注文を表示するには、以下をクリックします。 **すべての注文**.

  参照： [Amazonの注文を表示](./amazon-orders-all.md) 列の説明については、を参照してください [注文の管理](./managing-orders.md) を参照してください。

- **[!UICONTROL Seller Central links]**  – 重要なリンクを提供します [!DNL Amazon Seller Central] 情報。
