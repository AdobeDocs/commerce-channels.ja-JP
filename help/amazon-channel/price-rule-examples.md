---
title: 価格ルールの例
description: Amazon リストに使用する価格設定ルールを作成するには、一般的なシナリオに基づいて次の例を参照してください。
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 2%

---

# 価格ルールの例

## 標準価格ルールの例

### 後続のルールを破棄

後続のルールを破棄する機能は、価格設定ルール内に優れた機能を提供します。これにより、複数の価格ルールをスタックから除外し、意図しない追加割引を提供します。 後続のルールを破棄するには、価格設定ルールで、 _[!UICONTROL Priority]_「価格ルール」の「一般設定」セクションに設定されている優先順位を使用する必要があり [ ](./pricing-rule-general-settings.md) ます。

**[!UICONTROL Discard Subsequent Rules]**&#x200B;がに設定されている場合は `Yes` 、優先度が低い (数字が大きい) ルールは対象の製品に適用されません。

例えば、次のような3つの価格設定ルールがあるとします。

| 一 | ルール名 | 事項 | 後続のルールを破棄 |
|----------|----|----|----|
| raid-1 | 売上製品を10% オフにする | raid-1 | 違います |
| pplx-2 | $2 オフ販売製品 | pplx-2 | うん |
| 3-d | すべての製品を5% オフにする | 3-d | 違います |

このシナリオでは、ルール #1 および #2 対象製品に適用されます。 ルール #3 は、ルール #2 に含まれていない適格な製品にのみ適用されます。これは #2 よりも優先度が低く、「」 **[!UICONTROL Discard Subsequent Rules]** に設定されているためです `Yes` 。 そのため、「販売」カテゴリーの適格製品には、Amazon のリスト価格の10% 割引と $2 が適用されます。

### 2つの標準価格ルールの適用

| 名 | 設定-ルール1 | 設定-ルール2 |
|----------|----|----|
| [!UICONTROL Rule Name] | ルール-1 | ルール-2 |
| [!UICONTROL Priority] | raid-1 | pplx-2 |
| [!UICONTROL Rule Type] | 標準価格ルール | 標準価格ルール |
| [!UICONTROL Price action] | 減少 | 減少 |
| [!UICONTROL Apply] | 比率として適用 | 固定サイズとして適用 |
| [!UICONTROL Adjustment Amount] | 回 | 回 |

#### 製品1

価格: $45.49

ルール1が適用されている場合: $45.49 x (0.9) = $40.94

ルール2が適用されている場合: $40.94-$10.00 = $30.94

ルール1の後の最終価格とルール2が適用されます $30.94。

#### 製品2

価格: $47.76

ルール1が適用されている場合: $47.76 x (0.9) = $42.98

ルール2が適用されている場合: $42.98-$10.00 = $32.98

ルール1の後の最終価格とルール2が適用されます $32.98。

## インテリジェントな価格設定ルールの例

### 住宅価格ソースを使用してボックス価格を購入する = 価格

| 名 | , |
|----------|----|
| [!UICONTROL Rule Name] | ルール-1 |
| [!UICONTROL Priority] | raid-1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格ルール |
| [!UICONTROL Competitor Price Source] | 「購入ボックス」価格の使用 |
| [!UICONTROL Price Action] | 競合他社価格に合わせる |
| [!UICONTROL Floor Price Source] | 定価 |
| [!UICONTROL Floor Price Action] | Match |

#### 製品1

価格: $15

[](./buy-box-competitor-pricing.md)Amazon からの購入ボックス価格: $10

「 [ 購入」ボックスの ](./buy-box-competitor-pricing.md) 価格が元の価格より少ないため、製品は元の価格で表示されます。

ルールが適用された後の最終的な価格: $15

#### 製品2

価格: $5

[](./buy-box-competitor-pricing.md)Amazon からの購入ボックス価格: $10

[購入ボックス ](./buy-box-competitor-pricing.md) 価格が元の価格より大きいので、製品が購入ボックス価格で表示され [ ](./buy-box-competitor-pricing.md) ます。

ルールが適用された後の最終的な価格: $10

### 住宅価格の購入時に使用するボックス価格、価格、20% 減分

| 名 | , |
|----------|----|
| [!UICONTROL Rule Name] | ルール-1 |
| [!UICONTROL Priority] | raid-1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格ルール |
| [!UICONTROL Competitor Price Source] | 「購入ボックス」価格の使用 |
| [!UICONTROL Price Action] | 競合他社価格に合わせる |
| [!UICONTROL Floor Price Source] | 定価 |
| [!UICONTROL Floor Price Action] | 減少 |
| [!UICONTROL Apply] | 比率として適用 |
| [!UICONTROL Floor Adjustment Amount] | 約 |

#### 製品1

価格: $20

計算されたフロア価格: $16

[](./buy-box-competitor-pricing.md)Amazon からの購入ボックス価格: $15

△ [ 購入ボックス ](./buy-box-competitor-pricing.md) 価格が計算されたフロア価格より少ないので、製品は、計算された [ ](./floor-price.md) フロア価格で一覧表示され [ ](./floor-price.md) ます。

ルールが適用された後の最終的な価格: $16

#### 製品2

価格: $15

計算された [ フロア価格 ](./floor-price.md) : $12

[](./buy-box-competitor-pricing.md)Amazon からの購入ボックス価格: $15

「 [ 購入」ボックス ](./buy-box-competitor-pricing.md) 価格が計算されたフロア価格より大きいので、 [ ](./floor-price.md) 製品が購入ボックス価格で一覧表示され [ ](./buy-box-competitor-pricing.md) ます。

