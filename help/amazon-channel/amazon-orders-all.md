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

Amazonの注文を表示するには、次の 2 つの方法があります。 _[!UICONTROL Recent Orders]_および_[!UICONTROL All Orders]_.

どちらのオプションでも、Amazonから受け取った基本的な注文情報が表示されます。次の情報が含まれます。

- 購入日
- オーダー番号
- ステータス
- バイヤーの名前
- 総計
- 注文メモ

_[!UICONTROL All Orders]_表示：注文検索のフィルタリングオプションを追加します。

>[!NOTE]
>
>例外： _[!UICONTROL Order Notes]_列、_[!UICONTROL Amazon orders]_ テーブルには、Amazonから受け取った注文情報が入力されます。 この _注文メモ_ 列の更新者 [!DNL Commerce] 注文のプロセスとして。

## 最近の注文

最新の注文は、で確認できます _[!UICONTROL Recent Orders]_の節 [ストアダッシュボード](./amazon-store-dashboard.md).

![最近の注文](assets/amazon-recent-orders-imported.png){width="600" zoomable="yes"}

### 最近のAmazon注文を表示

1. クリック **[!UICONTROL View Store]** ストアカード。

1. で注文を表示 _[!UICONTROL Recent Orders]_セクション。

1. 注文の詳細を表示するには、のAmazon注文番号をクリックします _[!UICONTROL Order Number]_列。

   この _[!UICONTROL Amazon Order Details]_注文のページが開きます。

## すべての注文を表示

Amazonからのすべての注文は次の URL で確認できます _[!UICONTROL Amazon orders]_ページ（_[!UICONTROL All Orders]_ 表示）。 Amazonの注文テーブルは次に似ています _[!UICONTROL Recent Orders]_のセクションに表示されますが、Amazonのすべての注文を表示したり、次のフィルターオプションで注文リストを絞り込んだりできます。

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazonの注文](assets/amazon-orders-list-all.png){width="600" zoomable="yes"}

### すべてのAmazon注文を表示

1. クリック **[!UICONTROL View Store]** ストアカード。

1. クリック **[!UICONTROL All Orders]** が含まれる _[!UICONTROL Recent Orders]_セクション。

1. リストを絞り込んだり、特定の注文番号を検索したりするには、 **[!UICONTROL Filter by]** パラメーターを使用して、 **[!UICONTROL Apply filters]**.

1. 注文の詳細を表示するには、のAmazon注文番号をクリックします _[!UICONTROL Order Number]_列。

   この _[!UICONTROL Amazon Order Details]_注文のページが開きます。

## フィルターの使用

で注文リストにフィルターを適用できます。 _[!UICONTROL Filter by]_セクション。 必要な選択を行い、**[!UICONTROL Apply filters]**. 適用されたフィルターが注文グリッドの上に表示されます。

![Amazon注文を表示するためのフィルター](assets/amazon-orders-filter-view.png){width="600" zoomable="yes"}

### 適用されたフィルターの変更

- でフィルターを追加または変更できます _[!UICONTROL Filter by]_セクション。 クリック&#x200B;**[!UICONTROL Apply filters]**注文リストと、注文グリッドの上に表示されるフィルターオプションを更新します。

- フィルターを削除するには、をクリックします。一度に 1 つずつ削除するには、 `x` をクリックして、フィルターまたはすべてを一度に **[!UICONTROL Clear all filters]**. フィルターを削除すると、注文リストと、注文グリッドの上に表示されるフィルターオプションが更新されます。

- 注文リストが長い場合は、グリッドの下のページネーションコントロールを使用して、さらに多くの注文を表示できます。

>[!TIP]
>
>注文表示に関するいくつかのヒント：
>
>- 複数のAmazon ストア統合がある場合、現在のストアの注文リストとページネーションの両方のビューを更新するために、ストアビューを切り替える際にページビューを更新する必要が生じる場合があります。
>- 列で並べ替える場合、並べ替えは現在のリストビューにのみ適用されます。 リストをフィルタリングしてから、表示しているページを並べ替えることが、ベストプラクティスです。
>- 表示ウィンドウの幅によっては、列内にテキストが重なって表示される場合があります。 テキストを折り返す列を展開するには、ウィンドウの表示を広げます。
>- でフィルタリングする場合 _[!UICONTROL Total]_、整数でフィルタリングします。 小数を入力すると、結果にエラーが発生する場合があります。

### デフォルトの列

| 列 | 説明 |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Filter by] | 内でのみ使用可能 _[!UICONTROL All Orders]_表示。<br>注文のリストを以下に基づいて絞り込む<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Amazonから受け取った購入日。 |
| [!UICONTROL Order Number] | Amazonで生成され、から受け取った注文番号。 Amazon注文の詳細画面を表示するには、リンクをクリックします。 |
| [!UICONTROL Status] | Amazonが受け取った注文のステータス。 オプション： `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Amazonから受け取った、注文を行った人物の名前。 |
| [!UICONTROL Grand Total] | Amazonから受け取った注文の合計通貨値。 |
| [!UICONTROL Order Notes] | 注文が処理されるときに記録された最新のアクション [!DNL Commerce]. この情報には、注文の読み込みエラーや注文処理の更新などが含まれますが、これらに限定されません。<br>**注意**：このフィールドの更新者 [!DNL Commerce] 注文のプロセスとして。 |
