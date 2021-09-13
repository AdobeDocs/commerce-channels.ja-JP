---
title: サードパーティ製品リスト
description: サードパーティのリスト設定を更新して、コマースカタログで既存のAmazon Seller Centralリストから製品をインポートするかどうかを決定します。
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# サードパーティ製品リスト

サードパーティのリスト設定は、ストアリスト設定の一部です。 リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定は、[!DNL Commerce]カタログが既存の[!DNL Amazon Seller Central]リストから製品を読み込むかどうかを決定します。 すべてのリストに[!DNL Commerce]製品が一致するように、Amazonからリストを読み込むことをお勧めします。 リストが[!DNL Commerce]カタログに含まれている場合は、1つのカタログからすべての製品を管理し、Amazonの販売チャネル機能を使用できます。 これらの機能には、Amazonによるフルフィルメントと注文管理、インテリジェントな価格変更、数量管理が含まれます。

Amazonのリストをインポートするように設定すると、Amazonの販売チャネルはAmazonのリストを[!DNL Commerce]カタログにインポートし、既存の製品と照合します。 一致が自動的に見つからない場合は、Amazonリストを新しい[!DNL Commerce]製品として読み込むか、手動で製品に一致させます。

Amazonのリストを読み込む場合は、AmazonセラーSKUとAmazon ASINの値を持つ[!DNL Commerce]属性を選択します。 [!DNL Commerce] [製品属性](./ob-creating-magento-attributes.md)がない場合は、それらを作成して割り当てることを検討してください。 これらの属性をマッピングすると、読み込んだAmazonのリストを[!DNL Commerce]製品と正しく一致させることができます。

[ストア統合](./store-integration.md)が完了すると、最初のリストインポートが開始されます。 その後、cronSales Channelに基づいて、[!DNL Commerce]は新しく追加されたAmazonリストを(Amazon設定ではなく)継続的に確認し、サードパーティのリスト設定に従って[!DNL Commerce]カタログを更新します。

## サードパーティリストの設定

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL Third Party Listings]_セクションを展開します。

1. **[!UICONTROL Import Third Party Listings]**（必須）には、次のオプションを選択します。

   - `Import Listing` - （デフォルト）Amazonのリストから製品情報を製品カタログに読み込む場合に [!DNL Commerce] 選択します。このオプションはデフォルトで、お勧めします。

   - `Do Not Import Listing`  — 新しい商品を手動で作成し [て](https://docs.magento.com/user-guide/catalog/products.html)、Amazonの一覧のカタログに割り当てる場合に選択しま [!DNL Commerce] す。{:target=&quot;_blank&quot;}
   >[!NOTE]
   >次のオプションフィールドは、 `Import Listing`に設定した場合にのみ有効です。

1. **[!UICONTROL Attribute That Contains Amazon Seller SKU]**&#x200B;の場合、Amazonの販売者SKU値に対応する[!DNL Commerce]属性を選択します。

1. **[!UICONTROL Attribute That Contains Amazon ASIN]**&#x200B;の場合は、作成した[!DNL Commerce]属性を選択し、Amazon ASINに合わせます。

   >[!NOTE]
   >Amazonのリスト用にこれらの[!DNL Commerce]属性を作成しなかった場合は、[Amazonのマッチング用の属性の作成](./ob-creating-magento-attributes.md)を参照してください。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![サードパーティのリスト](assets/amazon-third-party-listings.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Import Third Party Listings] | 必須。 オプション：<ul><li>**[!UICONTROL Import Listing]** - （デフォルト）Amazonのリストから製品情報を製品カタログに読み込む場合に [!DNL Commerce] 選択します。 </li><li>**[!UICONTROL Do Not Import Listing]**  — 新しい商品を手動で作成し [て](https://docs.magento.com/user-guide/catalog/products.html)、Amazonの一覧のカタログに割り当てる場合に選択しま [!DNL Commerce] す。{:target=&quot;_blank&quot;}</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | `Import Listing`に設定された場合にのみ有効です。<br>Amazonセラ [!DNL Commerce] ーSKUのAmazon属性に一致する属性を選択します。この属性が存在しない場合は、[Amazonのマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md)を参照してください。 必要に応じて、[!DNL Commerce] [属性](./managing-attributes.md)を確認し、このAmazonデータに合致する属性を作成または編集します。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | `Import Listing`に設定された場合にのみ有効です。<br>Amazon ASIN [!DNL Commerce] のAmazon属性に一致する属性を選択します。この属性が存在しない場合は、[Amazonのマッチング用のAmazon製品属性の作成](./ob-creating-magento-attributes.md)を参照してください。 必要に応じて、[!DNL Commerce] [属性](./managing-attributes.md)を確認し、このAmazonデータに合致する属性を作成または編集します。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
