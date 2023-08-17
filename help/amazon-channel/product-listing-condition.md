---
title: Amazonセールスチャネル — 製品リスト条件
description: 「製品リスト条件」設定を使用して、コマース製品を「新規」や「リファース済み」などのAmazon製品の条件にマッピングします。
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 製品リスト条件

製品リスト条件の設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

Amazonでは、製品リストに定義済みの条件が必要です。 すべての製品が同じ条件の場合、Amazonの条件オプションを 1 つ選択して、すべての製品をグローバル条件値として表すことができます。 標準のAmazon条件は次のとおりです。

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
>更新された（リフュールされた）製品を販売する場合、 [!DNL Amazon Renewed Program]. 詳しくは、 [更新された製品](./renewed-products.md).

ただし、カタログに異なる条件（新規、使用済み、再製品など）の製品が含まれる場合は、 **[!UICONTROL Assign Condition Using Product Attribute]**. この設定では、 [!DNL Commerce] 条件属性と値をAmazonリストの条件に設定する必要があります。

期間 [事前設定タスク](./amazon-pre-setup-tasks.md)を使用する場合、 [!DNL Commerce] 製品の条件の製品属性。 様々な条件で製品を提供し、条件属性を作成していない場合は、 [での製品属性の作成 [!DNL Commerce]](./ob-creating-magento-attributes.md). 条件属性を作成したら、条件値を [!DNL Commerce] カタログ。

## 設定を構成

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 **[!UICONTROL Product Listing Condition]** 」セクションに入力します。

1. の場合 **[!UICONTROL Listing Product Condition]**、「 」オプションを選択します。

   すべてのリストのグローバル条件値に対して、標準のAmazon条件の 1 つを選択します。 デフォルト設定はです。 `New`.

   異なる条件を持つ製品/リストがある場合は、 `Assign Condition Using Product Attribute` をクリックして、表示される追加のフィールドで製品の条件設定を定義します。

1. の場合 **条件属性**、選択 [!DNL Commerce] 属性を使用して、各標準Amazon条件属性の値をマッピングします。

   製品が `Used` または `Collectible` 条件は識別できませんが、これ以上区別できない場合は、 `Used` または `Collectible` Amazon条件を満たし、残りは空白のまま残します。 このメソッドは、 `Used` または `Collectible` 条件を単一のAmazon Used 条件または Collectible 条件に適用する必要があります。

   例えば、 `Used` 条件を設定します。 マッピングの際に、Amazon条件にマッピングするかどうかを選択します `Used; Like New`, `Used; Very Good`, `Used; Good`または `Used; Acceptable`. 必要なAmazon条件のフィールドにのみ入力し、残りのフィールドは残します。 `Used` オプション設定 `--Select Option--`. 例の画像では、すべて [!DNL Commerce] の製品 `Used` 条件がAmazonにマッピングされる `Used; Very Good` 条件。

   また、条件に対して説明テキストを入力することもできます ( ただし、 `New`.

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![製品リスト条件](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | 製品リストの条件。 オプション： `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>1 つの製品条件を販売する場合は、標準のAmazon条件の 1 つを選択します。 次の場合、 [!DNL Commerce] カタログに様々な条件の製品が含まれています。 `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | The [!DNL Commerce] 製品の条件を定義する属性。 Amazon条件属性にマッピングするために作成した Magento 属性を選択します。 Adobe Analytics の [事前設定タスクの例](./ob-creating-magento-attributes.md) では、にと名前を付けることをお勧めします。 `Amazon Condition`. 選択すると、標準のAmazon条件のマッピングに使用する追加のフィールドが表示されます。 |
| [!UICONTROL Additional Condition fields] | 標準のAmazon条件のそれぞれに対して、対応する条件を選択します。 オプションは、 [Amazon条件属性を作成しました](./ob-creating-magento-attributes.md).<br><br>製品が `Used` または `Collectible` 条件は識別できませんが、これ以上区別できない場合は、 `Used` または `Collectible` Amazon条件を満たし、残りは空白のまま残します。 このメソッドは、 `Used` または `Collectible` 条件を単一のAmazon Used 条件または Collectible 条件に適用する必要があります。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
