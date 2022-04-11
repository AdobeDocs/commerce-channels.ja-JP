---
title: ウォルマートの前提条件
description: Channel Manager と統合するために必要な Walmart Marketplace 情報とリソースが揃っていることを確認します。
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ウォルマートの前提条件

チャネルマネージャーで Walmart Marketplace 用に Commerce 販売チャネルを設定するには、次のリソースと情報が必要です。

* 登録済み Marketplace セラーアカウントにログインするためのウォルマートでの販売の承認と資格情報

* Adobe CommerceまたはMagento Open Sourceを Walmart Marketplace に接続するための API キー

   Walmart Marketplace API キーは、Adobe CommerceまたはMagento Open Sourceのチャネルマネージャーとウォルマートマーケットプレイスとの統合を可能にします。 チャネルマネージャのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

## Marketplace セラーアカウントを設定する

1. [Walmart Seller の申し込みを送信](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. ウォルマートから承認を得て [ウォルマート販売者アカウントを設定する](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## Walmart Marketplace Production API キーを生成

1. Walmart Marketplace に移動して、 [Adobe用のソリューションプロバイダー実稼動 API キー](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. キーを作成し、権限を設定します。

   * ソリューションプロバイダーとして「Adobe」を選択します。

   * 次の表に示すように、権限を設定します。 詳しくは、 [API 資格情報](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) 内 _Walmart Marketplace セラーヘルプ_.

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

* ライブストアの場合は、製品オファーが一覧表示され、一致操作が完了したときに販売できます。

* ライブでないストアの場合、製品オファーはステージングされ、顧客には表示されません。 ストアがライブになると、ステージングされたリストがライブストアに自動的にプッシュされます。

![[!DNL Walmart Seller Central] 段階別製品](assets/walmart-seller-central-staged.png)
