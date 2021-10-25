---
title: 価格ルールのアクション
description: 価格ルールのアクションを使用して、Amazon のリスト価格を決定するために価格ソースに適用される調整計算を定義します。
redirect_from: /sales-channels/asc/ob-pricing-rules-actions.html
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 価格ルールのアクション

価格ルールのアクションによって、価格ソースに適用される調整計算が定義され、定価が特定されます。

## 標準価格ルール

[標準価格ルールを使用すると、 ](./standard-price-rules.md) Amazon の一覧表示価格を、 [!DNL Commerce] カタログ価格または価格ソースを基準として特定の比率または固定金額で増加または減少させることができます。

| 関連 | つい |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | ルールタイプをに設定 `Standard price rule` します。 |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | 価格ソースに適用される調整計算を定義して、リスト価格を決定します |

## インテリジェントな再価格ルール

インテリジェントな再 [ 価格ルール ](./intelligent-repricing-rules.md) では、Amazon の競合企業による価格設定によって、掲載価格が決定されます。 競合企業とは、Amazon に記載されたものと同じ製品が記載されている他の売り手です。

| 関連 | つい |
|--- |--- |
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | ルールタイプを、 `Intelligent repricing rule` 競合企業の価格ソースおよびフィードバック要件と共に設定します。 |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | 競合企業によって販売された同じ製品の条件の差異を定義します。 |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | 価格ソースに適用される調整計算を定義して、リスト価格を決定します |
| [[!UICONTROL Floor Price]](./floor-price.md) | 製品に最も安い価格を定義して、リスト価格が低すぎるように設定します。 |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | お客様の価格が競争力を維持するために、最も高い価格を製品について定義します。 |
