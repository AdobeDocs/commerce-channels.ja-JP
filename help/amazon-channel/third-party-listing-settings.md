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

サードパーティのリスト設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定は、[!DNL Commerce] カタログが既存の [!DNL Amazon Seller Central] ータリストから製品を読み込むかどうかを決定します。 Amazonからリストをインポートして、すべてのリストが一致する商品を持つようにする [!DNL Commerce] とをお勧めします。 リストが [!DNL Commerce] カタログの一部になっている場合は、1 つのカタログからすべての商品を管理し、Amazonのセールスチャネル機能を使用できます。 これらの機能には、Amazonを使用したフルフィルメントと注文管理、インテリジェントな再価格設定、数量の管理が含まれます。

Amazonの番組表を読み込むように設定されている場合、Amazonの営業チャネルは、既存の商品との照合を試みながら、Amazonの番組表を [!DNL Commerce] カタログに読み込みます。 一致が自動的に見つからない場合は、Amazonのリストを新しい [!DNL Commerce] 商品として読み込むか、手動でリストを商品に一致させることができます。

Amazonのリストを読み込む場合は、Amazon Seller SKU およびAmazon ASIN の値を持つ [!DNL Commerce] 属性を選択します。 [ 製品属性 ](./ob-creating-magento-attributes.md) が [!DNL Commerce] い場合は、作成して割り当てることを検討してください。 これらの属性をマッピングすると、読み込んだAmazonのリストを [!DNL Commerce] の製品と正しく一致させることができます。

[ ストアの統合 ](./store-integration.md) が完了すると、最初のリストの読み込みが開始されます。 その後、[!DNL Commerce] は cron の設定に基づいて、新しく追加された（Amazon Sales Channelでは作成されていない）Amazonのリストを継続的に確認し、サードパーティのリスト設定に従って [!DNL Commerce] カタログを更新します。

## サードパーティリスト設定の指定

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL Third Party Listings]_」セクションを展開します。

1. **[!UICONTROL Import Third Party Listings]** （必須）には、次のいずれかのオプションを選択します。

   - `Import Listing` - （デフォルト）Amazonのリストの商品情報を [!DNL Commerce] の商品カタログに読み込むタイミングを選択します。 これはデフォルトのオプションであり、推奨されます。

   - `Do Not Import Listing` - Amazon リストの [!DNL Commerce] カタログに手動で [ 新しい商品を作成して割り当てる ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) タイミングを選択します。

   >[!NOTE]
   >次のオプションフィールドは、を `Import Listing` に設定した場合にのみアクティブになります。

1. **[!UICONTROL Attribute That Contains Amazon Seller SKU]** しくは、Amazonの販売者 SKU 値に一致する [!DNL Commerce] 属性を選択します。

1. **[!UICONTROL Attribute That Contains Amazon ASIN]**：作成した [!DNL Commerce] 属性を選択して、Amazon ASIN と一致させます。

   >[!NOTE]
   >Amazon リストにこれらの [!DNL Commerce] 属性を作成しなかった場合は、[Amazon マッチングの属性の作成 ](./ob-creating-magento-attributes.md) を参照してください。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ 第三者上場 ](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | 必須。 オプション：<ul><li>**[!UICONTROL Import Listing]** - （デフォルト）Amazonのリストの商品情報を [!DNL Commerce] の商品カタログに読み込むタイミングを選択します。 </li><li>**[!UICONTROL Do Not Import Listing]** - Amazon リストの [!DNL Commerce] カタログに手動で [ 新しい商品を作成して割り当てる ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) タイミングを選択します。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | `Import Listing` に設定した場合にのみアクティブになります。<br>[!DNL Commerce] 属性を、Amazon Seller SKU のAmazon属性と一致するように選択します。 この属性が存在しない場合は、[Amazon マッチングのためのAmazon製品属性の作成 ](./ob-creating-magento-attributes.md) を参照してください。 必要に応じて、[!DNL Commerce] [ 属性 ](./managing-attributes.md) を確認し、このAmazon データに一致する属性を作成または編集します。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | `Import Listing` に設定した場合にのみアクティブになります。<br>Amazon ASIN のAmazon属性に一致する [!DNL Commerce] 属性を選択します。 この属性が存在しない場合は、[Amazon マッチングのためのAmazon製品属性の作成 ](./ob-creating-magento-attributes.md) を参照してください。 必要に応じて、[!DNL Commerce] [ 属性 ](./managing-attributes.md) を確認し、このAmazon データに一致する属性を作成または編集します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
