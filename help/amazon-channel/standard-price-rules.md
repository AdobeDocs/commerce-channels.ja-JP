---
title: Amazonセールスチャネル — 標準価格ルールのアクション
description: 標準価格ルールアクションを使用して、コマースカタログ価格（または価格ソース）に対するAmazonの定価を増減します。
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 標準価格ルールアクション

標準的な価格ルールアクションを使用すると、Amazonの定価を、 [!DNL Commerce] カタログ価格（または価格のソース）。

標準価格ルールのアクションのセクションは次のとおりです。

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 価格ルールアクションの設定

1. の場合 **[!UICONTROL Rule Type]**&#x200B;を選択します。 `Standard price rule`.

   このオプションを選択すると、 _[!UICONTROL Select Rule Type]_」セクションに入力します。

1. を展開します。 _[!UICONTROL Price Adjustment]_セクション（必要に応じて）で設定します。

1. の場合 **[!UICONTROL Price Action]**」で、変更する方法を指定するオプションを選択します。 *[!UICONTROL Magento Price Source]* ( [上場価格](./listing-price.md)) の値を指定します。

   - `Decrease By` - Amazonにリストする前に値を減らすタイミングを選択します。

   - `Increase By` - Amazonにリストする前に値を増やす場合を選択します。

1. の場合 **[!UICONTROL Apply]**&#x200B;を選択し、定義する *[!UICONTROL Magento Price Source]* が [上場価格](./listing-price.md) 調整する値：

   - `Apply as percentage`  — いつ定義するかを選択します *[!UICONTROL Magento Price Source]* が [上場価格](./listing-price.md) パーセンテージで調整された値

   - `Apply as fixed amount`  — いつ定義するかを選択します *[!UICONTROL Magento Price Source]* が [上場価格](./listing-price.md) 一定金額で調整された値。

1. の場合 **[!UICONTROL Adjustment Amount]** （必須）価格調整の数値を入力します。

   - 条件 *[!UICONTROL Apply]* が `Apply as percentage`、パーセント値を入力します ( 例： `25` （25%の価格調整）。

   - 条件 *[!UICONTROL Apply]* が `Apply as fixed amount`、固定金額の数値を入力します ( 例： `25` 25 ドルの固定価格調整 )。

1. 完了したら、「 **[!UICONTROL Save pricing rule]**.

![標準価格ルール](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | 選択 `Standard price rule`. |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]**  — いつ定義するかを選択します [!DNL Commerce] Amazonに上場する前に減らす価格ソースの値。</li><li>**[!UICONTROL Increase By]**  — いつ定義するかを選択します [!DNL Commerce] Amazonに上場する前に増やす価格ソースの値。</li></ul> |
| [!UICONTROL Apply] | オプション：<ul><li>**[!UICONTROL Apply as percentage]**  — いつ定義するかを選択します [!DNL Commerce] パーセントで調整された価格ソースの値。</li><li>**[!UICONTROL Apply as fixed amount]**  — いつ定義するかを選択します [!DNL Commerce] 固定金額で調整された価格ソースの値。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必須。<br><br>次を選択した場合： `Apply as percentage` 対象： *[!UICONTROL Apply]*、パーセント値を入力します ( 例： `25` （25%調整）。<br><br>次を選択した場合： `Apply as fixed amount` 対象： *[!UICONTROL Apply]*、固定金額の数値を入力します ( 例： `25` （25 ドルの固定調整）。 |
