---
title: Amazon注文の表示
description: AdobeコマースまたはMagento Open Source管理で、Amazon Marketplaceの注文を表示します。
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Amazon注文の表示

Amazonの注文を表示する方法は2つあります。_[!UICONTROL Recent Orders]_と_[!UICONTROL All Orders]_&#x200B;が表示されます。

どちらのオプションも、Amazonから受け取った次の基本注文情報を示します。

- 購入日
- 注文番号
- ステータス
- 購入者の名前
- 総計
- 注文メモ

_[!UICONTROL All Orders]_「表示」には、注文検索のフィルターオプションが追加されています。

>[!NOTE]
>
>_[!UICONTROL Order Notes]_列を除き、_[!UICONTROL Amazon orders]_&#x200B;テーブルには、Amazonから受け取った注文情報が入力されます。 _注文のメモ_&#x200B;列は、注文処理の際に[!DNL Commerce]によって更新されます。

## 最近の注文

[ストアダッシュボード](./amazon-store-dashboard.md)の&#x200B;_[!UICONTROL Recent Orders]_セクションで、最新の注文を確認できます。

![最近の注文件数](assets/amazon-recent-orders-imported.png)

### 最近のAmazon注文の表示

1. ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

1. _[!UICONTROL Recent Orders]_セクションで注文を確認します。

1. 注文の詳細を表示するには、_[!UICONTROL Order Number]_列のAmazonの注文番号をクリックします。

   注文の&#x200B;_[!UICONTROL Amazon Order Details]_ページが開きます。

## すべての注文を表示

_[!UICONTROL Amazon orders]_ページ（_[!UICONTROL All Orders]_&#x200B;ビューとも呼ばれます）で、Amazonの注文をすべて表示できます。 Amazonの注文件数テーブルは、店舗ダッシュボードの&#x200B;_[!UICONTROL Recent Orders]_セクションに似ていますが、Amazonの注文をすべて表示し、次のフィルターオプションを使用して注文リストを絞り込むことができます。

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon注文](assets/amazon-orders-list-all.png)

### すべてのAmazon注文の表示

1. ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

1. _[!UICONTROL Recent Orders]_セクションで&#x200B;**[!UICONTROL All Orders]**をクリックします。

1. リストを絞り込んだり、特定の注文番号を検索したりするには、**[!UICONTROL Filter by]**&#x200B;パラメーターを入力し、**[!UICONTROL Apply filters]**&#x200B;をクリックします。

1. 注文の詳細を表示するには、_[!UICONTROL Order Number]_列のAmazonの注文番号をクリックします。

   注文の&#x200B;_[!UICONTROL Amazon Order Details]_ページが開きます。

## フィルターの使用

_[!UICONTROL Filter by]_セクションの注文リストにフィルターを適用できます。 選択を行い、**[!UICONTROL Apply filters]**をクリックします。 適用したフィルターが注文グリッドの上に表示されます。

![Amazon注文を表示するためのフィルター](assets/amazon-orders-filter-view.png)

### 適用するフィルターの変更

- _[!UICONTROL Filter by]_セクションで、フィルターの追加や変更をおこなうことができます。**[!UICONTROL Apply filters]**をクリックして、注文リストと注文グリッドの上に表示されるフィルターオプションを更新します。

- フィルターを削除するには、フィルターの`x`をクリックするか、**[!UICONTROL Clear all filters]**&#x200B;をクリックして一度に1つずつ、またはすべてのフィルターを削除します。 フィルターを削除すると、注文リストと、注文グリッドの上に表示されるフィルターオプションが更新されます。

- 注文リストが長い場合は、グリッドの下のページネーションコントロールを使用して、さらに注文を表示できます。

>[!TIP]
>
>注文件数の表示に関するヒントを以下に示します。
>
>- 複数のAmazonストア統合がある場合、現在のストアの注文リストとページネーションビューの両方を更新するには、ストアビューを切り替える際にページビューの更新が必要になる場合があります。
>- 列で並べ替える場合、並べ替えは現在のリストビューにのみ適用されます。 リストをフィルタリングして、表示しているページを並べ替えるのがベストプラクティスです。
>- ビューウィンドウの幅に応じて、列に重なったテキストが表示される場合があります。 折り返すテキストの列を拡大するには、ウィンドウの表示を広げます。
>- _[!UICONTROL Total]_でフィルタリングする場合は、整数でフィルタリングします。 小数を入力すると、結果にエラーが発生する場合があります。


### デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Filter by] | _[!UICONTROL All Orders]_ビューでのみ使用できます。<br>次の項目に基づいて注文のリストを絞り込む：<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Amazonから受け取った購入日。 |
| [!UICONTROL Order Number] | Amazonが生成し、から受け取った注文番号。 Amazonの注文の詳細画面を表示するには、リンクをクリックします。 |
| [!UICONTROL Status] | Amazonが受け取った注文のステータス。 オプション：`Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Amazonから受け取った、注文をおこなった人の名前。 |
| [!UICONTROL Grand Total] | Amazonから受け取った注文の合計通貨値。 |
| [!UICONTROL Order Notes] | [!DNL Commerce]で処理される注文に対して記録された最新のアクション。 注文のインポートエラーや注文処理の更新に関する情報が含まれますが、これらに限定されません。<br>**注意**:このフィールドは、注文プロセ [!DNL Commerce] スの際にによって更新されます。 |
