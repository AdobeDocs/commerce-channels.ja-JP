---
title: '例： Amazonリストルールの条件の定義'
description: リストルールを作成する際に、Amazon Marketplace に表示する Commerce カタログ商品を識別する条件を定義します。
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---

# 例：条件の定義

## 条件

条件内の太字の領域をクリックすると、様々なオプションを表示できます。

**選択した Web サイト内のすべての製品が適格な場合は、条件を追加しないでください。**

>[!NOTE]
>
>Amazonのシステムと直接通信する複雑なバックエンドプロセスのセットがあります。 リストしようとしている項目の数と、Amazonのシステムのビジー状態（ブラックフライデーなど）に基づいて、Amazonに項目がリストされるまでに時間がかかる場合があります。

詳しくは、 [買い物かごの価格ルールの作成](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## 条件の定義

このプロセスは、カタログの設定に応じて、簡単に実行することも、詳細に設定することもできます。 条件を設定して、 `ALL` または `ANY` 定義条件のいずれかが `TRUE` または `FALSE` 製品の場合、その製品はAmazonにリストされる資格があります。

条件は、既存の製品属性値に基づいています。 すべての製品にルールを適用する場合は、「条件」セクションを空白のままにします。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、 **[!UICONTROL Use for Promo Rule Conditions]** 属性の設定 `Yes`. この設定には、 [ストアフロントのプロパティ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) ページを開きます。

![条件 — 行 1](assets/ob-listing-rule-conditions-start.png){width="500"}

この例のルールでは、 _AmazonFBA_ 属性を `Yes`.

ルールステートメントには 2 つの太字のリンクがあり、このリンクをクリックすると、ステートメントのその部分のオプションが表示されます。 太字オプションを変更せずに条件を保存した場合、ルールはすべての製品に適用されます。

- クリック **[!UICONTROL ALL]** を選択し、 `ALL` または `ANY`.
- クリック **[!UICONTROL TRUE]** を選択し、次のいずれかを選択します。 `TRUE` または `FALSE`.
- すべての製品にルールを適用する場合は、条件を変更しないでください。

これらの値の組み合わせを変更することで、異なる条件を作成できます。 この例では、次の条件が使用されます。

`If ALL of these conditions are TRUE:`

1. 「追加」(![追加アイコン](assets/btn-add-grn.png)) をクリックし、条件の基にする属性（条件の組み合わせや製品属性など）を選択します。

   - **[!UICONTROL Conditions Combination]**  — 別のセットを作成できるように選択します。 `All/Any` および `True/False` 条件を既存のセット内に配置する。

     ![条件の組み合わせ](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]**  — 製品属性は、属性の設定によって異なります。 属性をリストに表示するには、プロモーションルール条件での使用に合わせて設定する必要があります。 詳しくは、 _プロモーションルール条件に使用_ in [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     の下のリストで **[!UICONTROL Product Attribute]**」で、条件の基準として使用する属性を選択します。 この例では、選択された条件は次のようになります。 `Amazon FBA`.

     ![条件ライン 2、パート 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     選択した条件がステートメントに表示され、その後にさらに 2 つの太字のリンクが続きます。 オプションは、選択した製品属性によって異なります。

     属性を設定した後は、変更できません。 属性を変更するには、行を削除し、新しい属性を追加する必要があります。 条件行を削除するには、「削除」(![削除アイコン](assets/btn-del-red.png)) アイコンをクリックします。

      1. クリック **[!UICONTROL is]** を選択し、満たす製品の条件を記述する比較演算子を選択します。

         この例では、比較演算子は次のようになります。 `is`. 使用できるオプションは、前の手順で選択した属性によって異なります。 オプションには、一致する値（値を少なくとも 1 つ含まないか、含む）、より大きい、等しい、数値未満の値など ) など、異なる比較オプションを含めることができます。 この例では、次のオプションがあります。 `is` および `is not`.

      1. クリック **[!UICONTROL ...]** 条件の基となる属性値を選択します。

         オプションは、属性の設定によって異なります。 オプションを選択するか、条件のテキストまたは数値を入力するよう求められる場合があります。 この例では、「 」を選択します。 `Yes`.

         選択した項目が、条件を完了するためにステートメント内に表示されます。

         ![条件ライン 2、パート 3](assets/ob-listing-rule-condition-is.png){width="500"}

   この条件は完了しました。 この条件は、 [!DNL Commerce] Amazon FBA 属性が `Yes` は、その地域とストアにAmazonにリストする資格があります。 さらに条件ラインを追加して、対象製品を絞り込むことができます。

1，文に別の条件行を追加するには、手順 1 に戻り、必要なすべての条件が完了するまでプロセスを繰り返します。

条件文の行は、いつでも削除できます。削除するには、![削除アイコン](assets/btn-del-red.png)) アイコンをクリックします。
