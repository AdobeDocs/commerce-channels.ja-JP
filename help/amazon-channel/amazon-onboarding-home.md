---
title: 「オンボード  [!DNL Amazon Sales Channel]」
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

[!DNL Amazon Sales Channel] 拡張機能は、複数のAmazon ストアをサポートします。 Amazon米国/カナダ/メキシコ地域で営業する [!DNL Amazon Seller Central] アカウントの場合は、Amazonに 3 つの店舗を作成します（米国売上高、メキシコ売上高、カナダ売上高に 1 つずつ）。 3 つのストアのそれぞれは、作成時にマーケットプレイスの国を定義します。 複数の [!DNL Amazon Seller Central] アカウントがある場合、[!DNL Amazon Seller Central] アカウントごとに最大 3 つのAmazon ストアを持つことができます。 イギリスでも売れば、4 つ目のAmazon店ができますよ。

>[!TIP]
>
>北米またはヨーロッパ（英国）地域の [!DNL Amazon Seller Central] の [ プロの販売者アカウント ](https://sell.amazon.com/){target="_blank"} が必要です。 Amazonでは、月額利用料と販売価格を請求します。 [Amazon：販売計画の選択 ](https://sell.amazon.com/pricing.html){target="_blank"} を参照してください。<br><br>
>オンボーディングは簡単です。ストアを作成し、[!DNL Amazon Seller Central] アカウントに接続します。
>ストアが接続されると、Amazon チャンネルは、Amazonのリストを読み込み、[ 属性マッピング ](./attributes-view.md).<br><br> に基づいてそれらをカタログに一致させようとします。
>Amazonの販売チャネルの設定は、Amazonのリストに影響を与えます。 最初のリスト、価格および製品設定がデフォルトになります。 ストアが [!DNL Amazon Seller Central] アカウントに接続されたら、[ ストアの設定 ](./ob-store-review.md) （リスト、価格、注文、レポート）を変更できます。

| 手順 | 結果 |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ 事前設定タスク ](./amazon-pre-setup-tasks.md) | オンボーディングする前に、アクティブで承認済みの [!DNL Amazon Seller Central] アカウントがあることを確認する必要があります。 また、オンボーディング前に完了すべき [!DNL Commerce] な要件と推奨事項もあります。 |
| [Amazon API キーの確認 ](./amazon-verify-api-key.md) | Amazonのセールスチャネルにアクセスする際に、[!DNL Commerce] はストア設定に追加したAmazon API キーを自動的にチェックし、検証します。 API キーが追加されていない、または無効な場合は、[Amazon API キーを追加または更新 ](./amazon-verify-api-key.md) するように求められます。 |
| [ ストアの統合 ](./store-integration.md) | この手順には、Amazon セールスチャネルストアの作成と、[!DNL Amazon Seller Central] アカウントへの接続が含まれます。 この手順を実行するには、[!DNL Amazon Seller Central] アカウントのプライマリログイン資格情報（販売者アカウントの作成に使用するメールまたは電話）が必要です。 |
| [ リストルールの作成 ](./ob-create-listing-rule.md) | Amazonのセールスチャネルストアに接続すると、リストルールを作成するよう求められます。 この手順は推奨されますが、スキップしてリストの読み込みプロセスを開始することもできます。 また、ストア [ ダッシュボード ](./amazon-store-dashboard.md) で [ ストアとリストの設定 ](./ob-store-review.md) にアクセスすることもできます。 |
