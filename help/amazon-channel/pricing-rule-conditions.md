---
title: 価格ルール条件
description: 価格ルール条件を使用して、上場価格ルールに適格な製品を決定します。
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---

# 価格ルール条件

条件によって、価格ルールに適した製品が決まります。 Amazonの価格設定ルールの条件の定義は、 [買い物かごの価格ルール](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target="_blank"} in [!DNL Commerce].

>[!IMPORTANT]
>
>価格ルールが [!DNL Commerce] カタログを開き、このセクションは空白のままにします。

条件内の太字の領域をクリックすると、様々なオプションを表示できます。

## 例：価格ルール条件を作成する

このプロセスは、カタログ設定に応じて、簡単に実行することも、詳細に設定することもできます。 条件を定義して、 `ALL` または `ANY` の条件は、 `TRUE` または `FALSE` 製品の場合、製品は適用される価格ルールに適格です。

条件は、 [製品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"}. すべての製品にルールを適用する場合は、「条件」セクションを空白のままにします。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、 **プロモーションルール条件に使用** の場合、属性をに設定する必要があります。 `Yes` の [ストアフロントのプロパティ](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target="_blank"} 属性の。

![価格ルール条件 — 明細 1](assets/ob-price-rules-condition-1.png)

この例では、 `Books` カテゴリ。

ルールステートメントには 2 つの太字のリンクがあり、このリンクをクリックすると、条件ステートメントのその部分のオプションが表示されます。 太字オプションを変更せずに条件を保存した場合、ルールはすべての製品に適用されます。

- クリック **[!UICONTROL ALL]** を選択し、 `ALL` または `ANY`.
- クリック **[!UICONTROL TRUE]**&#x200B;を選択し、 `TRUE` または `FALSE`.
- すべての製品にルールを適用する場合は、条件を変更しないでください。

これらの値の組み合わせを変更することで、異なる条件を作成できます。 この例では、次の条件が使用されます。

`If ALL of these conditions are TRUE:`

1. 条件が適用される属性を表示するには、「追加」(![追加アイコン](assets/btn-add-grn.png)) アイコンをクリックし、条件の基準となる属性を選択します。

   **[!UICONTROL Conditions Combination]**  — 別のセットの作成を選択 `All/Any` および `True/False` 条件を既存の条件内に含めます。

   ![価格ルール条件の組み合わせ](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]**  — 使用可能な製品属性は、 [属性の設定](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target="_blank"}. For an attribute to show in the list, *[!UICONTROL Use for Promo Rule Conditions]* for the attribute must be set to `Yes` in your [storefront properties](https://docs.magento.com/user-guide/stores/attribute-product-create.html){target="_blank"}.

   - の場合 **[!UICONTROL Product Attribute]**「 」で、条件のベースとして定義する属性を選択します。 この例では、選択された条件は次のようになります。 `Category`.

      ![価格ルール条件 — 明細 2、パート 2](assets/ob-price-rule-condition-2.png)

      選択した条件がステートメントに表示され、その後にさらに 2 つの太字のリンクが続きます。 オプションは、選択した製品属性によって異なります。

      設定した属性は編集できません。 属性を変更するには、行を削除し、新しい属性を追加する必要があります。 条件行を削除するには、「削除」(![削除アイコン](assets/btn-del-red.png) アイコンをクリックします。

   - クリック **[!UICONTROL is]** を選択し、満たす製品の条件を記述する比較演算子を選択します。

      この例では、比較演算子は次のようになります。 `is`. 使用できるオプションは、前の手順で選択した属性によって異なり、異なる比較オプションを含めることができます。 オプションには、一致する値（値を少なくとも 1 つ含まないか、含まない）、およびより大きい、等しい、数値未満の値を含むことができます。 この例では、次のオプションがあります。 `is` および `is not`.

   - クリック **[!UICONTROL ...]** 条件の基となる属性値を選択します。 オプションは、属性の設定によって異なります。

      オプションを選択するか、条件の値を入力するよう求められる場合があります。 この例では、フィールドは空白で表示されます。 ルールのカテゴリを選択するには、選択アイコン (![選択アイコン](assets/btn-chooser.png)) をクリックして、選択オプションを表示します。 このルールは次用です。 _書籍_&#x200B;を選択し、 **[!UICONTROL Books]** チェックボックス。 カテゴリ番号が入力されます。 カテゴリの選択を受け入れるには、緑のチェックマークアイコン (![チェックマークアイコン](assets/btn-check-mark-green.png)) をクリックします。

      ![価格ルール条件 — 明細 2、パート 3](assets/ob-price-rule-condition-3.png)

      選択した項目が、条件を完了するためにステートメント内に表示されます。

      ![価格ルール条件 — 明細 2、パート 4](assets/ob-price-rule-condition-4.png)

      この例の条件は完了しました。 この条件は、 [!DNL Commerce] 定義された種類の書籍 (`4`) はこの価格ルールの対象です。 さらに条件ラインを追加して、対象製品を絞り込むことができます。

1. 文に別の条件行を追加するには、手順 1 に戻り、必要なすべての条件が完了するまでこの処理を繰り返します。

   条件文の行は、いつでも削除できます。削除するには、![削除アイコン](assets/btn-del-red.png)) アイコンをクリックします。
