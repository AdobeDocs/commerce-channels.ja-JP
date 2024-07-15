---
title: Amazon販売チャネル – 標準価格ルール処理
description: 標準価格ルール処理を使用して、Commerceカタログ価格（または価格ソース）に対するAmazonの上場価格を増減します。
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# 標準価格ルール アクション

標準価格ルール処理を使用すると、[!DNL Commerce] 定のカタログ価格（または価格ソース）に対して、Amazonの上場価格を特定の割合または固定ドル金額で増減させることができます。

標準価格ルール処理のセクションには、次のものがあります。

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 価格ルールアクションの設定

1. **[!UICONTROL Rule Type]** の場合は、「`Standard price rule`」を選択します。

   このオプションを選択すると、「_[!UICONTROL Select Rule Type]_」セクションの他のフィールドが無効になります。

1. 必要に応じて、「_[!UICONTROL Price Adjustment]_」セクションを展開します。

1. **[!UICONTROL Price Action]** の場合は、*[!UICONTROL Magento Price Source]* （[ 上場価格 ](./listing-price.md)）値に定義されている）値の変更方法を決定するオプションを選択します。

   - `Decrease By` - Amazonにリストする前に値を減らすタイミングを選択します。

   - `Increase By` - Amazonにリストする前に値を増やすタイミングを選択します。

1. **[!UICONTROL Apply]** の場合は、定義済 *[!UICONTROL Magento Price Source]* を [ 上場価格 ](./listing-price.md) 値で調整する方法を決定するオプションを選択します。

   - `Apply as percentage` - [ 上場価格 ](./listing-price.md) 値で定義された *[!UICONTROL Magento Price Source]* をパーセントで調整するタイミングを選択します

   - `Apply as fixed amount` - [ 上場価格 ](./listing-price.md) 値で定義された *[!UICONTROL Magento Price Source]* を固定金額で調整するタイミングを選択します。

1. **[!UICONTROL Adjustment Amount]** （必須）には、価格調整の数値を入力します。

   - *[!UICONTROL Apply]* を `Apply as percentage` に設定した場合は、パーセント値を入力します（例：25% の価格調整に `25` を入力します）。

   - *[!UICONTROL Apply]* を `Apply as fixed amount` に設定した場合は、固定金額の数値を入力します（例：$25 の固定価格調整の場合は `25` を入力します）。

1. 完了したら、「**[!UICONTROL Save pricing rule]**」をクリックします。

![ 標準価格ルール ](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | 「`Standard price rule`」を選択します。 |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]** – 定義済の [!DNL Commerce] 価格ソース値を減らしてからAmazonにリストするタイミングを選択します。</li><li>**[!UICONTROL Increase By]** - Amazonにリストする前に、定義済みの [!DNL Commerce] 価ソース値を増やすタイミングを選択します。</li></ul> |
| [!UICONTROL Apply] | オプション：<ul><li>**[!UICONTROL Apply as percentage]** – 定義済の [!DNL Commerce] 価格ソース値をパーセントで調整するタイミングを選択します。</li><li>**[!UICONTROL Apply as fixed amount]** – 定義済の [!DNL Commerce] 価格ソース値を固定金額で調整するタイミングを選択します。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必須。<br><br>*[!UICONTROL Apply]* に `Apply as percentage` を選択した場合は、パーセント値を入力します（例：25% の調整には `25` を入力します）。<br><br>*[!UICONTROL Apply]* に `Apply as fixed amount` を選択した場合は、固定金額の数値を入力します（例：$25 の固定調整には `25` を入力します）。 |
