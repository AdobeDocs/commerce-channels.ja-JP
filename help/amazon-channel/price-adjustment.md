---
title: 価格調整
description: 価格調整を設定して、Amazonの競合相手の価格ソースを特定した場合の価格計算を定義します。
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 価格調整

>[!NOTE]
>
>「価格調整」セクションは、標準およびインテリジェントな再価格設定ルールでは少し異なります。 **[!UICONTROL Match Competitor Price]** は、がに設定されている場合 _[!UICONTROL Price Action]_にの&#x200B;**[!UICONTROL Rule Type]**み使用できま `Intelligent repricing rule`す。

インテリジェントな価格変更ルールのセクションは次のとおりです。

- [ルールタイプの選択](./intelligent-repricing-rules.md)
- [競合相手の条件の相違](./competitor-conditional-variances.md)
- 価格調整
- [下限価格](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

価格調整は、競合相手の価格ソースを特定した場合の価格計算を定義します。

## 価格調整の設定

_[!UICONTROL Price Adjustment]_セクションで価格調整を定義します。

1. **[!UICONTROL Price Action]**&#x200B;の場合は、次のオプションを選択します。

   - `Decrease By` - Amazonにリストする前に、定義した価格のソース値を調整して、ルールの価格を下げるタイミングを選択します。

   - `Increase By` - Amazonにリストする前に、定義した価格のソース値を調整し、ルールの価格を高くするタイミングを選択します。

   - `Match Competitor Price` - （インテリジェントな再価格設定ルールのみ）競合相手のフィードバックと平方偏差のパラメーターに基づいて、最も低い競合価格に合わせてAmazonの定価を変更する場合に選択しま [](./lowest-competitor-pricing.md) す。`Match Competitor Price`に設定すると、_[!UICONTROL Apply]_フィールドと_[!UICONTROL Adjustment Amount]_&#x200B;フィールドは削除されます。

1. **[!UICONTROL Apply]**&#x200B;の場合は、次のオプションを選択します。

   - `Apply as percentage` - 「リスト価格」で定義した値をパーセ **[!UICONTROL Magento Price Source]** ントで調整 [す](./listing-price.md) る場合に選択します。

   - `Apply as fixed amount`  — 定義した定義済みの価格を一 **[!UICONTROL Magento Price Source]** 定の金額 [で](./listing-price.md) 調整する場合に選択します。

1. **[!UICONTROL Adjustment Amount]**（必須）に、価格調整の数値を入力します。

   - **[!UICONTROL Apply]**&#x200B;を`Apply as percentage`に設定した場合は、パーセント値を入力します(例：`25`と入力し、25%の調整を行います)。

   - **[!UICONTROL Apply]**&#x200B;を`Apply as fixed amount`に設定した場合は、固定金額の数値を入力します(例：$25の固定調整に対して`25`と入力します。

![インテリジェントな再価格設定ルール — 価格調整](assets/amazon-price-adjustment.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Price Action] | 価格調整処理を選択します。 オプション：<br>**[!UICONTROL Decrease By]**- [Listing Price](./listing-price.md)で定義した&#x200B;_[!UICONTROL Magento Price Source]_を調整し、ルールの価格を下げてからAmazonにリストする場合に選択します。<br>**[!UICONTROL Increase By]**- Amazonにリストする前に、リスト価格で定_[!UICONTROL Magento Price Source]_ 義した定義を調整 [し](./listing-price.md) て、ルールの価格を上げるタイミングを選択します。<br>**[!UICONTROL Match Competitor Price]**- （インテリジェントな再価格設定ルールのみ）競合相手のフィードバックと平方偏差のパラメーターに基づいて、最も低い競合価格に合わせてAmazonの定価を変更する場合に選択しま [](./lowest-competitor-pricing.md) す。選択すると、「_適用_」フィールドと「_調整額_」フィールドが削除されます。 |
| [!UICONTROL Apply] | オプション：<br>**[!UICONTROL Apply as percentage]**- [Listing Price](./listing-price.md)で定義した&#x200B;_[!UICONTROL Magento Price Source]_をパーセントで調整する場合に選択します。<br>**[!UICONTROL Apply as fixed amount]**— 定義した定義済みの価格を一_[!UICONTROL Magento Price Source]_ 定の金額 [で](./listing-price.md) 調整する場合に選択します。 |
| [!UICONTROL Adjustment Amount] | 必須。<br>「 `Apply as percentage` 」を選択 **[!UICONTROL Apply]**&#x200B;した場合は、パーセント値を入力します(例：25%の `25` 調整を入力します)。<br>「 `Apply as fixed amount`  **[!UICONTROL Apply]**」を選択した場合は、固定金額の数値を入力します(例：$25の `25` 固定調整を入力します)。 |
