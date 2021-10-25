---
title: 注文の管理
description: 商業管理者からの Amazon 注文をより簡単に管理できるように、注文設定の注文のインポートを有効にすることができます。
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 1d1b888db4de4f6e3658af768cd6f5cf30828788
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 注文の管理

Amazon から受信した注文情報を表示するには、 _[!UICONTROL Recent Orders]_[ ストアダッシュボードのセクション ](./amazon-store-dashboard.md) または_[!UICONTROL Amazon orders]_ ページ (ビューとも呼ばれ _[!UICONTROL All Orders]_ます) を使用します。

Amazon の注文を管理する方法は、注文の設定で注文のインポートが有効になっているか無効であるかによって異なり [ ](./order-settings.md#configure-order-settings) ます。

## 注文のインポートが有効になっています。

[ストア統合後に ](./store-integration.md) [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) デフォルトでこの設定が設定され `Enabled` ています。この設定によって、 [!DNL Commerce] Amazon の注文に対応する注文が作成され、 [[!DNL Commerce]  注文 ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} ワークフローで管理できるようになります。

>[!NOTE]
>
>注文の読み込み設定に関係なく、ストア統合の際に、お客様のアカウントに存在していた Amazon 受注 [!DNL Amazon Seller Central] [ はインポートされ ](./store-integration.md) ません。

読み込んだ Amazon orders は、 [[!DNL Commerce]  ](https://docs.magento.com/user-guide/sales/orders.html) 他のストアと同様に、{target = &quot;_blank&quot;} という注文で管理され [!DNL Commerce] ます。 列にある Amazon の注文番号をクリックして、 *[!UICONTROL Order Number]* [[!DNL Commerce]  注文処理 ( ](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions) {target = &quot;_blank&quot;}) の注文を開きます。 [Amazon Orders の表示を参照してください ](./amazon-orders-all.md) 。

### 注文のインポート処理

Amazon に注文が行われ、 [ 注文のインポート ](./order-settings.md) が有効になると、次の処理が開始されます。

| 変更 | 活動 |
|---|---|
| Amazon には注文が適用されます。 | <ul><li>Amazon によって注文状況がに設定され `Pending` ます。</li><li>注文情報は、宛先に送られ [!DNL Commerce] ます。</li><li>「Amazon orders」テーブルに注文が追加され [__ 、状態を示し ](./amazon-orders-all.md) `Pending` ます。</li></ul> |
| Amazon によって注文状況がに変更され `Unshipped` ます。 | <ul><li>状態の変更はに送られ [!DNL Commerce] ます。</li><li>[_Amazon orders テーブルでは、_ ](./amazon-orders-all.md) 注文状況がに変更され `Unshipped` ます。</li><li>[[!DNL Commerce] Orders workflow ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} には、対応する [!DNL Commerce] 注文が状態を使用して作成され `Processing` ます。</li></ul> |
| [[!DNL Commerce] Orders workflow ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} には、 [!DNL Commerce] 注文が処理され、状態がに変更され `Shipped` ます。 | <ul><li>[_Amazon orders テーブルでは、_ ](./amazon-orders-all.md) 注文状況がに変更され `Shipped` ます。</li><li>その後、次の cron ジョブでは、注文の状態は、 `Complete` [[!DNL Commerce]  orders workflow ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} に変更されます。</li></ul> |

### オーダー作成ブロックの作成

対応する順序を作成しないようにするシナリオはいくつかあり [!DNL Commerce] ます。 [!DNL Commerce] 次のいずれかの問題が発生したときに受信される注文については、注文が作成されません。

| よう | ソリューション |
|---|---|
| このアイテムはカタログに存在していません [!DNL Commerce] 。 | [](./creating-assigning-catalog-products.md)カタログに製品を作成 [!DNL Commerce] し、 [ それを製品に手動で一致させ ](./creating-assigning-catalog-products.md) ます。 |
| カタログ内のアイテムが無効化されています。 | [製品の状態 ](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html) {target = &quot;_blank&quot;} が有効になっていることを確認してください。 |
| 注文されたアイテムが在庫切れになっています。 | 製品オプションを更新または設定し [ ](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html) ます。 {target = &quot;_blank&quot;}、数量およびソースを設定します。 |

注文を読み込むことができない場合は、次のようなシステムメッセージが画面の上部に表示されます。

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

問題が解決されると、 [!DNL Commerce] 次の同期時に注文が作成されます。

## 注文のインポートが無効化される

で Amazon の注文のインポートと管理を行いたくない場合は、の [!DNL Commerce] 設定をに変更することができ [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) `Disabled` ます。 この設定を選択すると、Amazon から新しい注文を受信したときに、対応する [!DNL Commerce] 注文が作成されません。

無効の場合、Amazon から受け取った注文情報は、 _[!UICONTROL Recent Orders]_ストアダッシュボードのセクションとビューに表示され_[!UICONTROL All Orders]_ ます。 この注文情報はビューのみであり、によってこれらの注文が管理されている必要があり [!DNL Amazon Seller Central] ます。 で受注明細を開くには [!DNL Amazon Seller Central] 、列内の Amazon の注文番号をクリックし _[!UICONTROL Order Number]_ます。

「 [ Amazon の注文の表示」 ](./amazon-orders-all.md) 、「 [ amazon order Details を表示」、「 ](./amazon-order-details.md) [ 一般的な注文処理タスク ](./common-order-processing.md) 」も参照してください。
