---
title: '「インテリジェントな価格設定規則」: 「天井価格」'
description: 任意の天井価格設定を使用して、Amazon リストを管理するためのインテリジェントな価格設定ルールに基づいて最高の製品価格を保護します。
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール: 「天井価格」

インテリジェントな「価格設定」ルールのセクションには、次のものが含まれます。

- [ルールタイプを選択します。](./intelligent-repricing-rules.md)
- [競合企業の条件付き差異](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [フロア価格](./floor-price.md)
- オプションの天井価格

「最大天井価格」設定では、最高の製品価格がインテリジェントな価格設定ルールに自動的に適用されます。これにより、インテリジェントな価格設定ルールに最大価格を設定することができます。

## 任意の天井価格の設定

セクションで、必要に応じて最高価格設定を定義 _[!UICONTROL Optional Ceiling Price]_します。

1. については **[!UICONTROL Ceiling Price Source]** 、属性を選択します。

   現在の製品属性を選択し [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) ます {target = &quot;_blank&quot;}。これは相対的な上限値を示します。 例えば、Amazon の表示価格がアイテムの MSRP 上に移動しないようにするには、属性を選択し `Manufacturer's Suggested Retail Price` ます。

1. **[!UICONTROL Ceiling Price Action]**&#x200B;では、オプションを選択します。

   - `Decrease By` -定義した値を下に調整し、その値を設定した _[!UICONTROL Ceiling Price Source]_後、Amazon のリストに表示されるようにする場合は、このオプションを選択します。

   - `Increase By` -定義した _[!UICONTROL Ceiling Price Source]_値を調整して、Amazon の表示前にルールの天井価格を上げる場合に選択します。

   - `Match` -定義された値よりもリスト価格が変動しないようにする場合に選択し _[!UICONTROL Ceiling Price Source]_ます。 「」に設定されている場合、 `Match`_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効になります。

1. デフォルトのままにし **[!UICONTROL Apply]** ておき `Apply as percentage` ます。

1. に **[!UICONTROL Ceiling Adjustment Price]** 値を入力して調整するには、比率の数値を入力し _[!UICONTROL Ceiling Price Source]_ます。

この例では、天井価格が品目の MSRP よりも2% 下に設定されています。

![インテリジェントな「価格設定」ルール: 「天井価格」](assets/ob-intelligent-price-rule-ceiling.png)

| 名 | つい |
|---|---|
| [!UICONTROL Ceiling Price Source] | [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) 相対的な上限値を示す product 属性 {target = &quot;_blank&quot;} を選択します。例えば、製品の出展価格が品目の MSRP の上に移動しないようにするには、属性を選択し `Manufacturer's Suggested Retail Price` ます。 |
| [!UICONTROL Ceiling Price Action] | 「価格調整」アクションを選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** -定義した値を下に調整し、その値を設定した _[!UICONTROL Ceiling Price Source]_後、Amazon のリストに表示されるようにする場合は、このオプションを選択します。</li><li>**[!UICONTROL Increase By]** -定義した _[!UICONTROL Ceiling Price Source]_値を調整して、Amazon の表示前にルールの天井価格を上げる場合に選択します。</li><li>**[!UICONTROL Match]** -定義された値よりもリスト価格が変動しないようにする場合に選択し _[!UICONTROL Ceiling Price Source]_ます。 「」に設定されている場合、 `Match`_[!UICONTROL Apply]_ および _[!UICONTROL Ceiling Adjustment Amount]_フィールドは無効になります。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** -値を基準とした割合での比率を _[!UICONTROL Ceiling Price Source]_指定します。 |
| [!UICONTROL Ceiling Price Adjustment] | 値を調整する場合は、比率の数値を入力し _[!UICONTROL Ceiling Price Source]_ます。 |
