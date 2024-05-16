---
title: 返品注文と返品注文
description: から受領した返品要求に対する全額払い戻しまたは一部払い戻しの指示 [!DNL Walmart Marketplace] から [!DNL Channel Manager] （Adobe CommerceおよびMagento Open Sourceの場合）。
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 返品注文と返品注文

購入者が次の方法で購入した注文品目の返品を要求した場合 [!DNL Walmart Marketplace]、ウォルマートはリターンリクエストを作成します。 [!DNL Channel Manager] マーケットプレイスのチャネルでこれらのリクエストを監視し、リターンリクエスト情報を Channel Manager と自動的に同期します。

Commerce側では、返信リクエストによって次のワークフローが開始されます。

1. チャネルマネージャーは、受信したステータスで対応するリターンリクエストを作成し、リターン ID 番号（[!UICONTROL RMA #]）に設定します。 [!UICONTROL Returns] ダッシュボード。 日 [!DNL Orders] ダッシュボード。返品更新に関連付けられている受注のステータス詳細で、次の情報が含まれます [!UICONTROL Return requested] 返品を表示および処理するためのリンクです。

1. 加盟店は、次の手順に従ってクレジット・メモを作成することにより、返品に関連する払戻を処理します。 [Adobe Commerce返金ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). すべての払い戻しは、オフライン方式を使用して処理されます。

1. [!DNL Channel Manager] ウォルマートのマーケットプレイスに払い戻し更新を送信します。これにより、Adobe Commerceからの完了済み払い戻しを反映するように返品ステータスを更新できます。

ストアフロント管理者では、セールスチャネルストアを開いて選択することにより、チャネルマネージャーからの返品を表示および処理できます **[!UICONTROL Returns]**.

![チャネルマネージャー返品ダッシュボードで、から受信した返品リクエストの返金を処理します [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>出荷済の注文に対する払い戻しのみ処理できます。 対象： [!DNL Channel Manager]注文のステータスは、である必要があります [!UICONTROL Shipped]. 対象： [!DNL Walmart Marketplace] 販売者アカウント、注文は [!UICONTROL Delivered].

## コントロールおよび列の説明を戻します

次の表では、で使用できるコントロールと列について説明します [!DNL Channel Manager] を返します。

**のコントロール[!UICONTROL Returns]**

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>次のいずれかを選択してビューをフィルタリングします [!UICONTROL Return Status] カード。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>を持つリターンエントリの場合 [!UICONTROL Received] または [!UICONTROL Refunded] ステータス。「ステータス詳細」列のリンク・テキストを選択すると、払戻のクレジット・メモを作成または表示できます。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>注文の詳細を表示するには、 [!DNL Commerce] 内の注文番号 [!UICONTROL Order] Commerceの注文を開くためのテーブル。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネルウォルマート接続資格情報、マッピングされた属性または出荷識別子を選択し、設定を選択します [!DNL Commerce] 内の注文番号 [!UICONTROL Order] テーブル。 その後、を使用します。 [!DNL Commerce] 注文オプションを使用して注文を処理します。</td>
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
<td>から受信した返品要求に関連付けられた返品商品認証番号 [!DNL Walmart Marketplace]. この番号は、Walmart Marketplace によって生成されます [!UICONTROL Returns] 返品プロセスが開始された場合。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文#</td>
<td>この [!DNL Commerce] ウォルマート・マーケットプレイスからの返品リクエストに含まれる品目に関連付けられた注文番号。 注文番号を選択して、注文の詳細を表示します。</td>
</tr>
<tr>
<td>要求済み</td>
<td>返品がリクエストされた日付 [!DNL Walmart Marketplace]
現地時間に変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>返金期限の日付 [!DNL Walmart Marketplace] [requirements] （https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f）を現地時間に変換しました。</td>
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
<td>現在の復帰ステータスを [!DNL Commerce] ワークフローを返す – <i>受信済み</i>, <i>返済済み</i>、または <i>エラー</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>受入済および払戻済の返品エントリの場合、ステータスの詳細には、払戻処理のためにクレジット・メモにアクセスするためのリンクが表示されます。 でエラーが発生した場合、 [!DNL Channel Manager] Adobe Commerceとの間の同期プロセス [!DNL Walmart marketplace]、このフィールドにはエラーの説明が表示されます。</td>
</tr>
</table>

## 復帰ステータス

[!UICONTROL Return Status] 現在の状態に関する情報を提供します [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理される再来訪リクエスト。

復帰ステータスの更新は次の場合に発生します [!DNL Channel Manager] から返信リクエストを受信します [!DNL Walmart Marketplace] または [!DNL Commerce] 返品された品目の払戻を処理するためにクレジット・メモが作成されます。

返品には、次のステータスがあります。

* **[!UICONTROL Received]** – から受信したリターン リクエストの初期ステータスです。 [!DNL Walmart Marketplace] ストア。 マーチャントは、以下を選択して、返品の払い戻しを処理できます。 **[!UICONTROL Create credit memo]** が含まれる [!UICONTROL Status details].

* **[!UICONTROL Refunded]** – 返品された品目の払い戻しを発行するためにクレジット・メモが作成されたことを示します。 加盟店は、以下の項目を選択して払い戻し情報を表示できます **[!UICONTROL View credit memo]** が含まれる [!UICONTROL Status details].

* **[!UICONTROL Error]** – エラーのあるリクエストを返す。 ウォルマートからのリターンリクエストにデータが見つからないか、正しくない場合は、エラーが発生する可能性があります。 または、 [!DNL Channel Manager] 払い戻し更新通知をウォルマートに送信できません。

## シナリオを返します

次のシナリオでは、様々なタイプの返品要求に対して払戻を発行する方法を説明します。 [!DNL Channel Manager].

* **完全なリターン**—Walmart Marketplace の返品リクエストが注文のすべての品目に対するものである場合、すべての品目を払い戻すためにクレジット・メモ数量を更新します。

* **部分申告**- Walmart Marketplace の返品リクエストが一部の受注品目のみの場合は、払い戻す品目のクレジット・メモ数量のみを更新します。

* **ウォルマート マーケットプレイスから払い戻し済みの返品**・払い戻しの処理日 [!DNL Walmart Marketplace] チャネルマネージャーで返品を処理する前に。 例えば、ウォルマートが要求する 48 時間の払い戻し処理ウィンドウ内にCommerceの注文が払い戻されない場合、ウォルマートは注文を自動的に払い戻します。 この場合も、Channel Manager では引き続きAdobe Commerceへの返品要求を同期するので、ユーザーは返品を処理してクレジットメモを発行できます。 このワークフローにより、で注文の詳細が確認されます [!DNL Commerce] ウォルマート マーケットプレイスの注文情報と照合します。

>[!NOTE]
>
> 同期する払い戻し更新には、最大 5 分かかる場合があります [!DNL Walmart Marketplace]. 現在の復帰ステータスは、 [!DNL Channel Manager] [!UICONTROL Returns] ダッシュボード。

## 払戻要求の処理

1. を開きます [!UICONTROL Returns] 営業チャネルストアのダッシュボード。

   * 管理者から、を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * を選択すると、返品を確認できます。 **[!UICONTROL Returns]** タブ。

     返品情報には、 [!UICONTROL Orders] ページ。 を検索 [!UICONTROL Shipped] 返品リクエストがある注文。 次に、 `Return requested` 内のリンク [!UICONTROL Status Details] リクエストを表示および処理する列。

1. 「戻り値」テーブルから、を使用して戻り値を検索します *[!UICONTROL Received]* ステータス。

1. 「品目」列で、受注品目と払戻数量のリストを確認します。

1. クレジット・メモを発行して払戻を処理します。

   * から [!UICONTROL Status Details] 列、選択 **[!UICONTROL Create credit memo]** で注文の詳細ページを開くには [!DNL Commerce].

     注文が請求されていない場合、「注文の詳細」ページにエラーメッセージが表示され、注文を作成するように求められます。 を選択 **[!UICONTROL Create invoice]**. その後、 [請求書の作成と保存](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * 注文詳細ページで、を選択します **[!UICONTROL Credit Memo]**.

   * 対象： [!UICONTROL Items to Refund] の節 [!UICONTROL Credit Memo]、を更新します **[!UICONTROL Qty to refund]** および **[!UICONTROL Return to Stock]** 返品リクエストに含まれる品目の情報。

     必ず、再来訪リクエストにリストされている項目のみを返すようにします。

   * コメントを追加するには、 **[!UICONTROL Credit Memo Comments]**

   * を選択 **[!UICONTROL Refund Offline]**.

払い戻し完了後、 [!DNL Channel Manager] の復帰ステータスを更新します [!UICONTROL Returns] ダッシュボード先 [!UICONTROL Refunded] 更新をウォルマートに同期して、マーケットプレイスの返品ステータスを更新します。


## 返品の払戻情報の表示

返品リクエストと返金処理に関する情報は、から確認できます。 [!UICONTROL Returns] ダッシュボード。

1. 営業チャネルストアの返品ダッシュボードを開きます。

   * 管理者から、を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * を選択 **[!UICONTROL Returns]**.

1. を選択して、返金された注文を表示します **[!UICONTROL Refunded]** ステータスカード。

1. 選択して返品の払戻詳細を表示します。 **[!UICONTROL View credit memo]**.

   ![返品された品目を払い戻すためのクレジット・メモ [!DNL Walmart Marketplace] 順序](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>注文が返金された後、 [!UICONTROL Orders] ダッシュボードにリターン情報が表示されません。 返品情報を表示するには、次を使用します [!DNL Channel Manager] ダッシュボードを返します。 詳細な返品・払い戻し情報は、注文詳細ページからも入手できます。

## 戻り値エラーの修正

返信情報がから受信されると、エラーが発生する場合があります。 [!DNL Walmart Marketplace]または次の場合： [!DNL Channel Manager] からのステータス更新を同期 [!DNL Commerce] 対象： [!DNL Walmart Marketplace].

リターンアップデートの同期処理が失敗した場合、 [!DNL Channel Manager] ダッシュボードに表示されているを返します *[!UICONTROL Error]* 返品エントリのステータス。 返品および払い戻し情報が Walmart Marketplace アカウントに正確に反映されるようにするには、注文を手動で更新してください [!DNL Walmart Marketplace] ストア。
