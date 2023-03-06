---
title: 価格ルールの例
description: Amazonの一覧用の価格ルールを設計する際に役立つように、一般的なシナリオに基づいてこれらの例を確認してください。
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 価格ルールの例

## 標準価格ルールの例

### 後続のルールを破棄

後続のルールを破棄する機能は、複数の価格ルールを積み重ねて意図しない追加の割引を提供するのを防ぐ、価格ルール内の優れた機能です。 後続のルールを破棄するには、価格ルールで、 _[!UICONTROL Priority]_セクション [価格ルールの一般設定](./pricing-rule-general-settings.md).

If **[!UICONTROL Discard Subsequent Rules]** が `Yes`の場合、優先度が低い（数字が高い）ルールは対象の製品には適用されません。

例えば、次の 3 つの価格ルールがあるとします。

| 例 | ルール名 | 優先度 | 後続のルールを破棄 |
|----------|----|----|----|
| 1 | 10%オフセール商品 | 1 | いいえ |
| 2 | $2 の販売製品 | 2 | はい |
| 3 | すべての製品の 5%オフ | 3 | いいえ |

このシナリオでは、ルール#1とルール#2が適格な製品に適用されます。 ルール#3は、例と同様に優先度が低いので、ルール内に含まれていない適格な製品に対してのみ適用さ#2ます。 **[!UICONTROL Discard Subsequent Rules]** が `Yes`. したがって、販売カテゴリの対象製品には、Amazon上場価格から 10%の割引と 2 ドルの割引が適用されます。

### 2 つの標準価格ルールの適用

| フィールド | 設定 — ルール 1 | 設定 — ルール 2 |
|----------|----|----|
| [!UICONTROL Rule Name] | ルール —1 | ルール —2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 標準価格ルール | 標準価格ルール |
| [!UICONTROL Price action] | 減少基準 | 減少基準 |
| [!UICONTROL Apply] | 割合で適用 | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 製品 1

価格：$45.49

適用されるルール 1:$45.49 x (0.9) = $40.94

適用されるルール 2:$40.94 - $10.00 = $30.94

ルール 1 とルール 2 の後の最終価格は、次のように適用されます。30.94 ドル

#### 製品 2

価格：$47.76

適用されるルール 1:$47.76 x (0.9) = $42.98

適用されるルール 2:$42.98 - $10.00 = $32.98

ルール 1 とルール 2 の後の最終価格が適用されます。$32.98

## インテリジェントな価格変更ルールの例

### Buy Box価格（下限価格のソース=価格）

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合相手の価格と一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 一致 |

#### 製品 1

価格：$15

[Buy Box](./buy-box-competitor-pricing.md) Amazonからの価格：$10

これは、 [Buy Box](./buy-box-competitor-pricing.md) 価格が元の価格より低い場合は、商品は元の価格で表示されます。

ルール適用後の最終価格：$15

#### 製品 2

価格：$5

[Buy Box](./buy-box-competitor-pricing.md) Amazonからの価格：$10

これは、 [Buy Box](./buy-box-competitor-pricing.md) 価格が元の価格より大きい場合、製品は [Buy Box](./buy-box-competitor-pricing.md) 価格。

ルール適用後の最終価格：$10

### Buy Box価格（下限価格=価格、20%の価格減少）

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合相手の価格と一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 減少基準 |
| [!UICONTROL Apply] | パーセンテージで適用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 製品 1

価格：$20

計算された下限価格：$16

[Buy Box](./buy-box-competitor-pricing.md) Amazonからの価格：$15

これは、 [Buy Box](./buy-box-competitor-pricing.md) 価格が計算値より小さい [下限価格](./floor-price.md)」と入力すると、製品が計算指標にリストされます。 [下限価格](./floor-price.md).

ルール適用後の最終価格：$16

#### 製品 2

価格：$15

計算済み [下限価格](./floor-price.md):$12

[Buy Box](./buy-box-competitor-pricing.md) Amazonからの価格：$15

これは、 [Buy Box](./buy-box-competitor-pricing.md) 価格が計算済みの価格より大きい [下限価格](./floor-price.md)に分類する場合、製品は [Buy Box](./buy-box-competitor-pricing.md) 価格。

ルール適用後の最終価格：$15

#### Product 3

価格：$17

計算された下限価格：13.60 ドル

