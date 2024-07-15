---
title: Amazon販売チャネル – 価格ルールアクション
description: 価格ルール処理を使用して、Amazonの上場価格を決定するために価格ソースに適用される調整計算を定義します。
feature: Sales Channels, Price Rules
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 価格ルールアクション

価格ルール処理では、上場価格を決定するために価格ソースに適用される調整計算を定義します。

## 標準価格ルール

[ 標準価格ルール ](./standard-price-rules.md) を使用すると、[!DNL Commerce] 定のカタログ価格（または価格ソース）に対して、Amazonの上場価格を特定の割合または固定ドル金額で増減させることができます。

| セクション | 説明 |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | ルールの種類を `Standard price rule` に設定します。 |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 上場価格を決定するために価格ソースに適用される調整計算を定義します |

## インテリジェントな再価格設定ルール

[ インテリジェントな再価格設定ルール ](./intelligent-repricing-rules.md) は、Amazonの競合他社の価格を使用して、上場価格を決定します。 競合他社は、Amazonにリストするのと同じ製品をリストしている他のセラーです。

| セクション | 説明 |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | 「Competitor Price Source」と「Feedback」の要件に加えて「`Intelligent repricing rule`」というルールタイプを設定します。 |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 競合他社が販売する同じ製品の条件に関する差異を定義します。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 上場価格を決定するために価格ソースに適用される調整計算を定義します |
| [[!UICONTROL Floor Price]](./floor-price.md) | 複数の価格ルールで上場価格が低く設定されるのを防ぐため、製品の最低価格を定義します。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | 製品の最高価格を定義して、価格の競争力を維持します。 |
