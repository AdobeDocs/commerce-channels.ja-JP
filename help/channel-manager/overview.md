---
title: 'の概要 [!DNL Channel Manager]'
description: '''インストールと使用方法を学ぶ [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceストアを Walmart Marketplace と統合し、Marketplace のリスト、価格、在庫、販売をコマース管理者からシームレスに管理するためのセールスチャネルを作成します。」'
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# の概要 [!DNL Channel Manager]

[!DNL Channel Manager] Adobe CommerceまたはMagento Open Sourceの製品カタログを [!DNL Walmart Marketplace].

![[!DNL Channel Manager] 拡張機能の管理ビュー](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] 売りたがるAdobe CommerceまたはMagento Open Sourceの商人を支える [!DNL Walmart Marketplace] を拡張して [!DNL Commerce] 管理者。 を使用 [!DNL Channel Manager] インストール済み、ストア管理者、および運用スタッフが管理できる [!DNL Walmart Marketplace] 販売、在庫、製品の価格は、コマース環境からシームレスに設定できます。

拡張された管理者は、同じワークフローとプロセスを使用して両方の販売を管理できるので、運用を合理化します [!DNL Commerce] 店頭とウォルマート・マーケットプレイス

をインストールして設定した後 [!DNL Channel Manager]を使用すると、以下の機能を使用して Walmart Marketplace の販売注文を管理できます。

* **リスト管理** — お客様の [!DNL Commerce] 既存の [!DNL Walmart Marketplace] リスト

* **Inventory management** — 商家のマーケットプレイスセラーアカウント内の項目は、自動的に同期され、更新されます [!DNL Commerce] 正確な在庫レベルを確保する。

* **価格の更新**：自動価格同期を使用して、マーケットプレイスリストの正確な価格を維持します。 Adobe Commerceで価格が変更されると、変更が市場に反映されます。

* **注文管理** — マーケットプレイスで新しい注文が作成されたとき、 [!DNL Channel Manager] は注文をAdobe Commerceと同期し、注文確認をマーケットプレイスに送信します。 この確認により、注文ごとに在庫が確実に予約されます。 最後の手順は、 [!DNL Commerce] 処理のための Order Management システム。

* **出荷管理**—Adobe Commerceで注文が出荷済とマークされると、出荷の更新が [!DNL Walmart Marketplace]. この通知により、販売者は達成 SLA の要件を満たし、顧客は現在の注文の出荷更新通知を受け取ることができます。

* **キャンセル**- Adobe Commerceで注文がキャンセルされたとき、 [!DNL Channel Manager] は、更新された注文情報を marketplace に送信し、対応する marketplace 注文のアクションをレプリケートします。 注文のキャンセルが完了した後、 [!DNL Commerce] 返品品目を反映する在庫数量の更新と在庫の更新は、次の項目に自動的に同期されます： [!DNL Walmart Marketplace].

* **返品と返金**—Walmart Marketplace がAdobe CommerceまたはMagento Open Source販売チャネルを通じて注文された品目の返品を要求した場合、 [!DNL Channel Manager] リターンリクエスト情報を Commerce セールスチャネルストアに送信して、リターンリクエストをレプリケートします。 その後、払い戻しは、 [!DNL Commerce] [払い戻しワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow)、オフラインメソッド。 払い戻しが完了した後、 [!DNL Channel Manager] Walmart への更新を同期して、marketplace セラーアカウントの返品ステータスを更新して返金を反映させることができます。

## の予想遅延 [!DNL Channel Manager] 操作

次の間のデータ同期プロセス： [!DNL Channel Manager] リンクされた [!DNL Walmart Marketplace] ストアが完了するまでにしばらく時間が必要です。 次の予定処理時間を確認 [!DNL Channel Manager] 営業チャネルの運用を計画する際に役立つ操作です。

**の推定待ち時間 [!DNL Channel Manager] 操作**

| **操作** | **説明** | **予想される遅延** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 製品の追加先 [!DNL Channel Manager] | 次から製品を選択： [!DNL Commerce] 製品カタログと読み込み [!DNL Channel Manager]. | **最大 5 分** — 製品カタログ全体など、多数の製品を選択した場合、読み込み処理に時間がかかります。 |
| 次の製品を照合： [!DNL Walmart Marketplace] | で製品リストを選択 [!DNL Channel Manager] 照合のためにウォルマートに送信します。 | **最大 30 分** — 多数の製品を選択した場合、選択した数量に応じて、照合の処理に時間がかかります。 |
| 在庫の更新 | Commerce で在庫数量が変更された場合、 [!DNL Channel Manager] は、Walmart への更新を同期します。 | **最大 10 分** |
| 価格の更新 | 製品価格が変更された場合、 [!DNL Channel Manager] は、Walmart への更新を同期します。 | **最大 5 分** |
| ウォルマートからへの同期の注文 [!DNL Commerce] | 顧客が a を注文 [!DNL Commerce] 製品を Walmart Marketplace で利用できます。 ウォルマートが注文をに送る [!DNL Channel Manager]. 注文は注文ダッシュボードに表示されます。 | **最大 30 分** |
| 注文が次の場所で作成されました： [!DNL Commerce] Order Management | [!DNL Channel Manager] を作成 [!DNL Commerce] 注文をウォルマート注文から受け取り、注文ダッシュボードを更新して [!DNL Commerce] 注文番号。 | **最大 5 分** |
| 出荷ステータスの更新： [!DNL Commerce] Order Management | 注文がコマースから発送された場合、 [!DNL Channel Manager] 注文ダッシュボードの出荷ステータスを更新し、顧客に通知できるように更新を Walmart Marketplace に送信します。 | **最大 5 分** |
| Commerce Order Management での注文キャンセルの更新 | 注文がコマースからキャンセルされた場合、 [!DNL Channel Manager] 注文ダッシュボードの注文ステータスを更新し、顧客に通知できるように更新を Walmart marketplace に送信します。 注文のキャンセルが完了した後、 [!DNL Commerce] 返された品目を反映した在庫数量の更新 すると、 [!DNL Channel Manager] 更新を [!DNL Walmart Marketplace]. | **最大 5 分** |


