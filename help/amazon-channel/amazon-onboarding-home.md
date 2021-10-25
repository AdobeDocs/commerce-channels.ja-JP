---
title: オンボードの Amazon 販売チャンネル
description: 事前設定タスク、オンボードステップ、および、Adobe Commerce の Amazon 販売チャンネルと Amazon が Magento のオープンソースでの作業について説明します。
redirect_from: /sales-channels/amazon/amazon-onboarding-home.html
exl-id: 99b64083-36e6-442e-9d20-4676e78ec3ae
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# オンボードの Amazon 販売チャンネル

この節では、セットアップ前のタスク、オンボードの手順、および Amazon が Adobe Commerce および Magento Open Source の Amazon sales チャンネルを使用した作業について、主な概念について説明します。

拡張機能では、 [!DNL Amazon Sales Channel] 複数の Amazon stores がサポートされています。 Amazon 地方またはメキシコ地域で使用される1つのアカウントについて [!DNL Amazon Seller Central] 、amazon 店3つ (米国の売上、メキシコ販売、カナダ販売用) を作成します。 3つの各店舗は、作成時に marketplace の国を定義します。 複数のアカウントをお持ち [!DNL Amazon Seller Central] の場合は、それぞれのアカウントについて、Amazon ストアが3つまでインストールされている可能性があり [!DNL Amazon Seller Central] ます。 英国でも販売する場合は、4番目の Amazon store が表示されます。

>[!TIP]
>
>[ ](https://sell.amazon.com/) [!DNL Amazon Seller Central] 北米またはヨーロッパ (英国) 地域では、プロフェッショナルな販売店の {target = &quot;_blank&quot;} がオンになっています。Amazon は、毎月の購入料金と販売費用によって課金されます。 [Amazon: 販売プランの選択 ](https://sell.amazon.com/pricing.html) {target = &quot;_blank&quot;} を参照してください。<br><br>
>オンボードは簡単---ストアを作成して、それを [!DNL Amazon Seller Central] 取引先企業に関連付けます。
>ストアが接続されている場合、Amazon channel は、その属性マッピングに基づいて Amazon リストのインポートと、カタログとの一致を試み [ ](./attributes-view.md) ます。<br><br>
>Amazon 販売チャンネル設定は、Amazon リストに影響を与えます。 最初のリスト、価格、製品の設定がデフォルトで使用されます。 ストア [ ](./ob-store-review.md) が取引先企業に接続された後で、ストア設定 (一覧、価格、注文、レポート) を変更でき [!DNL Amazon Seller Central] ます。

| 従っ | 結果 |
|--- |--- |
| [事前設定タスク](./amazon-pre-setup-tasks.md) | Onboard を開始する前に、アクティブな承認済みアカウントがあることを確認する必要があり [!DNL Amazon Seller Central] ます。 オンボードにするには、いくつかの [!DNL Commerce] 要件や推奨事項も必要になります。 |
| [Amazon API キーを確認します。](./amazon-verify-api-key.md) | Amazon 販売チャンネルにアクセスすると、は、 [!DNL Commerce] ストア設定に追加された AMAZON API キーを自動的に確認して検証します。 API キーが追加されていないか、無効な場合は、Amazon API キーを追加または更新するよう求めるメッセージが表示され [ ](./amazon-verify-api-key.md) ます。 |
| [ストア統合](./store-integration.md) | この手順では、Amazon sales channel store を作成した後、アカウントに接続し [!DNL Amazon Seller Central] ます。 [!DNL Amazon Seller Central]この手順では、アカウント (販売者アカウントを作成するために使用される電子メールまたは電話) のプライマリログイン資格情報を必要とします。 |
| [リストルールの作成](./ob-create-listing-rule.md) | Amazon sales channel store に接続した後、リスティングルールを作成するように求めるメッセージが表示されます。 この手順は推奨されていますが、この手順を省略して、カタログのインポート処理を開始することもできます。 ストア [ ダッシュボードからストアとリストの設定にアクセスすることもでき ](./ob-store-review.md) [ ](./amazon-store-dashboard.md) ます。 |
