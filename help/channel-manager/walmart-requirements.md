---
title: '''[!DNL Walmart] 要件`'
description: '必要な [!DNL Walmart Marketplace]Channel Manager と統合するための情報およびリソースです。'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Walmart] 要件

[!DNL Channel Manager] を設定するには、次のリソースと情報が必要です。 [!DNL Commerce] ～の販売チャネル [!DNL Walmart Marketplace.]

* A [!DNL Walmart] 販売者アカウント

* Adobe CommerceまたはMagento Open Sourceの接続先となる API キー [!DNL Walmart Marketplace]

  The [!DNL Walmart Marketplace] API キーにより、 [!DNL Channel Manager] Adobe [!DNL Commerce] Magento Open Sourceとウォルマート・マーケットプレイス チャネルマネージャのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

## を設定します。 [!DNL Walmart Seller] アカウント

次に移動： [!DNL Walmart Seller Center] を設定するには、 [Walmart Seller アカウント](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## を生成する [!DNL Walmart Marketplace] 実稼動 API キー

1. に移動します。 [!DNL Walmart Marketplace] を生成する [Adobe用のソリューションプロバイダー実稼動 API キー](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. キーを作成し、権限を設定します。

   * ソリューションプロバイダーとして「Adobe」を選択します。

   * 次の表に示すように、権限を設定します。 詳しくは、 [API 資格情報](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) （内） _Walmart Marketplace セラーヘルプ_.

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

## [!DNL Walmart Marketplace] ストアのステータス

製品を Marketplace に接続する場合、リストの可用性は [!DNL Walmart Marketplace] ストア：

* ライブストアの場合は、製品オファーが一覧表示され、一致操作が完了したときに販売できます。

* ライブでないストアの場合、製品オファーはステージングされ、顧客には表示されません。 次の場合に [!DNL Walmart Marketplace] ストアはライブになり、ステージングされたリストは自動的にライブストアにプッシュされます。

![[!DNL Walmart Seller Central] 段階別製品](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>後 [!DNL Channel Manager] がインストールおよび設定されると、在庫、価格、注文の更新がすべて自動的に同期されます。 接続しない [!DNL Channel Manager] を Walmart Marketplace のライブストアに追加します。 他の統合を設定していた場合は、 [!DNL Commerce] ～の量に合う [!DNL Walmart Marketplace] ライブストアに接続する前に。

