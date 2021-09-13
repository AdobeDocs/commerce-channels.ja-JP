---
title: 事前設定タスク
description: AmazonSales ChannelにAdobeコマースまたはMagento Open Sourceストアを統合する前に、完了する必要があるタスクを確認します。
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# 事前設定タスク

[ストア統合](./store-integration.md)の前に、[!DNL Amazon Seller Central]アカウントと[!DNL Commerce]アカウントが統合に対応していることを確認する必要があります。 を正常に統合するには、事前設定タスクがいくつか必要です。

Amazonの販売チャネルに最初のAmazonストアを設定すると、設定タスクのリストが表示されます。 [Amazonストア](./store-integration.md)を追加する前に、これらのタスクを確認することをお勧めします。 最初のストアを追加した後、Amazonセールスチャネル[ホームページ](./amazon-sales-channel-home.md)の学習と準備ビューで、これらのタスクを確認できます。

## 1. [!DNL Commerce]でバックグラウンドタスクを有効にする

[!DNL Commerce]とAmazonの間で同期されたすべての製品とデータは、[cronジョブ](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}によって管理されます。 リストの追加や更新などのタスクを完了し、注文を受け取ると、cronジョブは[!DNL Commerce]バックエンドと[!DNL Amazon Seller Central]アカウントの間でデータの送受信を行います。

- [ [!DNL Commerce] Enablecron](https://docs.magento.com/user-guide/system/cron.html) {target=&quot;_blank&quot;}。

- 最高のパフォーマンスを得るには、[set [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;}を5分ごとに1回実行します。

## 2. [!DNL Amazon Seller Central]アカウントを作成する

Amazonの販売チャネルの設定を開始する前に、アクティブな[!DNL Amazon Seller Central]アカウントが必要です。 [北米(US、CA、MX)](https://sell.amazon.com/){target=&quot;_blank&quot;}または[ヨーロッパ(UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;}の地域に既存のAmazonセラーアカウントがない場合は、Amazonセラーのアカウント設定プロセスを完了できます。

Amazonの販売チャネルには、[!DNL Amazon Seller Central]の[!DNL Professional Seller]アカウントが必要です。 Amazonは月々の購読と販売料を請求します。 [Amazon:販売計画](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}を選択します。

## 3.お客様が承認済みのAmazon販売者であることを確認する

統合するには、承認済みの[!DNL Amazon Seller Central]アカウントが必要です。 アカウントに、製品やカテゴリに対する制限を設けないでください。 一部の製品やカテゴリでは、リストを作成する前に承認が必要です。 カテゴリおよび製品の承認に関するAmazonポリシーを確認して、製品が承認されていることを確認します。 [Amazon:承認](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;}が必要なカテゴリや製品（セラー一元ログインが必要）。

また、[!DNL Amazon Seller Central]アカウントで次の設定をおこなうことも重要です。

- 返品ポリシーがAmazonの返品ポリシーと同じか、それ以上に適していることを確認します。 [Amazon:ポリシー](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}を返します。

- 税金設定が設定されていることを確認します。 [Amazon:税ポリシー](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} （セラーセントラルログインが必要）。

- 発送方法が正しく設定されていることを確認します。 Amazonの注文を履行するために顧客に提供される配送方法を設定するには、[Amazonを更新します。[!DNL Amazon Seller Central]アカウントの配送設定](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;}。[!DNL Commerce]

## 4.店舗に対してVATが設定されていることを確認します。

（主に英国の販売者が使用） Amazonは、[Amazon VAT計算サービス](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}に新規登録することをお勧めします。 別の方法を選択する場合は、VATコンプライアンスに対する責任を負います。

>[!NOTE]
>
>AmazonがVAT計算サービスのアカウントを確認して有効化するまでに10 ～ 14日かかる場合があります。

## 5.カタログの自動一致数を増やす

オンボーディング時、Amazonの販売チャネルは製品属性を使用して、既存のAmazonリストを[!DNL Commerce]カタログ内の既存の製品に一致させます（該当する場合）。 オンボーディング後、これらの製品属性を使用して、[!DNL Commerce]カタログ項目をAmazonリストに公開し、[!DNL Commerce]とAmazonの間で製品データを同期します。

最も多くの[!DNL Commerce]製品がAmazonのリストと自動的に一致するようにするには、[!DNL Commerce]カタログの製品属性のセットを作成する必要があります。 Amazonセールスチャネルストアを設定する前に、次のように、これらのAmazon属性に一致する製品属性[!DNL Commerce]を追加する必要があります。ASIN、EAN、ISBN、UPC、またはGCID。 [ [!DNL Commerce]](./ob-creating-magento-attributes.md)での製品属性の作成を参照してください。

## 6.必要に応じて、通貨とコンバージョンを設定します

Amazonストアで、[!DNL Commerce]ストアに設定されている通貨とは異なる通貨が使用されている場合は、[currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}を有効にして、[currency換算レート](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}を設定します。

## 7.必要に応じて、製品条件属性を作成します。

Amazonのリストに複数の製品条件（_new_、_used_、_like new_&#x200B;など）が含まれる場合は、[!DNL Commerce]属性を作成し、条件値を割り当てます。 オンボーディング時に、この属性をAmazon条件製品属性にマッピングする必要があります。 [Amazon](./ob-creating-magento-attributes.md)の属性の作成を参照してください。

## 8.[!DNL Amazon Seller Central]発送方法を設定します

Amazonのご注文を満たすために提供する配送方法を設定するには、[!DNL Amazon Seller Central]アカウントの[設定と配送設定][10]を参照してください。

## 追加の設定

Amazonアカウントが設定されアクティブになっている場合、Amazonの販売チャネルのオンボーディングプロセスを効率化するのに役立つ、いくつかの[!DNL Commerce]推奨事項があります。

### 除外する製品を確認してメモします。

一部の製品をAmazonに表示したくない場合があります。 Amazonの販売チャネルには、Amazonに発行する資格のある製品を決定するために使用されるリストルールエンジンがあります。 [リスト](./listing-rules.md) ルールを使用すると、カテゴリの選択や1つ以上の製品属性の定義など、アカウントに公開する（または公開しない）製品のサブセットを選択できま [!DNL Amazon Seller Central] す。[!DNL Commerce] [catalog](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}や[shopping cart](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;}の価格ルールのように、Amazonリストの実施要件に使用する製品属性は&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;を`Yes`に設定する必要があります。 [製品属性](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}の&#x200B;**[!UICONTROL Use for Promo Rule Conditions]**&#x200B;を参照してください。

### [!DNL Amazon Seller Central]領域を非アクティブに設定します

統合中のエラーのないデータ移行を容易にするために、設定/アカウント情報/休暇の設定で、Amazon地域を`Inactive`ステータスに設定することをお勧めします。 [Amazonを参照：休暇][11]のステータスのリスト。 設定が完了したら、Amazonでステータスを`Active`に戻します。

![次のア](assets/btn-next.png) [**イコン属性の作成を続 [!DNL Commerce] 行**](./ob-creating-magento-attributes.md)
