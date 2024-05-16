---
title: AmazonSales Channel- [!UICONTROL Stock/Quantity]
description: Commerce ストアからユーザーへの製品数量の詳細の同期を制御するには [!DNL Amazon Seller Central] アカウントで、在庫/数量設定を更新します。
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]* 設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、の製品数量の詳細を同期するために使用されます [!DNL Commerce] ストアフロントからのご注文 [!DNL Amazon Seller Central] アカウント。 このツールは強力で、在庫を整理しながら購入者に緊急度を表示することで、追加の広告に使用できます。 例えば、一部のマーチャントは、倉庫内に特定の SKU の 150 個の商品があり、Amazonの買い物客が在庫全体を購入できるようにする必要がある場合があります。 他のマーチャントは、エンドユーザーに希少感を与えるために、一度に 1 つの項目のみをリストしたい場合があります。 この場合、を設定します *[!UICONTROL Maximum Listed Quantity]* 対象： `1`.

数量は地域属性で、 **[!UICONTROL Amazon Marketplace Country]** 設定中の定義 [ストアの統合](./store-integration.md). 製品の数量を変更すると、その変更は、その製品を共有するすべてのAmazonのリストに影響します [!DNL Amazon Seller SKU] 同じ国で販売されているAmazonの店舗で。 共有へのの変更 [!DNL Amazon Seller SKU] 米国では、別の国に設定されたAmazonのストアには影響しません。 数量の設定では、統合された（最も古い作成日を持つ）最初のAmazon ストアが優先度を制御します。

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source 2.3.x を使用しているユーザーの場合、Amazon sales channel では、追加の設定を行わずにInventory management拡張機能の使用をサポートしています。 参照： [在庫の管理](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## 在庫/数量の設定 {#configure-stock--quantity-settings}

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 **[!UICONTROL Stock / Quantity]** セクション。

1. の場合 **[!UICONTROL Out-of-Stock Threshold]** （必須）商品をAmazonリストに登録するには、商品の最小数量を表す数値を入力します。

   デフォルトはです `0`. 次の場合 [!DNL Commerce] 商品の在庫がこの数を下回る場合、それぞれのAmazon リストはAmazonを通じた販売に対して不適格となります。

1. の場合 **[!UICONTROL Maximum Listed Quantity]** （必須） Amazon リストに表示する数量の数値を入力します。

   この設定では、入力した値に適格なすべてのAmazonのリストを表示します。 商品が販売されても、Amazonのリスト数量は変わりません。 実際の製品の数量が多い場合や少ない場合でも、使用可能なリストの数量には常にこの値が使用されます。 この設定は、通常、製品インベントリを管理しない場合に使用されます。 例えば、数量が 80 の製品が [!DNL Commerce] カタログ。 をに設定した場合 `10`Amazonのリストには、常に次の数量が表示されます `10` 製品に対して販売が行われた場合も変更されません。

1. の場合 **[!UICONTROL "Do Not Manage Stock" Quantity]** （必須） Amazonのリストに表示する数量を入力します。

   Amazonでは、利用可能な数量を公開する必要があります。 の場合 [!DNL Commerce] 在庫を管理しないように設定された商品をAmazonに一覧表示する場合、ここに入力した利用可能数量でリストが公開されます。

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![在庫/数量設定](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | 商品をAmazon リストに登録するには、商品の最小数量の数値を入力します（デフォルトは） `0`）に設定します。<br><br>次の場合 [!DNL Commerce] 商品の在庫がこの数を下回る場合、それぞれのAmazon リストはAmazonを通じた販売に対して不適格となります。 |
| [!UICONTROL Maximum Listed Quantity] | Amazon リストに表示する数量の数値を入力します。<br><br>商品が販売されると、Amazonのリストは、ここに入力された数量で再公開されます。 この設定は、通常、製品インベントリを管理しない場合に使用されます。<br><br>例えば、「リストの最大数量」の値を `10`. 商品の実際の数量はです `80`. この値はに設定されているので、 `10`Amazonのリストには、常に次の数量が表示されます `10`. 在庫数が少ない場合でも、有効数量は常に定義済みの値で表示されます。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Amazon リストの表示数量を入力します。<br><br>Amazonでは、利用可能な数量を公開する必要があります。 の場合 [!DNL Commerce] 在庫を管理しないように設定された商品をAmazonでリストする場合、ここに入力した値の有効数量でリストが公開されます。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## 例：最大リスト数量

商品が販売されると、Amazonのリストではこの数量で販売が抑制されます。

例えば、次のように設定したとします *[!UICONTROL Maximum Listed Quantity]* as `12`を選択した場合、Amazonのリストには、商品の数量が 12 であるにもかかわらず、 [!DNL Commerce] 数量 80:

![最大リスト数量の例 1](assets/amazon-max-listed-quantity.png){width="300"}

を設定した場合 *[!UICONTROL Maximum Listed Quantity]* as `1`。すべての適格な製品が数量と共に一覧表示されます `1`. 商品が販売されると、システムはユーザーに検索します [!DNL Commerce] さらに在庫が存在する場合、は数量がの商品をAmazonに依存させます `1`.

このオプションは、通常 1 の数量で注文される製品で役立つ場合があります。 また、Amazonのリストを表示する際に、買い物客の緊急性が高まります。

![最大リスト数量の例 2](assets/amazon-max-listed-quantity-1.png){width="300"}
