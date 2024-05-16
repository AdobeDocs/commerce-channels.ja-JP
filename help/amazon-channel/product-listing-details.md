---
title: Amazon リストの詳細の表示
description: Amazonのリストおよび個々の SKU や商品の変更に関する競合指標を理解するには、商品リストの詳細ページを参照してください。
feature: Sales Channels, Products, Merchandising
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Amazon リストの詳細の表示

この _[!UICONTROL Product Listing Details]_ページには、個々の SKU/製品の変更を示すリストアクティビティログなど、アクティブな製品リストに関する追加情報が表示されます。 この情報は、製品および個々の SKU/製品の変更に関する競合指標を理解するのに役立ちます。 このページの追加情報には、次のものが含まれます。

- **[!UICONTROL Listing Details]**  – 名前やAmazonの販売者 SKU を含む製品の詳細
- **[!UICONTROL Listing Activity Log]**  – 価格や数量/在庫の変更など、このリストに対して発生したすべての変更の履歴レコード。 これ以上のアクションは必要ありません。 このログは、変更履歴を把握するために提供されます。
- **[!UICONTROL Buy Box Competitor Pricing]** - Amazonのデータ [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ステータスと競合他社価格
- **[!UICONTROL Lowest Competitor Pricing]** -Amazonの競合企業の価格とフィードバックに関する情報

Amazonのセールスチャネルのホームページには、いくつかの共通点があります [workspace コントロール](./workspace-controls.md) 表示するデータをカスタマイズできます。

## リストの詳細

表示される製品情報には、次のものが含まれます。

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![リストの詳細](assets/amazon-product-listing-details.png){width="600" zoomable="yes"}

## アクティビティログを一覧表示 {#listing-activity-log}

Amazon リストに関する最近のすべてのアクティビティを表示します。 表示される情報には、次のものが含まれます。

- Amazon販売者 SKU：リスト用に定義された最小在庫管理単位（SKU）を識別します。
- ASIN: 10 桁のAmazon商品識別子を識別します。
- リスト処理：リストに対して発生した処理のタイプを識別します。
- コメント：発生したリストアクションのタイプに関する追加の詳細が表示されます。
- 実行時間：アクションが発生した日時を識別します。

![製品リストの詳細 – アクティビティログのリスト](assets/amazon-listing-activity-log.png){width="600" zoomable="yes"}
__

## Buy Boxの競合他社価格 {#buy-box-competitor-pricing}

このタブには、を保持するAmazon マーチャントに関する情報が表示されます [[!DNL Buy Box]](./buy-box-competitor-pricing.md) リストの位置。 この情報は、Amazonにおける競合他社の価格の位置づけを理解するために使用できます。 表示される情報には、次のものが含まれます。

- ASIN: 10 桁のAmazon商品識別子。
- 販売者である：自分が販売者かどうかを識別します [!DNL Buy Box] 販売者 オプション Yes / No。
- 条件：リストに対して定義する条件を識別します。
- 上場価格：上場が公開された価格を識別します。
- 発送価格：リストに追加される発送価格を識別します。
- 上陸価格：上場価格にリストの出荷価格を加えた価格を識別します。
- 最終更新日：価格情報がAmazonから更新された日時を特定します。

![商品リストの詳細：Buy Boxの競合他社価格](assets/amazon-listing-details-buy-box-2.png){width="600" zoomable="yes"}

## 競合製品の最低価格 {#lowest-competitor-pricing}

このタブには、同じリストのAmazonの競合他社に関する情報が表示されます。 この情報は、価格の位置づけを理解するために使用できます。 [競合製品の最低価格](./lowest-competitor-pricing.md). 表示される情報には、次のものが含まれます。

- ASIN: 10 桁のAmazon商品識別子。
- 条件：リストに対して定義する条件を識別します。
- フルフィルメントチャネル：フルフィルメントを担当する関係者を識別します。 オプション：マーチャント/Amazon。
- 上場価格：上場が公開された価格を識別します。
- 発送価格：リストに追加される発送価格を識別します。
- 上陸価格：上場価格にリストの出荷価格を加えた価格を識別します。
- フィードバック評価：最低価格のマーチャントに対するAmazonのフィードバック評価を識別します。
- フィードバック数：最低価格のマーチャントのAmazon フィードバック数を識別します。
- 最終更新日：価格情報がAmazonから更新された日時を特定します。

![製品リストの詳細 – 競合他社価格の最低価格](assets/amazon-listing-details-lowest-comp.png){width="600" zoomable="yes"}
