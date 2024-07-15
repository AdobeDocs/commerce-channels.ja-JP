---
title: Amazon販売チャネル – 価格ルールの例
description: Amazon リストの価格ルールの設計に役立つように、一般的なシナリオに基づいてこれらの例を確認します。
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 1%

---

# 価格ルールの例

## 標準価格ルールの例

### 後続のルールを破棄

後続のルールを破棄する機能は、複数の価格ルールが積み重なるのを防ぎ、意図しない追加の割引を提供する価格ルール内の優れた機能です。 後続のルールを破棄するには、「価格設定ルールの一般設定 [ の _[!UICONTROL Priority]_のセクションで設定した優先度を使用する必要があ ](./pricing-rule-general-settings.md) ます。

**[!UICONTROL Discard Subsequent Rules]** を `Yes` に設定した場合、優先度が低い（数字が大きい）ルールは適格な製品には適用されません。

例えば、次の 3 つの価格ルールがあるとします。

| 例 | ルール名 | 優先度 | 後続のルールを破棄 |
|---------|-----------------------|----------|-------------------------|
| 1 | セール品 10% オフ | 1 | 不可 |
| 2 | 2 ドル割引の商品 | 2 | はい |
| 3 | 全製品の 5% 割引 | 3 | 不可 |

このシナリオでは、ルール#1 と#2 が適格な製品に適用されます。 ルール #3 は、例#2 よりも優先度が低く、**[!UICONTROL Discard Subsequent Rules]** が `Yes` に設定されているので、ルール #2 内に含まれていない適格な製品にのみ適用されます。 そのため、Amazonの対象商品には 10% の割引と 2 ドルの定価が適用されます。

### 2 つの標準価格ルールの適用

| フィールド | 設定 – ルール 1 | 設定 – ルール 2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | ルール 1 | 規則 2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | 標準価格ルール | 標準価格ルール |
| [!UICONTROL Price action] | 次の値で減少 | 次の値で減少 |
| [!UICONTROL Apply] | パーセンテージとして適用 | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### 製品 1

価格：45.49 ドル

ルール 1 が適用されました：45.49 x （0.9） = 40.94 ドル

ルール 2 が適用されました：40.94～10.00 ドル=30.94 ドル

ルール 1 とルール 2 の適用後の最終価格：$30.94

#### 製品 2

価格：47.76 ドル

ルール 1 が適用されました：47.76 x （0.9） = 42.98 ドル

ルール 2 が適用されました：42.98～10.00 ドル=32.98 ドル

ルール 1 とルール 2 の後の最終価格：$32.98

## インテリジェントな再価格設定ルールの例

### Buy Box価格と最低価格Source =価格

| フィールド | 設定 |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | ルール 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格設定ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合他社価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 次に一致 |

#### 製品 1

価格：15 ドル

[Buy Box](./buy-box-competitor-pricing.md)Amazonからの価格：10 ドル

[Buy Box](./buy-box-competitor-pricing.md) の価格が元の価格より低いため、商品は元の価格で表示されます。

ルール適用後の最終価格：$15

#### 製品 2

価格：5 ドル

[Buy Box](./buy-box-competitor-pricing.md)Amazonからの価格：10 ドル

[Buy Box](./buy-box-competitor-pricing.md) の価格が元の価格よりも高いため、商品は [Buy Box](./buy-box-competitor-pricing.md) の価格で表示されます。

ルール適用後の最終価格：$10

### Buy Box価格と最低価格Source =価格と 20% の価格下落

| フィールド | 設定 |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | ルール 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格設定ルール |
| [!UICONTROL Competitor Price Source] | 「Buy Box」価格を使用 |
| [!UICONTROL Price Action] | 競合他社価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 次の値で減少 |
| [!UICONTROL Apply] | 割合として適用 |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### 製品 1

価格：20 ドル

算出された最低価格：$16

[Buy Box](./buy-box-competitor-pricing.md)Amazonからの価格：15 ドル

[Buy Box](./buy-box-competitor-pricing.md) の価格が算出された [Floor Price](./floor-price.md) よりも低いため、商品は算出された [Floor Price](./floor-price.md) に一覧表示されます。

ルール適用後の最終価格：$16

#### 製品 2

価格：15 ドル

算出 [ 最低価格 ](./floor-price.md):$12

[Buy Box](./buy-box-competitor-pricing.md)Amazonからの価格：15 ドル

[Buy Box](./buy-box-competitor-pricing.md) の価格が算出された [ フロア価格 ](./floor-price.md) よりも高いため、商品は [Buy Box](./buy-box-competitor-pricing.md) の価格で表示されます。

ルール適用後の最終価格：$15

#### 製品 3

価格：17 ドル

算出された最低価格：$13.60

[Buy Box](./buy-box-competitor-pricing.md)Amazonからの価格：15 ドル

