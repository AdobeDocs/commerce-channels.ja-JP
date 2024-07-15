---
title: '[!DNL Walmart] 要件'
description: 'チャネルマネージャーと統合するために必要な情報およびリソースが  [!DNL Walmart Marketplace] っていることを確認します。'
role: Leader, Admin, Developer
feature: Sales Channels, Install, User Account, Tools and External Services
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# [!DNL Walmart] 要件

[!DNL Channel Manager] で [!DNL Walmart Marketplace.] の [!DNL Commerce] しい販売チャネルを設定するには、次のリソースと情報が必要です

* [!DNL Walmart] 売りアカウント

* Adobe CommerceまたはMagento Open Sourceを [!DNL Walmart Marketplace] に接続するための API キー

  [!DNL Walmart Marketplace] API キーを使用すると、Adobe[!DNL Commerce] ースまたはMagento Open Sourceの [!DNL Channel Manager] と Walmart Marketplace の連携が可能になります。 チャネルマネージャーのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

## [!DNL Walmart Seller] アカウントの設定

[!DNL Walmart Seller Center] に移動して、[ ウォルマート販売者アカウント ](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp) を設定します。

## [!DNL Walmart Marketplace] 実稼動 API キーの生成

1. [!DNL Walmart Marketplace] に移動して、[Adobe用のソリューションプロバイダー実稼動 API キー ](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey) を生成します。

1. キーを作成し、権限を設定します。

   * ソリューションプロバイダーとして「Adobe」を選択します。

   * 次の表に示すように、権限を設定します。 詳しくは、[Walmart Marketplace 販売者ヘルプ _の ](https://sellerhelp.walmart.com/seller/s/guide?article=000006422)API 資格情報_ を参照してください。

   **ウォルマートのAdobeAPI キーの構成**

   | **許可** | **設定** |
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

製品を Marketplace に接続する場合、リストを利用できるかどうかは、[!DNL Walmart Marketplace] ストアのステータスによって異なります。

* ライブストアの場合、製品オファーが一覧表示され、一致操作が完了すると販売できます。

* ライブではないストアの場合、製品オファーはステージングされ、顧客には表示されません。 [!DNL Walmart Marketplace] ストアがライブになると、ステージングされたリストは自動的にライブストアにプッシュされます。

ステージング ![[!DNL Walmart Seller Central] れた製品 ](assets/walmart-seller-central-staged.png){width="600" zoomable="yes"}

>[!IMPORTANT]
>
>[!DNL Channel Manager] のインストールと設定が完了すると、すべての在庫、価格、注文の更新が自動的に同期されます。 製品と注文データを更新するその他の統合を無効にするまでは、[!DNL Channel Manager] をライブのウォルマート Marketplace ストアに接続しないでください。 他の統合が設定されている場合は、ライブストアに接続する前に、[!DNL Commerce] の品目の数量と価格が [!DNL Walmart Marketplace] の数量と一致していることを確認します。

