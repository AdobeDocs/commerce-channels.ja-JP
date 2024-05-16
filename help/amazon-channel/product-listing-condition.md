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

商品リストの条件設定は、ストアリスト設定の一部です。 のリスト設定にアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

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
>再生品（再生品）を販売する場合は、に登録する必要があります [!DNL Amazon Renewed Program]. 参照： [更新済み製品](./renewed-products.md).

ただし、カタログに異なる条件（新規、使用中、再生済みなど）の製品が含まれている場合は、次のオプションを選択する必要があります **[!UICONTROL Assign Condition Using Product Attribute]**. この設定を使用すると、 [!DNL Commerce] Amazon リストの条件に対する条件属性と値。

次の期間 [事前設定タスク](./amazon-pre-setup-tasks.md)を作成することをお勧めします。 [!DNL Commerce] 製品の条件に対する製品属性。 様々な条件で製品をオファーし、条件属性をまだ作成していない場合は、を参照してください。 [での製品属性の作成 [!DNL Commerce]](./ob-creating-magento-attributes.md). 条件属性を作成したら、内の各製品に条件値を割り当てることができます [!DNL Commerce] カタログ。

## 設定

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 **[!UICONTROL Product Listing Condition]** セクション。

1. の場合 **[!UICONTROL Listing Product Condition]**、オプションを選択します。

   すべてのリストのグローバル条件値に対して、標準のAmazon条件のいずれかを選択します。 デフォルト設定は `New`.

   条件が異なる製品/リストがある場合は、次を選択します `Assign Condition Using Product Attribute` 表示される追加フィールドで製品条件の設定を定義します。

1. の場合 **条件属性**、を選択します [!DNL Commerce] 標準のAmazon条件属性ごとの値をマッピングする属性。

   に製品がある場合 `Used` または `Collectible` 条件が、それ以上区別されない場合は、1 つにマッピングできます `Used` または `Collectible` Amazonの条件を満たし、他は空白のままにします。 このメソッドは、次のすべてをマッピングします `Used` または `Collectible` 1 つのAmazonの使用済みまたは取得可能な条件。

   例えば、以下のような 1 つの `Used` 商品の条件。 マッピングする場合は、Amazon条件にマッピングするかどうかを選択します `Used; Like New`, `Used; Very Good`, `Used; Good`、または `Used; Acceptable`. もう 1 つを残して、必要なAmazon条件のフィールドにのみ入力します `Used` に設定されたオプション `--Select Option--`. サンプル画像では、すべて [!DNL Commerce] 製品： `Used` 条件はAmazonにマッピングされます `Used; Very Good` 条件。

   条件の説明テキストを入力することもできます（を除く） `New`.

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![商品リストの条件](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | 商品リストの状態。 オプション： `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>1 つの商品を販売する場合は、標準のAmazon条件のいずれかを選択します。 次の場合 [!DNL Commerce] カタログには様々な条件の製品が含まれています、を選択してください `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | この [!DNL Commerce] 製品の条件を定義する属性。 作成した Magneto 属性を選択して、Amazon条件属性にマッピングします。 が含まれる [事前設定タスクの例](./ob-creating-magento-attributes.md) では、という名前を付けることをお勧めします。 `Amazon Condition`. 選択すると、標準のAmazon条件をマッピングするための追加のフィールドが表示されます。 |
| [!UICONTROL Additional Condition fields] | 標準のAmazon条件ごとに、対応する条件を選択します。 オプションは、次の場合に追加した条件ラベルです [がAmazon条件属性を作成しました](./ob-creating-magento-attributes.md).<br><br>に製品がある場合 `Used` または `Collectible` 条件が、それ以上区別されない場合は、1 つにマッピングできます `Used` または `Collectible` Amazonの条件を満たし、他は空白のままにします。 このメソッドはすべてをマッピングします `Used` または `Collectible` 1 つのAmazonの使用済みまたは取得可能な条件。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
