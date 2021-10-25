---
title: 価格調整
description: 「価格調整を設定」では、Amazon の競合企業価格ソースを識別したときの価格計算を定義します。
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# 価格調整

>[!NOTE]
>
>標準的な価格設定とインテリジェントな再価格ルールでは、価格調整セクションが若干異なります。 **[!UICONTROL Match Competitor Price]** は、の「」に設定されている場合にのみ使用でき _[!UICONTROL Price Action]_**[!UICONTROL Rule Type]**`Intelligent repricing rule` ます。

インテリジェントな「価格設定」ルールのセクションには、次のものが含まれます。

- [ルールタイプを選択します。](./intelligent-repricing-rules.md)
- [競合企業の条件付き差異](./competitor-conditional-variances.md)
- 価格調整
- [フロア価格](./floor-price.md)
- [オプションの天井価格](./optional-ceiling-price.md)

価格調整により、競合企業の価格ソースを識別したときの価格計算が定義されます。

## 価格調整の設定

「」セクションで価格調整を指定し _[!UICONTROL Price Adjustment]_ます。

1. **[!UICONTROL Price Action]**&#x200B;で、次のいずれかのオプションを選択します。

   - `Decrease By` -このオプションを選択すると、Amazon の表示前に、定義されている価格ソース値を下に移動して、ルールにより低価格で作成することができます。

   - `Increase By` -このオプションを選択すると、Amazon の表示前に、定義された価格ソースの値を調整して、ルールにより高い価格を作成することができます。

   - `Match Competitor Price` -(インテリジェント再計算の規則のみ) [ ](./lowest-competitor-pricing.md) 競合企業のフィードバックおよび variance パラメーターに基づいて、Amazon の一覧価格を、競合企業の最低価格に合わせることができます。 「」に設定されている場合 `Match Competitor Price` _[!UICONTROL Apply]_は、と_[!UICONTROL Adjustment Amount]_ フィールドが削除されます。

1. **[!UICONTROL Apply]**&#x200B;で、次のいずれかのオプションを選択します。

   - `Apply as percentage` -リスト価格で定義された定義を、比率で調整する場合に選択し **[!UICONTROL Magento Price Source]** [ ](./listing-price.md) ます。

   - `Apply as fixed amount` - **[!UICONTROL Magento Price Source]** リスト価格で定義された定義を [ ](./listing-price.md) 固定金額で調整する場合に選択します。

1. **[!UICONTROL Adjustment Amount]**(必須) には、価格調整の数値を入力します。

   - **[!UICONTROL Apply]**「」に「」が設定されている場合は `Apply as percentage` 、パーセント値を入力します (例: enter: `25` 25%% 補正を入力します)。

   - **[!UICONTROL Apply]**&#x200B;がに設定されている場合は `Apply as fixed amount` 、固定金額の数値を入力します (例: 「$25 固定補正」を入力し `25` ます)。

![インテリジェントな再価格ルール-価格調整](assets/amazon-price-adjustment.png)

| 名 | つい |
|---|---|
| [!UICONTROL Price Action] | 「価格調整」アクションを選択します。 オプション:-リスト価格で定義された定義を下にして <br>**[!UICONTROL Decrease By]**_[!UICONTROL Magento Price Source]_調整し [ ](./listing-price.md) 、Amazon についての一覧を作成する前に、ルールにより低い価格を設定する場合に選択します。<br>**[!UICONTROL Increase By]**このオプションを選択すると、Amazon の一覧を作成する前に、出展価格で定義された定義を調整して、_[!UICONTROL Magento Price Source]_ [ ](./listing-price.md) ルールにより高い価格を設定することができます。<br>**[!UICONTROL Match Competitor Price]**-(インテリジェント再計算の規則のみ) [ ](./lowest-competitor-pricing.md) 競合企業のフィードバックおよび variance パラメーターに基づいて、Amazon の一覧価格を、競合企業の最低価格に合わせることができます。 この設定を選択すると、「 _適用」_ および「 _調整量」_ フィールドが削除されます。 |
| [!UICONTROL Apply] | 「オプション」: 「リスト価格で定義されている定義 <br>**[!UICONTROL Apply as percentage]**_[!UICONTROL Magento Price Source]_[ 値が ](./listing-price.md) 、比率で調整されるようにするには」を選択します。<br>**[!UICONTROL Apply as fixed amount]**-_[!UICONTROL Magento Price Source]_ リスト価格で定義された定義を [ ](./listing-price.md) 固定金額で調整する場合に選択します。 |
| [!UICONTROL Adjustment Amount] | 必須。<br>「」を選択した場合は `Apply as percentage` **[!UICONTROL Apply]** 、パーセント値を入力します (例: enter: `25` 25%% 補正を入力します)。<br>「」を選択した場合は `Apply as fixed amount` **[!UICONTROL Apply]** 、固定金額の数値を入力します (例: 入力した値が `25` $25 固定値である場合)。 |
