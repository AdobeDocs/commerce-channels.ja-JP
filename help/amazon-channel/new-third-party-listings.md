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

この _[!UICONTROL New Third Party]_tab キーを押すと、の商品と一致していない既存のAmazonのリストが表示されます [!DNL Commerce] カタログ。 数量、価格、処理時間などに対してリスト管理を使用するには、各Amazonのリストを自分の商品に一致させる（割り当てる）必要があります [!DNL Commerce] カタログ。 リストを製品に割り当てるには、 [!DNL Commerce] カタログ。

次の下 _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**:Amazonリストの情報を使用して、に商品を自動作成することを選択します [!DNL Commerce] カタログ。 このプロセスは、Amazonのリストを新しいカタログ商品と自動的に照合します。 参照： [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**：現在の設定に基づいて、カタログに対して選択されたリストの自動照合を試みるように選択します [カタログ検索](./catalog-search.md) リスト設定のオプション。 を変更した場合 _[!UICONTROL Catalog Search]_オプション。このアクションを使用すると、一致するプロセスを再試行できます。

次の下 _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**：リストを内の製品と照合するように選択します [!DNL Commerce] カタログを手動で。 参照： [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**:Amazonリストの情報を使用して、に商品を自動作成することを選択します [!DNL Commerce] カタログ。 このプロセスは、Amazonのリストを新しいカタログ商品と自動的に照合します。 参照： [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**：次のようなリストの詳細を表示することを選択します [アクティビティログを一覧表示](./product-listing-details.md#listing-activity-log), [Buy Box競合他社価格](./product-listing-details.md#buy-box-competitor-pricing)、および [競合製品の最低価格](./product-listing-details.md#lowest-competitor-pricing). このアクションは表示専用です。 リストの詳細は変更できません。 参照： [詳細を表示](./product-listing-details.md).

>[!NOTE]
>
>処理中のリストがある場合、タブの上に、リスト数を示すメッセージが表示されます。

![新しいサードパーティの一覧](assets/amazon-listings-new-third-party.png){width="600" zoomable="yes"}

Amazonのセールスチャネルのホームページには、いくつかの共通点があります [workspace コントロール](./workspace-controls.md) 表示するデータをカスタマイズできます。

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は AEM を表す [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | この [条件](./product-listing-condition.md) 商品の。 |
| [!UICONTROL Listing Price] | 価格ソースおよび該当する価格ルールで定義された、品目の上場価格を識別します。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列を選択してオプションを選択します。<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
