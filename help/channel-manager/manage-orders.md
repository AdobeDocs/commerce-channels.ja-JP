---
title: '注文の表示と管理  [!DNL Channel Manager]'
description: 'Adobe CommerceとMagento Open Source用に  [!DNL Walmart Marketplace]  注文を表示および管理  [!DNL Channel Manager]  管理。'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# [!DNL Channel Manager] からの注文の表示と追跡

[!DNL Commerce] 製品の注文データ [!DNL Walmart Marketplace]、注文の処理後に自動的に同期 [!DNL Channel Manager] れ [!DNL Walmart] 同期されます。

[!DNL Commerce] 側では、同期が成功すると、次のアクションがトリガーされます。

- [!DNL Channel Manager] がウォルマートに注文確認を送信します。

- 対応する [!DNL Commerce] 注文がウォルマート注文から作成されます。

- 更新された注文情報が [!DNL Channel Manager] 注書ダッシュボードに表示されます。

ストアフロント管理者で、販売チャネルストアを開いて「**[!UICONTROL Orders]**」を選択すると、[!DNL Channel Manager] からの注文データを表示できます。

![ チャネルマネージャーの注文ビューで [!DNL Walmart Marketplace] 注文を管理する ](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Walmart Marketplace] しい注文が [!DNL Channel Manager] 注文リストに表示されるまで、最大 35 分かかる場合があります。 [!DNL Walmart] は、入荷注文を処理して [!DNL Channel Manager] に送信するために約 30 分かかります。 Channel Manager がオーダーを受け取ってから、オーダーを作成してAdobe CommerceまたはMagento Open Sourceに表示するのにさらに約 5 分かかります。

## オーダー・コントロールと列の説明

次の表では、受注に使用できるコントロールと列について説明します。

**[!UICONTROL Orders]** 用コントロール

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>[!UICONTROL Order Status] のカードの 1 つを選択して、ビューを並べ替えます。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>注文エラーと返品リクエストに関する情報を提供します。 注文の返品情報と払い戻しステータスを表示するには、<strong>[!UICONTROL Return requested]</strong> のテキストを選択して [!UICONTROL Returns] ダッシュボードを開きます。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>注文の詳細を表示するには、[!UICONTROL Order] のテーブルで [!DNL Commerce] 注番号を選択します。 次に、注文オプション [!DNL Commerce] 使用して注文を処理します。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネル ウォルマート接続の資格情報、マッピングされた属性、または出荷識別子を選択します。設定は、[!UICONTROL Order] テーブルの [!DNL Commerce] 注番号を選択します。 次に、注文オプション [!DNL Commerce] 使用して注文を処理します。</td>
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
<td>[!DNL Walmart Marketplace] で注文に割り当てられた発注書番号。 注文が最初に [!DNL Channel Manager] に読み込まれると、[!DNL Walmart] の注文番号のみが表示されます。 [!DNL Commerce] 注番号が作成されると、[!DNL Walmart] 注番号が [!UICONTROL External ID] 製品属性に保存されます。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文#</td>
<td>[!DNL Walmart Marketplace] 注から作成された [!DNL Commerce] 注に割り当てられた番号。</td>
</tr>
<tr>
<td>項目</td>
<td>[!DNL Walmart Marketplace] に並べ替えられた品目の数。</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>注文された品目の合計金額。</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>オーダーが [!DNL Walmart Marketplace] に送信された日付がローカルタイムゾーンに変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>ローカルタイムゾーンに変換された要件を満たすために注文 [!DNL Walmart Marketplace] 発送する必要がある日付。
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>ローカルタイムゾーンに変換された要件を満たすために [!DNL Walmart Marketplace] 注文をお客様に配送する必要がある日付。</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>注文に対して選択された [[!DNL Walmart Marketplace] 発送方法 ] （https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>注文データが最後に更新された時間を示すタイムスタンプ。[!DNL Channel Manager] れはローカルタイムゾーンに変換されます。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>現在の注文ワークフローにおける現在の [!DNL Commerce] 注ステータスを示します。 [!DNL Walmart Marketplace] から読み込まれた注文の初期ステータスは_Open_です。 追加ステータスの更新は、[!DNL Commerce] 注文が処理され、出荷、一部出荷およびキャンセルの更新 [!DNL Channel Manager] 品 [!DNL Walmart Marketplace] に正常に同期される場合に発生します。</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>エラーが発生した注文や返金リクエストに関する詳細情報を提供します。</td>
</tr>
</table>

## 注文ステータス

Adobe Commerce[!UICONTROL Order Status] たはMagento Open Sourceから管理される [!DNL Walmart Marketplace] 注文の現在のステータスに関する情報を提供します。 注文ステータスの更新は、[!DNL Channel Manager] が [!DNL Walmart Marketplace] または [!DNL Commerce] 注システムから更新された注文情報を受信した場合に発生します。 注文には次のステータスがあります。

- **[!UICONTROL Shipped]** - [!DNL Commerce] ストアから出荷されたオーダー。 注文が出荷されると、[!DNL Channel Manager] は更新を [!DNL Walmart Marketplace] に送信し、ウォルマートの出荷ステータスを更新し、出荷の注文トラッキング番号を指定します。 注文が出荷された後、ウォルマートが返品承認フォームを発行した場合、注文品目は部分的または完全に返金されます。 [ 返品と払戻 ](return-refund-orders.md) を参照してください。

