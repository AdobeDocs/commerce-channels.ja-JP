---
title: '概要 [!DNL Channel Manager]'
description: '''インストール方法と使用方法を学ぶ [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceストアを Walmart Marketplace と統合し、マーケットプレイスのリスト、価格設定、在庫、売上をCommerce管理者からシームレスに管理できるセールスチャネルを作成するには、こちらを参照してください。'
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# の概要 [!DNL Channel Manager]

[!DNL Channel Manager] は、Adobe CommerceまたはMagento Open Sourceの製品カタログとを統合することで、マーチャントが売上の増加、新規顧客へのリーチ、営業業務の合理化、時間の節約を支援します [!DNL Walmart Marketplace].

![[!DNL Channel Manager] 拡張機能の管理者ビュー](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] は、での販売を希望するAdobe CommerceまたはMagento Open Sourceマーチャントをサポートします [!DNL Walmart Marketplace] を拡張して [!DNL Commerce] 管理者。 （を使用） [!DNL Channel Manager] インストール済み、ストア管理者、および運用スタッフが管理可能 [!DNL Walmart Marketplace] Commerce環境からシームレスに販売、在庫、商品の価格を決定します。

拡張された管理者は、マーチャントが同じワークフローとプロセスを使用して両方からの販売を管理できるので、操作を合理化します [!DNL Commerce] ストアフロントとウォルマート マーケットプレイス。

インストールおよび設定後 [!DNL Channel Manager]では、次の機能を使用して Walmart Marketplace の受注を管理できます。

* **リスト管理** – 製品リストを自分の製品と簡単に関連付ける [!DNL Commerce] カタログを既存のものに [!DNL Walmart Marketplace] listings.

* **Inventory management** – マーケットプレイスの販売者アカウントにある商品は、自動的に同期され、次から更新されます。 [!DNL Commerce] 正確な在庫レベルを確保する。

* **価格の更新** – 自動的な価格同期により、マーケットプレイス・リストの正確な価格設定を維持します。 Adobe Commerceで価格が変更されると、その変更がマーケットプレイスに反映されます。

* **注文管理** – マーケットプレイスで新しい注文が作成されると、 [!DNL Channel Manager] 注文をAdobe Commerceと同期し、注文確認を marketplace に送信します。 この確認により、在庫が注文ごとに予約されます。 最後の手順では、対応するオーダーをに作成します。 [!DNL Commerce] 処理のための注文管理システム。

* **出荷管理**—Adobe Commerceで注文が出荷済みとしてマークされると、出荷更新がに送信されます [!DNL Walmart Marketplace]. この通知により、セラーはフルフィルメントの SLA 要件を満たし、顧客は現在の注文に関する出荷更新通知を受け取ることができます。

* **キャンセル**—Adobe Commerceで注文がキャンセルされた場合、 [!DNL Channel Manager] 更新された注文情報をマーケットプレイスに送信して、対応するマーケットプレイスの注文のアクションをレプリケートします。 注文のキャンセルが完了すると、 [!DNL Commerce] 返品された品目を反映するための在庫数量の更新と、在庫の更新は自動的にに同期されます。 [!DNL Walmart Marketplace].

* **返品および返金**—Walmart Marketplace が、Adobe CommerceまたはMagento Open Sourceのセールス・チャネルを通じて注文された商品の返品をリクエストする場合、 [!DNL Channel Manager] 返品リクエスト情報をCommerce sales channel store に送信して、返品リクエストをレプリケートします。 その後、払い戻しは [!DNL Commerce] [返金ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow)、オフラインメソッド。 払い戻し完了後、 [!DNL Channel Manager] 更新をウォルマートに同期して、マーケットプレイスの販売者アカウントの返品ステータスを更新して払い戻しを反映できるようにします。

## の予想待ち時間 [!DNL Channel Manager] の操作

データ同期は、次の期間を処理します [!DNL Channel Manager] およびリンクされた [!DNL Walmart Marketplace] ストアの完了には時間がかかります。 の予想処理時間をレビューします [!DNL Channel Manager] 販売チャネルのオペレーション作業を計画するのに役立つオペレーション。

**推定待ち時間 [!DNL Channel Manager] の操作**

| **操作** | **説明** | **予想される遅延** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| への製品の追加 [!DNL Channel Manager] | から製品を選択 [!DNL Commerce] 製品カタログおよびへの読み込み [!DNL Channel Manager]. | **最大 5 分** – 製品カタログ全体など、多数の製品を選択した場合は、読み込み処理に時間がかかります。 |
| 次の商品と一致 [!DNL Walmart Marketplace] | の製品リストの選択 [!DNL Channel Manager] ウォルマートに送ってマッチングを行う。 | **最大 30 分**・複数製品を選択した場合、選択した数量によっては、照合に時間がかかります。 |
| インベントリの更新 | Commerceで在庫数量が変更された場合、 [!DNL Channel Manager] 更新をウォルマートに同期します。 | **最大 10 分** |
| 価格アップデート | 製品価格が変更された場合、 [!DNL Channel Manager] 更新をウォルマートに同期します。 | **最大 5 分** |
| ウォルマートから次に同期を注文 [!DNL Commerce] | 顧客からの注文 a [!DNL Commerce] ウォルマートマーケットプレイスに掲載されている商品。 ウォルマートが注文を送信： [!DNL Channel Manager]. 順序ダッシュボードに順序が表示されます。 | **最大 30 分** |
| 注文の作成場所 [!DNL Commerce] オーダー管理 | [!DNL Channel Manager] が [!DNL Commerce] ウォルマート注文からの注文し、注文ダッシュボードを更新してを含めます [!DNL Commerce] オーダー番号。 | **最大 5 分** |
| での出荷ステータスの更新 [!DNL Commerce] オーダー管理 | 注文がCommerceから出荷された場合、 [!DNL Channel Manager] 注文ダッシュボードの配送状況を更新し、その更新をウォルマートのマーケットプレイスに送信して、顧客に通知できるようにします。 | **最大 5 分** |
| Commerce Order Management での注文キャンセルの更新 | Commerceから注文がキャンセルされた場合、 [!DNL Channel Manager] 注文ダッシュボードの注文ステータスを更新し、顧客に通知できるよう更新をウォルマート Marketplace に送信します。 注文のキャンセルが完了すると、 [!DNL Commerce] 在庫数が更新され、返された項目が反映されます。 その後、 [!DNL Channel Manager] 更新内容をに同期します [!DNL Walmart Marketplace]. | **最大 5 分** |


