---
title: 「例：Amazon リストルールの条件の定義」
description: リストルールを作成する際には、Amazon Marketplace にリストされるCommerce カタログ商品を識別するための条件を定義します。
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 例：条件の定義

## 条件

条件内の太字で表示されている領域をクリックして、様々なオプションを表示できます。

**選択した web サイト内のすべての製品が対象となる場合は、条件を追加しないでください。**

>[!NOTE]
>
>Amazon システムと直接通信するための複雑なバックエンドプロセスのセットがあります。 リストを取得しようとしている商品の数や、Amazonのシステムのビジー状態（ブラックフライデーなど）によっては、Amazonに商品がリストされるまでに時間がかかる場合があります。

の「条件」セクションを参照してください。 [買い物かご価格ルールの作成](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## 条件の定義

このプロセスは、カタログの設定に応じて、単純なものでも詳細なものでもかまいません。 条件は、次の場合に設定できます `ALL` または `ANY` 定義条件のうちのは、次のいずれかです `TRUE` または `FALSE` 商品の場合、その商品はAmazonにリストされる資格があります。

条件は、既存の製品属性値に基づきます。 すべての製品にルールを適用する場合は、「条件」セクションを空白のままにします。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、 **[!UICONTROL Use for Promo Rule Conditions]** 属性の設定 `Yes`. この設定には [ストアフロント プロパティ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) 属性のページ。

![条件 – 1 行目](assets/ob-listing-rule-conditions-start.png){width="500"}

この例のルールは、次の条件を満たすすべてのカタログ製品について、Amazonの実施要件を設定するルールを定義します _AMAZONFBA_ 属性の設定 `Yes`.

ルール ステートメントには 2 つの太字リンクがあり、クリックすると、ステートメントのその部分のオプションが表示されます。 太字のオプションを変更せずに条件を保存すると、ルールはすべての商品に適用されます。

- クリック **[!UICONTROL ALL]** およびのいずれかを選択しました `ALL` または `ANY`.
- クリック **[!UICONTROL TRUE]** 次のいずれかを選択します `TRUE` または `FALSE`.
- すべての製品にルールを適用する場合は、条件を変更しません。

これらの値の組み合わせを変更することで、様々な条件を作成できます。 この例では、次の条件を使用します。

`If ALL of these conditions are TRUE:`

1. 「追加」（![アイコンを追加](assets/btn-add-grn.png)）アイコンをクリックし、条件のベースとなる属性（条件の組み合わせや製品属性など）を選択します。

   - **[!UICONTROL Conditions Combination]**  – 別のセットを作成できるようにを選択 `All/Any` および `True/False` 既存のセット内の条件。

     ![条件の組み合わせ](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]**  – 製品属性は、属性の設定によって異なります。 属性をリストに表示するには、プロモーションルールの条件で使用できるように設定する必要があります。 を参照してください。 _プロモルール条件に使用_ 。対象： [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     の下のリスト **[!UICONTROL Product Attribute]**&#x200B;で、条件の基礎として使用する属性を選択します。 この例では、選択した条件はです `Amazon FBA`.

     ![条件ライン 2、パート 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     選択した条件がステートメントに表示され、その後にさらに 2 つの太字リンクが表示されます。 オプションは、選択する製品属性によって異なります。

     属性を設定した後は、変更できません。 属性を変更するには、行を削除して新しい属性を追加する必要があります。 条件行を削除するには、「削除」（![アイコンを削除](assets/btn-del-red.png)）アイコンをクリックして行を終了します。

      1. クリック **[!UICONTROL is]** 製品が満たす条件を示す比較演算子を選択します。

         この例では、比較演算子はです `is`. 使用可能なオプションは、前の手順で選択した属性によって異なります。 オプションには、値の一致、1 つ以上の値を含まない、または含まない、数値より大きい、数値と等しい、数値より小さいなど、様々な比較オプションを含めることができます。 この例では、次のオプションがあります `is` および `is not`.

      1. クリック **[!UICONTROL ...]** 条件の基になる属性値を選択します。

         オプションは、属性の設定によって異なります。 オプションを選択するか、条件のテキストまたは数値を入力するように求めるプロンプトが表示される場合があります。 この例では、選択は次のようになります `Yes`.

         条件を完了するためのステートメントに、選択した項目が表示されます。

         ![条件 2 のパート 3](assets/ob-listing-rule-condition-is.png){width="500"}

   この条件が完了しました。 前述のように、この条件は、内の製品を意味します [!DNL Commerce] Amazonの FBA 属性がの値に設定されているカタログ `Yes` は、地域およびストアをAmazonにリストする資格があります。 条件ラインを追加して、実施要件を満たす製品をさらに絞り込むことができます。

1. ステートメントに別の条件行を追加するには、手順 1 に戻り、必要なすべての条件が完了するまで手順を繰り返します。

条件文の行は、削除（![アイコンを削除](assets/btn-del-red.png)）アイコンをクリックして行を終了します。
