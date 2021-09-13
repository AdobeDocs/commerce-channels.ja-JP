---
title: 価格ルールの例
description: Amazonリスト用の価格ルールをデザインするのに役立つように、一般的なシナリオに基づいてこれらの例を確認してください。
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 価格ルールの例

## 標準価格ルールの例

### 後続のルールを破棄

後続のルールを破棄する機能は、複数の価格ルールが積み重なり、意図しない追加の割引を提供するのを防ぐ、価格ルール内の優れた機能です。 以降のルールを破棄するには、価格ルールで、[価格ルールの一般設定](./pricing-rule-general-settings.md)の&#x200B;_[!UICONTROL Priority]_セクションで設定された優先度を使用する必要があります。

**[!UICONTROL Discard Subsequent Rules]**&#x200B;を`Yes`に設定した場合、優先度の低い（数値が高い）ルールは対象製品に適用されません。

例えば、次の3つの価格ルールがあるとします。

| 例 | ルール名 | 優先度 | 後続の規則を破棄 |
|----------|----|----|----|
| 1 | 10%オフの販売製品 | 1 | いいえ |
| 2 | 2ドルの販売商品 | 2 | はい |
| 1 | すべての製品の5% | 1 | いいえ |

このシナリオでは、ルール#1と#2が適格な製品に適用されます。 ルール#3は、例#2よりも優先度が低く、**[!UICONTROL Discard Subsequent Rules]**&#x200B;が`Yes`に設定されているので、ルール#2に含まれていない適格な製品にのみ適用されます。 したがって、販売カテゴリに属する適格な製品は、Amazon上場価格から10%の割引と2ドルの割引を受けます。

### 2つの標準価格ルールの適用

| フィールド | 設定 — ルール1 | 設定 — ルール2 |
|----------|----|----|
| [!UICONTROL Rule Name] | ルール —1 | ルール —2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 標準価格ルール | 標準価格ルール |
| [!UICONTROL Price action] | 次の値で減少 | 次の値で減少 |
| [!UICONTROL Apply] | 割合で適用 | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 製品1

価格：45.49ドル

ルール1の適用：$45.49 x (0.9) = $40.94

ルール2の適用：$40.94 - $10.00 = $30.94

ルール1とルール2の後の最終価格は次のように適用されます。30.94ドル

#### 製品2

価格：47.76ドル

ルール1の適用：$47.76 x (0.9) = $42.98

ルール2の適用：$42.98 - $10.00 = $32.98

ルール1とルール2の後の最終価格が適用されます。32.98ドル

## インテリジェントな再価格設定ルールの例

### Buy Box価格と下限価格のソース=価格

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合相手の価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 一致 |

#### 製品1

価格：15ドル

[Amazon](./buy-box-competitor-pricing.md) でBoxpriceを購入：10ドル

[Buy Box](./buy-box-competitor-pricing.md)の価格は元の価格より低いので、商品は元の価格で表示されます。

ルール適用後の最終価格：15ドル

#### 製品2

価格：$5

[Amazon](./buy-box-competitor-pricing.md) でBoxpriceを購入：10ドル

[Buy Box](./buy-box-competitor-pricing.md)の価格は元の価格よりも大きいので、商品は[Buy Box](./buy-box-competitor-pricing.md)価格で表示されます。

ルール適用後の最終価格：10ドル

### Buy Box価格（下限価格=価格、20%価格の下落）

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合相手の価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 次の値で減少 |
| [!UICONTROL Apply] | 割合で適用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 製品1

価格：20ドル

計算された下限価格：16ドル

[Amazon](./buy-box-competitor-pricing.md) でBoxpriceを購入：15ドル

[Buy Box](./buy-box-competitor-pricing.md)の価格は、計算済み[下限価格](./floor-price.md)よりも小さいので、製品は計算済み[下限価格](./floor-price.md)にリストされます。

ルール適用後の最終価格：16ドル

#### 製品2

価格：15ドル

計算済み[下限価格](./floor-price.md):12ドル

[Amazon](./buy-box-competitor-pricing.md) でBoxpriceを購入：15ドル

[Buy Box](./buy-box-competitor-pricing.md)の価格は、計算された[下限価格](./floor-price.md)よりも大きいので、商品は[Buy Box](./buy-box-competitor-pricing.md)価格で表示されます。

ルール適用後の最終価格：15ドル

#### 製品3

価格：17ドル

計算された下限価格：13.60ドル

[Amazon](./buy-box-competitor-pricing.md) でBoxpriceを購入：15ドル

