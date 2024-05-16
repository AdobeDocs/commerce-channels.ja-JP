---
title: AmazonSales Channel- [!UICONTROL Third-party Listings]
description: サードパーティのリスト設定を更新して、Commerce カタログが既存のAmazon Seller Central のリストから商品を読み込むかどうかを判断します。
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

サードパーティのリスト設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、 [!DNL Commerce] カタログは、既存の製品から製品を読み込みます [!DNL Amazon Seller Central] listings. Amazonからリストをインポートして、すべてのリストが一致するようにすることをお勧めします [!DNL Commerce] 製品。 一覧が自分の [!DNL Commerce] カタログを使用すると、1 つのカタログからすべての商品を管理し、Amazonのセールスチャネル機能を使用できます。 これらの機能には、Amazonを使用したフルフィルメントと注文管理、インテリジェントな再価格設定、数量の管理が含まれます。

Amazonのリストを読み込むように設定すると、AmazonのセールスチャネルによってAmazonのリストがユーザーの [!DNL Commerce] カタログ。既存の製品と照合しようとしています。 一致が自動的に見つからない場合は、Amazon リストを新しいリストとして読み込むことができます [!DNL Commerce] 製品を検索するか、リストを製品と手動で照合します。

Amazonのリストを読み込む場合は、 [!DNL Commerce] Amazon Seller SKU およびAmazon ASIN の値を持つ属性。 持っていない場合 [!DNL Commerce] [製品属性](./ob-creating-magento-attributes.md)を作成し、割り当てることを検討してください。 これらの属性をマッピングすると、読み込んだAmazonのリストをユーザーの [!DNL Commerce] 製品。

最初のリストの読み込みは次の場合に開始されます [ストアの統合](./store-integration.md) が完了しました。 その後、cron 設定に基づいて、 [!DNL Commerce] 新しく追加された（Amazon Sales Channelで作成されていない）Amazon リストを継続的にチェックし、 [!DNL Commerce] サードパーティのリスト設定に従ったカタログ。

## サードパーティリスト設定の指定

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 _[!UICONTROL Third Party Listings]_セクション。

1. の場合 **[!UICONTROL Import Third Party Listings]** （必須）、次のいずれかのオプションを選択します。

   - `Import Listing` - （デフォルト）Amazonのリストの商品情報をのに読み込むタイミングを選択します [!DNL Commerce] 商品カタログ。 これはデフォルトのオプションであり、推奨されます。

   - `Do Not Import Listing`  – 手動で実行するタイミングを選択します [新製品の作成と割り当て](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) 宛先： [!DNL Commerce] Amazonのリストのカタログ。

   >[!NOTE]
   >次のオプションフィールドは、に設定されている場合にのみ有効です。 `Import Listing`.

1. の場合 **[!UICONTROL Attribute That Contains Amazon Seller SKU]**、を選択します [!DNL Commerce] Amazon セラー SKU 値に一致する属性。

1. の場合 **[!UICONTROL Attribute That Contains Amazon ASIN]**、を選択します [!DNL Commerce] 作成した属性とAmazon ASIN を一致させます。

   >[!NOTE]
   >これらを作成していない場合 [!DNL Commerce] Amazon リストの属性。を参照してください。 [Amazonのマッチングの属性の作成](./ob-creating-magento-attributes.md).

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![サードパーティのリスト](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | 必須。 オプション：<ul><li>**[!UICONTROL Import Listing]** - （デフォルト）Amazonのリストの商品情報をのに読み込むタイミングを選択します [!DNL Commerce] 商品カタログ。 </li><li>**[!UICONTROL Do Not Import Listing]**  – 手動で実行するタイミングを選択します [新製品の作成と割り当て](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) 宛先： [!DNL Commerce] Amazonのリストのカタログ。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | に設定されている場合のみアクティブ `Import Listing`.<br>を選択します。 [!DNL Commerce] Amazon セラー SKU のAmazon属性と一致する属性です。 この属性が存在しない場合は、を参照してください [Amazonのマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md). 必要に応じて、 [!DNL Commerce] [属性](./managing-attributes.md) このAmazon データに一致する属性を作成または編集します。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | に設定されている場合のみアクティブ `Import Listing`.<br>を選択します。 [!DNL Commerce] Amazon ASIN のAmazon属性に一致する属性。 この属性が存在しない場合は、を参照してください [Amazonのマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md). 必要に応じて、 [!DNL Commerce] [属性](./managing-attributes.md) このAmazon データに一致する属性を作成または編集します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
