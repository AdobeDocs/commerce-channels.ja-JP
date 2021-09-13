---
title: オンボードAmazonSales Channel
description: AdobeのコマースとMagento Open Sourceの事前設定タスク、オンボーディング手順、AmazonとAmazonSales Channelの連携について説明します。
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Amazonの販売チャネルのオンボーディング

ここでは、事前設定タスク、オンボーディング手順、AmazonがAdobeコマースおよびMagento Open SourceのAmazonセールスチャネルと連携する方法に関する主な概念について説明します。

[!DNL Amazon Sales Channel]拡張機能は、複数のAmazonストアをサポートします。 Amazon U.S./Canada/Mexico地域で稼働する1つの[!DNL Amazon Seller Central]アカウントに対して、Amazonの店舗を3店舗（米国の販売店、メキシコの販売店、カナダの販売店それぞれ1店舗）を作成します。 3つの店舗のそれぞれが、市場の国を定義します。 複数の[!DNL Amazon Seller Central]アカウントがある場合、 [!DNL Amazon Seller Central]アカウントごとに最大3つのAmazonストアが存在する可能性があります。 イギリスでも売れば、4店舗目のAmazon店を持つ。

>[!TIP]
>
>北米またはヨーロッパ(UK)地域の[!DNL Amazon Seller Central]に、プロフェッショナルセラーアカウント[{target=&quot;_blank&quot;}が必要です。 ](https://sell.amazon.com/)Amazonは月々の購読と販売料を請求します。 [Amazon:販売計画](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.<br><br>を選択します。
>オンボーディングは簡単です。ストアを作成し、[!DNL Amazon Seller Central]アカウントに接続します。
>ストアに接続すると、Amazonチャネルは、[属性マッピング](./attributes-view.md).<br><br>に基づいて、Amazonのリストを読み込み、カタログと照合しようとします
>Amazonの販売チャネル設定は、Amazonのリストに影響します。 初期のリスト、価格、製品設定はデフォルトで設定されます。 ストアが[!DNL Amazon Seller Central]アカウントに接続されたら、[ストア設定](./ob-store-review.md)（リスト、価格、注文、およびレポート）を変更できます。

| 手順 | 動作 |
|--- |--- |
| [事前設定タスク](./amazon-pre-setup-tasks.md) | オンボーディングする前に、アクティブで承認済みの[!DNL Amazon Seller Central]アカウントがあることを確認する必要があります。 また、オンボーディングの前に完了する必要がある[!DNL Commerce]要件と推奨事項もいくつかあります。 |
| [Amazon APIキーの検証](./amazon-verify-api-key.md) | Amazonの販売チャネルにアクセスする場合、[!DNL Commerce]はストア設定に追加したAmazon APIキーを自動的に確認し、検証します。 APIキーが追加されていないか無効な場合は、Amazon APIキー](./amazon-verify-api-key.md)を追加または更新するよう求めるプロンプトが表示されます。[ |
| [ストア統合](./store-integration.md) | この手順では、Amazonセールスチャネルストアを作成し、[!DNL Amazon Seller Central]アカウントに接続する方法について説明します。 この手順では、[!DNL Amazon Seller Central]アカウント（販売者アカウントの作成に使用する電子メールまたは電話）のプライマリログイン資格情報が必要です。 |
| [リストルールの作成](./ob-create-listing-rule.md) | Amazon Sales Channel Storeに接続すると、リストルールを作成するよう求められます。 この手順は推奨されますが、スキップしてリストインポート処理を開始することもできます。 また、ストア[にアクセスし、ストア[ダッシュボード](./amazon-store-dashboard.md)の設定](./ob-store-review.md)をリストすることもできます。 |
