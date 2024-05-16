---
title: 'インテリジェント価格再設定ルール：最低価格'
description: 床価格の設定を使用して、Amazonのリストを管理するインテリジェントな価格ルールの最低価格を決定します。
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# インテリジェント再価格設定ルール：定価

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

この [床価格](./floor-price.md) 設定により、インテリジェントな価格設定ルールに対して自動的に最低価格の製品価格が保護されます。 これらの設定を使用して、インテリジェントな価格設定ルールの下限価格（最低価格）を設定し、製品が希望価格を下回らないようにします。

階価属性は、Web サイトの範囲に基づきます（使用する場合） [!DNL Commerce] ストアは web サイトの価格範囲を使用しています。 参照： [価格範囲](./price-scope.md).

最低価格は、次の場合にのみ使用されます **[!UICONTROL Rule Type]** はに設定されています。 `Intelligent repricing rule`.

## 最低価格の設定

で最低価格の設定を定義 _[!UICONTROL Floor Price]_セクション。

1. の場合 **[!UICONTROL Floor Price Source]**：価格ソース属性を選択します。

   を選択します。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、床の相対的な制限を示します。 例えば、Amazonのリスト価格を商品のコストを下回りたくない場合は、を選択します。 *コスト* 属性。

1. の場合 **[!UICONTROL Floor Price Action]**、オプションを選択します。

   - `Decrease By`  – を定義するタイミングを選択します _[!UICONTROL Floor Price Source]_Amazonにリストする前に調整する値で、ルールのフロア価格を下げます。

   - `Increase By`  – を定義するタイミングを選択します _[!UICONTROL Floor Price Source]_Amazonにリストする前に調整する値で、ルールのフロア価格を高めます。

   - `Match`  – 上場価格を定義済みより下に変動させたくない場合に選択します _[!UICONTROL Floor Price Source]_の値。 に設定されている場合 `Match`,_[!UICONTROL Apply]_ および _[!UICONTROL Floor Adjustment Amount]_フィールドは無効です。

1. を残す **[!UICONTROL Apply]** デフォルト： `Apply as percentage`.

1. の場合 **[!UICONTROL Floor Adjustment Price]**&#x200B;を選択し、調整する割合の数値を入力します _[!UICONTROL Floor Price Source]_の値。

この例では、フロアプライスを品目のコストより 3% 高く設定しています。

![インテリジェントな再価格設定ルールの例：下限価格](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | を選択します。 [!DNL Commerce] 相対的な最低価格の上限を示す属性。 例えば、Amazonのリスト価格を商品のコストを下回りたくない場合は、を選択します。 `Cost` 属性。 |
| [!UICONTROL Floor Price Action] | 価格設定調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]**  – を定義するタイミングを選択します _[!UICONTROL Floor Price Source]_Amazonにリストする前に調整する値で、ルールのフロア価格を下げます。</li><li>**[!UICONTROL Increase By]**  – を定義するタイミングを選択します _[!UICONTROL Floor Price Source]_Amazonにリストする前に調整する値で、ルールのフロア価格を高めます。</li><li>**[!UICONTROL Match]**  – 上場価格を定義済みより下に変動させたくない場合に選択します _[!UICONTROL Floor Price Source]_の値。 選択した場合、_[!UICONTROL Apply]_ および _[!UICONTROL Floor Adjustment Amount]_フィールドは無効です。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  – を基準としたパーセント調整 _[!UICONTROL Floor Price Source]_の値。 |
| [!UICONTROL Floor Adjustment Amount] | を調整するためのパーセントの数値を入力してください _[!UICONTROL Floor Price Source]_の値。 |
