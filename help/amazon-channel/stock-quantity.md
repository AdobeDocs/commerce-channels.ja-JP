---
title: 在庫/数量
description: コマースストアから [!DNL Amazon Seller Central] アカウントへの製品数量の詳細の同期を制御するには、在庫/数量の設定を更新します。
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# 在庫/数量

*[!UICONTROL Stock/Quantity]* 設定は、ストアリスト設定の一部です。リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定は、[!DNL Commerce]ストアフロントの製品数の詳細を[!DNL Amazon Seller Central]アカウントの数量と同期するために使用します。 このツールは強力で、在庫を整理したまま、購入者に緊急度を表示することで、追加の広告に使用できます。 例えば、ある商社の倉庫に特定のSKUの150品目が在庫されていて、Amazonの買い物客が在庫をすべて購入できるようにしたいと考えている場合があります。 他の商人は、一度に1つのアイテムのみをリストし、エンドユーザーに対して欠乏感を作り出したいと考える場合があります。 この場合、*[!UICONTROL Maximum Listed Quantity]*&#x200B;を`1`に設定します。

Quantityは地域属性で、[store integration](./store-integration.md)の間に定義された&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;設定に基づきます。 製品の数量に変更が加えられると、その変更は、同じ国で販売するAmazonの店舗で[!DNL Amazon Seller SKU]を共有するすべてのAmazonのリストに影響を与えます。 米国で共有[!DNL Amazon Seller SKU]を変更しても、別の国向けに設定されたAmazonストアには影響しません。 （作成日が最も古い）統合された最初のAmazonストアが、数量設定の優先順位を制御します。

>[!NOTE]
>
>AdobeコマースおよびMagento Open Source2.3.xのユーザーの場合、Amazonの販売チャネルは、追加の設定をおこなうことなく、在庫管理拡張機能の使用をサポートします。 [インベントリの管理](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){:target=&quot;_blank&quot;}を参照してください。

## 在庫/数量の設定 {#configure-stock--quantity-settings}

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. **[!UICONTROL Stock / Quantity]**&#x200B;セクションを展開します。

1. **[!UICONTROL Out-of-Stock Threshold]**（必須）には、Amazonリストに該当する製品を保持するために、製品の最も少ない数量の数値を入力します。

   デフォルトは`0`です。 [!DNL Commerce]製品の在庫がこの数を下回ると、それぞれのAmazonリストはAmazonを通じた販売の資格を持ちません。

1. **[!UICONTROL Maximum Listed Quantity]**（必須）には、Amazonリストに表示する数量の数値を入力します。

   この設定は、入力した値ですべての有効なAmazonリストをリストします。 品目が販売されても、Amazonのリスト数は変わりません。 実際の製品数が多い場合や少ない場合でも、使用可能なリスト数量は常にこの値を使用します。 この設定は、通常、製品在庫を管理しない場合に使用されます。 例えば、[!DNL Commerce]カタログに数量が80の製品があるとします。 `10`に設定すると、Amazonリストには常に`10`の数量が表示され、製品の販売時には変更されません。

1. **[!UICONTROL "Do Not Manage Stock" Quantity]**（必須）には、Amazonのリストに表示する数量の値を入力します。

   Amazonでは、使用可能な数量を公開する必要があります。 在庫を管理しないが、Amazonに一覧表示する[!DNL Commerce]製品の場合、ここに入力した在庫数量を使用してリストが公開されます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![在庫/数量の設定](assets/amazon-stock-quantity.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Amazonリストに該当する製品を保持するために、製品の最小数量の数値を入力します（デフォルトは`0`）。<br><br>この数より [!DNL Commerce] 小さい製品在庫は、それぞれのAmazonリストにAmazonを通じた販売の資格がありません。 |
| [!UICONTROL Maximum Listed Quantity] | Amazonリストに表示する数量の数値を入力します。<br><br>品目が販売されると、Amazonリストはここに入力された数量と共に再パブリッシュします。この設定は、通常、製品在庫を管理しない場合に使用されます。<br><br>例えば、「最大リスト数量」の値をに入力しま `10`す。製品の実際の数量は`80`です。 この値を`10`に設定しているので、Amazonのリストには常に`10`という数量が表示されます。 在庫数が少ない場合でも、使用可能な数量は常に値が定義された状態で表示されます。 |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Amazonリストの表示数量の値を入力します。<br><br>Amazonでは、使用可能な数量を公開する必要があります。在庫を管理しないがAmazonにリストするように設定された[!DNL Commerce]製品の場合、ここに入力した値の利用可能な数量と共にリストが公開されます。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## 例：最大一覧数量

品目が販売されると、Amazonのリストは、この数量でその品目を残します。

例えば、*[!UICONTROL Maximum Listed Quantity]*&#x200B;を`12`に設定した場合、Amazonのリストには、製品の数量が80([!DNL Commerce])であっても、数量が12と表示されます。

![最大リスト数量の例1](assets/amazon-max-listed-quantity.png)

*[!UICONTROL Maximum Listed Quantity]*&#x200B;を`1`に設定した場合、対象となるすべての製品が数量`1`で一覧表示されます。 品目が販売されると、システムは[!DNL Commerce]製品を探し、追加の在庫がある場合は、数量`1`の品目をAmazonに残します。

このオプションは、通常、数量1の商品を注文する場合に役立ちます。 また、Amazonリストを表示する際の買い物客の緊急性も高まります。

![最大リスト数量の例2](assets/amazon-max-listed-quantity-1.png)
