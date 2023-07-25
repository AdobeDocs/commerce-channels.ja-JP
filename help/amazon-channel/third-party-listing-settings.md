---
title: AmazonSales Channel- [!UICONTROL Third-party Listings]
description: サードパーティのリスト設定を更新して、コマースカタログで既存のAmazon Seller Central リストから製品を読み込むかどうかを決定します。
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

サードパーティのリスト設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、 [!DNL Commerce] カタログは、既存のから製品を読み込みます [!DNL Amazon Seller Central] リスト すべてのリストが一致するように、Amazonからリストを読み込むことをお勧めします [!DNL Commerce] 製品。 リストが [!DNL Commerce] カタログを使用すると、1 つのカタログからすべての製品を管理し、Amazonセールスチャネル機能を使用できます。 これらの機能には、Amazonによる達成と注文管理、インテリジェントな価格変更、数量管理が含まれます。

Amazonのリストをインポートするように設定すると、AmazonのセールスチャネルはAmazonのリストを [!DNL Commerce] カタログを作成し、既存の製品と照合します。 一致が自動的に見つからない場合は、Amazonリストを新しい [!DNL Commerce] 製品を選択するか、リストを手動で製品に一致させます。

Amazonリストを読み込む場合は、 [!DNL Commerce] 属性の値がAmazon Seller SKU およびAmazon ASIN の値に一致する。 次の条件を満たしていない場合、 [!DNL Commerce] [製品属性](./ob-creating-magento-attributes.md)を使用する場合は、作成して割り当てることを検討します。 これらの属性をマッピングすると、読み込まれたAmazonのリストを [!DNL Commerce] 製品。

最初のリストのインポートは、 [ストア統合](./store-integration.md) が完了しました。 その後、Cron 設定に基づいて [!DNL Commerce] 新しく追加されたAmazonリスト (AmazonSales Channelでは作成されない ) を継続的に確認し、 [!DNL Commerce] サードパーティのリスト設定に従ってカタログを作成します。

## サードパーティのリスト設定の構成

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL Third Party Listings]_」セクションに入力します。

1. の場合 **[!UICONTROL Import Third Party Listings]** （必須）、次のオプションを選択します。

   - `Import Listing` - （デフォルト）Amazonの一覧から製品情報を読み込むタイミングを選択します [!DNL Commerce] 商品カタログ このオプションはデフォルトで、お勧めします。

   - `Do Not Import Listing`  — 手動で行うタイミングを選択 [新しい製品の作成と割り当て](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) を [!DNL Commerce] Amazonリスト用のカタログ

   >[!NOTE]
   >次のオプションフィールドは、 `Import Listing`.

1. の場合 **[!UICONTROL Attribute That Contains Amazon Seller SKU]**、 [!DNL Commerce] 属性の値がAmazon Seller SKU 値に一致する場合。

1. の場合 **[!UICONTROL Attribute That Contains Amazon ASIN]**、 [!DNL Commerce] 属性を作成し、Amazon ASIN と照合します。

   >[!NOTE]
   >これらを作成しなかった場合 [!DNL Commerce] Amazonのリストの属性については、 [Amazonマッチングの属性の作成](./ob-creating-magento-attributes.md).

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![サードパーティのリスト](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | 必須。 オプション：<ul><li>**[!UICONTROL Import Listing]** - （デフォルト）Amazonの一覧から製品情報を読み込むタイミングを選択します [!DNL Commerce] 商品カタログ </li><li>**[!UICONTROL Do Not Import Listing]**  — 手動で行うタイミングを選択 [新しい製品の作成と割り当て](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) を [!DNL Commerce] Amazonリスト用のカタログ</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 次に設定した場合にのみ有効 `Import Listing`.<br>を選択します。 [!DNL Commerce] 属性をAmazonセラー SKU のAmazon属性に一致させる。 この属性が存在しない場合は、 [Amazonマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md). 必要に応じて、 [!DNL Commerce] [属性](./managing-attributes.md) このAmazonデータに一致する属性を作成または編集します。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 次に設定した場合にのみ有効 `Import Listing`.<br>を選択します。 [!DNL Commerce] Amazon ASIN のAmazon属性に一致する属性。 この属性が存在しない場合は、 [Amazonマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md). 必要に応じて、 [!DNL Commerce] [属性](./managing-attributes.md) このAmazonデータに一致する属性を作成または編集します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
