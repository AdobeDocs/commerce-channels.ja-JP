---
title: '''次の注文を表示および追跡： [!DNL Channel Manager]'''
description: '''表示と管理 [!DNL Walmart Marketplace] 注文件数 [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceの』'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8146be1c94ffb1c8abd0d28e53d3476fd78f2c62
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# 次の注文の表示と追跡： [!DNL Channel Manager]

[!DNL Walmart Marketplace] データを注文する [!DNL Commerce] 製品は自動的ににを [!DNL Channel Manager] 後 [!DNL Walmart] は順序を処理します。

の [!DNL Commerce] 側、同期が成功すると、次のトリガーが実行されます。

- [!DNL Channel Manager] は注文確認をウォルマートに送信します。

- 対応する [!DNL Commerce] 注文はウォルマートの注文から作成されます。

- 更新された注文情報は、 [!DNL Channel Manager] 注文ダッシュボード。

ストアフロント管理で、次の注文データを表示できます： [!DNL Channel Manager] セールスチャネルストアを開き、「 」を選択します。 **[!UICONTROL Orders]**.

![管理するチャネルマネージャーの注文表示 [!DNL Walmart Marketplace] 注文件数](assets/orders-dashboard-view.png)

>[!NOTE]
>
>1 回の処理に最大 35 分かかる場合があります [!DNL Walmart Marketplace] 表示する順序 [!DNL Channel Manager] 注文リスト。 [!DNL Walmart] 受信注文を処理し、に送信するには約 30 分かかります。 [!DNL Channel Manager]. チャネルマネージャーが注文を受け取ると、Adobe CommerceまたはMagento Open Sourceで注文を作成して表示するのに、さらに約 5 分かかります。

## 受注管理と列の説明

次の表に、注文で使用できるコントロールと列を示します。

**のコントロール[!UICONTROL Orders]**
| **制御**                    | **説明**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     |次のいずれかを選択してビューを並べ替え [!UICONTROL Order Status] カード。                                                                                                                                                                                                           | |エラーの説明 |エラーステータスの注文に関する詳細情報を提供します。                                                                                                                                                                                                            | | [!UICONTROL View order detail] |注文の詳細を表示するには、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。                                                                                                                    | | [!UICONTROL Channel Settings]  |チャネル設定を変更するには、チャネル Walmart Connection 認証情報、マッピングされた属性、または配送先の ID を選択し、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。 |


**列の説明**

| フィールド | 説明 |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | 内の注文に割り当てられた発注書番号 [!DNL Walmart Marketplace]. 注文が最初に次に読み込まれたとき： [!DNL Channel Manager]、 [!DNL Walmart] 注文番号が表示されます。 次の場合に [!DNL Commerce] 注文が作成されると、 [!DNL Walmart] 注文番号は [!UICONTROL External ID] 製品属性。 |
| [!DNL Commerce] 注文番号 | に割り当てられた番号 [!DNL Commerce] から作成された注文 [!DNL Walmart Marketplace] 注文。 |
| 項目 | 注文日の項目数 [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | 注文項目の合計コスト。 |
| [!UICONTROL Date Ordered] | 注文が [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | 注文を満たすために発送する必要がある日付 [!DNL Walmart Marketplace] 要件 |
| [!UICONTROL Deliver By Date] | 注文を顧客に配送して満たす必要がある日付 [!DNL Walmart Marketplace] UTC 形式の要件。 |
| [!UICONTROL Ship Method] | この [[!DNL Walmart Marketplace] 発送方法](https://sellerhelp.walmart.com/s/guide?article=000007893) オーダーに対して選択されています。 |
| [!UICONTROL Last Update At] | 注文データが最後に更新された時刻を示すタイムスタンプ [!DNL Channel Manager] （UTC 形式） |
| [!UICONTROL Status] | 現在の注文ステータスを [!DNL Commerce] 注文ワークフロー。 からインポートされた注文の初期ステータス [!DNL Walmart Marketplace] が _開く_. 追加のステータス更新は、 [!DNL Commerce] 注文が処理され、 [!DNL Channel Manager] 出荷、出荷の一部、および取り消しの更新を [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | 注文に関する詳細情報を _[!UICONTROL Error]_ステータス。 |

## 注文ステータス


[!UICONTROL Order Status] 現在の状態に関する情報を提供する [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理される注文。 注文ステータスの更新は、 [!DNL Channel Manager] 次のいずれかから更新された注文情報を受け取る [!DNL Walmart Marketplace] または [!DNL Commerce] 注文システム。 オーダーには、次のステータスがあります。

- **[!UICONTROL Shipped]** — から出荷された注文 [!DNL Commerce] ストア。 命令が出る時 [!DNL Channel Manager] 更新をに送信 [!DNL Walmart Marketplace] をクリックして、Walmart 上の出荷ステータスを更新し、出荷の注文追跡番号を指定します。

- **[!UICONTROL Partially Shipped]** — 一部の品目が出荷済とマークされ、他の品目が出荷待ちとなっている注文。 受注出荷時の品目 [!DNL Channel Manager] 更新をに送信 [!DNL Walmart Marketplace] 発送ステータスを次の値に更新するには： _[!DNL Partially Shipped]_ウォルマートで、出荷の注文追跡番号を入力します。

- **[!UICONTROL Canceled]** — からキャンセルされた注文 [!DNL Commerce] ストア。

   注文のキャンセルが完了した後、 [!DNL Commerce] 返された品目を反映した在庫数量の更新 すると、 [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace].

- **[!UICONTROL Error]** — エラーが発生した注文。 注文の更新操作に失敗した場合、エラーが発生する可能性があります。 例えば、次の場合にエラーが発生します。 [!DNL Channel Manager] は、ウォルマートから新しい注文を受け取ることができません。 また、 [!DNL Channel Manager] 注文出荷またはキャンセルの更新を [!DNL Walmart Marketplace]. 操作が失敗した場合、注文ページに _エラー_ オーダーのステータス。 詳しくは、 [注文エラーを修正](process-orders.md#fix-shipping-and-cancell-errors)。

- **[!UICONTROL Error description]** — 情報の不足や値の不正、出荷の詳細の誤り、注文のキャンセルの失敗などの問題が原因で発生する注文エラーに関する詳細情報を提供します。 説明は、 [!DNL Commerce] インスタンスまたは [!DNL Walmart Marketplace].

>[!NOTE]
>
>注文品目が複数の出荷で送信される場合、 [!DNL Channel Manager] は、使用可能な最後の注文ステータスを反映します。 例えば、最初の品目が出荷され、注文の更新が [!DNL Channel Manager] および [!DNL Walmart Marketplace]、 [!DNL Channel Manager] 注文ステータス： _[!UICONTROL Partially Shipped]_. 2 つ目の品目が出荷され、 [!DNL Channel Manager] エラーを返します。注文ステータスは次の値に更新されます：_[!UICONTROL Error]_.

## 注文の確認

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 開く [!UICONTROL Channel Manager Marketplace Stores] ページ。

1. ストアエントリ行の目のアイコンを選択して、ストアビューを開きます。

1. 注文情報を表示するには、*を選択します。[!UICONTROL *Orders]**.

1. 注文に関する情報を取得し、次の手順を判断するには、 **[ステータス](#about-order-status)** 列。

## 注文の詳細を表示

Marketplace から注文を受け取り、Adobe CommerceまたはMagento Open Sourceに読み込んだ後、 [!DNL Commerce] 注文 ID を使用して、Adobe Commerceで注文を表示します。

送信者 **[!UICONTROL Orders]**&#x200B;を選択し、 **[!UICONTROL Commerce Order Number]** 開く [!DNL Commerce] 注文の詳細。

![のコマース注文の詳細ビュー [!DNL Walmart Marketplace] 注文](assets/order-detail-with-external-order-id.png)

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

