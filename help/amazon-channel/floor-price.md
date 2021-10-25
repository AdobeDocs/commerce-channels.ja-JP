---
title: '「インテリジェントな価格設定ルール: フロア価格」'
description: 「フロア価格」設定を使用して、Amazon リストを管理するためのインテリジェントな価格設定ルールの最低価格を決定することができます。
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# インテリジェントな価格設定ルール: フロア価格

インテリジェントな「価格設定」ルールのセクションには、次のものが含まれます。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

[フロア価格設定では、 ](./floor-price.md) 最低製品価格がインテリジェントな価格設定ルールに自動的に適用されます。これらの設定を使用して、インテリジェントな価格設定ルールにフロア (最低価格) を設定します。製品が必要な価格の下に表示されていないことを確認してください。

フロア価格属性は、 [!DNL Commerce] ストアが web サイトの価格設定を使用している場合に、web サイトの範囲に基づいています。 「価格スコープ」を参照してください [ ](./price-scope.md) 。

フロア価格は、がに設定されている場合にのみ使用され **[!UICONTROL Rule Type]** `Intelligent repricing rule` ます。

## フロア価格の設定

「」セクションで、最低価格設定を定義 _[!UICONTROL Floor Price]_します。

1. については **[!UICONTROL Floor Price Source]** 、「価格ソース」属性を選択します。

   [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) 相対的なフロア上限数を示す product 属性 {target = &quot;_blank&quot;} を選択します。例えば、Amazon のリスト価格が品目のコストを下回ることがないようにするには、「cost」属性を選択し ** ます。

1. **[!UICONTROL Floor Price Action]**&#x200B;では、オプションを選択します。

   - `Decrease By` -設定されている _[!UICONTROL Floor Price Source]_値を下に調整し、Amazon の一覧を作成する前にルールのフロア価格を小さくする場合に選択します。

   - `Increase By` -設定した値が調整されて、 _[!UICONTROL Floor Price Source]_Amazon の表示前にルールのフロア価格が高くなるようにする場合に選択します。

   - `Match` -定義された値よりもリスト価格が変動しないようにする場合に選択し _[!UICONTROL Floor Price Source]_ます。 「」に設定されている場合、 `Match`_[!UICONTROL Apply]_ および _[!UICONTROL Floor Adjustment Amount]_フィールドは無効になります。

1. デフォルトのままにし **[!UICONTROL Apply]** ておき `Apply as percentage` ます。

1. に **[!UICONTROL Floor Adjustment Price]** 値を入力して調整するには、比率の数値を入力し _[!UICONTROL Floor Price Source]_ます。

この例では、フロア価格が品目のコストの3% 以上に設定されています。

![インテリジェントな価格設定ルール例: フロア価格](assets/ob-intelligent-pricde-rule-floor-price.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Floor Price Source] | [!DNL Commerce]相対フロア (最低価格) 制限を示す属性を選択します。例えば、Amazon のリスト価格が品目のコストを下回ることがないようにするには、属性を選択し `Cost` ます。 |
| [!UICONTROL Floor Price Action] | 「価格調整」アクションを選択します。 オプション：<ul><li>**[!UICONTROL Decrease By]** -設定されている _[!UICONTROL Floor Price Source]_値を下に調整し、Amazon の一覧を作成する前にルールのフロア価格を小さくする場合に選択します。</li><li>**[!UICONTROL Increase By]** -設定した値が調整されて、 _[!UICONTROL Floor Price Source]_Amazon の表示前にルールのフロア価格が高くなるようにする場合に選択します。</li><li>**[!UICONTROL Match]** -定義された値よりもリスト価格が変動しないようにする場合に選択し _[!UICONTROL Floor Price Source]_ます。 この設定を選択する_[!UICONTROL Apply]_ と、and _[!UICONTROL Floor Adjustment Amount]_フィールドが無効化されます。</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** -値を基準とした割合での比率を _[!UICONTROL Floor Price Source]_指定します。 |
| [!UICONTROL Floor Adjustment Amount] | 値を調整する場合は、比率の数値を入力し _[!UICONTROL Floor Price Source]_ます。 |
