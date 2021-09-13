---
title: インテリジェントな価格変更ルール：下限価格`
description: 最低価格設定を使用して、Amazonのリストを管理するインテリジェントな価格ルールの最低価格を決定します。
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール：価格

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

[下限価格](./floor-price.md)設定は、低価格の製品価格をインテリジェントな価格ルールから自動的に保護します。 これらの設定を使用して、インテリジェントな価格ルールの下限（最低価格）を設定し、製品が希望の価格以下に表示されないようにします。

[!DNL Commerce]ストアでWebサイトの価格スコープを使用している場合、下限価格属性はWebサイトの範囲に基づきます。 [価格範囲](./price-scope.md)を参照してください。

下限価格は、**[!UICONTROL Rule Type]**&#x200B;が`Intelligent repricing rule`に設定されている場合にのみ使用されます。

## 下限価格の設定

_[!UICONTROL Floor Price]_セクションで最低価格設定を定義します。

1. **[!UICONTROL Floor Price Source]**&#x200B;の場合、価格のソース属性を選択します。

   相対下限を示す[!DNL Commerce] [製品属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}を選択します。 例えば、Amazonの上場価格が商品のコストを下回りたくない場合は、*コスト*&#x200B;属性を選択します。

1. **[!UICONTROL Floor Price Action]**&#x200B;の場合は、オプションを選択します。

   - `Decrease By` - Amazonにリストする前に、定義し _[!UICONTROL Floor Price Source]_た値を調整して、ルールの下限価格を下げるタイミングを選択します。

   - `Increase By` - Amazonにリストする前 _[!UICONTROL Floor Price Source]_に、定義した値を調整して、ルールの下限価格を高くするタイミングを選択します。

   - `Match`  — 定義した値を下回る上場価格を変動させない場合に選択し _[!UICONTROL Floor Price Source]_ます。`Match`に設定すると、_[!UICONTROL Apply]_&#x200B;フィールドと&#x200B;_[!UICONTROL Floor Adjustment Amount]_フィールドは無効になります。

1. **[!UICONTROL Apply]**&#x200B;はデフォルトのまま`Apply as percentage`にします。

1. **[!UICONTROL Floor Adjustment Price]**&#x200B;には、_[!UICONTROL Floor Price Source]_値を調整する割合の数値を入力します。

この例では、販売価格は品目のコストを3%上回る値に設定されています。

![インテリジェントな価格変更ルールの例 — 下限価格](assets/ob-intelligent-pricde-rule-floor-price.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Floor Price Source] | 相対下限（最低価格）を示す[!DNL Commerce]属性を選択します。 例えば、Amazonの上場価格が商品のコストを下回りたくない場合は、`Cost`属性を選択します。 |
| [!UICONTROL Floor Price Action] | 価格調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** - Amazonにリストする前に、定義し _[!UICONTROL Floor Price Source]_た値を調整して、ルールの下限価格を下げるタイミングを選択します。</li><li>**[!UICONTROL Increase By]** - Amazonにリストする前 _[!UICONTROL Floor Price Source]_に、定義した値を調整して、ルールの下限価格を高くするタイミングを選択します。</li><li>**[!UICONTROL Match]**  — 定義した値を下回る上場価格を変動させない場合に選択し _[!UICONTROL Floor Price Source]_ます。選択すると、_[!UICONTROL Apply]_&#x200B;フィールドと&#x200B;_[!UICONTROL Floor Adjustment Amount]_フィールドが無効になります。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 値に対するパーセント調整 _[!UICONTROL Floor Price Source]_。 |
| [!UICONTROL Floor Adjustment Amount] | _[!UICONTROL Floor Price Source]_の値を調整するパーセントの数値を入力します。 |
