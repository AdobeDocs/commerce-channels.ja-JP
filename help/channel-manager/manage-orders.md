---
title: ウォルマートマーケットプレイス注文の管理
description: 表示と管理 [!DNL Walmart Marketplace] 注文件数 [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceの
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 61d72e655a9f9eaefddd7561e0bc5fe36da69577
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# ウォルマートマーケットプレイスの注文の管理

[!DNL Walmart Marketplace] 注文件数 [!DNL Commerce] 製品リストは自動的ににに同期 [!DNL Channel Manager] ウォルマートが注文を処理した後 同期が完了したら、「 」を選択して注文情報を表示できます。 **[!UICONTROL Orders]** 次の接続済みチャネルストア表示から： [!DNL Channel Manager].

![Walmart Marketplace の注文を管理するためのチャネルマネージャの注文ビュー](assets/orders-dashboard-view.png)

>[!NOTE]
>
>1 回の処理に最大 35 分かかる場合があります [!DNL Walmart Marketplace] 表示する順序 [!DNL Channel Manager] 注文リスト。 [!DNL Walmart] 受信注文を処理し、に送信するには約 30 分かかります。 [!DNL Channel Manager].  チャネルマネージャーがこの注文を受け取ると、Adobe CommerceまたはMagento Open Sourceで注文を作成して表示するのに、さらに 5 分かかります。

## 注文の確認

1. 管理者から、 **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** 開く [!UICONTROL Channel Manager Marketplace Stores] ページ。

1. ストアエントリ行の鉛筆アイコンを選択して、ストアビューを開きます。

1. 注文情報を表示するには、*を選択します。[!UICONTROL *Orders]**.

## 注文の詳細を表示

Marketplace から注文を受け取り、Adobe CommerceまたはMagento Open Sourceに読み込んだ後、 [!DNL Commerce] 注文 ID を使用して、Adobe Commerceで注文を表示します。

送信者 **[!UICONTROL Orders]**&#x200B;を選択し、 **[!UICONTROL Commerce Order Number]** 開く [!DNL Commerce] 注文の詳細。

![ウォルマートマーケットプレイス注文のコマース注文の詳細ビュー](assets/order-detail-with-external-order-id.png)

### 受注管理と列の説明

次の表に、注文で使用できるコントロールと列を示します。

**のコントロール[!UICONTROL Orders]**
| **制御**                    | **説明**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     |次のいずれかを選択してビューを並べ替え [!UICONTROL Order Status] カード。                                                                                        | |エラーメッセージの詳細 | [!UICONTROL Error Status] を参照して、詳細なエラーメッセージを確認します。                                                                      | | [!UICONTROL View order detail] |注文の詳細を表示するには、 [!DNL Commerce] 注文番号 [!UICONTROL Order] 表。 次に、 [!DNL Commerce] オーダーのオプションを使用してオーダーを処理します。 |

**列の説明**

| フィールド | 説明 |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | 内の注文に割り当てられた発注書番号 [!DNL Walmart Marketplace]. 注文が最初に次に読み込まれたとき： [!DNL Channel Manager]に設定されている場合、ウォルマートの注文番号のみが表示されます。 次の場合に [!DNL Commerce] 注文が作成されると、 [!DNL Walmart] 注文番号は [!UICONTROL External ID] 製品属性。 |
| [!DNL Commerce]  注文番号 | に割り当てられた番号 [!DNL Commerce]  から作成された注文 [!DNL Walmart Marketplace] 注文。 |
| 項目 | 注文日の項目数 [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | 注文項目の合計コスト。 |
| [!UICONTROL Date Created] | 注文が [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | 注文を満たすために発送する必要がある日付 [!DNL Walmart Marketplace] 要件 |
| [!UICONTROL Order Status] | 現在の注文ステータスを [!DNL Commerce] 注文ワークフロー。 製品をに正常に追加すると、ステータスが更新されます。 [!DNL Channel Manager] 製品が [!DNL Walmart Marketplace]. 操作に失敗した場合は、リストにエラーステータスが表示されます。 エラーを修正した後、 [!DNL Channel Manager] 操作を再試行し、ステータスを更新します。 |

### オーダーステータスについて

[!UICONTROL Order Status] 現在の状態に関する情報を提供する [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceから管理される注文。 注文ステータスの更新は、 [!DNL Channel Manager] 次のいずれかから更新された注文情報を受け取る [!DNL Walmart Marketplace] または [!DNL Commerce] 注文システム。 オーダーには、次のステータスがあります。

* **[!UICONTROL Open]** — から受け取った注文 [!DNL Walmart Marketplace] Adobe CommerceまたはMagento Open Sourceでレビューおよび処理する準備が整いました。

   顧客が [!DNL Walmart Marketplace]の場合、接続されたチャネルの注文ワークスペースに開いた注文が表示されるまで、最大 35 分かかる場合があります。 [!DNL Commerce] 受信注文を処理し、に送信するには約 30 分かかります。 [!DNL Channel Manager]. チャネルマネージャーがこの注文を受け取ると、 [!DNL Commerce] 注文。

* **[!UICONTROL Processed]**・出荷、取り消し、返金された注文 [!DNL Commerce] ストア。

   出荷済、取消済および払戻済の受注をすべて表示するには、 **処理済み** ステータスカード。

* **[!UICONTROL Canceled]** — からキャンセルされた注文 [!DNL Commerce] ストア。

   注文のキャンセルが完了した後、 [!DNL Commerce] 返された品目を反映した在庫数量の更新 すると、 [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]**・払い戻しを受けた注文 [!DNL Commerce] ストア。

   払い戻しが完了した後、 [!DNL Commerce] 返済品目を反映する在庫数量の更新。 すると、 [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace].

* **[!UICONTROL Error]** — 情報が見つからないか、その他の問題が原因で、注文リポジトリにインポートされなかった注文。

   エラーメッセージの詳細を表示するには、 *[!UICONTROL Error]* ステータスインジケーター。 エラーを解決すると、注文が自動的に更新され、現在の情報とステータスが表示されます。
