---
title: Amazonセールスチャネル — [!UICONTROL Price Adjustment]
description: 価格調整を設定して、Amazonの競合相手の価格ソースを特定した場合の価格計算を定義します。
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>「価格調整」セクションは、標準およびインテリジェントの再価格設定ルールでは少し異なります。 **[!UICONTROL Match Competitor Price]** は以下でのみ使用できます。 _[!UICONTROL Price Action]_when **[!UICONTROL Rule Type]**が `Intelligent repricing rule`.

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [ルールタイプを選択](./intelligent-repricing-rules.md)
- [競合相手の条件付き相違](./competitor-conditional-variances.md)
- 価格調整
- [下限価格](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

価格調整は、競合相手の価格のソースを特定した場合の価格計算を定義します。

## 価格調整の構成

価格調整を _[!UICONTROL Price Adjustment]_」セクションに入力します。

1. の場合 **[!UICONTROL Price Action]**、オプションを選択します。

   - `Decrease By` - Amazonにリストする前に、定義した価格のソース値を調整して、ルールの価格を下げる場合に選択します。

   - `Increase By` - Amazonにリストする前に、定義した価格ソースの値を調整し、ルールの価格を高くする場合に選択します。

   - `Match Competitor Price` - （インテリジェントな価格変更ルールのみ）Amazonの定価を [最も低い競争相手](./lowest-competitor-pricing.md) 価格。競合相手のフィードバックおよび差異のパラメーターに基づきます。 に設定する場合 `Match Competitor Price`、 _[!UICONTROL Apply]_および_[!UICONTROL Adjustment Amount]_ フィールドが削除されます。

1. の場合 **[!UICONTROL Apply]**、オプションを選択します。

   - `Apply as percentage`  — 定義する **[!UICONTROL Magento Price Source]** が [上場価格](./listing-price.md) パーセンテージで調整されます。

   - `Apply as fixed amount`  — 定義する **[!UICONTROL Magento Price Source]** が [上場価格](./listing-price.md) 一定金額で調整されます。

1. の場合 **[!UICONTROL Adjustment Amount]** （必須）価格調整の数値を入力します。

   - 条件 **[!UICONTROL Apply]** が `Apply as percentage`パーセント値を入力します ( 例：入力 `25` （25%調整）。

   - 条件 **[!UICONTROL Apply]** が `Apply as fixed amount`、固定金額の数値を入力します ( 例：入力 `25` （25 ドルの固定調整）。

![インテリジェントな価格変更ルール — 価格調整](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|---|---|
| [!UICONTROL Price Action] | 価格調整処理を選択します。 オプション：<br>**[!UICONTROL Decrease By]**— 定義する _[!UICONTROL Magento Price Source]_が [上場価格](./listing-price.md) 調整して、Amazonに上場する前に、ルールの価格を下げます。<br>**[!UICONTROL Increase By]**— 定義する_[!UICONTROL Magento Price Source]_ が [上場価格](./listing-price.md) 調整するには、Amazonに上場する前に、ルールの価格を高くします。<br>**[!UICONTROL Match Competitor Price]**- （インテリジェントな価格変更ルールのみ）Amazonの定価を [最も低い競争相手](./lowest-competitor-pricing.md) 価格。競合相手のフィードバックおよび差異のパラメーターに基づきます。 選択すると、 _適用_ および _調整額_ フィールドが削除されます。 |
| [!UICONTROL Apply] | オプション：<br>**[!UICONTROL Apply as percentage]**— 定義する _[!UICONTROL Magento Price Source]_が [上場価格](./listing-price.md) パーセンテージで調整されます。<br>**[!UICONTROL Apply as fixed amount]**— 定義する_[!UICONTROL Magento Price Source]_ が [上場価格](./listing-price.md) 一定金額で調整されます。 |
| [!UICONTROL Adjustment Amount] | 必須。<br>次を選択した場合： `Apply as percentage` 対象 **[!UICONTROL Apply]**&#x200B;パーセント値を入力します ( 例：入力 `25` （25%調整）。<br>次を選択した場合： `Apply as fixed amount` 対象 **[!UICONTROL Apply]**、固定金額の数値を入力します ( 例：入力 `25` （25 ドルの固定調整）。 |
