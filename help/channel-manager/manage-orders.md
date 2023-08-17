---
title: '注文の表示と管理元 [!DNL Channel Manager]'
description: '''表示と管理 [!DNL Walmart Marketplace] 注文件数 [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceの』'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# 注文の表示と追跡 [!DNL Channel Manager]

[!DNL Walmart Marketplace] データを注文する [!DNL Commerce] 製品は自動的ににを [!DNL Channel Manager] 次より後 [!DNL Walmart] は順序を処理します。

次の日： [!DNL Commerce] 側にある場合、同期が成功すると、次のトリガーが実行されます。

- [!DNL Channel Manager] は注文確認をウォルマートに送信します。

- 対応する [!DNL Commerce] 注文はウォルマートの注文から作成されます。

- 更新された注文情報は、 [!DNL Channel Manager] 注文ダッシュボード。

ストアフロント管理で、次の注文データを表示できます： [!DNL Channel Manager] セールスチャネルストアを開き、「 」を選択します。 **[!UICONTROL Orders]**.

![管理するチャネルマネージャーの注文表示 [!DNL Walmart Marketplace] 注文件数](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>1 回の処理に最大 35 分かかる場合があります [!DNL Walmart Marketplace] 表示する順序 [!DNL Channel Manager] 注文リスト。 [!DNL Walmart] 受信注文を処理し、に送信するには約 30 分かかります。 [!DNL Channel Manager]. チャネルマネージャーがこの注文を受け取ると、Adobe CommerceまたはMagento Open Sourceで注文を作成して表示するのに、さらに約 5 分かかります。

## 受注管理と列の説明

次の表に、注文で使用できるコントロールと列を示します。

**のコントロール[!UICONTROL Orders]**

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>いずれかを選択してビューを並べ替える [!UICONTROL Order Status] カード。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>注文エラーおよび返品リクエストに関する情報を提供します。 注文の返品情報と返金ステータスを表示するには、 <strong>[!UICONTROL Return requested]</strong> 開くテキスト [!UICONTROL Returns] ダッシュボード。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>オーダーの詳細を表示するには、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネル Walmart Connection 認証情報、マッピングされた属性、または配送先の ID を選択し、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。</td>
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
<td>内の注文に割り当てられた発注書番号 [!DNL Walmart Marketplace]. 注文が最初に次に読み込まれたとき： [!DNL Channel Manager]、 [!DNL Walmart] 注文番号が表示されます。 次の場合に [!DNL Commerce] 注文が作成されると、 [!DNL Walmart] 注文番号は [!UICONTROL External ID] 製品属性。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文番号</td>
<td>に割り当てられた番号 [!DNL Commerce] から作成された注文 [!DNL Walmart Marketplace] 注文。</td>
</tr>
<tr>
<td>項目</td>
<td>注文日の項目数 [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>注文項目の合計コスト。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>注文が [!DNL Walmart Marketplace] ローカルタイムゾーンに変換されます。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>満たすために注文を発送する必要がある日付 [!DNL Walmart Marketplace] 要件をローカルタイムゾーンに変換しました。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>注文が顧客に配信されて満たす必要がある日付 [!DNL Walmart Marketplace] 要件をローカルタイムゾーンに変換しました。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>[[!DNL Walmart Marketplace] 発送方法 ](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29注文に対して選択されています。</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>注文データが最後に更新された時刻を示すタイムスタンプ [!DNL Channel Manager] ローカルタイムゾーンに変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>現在の注文ステータスを示します。 [!DNL Commerce] 注文ワークフロー。 からインポートされた注文の初期ステータス [!DNL Walmart Marketplace] は_Open_です。 次の場合に追加のステータス更新が発生します。 [!DNL Commerce] 注文が処理され、 [!DNL Channel Manager] 出荷、出荷の一部、および取り消しの更新を [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>エラーまたは返金要求のある注文に関する詳細な情報を提供します。</td>
</tr>
</table>

## 注文ステータス

[!UICONTROL Order Status] 現在の状態に関する情報を提供する [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理される注文。 注文ステータスの更新は、 [!DNL Channel Manager] 次のいずれかから更新された注文情報を受け取る： [!DNL Walmart Marketplace] または [!DNL Commerce] 注文システム。 オーダーには、次のステータスがあります。

- **[!UICONTROL Shipped]** — から出荷された注文 [!DNL Commerce] ストア。 命令が出る時 [!DNL Channel Manager] がに更新を送信します。 [!DNL Walmart Marketplace] をクリックして、Walmart 上の出荷ステータスを更新し、出荷の注文追跡番号を指定します。 注文が出荷された後、Walmart が返品商品承認フォームを発行する場合、注文品の一部または完全払い戻しが可能です。 詳しくは、 [返品と返金](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** — 一部の品目が出荷済とマークされ、他の品目が出荷待ちとなっている注文。 受注出荷時の品目 [!DNL Channel Manager] がに更新を送信します。 [!DNL Walmart Marketplace] 発送ステータスを次の値に更新するには： _[!DNL Partially Shipped]_ウォルマートで、出荷の注文追跡番号を入力します。

- **[!UICONTROL Canceled]** — からキャンセルされたオーダー [!DNL Commerce] ストア。

  注文のキャンセルが完了した後、 [!DNL Commerce] 返された品目を反映した在庫数量の更新。 すると、 [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**—Walmart Marketplace が出荷済の注文品に対して返品を要求した場合、 `Return requested` リンクが [!UICONTROL Status details] 列。 リンクを選択すると、 [!UICONTROL Returns] ダッシュボードを使用して返品を表示し、払い戻しプロセスを管理します。

- **[!UICONTROL Error]** — エラーが発生したオーダー。 注文の更新操作に失敗した場合、エラーが発生する可能性があります。 例えば、次の場合にエラーが発生します。 [!DNL Channel Manager] は、ウォルマートから新しい注文を受け取ることができません。 また、 [!DNL Channel Manager] 注文出荷またはキャンセルの更新を [!DNL Walmart Marketplace]. 操作が失敗した場合、注文ページに _エラー_ オーダーのステータス。 詳しくは、 [注文エラーを修正](process-orders.md#fix-shipping-and-cancell-errors)。

- **[!UICONTROL Status details]** — 情報の不足や値の不正、出荷の詳細の誤り、注文のキャンセルの失敗などの問題が原因で発生する注文エラーに関する詳細を提供します。 説明は、 [!DNL Commerce] インスタンスまたは [!DNL Walmart Marketplace].

>[!NOTE]
>
>注文品目が複数の出荷で送信される場合、 [!DNL Channel Manager] は、使用可能な最後の注文ステータスを反映します。 例えば、最初の品目が出荷され、注文の更新が [!DNL Channel Manager] および [!DNL Walmart Marketplace]、 [!DNL Channel Manager] 注文ステータス： _[!UICONTROL Partially Shipped]_. 2 つ目の品目が出荷され、 [!DNL Channel Manager] エラーを返します。注文ステータスは次の値に更新されます：_[!UICONTROL Error]_.

## 注文の確認

1. 管理者で、「 」を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 開く [!UICONTROL Channel Manager Marketplace Stores] ページに貼り付けます。

1. ストアエントリ行の目のアイコンを選択して、ストアビューを開きます。

1. 注文情報を表示するには、*を選択します。[!UICONTROL *Orders]**.

1. 注文に関する情報を取得し、次の手順を判断するには、 **[ステータス](#order-status)** 列。

## 注文の詳細を確認

マーケットプレイスから注文を受け取り、セールスチャネルストアにインポートしたら、 [!DNL Commerce] 注文 ID :Adobe Commerceで注文の詳細を表示します。

送信者 **[!UICONTROL Orders]**&#x200B;を選択し、 **[!UICONTROL Commerce Order Number]** 開く [!DNL Commerce] 注文の詳細。

![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

Commerce ストアフロントで、次の場所からインポートされた注文： [!DNL Walmart Marketplace] 注文データには、次の追加情報が含まれています。

- **支払い情報と発送方法** — ウォルマートからインポートされた注文には、支払いフィールドと配送フィールドに関する次の値が含まれます。

   - **[!UICONTROL Offline Channel Payment]** — 注文の支払いが次の条件でオフラインで処理されることを示します： [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**— [!DNL Walmart Marketplace] 注文番号。

   - **[!UICONTROL Channel Shipping - Value]** — 送料が処理されることを示します [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** — このフィールドは、次の場所からインポートされた注文の場合にのみ表示されます： [!DNL Walmart Marketplace] がキャンセルされました。 キャンセルの理由は次のとおりです。

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **並べ替え済み項目** — このセクションには、すべてのコマースオーダーのオーダー項目がリスト表示されます。 The [!UICONTROL Qty] 列には、注文項目のステータス履歴が表示されます。 例えば、注文が請求済み、出荷済み、返金済みの場合、ステータス遷移を表示できます。

  ![注文の詳細順序付き品目ステータス履歴 [!DNL Walmart Marketplace] 注文件数](assets/order-detail-status-history.png){width="600" zoomable="yes"}

項目の請求書と払い戻しの詳細を表示するには、 [!UICONTROL Invoice] および [!UICONTROL Credit Memo] オプションを使用します。 クレジットメモには、 [[!UICONTROL Returns]](return-refund-orders.md) ダッシュボードをセールスチャネルストアに追加します。
