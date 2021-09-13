---
title: 新しいサードパーティ製リスト
description: 新しいAmazonリストをコマースカタログ内の製品と照合して管理します。
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 新しいサードパーティのリスト

「_[!UICONTROL New Third Party]_」タブには、[!DNL Commerce]カタログ内の製品と一致しない既存のAmazonリストが表示されます。 数量、価格、処理時間などのリスト管理を使用するには、Amazonの各リストを[!DNL Commerce]カタログ内の製品と照合（割り当て）する必要があります。 [!DNL Commerce]カタログ内の製品にリストを割り当てる方法はいくつかあります。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Create New Catalog Product(s)]**:Amazonリストの情報を使用して、カタログに商品を自動的に作成するように選択 [!DNL Commerce] します。このプロセスは、Amazonのリストを新しいカタログ製品に自動的に一致させます。 [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md)を参照してください。

- **[!UICONTROL Attempt Automatic Match]**:現在のカタログ検索オプションに基づいて、選択したリストをカタログに自動一致させ [る](./catalog-search.md) 場合に選択します。_[!UICONTROL Catalog Search]_オプションを変更した場合は、この操作により、一致する処理を再試行できます。

_[!UICONTROL Select]_の下：

- **[!UICONTROL Assign Catalog Product]**:カタログ内の製品とリストを手動で一致させるように [!DNL Commerce] 選択します。[カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md)を参照してください。

- **[!UICONTROL Create New Catalog Product]**:Amazonリストの情報を使用して、カタログに商品を自動的に作成するように選択 [!DNL Commerce] します。このプロセスは、Amazonのリストを新しいカタログ製品に自動的に一致させます。 [カタログ製品の作成と割り当て](./creating-assigning-catalog-products.md)を参照してください。

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

>[!NOTE]
>
>処理中のリストがある場合、タブの上にメッセージが表示され、リストの数が示されます。

![新しいサードパーティのリスト](assets/amazon-listings-new-third-party.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Listing Price] | 価格ソースおよび適用可能な価格ルールで定義された品目の上場価格を識別します。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた場合に使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス(Amazonで定義)。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