[Buy Box](./buy-box-competitor-pricing.md) Amazonからの価格：$15

これは、 [Buy Box](./buy-box-competitor-pricing.md) 価格が計算済みの価格より大きい [下限価格](./floor-price.md)に分類する場合、製品は [Buy Box](./buy-box-competitor-pricing.md) 価格。

ルール適用後の最終価格：$15

### すべての競合相手の価格で最低価格で、すべての競合相手の製品条件を使用

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 競合相手の最も低い価格を使用 |
| [!UICONTROL Minimum Positive Feedback] | すべての競合相手の価格 |
| [!UICONTROL Conditional Variance] | すべての競合他社の製品条件を使用 |
| [!UICONTROL Price Action] | 競合相手の価格と一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 一致 |

| 価格 | 条件 |
|----------|----|
| $17 | 新規 |
| $15 | 新規 |
| $14 | 使用済み；非常に良い |
| $13 | 使用済み；良い |

#### 製品 1

価格：$10

条件：新規

New 条件の競合相手の最も低い価格は$15 なので、製品は$15 にリストされます。

ルール適用後の最終価格：$15

#### 製品 2

価格：$10

条件：使用済み；許容可能

これは、 [最低競争価格](./lowest-competitor-pricing.md) 「使用済み」条件が$13 の場合、製品は$13 にリストされます。

ルール適用後の最終価格：$13

### 上限価格、通貨換算、VAT を組み合わせたインテリジェントな再価格設定ルール

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1.25 ユーロ：1USD |

[上限価格](./optional-ceiling-price.md) 欧州 (VAT) 市場では、$10 x 1.25 = $12.50

次の場合に [上限価格](./optional-ceiling-price.md) 欧州 (VAT) 市場がヒットした場合、VAT が計算されて追加されます。

VAT 後の最終価格：$12.50 x (1.1) = $13.75

### 複数の価格ルール、上限価格、通貨換算、VAT の組み合わせ

#### インテリジェントな価格ルール（前の例から）

| フィールド | 設定 |
|----------|----|
| 優先度 | 1 |
| VAT | 10% |
| 上限価格のソース | $10 |
| 通貨換算 | 1.25 ユーロ：1USD |

[上限価格](./optional-ceiling-price.md) 欧州 (VAT) 市場では、$10 x 1.25 = $12.50

VAT 後の最終価格：$12.50 x (1.1) = $13.75

#### 標準価格ルール

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 次の値で増加 |
| [!UICONTROL Apply] | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | $5.00 |

次の場合に [上限価格](./optional-ceiling-price.md) がヒットした場合、標準の価格ルールがインテリジェント価格ルールの上に適用されます。

標準価格ルールの適用後の最終価格：$13.75 + $5.00 = $18.75

### 価格調整

この例では、最も競争力のある価格は、Amazon [競争相手の最低価格](./lowest-competitor-pricing.md) 95%の肯定的なフィードバックと、1,000 の商人レビューの最小フィードバック数を含む。

![価格調整の例](assets/amazon-price-adjustment-example.png)

これらのパラメーターに基づいてこの検索を実行すると、競合価格は$25 に戻ります。

ここから、3 つの異なる点があります [価格ルールアクション](./pricing-rule-actions.md) この最低価格に基づく選択肢

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]**  — このオプションを選択すると、 [最低競争価格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]**  — このオプションは、 [最低競争価格](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]**  — このオプションは、パラメーターに基づいて最も安い価格に一致するようにAmazonの定価を変更します。 この例では、Amazonの上場価格は$25 です。</li></ul> |
| [!UICONTROL Apply] | オプション：割合で適用/固定金額で適用 |
| [!UICONTROL Adjustment Amount] | 数値：適用する割引の割合または固定金額を定義します。 <br>これらの選択により、最低価格を設定し、0.01 ドル未満に設定することになります。 |

### 下限価格

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Floor Price Source] | コスト= $5 |
| [!UICONTROL Floor Price Action] | 次の値で増加 |
| [!UICONTROL Apply] | 割合で適用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[下限価格](./floor-price.md) 計算=下限価格のソース `$5` x 床調整量 `5%` = 5.25 ドル

インテリジェント価格ルールを適用すると、コストが 5 ドルの場合に、この特定の製品の上場価格を$5.25 より低くすることができます。
