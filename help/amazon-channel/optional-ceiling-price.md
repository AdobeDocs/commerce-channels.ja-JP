---
title: インテリジェントな価格変更ルール：オプション上限価格`
description: オプションの上限価格設定を使用して、Amazonの上限を管理するインテリジェントな価格ルールから最高の製品価格を保護します。
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール：オプションの上限価格

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [ルールタイプの選択](./intelligent-repricing-rules.md)
- [競合相手の条件の相違](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [下限価格](./floor-price.md)
- オプションの上限価格

自動上限価格設定は、最も高い製品価格をインテリジェントな価格ルールから自動的に保護し、インテリジェントな価格ルールの上限（最高価格）を設定できます。

## オプションの上限価格の設定

_[!UICONTROL Optional Ceiling Price]_セクションで、オプションの最高価格設定を定義します。

1. **[!UICONTROL Ceiling Price Source]**&#x200B;の場合、属性を選択します。

   相対的な上限を示す[!DNL Commerce] [product属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}を選択します。 例えば、Amazonの上場価格を品目のMSRPより上にしたくない場合は、`Manufacturer's Suggested Retail Price`属性を選択します。

1. **[!UICONTROL Ceiling Price Action]**&#x200B;の場合は、オプションを選択します。

   - `Decrease By` - Amazonにリストする前 _[!UICONTROL Ceiling Price Source]_に、定義した値を調整して、ルールの上限価格を下げるタイミングを選択します。

   - `Increase By` - Amazonにリストする前 _[!UICONTROL Ceiling Price Source]_に、定義した値を調整して、ルールの上限価格を高くするタイミングを選択します。

   - `Match`  — 定義した値を上回る上場価格を変動させない場合に選択し _[!UICONTROL Ceiling Price Source]_ます。`Match`に設定すると、_[!UICONTROL Apply]_&#x200B;フィールドと&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効になります。

1. **[!UICONTROL Apply]**&#x200B;はデフォルトのまま`Apply as percentage`にします。

1. **[!UICONTROL Ceiling Adjustment Price]**&#x200B;には、_[!UICONTROL Ceiling Price Source]_値を調整する割合の数値を入力します。

この例では、上限価格が品目のMSRPより2%低く設定されています。

![インテリジェントな価格変更ルール — オプションの上限価格](assets/ob-intelligent-price-rule-ceiling.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Ceiling Price Source] | 相対的な上限を示す[!DNL Commerce] [product属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}を選択します。 例えば、製品のリスト価格を品目のMSRPより上にしたくない場合は、`Manufacturer's Suggested Retail Price`属性を選択します。 |
| [!UICONTROL Ceiling Price Action] | 価格調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** - Amazonにリストする前 _[!UICONTROL Ceiling Price Source]_に、定義した値を調整して、ルールの上限価格を下げるタイミングを選択します。</li><li>**[!UICONTROL Increase By]** - Amazonにリストする前 _[!UICONTROL Ceiling Price Source]_に、定義した値を調整して、ルールの上限価格を高くするタイミングを選択します。</li><li>**[!UICONTROL Match]**  — 定義した値を上回る上場価格を変動させない場合に選択し _[!UICONTROL Ceiling Price Source]_ます。`Match`に設定すると、_[!UICONTROL Apply]_&#x200B;フィールドと&#x200B;_[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効になります。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 値に対するパーセント調整 _[!UICONTROL Ceiling Price Source]_。 |
| [!UICONTROL Ceiling Price Adjustment] | _[!UICONTROL Ceiling Price Source]_の値を調整するパーセントの数値を入力します。 |
