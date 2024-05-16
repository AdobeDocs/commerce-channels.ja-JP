---
title: 'からの注文の表示と管理 [!DNL Channel Manager]'
description: '''表示と管理 [!DNL Walmart Marketplace] 次を使用した注文 [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceのために。'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# からの注文の表示と追跡 [!DNL Channel Manager]

[!DNL Walmart Marketplace] のデータを注文 [!DNL Commerce] 製品は次の場所に自動的に同期されます [!DNL Channel Manager] 後 [!DNL Walmart] 注文を処理します。

日 [!DNL Commerce] 側で、同期が成功すると、次のアクションがトリガーされます。

- [!DNL Channel Manager] ウォルマートに注文確認を送信します。

- 対応する [!DNL Commerce] オーダーはウォルマート・オーダーから作成されます。

- 更新された注文情報がに表示されます [!DNL Channel Manager] 注文ダッシュボード。

ストアフロントの Admin では、次の場所から注文データを表示できます [!DNL Channel Manager] 営業チャネル・ストアを開き、 **[!UICONTROL Orders]**.

![管理するチャネルマネージャーの注文表示 [!DNL Walmart Marketplace] 注文件数](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>所要時間は最大 35 分です [!DNL Walmart Marketplace] に表示する順序 [!DNL Channel Manager] 注文リスト。 [!DNL Walmart] 入荷注文を処理してに送信するのに約 30 分かかります [!DNL Channel Manager]. Channel Manager がオーダーを受け取ってから、オーダーを作成してAdobe CommerceまたはMagento Open Sourceに表示するのにさらに約 5 分かかります。

## オーダー・コントロールと列の説明

次の表では、受注に使用できるコントロールと列について説明します。

**のコントロール[!UICONTROL Orders]**

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>以下のいずれかを選択して、ビューを並べ替えます。 [!UICONTROL Order Status] カード。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>注文エラーと返品リクエストに関する情報を提供します。 注文の返品情報と返金ステータスを表示するには、 <strong>[!UICONTROL Return requested]</strong> を開くテキスト [!UICONTROL Returns] ダッシュボード。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>注文の詳細を表示するには、 [!DNL Commerce] 内の注文番号 [!UICONTROL Order] テーブル。 その後、を使用します。 [!DNL Commerce] 注文オプションを使用して注文を処理します。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネルウォルマート接続資格情報、マッピングされた属性または出荷識別子を選択し、設定を選択します [!DNL Commerce] 内の注文番号 [!UICONTROL Order] テーブル。 その後、を使用します。 [!DNL Commerce] 注文オプションを使用して注文を処理します。</td>
</tr>
</table>


**列の説明**

<table>
<tr>
<td>フィールド</td>
<td>説明</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>で注文に割り当てられた発注書番号 [!DNL Walmart Marketplace]. オーダーを最初に読み込むとき [!DNL Channel Manager]、のみ [!DNL Walmart] 注文番号が表示されます。 いつ [!DNL Commerce] オーダーが作成され、 [!DNL Walmart] 注文番号は、に保存されます。 [!UICONTROL External ID] 製品属性。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文#</td>
<td>に割り当てられた番号 [!DNL Commerce] 注文はから作成されました [!DNL Walmart Marketplace] オーダー。</td>
</tr>
<tr>
<td>項目</td>
<td>で注文された品目の数 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>注文された品目の合計金額。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>注文が送信された日付 [!DNL Walmart Marketplace] ローカルタイムゾーンに変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>注文の出荷期限の日付 [!DNL Walmart Marketplace] 要件がローカルタイムゾーンに変換されました。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>注文が顧客に配送される必要がある日付 [!DNL Walmart Marketplace] 要件がローカルタイムゾーンに変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>[[!DNL Walmart Marketplace] 配送方法 ] （https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29注文に対して選択されました。</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>注文データが最後に更新された時間を示すタイムスタンプ [!DNL Channel Manager] ローカルタイムゾーンに変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>現在の注文ステータスを示します [!DNL Commerce] 注文ワークフロー。 から読み込まれた注文の初期ステータス。 [!DNL Walmart Marketplace] _Open_です。 追加のステータス更新は次の場合に行われます [!DNL Commerce] 注文が処理され、 [!DNL Channel Manager] への出荷、部分出荷および取消の更新が正常に同期されます [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>エラーが発生した注文や返金リクエストに関する詳細情報を提供します。</td>
</tr>
</table>

## 注文ステータス

[!UICONTROL Order Status] 現在の状態に関する情報を提供します [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理される注文。 注文ステータスの更新は次の場合に行われます [!DNL Channel Manager] は、次のいずれかから更新された注文情報を受信します [!DNL Walmart Marketplace] または [!DNL Commerce] 注文システム。 注文には次のステータスがあります。

- **[!UICONTROL Shipped]** – 出荷された注文は、 [!DNL Commerce] ストア。 注文が出荷されると、 [!DNL Channel Manager] に更新を送信します [!DNL Walmart Marketplace] ウォルマートの出荷ステータスを更新し、出荷の注文トラッキング番号を入力します。 注文が出荷された後、ウォルマートが返品承認フォームを発行した場合、注文品目は部分的または完全に返金されます。 参照： [返品および返金](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** – 出荷済みとマークされた品目がある注文と、出荷待ちの品目がある注文。 注文内の項目が出荷されると、 [!DNL Channel Manager] に更新を送信します [!DNL Walmart Marketplace] 出荷ステータスを更新する手順は、次のとおりです _[!DNL Partially Shipped]_ウォルマートで、出荷の注文追跡番号を入力します。

- **[!UICONTROL Canceled]** – からキャンセルされた注文 [!DNL Commerce] ストア。

  注文のキャンセルが完了すると、 [!DNL Commerce] 在庫数が更新され、返された項目が反映されます。 その後、 [!DNL Channel Manager] 更新内容をに同期します [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**—Walmart Marketplace が、出荷済みの注文品目に対する返品をリクエストした場合、 `Return requested` リンクがに表示される [!UICONTROL Status details] 列。 リンクを選択すると、 [!UICONTROL Returns] 返品を表示し、返金プロセスを管理するためのダッシュボード。

- **[!UICONTROL Error]** – エラーが発生した注文。 注文の更新操作に失敗すると、エラーが発生する場合があります。 例えば、次の場合にエラーが発生します。 [!DNL Channel Manager] ウォルマートから新しい注文を受け取ることはできません。 また、以下の場合にも発生する可能性があります。 [!DNL Channel Manager] に注文出荷またはキャンセル更新を送信できません [!DNL Walmart Marketplace]. 操作が失敗した場合、「受注」ページに次の内容が表示されます _エラー_ 注文のステータス。 詳しくは、を参照してください [注文エラーの修正]（process-orders.md#fix-shipping-and-cancellation- errors）。

- **[!UICONTROL Status details]** – 情報の欠落や無効な値、出荷の詳細の誤り、注文のキャンセル失敗などの問題が原因で発生する注文エラーに関する詳細情報を提供します。 説明は、エラーが発生したかどうかを判断するのに役立ちます [!DNL Commerce] インスタンスまたは [!DNL Walmart Marketplace].

>[!NOTE]
>
>複数の出荷で注文品目が送信された場合、注文ステータスは [!DNL Channel Manager] 利用可能な最後の注文ステータスを反映します。 例えば、最初の項目が出荷され、注文の更新がに同期されたときにエラーが返されない場合などです [!DNL Channel Manager] および [!DNL Walmart Marketplace], [!DNL Channel Manager] 注文ステータス : _[!UICONTROL Partially Shipped]_. 2 つ目の品目が出荷された場合、および [!DNL Channel Manager] エラーが返され、注文ステータスが次のように更新されます_[!UICONTROL Error]_.

## 注文を確認

1. 管理者から、を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** を開きます [!UICONTROL Channel Manager Marketplace Stores] ページ。

1. ストアエントリ行の目のアイコンを選択してストア表示を開きます。

1. 注文情報を表示するには、*[!UICONTROL *Orders]**。

1. 注文に関する情報を取得し、 **[ステータス](#order-status)** 列。

## 注文の詳細を確認

Marketplace から注文を受け取り、セールスチャネルストアに読み込んだ後、 [!DNL Commerce] 注文 ID :Adobe Commerceで注文詳細を表示します。

送信元 **[!UICONTROL Orders]**&#x200B;を選択し、 **[!UICONTROL Commerce Order Number]** を開きます [!DNL Commerce] 注文詳細。

![のCommerce注文詳細ビュー [!DNL Walmart Marketplace] 順序](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

Commerce ストアフロントでは、次の場所から注文がインポートされました [!DNL Walmart Marketplace] 注文データには、以下の追加情報が含まれています。

- **お支払い情報と配送方法** – ウォルマートからインポートされた注文には、以下の支払いフィールドと配送フィールドの値が含まれます。

   - **[!UICONTROL Offline Channel Payment]** – 注文の支払いがオフラインで次のように処理されることを示します。 [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** – を表示する [!DNL Walmart Marketplace] オーダー番号。

   - **[!UICONTROL Channel Shipping - Value]** – 配送料が経由で処理されることを示します [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** – このフィールドは、注文がからインポートされた場合にのみ表示されます [!DNL Walmart Marketplace] がキャンセルされました。 キャンセルの理由は次のとおりです。

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **注文済み品目** – このセクションには、すべてのCommerce注文の注文項目が一覧表示されます。 この [!UICONTROL Qty] 列には、注文項目のステータス履歴が表示されます。 例えば、注文が請求、出荷、および払い戻された場合、ステータスの推移を確認できます。

  ![受注詳細の受注品目ステータス履歴 [!DNL Walmart Marketplace] 注文件数](assets/order-detail-status-history.png){width="600" zoomable="yes"}

を選択して、品目請求書および払戻詳細を表示します [!UICONTROL Invoice] および [!UICONTROL Credit Memo] ナビゲーションメニューのオプション。 また、から直接クレジットメモにアクセスすることもできます。 [[!UICONTROL Returns]](return-refund-orders.md) 営業チャネルストアのダッシュボード。
