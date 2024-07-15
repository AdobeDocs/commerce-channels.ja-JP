---
title: 返品注文と返品注文
description: Adobe CommerceおよびMagento Open Sourceから  [!DNL Walmart Marketplace] from [!DNL Channel Manager]  を受け取った返品リクエストに対して完全または一部の払い戻しを行う手順。
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 返品注文と返品注文

買い手が [!DNL Walmart Marketplace] を通じて購入した注文品目の返品を要求すると、ウォルマートは返品要求を作成します。 [!DNL Channel Manager] は、これらのリクエストについて Marketplace チャネルを監視し、リターンリクエスト情報を自動的に Channel Manager に同期します。

Commerce側では、返信リクエストによって次のワークフローが開始されます。

1. チャネルマネージャーは、受信したステータスで対応するリターンリクエストを作成し、リターン ID 番号（[!UICONTROL RMA #]）を [!UICONTROL Returns] ダッシュボードに追加します。 [!DNL Orders] ダッシュボードでは、返品に関連付けられた受注のステータス詳細が更新され、返品を表示および処理するための [!UICONTROL Return requested] リンクが含まれます。

1. マーチャントは、[Adobe Commerce返金ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html) の後にクレジットメモを作成することで、返品に関連する返金を処理します。 すべての払い戻しは、オフライン方式を使用して処理されます。

1. [!DNL Channel Manager] がウォルマートのマーケットプレイスに払い戻し更新を送信します。これにより、Adobe Commerceからの完了済み払い戻しを反映するように返品ステータスを更新できます。

ストアフロント管理者では、セールスチャネルストアを開いて **[!UICONTROL Returns]** を選択することで、チャネルマネージャーからの返品を表示および処理できます。

![ チャネルマネージャー：[!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"} から受信した返品リクエストの払い戻しを処理する返品ダッシュボード

>[!NOTE]
>
>出荷済の注文に対する払い戻しのみ処理できます。 [!DNL Channel Manager] では、注文ステータスは [!UICONTROL Shipped] である必要があります。 売 [!DNL Walmart Marketplace] 者アカウントでは、注文は [!UICONTROL Delivered] である必要があります。

## コントロールおよび列の説明を戻します

次の表に、[!DNL Channel Manager] の戻り値に使用できるコントロールと列を示します。

**[!UICONTROL Returns]** 用コントロール

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>[!UICONTROL Return Status] カードの 1 つを選択して表示をフィルタリングします。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>ステータスが「[!UICONTROL Received]」または「[!UICONTROL Refunded]」の返品入力の場合は、「ステータス詳細」列のリンク・テキストを選択して、払戻のクレジット・メモを作成または表示できます。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>注文の詳細を表示するには、[!UICONTROL Order] テーブルの [!DNL Commerce] 注番号を選択して、Commerce注文を開きます。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネル ウォルマート接続の資格情報、マッピングされた属性、または出荷識別子を選択します。設定は、[!UICONTROL Order] テーブルの [!DNL Commerce] 注番号を選択します。 次に、注文オプション [!DNL Commerce] 使用して注文を処理します。</td>
</tr>
</table>

**列の説明**

<table>
<tr>
<td><strong>フィールド</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>[!DNL Walmart Marketplace] から受信した返品要求に関連付けられた返品商品認証番号。 この番号は、返品プロセスの開始時に Walmart Marketplace [!UICONTROL Returns] によって生成されます。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文#</td>
<td>Walmart Marketplace からの返品リクエストに含まれる品目に関連付けられた [!DNL Commerce] 注番号。 注文番号を選択して、注文の詳細を表示します。</td>
</tr>
<tr>
<td>要求済み</td>
<td>返品がリクエストされた日（[!DNL Walmart Marketplace]）
現地時間に変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>現地時間に変換された [ 要件 ] （https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f）を満たすため [!DNL Walmart Marketplace] 返品の返金期限となる日付。</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>返品に記載されている各品目の SKU と数量をリストします。</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>返品された品目に対して払い戻される合計金額。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>[!DNL Commerce] の返品ワークフローの現在の返品ステータスを示します <i>Received</i>、<i>Refunded</i>、または <i>Error</i>。</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>受入済および払戻済の返品エントリの場合、ステータスの詳細には、払戻処理のためにクレジット・メモにアクセスするためのリンクが表示されます。 Adobe Commerceと [!DNL Walmart marketplace] の間で [!DNL Channel Manager] 同期プロセス中にエラーが発生した場合、このフィールドにはエラーの説明が表示されます。</td>
</tr>
</table>

## 復帰ステータス

Adobe Commerce[!UICONTROL Return Status] たはMagento Open Sourceから管理される、[!DNL Walmart Marketplace] の返信リクエストの現在のステータスに関する情報を提供します。

返品ステータスの更新は、[!DNL Walmart Marketplace] から返品要求を受け取 [!DNL Channel Manager] た場合、または返品された品目の払い戻しを処理するために [!DNL Commerce] のクレジット・メモが作成された場合に発生します。

返品には、次のステータスがあります。

* **[!UICONTROL Received]** - [!DNL Walmart Marketplace] ストアから受信したリターンリクエストの初期ステータスです。 マーチャントは、[!UICONTROL Status details] ージで **[!UICONTROL Create credit memo]** を選択して、返品の払い戻しを処理できます。

* **[!UICONTROL Refunded]** – 返品された品目に対する払戻を発行するためにクレジット・メモが作成されたことを示します。 マーチャントは、[!UICONTROL Status details] ールバーで **[!UICONTROL View credit memo]** を選択すると、返金情報を表示できます。

* **[!UICONTROL Error]** - エラーが発生したリクエストを返します。 ウォルマートからのリターンリクエストにデータが見つからないか、正しくない場合は、エラーが発生する可能性があります。 または、払い戻し更新通知をウォルマートに送信で [!DNL Channel Manager] ない場合も同様です。

## シナリオを返します

次のシナリオでは、様々なタイプの返品リクエストに対して [!DNL Channel Manager] から払戻を発行する方法について説明します。

* **全返品** - Walmart Marketplace の返品リクエストが注文のすべての品目に対するものである場合、すべての品目を払い戻すためにクレジット・メモ数量を更新します。

* **部分返品**- Walmart Marketplace の返品要求が一部の受注品目のみの場合は、払い戻す品目のクレジット・メモ数量のみを更新します。

* **Walmart Marketplace を通じてすでに返金された返品** - チャネルマネージャーで返品を処理する前に、[!DNL Walmart Marketplace] 時に返金が処理される場合があります。 例えば、ウォルマートが要求する 48 時間の払い戻し処理ウィンドウ内にCommerceの注文が払い戻されない場合、ウォルマートは注文を自動的に払い戻します。 この場合も、Channel Manager では引き続きAdobe Commerceへの返品要求を同期するので、ユーザーは返品を処理してクレジットメモを発行できます。 このワークフローにより、[!DNL Commerce] の注文詳細が Walmart Marketplace の注文情報と一致するようになります。

>[!NOTE]
>
> [!DNL Walmart Marketplace] に同期するための払い戻し更新には、最大 5 分かかる場合があります。 [!DNL Channel Manager] [!UICONTROL Returns] ダッシュボードから、現在の復帰ステータスを確認できます。

## 払戻要求の処理

1. 営業チャネルストアの [!UICONTROL Returns] ダッシュボードを開きます。

   * 管理者から、**[!UICONTROL Marketing]**/**[!UICONTROL Channel Manager]** を選択します。

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * 「**[!UICONTROL Returns]**」タブを選択すると、返品を確認できます。

     [!UICONTROL Orders] のページから返却情報にアクセスすることもできます。 返品リクエスト [!UICONTROL Shipped] ある受注を検索します。 次に、[!UICONTROL Status Details] 列の `Return requested` リンクを選択して、リクエストを表示および処理します。

1. 「戻り値」表から、ステータスが「*[!UICONTROL Received]*」の戻り値を検索します。

1. 「品目」列で、受注品目と払戻数量のリストを確認します。

1. クレジット・メモを発行して払戻を処理します。

   * [!UICONTROL Status Details] の列から「**[!UICONTROL Create credit memo]**」を選択して、[!DNL Commerce] で注文の詳細ページを開きます。

     注文が請求されていない場合、「注文の詳細」ページにエラーメッセージが表示され、注文を作成するように求められます。 「**[!UICONTROL Create invoice]**」を選択します。 次に、[ 請求書を作成して保存 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html) します。

   * 注文詳細ページで、「**[!UICONTROL Credit Memo]**」を選択します。

   * [!UICONTROL Credit Memo][!UICONTROL Items to Refund] セクションで、返品リクエストに含まれる品目の **[!UICONTROL Qty to refund]** と **[!UICONTROL Return to Stock]** の情報を更新します。

     必ず、再来訪リクエストにリストされている項目のみを返すようにします。

   * コメントを追加するには、**[!UICONTROL Credit Memo Comments]** にテキストを入力します

   * 「**[!UICONTROL Refund Offline]**」を選択します。

払い戻しを完了した後、[!DNL Channel Manager] は [!UICONTROL Returns] ダッシュボードの返品ステータスを [!UICONTROL Refunded] に更新し、更新をウォルマートに同期して、マーケットプレイスの返品ステータスを更新します。


## 返品の払戻情報の表示

返品リクエストと返金処理に関する情報は、[!UICONTROL Returns] ダッシュボードから表示できます。

1. 営業チャネルストアの返品ダッシュボードを開きます。

   * 管理者から、**[!UICONTROL Marketing]**/**[!UICONTROL Channel Manager]** を選択します。

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * 「**[!UICONTROL Returns]**」を選択します。

1. **[!UICONTROL Refunded]** ステータスカードを選択すると、返金された注文を表示できます。

1. 「**[!UICONTROL View credit memo]**」を選択して、返品の払戻詳細を表示します。

   ![[!DNL Walmart Marketplace] 注品の返品品目を払い戻すためのクレジット メモ ](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>注文が返金された後、[!UICONTROL Orders] ダッシュボードに返品情報が表示されません。 返品情報を表示するには、[!DNL Channel Manager] Returns ダッシュボードを使用します。 詳細な返品・払い戻し情報は、注文詳細ページからも入手できます。

## 戻り値エラーの修正

エラーは、返信情報が [!DNL Walmart Marketplace] から受信されたとき、または [!DNL Channel Manager] が [!DNL Commerce] から [!DNL Walmart Marketplace] へのステータス更新を同期したときに発生する可能性があります。

返品更新の同期操作が失敗した場合、「返品 [!DNL Channel Manager] ダッシュボード」には、返品エントリの *[!UICONTROL Error]* ステータスが表示されます。 返品および払い戻し情報が Walmart Marketplace アカウントに正確に反映されていることを確認するには、[!DNL Walmart Marketplace] 店舗で注文を手動で更新します。
