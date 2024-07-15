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

_[!UICONTROL Fulfilled By]_の設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定は、注文を履行（または出荷）するパーティを定義します。 注文がすべて 1 つの方法で履行される場合は、マーチャント（自分）またはAmazonのいずれかを選択します。 拠点からの注文を受け付け、Amazonを使用する予定がある場合は、3 つ目のオプションを使用し、[!DNL Commerce] しい商品属性を設定することをお勧めします。

- **[!UICONTROL Fulfilled by Merchant]** – あなたは、商人、すべての注文を満たしている場合に選択します。 注文すると、在庫が [!DNL Commerce] ーザーカタログから差し引かれます。

- **[!UICONTROL Fulfilled by Amazon]** - Amazonがすべての注文を履行するかどうかを選択します。 このオプションを使用すると、注文の際に商品の在庫が [!DNL Commerce] カタログから差し引かれることはありません。 Amazonの出荷済み注文の在庫在庫が保管され、倉庫から差し引かれます。 このオプションを割り当てる前に、[!DNL Amazon Seller Central] アカウントで、商品が _Amazonによる履行_ （FBA）のフルフィルメントの対象であることを確認する必要があります。 FBA インベントリは、[!DNL Amazon Seller Central] アカウントを通じて直接管理されます。 このフルフィルメント方法を使用すると、Amazonの営業チャネルは、[!DNL Commerce] とAmazonの間で数量の更新を共有しなくなります。 そのため、数量設定に記載されているすべてのマーケティングツールがAmazon Sales Channel で使用できるわけではありません。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** – 商品が顧客とAmazonによって履行される場合は、「マーチャントによる履行」および「Amazonによる履行」の値を持つ [!DNL Commerce] しい商品属性を作成できます。 製品ごとにこの値を設定すると、誰が注文を満たしているかを示します。

フルフィルメント方法は地域の属性であり、[ ストアの統合 ](./store-integration.md) 時に定義された **[!UICONTROL Amazon Marketplace Country]** 設定に基づいています。 [!DNL Amazon Seller SKU] 変更を加えると、同じリージョンで販売されているAmazon ストアで共有されている、すべてのAmazon リストに変更が影響します（[ ストア統合 ](./store-integration.md) 中に _[!UICONTROL Amazon Marketplace Country]_で定義された通り）。 米国の共有 [!DNL Amazon Seller SKU] を変更しても、（ストアの統合時に定義された）別のリージョンに設定されたAmazon ストアには影響しません。

>[!NOTE]
>
>注文がAmazon（FBA）で履行され、注文が読み込まれると、注文の詳細のいくつかのフィールドにダミーデータが表示される場合があります。 [Amazon注文の詳細 ](./amazon-order-details.md) を参照してください。

## [!UICONTROL Fulfilled By] の設定 {#configure-fulfilled-by-settings}

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL Fulfilled By]_」セクションを展開します。

1. **[!UICONTROL Product Fulfilled By]**：注文を満たす（出荷する）ユーザーを選択します。

   - `Fulfilled by Merchant` - マーチャントは注文を満たします。

   - `Fulfilled by Amazon` - Amazon ウェアハウスは注文を満たします。

   - `Assign Fulfilled By Using Magento Product Attribute` - [!DNL Commerce] 属性は、製品ごとの注文を満たすユーザーを示します。

     選択した場合、**[!UICONTROL Fulfilled by Attribute]** でマッピングする [!DNL Commerce] 属性を選択します。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ フルフィルメント実行者設定 ](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | オプション：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - （FBM）注文を履行するかどうかを選択します。 注文すると、在庫が [!DNL Commerce] ーザーカタログから差し引かれます。 新しい商品が作成されると、発送済みのマーチャントの発送方法が割り当てられます。</li><li>**[!UICONTROL Fulfilled by Amazon]** - （FBA） Amazonが注文を満たしているかどうかを選択します。 このフルフィルメント方法を使用すると、注文の際に商品の在庫が [!DNL Commerce] カタログから差し引かれることはありません。 商品を作成する際は、フルフィルメントタイプとして _[!UICONTROL Fulfilled by Amazon (FBA)]_を使用して作成されます。 お客様の商品が [!DNL Amazon Seller Central] アカウント内の FBA フルフィルメントの対象であることを確認してください。 FBA インベントリは、[!DNL Amazon Seller Central] アカウントを介して直接管理されます。 このフルフィルメント方法を使用すると、数量の更新が [!DNL Commerce] カタログに相対的にプッシュされないので、[ 在庫/数量設定 ](./stock-quantity.md) で説明しているマーケティングツールの一部を使用できません。</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - マーチャントによって履行されるか、Amazonによって履行されるかを決定する既存の [!DNL Commerce] 属性がある場合に選択します。 選択すると、**[!UICONTROL Fulfilled by Attribute]** が有効になります。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | フルフィルメント方法を決定するために使用する [!DNL Commerce] 属性を選択します。<br><br> 例えば、属性が _履行者_ で、属性値を `Fulfilled By Merchant` または `Fulfilled By Amazon (FBA)` に選択した場合、その値が新規製品の履行タイプとして使用されます。 マーチャントは、商品が [!DNL Amazon Seller Central] アカウント内の FBA フルフィルメントの対象であることを確認する必要があります。 FBA インベントリは、Amazonセラーアカウントを通じて直接管理されます。<br><br> オプションは、Amazon製品に設定した属性によって異なります。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
