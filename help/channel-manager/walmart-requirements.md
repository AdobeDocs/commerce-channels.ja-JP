---
title: '[!DNL Walmart] 要件'
description: '''が必要であることを確認します [!DNL Walmart Marketplace]チャネルマネージャーと統合するための情報とリソース。'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!DNL Walmart] 要件

[!DNL Channel Manager] の設定には、以下のリソースと情報が必要です。 [!DNL Commerce] の販売チャネル [!DNL Walmart Marketplace.]

* A [!DNL Walmart] 販売者アカウント

* Adobe CommerceまたはMagento Open Sourceを接続するための API キー [!DNL Walmart Marketplace]

  この [!DNL Walmart Marketplace] API キーにより、 [!DNL Channel Manager] Adobe用 [!DNL Commerce] またはMagento Open Sourceとウォルマート・マーケットプレイス。 チャネルマネージャーのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

## を設定 [!DNL Walmart Seller] アカウント

に移動します [!DNL Walmart Seller Center] を設定するには [ウォルマート販売者アカウント](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

## を生成 [!DNL Walmart Marketplace] 実稼動 API キー

1. に移動 [!DNL Walmart Marketplace] を生成するには [Adobe用のソリューションプロバイダー実稼動 API キー](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

1. キーを作成し、権限を設定します。

   * ソリューションプロバイダーとして「Adobe」を選択します。

   * 次の表に示すように、権限を設定します。 詳しくは、を参照してください [API 資格情報](https://sellerhelp.walmart.com/seller/s/guide?article=000006422) が含まれる _Walmart Marketplace 販売者ヘルプ_.

   **ウォルマートのAdobeAPI キーの設定**

   | **権限** | **設定** |
   |----------------|-------------|
   | コンテンツ | フルアクセス |
   | フィードを取得 | 表示のみ |
   | 在庫 | フルアクセス |
   | 項目 | フルアクセス |
   | 間隔時間 | フルアクセス |
   | 順序 | フルアクセス |
   | 価格 | フルアクセス |
   | レポート | 表示のみ |
   | 戻り値 | フルアクセス |
   | ルール | フルアクセス |
   | 送料 | フルアクセス |

## [!DNL Walmart Marketplace] ストアステータス

製品を Marketplace に接続する場合、リストを利用できるかどうかは、のステータスによって異なります [!DNL Walmart Marketplace] ストア：

* ライブストアの場合、製品オファーが一覧表示され、一致操作が完了すると販売できます。

* ライブではないストアの場合、製品オファーはステージングされ、顧客には表示されません。 いつ [!DNL Walmart Marketplace] ストアがライブになると、ステージングされたリストは自動的にライブストアにプッシュされます。

![[!DNL Walmart Seller Central] ステージングされた製品](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>後 [!DNL Channel Manager] はインストールおよび設定され、すべての在庫、価格、注文の更新は自動的に同期されます。 接続しない [!DNL Channel Manager] 製品と注文データを更新する他の統合を無効にするまで、ライブのウォルマート マーケットプレイス ストアに移動します。 他の統合が設定されている場合は、で項目数と価格を確認します。 [!DNL Commerce] ～の数量に一致する [!DNL Walmart Marketplace] ライブストアに接続する前に。

