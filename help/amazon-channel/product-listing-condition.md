---
title: Amazon販売チャネル – 商品リストの条件
description: 商品リストの条件設定を使用して、「新規」や「再生済み」などのAmazon商品の条件にCommerce商品をマッピングします。
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 商品リストの条件

商品リストの条件設定は、ストアリスト設定の一部です。 [ ストアダッシュボード ](./amazon-store-dashboard.md) のリスト設定にアクセスできます。

Amazonでは、製品リストに条件を定義する必要があります。 すべての商品が同じ条件の場合、Amazonの条件オプションの 1 つを選択して、すべての商品をグローバル条件値として表すことができます。 Amazonの標準的な条件は次のとおりです。

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>リニューアル済み商品を販売する場合は、[!DNL Amazon Renewed Program] ールに登録する必要があります。 詳しくは、[ 更新済み製品 ](./renewed-products.md) を参照してください。

ただし、カタログに異なる条件（新規、使用中、再生済みなど）の製品が含まれる場合は、**[!UICONTROL Assign Condition Using Product Attribute]** を選択する必要があります。 この設定を使用すると、[!DNL Commerce] 条件の属性と値をAmazon リストの条件にマッピングできます。

[ 事前設定タスク ](./amazon-pre-setup-tasks.md) の間に、製品の状態に対して [!DNL Commerce] しい製品属性を作成することをお勧めします。 様々な条件で製品をオファーし、条件属性を作成していない場合は、[ での製品属性の作成  [!DNL Commerce]](./ob-creating-magento-attributes.md) を参照してください。 条件属性を作成したら、[!DNL Commerce] カタログ内の各製品に条件値を割り当てることができます。

## 設定

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「**[!UICONTROL Product Listing Condition]**」セクションを展開します。

1. **[!UICONTROL Listing Product Condition]** の場合は、オプションを選択します。

   すべてのリストのグローバル条件値に対して、標準のAmazon条件のいずれかを選択します。 デフォルト設定は `New` です。

   異なる条件を持つ製品またはリストがある場合は、表示される追加のフィールドで製品条件の設定を定義する `Assign Condition Using Product Attribute` を選択します。

1. **条件属性** には、標準のAmazon条件属性ごとに値をマッピングする [!DNL Commerce] 属性を選択します。

   `Used` または `Collectible` の条件に商品があるが、それ以上の区別がない場合は、1 つの `Used` またはAmazonの条件にマッピングし、それ以外 `Collectible` 空白のままにすることができます。 このメソッドは、すべての `Used` 条件または `Collectible` 条件を、1 つのAmazonの使用済み条件または取得可能条件にマッピングします。

   例えば、製品の `Used` 条件が 1 つあるとします。 マッピングする場合は、Amazon条件 `Used; Like New`、`Used; Very Good`、`Used; Good` または `Used; Acceptable` にマッピングするかどうかを選択します。 必要なAmazon条件のフィールドにのみ入力し、他の `Used` のオプションは `--Select Option--` に設定したままにします。 この例の画像では、条件内 [!DNL Commerce] すべての商品がAmazon `Used; Very Good` 条件 `Used` マッピングされています。

   条件の説明テキストを入力することもできます（`New` を除く）。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ 商品リストの条件 ](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | 商品リストの状態。 Options: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>1 つの商品を販売する場合は、標準のAmazon条件のいずれかを選択します。 [!DNL Commerce] カタログに様々な条件の製品が含まれている場合は、「`Assign Condition Using Product Attribute`」を選択します。 |
| [!UICONTROL Condition Attribute] | 商品の条件を定義する [!DNL Commerce] 属性。 作成した Magneto 属性を選択して、Amazon条件属性にマッピングします。 [ 事前設定タスクの例 ](./ob-creating-magento-attributes.md) では、`Amazon Condition` のように名前を付けることをお勧めします。 選択すると、標準のAmazon条件をマッピングするための追加のフィールドが表示されます。 |
| [!UICONTROL Additional Condition fields] | 標準のAmazon条件ごとに、対応する条件を選択します。 オプションは、（Amazon条件属性を作成した [ ときに追加した条件ラベル ](./ob-creating-magento-attributes.md) です。<br><br>`Used` または `Collectible` の条件に商品が含まれているが、それ以上の区別がない場合、1 つの `Used` または `Collectible` のAmazonの条件にマッピングし、他の条件は空白のままにすることができます。 このメソッドは、すべての `Used` 条件または `Collectible` 条件を、1 つのAmazonの使用済み条件または収集可能条件にマッピングします。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
