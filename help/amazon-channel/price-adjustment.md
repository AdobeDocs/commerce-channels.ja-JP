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
>「価格調整」セクションは、「標準」および「インテリジェント」再価格設定ルールとは少し異なります。 **[!UICONTROL Match Competitor Price]** は次の場所でのみ使用できます _[!UICONTROL Price Action]_条件&#x200B;**[!UICONTROL Rule Type]**はに設定されています。 `Intelligent repricing rule`.

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- [ルールタイプを選択](./intelligent-repricing-rules.md)
- [競合他社条件付き差異](./competitor-conditional-variances.md)
- 価格調整
- [フロアプライス](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

価格調整は、競合他社価格ソースを識別した場合の価格計算を定義します。

## 価格調整の設定

で価格調整を定義します。 _[!UICONTROL Price Adjustment]_セクション。

1. の場合 **[!UICONTROL Price Action]**、次のいずれかのオプションを選択します。

   - `Decrease By` -Amazonにリストする前に、定義された価格ソース値を下に調整し、ルールの価格を下げるタイミングを選択します。

   - `Increase By` -Amazonにリストする前に、定義された価格ソース値を調整し、ルールの価格を高くするタイミングを選択します。

   - `Match Competitor Price` - （インテリジェントな価格再設定ルールのみ）次の条件を満たすためにAmazonの上場価格を変更するタイミングを選択します [競合他社の最低値](./lowest-competitor-pricing.md) 価格：競合他社のフィードバックおよび差異パラメータに基づきます。 に設定されている場合 `Match Competitor Price`, _[!UICONTROL Apply]_および_[!UICONTROL Adjustment Amount]_ フィールドは削除されます。

1. の場合 **[!UICONTROL Apply]**、次のいずれかのオプションを選択します。

   - `Apply as percentage`  – を定義するタイミングを選択します **[!UICONTROL Magento Price Source]** に定義済み [上場価格](./listing-price.md) 割合で調整。

   - `Apply as fixed amount`  – を定義するタイミングを選択します **[!UICONTROL Magento Price Source]** に定義済み [上場価格](./listing-price.md) 固定金額で調整されます。

1. の場合 **[!UICONTROL Adjustment Amount]** （必須）価格調整の数値を入力します。

   - 条件 **[!UICONTROL Apply]** はに設定されています。 `Apply as percentage`を入力し、パーセント値を入力します（例：enter `25` （25% 調整の場合）。

   - 条件 **[!UICONTROL Apply]** はに設定されています。 `Apply as fixed amount`に固定金額の数値を入力します（例： `25` $25 の固定調整）。

![インテリジェントな再価格設定ルール – 価格調整](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | 価格設定調整処理を選択します。 オプション：<br>**[!UICONTROL Decrease By]**– を定義するタイミングを選択します _[!UICONTROL Magento Price Source]_に定義済み [上場価格](./listing-price.md) Amazonに上場する前にルールの価格を下げて調整を行う。<br>**[!UICONTROL Increase By]**– を定義するタイミングを選択します_[!UICONTROL Magento Price Source]_ に定義済み [上場価格](./listing-price.md) Amazonに上場する前にルールの価格を引き上げ、調整を行う。<br>**[!UICONTROL Match Competitor Price]**- （インテリジェントな価格再設定ルールのみ）次の条件を満たすためにAmazonの上場価格を変更するタイミングを選択します [競合他社の最低値](./lowest-competitor-pricing.md) 価格：競合他社のフィードバックおよび差異パラメータに基づきます。 選択した場合、 _適用_ および _調整金額_ フィールドは削除されます。 |
| [!UICONTROL Apply] | オプション：<br>**[!UICONTROL Apply as percentage]**– を定義するタイミングを選択します _[!UICONTROL Magento Price Source]_に定義済み [上場価格](./listing-price.md) 割合で調整。<br>**[!UICONTROL Apply as fixed amount]**– を定義するタイミングを選択します_[!UICONTROL Magento Price Source]_ に定義済み [上場価格](./listing-price.md) 固定金額で調整されます。 |
| [!UICONTROL Adjustment Amount] | 必須。<br>を選択した場合 `Apply as percentage` （用） **[!UICONTROL Apply]**&#x200B;を入力し、パーセント値を入力します（例：enter `25` （25% 調整の場合）。<br>を選択した場合 `Apply as fixed amount` （用） **[!UICONTROL Apply]**&#x200B;に固定金額の数値を入力します（例： `25` $25 の固定調整）。 |