[Buy Box](./buy-box-competitor-pricing.md)の価格は、計算された[下限価格](./floor-price.md)よりも大きいので、商品は[Buy Box](./buy-box-competitor-pricing.md)価格で表示されます。

ルール適用後の最終価格：15ドル

### すべての競合他社の価格で最低価格を実現し、すべての競合他社の製品条件を使用

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL Rule Name] | ルール —1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな価格変更ルール |
| [!UICONTROL Competitor Price Source] | 競合相手の最も低い価格を使用 |
| [!UICONTROL Minimum Positive Feedback] | すべての競合他社の価格 |
| [!UICONTROL Conditional Variance] | 競合他社の製品条件をすべて使用する |
| [!UICONTROL Price Action] | 競合相手の価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 一致 |

| 価格 | 条件 |
|----------|----|
| 17ドル | 新規 |
| 15ドル | 新規 |
| 14ドル | 使用済み非常に良い |
| 13ドル | 使用済み良い |

#### 製品1

価格：10ドル

条件：新規

New条件の競合相手の最も低い価格は$15なので、製品は$15にリストされます。

ルール適用後の最終価格：15ドル

#### 製品2

価格：10ドル

条件：使用済み許容可能

Used条件の[競合相手の価格](./lowest-competitor-pricing.md)は$13なので、製品は$13にリストされます。

ルール適用後の最終価格：13ドル

### 上限価格、通貨換算、VATを組み合わせたインテリジェントな再価格設定ルール

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | 10ドル |
| [!UICONTROL Currency conversion] | 1.25ユーロ：1USD |

[欧州](./optional-ceiling-price.md) (VAT)市場の上限価格：$10 x 1.25 = $12.50

欧州(VAT)市場の[上限価格](./optional-ceiling-price.md)にヒットした場合、VATが計算され、加算されます。

VAT後の最終価格：$12.50 x (1.1) = $13.75

### 複数の価格ルール、上限価格、通貨換算、VATの組み合わせ

#### インテリジェントな価格ルール（前の例のもの）

| フィールド | 設定 |
|----------|----|
| 優先度 | 1 |
| VAT | 10% |
| 上限価格源 | 10ドル |
| 通貨換算 | 1.25ユーロ：1USD |

[欧州](./optional-ceiling-price.md) (VAT)市場の上限価格：$10 x 1.25 = $12.50

VAT後の最終価格：$12.50 x (1.1) = $13.75

#### 標準価格ルール

| フィールド | 設定 |
|----------|-----|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 増分基準 |
| [!UICONTROL Apply] | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 5.00ドル |

[上限価格](./optional-ceiling-price.md)がヒットすると、標準価格ルールがインテリジェント価格ルールの上に適用されます。

標準価格ルール適用後の最終価格：$13.75 + $5.00 = $18.75

### 価格調整

この例では、最も競争力の高い価格を定義します。Amazonの競合他社[の最低価格](./lowest-competitor-pricing.md)を調べ、95%の肯定的なフィードバックと最小フィードバック数が1,000人の商人レビューを得ます。

![価格調整の例](assets/amazon-price-adjustment-example.png)

これらのパラメーターに基づいてこの検索を実行すると、競合価格は$25に戻ります。

ここから、この最低価格に基づいて、3つの異なる[価格ルールアクション](./pricing-rule-actions.md)を選択します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]**  — このオプションは、競合相手の最も低い価格に対して [上場価格を下げます](./lowest-competitor-pricing.md)。</li><li>**[!UICONTROL Increase By]**  — このオプションは、競合相手の最も低い価格に対して [上場価格を上げます](./lowest-competitor-pricing.md)。</li><li>**[!UICONTROL Match Competitor Price]**  — このオプションは、パラメーターに基づいて最も安い価格に一致するようにAmazonの上場価格を変更します。この例では、Amazonの上場価格は$25です。</li></ul> |
| [!UICONTROL Apply] | オプション：割合として適用/固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 数値：適用する割引の割合または固定金額を定義します。 <br>これらの選択は、最低価格を取り、$ 0.01に設定します。 |

### 下限価格

| フィールド | 設定 |
|----------|----|
| [!UICONTROL Floor Price Source] | コスト= 5ドル |
| [!UICONTROL Floor Price Action] | 増分基準 |
| [!UICONTROL Apply] | 割合で適用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[下限](./floor-price.md) 計算=下限価格ソ `$5` ースx床調整額 `5%` = $5.25

インテリジェント価格ルールを適用すると、コストが5ドルの場合に、この特定の製品の上場価格が$5.25より低くなることができます。
