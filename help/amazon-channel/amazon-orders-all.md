---
title: Amazonの注文を表示
description: Amazon Marketplace の注文をAdobe CommerceまたはMagento Open Source管理者で表示できます。
feature: Sales Channels, Orders
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Amazonの注文を表示

Amazonの注文を表示する方法には、_[!UICONTROL Recent Orders]_と_[!UICONTROL All Orders]_ の 2 つがあります。

どちらのオプションでも、Amazonから受け取った基本的な注文情報が表示されます。次の情報が含まれます。

- 購入日
- オーダー番号
- ステータス
- バイヤーの名前
- 総計
- 注文メモ

表示 _[!UICONTROL All Orders]_は、注文検索のフィルタリングオプションが追加されます。

>[!NOTE]
>
>_[!UICONTROL Order Notes]_列を除き、_[!UICONTROL Amazon orders]_ テーブルには、Amazonから受け取った注文情報が入力されます。 _注文メモ_ 列は、注文の処理に合わせて [!DNL Commerce] によって更新されます。

## 最近の注文

最新の注文は、[ ストアダッシュボード ](./amazon-store-dashboard.md) の「_[!UICONTROL Recent Orders]_」セクションに表示されます。

![ 最近の注文 ](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### 最近のAmazon注文を表示

1. ストアカードの **[!UICONTROL View Store]** をクリックします。

1. 注文を「_[!UICONTROL Recent Orders]_」セクションで確認します。

1. 注文の詳細を表示するには、_[!UICONTROL Order Number]_列のAmazon注文番号をクリックします。

   注文の _[!UICONTROL Amazon Order Details]_ページが開きます。

## すべての注文を表示

Amazonのすべての注文を _[!UICONTROL Amazon orders]_ページで確認できます（_[!UICONTROL All Orders]_ ビューとも呼ばれます）。 「Amazon注文」テーブルは、ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションに似ていますが、すべてのAmazon注文を表示し、次のフィルターオプションを使用して注文リストを絞り込むことができます。

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon注文 ](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### すべてのAmazon注文を表示

1. ストアカードの **[!UICONTROL View Store]** をクリックします。

1. _[!UICONTROL Recent Orders]_のセクションの「**[!UICONTROL All Orders]**」をクリックします。

1. リストを絞り込んだり、特定の注文番号を検索したりするには、**[!UICONTROL Filter by]** のパラメーターを入力し、「**[!UICONTROL Apply filters]**」をクリックします。

1. 注文の詳細を表示するには、_[!UICONTROL Order Number]_列のAmazon注文番号をクリックします。

   注文の _[!UICONTROL Amazon Order Details]_ページが開きます。

## フィルターの使用

_[!UICONTROL Filter by]_のセクションで注文リストにフィルターを適用できます。 選択を行い、「**[!UICONTROL Apply filters]**」をクリックします。 適用されたフィルターが注文グリッドの上に表示されます。

![Amazon注文を表示するためのフィルター ](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### 適用されたフィルターの変更

- _[!UICONTROL Filter by]_のセクションでフィルターを追加または変更できます。**[!UICONTROL Apply filters]**をクリックして、注文リストと、注文グリッドの上に表示されるフィルターオプションを更新します。

- フィルターの `x` をクリックして一度に 1 つずつフィルターを削除することも、「**[!UICONTROL Clear all filters]**」をクリックして一度にすべて削除することもできます。 フィルターを削除すると、注文リストと、注文グリッドの上に表示されるフィルターオプションが更新されます。

- 注文リストが長い場合は、グリッドの下のページネーションコントロールを使用して、さらに多くの注文を表示できます。

>[!TIP]
>
>注文表示に関するいくつかのヒント：
>
>- 複数のAmazon ストア統合がある場合、現在のストアの注文リストとページネーションの両方のビューを更新するために、ストアビューを切り替える際にページビューを更新する必要が生じる場合があります。
>- 列で並べ替える場合、並べ替えは現在のリストビューにのみ適用されます。 リストをフィルタリングしてから、表示しているページを並べ替えることが、ベストプラクティスです。
>- 表示ウィンドウの幅によっては、列内にテキストが重なって表示される場合があります。 テキストを折り返す列を展開するには、ウィンドウの表示を広げます。
>- _[!UICONTROL Total]_でフィルタリングする場合は、整数でフィルタリングします。 小数を入力すると、結果にエラーが発生する場合があります。

### デフォルトの列

| 列 | 説明 |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | _[!UICONTROL All Orders]_ビューでのみ使用できます。<br> 注文のリストを以下に基づいて絞り込む<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Amazonから受け取った購入日。 |
| [!UICONTROL Order Number] | Amazonで生成され、から受け取った注文番号。 Amazon注文の詳細画面を表示するには、リンクをクリックします。 |
| [!UICONTROL Status] | Amazonが受け取った注文のステータス。 オプション：`Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Amazonから受け取った、注文を行った人物の名前。 |
| [!UICONTROL Grand Total] | Amazonから受け取った注文の合計通貨値。 |
| [!UICONTROL Order Notes] | 注文が [!DNL Commerce] で処理される際に記録された最新のアクション。 この情報には、注文の読み込みエラーや注文処理の更新などが含まれますが、これらに限定されません。<br>**メモ**：このフィールドは、注文の処理時に [!DNL Commerce] によって更新されます。 |
