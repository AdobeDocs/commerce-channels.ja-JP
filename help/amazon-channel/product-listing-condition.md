---
title: 製品リスト条件
description: 「製品リスト条件」設定を使用して、コマース製品を「新規」や「改装済み」などのAmazon製品の条件にマップします。
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# 製品リスト条件

製品リスト条件の設定は、ストアリスト設定の一部です。 [ストアダッシュボード](./amazon-store-dashboard.md)でリスト設定にアクセスできます。

Amazonでは、製品リストに条件を定義する必要があります。 すべての製品が同じ条件の場合、Amazonの条件オプションを1つ選択して、すべての製品をグローバル条件値として表すことができます。 標準のAmazon条件は次のとおりです。

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
>更新（リフュース）された製品を販売する場合は、[!DNL Amazon Renewed Program]に登録する必要があります。 [更新された製品](./renewed-products.md)を参照してください。

ただし、カタログに異なる条件（新規、使用済み、再製品など）の商品が含まれる場合は、**[!UICONTROL Assign Condition Using Product Attribute]**&#x200B;を選択する必要があります。 この設定を使用すると、[!DNL Commerce]条件属性と値をAmazonリストの条件にマップできます。

[事前設定タスク](./amazon-pre-setup-tasks.md)の間に、製品の条件に対して[!DNL Commerce]製品属性を作成することをお勧めします。 様々な条件で製品を提供し、条件属性を作成していない場合は、[ [!DNL Commerce]](./ob-creating-magento-attributes.md)での製品属性の作成を参照してください。 条件属性を作成したら、[!DNL Commerce]カタログ内の各製品に条件値を割り当てることができます。

## 設定を行う

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. **[!UICONTROL Product Listing Condition]**&#x200B;セクションを展開します。

1. **[!UICONTROL Listing Product Condition]**&#x200B;の場合は、オプションを選択します。

   すべてのリストのグローバル条件値に対して、標準のAmazon条件の1つを選択します。 デフォルト設定は`New`です。

   異なる条件を持つ製品/リストがある場合は、`Assign Condition Using Product Attribute`を選択して、表示される追加のフィールドで製品の条件の設定を定義します。

1. **条件属性**&#x200B;の場合は、[!DNL Commerce]属性を選択して、標準のAmazon条件属性のそれぞれの値をマッピングします。

   製品が`Used`または`Collectible`条件にあるが、それ以上区別できない場合は、1つの`Used`または`Collectible` Amazon条件にマッピングし、それ以外の条件は空白のままにすることができます。 このメソッドは、すべての`Used`または`Collectible`条件を、1つのAmazonの使用済みまたは収集可能な条件にマッピングします。

   例えば、製品に対して1つの`Used`条件があるとします。 マッピングの際に、Amazon条件`Used; Like New`、`Used; Very Good`、`Used; Good`、`Used; Acceptable`のいずれにマッピングするかを選択します。 必要なAmazon条件のフィールドにのみ入力し、他の`Used`オプションは`--Select Option--`に設定したままにします。 この例の画像では、`Used`条件内のすべての[!DNL Commerce]製品がAmazon `Used; Very Good`条件にマッピングされています。

   条件に対して、`New`を除く説明テキストを入力することもできます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![製品リスト条件](assets/amazon-product-listing-condition.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Listing Product Condition] | 製品リストの条件。 オプション：`New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>1つの製品条件を販売する場合は、標準のAmazon条件の1つを選択します。 [!DNL Commerce]カタログに様々な条件の商品が含まれている場合は、`Assign Condition Using Product Attribute`を選択します。 |
| [!UICONTROL Condition Attribute] | 製品の条件を定義する[!DNL Commerce]属性。 Amazon条件属性にマップするために作成したマグネト属性を選択します。 [事前設定タスクの例](./ob-creating-magento-attributes.md)では、`Amazon Condition`という名前にすることをお勧めします。 選択すると、標準のAmazon条件をマッピングするための追加のフィールドが表示されます。 |
| [!UICONTROL Additional Condition fields] | 標準のAmazon条件ごとに、対応する条件を選択します。 オプションは、[Amazon条件属性](./ob-creating-magento-attributes.md)を作成したときに追加した条件ラベルです。<br><br>製品がor条件に該当する `Used` が、それ以 `Collectible` 上区別できない場合、1つの `Used` Amazon条件または `Collectible` 条件にマッピングし、それ以外の条件は空白のままにすることができます。このメソッドは、すべての`Used`または`Collectible`条件を、1つのAmazon使用または収集可能な条件にマッピングします。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
