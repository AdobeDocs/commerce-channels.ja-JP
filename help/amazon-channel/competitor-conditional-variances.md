---
title: インテリジェントな価格変更ルール：競合相手の条件付き相違`
description: インテリジェントな価格変更ルールを作成し、競合相手の価格と製品の条件に基づいてAmazonの上場価格を決定します。
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール：競合相手の条件の相違

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

インテリジェントな価格変更ルールでは、Amazonの競合他社の価格を使用して上場価格を決定します。 競合他社は、Amazonにリストしているのと同じ製品をリストしている他の販売者です。

同じ条件の製品が存在する場合、基本一致価格は同じ条件の[最も低い競合相手](./lowest-competitor-pricing.md)価格になります。 条件に一致する競合製品がない場合、基準一致価格は、「新規」、「改装」、「使用可能な条件」から始まり、使用可能な条件を続けて他の使用可能な競合製品の条件を調べます。 条件が見つかったら、基準一致価格がその条件内の最低価格になります。

条件`Used; Good`と基準一致価格が付いた製品があり、競合相手が同じ条件に同じ製品を低価格で持っている場合は、競合相手の価格が使用されます。 同じ条件で競合相手が存在しない場合は、次の条件(`New`)を持つ競合相手を確認します。 その条件で競合相手が見つかった場合は、最も安い価格が使用されます。

## 競合相手の条件の相違の設定

_[!UICONTROL Competitor Conditional Variances]_セクションで条件の相違を定義します。

**[!UICONTROL Conditional Variance]**&#x200B;の場合は、次のオプションを選択します。

- `Use all competitor's product conditions` - （デフォルト）商品を使用可能な条件と比較するタイミングを選択します（リストする条件に一致が存在しない場合）。

- `Use Only Matching Competitor's Product Condition`  — 同じ条件で競合他社の製品とのみ比較する場合に選択します。一致が存在しない場合は、[Magento価格](./listing-price.md)で定義された&#x200B;_リスト価格のソース_&#x200B;で価格が設定されます。

- `Apply Variance (if competitor's product condition differs)`  — 最初に、一致する製品条件との比較を試みることを選択します。一致条件が存在しない場合、差異（割合）は製品条件と最も低い競合相手の条件に対して適用されます。

   _[!UICONTROL Apply Variance]_機能を選択すると、Amazonの各条件に対して追加の平方偏差フィールドが表示されます。 この機能を使用すると、競合他社とは異なる条件の製品を提供する場合に、インテリジェントな価格変更ルールを使用できます。 条件付き差異の計算を理解するには、まずすべての差異が基準一致価格から決定されることを理解する必要があります。

   表示される条件付き分散オプションは、[!DNL Commerce] [product属性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}を使用して条件値にマッピングされる`Condition`のリスト設定に基づいています。 マッピングされたすべての条件に対して、1 ～ 100の分散の割合を定義できます。 例外は収集可能なもので、100を超える割合が適用される場合があります。

![インテリジェントな価格変更ルール — 競合相手の条件付き相違](assets/amazon-competitor-cond-variances.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | オプション： <ul><li>**[!UICONTROL Use all competitor's product conditions]**  — 製品をリストする条件に一致が存在しない場合、このオプションは使用可能な条件と一致します。最初に条件の照合を試み、次に`New`条件から`Used; Acceptable`条件へと進みます。</li><li>**[!UICONTROL Use only matching competitor's product condition]**  — このオプションは、製品の条件と一致します。一致する製品が存在しない場合は、_[!UICONTROL Magento Price Source]_の製品価格が表示されます。</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** — このオプションは、まず製品の条件との照合を試みます。 一致条件が存在しない場合、製品条件と最も低い競合相手の条件に対して差異（割合）が適用されます。</li></ul><br><br>製品属 [!DNL Commerce] [性](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}を使用して条件値にマッピングされる条件のリスト設定に基づいて表示される条件付き分散オプション。マッピングされたすべての条件に対して、1 ～ 100の分散の割合を示すことができます。 例外は収集可能なもので、100を超える割合が適用される場合があります。<br><br>この機能を使用すると、競合他社とは異なる条件の製品を提供する場合に、インテリジェントな価格変更ルールを使用できます。条件付き差異の計算を理解するには、まずすべての差異が基準一致価格から決定されることを理解する必要があります。 |

## 条件付き分散の基準の計算

- Base Match Condition Variance(BMC) =基準一致価格競合相手の条件の差異。 前の例では、BMCは`New`条件の平方偏差です。
- Merchant Condition Variance(MCV) =製品の条件の差異。 前の例では、MCV = `Used; Good`条件の平方偏差です。
- 基準マッチ価格(BMP) = $7.99（上記で説明）

条件付き分散の基準を計算する式は次のとおりです。

![条件付き差異の基準計算式](assets/amazon-cond-variance-calc-1.png)

## 例

条件付き分散の設定は次のとおりです。

![条件付き分散の例](assets/amazon-cond-variances.png)

- BMC = 100（競合相手の条件=新規）
- MCV = 80(商人条件=使用済み；良い)
- BMP = $7.99 （基準一致価格=照合した競合相手の条件の最低価格）

![条件付き分散の基本計算の例](assets/amazon-cond-variance-calc-2.png)

上記の条件付き差異ベースの計算を使用して、条件付き差異ベース= $6.39。この計算は、価格ルールの処理に使用する競合相手の価格ソースです。詳しくは、[価格調整](./price-adjustment.md)を参照してください。
