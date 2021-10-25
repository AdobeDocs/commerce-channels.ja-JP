---
title: 標準価格ルールアクション
description: 標準価格ルールのアクションを使用して、Commerce カタログ価格 (または価格ソース) を基準とした、Amazon のリスト価格を増加または減少させます。
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# 標準価格ルールアクション

標準価格ルールのアクションを使用すると、Amazon の一覧価格を特定の比率または価格ソースに基づいて一定の金額に延長または固定することができ [!DNL Commerce] ます。

標準価格ルールアクションには、次のセクションがあります。

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 価格ルールのアクションの設定

1. について **[!UICONTROL Rule Type]** は、を選択 `Standard price rule` します。

   このオプションを選択すると、セクション内の他のフィールドが無効化さ _[!UICONTROL Select Rule Type]_れます。

1. 必要に応じて、 _[!UICONTROL Price Adjustment]_セクションを展開します。

1. については、「 **[!UICONTROL Price Action]** 出展価格で定義します」の値を変更する方法を指定するオプションを選択し *[!UICONTROL Magento Price Source]* [ ](./listing-price.md) ます。

   - `Decrease By` -Amazon に一覧表示される前に値が減らされるようにするには、「いいえ」を選択します。

   - `Increase By` -Amazon に一覧表示する前に値を増加させたい場合は、このオプションを選択します。

1. については **[!UICONTROL Apply]** 、オプションを選択して、 *[!UICONTROL Magento Price Source]* 掲載価格値で定義されている定義を調整する方法を指定でき [ ](./listing-price.md) ます。

   - `Apply as percentage` -対象価格値で定義された定義を *[!UICONTROL Magento Price Source]* [ ](./listing-price.md) 、比率で調整する場合に選択します。

   - `Apply as fixed amount` -定価の値で定義された定義を *[!UICONTROL Magento Price Source]* [ 固定金額で調整する場合に選択し ](./listing-price.md) ます。

1. **[!UICONTROL Adjustment Amount]**(必須) には、価格調整の数値を入力します。

   - *[!UICONTROL Apply]*&#x200B;がに設定されている場合は `Apply as percentage` 、パーセント値を入力します (例: 価格調整には入力し `25` ます)。

   - *[!UICONTROL Apply]*&#x200B;がに設定されている場合は `Apply as fixed amount` 、固定金額の数値を入力します (例: `25` $25 固定価格調整の場合は入力します)。

1. 完了したら、をクリックし **[!UICONTROL Save pricing rule]** ます。

![標準価格ルール](assets/ob-price-rule-action-standard-example.png)

| 名 | つい |
|---|---|
| [!UICONTROL Rule Type] | を選択し `Standard price rule` ます。 |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]** -Amazon に一覧表示する前に、定義されている価格のソース値が減少するようにする場合に選択し [!DNL Commerce] ます。</li><li>**[!UICONTROL Increase By]** -Amazon に一覧表示する前に、定義されている [!DNL Commerce] 価格ソース値を増加させたい場合に選択します。</li></ul> |
| [!UICONTROL Apply] | オプション：<ul><li>**[!UICONTROL Apply as percentage]** このオプションを選択すると、定義されている [!DNL Commerce] 価格のソース値を割合で調整することができます。</li><li>**[!UICONTROL Apply as fixed amount]** このオプションを選択すると、定義されている [!DNL Commerce] 価格ソース値を一定量に合わせて調整することができます。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必須。<br><br>「For」を選択した場合は `Apply as percentage` *[!UICONTROL Apply]* 、パーセント値を入力します (例: enter: `25` 25%% 補正を入力します)。<br><br>「」を選択した場合は `Apply as fixed amount` *[!UICONTROL Apply]* 、固定金額の数値を入力します (例: 入力した値が `25` $25 固定値である場合)。 |
