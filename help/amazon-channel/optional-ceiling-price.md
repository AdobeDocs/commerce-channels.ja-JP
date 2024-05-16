---
title: 「インテリジェント再価格設定ルール：オプションの上限価格」
description: オプションの上限価格の設定を使用すると、Amazonのリストを管理するインテリジェントな価格ルールに対して最高の商品価格を保護できます。
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# インテリジェント再価格設定ルール：オプションの上限価格

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- [ルールタイプを選択](./intelligent-repricing-rules.md)
- [競合他社条件付き差異](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [フロアプライス](./floor-price.md)
- オプションの上限価格

自動化された天井価格の設定により、インテリジェントな価格設定ルールに対して最高の製品価格が自動的に保護されるため、インテリジェントな価格設定ルールに対して上限（最高価格）を設定できます。

## オプションの上限価格を設定

オプションの最高価格設定をで定義する _[!UICONTROL Optional Ceiling Price]_セクション。

1. の場合 **[!UICONTROL Ceiling Price Source]**&#x200B;属性を選択します。

   を選択 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、相対的な上限を示します。 例えば、Amazonのリスト価格を商品の MSRP を超えたくない場合は、 `Manufacturer's Suggested Retail Price` 属性。

1. の場合 **[!UICONTROL Ceiling Price Action]**、オプションを選択します。

   - `Decrease By`  – を定義するタイミングを選択します _[!UICONTROL Ceiling Price Source]_Amazonにリストする前に調整する値で、ルールの上限価格を下げます。

   - `Increase By`  – を定義するタイミングを選択します _[!UICONTROL Ceiling Price Source]_Amazonにリストする前に調整する値を指定し、ルールの上限価格を高めます。

   - `Match`  – 上場価格を定義済みの価格を超えて変動させたくない場合に選択します _[!UICONTROL Ceiling Price Source]_の値。 に設定されている場合 `Match`,_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効です。

1. を残す **[!UICONTROL Apply]** デフォルト： `Apply as percentage`.

1. の場合 **[!UICONTROL Ceiling Adjustment Price]**&#x200B;を選択し、調整する割合の数値を入力します _[!UICONTROL Ceiling Price Source]_の値。

この例では、天井の価格は品目の MSRP を 2% 下回るように設定されています。

![インテリジェントな価格設定ルール：オプションの上限価格](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | を選択します。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、相対的な上限を示します。 例えば、製品一覧価格を商品の MSRP を超えたくない場合は、 `Manufacturer's Suggested Retail Price` 属性。 |
| [!UICONTROL Ceiling Price Action] | 価格設定調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]**  – を定義するタイミングを選択します _[!UICONTROL Ceiling Price Source]_Amazonにリストする前に調整する値で、ルールの上限価格を下げます。</li><li>**[!UICONTROL Increase By]**  – を定義するタイミングを選択します _[!UICONTROL Ceiling Price Source]_Amazonにリストする前に調整する値を指定し、ルールの上限価格を高めます。</li><li>**[!UICONTROL Match]**  – 上場価格を定義済みの価格を超えて変動させたくない場合に選択します _[!UICONTROL Ceiling Price Source]_の値。 に設定されている場合 `Match`,_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効です。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  – を基準としたパーセント調整 _[!UICONTROL Ceiling Price Source]_の値。 |
| [!UICONTROL Ceiling Price Adjustment] | を調整するためのパーセントの数値を入力してください _[!UICONTROL Ceiling Price Source]_の値。 |
