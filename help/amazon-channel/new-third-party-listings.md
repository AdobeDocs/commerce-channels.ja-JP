---
title: 新しいサードパーティ製品リスト
description: 新しいAmazonリストをコマースカタログの製品と照合して管理します。
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 新しいサードパーティ製品リスト

この _[!UICONTROL New Third Party]_「 」タブには、お使いのAmazonの製品に一致しない既存の製品リストが表示されます [!DNL Commerce] カタログ。 数量、価格、処理時間などのリスト管理を使用するには、Amazonの各リストを製品に対して照合（割り当て）する必要があります [!DNL Commerce] カタログ。 リストを [!DNL Commerce] カタログ。

の下 _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**:Amazonリストの情報を使用して、 [!DNL Commerce] カタログ。 このプロセスは、Amazonリストを新しいカタログ製品に自動的に一致させます。 詳しくは、 [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**:現在の [カタログ検索](./catalog-search.md) 」オプションを使用します。 次の変更を加えた場合、 _[!UICONTROL Catalog Search]_オプションを指定すると、一致するプロセスを再試行できます。

の下 _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**:リストとの一致を、 [!DNL Commerce] カタログを手動で作成します。 詳しくは、 [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**:Amazonリストの情報を使用して、 [!DNL Commerce] カタログ。 このプロセスは、Amazonリストを新しいカタログ製品に自動的に一致させます。 詳しくは、 [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**：リストの詳細 ( [アクティビティログのリスト](./product-listing-details.md#listing-activity-log), [Buy Box競合他社の価格](./product-listing-details.md#buy-box-competitor-pricing)、および [競合他社の最低価格](./product-listing-details.md#lowest-competitor-pricing). このアクションは表示専用です。 リストの詳細は変更できません。 詳しくは、 [詳細を表示](./product-listing-details.md).

>[!NOTE]
>
>処理中のリストがある場合、タブの上にメッセージが表示され、リストの数を示します。

![新しいサードパーティのリスト](assets/amazon-listings-new-third-party.png)

Amazonセールスチャネルのホームページは、いくつかの共通を共有します [workspace コントロール](./workspace-controls.md) を使用すると、表示されるデータをカスタマイズできます。

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | 製品、オプション、価格および製造元を識別するために、Amazonが製品に割り当てた SKU(Stock Keeping Unit)。 |
| [!UICONTROL ASIN] | アイテムを識別する 10 文字または数字の一意のブロック。<br><br>ASIN は、 [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字の一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合は、アイテムがカタログにアップロードされると新しい ASIN が作成されます。 ASIN は、Amazonの製品の詳細ページに、その品目に関する詳細と共に表示されます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | この [条件](./product-listing-condition.md) 製品の。 |
| [!UICONTROL Listing Price] | 価格ソースおよび適用可能な価格ルールで定義された品目の上場価格を識別します。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされたときに使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス (Amazonで定義 )。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、 **[!UICONTROL Select]** 内 _[!UICONTROL Action]_列を選択し、次のオプションを選択します。<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
