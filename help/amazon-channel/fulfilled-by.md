---
title: によって満たされる
description: 「フルフィルメント」設定を使用して、Amazon リストからの注文がどのように履行されるかを指定します。
redirect_from: /sales-channels/asc/ob-fulfilled-by.html
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# によって満たされる

_[!UICONTROL Fulfilled By]_設定は、ストア一覧の設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

この設定では、注文を履行する (または出荷する) 当事者を指定します。 1つの方法ですべての注文が満たされている場合は、「マーチャント (ご購入)」または「Amazon」のいずれかを選択します。 現在の場所から、Amazon を使用して注文を行う予定がある場合は、3番目のオプションを使用して、product 属性を設定することをお勧めし [!DNL Commerce] ます。

- **[!UICONTROL Fulfilled by Merchant]** -商人がすべての注文を受け付けた場合に選択します。 注文が行われると、カタログから在庫が差し引かれ [!DNL Commerce] ます。

- **[!UICONTROL Fulfilled by Amazon]** -Amazon によってすべての注文が満たされるかどうかを選択します。 このオプションを使用すると、 [!DNL Commerce] 注文が発生したときにカタログから製品インベントリが控除されません。 Amazon 履行注文の在庫在庫が倉庫に格納および控除されます。 このオプションを割り当てる前に、 [!DNL Amazon Seller Central] _Amazon_ (FBA) フルフィルメントによって製品が満たされていることをご確認ください。 FBA インベントリは、アカウントを使用して直接管理され [!DNL Amazon Seller Central] ます。 このフルフィルメント方法を使用すると、Amazon sales channel で、Amazon の間に数量が更新されることはありません [!DNL Commerce] 。 そのため、「Quantity」設定で説明されているすべてのマーケティングツールが Amazon sales channel では使用できないようになっています。

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** -お客様と Amazon によって製品が履行される可能性がある場合は、この値を使用して、 [!DNL Commerce] amazon によって履行され、フルフィルメントによって履行される値を含む product 属性を作成することもできます。 製品ごとにこの値を設定すると、注文を履行したユーザーが表示されます。

フルフィルメントメソッドは、 **[!UICONTROL Amazon Marketplace Country]** ストア統合時に定義された設定に基づいて、地域によって異なり [ ](./store-integration.md) ます。 変更が加えられると、その変更は、 [!DNL Amazon Seller SKU] amazon stores によって同じ地域 (ストア統合時に定義されて _[!UICONTROL Amazon Marketplace Country]_います) 内で販売されているすべての amazon リストに反映され [ ](./store-integration.md) ます。 米国で共有に変更を [!DNL Amazon Seller SKU] 加えても、異なる地域に設定された Amazon store には影響しません (ストア統合の際に定義されています)。

>[!NOTE]
>
>Amazon (FBA) によって注文が満たされ、注文がインポートされると、注文明細の一部のフィールドについてダミーデータが表示されます。 「 [ Amazon Order Details」を参照してください ](./amazon-order-details.md) 。

## 設定を構成します。 [!UICONTROL Fulfilled By] {#configure-fulfilled-by-settings}

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL Fulfilled By]_ます。

1. については **[!UICONTROL Product Fulfilled By]** 、次のいずれかを選択してください。

   - `Fulfilled by Merchant` -商人が注文を満たしていることを指定します。

   - `Fulfilled by Amazon` -Amazon warehouse が注文を満たしていることを指定します。

   - `Assign Fulfilled By Using Magento Product Attribute` - [!DNL Commerce] 属性は製品ごとの注文の履行者を示します。

      このオプションを選択した場合は、 [!DNL Commerce] マップする属性を選択し **[!UICONTROL Fulfilled by Attribute]** ます。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![設定によって満たされる](assets/amazon-fulfilled-by.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | オプション：<ul><li>**[!UICONTROL Fulfilled by Merchant]** (FBM) 注文を履行する場合に選択します。 注文が行われると、カタログから在庫が差し引かれ [!DNL Commerce] ます。 新製品を作成すると、マーチャントフルフィルメントのフルフィルメント方法が割り当てられます。</li><li>**[!UICONTROL Fulfilled by Amazon]** -(FBA) その注文が Amazon によって満たされるかどうかを選択します。 このフルフィルメント方法では、 [!DNL Commerce] 注文が発生したときに、カタログから製品インベントリが控除されません。 作成された製品は、 _[!UICONTROL Fulfilled by Amazon (FBA)]_フルフィルメントタイプとして作成されます。 お客様の製品が、アカウント内の FBA のフルフィルメント対象となることを確認してください [!DNL Amazon Seller Central] 。 FBA インベントリは、アカウントを使用して直接管理することも [!DNL Amazon Seller Central] できます。 このフルフィルメント方法を使用した場合、数量の更新はカタログに対しては実行されないので、 [!DNL Commerce] [ Stock/quantity 設定で説明されているようなマーケティングツールを使用することはできません ](./stock-quantity.md) 。</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** -この属性を使用して、 [!DNL Commerce] その属性がマーチャントによって満たされるか、Amazon によって履行されるかを決定する既存の属性があるかどうかを選択します。 選択すると、が **[!UICONTROL Fulfilled by Attribute]** 有効になります。</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | [!DNL Commerce]フルフィルメント方法を決定するために使用する属性を選択します。<br><br>例えば、その属性が「in」に設定されている場合、 __ またはによって属性値を指定すると、 _[!UICONTROL Fulfilled By Merchant]__[!UICONTROL Fulfilled By Amazon (FBA)]_ その値が新製品のフルフィルメントタイプとして使用されます。 マーチャントは、お客様の製品が、アカウント内の FBA の履行対象となることを確認する必要があり [!DNL Amazon Seller Central] ます。 FBA インベントリは、Amazon 売り手アカウントを使用して直接管理することもできます。<br><br>オプションは、Amazon 製品用に設定された属性によって異なります。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
