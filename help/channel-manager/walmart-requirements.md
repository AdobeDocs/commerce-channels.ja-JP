---
title: '"[!DNL Walmart] 要件»'
description: 「必要な[!DNL Walmart Marketplace]Channel Manager と統合するための情報およびリソースです。」
exl-id: c4f247e8-280a-4595-a6c8-cf8b732d7aab
source-git-commit: fffbdac54443b7b9bed8854eba8341446e78cc80
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# [!DNL Walmart] 要件

[!DNL Channel Manager] を設定するには、次のリソースと情報が必要です。 [!DNL Commerce] ～の販売チャネル [!DNL Walmart Marketplace.]

* 販売の承認 [!DNL Walmart] および登録済みの Marketplace Seller アカウントにログインするための資格情報

* Adobe CommerceまたはMagento Open Sourceの接続先となる API キー [!DNL Walmart Marketplace]

   この [!DNL Walmart Marketplace] API キーにより、 [!DNL Channel Manager] Adobe CommerceやMagento Open Sourceやウォルマート・マーケットプレイスの チャネルマネージャのオンボーディングプロセスを開始する前に、Seller Central で API キーを設定します。

## Marketplace セラーアカウントを設定する

1. [Walmart Seller の申し込みを送信](https://marketplace-apply.walmart.com/apply?id=0014M00001zivMpQAI).
1. から承認を得た後 [!DNL Walmart], [ウォルマート販売者アカウントを設定する](https://sellerhelp.walmart.com/seller/s/guide?article=000008219).

## を生成する [!DNL Walmart Marketplace] 実稼動 API キー

1. に移動します。 [!DNL Walmart Marketplace]を生成する [Adobe用のソリューションプロバイダー実稼動 API キー](https://developer.walmart.com/#preloginModal?redirectUri=https%3A%2F%2Fdeveloper.walmart.com%2Faccount%2FgenerateKey).

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

## [!DNL Walmart Marketplace] ストアのステータス

製品を Marketplace に公開する際に使用できるリストは、 [!DNL Walmart Marketplace] ストア：

* ライブストアの場合は、製品オファーが一覧表示され、一致操作が完了したときに販売できます。

* ライブでないストアの場合、製品オファーはステージングされ、顧客には表示されません。 次の場合に [!DNL Walmart Marketplace] ストアはライブになり、ステージングされたリストは自動的にライブストアにプッシュされます。

![[!DNL Walmart Seller Central] 段階別製品](assets/walmart-seller-central-staged.png)
