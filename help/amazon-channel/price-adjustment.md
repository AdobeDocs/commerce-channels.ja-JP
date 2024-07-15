---
title: Amazon販売チャネル - [!UICONTROL Price Adjustment]
description: Amazon競合他社価格ソースを識別した場合は、価格調整を構成して価格計算を定義します。
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>「価格調整」セクションは、「標準」および「インテリジェント」再価格設定ルールとは少し異なります。 **[!UICONTROL Match Competitor Price]** は、**[!UICONTROL Rule Type]** が `Intelligent repricing rule` に設定されている場合に _[!UICONTROL Price Action]_でのみ使用できます。

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- [ルールタイプを選択](./intelligent-repricing-rules.md)
- [競合他社条件付き差異](./competitor-conditional-variances.md)
- 価格調整
- [フロアプライス](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

価格調整は、競合他社価格ソースを識別した場合の価格計算を定義します。

## 価格調整の設定

「_[!UICONTROL Price Adjustment]_」セクションで価格調整を定義します。

1. **[!UICONTROL Price Action]** の場合は、次のいずれかのオプションを選択します。

   - `Decrease By` – 定義された価格ソース値を下に調整し、ルールの価格を下げるタイミングを選択してから、Amazonにリストします。

   - `Increase By` – 定義済の価格ソース値を調整するタイミングを選択し、Amazonにリストする前にルールの価格を高くします。

   - `Match Competitor Price` - （インテリジェントな価格再設定ルールのみ）競合企業のフィードバックおよび差異パラメータに基づいて、Amazonの上場価格を [ 競合企業の最下位 ](./lowest-competitor-pricing.md) 価格に一致するように変更するタイミングを選択します。 `Match Competitor Price` に設定すると、「_[!UICONTROL Apply]_」フィールドと「_[!UICONTROL Adjustment Amount]_」フィールドが削除されます。

1. **[!UICONTROL Apply]** の場合は、次のいずれかのオプションを選択します。

   - `Apply as percentage` – 定義済 **[!UICONTROL Magento Price Source]** を [ 上場価格 ](./listing-price.md) でパーセントで調整するタイミングを選択します。

   - `Apply as fixed amount` – 定義済 **[!UICONTROL Magento Price Source]** を [ 定価 ](./listing-price.md) で定義し、固定金額で調整するタイミングを選択します。

1. **[!UICONTROL Adjustment Amount]** （必須）には、価格調整の数値を入力します。

   - **[!UICONTROL Apply]** を `Apply as percentage` に設定した場合は、パーセント値を入力します（例：25% の調整を行うには `25` を入力します）。

   - **[!UICONTROL Apply]** を `Apply as fixed amount` に設定した場合は、固定金額の数値を入力します（例：$25 の固定調整の場合は `25` を入力します）。

![ インテリジェント価格再設定ルール – 価格調整 ](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 価格設定調整処理を選択します。 オプション：<br>**[!UICONTROL Decrease By]**- Amazonにリストする前に、[ リスト価格 ](./listing-price.md) で定義した定義済みの _[!UICONTROL Magento Price Source]_を下に調整し、ルールの価格を下げるタイミングを選択します。<br>**[!UICONTROL Increase By]**- [ 上場価格 ](./listing-price.md) で定義した定義済みの_[!UICONTROL Magento Price Source]_ を調整するタイミングを選択し、Amazonにリストする前にルールの価格を高くします。<br>**[!UICONTROL Match Competitor Price]**- （インテリジェントな価格再設定ルールのみ）競合企業のフィードバックおよび差異パラメータに基づいて、Amazonの上場価格を [ 競合企業の最下位 ](./lowest-competitor-pricing.md) 価格に一致するように変更するタイミングを選択します。 選択すると、「_適用_」および「_調整金額_ フィールドが削除されます。 |
| [!UICONTROL Apply] | オプション：<br>**[!UICONTROL Apply as percentage]**– 定義済 _[!UICONTROL Magento Price Source]_を [ 上場価格 ](./listing-price.md) で定義するタイミングをパーセントで調整して選択します。<br>**[!UICONTROL Apply as fixed amount]**– 定義済_[!UICONTROL Magento Price Source]_ を [ 定価 ](./listing-price.md) で定義し、固定金額で調整するタイミングを選択します。 |
| [!UICONTROL Adjustment Amount] | 必須。<br>**[!UICONTROL Apply]** に `Apply as percentage` を選択した場合は、パーセント値を入力します（例：25% 調整には `25` を入力します）。<br>**[!UICONTROL Apply]** に `Apply as fixed amount` を選択した場合は、固定金額の数値を入力します（例：$25 の固定調整には `25` を入力します）。 |
