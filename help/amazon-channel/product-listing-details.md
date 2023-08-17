---
title: Amazonリストの詳細を表示
description: Amazonのリストや個々の SKU/製品の変更に関する競合指標を理解するには、製品リストの詳細ページを確認してください。
feature: Sales Channels, Products, Merchandising
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# Amazonリストの詳細を表示

The _[!UICONTROL Product Listing Details]_ページには、個々の SKU /製品の変更を表示する「アクティビティログを一覧表示」など、アクティブな製品リストに関する追加情報が表示されます。 この情報は、製品に関する競合指標や、個々の SKU/製品の変更に関する指標を理解するのに役立ちます。 このページの追加情報には、次のものが含まれます。

- **[!UICONTROL Listing Details]**  — 製品の詳細 ( 名前、Amazonセラー SKU など )
- **[!UICONTROL Listing Activity Log]**  — 価格、数量/在庫変更など、このリストに対して発生したすべての変更の履歴レコード。 それ以上のアクションは必要ありません。 このログは、変更履歴を理解するためのレビュー用に提供されます。
- **[!UICONTROL Buy Box Competitor Pricing]** - Amazonのデータ [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ステータスと競合他社の価格
- **[!UICONTROL Lowest Competitor Pricing]**  — 最も低いAmazonの競合相手の価格とフィードバック情報に関する情報

Amazonセールスチャネルのホームページは、いくつかの共通を共有します [workspace コントロール](./workspace-controls.md) を使用すると、表示されるデータをカスタマイズできます。

## リストの詳細

表示される製品情報には、次の情報が含まれます。

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![リストの詳細](assets/amazon-product-listing-details.png){width="600" zoomable="yes"}

## アクティビティログの一覧表示 {#listing-activity-log}

Amazon一覧の最近のアクティビティをすべて表示します。 表示される情報は次のとおりです。

- Amazon販売者 SKU：リストに定義された Stock Keeping Unit(SKU) を識別します。
- ASIN: 10 桁のAmazon製品 ID。
- リストアクション：リストに対して発生したアクションのタイプを識別します。
- コメント：発生したリストアクションのタイプに関する追加の詳細を提供します。
- 実行時刻：アクションが発生した日時を識別します。

![製品リストの詳細 — アクティビティログのリスト](assets/amazon-listing-activity-log.png){width="600" zoomable="yes"}
__

## Buy Boxの競合相手の価格 {#buy-box-competitor-pricing}

このタブには、 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) リストの位置。 この情報を使用して、Amazonでの競合他社の価格の位置付けを理解できます。 表示される情報は次のとおりです。

- ASIN:10 桁のAmazon製品 ID。
- Is Seller：自分が [!DNL Buy Box] 売り手 オプションはい/いいえ。
- 条件：リストに定義された条件を識別します。
- 上場価格：上場が発行された価格を識別します。
- 出荷価格：リストに追加された出荷価格を識別します。
- 上場価格：上場価格とリストの送料を加えた値です。
- 最終更新：価格情報がAmazonから更新された日時を識別します。

![製品リストの詳細：Buy Boxの競合他社の価格](assets/amazon-listing-details-buy-box-2.png){width="600" zoomable="yes"}

## 競合相手の最も低い価格 {#lowest-competitor-pricing}

このタブには、同じリストに関するAmazonの競合相手に関する情報が表示されます。 この情報は、価格の位置付けと [最も低い競合他社価格](./lowest-competitor-pricing.md). 表示される情報は次のとおりです。

- ASIN:10 桁のAmazon製品 ID。
- 条件：リストに定義された条件を識別します。
- 達成チャネル：履行の責任者を識別します。 オプション：マーチャント/Amazon。
- 上場価格：上場が発行された価格を識別します。
- 出荷価格：リストに追加された出荷価格を識別します。
- 上場価格：上場価格とリストの送料を加えた値です。
- フィードバック評価：最低価格の商人のAmazonフィードバック評価を識別します。
- フィードバック数：最低価格の商人に対するAmazonのフィードバック数を識別します。
- 最終更新：価格情報がAmazonから更新された日時を識別します。

![製品リストの詳細 — 競合相手の最も低い価格](assets/amazon-listing-details-lowest-comp.png){width="600" zoomable="yes"}
