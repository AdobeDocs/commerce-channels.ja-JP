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

[ フロア価格 ](./floor-price.md) 設定は、インテリジェントな価格設定ルールに対して自動的に最低価格の製品価格を保護します。 これらの設定を使用して、インテリジェントな価格設定ルールの下限価格（最低価格）を設定し、製品が希望価格を下回らないようにします。

[!DNL Commerce] ストアが web サイトの価格範囲を使用している場合、フロアの価格属性は web サイトの範囲に基づきます。 [ 価格範囲 ](./price-scope.md) を参照してください。

Floor price は、**[!UICONTROL Rule Type]** が `Intelligent repricing rule` に設定されている場合にのみ使用されます。

## 最低価格の設定

_[!UICONTROL Floor Price]_のセクションで最低価格の設定を定義します。

1. **[!UICONTROL Floor Price Source]** の場合は、価格ソース属性を選択します。

   床の相対的な制限を示す [!DNL Commerce] [product 属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) を選択します。 例えば、Amazonのリスト価格が商品のコストを下回らないようにする場合は、*コスト* 属性を選択します。

1. **[!UICONTROL Floor Price Action]** の場合は、オプションを選択します。

   - `Decrease By` – 定義済みの _[!UICONTROL Floor Price Source]_値を下に調整するタイミングを選択し、Amazonにリストする前にルールの下限価格を下げます。

   - `Increase By` – 定義済みの _[!UICONTROL Floor Price Source]_値を調整するタイミングを選択し、Amazonにリストする前にルールのフロア価格を高くします。

   - `Match` – 上場価格を定義済みの _[!UICONTROL Floor Price Source]_値を下回って変動させたくない場合に選択します。 `Match` に設定すると、「_[!UICONTROL Apply]_」フィールドと「_[!UICONTROL Floor Adjustment Amount]_」フィールドが無効になります。

1. **[!UICONTROL Apply]** のデフォルトは `Apply as percentage` のままにします。

1. **[!UICONTROL Floor Adjustment Price]** の場合は、パーセントの数値を入力して、_[!UICONTROL Floor Price Source]_値を調整します。

この例では、フロアプライスを品目のコストより 3% 高く設定しています。

![ インテリジェントな再価格設定ルールの例 – 下限価格 ](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | 相対的な最低価格の上限を示す [!DNL Commerce] 属性を選択します。 例えば、Amazonのリスト価格が商品のコストを下回らないようにする場合は、`Cost` 属性を選択します。 |
| [!UICONTROL Floor Price Action] | 価格設定調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** – 定義済みの _[!UICONTROL Floor Price Source]_値を下に調整するタイミングを選択し、Amazonにリストする前にルールの下限価格を下げます。</li><li>**[!UICONTROL Increase By]** – 定義済みの _[!UICONTROL Floor Price Source]_値を調整するタイミングを選択し、Amazonにリストする前にルールのフロア価格を高くします。</li><li>**[!UICONTROL Match]** – 上場価格を定義済みの _[!UICONTROL Floor Price Source]_値を下回って変動させたくない場合に選択します。 これを選択すると、「_[!UICONTROL Apply]_」フィールドと「_[!UICONTROL Floor Adjustment Amount]_」フィールドが無効になります。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - _[!UICONTROL Floor Price Source]_値に対するパーセント調整。 |
| [!UICONTROL Floor Adjustment Amount] | パーセントの数値を入力して、_[!UICONTROL Floor Price Source]_値を調整します。 |
