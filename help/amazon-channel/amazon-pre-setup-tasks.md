---
title: の事前設定タスク [!DNL Amazon sales channel]
description: Adobe CommerceまたはMagento Open SourceストアをAmazon Sales Channelに統合する前に、完了する必要があるタスクを確認します。
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# の事前設定タスク [!DNL Amazon sales channel]

次の前 [ストアの統合](./store-integration.md)。次のことを確認する必要があります [!DNL Amazon Seller Central] アカウントと [!DNL Commerce] アカウントを統合する準備が整いました。 を正常に統合するには、いくつかの必須の事前設定タスクがあります。

Amazon セールスチャネルで最初のAmazon ストアを設定すると、設定タスクのリストが表示されます。 事前にこれらのタスクを確認することをお勧めします [Amazon ストアを追加](./store-integration.md). 最初の店舗を追加した後、Amazon Sales Channel の「Learning and Preparation」ビューで、これらのタスクを確認できます [ホームページ](./amazon-sales-channel-home.md).

## 1.でのバックグラウンドタスクの有効化 [!DNL Commerce]

間で同期されたすべての製品とデータ [!DNL Commerce] Amazonはによって管理されます。 [cron ジョブ](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). リストの追加や更新、注文の受信などのタスクを完了すると、cron ジョブはユーザーとユーザーの間でデータを送受信します [!DNL Commerce] バックエンドと [!DNL Amazon Seller Central] アカウント。

- [Enable （有効） [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- 最大のパフォーマンスを実現するには、 [set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) を 5 分ごとに実行します。

## 2.を作成する [!DNL Amazon Seller Central] アカウント

Amazonのセールスチャネルの設定を開始する前に、をアクティブにする必要があります [!DNL Amazon Seller Central] アカウント。 に既存のAmazon販売者アカウントがない場合 [北米（米国、CA、MX）](https://sell.amazon.com/){target="_blank"} または [ヨーロッパ （UK）](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} 地域を選択すると、Amazonの販売者アカウントの設定プロセスを完了できます。

Amazon sales channel にはが必要です [!DNL Professional Seller] アカウント日 [!DNL Amazon Seller Central]. Amazonでは、月額利用料と販売価格を請求します。 参照： [Amazon：販売プランを選択します](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3.承認されたAmazonの販売者であることを確認する

統合するには、を承認する必要があります [!DNL Amazon Seller Central] アカウント。 アカウントには、製品またはカテゴリに関する制限を設定しないでください。 一部の製品およびカテゴリでは、リストを作成する前に承認が必要です。 Amazonのカテゴリおよび商品承認ポリシーを確認して、商品が承認されていることを確認します。 参照： [Amazon：承認が必要なカテゴリと製品](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （販売者中央ログインが必要です）

また、で以下が設定されていることを確認することも重要です [!DNL Amazon Seller Central] アカウント :

- 返品ポリシーがAmazonの返品ポリシーと同等かそれ以上であることを確認してください。 参照： [Amazon：再来訪ポリシー](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- 税金設定が構成されていることを確認します。 参照： [Amazon：税務ポリシー](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} （販売者中央ログインが必要です）

- 発送方法が正しく設定されていることを確認します。 次の出荷方法を設定します [!DNL Commerce] は、Amazonの注文を履行するために顧客に提供されています。 [Amazon：配送設定](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} が含まれる [!DNL Amazon Seller Central] アカウント。

## 4. VAT が店舗に設定されていることを確認します

（主に英国のセラーが使用）。 Amazonでは、に新規登録することをお勧めします [AmazonVAT 算定サービス](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. 別の方法を選択した場合は、VAT コンプライアンスに責任があります。

>[!NOTE]
>
>Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

## 5. カタログの自動マッチの数を増やす

オンボーディング中、Amazon セールスチャネルは製品属性を使用して、既存のAmazon リスト（該当する場合）をユーザーの既存の製品に一致させます [!DNL Commerce] カタログ。 オンボーディング後、これらの製品属性を使用して [!DNL Commerce] Amazon リストへの商品のカタログ化と商品データの間での同期 [!DNL Commerce] とAmazon。

の数を最も多くする [!DNL Commerce] 商品はAmazonのリストと自動的に一致します。の商品属性のセットを作成する必要があります [!DNL Commerce] カタログ。 Amazon営業チャネルストアを設定する前に、次を追加する必要があります [!DNL Commerce] Amazonの各属性に一致する製品属性（例：ASIN、EAN、ISBN、UPC、GCID）。 参照： [での製品属性の作成 [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6.通貨とコンバージョンの設定（必要に応じて）

Amazon ストアで、で設定されている以外の通貨を使用している場合 [!DNL Commerce] ストア、 [通貨を有効にする](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) を設定して、 [通貨コンバージョンレート](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7.必要に応じて製品条件属性を作成する

Amazonのリストに複数の商品条件（など）が含まれる場合 _新規_, _使用済み_、または _新規と同様_）、作成します。 [!DNL Commerce] 条件値の属性と割り当て。 オンボーディング中にこの属性をAmazon条件の製品属性にマッピングする必要があります。 参照： [Amazonの属性の作成](./ob-creating-magento-attributes.md).

## 8.の設定 [!DNL Amazon Seller Central] 発送方法

Amazonの注文を処理するための発送方法を設定するには、以下を参照してください。 _設定と配送設定_ が含まれる [!DNL Amazon Seller Central] アカウント。

## その他の設定

Amazon アカウントが設定されてアクティブな場合は、次のものが存在します [!DNL Commerce] Amazon セールスチャネルのオンボーディングプロセスを合理化するための推奨事項です。

### 除外する製品を確認してメモします

一部の商品をAmazonに表示したくないことがあります。 Amazon sales channel にはリストルールエンジンがあり、Amazonへの公開が可能な商品を判断するために使用されます。 [リストルール](./listing-rules.md) に公開（または公開しない）する製品のサブセットを選択できます [!DNL Amazon Seller Central] アカウント （カテゴリ選択または 1 つ以上の製品属性の定義などによる）。 類似 [!DNL Commerce] [カタログ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) または [ショッピングカート](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) 価格ルール、Amazon リストの実施要件に使用される製品属性には、次のものが必要です **[!UICONTROL Use for Promo Rule Conditions]** をに設定 `Yes`. を参照してください。 **[!UICONTROL Use for Promo Rule Conditions]** 。対象： [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### を設定 [!DNL Amazon Seller Central] 非アクティブ化する領域

統合中にエラーのないデータ移行を容易にするために、Amazonリージョンをに設定することをお勧めします `Inactive` ステータス：設定/ アカウント情報/休暇設定。 設定が完了したら、ステータスをに戻します。 `Active` Amazonで。

![次へアイコン](assets/btn-next.png) [**作成を続行 [!DNL Commerce] 属性**](./ob-creating-magento-attributes.md)
