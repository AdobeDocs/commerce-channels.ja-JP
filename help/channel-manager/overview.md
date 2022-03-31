---
title: について [!DNL Channel Manager]
description: インストールと使用の方法を学ぶ [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceストアをサードパーティのマーケットプレイスと統合し、販売チャネルを作成して、コマース管理者からシームレスにマーケットプレイスリスト、価格、在庫、販売を管理します。
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ac084bf968a262dd4e7f6b6040aea2e6dc6197c2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# 概要

Adobe CommerceとMagento Open Sourceの Channel Manager は、Walmart、Amazon、eBay などのサードパーティマーケットプレイスでチャネル販売を管理するための、管理者の便利なワークスペースを提供します。 コマース管理者からセールスチャネルの運営をシームレスに管理しながら、セールスを増やし、新しい市場へと展開します。

![[!DNL Channel Manager] 拡張機能の管理ビュー](assets/channel-manager-admin-entry-page.png)

## ベータリリースの概要

Channel Manager のベータリリースでは、Walmart Marketplace で製品を提供するAdobe CommerceまたはMagento Open Sourceセラーがサポートされています。

このリリースでは、セールスチャネルの運用を管理する次の機能がサポートされています。

* Adobe CommerceまたはMagento Open Sourceと Walmart Marketplace 間の API 接続の確立

* 製品マッチングを使用して、Channel Manager から Walmart に製品を公開

* チャネルマネージャーでの製品リストのステータスの表示（例： ） *ドラフト*, *処理中*, *一致*, *エラー*.

* Commerce から Walmart に一致製品の在庫数量を同期

* 一致した製品のカタログ価格をコマースからウォルマートに同期

* Walmart Marketplace から注文を受け取り、 [!DNL Commerce] 注文ダッシュボード

### Channel Manager の操作で予想される遅延

次の間のデータ同期プロセス： [!DNL Channel Manager] リンクされた [!DNL Walmart Marketplace] ストアが完了するまでにしばらく時間が必要です。 次の予定処理時間を確認 [!DNL Channel Manager] 営業チャネルの運用を計画する際に役立つ操作です。

**Channel Manager 操作の推定待ち時間**

| **操作** | **説明** | **予想される遅延** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| チャネルマネージャーへの製品の追加 | コマース製品カタログから製品を選択し、チャネルマネージャに読み込みます。 | **最大 5 分** — 製品カタログ全体など、多数の製品を選択した場合、読み込み処理に時間がかかります。 |
| Walmart Marketplace での製品のマッチング | チャネルマネージャで製品リストを選択し、ウォルマートに送信して照合します。 | **最大 30 分** — 多数の製品を選択した場合、選択した数量に応じて、照合の処理に時間がかかります。 |
| 在庫の更新 | Commerce で在庫数量が変更された場合。 Channel Manager は Walmart に同期します。 | **最大 10 分** |
| 価格の更新 | 製品価格が変更されると、Channel Manager は Walmart に更新を同期します。 | **最大 5 分** |
| ウォルマートからコマースへの同期の注文 | お客様がウォルマートマーケットプレイスでコマース製品を注文します。 ウォルマートが注文をチャネルマネージャに送信します。 注文は注文ダッシュボードに表示されます。 | **最大 30 分** |
| Commerce Order Management で作成された注文 | Channel Manager は、ウォルマート注文からコマース注文を作成し、注文ダッシュボードを更新してコマース注文番号を含めます。 | **最大 5 分** |

## ウォルマートの前提条件

コマースを Walmart Marketplace と統合するには、以下の Walmart からの情報が必要です。

* 登録済み Marketplace セラーアカウントにログインするためのウォルマートでの販売の承認と資格情報

* Adobe CommerceまたはMagento Open Sourceを Walmart Marketplace に接続するための API キー

   Walmart Marketplace API キーは、Adobe CommerceまたはMagento Open Sourceのチャネルマネージャーとウォルマートマーケットプレイスとの統合を可能にします。 チャネルマネージャのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

### Marketplace セラーアカウントを設定する

1. [Walmart Seller の申し込みを送信](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI)
2. ウォルマートから承認を得て [ウォルマート販売者アカウントを設定する](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

### Walmart Marketplace API キーを生成

1. Walmart Marketplace に移動して、 [Adobe用のソリューションプロバイダー実稼動 API キー](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. キーを作成し、権限を設定します。

   * ソリューションプロバイダーとして「Adobe」を選択します。

   * 次の表に示すように、権限を設定します。 詳しくは、 [API 資格情報](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 内 *Walmart Marketplace セラーヘルプ*.

   **AdobeAPI の Walmart のキー設定**

   | **権限** | **設定** |
   |----------------|-------------|
   | コンテンツ | フルアクセス |
   | フィードの取得 | 表示のみ |
   | 在庫 | フルアクセス |
   | 項目 | フルアクセス |
   | ラグタイム | フルアクセス |
   | 注文 | フルアクセス |
   | 価格 | フルアクセス |
   | レポート | 表示のみ |
   | 戻り値 | フルアクセス |
   | ルール | フルアクセス |
   | 送料 | フルアクセス |

## ウォルマートマーケットプレイスストアのステータス

製品を Walmart Marketplace に発行する場合、リストの可用性は Walmart Marketplace ストアのステータスによって異なります。

* ライブストアの場合は、製品オファーが一覧表示され、一致操作が完了するとすぐに販売できます。

* ライブでないストアの場合、製品オファーはステージングされ、顧客には表示されません。 ストアがライブになるとすぐに、ステージングされたリストがライブストアに自動的にプッシュされます。


![[!DNL Walmart Seller Central] 段階別製品](assets/walmart-seller-central-staged.png)
