---
title: 'インテリジェントな価格変更ルール：下限価格'
description: 最低価格設定を使用して、Amazonのリストを管理するインテリジェントな価格ルールの最低価格を決定します。
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# インテリジェントな価格変更ルール：下限価格

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

The [下値](./floor-price.md) 設定は、インテリジェントな価格ルールに対して、最低価格の製品を自動的に保護します。 これらの設定を使用して、インテリジェントな価格ルールの下限（最低価格）を設定し、製品が希望の価格以下に表示されないようにします。

下限価格属性は、Web サイトの範囲に基づきます ( [!DNL Commerce] ストアは web サイトの価格範囲を使用しています。 詳しくは、 [価格範囲](./price-scope.md).

下限価格は、 **[!UICONTROL Rule Type]** が `Intelligent repricing rule`.

## 下限価格を設定

最も低い価格設定を _[!UICONTROL Floor Price]_」セクションに入力します。

1. の場合 **[!UICONTROL Floor Price Source]**、価格のソース属性を選択します。

   を選択します。 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) これは、相対的な床の限界を示します。 例えば、Amazonの上場価格が商品のコストを下回りたくない場合は、 *コスト* 属性。

1. の場合 **[!UICONTROL Floor Price Action]**、「 」オプションを選択します。

   - `Decrease By`  — いつ定義するかを選択します _[!UICONTROL Floor Price Source]_値を調整して、Amazonにリストする前に、ルールの下限価格を下げます。

   - `Increase By`  — いつ定義するかを選択します _[!UICONTROL Floor Price Source]_値を調整して、ルールの下限価格を高くし、Amazonにリストする前に作成します。

   - `Match`  — 定義した価格を下回る株価変動を望まない場合に選択します _[!UICONTROL Floor Price Source]_の値です。 に設定する場合 `Match`、_[!UICONTROL Apply]_ および _[!UICONTROL Floor Adjustment Amount]_フィールドは無効です。

1. を残します。 **[!UICONTROL Apply]** デフォルトは次のとおりです `Apply as percentage`.

1. の場合 **[!UICONTROL Floor Adjustment Price]**、調整する割合の数値を入力します。 _[!UICONTROL Floor Price Source]_の値です。

この例では、単価は品目のコストを 3%上回る値に設定されています。

![インテリジェントな価格変更ルールの例 — 下限価格](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | を選択します。 [!DNL Commerce] 相対下限（最低価格）を示す属性。 例えば、Amazonの上場価格が商品のコストを下回りたくない場合は、 `Cost` 属性。 |
| [!UICONTROL Floor Price Action] | 価格調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]**  — いつ定義するかを選択します _[!UICONTROL Floor Price Source]_値を調整して、Amazonにリストする前に、ルールの下限価格を下げます。</li><li>**[!UICONTROL Increase By]**  — いつ定義するかを選択します _[!UICONTROL Floor Price Source]_値を調整して、ルールの下限価格を高くし、Amazonにリストする前に作成します。</li><li>**[!UICONTROL Match]**  — 定義した価格を下回る株価変動を望まない場合に選択します _[!UICONTROL Floor Price Source]_の値です。 選択すると、_[!UICONTROL Apply]_ および _[!UICONTROL Floor Adjustment Amount]_フィールドは無効です。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]**  — 基準となる割合調整 _[!UICONTROL Floor Price Source]_の値です。 |
| [!UICONTROL Floor Adjustment Amount] | パーセントを調整する数値を入力します _[!UICONTROL Floor Price Source]_の値です。 |
