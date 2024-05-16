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

標準価格ルール処理を使用すると、Amazonの上場価格を、基準に対して指定した割合または固定のドル金額で増減させることができます [!DNL Commerce] カタログ価格（または価格ソース）。

標準価格ルール処理のセクションには、次のものがあります。

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## 価格ルールアクションの設定

1. の場合 **[!UICONTROL Rule Type]**、を選択 `Standard price rule`.

   このオプションは、内の他のフィールドを無効にします _[!UICONTROL Select Rule Type]_セクション。

1. を展開します。 _[!UICONTROL Price Adjustment]_必要に応じて、セクションに追加します。

1. の場合 **[!UICONTROL Price Action]**&#x200B;を選択して、 *[!UICONTROL Magento Price Source]* （で定義） [上場価格](./listing-price.md)）の値を使用します。

   - `Decrease By` -Amazonにリストする前に値を減らすタイミングを選択します。

   - `Increase By` -Amazonにリストする前に値を増やすタイミングを選択します。

1. の場合 **[!UICONTROL Apply]**&#x200B;を選択し、定義方法を決定します *[!UICONTROL Magento Price Source]* に定義済み [上場価格](./listing-price.md) 調整する値：

   - `Apply as percentage`  – を定義するタイミングを選択します *[!UICONTROL Magento Price Source]* に定義済み [上場価格](./listing-price.md) 割合で調整された値

   - `Apply as fixed amount`  – を定義するタイミングを選択します *[!UICONTROL Magento Price Source]* に定義済み [上場価格](./listing-price.md) 固定金額で調整された値。

1. の場合 **[!UICONTROL Adjustment Amount]** （必須）価格調整の数値を入力します。

   - 条件 *[!UICONTROL Apply]* はに設定されています。 `Apply as percentage`を入力し、パーセント値を入力します（例：enter `25` （25% の価格調整の場合）。

   - 条件 *[!UICONTROL Apply]* はに設定されています。 `Apply as fixed amount`に固定金額の数値を入力します（例： `25` $25 の固定価格調整）。

1. 完了したら、 **[!UICONTROL Save pricing rule]**.

![標準価格ルール](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | を選択 `Standard price rule`. |
| [!UICONTROL Price Action] | オプション：<ul><li>**[!UICONTROL Decrease By]**  – を定義するタイミングを選択します [!DNL Commerce] Amazonにリストする前に減らす価格ソースの値。</li><li>**[!UICONTROL Increase By]**  – を定義するタイミングを選択します [!DNL Commerce] Amazonにリストする前に増やす価格ソースの値。</li></ul> |
| [!UICONTROL Apply] | オプション：<ul><li>**[!UICONTROL Apply as percentage]**  – を定義するタイミングを選択します [!DNL Commerce] パーセンテージで調整された価格ソース値。</li><li>**[!UICONTROL Apply as fixed amount]**  – を定義するタイミングを選択します [!DNL Commerce] 固定金額で調整された価格ソースの値。</li></ul> |
| [!UICONTROL Adjustment Amount] | 必須。<br><br>次を選択した場合： `Apply as percentage` （用） *[!UICONTROL Apply]*&#x200B;を入力し、パーセント値を入力します（例：enter `25` （25% 調整の場合）。<br><br>を選択した場合 `Apply as fixed amount` （用） *[!UICONTROL Apply]*&#x200B;に固定金額の数値を入力します（例： `25` $25 の固定調整）。 |
