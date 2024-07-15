---
title: 新しいサードパーティAmazonのリスト
description: 新しいAmazonのリストを管理するには、Commerce カタログ内の製品と照合します。
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# 新しいサードパーティAmazonのリスト

「_[!UICONTROL New Third Party]_」タブには、[!DNL Commerce] カタログ内の商品と一致していない既存のAmazonのリストが表示されます。 数量、価格、処理時間などに対してリスト管理を使用するには、各Amazonのリストが [!DNL Commerce] カタログの商品に一致（割り当て）する必要があります。 [!DNL Commerce] カタログ内の製品にリストを割り当てるには、いくつかのオプションがあります。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Create New Catalog Product(s)]**: Amazon リストの情報を使用して、[!DNL Commerce] カタログに商品を自動作成することを選択します。 このプロセスは、Amazonのリストを新しいカタログ商品と自動的に照合します。 [ カタログ製品の作成と割り当て ](./creating-assigning-catalog-products.md) を参照してください。

- **[!UICONTROL Attempt Automatic Match]**：リスト設定の現在の [ カタログ検索 ](./catalog-search.md) オプションに基づいて、選択したリストをカタログに自動照合することを選択します。 _[!UICONTROL Catalog Search]_のオプションを変更した場合、このアクションを使用すると、照合プロセスを再試行できます。

_[!UICONTROL Select]_の下：

- **[!UICONTROL Assign Catalog Product]**：リストを [!DNL Commerce] カタログ内の製品と手動で照合することを選択します。 [ カタログ製品の作成と割り当て ](./creating-assigning-catalog-products.md) を参照してください。

- **[!UICONTROL Create New Catalog Product]**: Amazon リストの情報を使用して、[!DNL Commerce] カタログに商品を自動作成することを選択します。 このプロセスは、Amazonのリストを新しいカタログ商品と自動的に照合します。 [ カタログ製品の作成と割り当て ](./creating-assigning-catalog-products.md) を参照してください。

- **[!UICONTROL View Details]**: [ リスト活動ログ ](./product-listing-details.md#listing-activity-log)、[Buy Box競合他社価格 ](./product-listing-details.md#buy-box-competitor-pricing)、および [ 最低競合他社価格 ](./product-listing-details.md#lowest-competitor-pricing) を含むリスト詳細を表示します。 このアクションは表示専用です。 リストの詳細は変更できません。 [ 詳細を表示 ](./product-listing-details.md) を参照してください。

>[!NOTE]
>
>処理中のリストがある場合、タブの上に、リスト数を示すメッセージが表示されます。

![ 新しいサード パーティの一覧 ](assets/amazon-listings-new-third-party.png){width="600" zoomable="yes"}

Amazon sales channel のホームページには、表示するデータをカスタマイズできる共通の [workspace コントロール ](./workspace-controls.md) がいくつか用意されています。

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は [!DNL Amazon Standard Identification Number] を表す。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | 商品の [ 条件 ](./product-listing-condition.md)。 |
| [!UICONTROL Listing Price] | 価格ソースおよび該当する価格ルールで定義された、品目の上場価格を識別します。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、オプションを選択します。<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
