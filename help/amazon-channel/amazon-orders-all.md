---
title: Amazon の注文の表示
description: Amazon Marketplace の注文内容を Adobe Commerce または Magento Open Source Admins で表示します。
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Amazon の注文の表示

Amazon の注文内容を表示する方法は2つあり _[!UICONTROL Recent Orders]__[!UICONTROL All Orders]_ ます。

次のいずれかのオプションを選択すると、Amazon から受信した基本的な注文情報が表示されます。

- 購買日付
- 注文番号
- 現状
- バイヤーの名前
- 総計
- ノートの注文

_[!UICONTROL All Orders]_「表示」では、注文の検索にフィルタオプションが追加されます。

>[!NOTE]
>
>列を除い _[!UICONTROL Order Notes]__[!UICONTROL Amazon orders]_ て、Amazon から受け取った注文情報がテーブルに設定されます。 Order _Notes_ 列は、注文処理によって更新され [!DNL Commerce] ます。

## 最近使用した注文

最新の注文は、 _[!UICONTROL Recent Orders]_ストアダッシュボードのセクションに表示でき [ ](./amazon-store-dashboard.md) ます。

![最近使用した注文](assets/amazon-recent-orders-imported.png)

### 最近使用した Amazon orders の表示

1. ストアカードをクリックし **[!UICONTROL View Store]** ます。

1. セクションに注文を表示 _[!UICONTROL Recent Orders]_します。

1. 受注明細を表示するには、列内の Amazon の注文番号をクリックし _[!UICONTROL Order Number]_ます。

   _[!UICONTROL Amazon Order Details]_注文のページが表示されます。

## すべての注文を表示

すべての Amazon の注文をページ上に表示することができ _[!UICONTROL Amazon orders]_ます (ビューとも呼ば_[!UICONTROL All Orders]_ れます)。 Amazon Orders テーブルは、 _[!UICONTROL Recent Orders]_「store」ダッシュボードのセクションに似ていますが、すべての Amazon の注文を表示し、以下のフィルターオプションを使用して注文リストを絞り込むことができます。

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon の注文](assets/amazon-orders-list-all.png)

### すべての Amazon の注文を表示

1. ストアカードをクリックし **[!UICONTROL View Store]** ます。

1. **[!UICONTROL All Orders]**&#x200B;セクション内をクリックし _[!UICONTROL Recent Orders]_ます。

1. リストまたは特定の注文番号を検索するには、パラメーターを入力 **[!UICONTROL Filter by]** してをクリックし **[!UICONTROL Apply filters]** ます。

1. 受注明細を表示するには、列内の Amazon の注文番号をクリックし _[!UICONTROL Order Number]_ます。

   _[!UICONTROL Amazon Order Details]_注文のページが表示されます。

## フィルターの使用

セクション内の注文リストにフィルターを適用することができ _[!UICONTROL Filter by]_ます。 選択を行い、をクリックし&#x200B;**[!UICONTROL Apply filters]**ます。 適用されたフィルターは、注文グリッドの上に表示されます。

![Amazon の注文を表示するためのフィルター](assets/amazon-orders-filter-view.png)

### 適用されたフィルターの変更

- セクションにフィルターを追加したり、変更したりすることができ _[!UICONTROL Filter by]_ます。 クリック&#x200B;**[!UICONTROL Apply filters]**すると、注文リストと、注文グリッドの上に表示されるフィルターオプションが更新されます。

- フィルターを削除するには、フィルターを一度に1つずつクリックして選択するか、「すべて」を `x` クリックし **[!UICONTROL Clear all filters]** ます。 フィルターを削除すると、注文グリッドの上に表示される順序リストとフィルターオプションが更新されます。

- 注文リストが長い場合は、グリッドの下にあるページネーションコントロールを使用して、さらに注文を表示することができます。

>[!TIP]
>
>次に、注文ビューについてのヒントを示します。
>
>- Amazon store の統合が複数ある場合は、注文リストと現在のストアのページネーションビューの両方を更新する必要がある場合があります。これにより、ストアビューを切り替えたときのページの表示の更新が必要になります。
>- 列で並べ替える場合、並べ替えは現在のリストビューにのみ適用されます。 リストのフィルター処理、および表示中のページの並べ替えは、ベストプラクティスです。
>- ビューウィンドウの幅にもよりますが、列内のテキストが重なって表示される場合があります。 テキストが折り返し表示されるように列を拡大するには、ウィンドウの表示の幅を広げます。
>- を使用してフィルター処理を行う場合 _[!UICONTROL Total]_は、整数にフィルターをかけることができます。 10進数の値を入力すると、結果にエラーが発生する可能性があります。


### デフォルトの列

| 段 | つい |
|---|---|
| [!UICONTROL Filter by] | ビューでのみ使用でき _[!UICONTROL All Orders]_ます。<br>以下に基づいて注文の一覧を絞り込みます。<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Amazon から受信した購入日を指定します。 |
| [!UICONTROL Order Number] | によって生成され、Amazon から受信された注文番号を指定します。 「Amazon Order Details」画面を表示するには、リンクをクリックします。 |
| [!UICONTROL Status] | Amazon によって受信された注文のステータスを指定します。 オプション: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` `Unshipped` // `PartiallyShipped``PendingAvailability` |
| [!UICONTROL Buyer's Name] | Amazon から受信した注文を送信した人物の名前。 |
| [!UICONTROL Grand Total] | Amazon から受信した、注文の合計通貨値です。 |
| [!UICONTROL Order Notes] | 最後に記録されたアクションは、で処理される順に記録さ [!DNL Commerce] れます。 ここには、注文のインポートエラーや注文処理の更新に関する情報が含まれています。<br>**注意** : このフィールドは、注文処理によって更新され [!DNL Commerce] ます。 |
