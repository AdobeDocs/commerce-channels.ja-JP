---
title: リストの詳細の表示
description: Amazonのリストや個々のSKU/製品の変更に関する競合指標を理解するには、製品リストの詳細ページを参照してください。
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# リストの詳細の表示

_[!UICONTROL Product Listing Details]_ページには、個々のSKU /製品の変更を表示する「リストアクティビティログ」など、アクティブな製品リストに関する追加情報が表示されます。 この情報は、製品や個々のSKU/製品の変更に関する競合上の指標を理解するのに役立ちます。 このページには、次のような追加情報が含まれます。

- **[!UICONTROL Listing Details]**  — 製品の詳細(名前、Amazon Seller SKUなど)
- **[!UICONTROL Listing Activity Log]**  — 価格や数量/在庫の変更など、このリストに対して発生したすべての変更の履歴記録。それ以上のアクションは不要です。 このログは、変更履歴を理解するためのレビュー用に提供されます。
- **[!UICONTROL Buy Box Competitor Pricing]** - Amazonのステータスと競合 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 相手の価格に関するデータ
- **[!UICONTROL Lowest Competitor Pricing]**  — 最も低いAmazonの競合他社の価格とフィードバック情報に関する情報

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

## リストの詳細

表示される製品情報は次のとおりです。

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![リストの詳細](assets/amazon-product-listing-details.png)

## アクティビティログの一覧表示 {#listing-activity-log}

Amazonリストの最近のアクティビティをすべて表示します。 表示される情報は次のとおりです。

- Amazon販売者SKU:リストに定義された在庫管理単位(SKU)を識別します。
- ASIN:10桁のAmazon製品識別子を識別します。
- リストアクション：リストに対して発生したアクションのタイプを識別します。
- コメント：発生したリストアクションのタイプに関する追加の詳細を示します。
- 実行日：アクションが発生した日時を識別します。

![製品リストの詳細 — アクティビティログのリスト](assets/amazon-listing-activity-log.png)
__

## Buy Box競合他社の価格 {#buy-box-competitor-pricing}

このタブには、リストの[[!DNL Buy Box]](./buy-box-competitor-pricing.md)ポジションを保持しているAmazonの商人に関する情報が表示されます。 この情報を使用して、Amazonでの競合他社の価格の位置付けを把握できます。 表示される情報は次のとおりです。

- ASIN:10桁のAmazon製品ID。
- 販売者：自分が[!DNL Buy Box]の販売者であるかどうかを示します。 オプションはい/いいえ。
- 条件：リスト用に定義された条件を識別します。
- 上場価格：リストが発行された価格を示します。
- 送料：リストに追加された出荷価格を識別します。
- 地価：リストの価格と出荷価格を識別します。
- 最終更新日：価格情報がAmazonから更新された日時を識別します。

![製品リストの詳細：Buy Box競合他社の価格](assets/amazon-listing-details-buy-box-2.png)

## 競合他社の最低価格 {#lowest-competitor-pricing}

このタブには、同じリストにあるAmazonの競合相手に関する情報が表示されます。 この情報は、価格の位置づけと[競合相手の最も低い価格](./lowest-competitor-pricing.md)を理解するために使用できます。 表示される情報は次のとおりです。

- ASIN:10桁のAmazon製品ID。
- 条件：リスト用に定義された条件を識別します。
- フルフィルメントチャネル：履行の責任を負う当事者を特定します。 オプション：商人/Amazon
- 上場価格：リストが発行された価格を示します。
- 送料：リストに追加された出荷価格を識別します。
- 地価：リストの価格と出荷価格を識別します。
- フィードバック評価：最低価格の商人のAmazonフィードバック評価を識別します。
- フィードバック数：最低価格の商人のAmazonフィードバック数を識別します。
- 最終更新日：価格情報がAmazonから更新された日時を識別します。

![製品リストの詳細 — 競合他社の最も低い価格](assets/amazon-listing-details-lowest-comp.png)
