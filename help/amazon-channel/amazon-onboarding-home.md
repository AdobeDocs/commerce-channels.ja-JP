---
title: Onboard AmazonSales Channel
description: Adobe CommerceとMagento Open Sourceの事前設定タスク、オンボーディング手順、AmazonとAmazonSales Channelの連携方法について説明します。
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Onboard AmazonSales Channel

ここでは、Adobe CommerceおよびMagento Open SourceのAmazonセールスチャネルとの連携に関する、事前設定タスク、オンボーディング手順、主な概念について説明します。

この [!DNL Amazon Sales Channel] 拡張機能は、複数のAmazonストアをサポートしています。 単一の [!DNL Amazon Seller Central] Amazon U.S./Canada/Mexico 地域で運営するアカウントで、Amazonの店舗を 3 店舗（米国の販売、メキシコの販売、カナダの販売それぞれ 1 店舗）を作成します。 3 つの店舗のそれぞれが、作成時の市場の国を定義します。 複数の [!DNL Amazon Seller Central] アカウントには、それぞれ最大 3 つのAmazonストアが存在する可能性があります [!DNL Amazon Seller Central] アカウント。 イギリスでも売れば、4 店舗目のAmazon店を持つ。

>[!TIP]
>
>A [Professional Seller アカウント](https://sell.amazon.com/){target="_blank"} on [!DNL Amazon Seller Central] in the North America or European (UK) region is required. Amazon charges a monthly subscription and fees for selling. See [Amazon: Choose your selling plan](https://sell.amazon.com/pricing.html){target="_blank"}.<br><br>
>オンボーディングは簡単です。ストアを作成してから、 [!DNL Amazon Seller Central] アカウント
>ストアに接続すると、AmazonチャネルはAmazonの一覧を読み込み、ユーザーのカタログと照合しようとします。 [属性マッピング](./attributes-view.md).<br><br>
>Amazonのセールスチャネルの設定は、Amazonのリストに影響します。 初期のリスト、価格、製品設定はデフォルトで設定されます。 次の項目を変更できます： [ストア設定](./ob-store-review.md) ストアが [!DNL Amazon Seller Central] アカウント

| 手順 | 結果 |
|--- |--- |
| [事前設定タスク](./amazon-pre-setup-tasks.md) | オンボーディングする前に、アクティブで承認済みであることを確認する必要があります [!DNL Amazon Seller Central] アカウント また、 [!DNL Commerce] オンボーディングの前に完了する必要がある要件と推奨事項。 |
| [Amazon API キーの確認](./amazon-verify-api-key.md) | Amazonセールスチャネルにアクセスする場合、 [!DNL Commerce] は、ストア設定に追加したAmazon API キーを自動的に確認して検証します。 API キーが追加されていないか無効な場合は、 [Amazon API キーの追加または更新](./amazon-verify-api-key.md). |
| [ストア統合](./store-integration.md) | この手順では、Amazonセールスチャネルストアを作成し、それを [!DNL Amazon Seller Central] アカウント のプライマリログイン資格情報が必要です [!DNL Amazon Seller Central] この手順のアカウント（販売者アカウントの作成に使用する電子メールまたは電話）。 |
| [リストルールを作成](./ob-create-listing-rule.md) | Amazonセールスチャネルストアに接続すると、リストルールを作成するよう求められます。 この手順は推奨されますが、スキップして読み込みのリストを開始することもできます。 また、 [ストアとリストの設定](./ob-store-review.md) 店で [dashboard](./amazon-store-dashboard.md). |
