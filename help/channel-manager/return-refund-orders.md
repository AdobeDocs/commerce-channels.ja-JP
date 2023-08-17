---
title: 返品・返金命令
description: から受け取った返品要求に対して、全額または一部払い戻しを発行する手順 [!DNL Walmart Marketplace] から [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceの
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# 返品・返金命令

購入者が、を通じて購入した注文品目の返品をリクエストした場合 [!DNL Walmart Marketplace]を指定した場合、ウォルマートは返品リクエストを作成します。 [!DNL Channel Manager] はこれらのリクエストの marketplace チャネルを監視し、返されるリクエスト情報をチャネルマネージャーに自動的に同期します。

コマース側では、戻り要求によって次のワークフローが開始されます。

1. チャネルマネージャーは、受け取ったステータスを持つ対応する戻り要求を作成し、戻り ID 番号 ([!UICONTROL RMA #]) を [!UICONTROL Returns] ダッシュボード。 次の日： [!DNL Orders] ダッシュボードに表示される場合、返品に関連付けられた注文のステータスの詳細。 [!UICONTROL Return requested] リンクをクリックして、リターンを表示および処理します。

1. マーチャントは、返品に関連する払い戻しを処理し、 [Adobe Commerce払い戻しワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). すべての返金は、オフライン方式を使用して処理されます。

1. [!DNL Channel Manager] は払い戻しの更新を Walmart マーケットプレイスに送信し、Adobe Commerceからの完了した返金を反映するために返金のステータスを更新できます。

ストアフロント管理で、Channel Manager からの返品を表示および処理するには、セールスチャネルストアを開き、「 」を選択します **[!UICONTROL Returns]**.

![チャネルマネージャー：から受け取った返品要求の返金を処理するためのダッシュボードを返します。 [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>出荷済注文の返金のみを処理できます。 In [!DNL Channel Manager]の場合、注文ステータスは [!UICONTROL Shipped]. In [!DNL Walmart Marketplace] 売り手の口座、注文は次の条件を満たす必要があります [!UICONTROL Delivered].

## 戻り値コントロールと列の説明

次の表に、で使用できるコントロールと列を示します。 [!DNL Channel Manager] はを返します。

**のコントロール[!UICONTROL Returns]**

<table>
<tr>
<td><strong>制御</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>次のいずれかを選択して、ビューをフィルターします。 [!UICONTROL Return Status] カード。</td>
</tr>
<tr>
<td>ステータスの詳細</td>
<td>を返します。 [!UICONTROL Received] または [!UICONTROL Refunded] ステータスの場合は、「ステータスの詳細」列でリンクされたテキストを選択して、返金のクレジットメモを作成または表示できます。</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>オーダーの詳細を表示するには、 [!DNL Commerce] 注文番号 [!UICONTROL Order] コマースオーダーを開くためのテーブル。</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>チャネル設定を変更するには、チャネル Walmart Connection 認証情報、マッピングされた属性、または配送先の ID を選択し、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。</td>
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
<td>から受け取った返品要求に関連付けられた返品商品認証番号。 [!DNL Walmart Marketplace]. この番号は、Walmart Marketplace によって生成されます [!UICONTROL Returns] 戻りプロセスが開始されたとき。</td>
</tr>
<tr>
<td>[!DNL Commerce] 注文番号</td>
<td>The [!DNL Commerce] Walmart Marketplace からの返品リクエストに含まれる品目に関連付けられた注文番号。 注文番号を選択して、注文の詳細を表示します。</td>
</tr>
<tr>
<td>リクエスト済み</td>
<td>返却がリクエストされた日付 [!DNL Walmart Marketplace]
ローカル時間に変換されました。</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>返品を満たすために返金する必要がある日付 [!DNL Walmart Marketplace] [ 要件 ](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) を現地時間に変換しました。</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>リターンにリストされる各品目の SKU と数量を表示します。</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>返された項目に対して払い戻される合計値。</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>現在の戻り値のステータスを [!DNL Commerce] ワークフローを返す —<i>受信済み</i>, <i>返金済み</i>または <i>エラー</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>受け取った返品エントリと返金された返品エントリについて、ステータスの詳細は返金処理用のクレジットメモにアクセスするためのリンクを提供します。 次の期間に [!DNL Channel Manager] Adobe Commerceと [!DNL Walmart marketplace]に値を指定しない場合、このフィールドにはエラーの説明が表示されます。</td>
</tr>
</table>

## 戻りステータス

[!UICONTROL Return Status] 現在の状態に関する情報を提供する [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理されたリクエストを返す

次の場合にステータスの更新が返されます。 [!DNL Channel Manager] からの返信要求を受信 [!DNL Walmart Marketplace] または [!DNL Commerce] 返品された品目の返金を処理するために、クレジットメモが作成されます。

戻り値には、次のステータスがあります。

* **[!UICONTROL Received]** — これは、 [!DNL Walmart Marketplace] ストア。 商人は、次を選択することで返品の返金を処理できます： **[!UICONTROL Create credit memo]** （内） [!UICONTROL Status details].

* **[!UICONTROL Refunded]** — 返品された品目の返金を発行するためにクレジットメモが作成されたことを示します。 商人は、次を選択することで払い戻し情報を表示できます： **[!UICONTROL View credit memo]** （内） [!UICONTROL Status details].

* **[!UICONTROL Error]** — エラーを持つリクエストを返します。 Walmart からの返信要求にデータがないか正しくない場合に、エラーが発生する可能性があります。 または、 [!DNL Channel Manager] 払い戻しの更新通知をウォルマートに送信できません。

## 戻りシナリオ

次のシナリオでは、次のシナリオで、からの様々なタイプの返品要求に対して払い戻しを発行する方法を説明します。 [!DNL Channel Manager].

* **フルリターン**—Walmart Marketplace の返品要求が注文の全品目に対するものである場合は、クレジット・メモ数量を更新してすべての品目を返金します。

* **部分的な戻り値**-Walmart Marketplace の返品要求が一部の受注品目に対してのみの場合は、払い戻す品目に対してのみクレジット・メモ数量を更新します。

* **Walmart Marketplace から返金済みの返品**・場合によっては、払い戻し処理が行われる [!DNL Walmart Marketplace] チャネルマネージャでリターンを処理する前に、以下の手順を実行します。 たとえば、Walmart が要求する 48 時間払い戻し処理期間内にコマース注文が払い戻されない場合、Walmart は自動的に注文を払い戻します。 この場合も、チャネルマネージャーは戻り要求をAdobe Commerceに同期するので、返信を処理してクレジットメモを発行できます。 このワークフローにより、 [!DNL Commerce] は、Walmart Marketplace の注文情報に一致します。

>[!NOTE]
>
> 同期する払い戻しの更新には最大 5 分かかる場合があります。 [!DNL Walmart Marketplace]. 現在の戻りステータスは、 [!DNL Channel Manager] [!UICONTROL Returns] ダッシュボード。

## 払い戻し要求の処理

1. を開きます。 [!UICONTROL Returns] セールスチャネルストアのダッシュボード。

   * 管理者で、「 」を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * 返り値を確認するには、 **[!UICONTROL Returns]** タブをクリックします。

     また、 [!UICONTROL Orders] ページに貼り付けます。 を探す [!UICONTROL Shipped] 返品リクエストを持つ注文。 次に、 `Return requested` リンクを [!UICONTROL Status Details] 列を使用して、リクエストを表示および処理します。

1. 「戻り値」テーブルで、 *[!UICONTROL Received]* ステータス。

1. 「品目」列で、返品する受注品目と数量のリストを確認します。

1. クレジットメモを発行して返金を処理します。

   * 次から： [!UICONTROL Status Details] 列、選択 **[!UICONTROL Create credit memo]** 注文の詳細ページを開くには、 [!DNL Commerce].

     注文が請求されていない場合、注文の詳細ページに、作成を促すエラーメッセージが表示されます。 選択 **[!UICONTROL Create invoice]**. すると、 [請求書の作成と保存](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * 注文の詳細ページで、「 」を選択します。 **[!UICONTROL Credit Memo]**.

   * In [!UICONTROL Items to Refund] のセクション [!UICONTROL Credit Memo]、を更新します。 **[!UICONTROL Qty to refund]** および **[!UICONTROL Return to Stock]** 返却リクエストに含まれる項目の情報。

     必ず、リターンリクエストにリストされている項目のみを返すようにしてください。

   * コメントを追加するには、 **[!UICONTROL Credit Memo Comments]**

   * 選択 **[!UICONTROL Refund Offline]**.

払い戻しを完了した後、 [!DNL Channel Manager] の返り値のステータスを更新します。 [!UICONTROL Returns] ダッシュボードから [!UICONTROL Refunded] とは、更新をウォルマートに同期して、marketplace の戻り状態を更新します。


## 返品の返金情報を表示します

返品要求および返金処理に関する情報は、 [!UICONTROL Returns] ダッシュボード。

1. セールスチャネルストアの返品ダッシュボードを開きます。

   * 管理者で、「 」を選択します。 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * 販売チャネルストアの目のアイコンを選択して、ストア表示を開きます。

   * 選択 **[!UICONTROL Returns]**.

1. 次を選択して払い戻し済みのオーダーを表示： **[!UICONTROL Refunded]** ステータスカード。

1. 選択して返品の返金の詳細を表示 **[!UICONTROL View credit memo]**.

   ![A の返品済品目を返金するクレジットメモ [!DNL Walmart Marketplace] 注文](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>命令が返還された後、 [!UICONTROL Orders] ダッシュボードに戻り値が表示されない。 戻り情報を表示するには、 [!DNL Channel Manager] ダッシュボードを返します。 詳細な返金および返金情報は、注文の詳細ページからも参照できます。

## リターンエラーを修正

エラーは、次の場所から返された情報を受け取ったときに発生する可能性があります： [!DNL Walmart Marketplace]または [!DNL Channel Manager] ステータスの更新を同期します： [!DNL Commerce] から [!DNL Walmart Marketplace].

戻りの更新の同期操作が失敗した場合、 [!DNL Channel Manager] ダッシュボードに *[!UICONTROL Error]* 戻り値エントリのステータス。 返金情報と返金情報が Walmart Marketplace アカウントに正確に反映されるようにするには、お客様の [!DNL Walmart Marketplace] ストア。
