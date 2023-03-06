---
title: 在庫/数量
description: コマースストアからユーザーへの製品数量の詳細の同期を制御するには [!DNL Amazon Seller Central] アカウントに追加する場合は、「在庫/数量」設定を更新します。
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# 在庫/数量

*[!UICONTROL Stock/Quantity]* 設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、製品数量の詳細を [!DNL Commerce] あなたの上の量に対する店頭 [!DNL Amazon Seller Central] アカウント このツールは強力で、在庫を整理したまま、バイヤーに緊急度を表示することで、追加の広告に使用できます。 例えば、一部の商人は、特定の SKU の 150 品目を倉庫に保管しており、Amazonの買い物客が在庫をすべて購入できるようにしたいと考えている場合があります。 他の商人は、エンドユーザーに対して希少感を与えるために、一度に 1 つのアイテムだけをリストする場合があります。 この場合、 *[!UICONTROL Maximum Listed Quantity]* から `1`.

数量は地域属性で、 **[!UICONTROL Amazon Marketplace Country]** 次の期間に定義を設定 [ストア統合](./store-integration.md). 製品の数量を変更すると、その変更は、共有するすべてのAmazonリストに影響します [!DNL Amazon Seller SKU] 同じ国で売っているAmazonの店で 共有に対する変更 [!DNL Amazon Seller SKU] 米国では、別の国用に設定されたAmazonストアには影響しません。 統合された最初のAmazonストア（作成日が最も古いストア）が、数量設定の優先度を制御します。

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source2.3.x のユーザーの場合、Amazonセールスチャネルは、追加の設定なしでInventory management拡張機能の使用をサポートします。 詳しくは、 [在庫の管理](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## 在庫/数量の設定 {#configure-stock--quantity-settings}

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 **[!UICONTROL Stock / Quantity]** 」セクションに入力します。

1. の場合 **[!UICONTROL Out-of-Stock Threshold]** （必須）製品をAmazonリストに含める資格を持たせるために、製品の最小数量の数値を入力します。

   デフォルトはです。 `0`. 次に、 [!DNL Commerce] 製品の在庫がこの数より少なくなると、それぞれのAmazonリストはAmazonを通じた販売の資格を持ちません。

1. の場合 **[!UICONTROL Maximum Listed Quantity]** （必須）Amazonリストに表示する数量の数値を入力します。

   この設定では、すべての適格なAmazonリストが入力値で一覧表示されます。 品目が販売されても、Amazonのリスト数量は変更されません。 実際の製品数量が多い場合や少ない場合でも、使用可能なリスト数量は常にこの値を使用します。 この設定は、通常、製品在庫を管理しない場合に使用されます。 例えば、製品の数量が 80 の場合、 [!DNL Commerce] カタログ。 をに設定します。 `10`を指定しない場合、Amazonリストには常に使用可能な数量が表示されます。 `10` また、製品の販売時には変更されません。

1. の場合 **[!UICONTROL "Do Not Manage Stock" Quantity]** （必須）Amazonの一覧に表示する数量の値を入力します。

   Amazonでは、使用可能な数量を公開する必要があります。 の場合 [!DNL Commerce] 在庫を管理しないが、Amazonにリストするように設定された製品は、ここに入力した在庫数量でリストが公開されます。

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![在庫/数量の設定](assets/amazon-stock-quantity.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Amazonリストに適格な製品を保持するために、製品の最小数量の数値を入力します ( デフォルトは `0`) をクリックします。<br><br>次に、 [!DNL Commerce] 製品の在庫がこの数より少なくなると、それぞれのAmazonリストはAmazonを通じた販売の資格を持ちません。 |
| [!UICONTROL Maximum Listed Quantity] | Amazonリストに表示する数量の数値を入力します。<br><br>品目が販売されると、Amazonリストはここに入力された数量で再発行します。 この設定は、通常、製品在庫を管理しない場合に使用されます。<br><br>例えば、「最大リスト数量」の値を「 `10`. 製品の実際の数量は次のとおりです `80`. この値は `10`を指定しない場合、Amazonリストには常に使用可能な数量が表示されます。 `10`. 在庫数量が少ない場合でも、使用可能な数量は常に、値が定義された状態で表示されます。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Amazon一覧の表示数量の値を入力します。<br><br>Amazonでは、使用可能な数量を公開する必要があります。 の場合 [!DNL Commerce] 在庫を管理しないが、Amazonにリストするように設定された製品の場合、ここに入力した値の使用可能な数量と共にリストが公開されます。 |

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

品目が販売されると、Amazonリストはこの数量でその品目を残します。

例えば、 *[!UICONTROL Maximum Listed Quantity]* as `12`を指定した場合、Amazonのリストには、製品の数量が 12 と表示されます ( 製品に [!DNL Commerce] 数量 80:

![最大リスト数量の例 1](assets/amazon-max-listed-quantity.png)

次に、 *[!UICONTROL Maximum Listed Quantity]* as `1`に設定されている場合、すべての対象製品が `1`. 商品が販売されると、システムはユーザーの [!DNL Commerce] 製品および、追加の在庫が存在する場合は、その品目を数量のAmazonに依存します。 `1`.

このオプションは、通常、数量 1 の商品を注文する場合に役立ちます。 また、Amazonのリストを表示する際の買い物客の緊急度を高めます。

![最大リスト数量の例 2](assets/amazon-max-listed-quantity-1.png)
