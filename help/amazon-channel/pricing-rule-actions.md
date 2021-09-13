---
title: 価格ルールの処理
description: 価格ルールの処理を使用して、価格ソースに適用される調整計算を定義し、Amazon上場価格を決定します。
redirect_from: /sales-channels/asc/ob-pricing-rules-actions.html
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 価格ルールのアクション

価格基準処理では、価格表の価格を決定するために価格ソースに適用される調整計算を定義します。

## 標準価格ルール

[標準価格ルール](./standard-price-rules.md)を使用すると、Amazonの上場価格を[!DNL Commerce]カタログ価格（または価格ソース）に対して、特定の割合または固定ドル額で増減できます。

| セクション | 説明 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | ルールタイプを`Standard price rule`に設定します。 |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 価格ソースに適用される調整計算を定義して、上場価格を決定します |

## インテリジェントな価格変更ルール

[インテリジェントな再価格ルール](./intelligent-repricing-rules.md)では、Amazonの競合他社の価格を使用して、貴社の上場価格を決定します。 競合他社は、Amazonにリストしているのと同じ製品をリストしている他の販売者です。

| セクション | 説明 |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | ルールタイプを競合相手の価格ソースおよびフィードバック要件と共に`Intelligent repricing rule`に設定します。 |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 競合相手が販売した同じ製品の条件の差異を定義します。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 価格ソースに適用される調整計算を定義して、上場価格を決定します |
| [[!UICONTROL Floor Price]](./floor-price.md) | 複数の価格ルールで表示価格が低すぎるのを防ぐために、製品の最低価格を定義します。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | 価格を引き続き競争力のある製品に対して最高価格を定義します。 |
