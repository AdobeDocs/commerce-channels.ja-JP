---
title: サードパーティの新リスト
description: 新しい Amazon リストを管理するために、Commerce カタログ内の1つの製品に一致させることができます。
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# サードパーティの新リスト

このタブには、 _[!UICONTROL New Third Party]_カタログ内の製品に対応していない既存の Amazon リストが表示され [!DNL Commerce] ます。 数、価格、処理時間などを表示するには、各 Amazon リストがカタログ内の製品に適合している必要があり [!DNL Commerce] ます。 カタログ内の製品に一覧を割り当てるには、いくつかの方法があり [!DNL Commerce] ます。

_[!UICONTROL Actions]_以下に示します。

- **[!UICONTROL Create New Catalog Product(s)]**: Amazon リストに記載されている情報を使用して、カタログに製品を自動的に作成することが [!DNL Commerce] できます。 この処理によって、Amazon リスティングが新しいカタログ製品に自動的に照合されます。 詳しくは [ 、カタログ製品の作成と割り当てを参照してください ](./creating-assigning-catalog-products.md) 。

- **[!UICONTROL Attempt Automatic Match]**: 現在のカタログ検索オプションを使用して、選択されているリストについてカタログへ自動的に一致するように選択し [ ](./catalog-search.md) ます。 オプションを変更すると _[!UICONTROL Catalog Search]_、このアクションによって、照合処理を再実行できるようになります。

_[!UICONTROL Select]_以下に示します。

- **[!UICONTROL Assign Catalog Product]**: カタログ内の製品の一覧を手動で検索する場合に選択し [!DNL Commerce] ます。 詳しくは [ 、カタログ製品の作成と割り当てを参照してください ](./creating-assigning-catalog-products.md) 。

- **[!UICONTROL Create New Catalog Product]**: Amazon リストに記載されている情報を使用して、カタログに製品を自動的に作成することが [!DNL Commerce] できます。 この処理によって、Amazon リスティングが新しいカタログ製品に自動的に照合されます。 詳しくは [ 、カタログ製品の作成と割り当てを参照してください ](./creating-assigning-catalog-products.md) 。

- **[!UICONTROL View Details]**: 一覧表示された [ 利用状況ログ、購入ボックスの価格、競合企業の価格が表示さ ](./product-listing-details.md#listing-activity-log) [ ](./product-listing-details.md#buy-box-competitor-pricing) [ ](./product-listing-details.md#lowest-competitor-pricing) れます。 このアクションは、表示専用です。 一覧の詳細に変更を加えることはできません。 [詳しくは、詳細の表示を参照してください ](./product-listing-details.md) 。

>[!NOTE]
>
>リストが進行中である場合は、リストの数を示すタブの上にメッセージが表示されます。

![サードパーティリストの新規作成](assets/amazon-listings-new-third-party.png)

Amazon セールスチャンネルのホームページ [ ](./workspace-controls.md) は、表示されるデータをカスタマイズするための一般的なワークスペースコントロールの一部を共有しています。

## デフォルトの列

| 段 | つい |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>「アーク」は、 [!DNL Amazon Standard Identification Number] . アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Condition] | [ ](./product-listing-condition.md) 製品の状態。 |
| [!UICONTROL Listing Price] | 価格ソースによって定義された品目の定価を指定します。適用可能な価格ルールが表示されます。 |
| [!UICONTROL Amazon Quantity] | この製品が Amazon に積極的に一覧表示されるときに使用可能な数量です。 |
| [!UICONTROL Status] | Amazon によって定義される一覧の状態。 |
| [!UICONTROL Action] | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、列内をクリックし、次のいずれ **[!UICONTROL Select]** _[!UICONTROL Action]_かのオプションを選択します。<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
