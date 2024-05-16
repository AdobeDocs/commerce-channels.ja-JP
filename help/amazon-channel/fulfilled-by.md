---
title: Amazon一覧の指定者の設定
description: 「履行者」設定を使用して、Amazon一覧からの受注の履行方法（出荷済）を決定します。
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Amazon一覧の指定者の設定

_[!UICONTROL Fulfilled By]_設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、注文を履行（または出荷）するパーティを定義します。 注文がすべて 1 つの方法で履行される場合は、マーチャント（自分）またはAmazonのいずれかを選択します。 拠点からの注文を受け付け、Amazonを使用する計画がある場合は、3 番目の選択肢を使用し、 [!DNL Commerce] 製品属性。

- **[!UICONTROL Fulfilled by Merchant]**  – あなたは、商人、すべての注文を満たしている場合に選択します。 注文すると、在庫が注文から差し引かれます [!DNL Commerce] カタログ。

- **[!UICONTROL Fulfilled by Amazon]** - Amazonがすべての注文を履行するかどうかを選択します。 このオプションを使用すると、製品インベントリは [!DNL Commerce] カタログ注文時。 Amazonの出荷済み注文の在庫在庫が保管され、倉庫から差し引かれます。 このオプションを割り当てる前に、 [!DNL Amazon Seller Central] 商品が適格なアカウント _Amazonで処理_ （FBA）フルフィルメント。 FBA インベントリは、 [!DNL Amazon Seller Central] アカウント。 このフルフィルメント方式では、Amazonの営業チャネルは、間で数量の更新を共有しません [!DNL Commerce] とAmazon。 そのため、数量設定に記載されているすべてのマーケティングツールがAmazon Sales Channel で使用できるわけではありません。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  – お客様とAmazonが商品を受け取る可能性がある場合は、 [!DNL Commerce] 販売者による履行済およびAmazonによる履行済の値を持つ製品属性。 製品ごとにこの値を設定すると、誰が注文を満たしているかを示します。

フルフィルメント方法は地域属性であり、に基づいています **[!UICONTROL Amazon Marketplace Country]** 次の期間に定義された設定 [ストアの統合](./store-integration.md). 変更を加えると、その変更を共有するすべてのAmazon リストに影響します [!DNL Amazon Seller SKU] （で定義されているように）Amazon内の同じリージョンで販売されるストア _[!UICONTROL Amazon Marketplace Country]_次の期間 [ストアの統合](./store-integration.md)）に設定します。 共有へのの変更 [!DNL Amazon Seller SKU] 米国では、（ストアの統合時に定義された）別のリージョンに設定されたAmazon ストアには影響しません。

>[!NOTE]
>
>注文がAmazon（FBA）で履行され、注文が読み込まれると、注文の詳細のいくつかのフィールドにダミーデータが表示される場合があります。 参照： [Amazon注文の詳細](./amazon-order-details.md).

## の設定 [!UICONTROL Fulfilled By] 設定 {#configure-fulfilled-by-settings}

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 _[!UICONTROL Fulfilled By]_セクション。

1. の場合 **[!UICONTROL Product Fulfilled By]**&#x200B;注文を満たす（出荷する）ユーザーを選択：

   - `Fulfilled by Merchant` - マーチャントは注文を満たします。

   - `Fulfilled by Amazon` -Amazon倉庫は注文を満たしています。

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] 属性は、製品ごとの注文を満たすユーザーを示します。

     選択した場合は、 [!DNL Commerce] マッピングする属性 **[!UICONTROL Fulfilled by Attribute]**.

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![フルフィルメント実行者設定](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | オプション：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - （FBM）注文を履行するかどうかを選択します。 注文すると、在庫が注文から差し引かれます [!DNL Commerce] カタログ。 新しい商品が作成されると、発送済みのマーチャントの発送方法が割り当てられます。</li><li>**[!UICONTROL Fulfilled by Amazon]** - （FBA）Amazonが注文を満たすかどうかを選択します。 このフルフィルメント方法では、商品の在庫は引き落とされません [!DNL Commerce] カタログ注文時。 製品を作成する際は、次を使用します。 _[!UICONTROL Fulfilled by Amazon (FBA)]_フルフィルメントタイプとして。 お客様の製品が FBA フルフィルメントの対象であることを確認してください [!DNL Amazon Seller Central] アカウント。 FBA インベントリは、 [!DNL Amazon Seller Central] アカウント。 このフルフィルメント方法を使用すると、数量の更新がユーザーに相対的にプッシュされることはありません [!DNL Commerce] カタログが存在するため、「」で説明されている一部のマーケティングツールは使用できません。 [在庫/数量の設定](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  – 既存のを持っているかどうかを選択 [!DNL Commerce] マーチャントによって履行されるか、Amazonによって履行されるかを決定する属性。 選択した場合、 **[!UICONTROL Fulfilled by Attribute]** を有効にします。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | を選択します。 [!DNL Commerce] フルフィルメント方法を決定するために使用される属性。<br><br>例えば、属性がの場合 _フルフィルメント者_ また、属性値をとして選択します `Fulfilled By Merchant` または `Fulfilled By Amazon (FBA)`の場合、その値が新しい商品のフルフィルメントタイプとして使用されます。 マーチャントは、商品が FBA フルフィルメントの対象であることを確認する必要があります [!DNL Amazon Seller Central] アカウント。 FBA インベントリは、Amazonセラーアカウントを通じて直接管理されます。<br><br>オプションは、Amazon商品に対して設定した属性によって異なります。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
