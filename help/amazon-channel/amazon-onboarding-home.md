---
title: '"オンボード [!DNL Amazon Sales Channel]“'
description: 事前設定タスク、オンボーディング手順、AmazonがAdobe CommerceとMagento Open SourceでAmazonSales Channelと連携する方法について説明します。
role: Leader, Admin, User
feature: Sales Channels, Integration, Tools and External Services
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 6321f17c0e6f9e86bb3f5755dc7710fa68d68b0d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Onboard [!DNL Amazon Sales Channel]

ここでは、事前設定タスク、オンボーディング手順、Adobe CommerceとMagento Open SourceでAmazonがAmazon セールスチャネルと連携する仕組みについての主要な概念について説明します。

この [!DNL Amazon Sales Channel] 拡張機能は、複数のAmazon ストアをサポートします。 シングルの場合 [!DNL Amazon Seller Central] Amazon米国/カナダ/メキシコ地域で運営されるアカウントでは、Amazonの 3 つの店舗（米国売上高、メキシコ売上高、カナダ売上高のそれぞれに 1 つずつ）を作成します。 3 つのストアのそれぞれは、作成時にマーケットプレイスの国を定義します。 2 つ以上の場合 [!DNL Amazon Seller Central] アカウントに追加する場合、各Amazon ストアを最大 3 つ作成できます [!DNL Amazon Seller Central] アカウント。 イギリスでも売れば、4 つ目のAmazon店ができますよ。

>[!TIP]
>
>A [プロの販売者アカウント](https://sell.amazon.com/){target="_blank"} 日付： [!DNL Amazon Seller Central] 北米またはヨーロッパ（英国）地域は必須です。 Amazonでは、月額利用料と販売価格を請求します。 参照： [Amazon：販売プランを選択します](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>オンボーディングは簡単です。ストアを作成して、次にストアに接続します [!DNL Amazon Seller Central] アカウント。
>ストアが接続されると、Amazon チャネルは、Amazonのリストを読み込み、それに基づいてカタログと照合しようとします [属性マッピング](./attributes-view.md).<br><br>
>Amazonの販売チャネルの設定は、Amazonのリストに影響を与えます。 最初のリスト、価格および製品設定がデフォルトになります。 を変更できます [ストアの設定](./ob-store-review.md) ストアがユーザーに接続された後のリスト、価格設定、注文、レポート [!DNL Amazon Seller Central] アカウント。

| 手順 | 結果 |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [事前設定タスク](./amazon-pre-setup-tasks.md) | オンボードする前に、がアクティブで承認済みであることを確認する必要があります [!DNL Amazon Seller Central] アカウント。 他にもいくつかあります [!DNL Commerce] オンボーディング前に完了すべき要件と推奨事項です。 |
| [Amazon API キーの確認](./amazon-verify-api-key.md) | Amazon Sales Channel にアクセスする場合、 [!DNL Commerce] ストア設定に追加したAmazon API キーを自動的にチェックし検証します。 API キーが追加されていないか無効な場合は、次の操作を実行するように求められます。 [Amazon API キーを追加または更新](./amazon-verify-api-key.md). |
| [ストアの統合](./store-integration.md) | この手順には、Amazonのセールスチャネルストアを作成し、それをに接続することが含まれます [!DNL Amazon Seller Central] アカウント。 のプライマリログイン資格情報が必要です [!DNL Amazon Seller Central] この手順のアカウント （販売者アカウントの作成に使用される電子メールまたは電話）。 |
| [リストルールの作成](./ob-create-listing-rule.md) | Amazonのセールスチャネルストアに接続すると、リストルールを作成するよう求められます。 この手順は推奨されますが、スキップしてリストの読み込みプロセスを開始することもできます。 にアクセスすることもできます [ストアとリストの設定](./ob-store-review.md) 店舗で [dashboard](./amazon-store-dashboard.md). |
