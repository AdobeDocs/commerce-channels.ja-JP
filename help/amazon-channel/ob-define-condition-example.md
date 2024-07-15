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

[ 買い物かご価格ルールの作成 ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html) の「条件」の節を参照してください。

## 条件の定義

このプロセスは、カタログの設定に応じて、単純なものでも詳細なものでもかまいません。 条件を設定して、定義条件の `ALL` または `ANY` が商品に対して `TRUE` または `FALSE` である場合、その商品がAmazonにリストされる資格を得ることができます。

条件は、既存の製品属性値に基づきます。 すべての製品にルールを適用する場合は、「条件」セクションを空白のままにします。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、属性の **[!UICONTROL Use for Promo Rule Conditions]** 設定を `Yes` に設定します。 この設定には、属性の [ ストアフロントのプロパティ ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) ページでアクセスできます。

![ 条件 – 1 行目 ](assets/ob-listing-rule-conditions-start.png){width="500"}

この例のルールは、_Amazon FBA_ 属性が `Yes` に設定されているすべてのカタログ製品に対してAmazonの実施要件を設定するルールを定義します。

ルール ステートメントには 2 つの太字リンクがあり、クリックすると、ステートメントのその部分のオプションが表示されます。 太字のオプションを変更せずに条件を保存すると、ルールはすべての商品に適用されます。

- 「**[!UICONTROL ALL]**」をクリックし、`ALL` または `ANY` を選択します。
- 「**[!UICONTROL TRUE]**」をクリックし、「`TRUE`」または「`FALSE`」を選択します。
- すべての製品にルールを適用する場合は、条件を変更しません。

これらの値の組み合わせを変更することで、様々な条件を作成できます。 この例では、次の条件を使用します。

`If ALL of these conditions are TRUE:`

1. 条件行の先頭にある「追加」（![ 追加アイコン ](assets/btn-add-grn.png)）アイコンをクリックし、条件のベースとなる属性（条件の組み合わせや製品属性など）を選択します。

   - **[!UICONTROL Conditions Combination]** – 既存のセット内に条件と条件の別のセットを作成できる `All/Any` うに選択 `True/False` ます。

     ![ 条件の組み合わせ ](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]** – 製品属性は、属性の設定によって異なります。 属性をリストに表示するには、プロモーションルールの条件で使用できるように設定する必要があります。 [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) の _プロモルール条件の使用_ を参照してください。

     **[!UICONTROL Product Attribute]** の下のリストで、条件の基礎として使用する属性を選択します。 この例では、選択した条件は `Amazon FBA` です。

     ![ 条件 2 行目、パート 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     選択した条件がステートメントに表示され、その後にさらに 2 つの太字リンクが表示されます。 オプションは、選択する製品属性によって異なります。

     属性を設定した後は、変更できません。 属性を変更するには、行を削除して新しい属性を追加する必要があります。 条件行を削除するには、行の最後にある削除（![ 削除アイコン ](assets/btn-del-red.png)）アイコンをクリックします。

      1. 「**[!UICONTROL is]**」をクリックして、満たす製品の条件を説明する比較演算子を選択します。

         この例では、比較演算子は `is` です。 使用可能なオプションは、前の手順で選択した属性によって異なります。 オプションには、値の一致、1 つ以上の値を含まない、または含まない、数値より大きい、数値と等しい、数値より小さいなど、様々な比較オプションを含めることができます。 この例では、オプションは `is` と `is not` です。

      1. 「**[!UICONTROL ...]**」をクリックして、条件の基となる属性値を選択します。

         オプションは、属性の設定によって異なります。 オプションを選択するか、条件のテキストまたは数値を入力するように求めるプロンプトが表示される場合があります。 この例では、選択範囲は `Yes` です。

         条件を完了するためのステートメントに、選択した項目が表示されます。

         ![ 条件 2 のパート 3](assets/ob-listing-rule-condition-is.png){width="500"}

   この条件が完了しました。 前述のように、この条件は、Amazon FBA 属性の値が `Yes` に設定された [!DNL Commerce] カタログ内の商品が、地域およびストアに関してAmazonにリストできる資格があることを意味します。 条件ラインを追加して、実施要件を満たす製品をさらに絞り込むことができます。

1. ステートメントに別の条件行を追加するには、手順 1 に戻り、必要なすべての条件が完了するまで手順を繰り返します。

条件文の行の最後にある削除（![ 削除アイコン ](assets/btn-del-red.png)）アイコンをクリックすると、その行をいつでも削除できます。
