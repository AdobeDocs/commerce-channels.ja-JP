---
title: AmazonSales Channel- [!UICONTROL Stock/Quantity]
description: Commerce ストアからアカウントへの製品数量の詳細の同期を制御するには  [!DNL Amazon Seller Central]  在庫/数量の設定を更新します。
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]* の設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定は、[!DNL Commerce] ストアフロントの製品数量の詳細を [!DNL Amazon Seller Central] アカウントの数量に同期するために使用されます。 このツールは強力で、在庫を整理しながら購入者に緊急度を表示することで、追加の広告に使用できます。 例えば、一部のマーチャントは、倉庫内に特定の SKU の 150 個の商品があり、Amazonの買い物客が在庫全体を購入できるようにする必要がある場合があります。 他のマーチャントは、エンドユーザーに希少感を与えるために、一度に 1 つの項目のみをリストしたい場合があります。 この場合は、*[!UICONTROL Maximum Listed Quantity]* を `1` に設定します。

数量は地域属性で、[ ストアの統合 ](./store-integration.md) 時に定義される **[!UICONTROL Amazon Marketplace Country]** 設定に基づきます。 商品の数量を変更すると、その変更は、同じ国で販売されているAmazonのストアで [!DNL Amazon Seller SKU] 用されているすべてのAmazonのリストに影響します。 米国の共有 [!DNL Amazon Seller SKU] の変更は、別の国に設定されたAmazonのストアには影響しません。 数量の設定では、統合された（最も古い作成日を持つ）最初のAmazon ストアが優先度を制御します。

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source 2.3.x を使用しているユーザーの場合、Amazon sales channel では、追加の設定を行わずにInventory management拡張機能の使用をサポートしています。 [ 在庫の管理 ](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"} を参照してください。

## 在庫/数量の設定 {#configure-stock--quantity-settings}

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「**[!UICONTROL Stock / Quantity]**」セクションを展開します。

1. **[!UICONTROL Out-of-Stock Threshold]** （必須）には、Amazonリストへの登録対象を商品に維持するために、商品の最小数量を表す数値を入力します。

   デフォルトは `0` です。 [!DNL Commerce] 商品の在庫がこの数を下回った場合、それぞれのAmazon リストはAmazonを通じた販売に対して不適格となります。

1. **[!UICONTROL Maximum Listed Quantity]** （必須）には、Amazon リストに表示する数量の数値を入力します。

   この設定では、入力した値に適格なすべてのAmazonのリストを表示します。 商品が販売されても、Amazonのリスト数量は変わりません。 実際の製品の数量が多い場合や少ない場合でも、使用可能なリストの数量には常にこの値が使用されます。 この設定は、通常、製品インベントリを管理しない場合に使用されます。 例えば、[!DNL Commerce] カタログに数量 80 の製品があるとします。 `10` に設定すると、Amazonのリストには常に使用可能な `10` の数量が表示され、商品が売り出されても変更されません。

1. **[!UICONTROL "Do Not Manage Stock" Quantity]** （必須）には、Amazonのリストに表示する数量の値を入力します。

   Amazonでは、利用可能な数量を公開する必要があります。 在庫を管理しない設定になっているが、Amazonでリストする [!DNL Commerce] の商品については、ここに入力された有効数量でリストが公開されます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ 在庫/数量設定 ](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | 商品をAmazonリストに登録するには、商品の最小数量の数値を入力します（デフォルトは `0`）。<br><br> お使いの [!DNL Commerce] 製品の在庫がこの数を下回った場合、それぞれのAmazon リストはAmazonを通じた販売に対して不適格となります。 |
| [!UICONTROL Maximum Listed Quantity] | Amazon リストに表示する数量の数値を入力します。<br><br> 商品が販売されると、Amazonのリストは、ここに入力された数量で再公開されます。 この設定は、通常、製品インベントリを管理しない場合に使用されます。<br><br> 例えば、「リストの最大数量」の値を「`10`」と入力します。 実際の製品数量は `80` です。 この値は `10` に設定しているので、Amazonのリストには常に `10` の有効数量が表示されます。 在庫数が少ない場合でも、有効数量は常に定義済みの値で表示されます。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Amazon リストの表示数量を入力します。<br><br>Amazonでは、利用可能な数量を公開する必要があります。 在庫を管理しない設定になっているが、Amazonでリストする [!DNL Commerce] の商品については、ここに入力した値の有効数量でリストが公開されます。 |

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

例えば、*[!UICONTROL Maximum Listed Quantity]* を `12` に設定した場合、商品の数量が [!DNL Commerce] 数 80 であっても、Amazonのリストには数量 12 が表示されます。

![ 最大上場数量の例 1](assets/amazon-max-listed-quantity.png){width="300"}

*[!UICONTROL Maximum Listed Quantity]* を `1` に設定すると、すべての適格な製品が `1` の数量で表示されます。 商品が販売されると、[!DNL Commerce] 商品が検索され、追加の在庫がある場合は、その商品が数量 `1` のAmazonに依存します。

このオプションは、通常 1 の数量で注文される製品で役立つ場合があります。 また、Amazonのリストを表示する際に、買い物客の緊急性が高まります。

![ 最大上場数量の例 2](assets/amazon-max-listed-quantity-1.png){width="300"}
