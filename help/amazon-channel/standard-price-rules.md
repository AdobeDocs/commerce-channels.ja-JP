---
title: 標準価格ルール処理
description: 標準価格ルールのアクションを使用して、コマースカタログ価格（または価格ソース）に対するAmazonの上場価格を増減します。
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# 標準価格ルールのアクション

標準価格ルールアクションを使用すると、Amazonの上場価格を[!DNL Commerce]カタログ価格（または価格ソース）に対して、特定の割合または固定ドル額で増減できます。

標準価格ルールのアクションのセクションは次のとおりです。

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 価格ルールのアクションの設定

1. **[!UICONTROL Rule Type]**&#x200B;の場合は、`Standard price rule`を選択します。

   このオプションは、_[!UICONTROL Select Rule Type]_セクションの他のフィールドを無効にします。

1. 必要に応じて、_[!UICONTROL Price Adjustment]_セクションを展開します。

1. **[!UICONTROL Price Action]**&#x200B;の場合は、*[!UICONTROL Magento Price Source]*（[Listing Price](./listing-price.md)で定義）の値の変更方法を決定するオプションを選択します。

   - `Decrease By` - Amazonにリストする前に値を減らすタイミングを選択します。

   - `Increase By` - Amazonにリストする前に値を増やすタイミングを選択します。

1. **[!UICONTROL Apply]**&#x200B;の場合は、オプションを選択し、定義した&#x200B;*[!UICONTROL Magento Price Source]*&#x200B;を[Listing Price](./listing-price.md)の値でどのように調整するかを決定します。

   - `Apply as percentage` - 「リスト価格」で定義した値をパーセ *[!UICONTROL Magento Price Source]* ントで調整 [す](./listing-price.md) るタイミングを選択します

   - `Apply as fixed amount` - 「リスト価格」で定義した値を *[!UICONTROL Magento Price Source]* 一定金額で [調整](./listing-price.md) する場合に選択します。

1. **[!UICONTROL Adjustment Amount]**（必須）に、価格調整の数値を入力します。

   - *[!UICONTROL Apply]*&#x200B;を`Apply as percentage`に設定した場合は、パーセント値を入力します(例：「`25`」と入力して、価格調整を25%にします)。

   - *[!UICONTROL Apply]*&#x200B;を`Apply as fixed amount`に設定した場合は、固定金額の数値を入力します(例：$25固定価格調整の場合は、`25`と入力します。

1. 完了したら、「**[!UICONTROL Save pricing rule]**」をクリックします。

![標準価格ルール](assets/ob-price-rule-action-standard-example.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Rule Type] | `Standard price rule`を選択します。 |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]** - Amazonにリストする前に、定義した価格ソ [!DNL Commerce] ースの値を減らす場合に選択します。</li><li>**[!UICONTROL Increase By]** - Amazonにリストする前に、定義し [!DNL Commerce] た価格のソース値を増やすタイミングを選択します。</li></ul> |
| [!UICONTROL Apply] | オプション：<ul><li>**[!UICONTROL Apply as percentage]**  — 定義した価格ソースの値をパーセ [!DNL Commerce] ンテージで調整する場合に選択します。</li><li>**[!UICONTROL Apply as fixed amount]**  — 定義した価格ソース値を固定金 [!DNL Commerce] 額で調整する場合に選択します。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必須。<br><br>「 」を選択し `Apply as percentage` た場合 *[!UICONTROL Apply]*&#x200B;は、パーセント値を入力します(例：25%の `25` 調整を入力します)。<br><br>「 `Apply as fixed amount`  *[!UICONTROL Apply]*」を選択した場合は、固定金額の数値を入力します(例：$25の `25` 固定調整を入力します)。 |
