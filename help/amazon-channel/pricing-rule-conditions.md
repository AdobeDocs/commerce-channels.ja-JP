---
title: Amazon販売チャネル – 価格ルール条件
description: 価格ルール条件を使用して、上場価格ルールの対象となる製品を決定します。
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# 価格ルール条件

条件は、価格ルールの対象となる製品を決定します。 Amazonの価格ルールの条件の定義は、[!DNL Commerce] での [ 買い物かご価格ルール ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) の条件の定義と同じロジックとプロセスに従います。

>[!IMPORTANT]
>
>価格ルールが [!DNL Commerce] カタログ内のすべての製品に適用される場合は、このセクションを空白のままにします。

条件内の太字で表示されている領域をクリックして、様々なオプションを表示できます。

## 例：価格ルール条件の作成

このプロセスは、カタログの設定に応じて、単純なものでも詳細なものでもかまいません。 条件を定義すると、`ALL` または `ANY` の条件が商品に対して `TRUE` または `FALSE` の場合に、その商品が価格設定ルールの適用対象となります。

条件は [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) に基づいています。 すべての製品にルールを適用する場合は、「条件」セクションを空白のままにします。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、属性の **ストアフロントのプロパティ** で、属性の [ プロモルール条件に使用 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) を `Yes` に設定する必要があります。

![ 価格ルール条件 – 1 行目 ](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

次の例では、`Books` カテゴリに定義されているすべての製品に 25% の割引を適用するルールを定義します。

ルール ステートメントには 2 つの太字リンクがあり、クリックすると、条件ステートメントのその部分のオプションが表示されます。 太字のオプションを変更せずに条件を保存すると、ルールはすべての商品に適用されます。

- 「**[!UICONTROL ALL]**」をクリックし、「`ALL`」または「`ANY`」を選択します。
- 「**[!UICONTROL TRUE]**」をクリックし、「`TRUE`」または「`FALSE`」を選択します。
- すべての製品にルールを適用する場合は、条件を変更しません。

これらの値の組み合わせを変更することで、様々な条件を作成できます。 この例では、次の条件を使用します。

`If ALL of these conditions are TRUE:`

1. 条件が適用される使用可能な属性を表示するには、条件行の先頭にある「追加」（![ 追加アイコン ](assets/btn-add-grn.png)）アイコンをクリックし、条件のベースとなる属性を選択します。

   **[!UICONTROL Conditions Combination]** – 既存の条件内に `All/Any` 条件と `True/False` 条件の別のセットを作成する場合に選択します。

   ![ 価格ルール条件の組み合わせ ](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]** – 使用できる製品属性は、[ 属性の設定 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) によって異なります。 リストに属性を表示するには、ストアフロントのプロパティで属性の *[!UICONTROL Use for Promo Rule Conditions]* を `Yes` に設定する必要があります。

   - **[!UICONTROL Product Attribute]**：条件のベースとして定義する属性を選択します。 この例では、選択した条件は `Category` です。

     ![ 価格ルール条件 – ライン 2、パート 2](assets/ob-price-rule-condition-2.png){width="500"}

     選択した条件がステートメントに表示され、その後にさらに 2 つの太字リンクが表示されます。 オプションは、選択する製品属性によって異なります。

     属性を設定した後は、編集できません。 属性を変更するには、行を削除して新しい属性を追加する必要があります。 条件行を削除するには、行の最後にある削除（![ 削除アイコン ](assets/btn-del-red.png) アイコンをクリックします。

   - 「**[!UICONTROL is]**」をクリックして、満たす製品の条件を説明する比較演算子を選択します。

     この例では、比較演算子は `is` です。 使用できるオプションは、前の手順で選択した属性によって異なり、異なる比較オプションが含まれる場合があります。 オプションには、一致する値を含めたり、1 つ以上の値を含めなかったり、数値より大きい、数値と等しい、または数値より小さい値を含めることができます。 この例では、オプションは `is` と `is not` です。

   - 「**[!UICONTROL ...]**」をクリックして、条件の基となる属性値を選択します。 オプションは、属性の設定によって異なります。

     条件のオプションを選択するか、値を入力するように求めるプロンプトが表示される場合があります。 この例では、フィールドは空白で表示されます。 ルールのカテゴリを選択するには、選択アイコン（![ 選択アイコン ](assets/btn-chooser.png)）をクリックして選択オプションを表示します。 このルールは _ブック_ 用です。「**[!UICONTROL Books]**」チェックボックスをオンにします。 カテゴリ番号が入力されます。 カテゴリの選択を受け入れるには、緑色のチェックマークアイコン（![ チェックマークアイコン ](assets/btn-check-mark-green.png)）をクリックします。

     ![ 価格ルール条件 – 2 行目、パート 3](assets/ob-price-rule-condition-3.png){width="500"}

     条件を完了するためのステートメントに、選択した項目が表示されます。

     ![ 価格ルール条件 – 2 行目、パート 4](assets/ob-price-rule-condition-4.png){width="500"}

     この条件の例はこれで完了です。 前述のように、この条件は、[!DNL Commerce] カタログ内の商品で、カテゴリが「帳簿」（`4`）が定義されているものがこの価格ルールの対象であることを意味します。 条件ラインを追加して、実施要件を満たす製品をさらに絞り込むことができます。

1. ステートメントに別の条件行を追加するには、手順 1 に戻り、必要なすべての条件が完了するまでプロセスを繰り返します。

   条件文の行の最後にある削除（![ 削除アイコン ](assets/btn-del-red.png)）アイコンをクリックすると、その行をいつでも削除できます。
