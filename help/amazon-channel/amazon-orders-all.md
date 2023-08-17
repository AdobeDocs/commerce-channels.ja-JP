---
title: Amazon注文の表示
description: Adobe CommerceまたはMagento Open Source管理で、Amazon Marketplace の注文を表示します。
feature: Sales Channels, Orders
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Amazon注文の表示

Amazonの注文を表示する方法は 2 つあります。 _[!UICONTROL Recent Orders]_および_[!UICONTROL All Orders]_.

どちらのオプションも、Amazonから受け取った基本的な注文情報を示します。これには以下が含まれます。

- 購入日
- 注文番号
- ステータス
- 購入者の名前
- 総計
- 注文に関する注意

_[!UICONTROL All Orders]_「表示」では、注文検索のフィルターオプションが追加されます。

>[!NOTE]
>
>を除く _[!UICONTROL Order Notes]_列、_[!UICONTROL Amazon orders]_ テーブルには、Amazonから受け取った注文情報が入力されます。 The _注文に関する注意_ 列の更新者： [!DNL Commerce] を設定します。

## 最近の注文

最新の注文を _[!UICONTROL Recent Orders]_のセクション [ストアダッシュボード](./amazon-store-dashboard.md).

![最近の注文](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### 最近のAmazon注文を表示

1. クリック **[!UICONTROL View Store]** をストアカードに貼り付けます。

1. で注文を表示 _[!UICONTROL Recent Orders]_」セクションに入力します。

1. オーダーの詳細を表示するには、 _[!UICONTROL Order Number]_列。

   The _[!UICONTROL Amazon Order Details]_注文のページが開きます。

## すべての注文を表示

すべてのAmazon注文を _[!UICONTROL Amazon orders]_ページ (_[!UICONTROL All Orders]_ 表示 )。 Amazonの注文テーブルは、 _[!UICONTROL Recent Orders]_」セクションに表示されますが、Amazonのすべての注文を表示したり、次のフィルターオプションを使用して注文リストを絞り込んだりすることができます。

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon注文](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### すべてのAmazon注文を表示

1. クリック **[!UICONTROL View Store]** をストアカードに貼り付けます。

1. クリック **[!UICONTROL All Orders]** （内） _[!UICONTROL Recent Orders]_」セクションに入力します。

1. リストを絞り込んだり、特定の注文番号を検索したりするには、 **[!UICONTROL Filter by]** パラメーターとクリック **[!UICONTROL Apply filters]**.

1. オーダーの詳細を表示するには、 _[!UICONTROL Order Number]_列。

   The _[!UICONTROL Amazon Order Details]_注文のページが開きます。

## フィルターの使用

フィルターは、 _[!UICONTROL Filter by]_」セクションに入力します。 選択を行い、**[!UICONTROL Apply filters]**. 適用したフィルターが、注文グリッドの上に表示されます。

![Amazon注文を表示するためのフィルター](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### 適用されるフィルターの変更

- フィルターは、 _[!UICONTROL Filter by]_」セクションに入力します。 クリック&#x200B;**[!UICONTROL Apply filters]**をクリックして、注文グリッドの上に表示される注文リストとフィルターオプションを更新します。

- フィルターを削除するには、 `x` をクリックすると、フィルターまたはすべてを一度に **[!UICONTROL Clear all filters]**. フィルターを削除すると、注文リストと、注文グリッドの上に表示されるフィルターオプションが更新されます。

- 注文リストが長い場合、グリッドの下のページネーションコントロールを使用して、さらに多くの注文を表示できます。

>[!TIP]
>
>注文件数ビューに関するヒントを以下に示します。
>
>- 複数のAmazonストア統合がある場合、現在のストアの注文リストとページネーションビューの両方を更新するには、ストアビューを切り替える際にページビューを更新する必要が生じる場合があります。
>- 列で並べ替える場合、並べ替えは現在のリストビューにのみ適用されます。 リストをフィルタリングし、表示しているページを並べ替えるのがベストプラクティスです。
>- 表示ウィンドウの幅に応じて、列に重なったテキストが表示される場合があります。 折り返すテキストの列を拡大するには、ウィンドウの表示を広げます。
>- 次の条件でフィルターする場合： _[!UICONTROL Total]_、整数でフィルターします。 小数を入力すると、結果にエラーが発生する場合があります。

### デフォルトの列

| 列 | 説明 |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | 次の場所でのみ使用できます： _[!UICONTROL All Orders]_表示。<br>次の条件に基づいてオーダーのリストを絞り込みます。<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Amazonから受け取った購入日。 |
| [!UICONTROL Order Number] | Amazonが生成し、から受け取った注文番号。 Amazonの注文の詳細画面を表示するには、リンクをクリックします。 |
| [!UICONTROL Status] | Amazonが受け取った注文のステータス。 オプション： `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Amazonから受け取った、注文をした人の名前。 |
| [!UICONTROL Grand Total] | Amazonから受け取った注文の合計通貨値。 |
| [!UICONTROL Order Notes] | 注文の処理中に記録された最新のアクション [!DNL Commerce]. オーダーのインポートエラーやオーダー処理の更新などが情報に含まれますが、これらに限定されません。<br>**注意**：このフィールドは次の日付で更新されます： [!DNL Commerce] を設定します。 |
