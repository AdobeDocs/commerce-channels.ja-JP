---
title: '「インテリジェントな価格設定ルール: 競合相手の条件付き差異」'
description: インテリジェントな再価格ルールを作成することにより、製品の競合他社の価格と状態に基づいて、Amazon のリスト価格を決定します。
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール: 競合企業の条件付き差異

インテリジェントな「価格設定」ルールのセクションには、次のものが含まれます。

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

インテリジェントな再価格ルールでは、Amazon の競合企業による価格設定によって、掲載価格が決定されます。 競合企業とは、Amazon に記載されたものと同じ製品が記載されている他の売り手です。

同じ条件の製品がある場合、基準となる対戦価格は、 [ 同じ条件を満たす最も低い競合価格になり ](./lowest-competitor-pricing.md) ます。 お客様の条件に合致する競合製品がない場合、新機能を利用して、新、再作成、使用可能な条件に基づいて継続的にその他の競合条件が表示されます。 条件が検出されると、その条件内の基数が最も低い価格になります。

条件と基本照合価格が記載された製品があり、 `Used; Good` 競合企業が同じ条件に基づいて同じ製品を使用している場合は、競合他社価格が使用されます。 競合企業が同じ条件で存在しない場合は、次の条件によって競合企業があるかどうかがシステムによって確認され `New` ます。 このような条件に一致する競合企業が見つかった場合は、最低価格が使用されます。

## 競合企業の条件付き差異の設定

セクションで、条件の違いを定義し _[!UICONTROL Competitor Conditional Variances]_ます。

**[!UICONTROL Conditional Variance]**&#x200B;で、次のいずれかのオプションを選択します。

- `Use all competitor's product conditions` -(デフォルト) 製品を使用可能な条件と比較する場合に選択します (表示されている条件に一致するものが見つからない場合)。

- `Use Only Matching Competitor's Product Condition` -競合製品と同一の条件でのみ比較する場合に選択します。 一致する製品がない場合は、 __ 出展価格で定義されている Magento 価格ソースで価格設定され [ ](./listing-price.md) ます。

- `Apply Variance (if competitor's product condition differs)` -「選択」を選択すると、一致した製品条件と比較が試みられます。 一致条件が存在しない場合は、製品条件および競合企業の最小条件を基準として一時的認可が適用されます。

   この機能を選択すると _[!UICONTROL Apply Variance]_、各 Amazon 条件に対して追加の分散フィールドが表示されます。 この機能を使用すると、競合企業とは異なる条件の製品を提供する場合に、インテリジェントな再価格ルールを使用できます。 条件付き分散の背後にある計算を理解するには、すべての可変性が基本の適合価格から決定される必要があるということをまず理解する必要があります。

   表示される条件付き一時的に関するオプションは、 `Condition` product 属性を使用して条件値にマップされるリスト設定に基づいてい [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) ます {target = &quot;_blank&quot;}。 マップされているすべての条件について、分散率1-100 を定義することができます。 ただし、collectibles では、100より大きな値が適用されている場合があります。

![インテリジェントな再価格設定ルール-競合企業の条件付き差異](assets/amazon-competitor-cond-variances.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Competitor Conditional Variances] | オプション： <ul><li>**[!UICONTROL Use all competitor's product conditions]** -製品の一覧を表示している条件に一致するものがない場合は、使用可能な条件に対してこのオプションが適用されます。 最初に、条件に一致することを試み、その後、 `New` 条件に対してに作用し `Used; Acceptable` ます。</li><li>**[!UICONTROL Use only matching competitor's product condition]** -このオプションは製品の条件と一致します。 一致するものがない場合は、によってに製品価格が指定され _[!UICONTROL Magento Price Source]_ます。</li><li>> **[!UICONTROL Apply variance (if competitor's product condition differs)]** -このオプションを使用すると、最初に製品の条件に一致することが試みられます。 条件が一致していない場合は、製品条件と競合している最低条件を基準として、分散率 (%) が適用されます。</li></ul><br><br>Product 属性を使用して条件値にマップされた条件について、条件の表示設定に基づいて表示される条件付き変性のオプション [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) {target = &quot;_blank&quot;}。 割り当てられているすべての条件については、1-100 の分散率を表すことができます。 ただし、collectibles では、100より大きな値が適用されている場合があります。<br><br>この機能を使用すると、競合企業とは異なる条件の製品を提供する場合に、インテリジェントな再価格ルールを使用できます。 条件付き分散の背後にある計算を理解するには、すべての可変性が基本の適合価格から決定される必要があるということをまず理解する必要があります。 |

## 条件分散の基準を計算します。

- ベース対戦条件の分散 (BMC) = 基準となる価格の競合企業の条件の分散を指定します。 前述の例では、BMC は条件の分散を示してい `New` ます。
- マーチャント条件分散 (MCV) = 製品の状態の分散 前述の例を使用して、MCV = 条件の分散を示し `Used; Good` ます。
- ベースとなる価格 (BMP) = $7.99 (上記を説明)

条件付き変性の基準の計算には、次のような数式が使用されます。

![条件付き差異基準計算式](assets/amazon-cond-variance-calc-1.png)

## 一

条件付き分散設定は、次のとおりです。

![条件付き変性の設定例](assets/amazon-cond-variances.png)

- BMC = 100 (競合企業の状態 = 新規)
- MCV = 80 (マーチャント condition = 使用されています。役立ち
- BMP = $7.99 (基数は、条件に一致した競合条件の最低価格)

![条件付き変性の基本計算の例](assets/amazon-cond-variance-calc-2.png)

上記の条件分散の基本計算を使用すると、条件分散の基準 = $6.39 になります。この計算は、価格ルールの操作に使用される、価格調整について詳しく説明されている、競合価格ソースです [ ](./price-adjustment.md) 。
