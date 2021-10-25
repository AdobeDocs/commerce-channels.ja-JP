---
title: 事前設定タスク
description: Adobe Commerce または Magento Open Source store を Amazon 販売チャンネルに組み込む前に、必要なタスクを確認してください。
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# 事前設定タスク

ストアを統合する前に [ ](./store-integration.md) 、 [!DNL Amazon Seller Central] アカウントと [!DNL Commerce] アカウントが統合に向けて準備されていることを確認する必要があります。 統合を成功させるためには、いくつかの事前設定タスクが必要になります。

Amazon sales チャネルに最初の Amazon store を設定すると、セットアップタスクの一覧が表示されます。 Amazon store を追加する前に、これらのタスクを確認しておくことをお勧め [ ](./store-integration.md) します。 最初のストアを追加した後で、Amazon sales channel のホームページの学習ビューと準備ビューで、これらのタスクを確認することができ [ ](./amazon-sales-channel-home.md) ます。

## 1. 「バックグラウンドタスクを有効にする」 [!DNL Commerce]

と Amazon の間で同期されているすべての製品とデータ [!DNL Commerce] は、 [ cron ジョブ ](https://docs.magento.com/user-guide/system/cron.html) {target = &quot;_blank&quot;} によって管理されます。 リストの追加または更新、注文の受信などのタスクを完了すると、cron ジョブがバックエンドのユーザーとアカウントの間でデータを送受信するように [!DNL Commerce] [!DNL Amazon Seller Central] なります。

- [ [!DNL Commerce] Cron ](https://docs.magento.com/user-guide/system/cron.html) {target = &quot;_blank&quot;} を有効にします。

- パフォーマンスを最大にするには、 [  [!DNL Commerce]  cron ](https://docs.magento.com/user-guide/configuration/advanced/system.html) {target = &quot;_blank&quot;} を5分ごとに実行するように設定します。

## 2. アカウントを作成します。 [!DNL Amazon Seller Central]

Amazon sales チャンネルの設定を開始する前に、アクティブなアカウントを持っている必要があり [!DNL Amazon Seller Central] ます。 北米の Amazon 売り手のアカウントが存在しない場合 [ (US、CA、MX) ](https://sell.amazon.com/) {target = &quot;_blank&quot;} または [ ヨーロッパ言語 (英国) ](https://sell.amazon.co.uk/sell-online/beginners-guide) {target = &quot;_blank&quot;} 地域の場合は、Amazon の売り手のアカウント設定プロセスを完了することができます。

Amazon セールスチャネルを使用している場合は、アカウントが必要 [!DNL Professional Seller] に [!DNL Amazon Seller Central] なります。 Amazon は、毎月の購入料金と販売費用によって課金されます。 [Amazon: 販売プランの選択 ](https://sell.amazon.com/pricing.html) {target = &quot;_blank&quot;} を参照してください。

## 3. 承認された Amazon 売り手になっていることを確認してください。

統合するには、承認されたアカウントを持っている必要があり [!DNL Amazon Seller Central] ます。 取引先企業には、製品またはカテゴリについて制限が適用されていないことが必要です。 リストを作成する前に承認が必要な製品やカテゴリもあります。 カテゴリと製品の承認に関する Amazon ポリシーを確認して、製品が承認されたことを確認します。 [Amazon: カテゴリと製品の承認が必要な場合は、 ](https://sellercentral.amazon.com/gp/help/200333160) {target = &quot;_blank&quot;} (販売者の中央ログインが必要) を参照してください。

また、アカウントで次のように設定されているかどうかを確認することも重要です [!DNL Amazon Seller Central] 。

- 返されるポリシーが、Amazon return ポリシーよりも優れたものであることを確認してください。 [Amazon: ポリシーの返却 ](https://www.amazon.com/gp/help/customer/display.html) を参照 {target = &quot;_blank&quot;} を参照してください。

- 税設定が設定されていることを確認します。 [Amazon: 税務方針 ](https://sellercentral.amazon.com/gp/help/external/help.html) の確認 {target = &quot;_blank&quot;} (売り手の中央ログインが必要) を参照してください。

- 送付方法が正確に設定されていることを確認します。 [!DNL Commerce]Amazon の注文を満たすために顧客に提供される送付方法を設定するには、 [ Amazon: 出荷設定 ](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates) {target = &quot;_blank&quot;} を口座に更新して [!DNL Amazon Seller Central] ください。

## 4. VAT が店舗用に設定されていることを確認します。

(主に UK の売り手によって使用されています)。 Amazon [ VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon) {target = &quot;_blank&quot;} にサインアップすることが推奨されます。 別の方法を選択した場合は、VAT コンプライアンスが担当されます。

>[!NOTE]
>
>Amazon が VAT 計算サービスアカウントを確認し、アクティブ化するのに10-14 時間がかかる場合があります。

## 5. 自動カタログ一致の数を増やす

オンボード時に、Amazon 販売チャンネルは製品属性を使用して、既存の Amazon リスト (該当する場合) をカタログ内の既存の製品に適合させ [!DNL Commerce] ます。 オンにした後、これらの製品属性を使用して、 [!DNL Commerce] amazon リストにカタログアイテムを公開し、ユーザーの製品データをと amazon の間で同期させることが [!DNL Commerce] できます。

最大数の製品が Amazon リストと一致するようにするには [!DNL Commerce] 、カタログの一連の製品属性を作成する必要があり [!DNL Commerce] ます。 Amazon 販売チャンネルストアを設定する前に、これらの Amazon 属性に適合するように製品属性を追加する必要があります ( [!DNL Commerce] 例: アーク、EAN、ISBN、UPC、GCID)。 [の「製品属性の作成」を参照してください  [!DNL Commerce]](./ob-creating-magento-attributes.md) 。

## 6. 必要に応じて、通貨と変換を設定します。

使用している web store 用に設定されている通貨と別の通貨が Amazon store によって使用されている場合は、 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/configuration/general/currency-setup.html) {target = &quot;_blank&quot;} という通貨を有効にし、為替 [ 換算レート ](https://docs.magento.com/user-guide/stores/currency-update.html) {target = &quot;_blank&quot;} に設定します。

## 7. 製品条件属性を作成します (必要に応じて)。

Amazon リストに複数の製品条件が含まれている場合 (new、を使用した場合、新規作成した場合など __ ) は __ __ 、属性を作成 [!DNL Commerce] して条件値を割り当てます。 この属性は、オンボードの Amazon Condition 製品属性にマップする必要があります。 [Amazon の属性の作成を参照してください ](./ob-creating-magento-attributes.md) 。

## 8. 送付方法を設定します。 [!DNL Amazon Seller Central]

Amazon の注文を行うための送付方法を設定する方法については、 [ お使いのアカウントの設定 &amp; 出荷設定を参照してください ][10] [!DNL Amazon Seller Central] 。

## その他の設定

Amazon account が設定されていて、アクティブになっている場合は、 [!DNL Commerce] amazon 販売チャンネルのオンボード処理を効率化するためのいくつかのアドバイスが表示されます。

### 除外する製品を確認および注意してください。

Amazon には一部の製品が記載されていない場合があります。 Amazon sales channel には、Amazon に公開する対象となる製品を決定するために使用されるリスティングルールエンジンが含まれています。 [リストルールで ](./listing-rules.md) [!DNL Amazon Seller Central] は、カテゴリ選択によって、または1つまたは複数の製品属性を定義することによって、公開する (またはパブリッシュしない) 製品のサブセットを選択することができます。 [!DNL Commerce] [ Catalog ](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html) {target = &quot;_blank&quot;} または [ ショッピングカート ](https://docs.magento.com/user-guide/marketing/price-rules-cart.html) {target = &quot;_blank&quot;} のような価格ルールの場合は、Amazon の一覧特典に使用する製品属性にがに設定されている必要があり **[!UICONTROL Use for Promo Rule Conditions]** `Yes` ます。「製品について」属性の「 **[!UICONTROL Use for Promo Rule Conditions]** [ ](https://docs.magento.com/user-guide/stores/attributes-product.html) {target = &quot;_blank&quot;}」を参照してください。

### [!DNL Amazon Seller Central]非アクティブにするには地域設定を行います。

統合中にエラーが発生しないデータの移行を容易にするために、Amazon region には、 `Inactive` アカウント情報 > 休暇設定 > 設定で状態を設定することをお勧めします。 [Amazon: 休暇の状態のリストを参照して ][11] ください。セットアップが完了したら、Amazon の状態に戻し `Active` ます。

![次 ](assets/btn-next.png) [**のアイコン属性の作成 [!DNL Commerce]**](./ob-creating-magento-attributes.md)
