---
title: Amazonセールスチャネル — 価格ルールアクション
description: 価格ルールの処理を使用して、価格ソースに適用する調整計算を定義し、Amazon上場価格を決定します。
redirect_from: /sales-channels/asc/ob-pricing-rules-actions.html
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 価格ルールアクション

「価格ルール処理」は、価格表示価格を決定するために価格ソースに適用される調整計算を定義します。

## 標準価格ルール

A [標準価格ルール](./standard-price-rules.md) Amazonの定価を [!DNL Commerce] カタログ価格（または価格のソース）。

| セクション | 説明 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | ルールタイプをに設定します。 `Standard price rule`. |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 価格ソースに適用される調整計算を定義して、上場価格を決定します |

## インテリジェントな価格変更ルール

An [インテリジェントな再価格設定ルール](./intelligent-repricing-rules.md) はAmazonの競合他社の価格を使用して、上場価格を決定します。 競合他社は、Amazonにリストしているのと同じ製品をリストしている他のセラーです。

| セクション | 説明 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | ルールタイプをに設定します。 `Intelligent repricing rule` お客様の競合相手の価格のソースおよびフィードバック要件に合わせて |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 競合相手が販売した同じ製品の条件の差異を定義します。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 価格ソースに適用される調整計算を定義して、上場価格を決定します |
| [[!UICONTROL Floor Price]](./floor-price.md) | 複数の価格ルールでリスト価格が低すぎる設定を防ぐために、製品の最低価格を定義します。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | 価格を引き続き競争力を保つために、製品の最高価格を定義します。 |
