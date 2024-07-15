---
title: ' [!DNL Amazon sales channel] のタスクの事前設定'
description: Adobe CommerceまたはMagento Open SourceストアをAmazon Sales Channelに統合する前に、完了する必要があるタスクを確認します。
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# [!DNL Amazon sales channel] の事前設定タスク

[ ストアの統合 ](./store-integration.md) の前に、[!DNL Amazon Seller Central] アカウントと [!DNL Commerce] アカウントで統合の準備ができていることを確認する必要があります。 を正常に統合するには、いくつかの必須の事前設定タスクがあります。

Amazon セールスチャネルで最初のAmazon ストアを設定すると、設定タスクのリストが表示されます。 [Amazon ストアを追加 ](./store-integration.md) する前に、これらのタスクを確認することをお勧めします。 最初のストアを追加した後、Amazon sales channel [ ホームページ ](./amazon-sales-channel-home.md) の「Learning and Preparation」ビューで、これらのタスクを確認できます。

## 1. [!DNL Commerce] でバックグラウンドタスクを有効にする

[!DNL Commerce] とAmazonの間で同期されたすべての製品とデータは、[cron ジョブ ](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) によって管理されます。 リストの追加や更新、注文の受信などのタスクを完了すると、cron ジョブは、[!DNL Commerce] バックエンドと [!DNL Amazon Seller Central] アカウントの間でデータを送受信します。

- [Enable [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html)。

- 最大のパフォーマンスを得るには、[set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) を 5 分ごとに 1 回実行します。

## 2. [!DNL Amazon Seller Central] アカウントを作成する

Amazonのセールスチャネルの設定を開始する前に、有効な [!DNL Amazon Seller Central] アカウントが必要です。 [ 北米（米国、CA、MX）または [ ヨーロッパ（英国） ](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} リージョンに既存のAmazon販売者アカウントがない場合は ](https://sell.amazon.com/){target="_blank"}Amazonの販売者アカウント設定プロセスを完了できます。

Amazon sales channel には、[!DNL Amazon Seller Central] で [!DNL Professional Seller] アカウントが必要です。 Amazonでは、月額利用料と販売価格を請求します。 [Amazon：販売プランの選択 ](https://sell.amazon.com/pricing.html){target="_blank"} を参照してください。

## 3.承認されたAmazonの販売者であることを確認する

統合するには、承認済みの [!DNL Amazon Seller Central] アカウントが必要です。 アカウントには、製品またはカテゴリに関する制限を設定しないでください。 一部の製品およびカテゴリでは、リストを作成する前に承認が必要です。 Amazonのカテゴリおよび商品承認ポリシーを確認して、商品が承認されていることを確認します。 詳しくは、[Amazon：承認が必要なカテゴリと商品 ](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} （販売者中央ログインが必要）を参照してください。

また、[!DNL Amazon Seller Central] アカウントで次の設定が完了していることを確認することも重要です。

- 返品ポリシーがAmazonの返品ポリシーと同等かそれ以上であることを確認してください。 [Amazon：返品ポリシー ](https://www.amazon.com/gp/help/customer/display.html){target="_blank"} を参照してください。

- 税金設定が構成されていることを確認します。 [Amazon：税ポリシー ](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} を参照してください（販売者中央ログインが必要です）。

- 発送方法が正しく設定されていることを確認します。 Amazonからのご注文に応 [!DNL Commerce] るために顧客に提供する配送方法を設定するには、[!DNL Amazon Seller Central] アカウントの [Amazon：配送設定 ](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} を更新してください。

## 4. VAT が店舗に設定されていることを確認します

（主に英国のセラーが使用）。 Amazonでは、[Amazon VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"} に新規登録することをお勧めします。 別の方法を選択した場合は、VAT コンプライアンスに責任があります。

>[!NOTE]
>
>Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

## 5. カタログの自動マッチの数を増やす

オンボーディング中、Amazon セールスチャネルは製品属性を使用して、既存のAmazon リスト（該当する場合）を [!DNL Commerce] カタログの既存の製品に一致させます。 オンボーディング後、これらの商品属性は、[!DNL Commerce] カタログ項目をAmazon リストに公開したり、[!DNL Commerce] とAmazonの間で商品データを同期したりするために使用されます。

[!DNL Commerce] の商品の最大数をAmazonのリストと自動的に一致させるには、[!DNL Commerce] カタログの一連の商品属性を作成する必要があります。 Amazon営業チャネルストアを設定する前に、ASIN、EAN、ISBN、UPC、GCID などのAmazon属性に一致する [!DNL Commerce] の製品属性を追加する必要があります。 [ 製品属性の作成  [!DNL Commerce]](./ob-creating-magento-attributes.md) を参照してください。

## 6.通貨とコンバージョンの設定（必要に応じて）

Amazon ストアで、[!DNL Commerce] ストアに設定されているものとは異なる通貨を使用している場合は、[ 通貨を有効にする ](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) と [ 通貨換算レート ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html) を設定します。

## 7.必要に応じて製品条件属性を作成する

Amazon リストに複数の商品条件（_new_、_used_、または _like new_ など）が含まれる場合は、[!DNL Commerce] 属性を作成して条件値を割り当てます。 オンボーディング中にこの属性をAmazon条件の製品属性にマッピングする必要があります。 [Amazonの属性の作成 ](./ob-creating-magento-attributes.md) を参照してください。

## 8. [!DNL Amazon Seller Central] 発送方法の設定

Amazonの注文を受け付けるための配送方法を設定するには、[!DNL Amazon Seller Central] アカウントの _設定と配送設定_ を参照してください。

## その他の設定

Amazon アカウントが設定されてアクティブになっている場合は、Amazon セールスチャネルのオンボーディングプロセスの合理化に役立つ、いくつかの [!DNL Commerce] な推奨事項があります。

### 除外する製品を確認してメモします

一部の商品をAmazonに表示したくないことがあります。 Amazon sales channel にはリストルールエンジンがあり、Amazonへの公開が可能な商品を判断するために使用されます。 [ リストルール ](./listing-rules.md) を使用すると、カテゴリ選択や 1 つ以上の製品属性の定義など、[!DNL Amazon Seller Central] アカウントに公開（または公開しない）する製品のサブセットを選択できます。 [!DNL Commerce][ カタログ ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) または [ 買い物かご ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) 価格ルールと同様に、Amazon リストの実施要件に使用する製品属性は、`Yes` に設定する必要 **[!UICONTROL Use for Promo Rule Conditions]** あります。 [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) の **[!UICONTROL Use for Promo Rule Conditions]** を参照してください。

### [!DNL Amazon Seller Central] 地域を非アクティブに設定します

統合中にエラーが発生しないよう、Amazonのリージョンを [ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] でステータスに `Inactive` 定することをお勧めします。 設定が完了したら、Amazonでステータスを `Active` に戻します。

![ 次へアイコン ](assets/btn-next.png)[**引き続き [!DNL Commerce] 属性を作成**](./ob-creating-magento-attributes.md)
