---
title: '概要  [!DNL Channel Manager]'
description: Adobe CommerceとMagento Open Sourceストアを Walmart Marketplace と統合し、マーケットプレイスのリスト、価格、在庫、売上をCommerce管理者からシームレスに管理する営業チャネルを作成するためのインストールおよび使用方法に  [!DNL Channel Manager]  いて説明します。」
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# [!DNL Channel Manager] の概要

[!DNL Channel Manager] は、Adobe CommerceまたはMagento Open Sourceの製品カタログを [!DNL Walmart Marketplace] と統合することで、マーチャントの売上の増加、新規顧客へのリーチ、営業業務の合理化、時間の節約を支援します。

拡張機 ![[!DNL Channel Manager] の管理者表示 ](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] は、[!DNL Commerce] Admin を拡張することで、[!DNL Walmart Marketplace] で販売を行うAdobe CommerceまたはMagento Open Sourceマーチャントをサポートしています。 [!DNL Channel Manager] をインストールすると、店舗管理者や運営スタッフは、Commerce環境から [!DNL Walmart Marketplace] 売、在庫、商品の価格をシームレスに管理できます。

拡張された管理者は、マーチャントが同じワークフローとプロセスを使用して、ストアフロントと Walmart Marketplace の両方から販売を管理でき [!DNL Commerce] ので、操作を合理化します。

[!DNL Channel Manager] をインストールして構成した後、次の機能を使用して Walmart Marketplace の受注を管理できます。

* **リスト管理** – 製品カタログの製品を既存のリストに一致させることで、製 [!DNL Commerce] リストを簡単に接続 [!DNL Walmart Marketplace] ます。

* **Inventory management** – 正確な在庫レベルを確保するために、マーケットプレイスの販売者アカウントの商品は [!DNL Commerce] から自動的に同期および更新されます。

* **価格の更新**：自動的な価格の同期により、マーケットプレイス・リストの正確な価格を維持します。 Adobe Commerceで価格が変更されると、その変更がマーケットプレイスに反映されます。

* **Order Management**:Marketplace で新しい注文が作成されると、[!DNL Channel Manager] は注文をAdobe Commerceと同期し、注文確認を Marketplace に送信します。 この確認により、在庫が注文ごとに予約されます。 最後の手順では、対応するオーダーを [!DNL Commerce] Order Management システムで作成して処理します。

* **出荷管理** - Adobe Commerceで受注が出荷済としてマークされると、出荷更新が [!DNL Walmart Marketplace] に送信されます。 この通知により、セラーはフルフィルメントの SLA 要件を満たし、顧客は現在の注文に関する出荷更新通知を受け取ることができます。

* **キャンセル** - Adobe Commerceで注文がキャンセルされると、[!DNL Channel Manager] は、更新された注文情報をマーケットプレイスに送信して、対応するマーケットプレイスの注文に対してアクションをレプリケートします。 注文のキャンセルが完了すると、返品された品目を反映するように [!DNL Commerce] の在庫数量が更新され、在庫の更新が [!DNL Walmart Marketplace] に自動的に同期されます。

* **返品と払い戻し** - Walmart Marketplace がAdobe CommerceまたはMagento Open Source営業チャンネルを通じて注文された商品の返品をリクエストする [!DNL Channel Manager]、返品リクエスト情報をCommerce営業チャンネル店に送信して返品リクエストを複製します。 その後、[!DNL Commerce][ 返金ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow)、オフラインメソッドを使用して払い戻しを処理できます。 払い戻しが完了した後、[!DNL Channel Manager] は更新をウォルマートに同期して、マーケットプレイスの販売者アカウントの返品ステータスを更新して払い戻しを反映させることができます。

## [!DNL Channel Manager] 操作で予想される遅延

[!DNL Channel Manager] とリンクされた [!DNL Walmart Marketplace] ストアの間のデータ同期処理には、完了までにある程度の時間が必要です。 販売チャネルのオペレーション作業の計画に役立てるため、[!DNL Channel Manager] オペレーションの予想処理時間を確認します。

**[!DNL Channel Manager] 操作の推定待ち時間**

| **操作** | **説明** | **予想される遅延** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [!DNL Channel Manager] への製品の追加 | [!DNL Commerce] 製品カタログから製品を選択して、[!DNL Channel Manager] に読み込みます。 | **最大 5 分** – 製品カタログ全体など、多数の製品を選択した場合は、読み込み処理に時間がかかります。 |
| [!DNL Walmart Marketplace] で製品を照合 | [!DNL Channel Manager] で商品リストを選択し、マッチングのためにウォルマートに送信します。 | **最大 30 分** – 多くの製品を選択する場合、選択する数量によっては、照合プロセスに時間がかかります。 |
| インベントリの更新 | Commerceで在庫数量が変更されると、[!DNL Channel Manager] は更新をウォルマートに同期します。 | **最大 10 分** |
| 価格アップデート | 製品価格が変更されると、[!DNL Channel Manager] は更新をウォルマートに同期します。 | **最大 5 分** |
| ウォルマートから [!DNL Commerce] への同期の注文 | 顧客はウォルマートのマーケットプレイスで [!DNL Commerce] 製品を注文します。 ウォルマートが注文を [!DNL Channel Manager] に送る。 順序ダッシュボードに順序が表示されます。 | **最大 30 分** |
| [!DNL Commerce] Order Managementで作成された注文 | [!DNL Channel Manager] は、ウォルマート注文から [!DNL Commerce] 注番号を作成し、[!DNL Commerce] 注番号を含むように注文ダッシュボードを更新します。 | **最大 5 分** |
| Order Managementでの配送ステータス [!DNL Commerce] 更新 | 注文がCommerceから発送されると、[!DNL Channel Manager] は注文ダッシュボードの配送ステータスを更新し、更新をウォルマートの Marketplace に送信して、お客様に通知できるようにします。 | **最大 5 分** |
| Commerce Order Managementでの注文キャンセルの更新 | 注文がCommerceからキャンセルされると、[!DNL Channel Manager] は注文ダッシュボードの注文ステータスを更新し、顧客に通知できるように更新をウォルマート Marketplace に送信します。 注文のキャンセルが完了すると、[!DNL Commerce] の在庫数が更新され、返品された品目が反映されます。 次に、[!DNL Channel Manager] が更新を [!DNL Walmart Marketplace] に同期します。 | **最大 5 分** |