[Buy Box](./buy-box-competitor-pricing.md) の価格が算出された [ フロア価格 ](./floor-price.md) よりも高いため、商品は [Buy Box](./buy-box-competitor-pricing.md) の価格で表示されます。

ルール適用後の最終価格：$15

### すべての競合企業の価格で最低価格を設定し、すべての競合企業の製品条件を使用する

| フィールド | 設定 |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | ルール 1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | インテリジェントな再価格設定ルール |
| [!UICONTROL Competitor Price Source] | 競合他社最低価格を使用 |
| [!UICONTROL Minimum Positive Feedback] | すべての競合他社価格 |
| [!UICONTROL Conditional Variance] | すべての競合製品の条件を使用する |
| [!UICONTROL Price Action] | 競合他社価格に一致 |
| [!UICONTROL Floor Price Source] | 価格 |
| [!UICONTROL Floor Price Action] | 次に一致 |

| 価格 | 条件 |
|-------|-----------------|
| $17 | 新規 |
| $15 | 新規 |
| $14 | 使用済み；非常に良好 |
| $13 | 使用済み；良好 |

#### 製品 1

価格：10 ドル

条件：新規

新規条件の競合他社価格が最低 15 ドルであるため、製品は 15 ドルでリストされます。

ルール適用後の最終価格：$15

#### 製品 2

価格：10 ドル

条件：使用済み、許容可能

使用済み条件の [ 競合他社価格の最低価格 ](./lowest-competitor-pricing.md) は 13 ドルなので、製品は 13 ドルでリストされます。

ルール適用後の最終価格：$13

### 天井価格、通貨換算、VAT を組み合わせたインテリジェントな再価格設定ルール

| フィールド | 設定 |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1.25 ユーロ：1USD |

[ ヨーロッパ（VAT）市場の上限価格 ](./optional-ceiling-price.md)10 ドル×1.25 ドル=12.50 ドル

ヨーロッパ（VAT](./optional-ceiling-price.md) 市場の [ 天井価格）がヒットすると、VAT が計算され、追加されます。

VAT 後の最終価格：$12.50 x （1.1） = $13.75

### 複数の価格設定ルール、天井価格、通貨換算および VAT の組合せ

#### インテリジェントな価格設定ルール（前述の例から）

| フィールド | 設定 |
|----------------------|---------------|
| 優先度 | 1 |
| VAT | 10% |
| 天井価格ソース | $10 |
| 通貨換算 | 1.25 ユーロ：1USD |

[ ヨーロッパ（VAT）市場の上限価格 ](./optional-ceiling-price.md)10 ドル×1.25 ドル=12.50 ドル

VAT 後の最終価格：$12.50 x （1.1） = $13.75

#### 標準価格ルール

| フィールド | 設定 |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | 増分 |
| [!UICONTROL Apply] | 固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 500 ドル |

[ 天井価格 ](./optional-ceiling-price.md) に達すると、インテリジェント価格ルールの上に標準価格ルールが適用されます。

標準価格設定ルール適用後の最終価格：$13.75 + $5.00 = $18.75

### 価格調整

この例では、最も競争力のある価格は、95% の肯定的なフィードバックと最小のフィードバック数 1,000 件のマーチャントレビューを備えたAmazon[ 競合他社の最低価格 ](./lowest-competitor-pricing.md) を調べることで定義されています。

![ 価格調整の例 ](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

これらのパラメーターに基づいてこの検索を実行すると、競争力のある価格は 25 ドルに戻ります。

ここから、この最低価格に基づいて 3 つの異なる [ 価格ルールアクション ](./pricing-rule-actions.md) 選択肢があります。

| フィールド | 説明 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]** – このオプションは、[ 競合他社価格の最低価格 ](./lowest-competitor-pricing.md) に対して価格を下げます。</li><li>**[!UICONTROL Increase By]** – このオプションは、[ 競合他社価格の最低価格 ](./lowest-competitor-pricing.md) に対して上場価格を増加させます。</li><li>**[!UICONTROL Match Competitor Price]** – このオプションは、パラメーターに基づいて最低価格に一致するようにAmazonの上場価格を変更します。 この例では、Amazonの上場価格は 25 ドルです。</li></ul> |
| [!UICONTROL Apply] | オプション：パーセンテージとして適用/固定金額として適用 |
| [!UICONTROL Adjustment Amount] | 適用される割引の割合または固定金額を定義する数値。 <br> これらの選択により、最低価格を選択し、0.01 ドル安に設定することになります。 |

### フロアプライス

| フィールド | 設定 |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | コスト = $5 |
| [!UICONTROL Floor Price Action] | 増分 |
| [!UICONTROL Apply] | パーセンテージとして適用 |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[ 最低価格 ](./floor-price.md) 算定=最低価格Source`$5` x 最低調整額 `5%` = $5.25

インテリジェント価格ルールが適用されると、コストが 5 ドルの場合、この特定の製品の上場価格が 5.25 ドルより低くなることが許可されます。
