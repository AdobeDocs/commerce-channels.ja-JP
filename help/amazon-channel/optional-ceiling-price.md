---
title: '''インテリジェントな価格変更ルール：オプションの上限価格`'
description: オプションの上限価格設定を使用して、Amazonの一覧を管理するインテリジェントな価格ルールから最も高い製品価格を保護します。
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# インテリジェントな価格変更ルール：オプションの上限価格

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [ルールタイプを選択](./intelligent-repricing-rules.md)
- [競合相手の条件付き相違](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [下限価格](./floor-price.md)
- オプションの上限価格

自動上限価格設定は、インテリジェントな価格ルールに対して最高の製品価格を自動的に保護し、インテリジェントな価格ルールの上限（最高価格）を設定できます。

## オプションの上限価格の設定

オプションの最高価格設定を _[!UICONTROL Optional Ceiling Price]_」セクションに入力します。

1. の場合 **[!UICONTROL Ceiling Price Source]**、属性を選択します。

   を選択します。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、相対的な上限を示します。 例えば、Amazonの上場価格を品目の MSRP よりも高くしたくない場合は、 `Manufacturer's Suggested Retail Price` 属性。

1. の場合 **[!UICONTROL Ceiling Price Action]**、「 」オプションを選択します。

   - `Decrease By`  — 定義する _[!UICONTROL Ceiling Price Source]_値を調整して、ルールの上限価格を下げ、Amazonにリストする前に作成します。

   - `Increase By`  — 定義する _[!UICONTROL Ceiling Price Source]_値を調整して、ルールの上限価格を高くし、Amazonにリストする前に設定します。

   - `Match`  — 定義した _[!UICONTROL Ceiling Price Source]_の値です。 に設定する場合 `Match`、_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効です。

1. を **[!UICONTROL Apply]** デフォルト： `Apply as percentage`.

1. の場合 **[!UICONTROL Ceiling Adjustment Price]**、調整する割合の数値を入力します。 _[!UICONTROL Ceiling Price Source]_の値です。

この例では、上限価格が品目の MSRP より 2%低く設定されています。

![インテリジェントな価格変更ルール — オプションの上限価格](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | を選択します。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、相対的な上限を示します。 例えば、製品リストの価格を品目の MSRP よりも高くしたくない場合、 `Manufacturer's Suggested Retail Price` 属性。 |
| [!UICONTROL Ceiling Price Action] | 価格調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]**  — 定義する _[!UICONTROL Ceiling Price Source]_値を調整して、ルールの上限価格を下げ、Amazonにリストする前に作成します。</li><li>**[!UICONTROL Increase By]**  — 定義する _[!UICONTROL Ceiling Price Source]_値を調整して、ルールの上限価格を高くし、Amazonにリストする前に設定します。</li><li>**[!UICONTROL Match]**  — 定義した _[!UICONTROL Ceiling Price Source]_の値です。 に設定する場合 `Match`、_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効です。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - _[!UICONTROL Ceiling Price Source]_の値です。 |
| [!UICONTROL Ceiling Price Adjustment] | パーセントを調整する数値を入力します _[!UICONTROL Ceiling Price Source]_の値です。 |
