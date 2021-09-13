---
title: 履行者
description: 「履行者」設定を使用して、Amazonの一覧からの注文がどのように履行（出荷）されるかを決定します。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 618
ht-degree: 0%

---

# 履行者

_[!UICONTROL Fulfilled By]_設定は、ストアリスト設定の一部です。リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定は、注文（または出荷）を実行するパーティを定義します。 すべての注文が1つの方法で処理された場合は、マーチャント（お客様）かAmazonかを選択します。 お客様の場所からの注文を完了し、Amazonを使用する場合は、3つ目のオプションを使用して[!DNL Commerce]製品属性を設定することをお勧めします。

- **[!UICONTROL Fulfilled by Merchant]**  — お客様、商人、すべての注文を満たすかどうかを選択します。注文が行われると、在庫が[!DNL Commerce]カタログから差し引かれます。

- **[!UICONTROL Fulfilled by Amazon]** - Amazonがすべての注文を処理する場合に選択します。このオプションを使用すると、注文時に製品在庫が[!DNL Commerce]カタログから差し引かれることはありません。 Amazonが履行した注文の在庫は、倉庫から引き落とされます。 このオプションを割り当てる前に、[!DNL Amazon Seller Central]アカウントで、お使いの製品が&#x200B;_Amazon_(FBA)で履行できるかどうかを確認する必要があります。 FBAインベントリは、[!DNL Amazon Seller Central]アカウントを通じて直接管理されます。 このフルフィルメント方法では、Amazonの販売チャネルは、[!DNL Commerce]とAmazonの間で数量の更新を共有しません。 したがって、Amazonの販売チャネルでは、数量設定で説明されているすべてのマーケティングツールを使用できるわけではありません。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — 製品がお客様とAmazonによって満たされる場合、「マーチャントによる履行」および「Amazonによる履行」の値を持つ製品属性を作成する必要が生じる場合がありま [!DNL Commerce] す。製品ごとにこの値を設定すると、注文を実行するユーザーが示されます。

フルフィルメント方法は、地域属性で、[store integration](./store-integration.md)で定義された&#x200B;**[!UICONTROL Amazon Marketplace Country]**&#x200B;設定に基づいています。 変更が加えられると、Amazonで[!DNL Amazon Seller SKU]が共有するすべてのAmazonのリストが、同じ地域で販売されている（[store integration](./store-integration.md)の際に&#x200B;_[!UICONTROL Amazon Marketplace Country]_で定義されている）場合に影響を受けます。 米国で共有[!DNL Amazon Seller SKU]に対する変更は、（ストア統合時に定義された）別の地域用に設定されたAmazonストアには影響しません。

>[!NOTE]
>
>注文がAmazon(FBA)で処理され、注文がインポートされると、注文の詳細に一部のフィールドのダミーデータが表示されます。 [Amazon Order Details](./amazon-order-details.md)を参照してください。

## [!UICONTROL Fulfilled By]設定を構成します {#configure-fulfilled-by-settings}

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL Fulfilled By]_セクションを展開します。

1. **[!UICONTROL Product Fulfilled By]**&#x200B;の場合は、注文を実行する（出荷する）人を選択します。

   - `Fulfilled by Merchant`  — 商人が注文を完了。

   - `Fulfilled by Amazon` -Amazon倉庫は受注を完了。

   - `Assign Fulfilled By Using Magento Product Attribute`  — 属性 [!DNL Commerce] は、製品ごとの注文を実行するユーザーを示します。

      選択した場合、**[!UICONTROL Fulfilled by Attribute]**&#x200B;にマッピングする[!DNL Commerce]属性を選択します。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![実行者設定](assets/amazon-fulfilled-by.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | オプション：<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM)注文を満たす場合に選択します。注文が行われると、在庫が[!DNL Commerce]カタログから差し引かれます。 新しい製品が作成されると、Merchant Fullimentsの履行方法が割り当てられます。</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA)Amazonが注文を処理するかどうかを選択します。この履行方法では、注文が行われた際に、製品在庫が[!DNL Commerce]カタログから差し引かれることはありません。 製品を作成すると、_[!UICONTROL Fulfilled by Amazon (FBA)]_がフルフィルメントタイプとして作成されます。 [!DNL Amazon Seller Central]アカウント内で、製品がFBAを満たす資格があることを確認します。 FBAインベントリは、[!DNL Amazon Seller Central]アカウントを通じて直接管理されます。 このフルフィルメント方法では、数量の更新は[!DNL Commerce]カタログに対してプッシュされないので、[在庫/数量の設定](./stock-quantity.md)で説明されているマーケティングツールの一部を使用できません。</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]**  — マーチャントが履行するか、Amazonが [!DNL Commerce] 履行するかを決定する既存の属性があるかどうかを選択します。選択すると、**[!UICONTROL Fulfilled by Attribute]**&#x200B;が有効になります。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | フルフィルメント方法を決定するために使用する[!DNL Commerce]属性を選択します。<br><br>例えば、属性が「履行済 _期_ 間」で、属性値をまたはとして選択した場合、その値が新しい製品の履行タイプとして使用されま _[!UICONTROL Fulfilled By Merchant]_す_[!UICONTROL Fulfilled By Amazon (FBA)]_。マーチャントは、[!DNL Amazon Seller Central]アカウント内で製品がFBAに対応できることを確認する必要があります。 また、FBA在庫は、Amazonセラーアカウントを通じて直接管理されます。<br><br>オプションは、Amazon製品用に設定した属性によって異なります。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
