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

オプションの最高価格設定を「_[!UICONTROL Optional Ceiling Price]_」セクションで定義します。

1. **[!UICONTROL Ceiling Price Source]**：属性を選択します。

   相対的な上限を示す [!DNL Commerce] [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) を選択します。 例えば、Amazonのリスト価格を商品の MSRP を超えたくない場合は、`Manufacturer's Suggested Retail Price` 属性を選択します。

1. **[!UICONTROL Ceiling Price Action]** の場合は、オプションを選択します。

   - `Decrease By` – 定義済みの _[!UICONTROL Ceiling Price Source]_値を下に調整するタイミングを選択し、Amazonにリストする前にルールの上限価格を下げます。

   - `Increase By` – 定義済みの _[!UICONTROL Ceiling Price Source]_値を調整するタイミングを選択し、Amazonにリストする前にルールの上限価格を高めます。

   - `Match` – 上場価格を定義済みの _[!UICONTROL Ceiling Price Source]_値を超えて変動させたくない場合に選択します。 `Match` に設定すると、「_[!UICONTROL Apply]_」フィールドと「_[!UICONTROL Ceiling Adjustment Amount]_」フィールドが無効になります。

1. **[!UICONTROL Apply]** のデフォルトは `Apply as percentage` のままにします。

1. **[!UICONTROL Ceiling Adjustment Price]** の場合は、パーセントの数値を入力して、_[!UICONTROL Ceiling Price Source]_値を調整します。

この例では、天井の価格は品目の MSRP を 2% 下回るように設定されています。

![ インテリジェントな価格再設定ルール – オプションの上限価格 ](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | 相対的な上限を示す [!DNL Commerce] [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) を選択します。 例えば、製品のリスト価格を商品の MSRP を超えたくない場合は、`Manufacturer's Suggested Retail Price` 属性を選択します。 |
| [!UICONTROL Ceiling Price Action] | 価格設定調整処理を選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** – 定義済みの _[!UICONTROL Ceiling Price Source]_値を下に調整するタイミングを選択し、Amazonにリストする前にルールの上限価格を下げます。</li><li>**[!UICONTROL Increase By]** – 定義済みの _[!UICONTROL Ceiling Price Source]_値を調整するタイミングを選択し、Amazonにリストする前にルールの上限価格を高めます。</li><li>**[!UICONTROL Match]** – 上場価格を定義済みの _[!UICONTROL Ceiling Price Source]_値を超えて変動させたくない場合に選択します。 `Match` に設定すると、「_[!UICONTROL Apply]_」フィールドと「_[!UICONTROL Ceiling Adjustment Amount]_」フィールドが無効になります。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - _[!UICONTROL Ceiling Price Source]_値に対するパーセント調整。 |
| [!UICONTROL Ceiling Price Adjustment] | パーセントの数値を入力して、_[!UICONTROL Ceiling Price Source]_値を調整します。 |
