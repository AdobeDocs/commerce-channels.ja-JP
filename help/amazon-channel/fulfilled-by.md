---
title: Amazon一覧の設定で実行
description: Amazonの一覧からの注文がどのように履行（発送）されるかを決定するには、「履行者」設定を使用します。
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Amazon一覧の設定で実行

_[!UICONTROL Fulfilled By]_設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、注文（または発送）を実行するパーティを定義します。 すべての注文が 1 つの方法で満たされた場合、マーチャント（あなた）かAmazonのどちらかを選択します。 お客様の場所からの注文を完了し、Amazonを使用する予定がある場合は、3 番目のオプションを使用して [!DNL Commerce] 製品属性。

- **[!UICONTROL Fulfilled by Merchant]**  — あなたが、商人が、すべての注文を満たすかどうかを選択します。 注文が行われると、在庫が貴社の [!DNL Commerce] カタログ。

- **[!UICONTROL Fulfilled by Amazon]** - Amazonがすべての注文を完了するかどうかを選択します。 このオプションを選択した場合、製品の在庫は [!DNL Commerce] カタログを表示します。 Amazonが満たした注文の在庫は、倉庫から引き落とされ保管されます。 このオプションを割り当てる前に、 [!DNL Amazon Seller Central] 製品に適したアカウント _Amazonで実現_ (FBA) 達成 FBA インベントリは、 [!DNL Amazon Seller Central] アカウント。 この達成方法では、Amazonの販売チャネルは、次の期間で数量の更新を共有しません： [!DNL Commerce] Amazon したがって、「数量の設定」で説明されているすべてのマーケティングツールがAmazonセールスチャネルで使用できるわけではありません。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — お客様とAmazonが製品を満たす場合、 [!DNL Commerce] 「マーチャントが満たした」および「Amazonが満たした」の値を持つ product 属性。 製品ごとにこの値を設定すると、注文を実行するユーザーが示されます。

達成方法は、地域属性で、 **[!UICONTROL Amazon Marketplace Country]** 次の間に定義された設定 [ストア統合](./store-integration.md). 変更を加えると、その変更は、共有するすべてのAmazonリストに影響します [!DNL Amazon Seller SKU] をAmazonの店舗で同じ地域に販売している ( _[!UICONTROL Amazon Marketplace Country]_期間 [ストア統合](./store-integration.md)) をクリックします。 共有に対する変更 [!DNL Amazon Seller SKU] 米国の場合は、（store 統合時に定義された）異なる地域用に設定されたAmazon店舗には影響しません。

>[!NOTE]
>
>注文がAmazon(FBA) で処理され、注文がインポートされると、注文の詳細に一部のフィールドのダミーデータが表示されます。 詳しくは、 [Amazon注文の詳細](./amazon-order-details.md).

## の設定 [!UICONTROL Fulfilled By] 設定 {#configure-fulfilled-by-settings}

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL Fulfilled By]_」セクションに入力します。

1. の場合 **[!UICONTROL Product Fulfilled By]**、（船）注文を実行する人を選択します。

   - `Fulfilled by Merchant`  — 商人が注文を完了。

   - `Fulfilled by Amazon` -Amazon倉庫は受注を完了。

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] 属性は、製品ごとの注文を実行するユーザーを示します。

     選択した場合は、 [!DNL Commerce] 属性を **[!UICONTROL Fulfilled by Attribute]**.

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![満たされたユーザー設定](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | オプション：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) 注文を満たす場合に選択します。 注文が行われると、在庫が貴社の [!DNL Commerce] カタログ。 新しい製品が作成されると、マーチャントフルメントの達成方法が割り当てられます。</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA)Amazonが注文を処理するかどうかを選択します。 この達成方法では、製品の在庫は [!DNL Commerce] カタログを表示します。 製品を作成すると、 _[!UICONTROL Fulfilled by Amazon (FBA)]_達成タイプとして。 お客様の製品が FBA を満たす資格を満たしていることをお客様の [!DNL Amazon Seller Central] アカウント また、FBA インベントリは、 [!DNL Amazon Seller Central] アカウント この達成方法では、数量の更新は、 [!DNL Commerce] カタログに含まれるので、 [在庫/数量の設定](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 既存の [!DNL Commerce] 属性は、それが商人によって果たされるか、Amazonによって果たされるかを決定します。 選択した場合、 **[!UICONTROL Fulfilled by Attribute]** 有効にします。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | を選択します。 [!DNL Commerce] 達成方法の決定に使用される属性。<br><br>例えば、属性が _達成者_ 属性値を `Fulfilled By Merchant` または `Fulfilled By Amazon (FBA)`の場合、その値が新しい製品の達成タイプとして使用されます。 マーチャントは、お客様の製品が FBA を満たす資格をお持ちであることをお客様に確認する必要があります [!DNL Amazon Seller Central] アカウント また、FBA 在庫は、Amazonセラーアカウントを通じて直接管理されます。<br><br>オプションは、Amazon製品に設定した属性によって異なります。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
