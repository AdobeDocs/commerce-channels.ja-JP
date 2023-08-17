---
title: の事前設定タスク [!DNL Amazon sales channel]
description: AmazonSales ChannelにAdobe CommerceまたはMagento Open Sourceストアを統合する前に、完了する必要のあるタスクを確認します。
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# の事前設定タスク [!DNL Amazon sales channel]

前 [ストア統合](./store-integration.md)次の場合、 [!DNL Amazon Seller Central] アカウントと [!DNL Commerce] アカウントを統合する準備が整いました。 統合を成功させるには、いくつかの事前設定タスクが必要です。

Amazonセールスチャネルに最初のAmazonストアを設定すると、設定タスクのリストが表示されます。 次のタスクを確認してから、 [Amazonストアを追加](./store-integration.md). 最初のストアを追加した後、Amazon Sales Channel の「Learning and Preparation」表示でこれらのタスクを確認できます [ホームページ](./amazon-sales-channel-home.md).

## 1.でのバックグラウンドタスクの有効化 [!DNL Commerce]

間で同期されたすべての製品とデータ [!DNL Commerce] Amazonは [cron ジョブ](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). リストの追加や更新などのタスクを完了して注文を受け取ると、cron ジョブは、 [!DNL Commerce] のバックエンドと [!DNL Amazon Seller Central] アカウント。

- [有効にする [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- 最高のパフォーマンスを得るには、 [設定 [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) 5 分に 1 回実行する

## 2. [!DNL Amazon Seller Central] アカウント

Amazonセールスチャネルの設定を開始する前に、アクティブな [!DNL Amazon Seller Central] アカウント。 既存のAmazon Seller アカウントが [北米（米国、カリフォルニア州、MX）](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} 地域に移動する場合は、Amazonの販売者アカウントの設定プロセスを完了できます。

Amazonセールスチャネルには、 [!DNL Professional Seller] ～のアカウント [!DNL Amazon Seller Central]. Amazonは月々の購読と販売料を請求します。 詳しくは、 [Amazon：販売プランを選択](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3.自分が承認済みのAmazonの販売者であることを確認する

統合するには、承認済みの [!DNL Amazon Seller Central] アカウント。 アカウントには、製品やカテゴリに対する制限を設けないでください。 一部の製品やカテゴリでは、リストを作成する前に承認が必要です。 カテゴリおよび製品の承認に関するAmazonポリシーを確認して、製品が承認されていることを確認します。 詳しくは、 [Amazon：承認が必要なカテゴリおよび製品](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （販売者の中央ログインが必要です）。

また、 [!DNL Amazon Seller Central] アカウント：

- 返品ポリシーがAmazonの返品ポリシーと同じか、それ以上に良いことを確認します。 詳しくは、 [Amazon：リターンポリシー](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- 税金設定が構成されていることを確認します。 詳しくは、 [Amazon：税制](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} （販売者の中央ログインが必要です）。

- 発送方法が正しく設定されていることを確認します。 発送方法を設定するには、以下を実行します。 [!DNL Commerce] は、Amazonの注文を満たすために顧客に提供され、 [Amazon：配送設定](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} の [!DNL Amazon Seller Central] アカウント。

## 4.お客様の店舗に対して VAT が設定されていることを確認します。

（主に英国の販売者が使用） Amazonは、 [AmazonVAT 計算サービス](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. 別の方法を選択する場合は、VAT コンプライアンスに対する責任を負います。

>[!NOTE]
>
>Amazonが VAT 計算サービスアカウントを検証および有効化するまでに 10 ～ 14 日かかる場合があります。

## 5.自動カタログ一致数を増やします

オンボーディング中、Amazonのセールスチャネルは製品属性を使用して、既存のAmazonリスト（該当する場合）を [!DNL Commerce] カタログ。 オンボーディング後、これらの製品属性を使用して [!DNL Commerce] カタログ項目をAmazonリストに追加し、製品データを [!DNL Commerce] Amazon

最も多くの [!DNL Commerce] 製品はAmazonのリストに自動的に一致します。 [!DNL Commerce] カタログ。 Amazonセールスチャネルストアを設定する前に、 [!DNL Commerce] これらのAmazon属性に一致する製品属性（例：ASIN、EAN、ISBN、UPC、GCID）。 詳しくは、 [での製品属性の作成 [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6.通貨とコンバージョンを（必要に応じて）設定します

Amazonストアで、 [!DNL Commerce] 保存 [通貨を有効にする](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) をクリックし、 [通貨換算レート](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7.必要に応じて、製品条件属性を作成します。

Amazonのリストに複数の製品条件 ( _新規_, _使用済み_&#x200B;または _新規に_)、作成する [!DNL Commerce] 属性と条件値の割り当て。 この属性は、Amazon条件の製品属性にオンボーディングする際にマッピングする必要があります。 詳しくは、 [Amazonの属性の作成](./ob-creating-magento-attributes.md).

## 8. [!DNL Amazon Seller Central] 輸送方法

Amazonの注文を満たすために提供する発送方法を設定するには、 _設定と配送設定_ の [!DNL Amazon Seller Central] アカウント。

## 追加の設定

Amazonアカウントが設定され、アクティブになっている場合は、次のようになります。 [!DNL Commerce] Amazonセールスチャネルのオンボーディングプロセスの合理化に役立つ推奨事項。

### 除外する製品を確認してメモします。

一部の製品をAmazonに表示したくない場合があります。 Amazonセールスチャネルには、Amazonへの公開の対象となる製品を決定するために使用されるリストルールエンジンがあります。 [リストルール](./listing-rules.md) に公開する（または公開しない）製品のサブセットを選択できます。 [!DNL Amazon Seller Central] アカウント（カテゴリ別、または 1 つ以上の製品属性を定義するなど）。 次に類似 [!DNL Commerce] [カタログ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) または [買い物かご](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) 価格ルール、Amazonリストへの適格要件に使用する製品属性は、次の条件を満たす必要があります。 **[!UICONTROL Use for Promo Rule Conditions]** に設定 `Yes`. 詳しくは、 **[!UICONTROL Use for Promo Rule Conditions]** in [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### を [!DNL Amazon Seller Central] 非アクティブな地域

統合時にエラーのないデータ切り替えを容易におこなえるように、Amazon地域を `Inactive` のステータスが [ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] に表示されます。 設定が完了したら、ステータスを「 `Active` Amazonで

![次のアイコン](assets/btn-next.png) [**作成を続行 [!DNL Commerce] 属性**](./ob-creating-magento-attributes.md)