- **[!UICONTROL Partially Shipped]** – 一部の品目が出荷済としてマークされ、その他の品目が出荷待ちの状態にある受注。 注文出荷内の品目が出荷されると、[!DNL Channel Manager] は更新を [!DNL Walmart Marketplace] に送信し、出荷ステータスを _[!DNL Partially Shipped]_on Walmart に更新して、出荷の注文トラッキング番号を提供します。

- **[!UICONTROL Canceled]** - [!DNL Commerce] ストアからキャンセルされた注文。

  注文のキャンセルが完了すると、[!DNL Commerce] の在庫数が更新され、返品された品目が反映されます。 次に、[!DNL Channel Manager] が更新を [!DNL Walmart Marketplace] に同期します。

- **[!UICONTROL Return requested]** - Walmart Marketplace が出荷済の受注品目に対する返品を要求すると、「[!UICONTROL Status details]」列に「`Return requested`」リンクが表示されます。 リンクを選択すると、[!UICONTROL Returns] のダッシュボードが開き、返品を表示して返金プロセスを管理できます。

- **[!UICONTROL Error]** - エラーがある受注。 注文の更新操作に失敗すると、エラーが発生する場合があります。 例えば、ウォルマートから新しい注文を受け取れない [!DNL Channel Manager] 合はエラーが発生します。 また、注文の出荷 [!DNL Channel Manager] キャンセルの更新を [!DNL Walmart Marketplace] に送信できない場合にも発生する可能性があります。 操作が失敗した場合、「注文」ページにその注文の _エラー_ ステータスが表示されます。 詳しくは、[ 注文エラーの修正 ] （process-orders.md#fix-shipping-and-cancellation- errors）を参照してください。

- **[!UICONTROL Status details]** – 情報の欠落や無効な値、出荷詳細の誤り、注文のキャンセル失敗などの問題が原因で発生する注文エラーに関する詳細情報を提供します。 この説明は、エラーが [!DNL Commerce] インスタンスで発生したか、[!DNL Walmart Marketplace] で発生したかを判断するのに役立ちます。

>[!NOTE]
>
>複数の出荷で注文品目が送信された場合、[!DNL Channel Manager] の注文ステータスは使用可能な最後の注文ステータスを反映します。 例えば、最初の品目が出荷され、注文の更新が [!DNL Channel Manager] と [!DNL Walmart Marketplace] に同期されたときにエラーが返されない場合、[!DNL Channel Manager] の注文のステータスは _[!UICONTROL Partially Shipped]_になります。 2 番目の品目が出荷され、[!DNL Channel Manager] がエラーを返した場合、注文ステータスは_[!UICONTROL Error]_ に更新されます。

## 注文を確認

1. 管理者から、**[!UICONTROL Marketing]** / **[!UICONTROL Channel Manager]** を選択して [!UICONTROL Channel Manager Marketplace Stores] ページを開きます。

1. ストアエントリ行の目のアイコンを選択してストア表示を開きます。

1. 注文情報を表示するには、*[!UICONTROL *Orders]**を選択します。

1. 注文に関する情報を取得し、**[ステータス](#order-status)** 列を確認して次の手順を決定します。

## 注文の詳細を確認

Marketplace から注文を受け取り、セールスチャネルストアに読み込んだ後、[!DNL Commerce] 注文 ID を使用して、注文の詳細をAdobe Commerceに表示します。

**[!UICONTROL Orders]** から **[!UICONTROL Commerce Order Number]** を選択して、[!DNL Commerce] 注文の詳細を開きます。

![[!DNL Walmart Marketplace] 注文のCommerce注文の詳細ビュー ](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

Commerce ストアフロントでは、[!DNL Walmart Marketplace] から読み込まれた注文に含まれる以下の追加情報が注文データに含まれます。

- **Payment Information &amp; Shipping Method** - ウォルマートからインポートされた注文には、以下の支払いフィールドと配送フィールドの値が含まれます。

   - **[!UICONTROL Offline Channel Payment]** – 注文の支払いが [!DNL Walmart Marketplace] によってオフラインで処理されることを示します。

   - **[!UICONTROL External Order Number]** -[!DNL Walmart Marketplace] 注番号を表示します。

   - **[!UICONTROL Channel Shipping - Value]** – 配送料が [!DNL Walmart Marketplace] で処理されることを示します。

   - **[!UICONTROL Cancellation Reason]** – このフィールドは、[!DNL Walmart Marketplace] からインポートしたオーダーがキャンセルされた場合にのみ表示されます。 キャンセルの理由は次のとおりです。

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **注文品目** – このセクションでは、すべてのCommerce注文の注文品目を一覧表示します。 [!UICONTROL Qty] 列には、注文項目のステータス履歴が表示されます。 例えば、注文が請求、出荷、および払い戻された場合、ステータスの推移を確認できます。

  ![ 受注詳細の受注品目ステータス履歴 [!DNL Walmart Marketplace] 受注 ](assets/order-detail-status-history.png){width="600" zoomable="yes"}

ナビゲーション・メニューから「[!UICONTROL Invoice]」および「[!UICONTROL Credit Memo]」オプションを選択して、品目請求書および払戻詳細を表示します。 また、販売チャネルストアの [[!UICONTROL Returns]](return-refund-orders.md) ダッシュボードから直接クレジットメモにアクセスすることもできます。