ルールが適用された後の最終的な価格: $15

#### 製品3

価格: $17

計算されたフロア価格: $13.60

[](./buy-box-competitor-pricing.md)Amazon からの購入ボックス価格: $15

「 [ 購入」ボックス ](./buy-box-competitor-pricing.md) 価格が計算されたフロア価格より大きいので、 [ ](./floor-price.md) 製品が購入ボックス価格で一覧表示され [ ](./buy-box-competitor-pricing.md) ます。

ルールが適用された後の最終的な価格: $15

### すべての競合企業の価格を使用して低価格で、すべての競合企業の製品条件を使用

| 名 | , |
|----------|-----|
| [!UICONTROL Rule Name] | ルール-1 |
| [!UICONTROL Priority] | raid-1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格ルール |
| [!UICONTROL Competitor Price Source] | 競合企業の最下位価格の使用 |
| [!UICONTROL Minimum Positive Feedback] | すべての競合企業価格 |
| [!UICONTROL Conditional Variance] | すべての競合企業の製品条件の使用 |
| [!UICONTROL Price Action] | 競合他社価格に合わせる |
| [!UICONTROL Floor Price Source] | 定価 |
| [!UICONTROL Floor Price Action] | Match |

| 定価 | 条件 |
|----------|----|
| $17 | 新機能 |
| $15 | 新機能 |
| $14 | 使え非常にいいです |
| $13 | 使えよし |

#### 製品1

価格: $10

条件: 新規作成

この新しい条件の対象となる最も低い競合価格は $15 $15 になります。

ルールが適用された後の最終的な価格: $15

#### 製品2

価格: $10

Condition: 使用されます。普通

使用されている [ 条件の最低価格の競合企業価格が $13 のため、 ](./lowest-competitor-pricing.md) 製品が $13 に一覧表示されます。

ルールが適用された後の最終的な価格: $13

### 天井価格、為替換算、VAT を組み合わせたインテリジェントな再価格ルール

| 名 | , |
|----------|-----|
| [!UICONTROL VAT] | 回 |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1.25 ユーロ: 1 USD |

[](./optional-ceiling-price.md)欧州 (VAT) 市場における天井価格: $10 x 1.25 = $12.50

[欧州 (vat) 市場の天井価格に達したときに ](./optional-ceiling-price.md) 、vat が計算され加算されます。

VAT の後の最終的な価格: $12.50 x (1.1) = $13.75

### 複数の価格設定ルール、天井価格、為替換算、VAT を組み合わせる

#### インテリジェントな価格設定ルール (前の例)

| 名 | , |
|----------|----|
| 事項 | raid-1 |
| VAT | 回 |
| 天井価格ソース | $10 |
| 為替換算 | 1.25 ユーロ: 1 USD |

[](./optional-ceiling-price.md)欧州 (VAT) 市場における天井価格: $10 x 1.25 = $12.50

VAT の後の最終的な価格: $12.50 x (1.1) = $13.75

#### 標準価格設定ルール

| 名 | , |
|----------|-----|
| [!UICONTROL Priority] | pplx-2 |
| [!UICONTROL Price Action] | 増加率 |
| [!UICONTROL Apply] | 固定サイズとして適用 |
| [!UICONTROL Adjustment Amount] | $5.00 |

「天井価格」に達したときに、標準価格設定 [ ](./optional-ceiling-price.md) ルールがインテリジェント価格設定ルールの上に適用されます。

標準価格設定ルールが適用された後の最終価格: $13.75 + $5.00 = $18.75

### 価格調整

この例では、Amazon の競合企業にとって最も高い価格設定を定義しています。これは、Amazon の [ 競合相手の最低価格を ](./lowest-competitor-pricing.md) 95%、ポジティブフィードバックを%、そして最低限のフィードバック数を1000商社に調べることによって定義されます。

![価格調整の例](assets/amazon-price-adjustment-example.png)

これらのパラメーターに基づいてこの検索を実行した後、競争価格が $25 に戻ります。

ここでは、 [ ](./pricing-rule-actions.md) この最低価格に基づいて3つの異なる価格ルールアクションが選択されています。

| 名 | つい |
|--- |--- |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]** –このオプションを使用すると、競合企業の最低価格を基準として定価の価格が減少 [ ](./lowest-competitor-pricing.md) します。</li><li>**[!UICONTROL Increase By]** –このオプションを使用すると、競合企業の最低価格を基準として表示価格が向上 [ ](./lowest-competitor-pricing.md) します。</li><li>**[!UICONTROL Match Competitor Price]** –このオプションを使用すると、Amazon の一覧価格が、パラメーターに基づいて最低価格に一致するように変更されます。 この例では、Amazon のリスト価格は $25 になります。</li></ul> |
| [!UICONTROL Apply] | オプション: 割合または固定量として適用 |
| [!UICONTROL Adjustment Amount] | 適用される割引の比率または固定量を指定する数値。 <br>このオプションを選択すると、最低価格である $0.01 に設定されます。 |

### フロア価格

| 名 | , |
|----------|----|
| [!UICONTROL Floor Price Source] | Cost = $5 |
| [!UICONTROL Floor Price Action] | 増加率 |
| [!UICONTROL Apply] | 比率として適用 |
| [!UICONTROL Floor Adjustment Amount] | . |

[「フロア価格 ](./floor-price.md) 計算」 = 「フロア価格ソース `$5` x フロア補正量 `5%` = $5.25

インテリジェントな価格設定が適用された場合、コストが $5 の場合、この特定の製品については、リスト価格が $5.25 より小さくなることがあります。
