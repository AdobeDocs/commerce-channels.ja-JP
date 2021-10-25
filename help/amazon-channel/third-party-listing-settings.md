---
title: サードパーティリスト
description: サードパーティリストの設定を更新すると、既存の Amazon 売り手の中央の一覧から、Commerce カタログに製品がインポートされるかどうかが決まります。
redirect_from: /sales-channels/asc/ob-third-party-listings.html
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# サードパーティリスト

サードパーティリストの設定は、ストアリストの設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

この設定によって、 [!DNL Commerce] 既存の一覧から製品がカタログによりインポートされるかどうかが決まり [!DNL Amazon Seller Central] ます。 どのリストにも一致する製品が含まれていることを確認するには、Amazon から一覧を読み込んでおくことをお勧めし [!DNL Commerce] ます。 リストがカタログに含まれている場合は [!DNL Commerce] 、すべての製品を1つのカタログから管理し、Amazon 販売チャンネルの機能を使用することができます。 このような機能には、Amazon、知的価格のインテリジェントな価格設定、数量管理などの注文管理が含まれています。

Amazon の一覧をインポートするように構成されている場合、amazon sales channel によって Amazon リストがカタログにインポートされ [!DNL Commerce] 、既存の製品に適合させようとします。 自動的に検索が実行されない場合は、Amazon リストを新製品として読み込む [!DNL Commerce] か、またはこの一覧を製品に手動で一致させることができます。

Amazon の一覧をインポートすることを選択した場合は、 [!DNL Commerce] Amazon 売り手 SKU と AMAZON アークの値を含む属性を選択します。 製品属性が設定されていない場合は [!DNL Commerce] [ ](./ob-creating-magento-attributes.md) 、その作成および割り当てを検討してください。 これらの属性をマッピングすることで、インポートされた Amazon リストを製品に正確に一致させることができ [!DNL Commerce] ます。

最初のリストインポートは、 [ ストア統合 ](./store-integration.md) が完了すると開始されます。 Cron 設定に基づいて、その後、 [!DNL Commerce] 新しく追加された amazon リスト (Amazon Sales チャンネルで作成されていません) があるかどうかがチェックされ、 [!DNL Commerce] サードパーティの一覧設定に基づいてカタログが更新されます。

## サードパーティの一覧設定を構成します。

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL Third Party Listings]_ます。

1. **[!UICONTROL Import Third Party Listings]**(必須) には、次のいずれかのオプションを選択します。

   - `Import Listing` -(デフォルト) Amazon リストの製品情報を製品カタログにインポートする場合は、このオプションを選択し [!DNL Commerce] ます。 このオプションは初期設定であり、推奨されます。

   - `Do Not Import Listing` - [ 新規 _blank 製品を作成して、 ](https://docs.magento.com/user-guide/catalog/products.html) Amazon リストのカタログに手動で作成して割り当てる時期を選択し [!DNL Commerce] ます。
   >[!NOTE]
   >次のオプションフィールドは、「」に設定されている場合にのみ有効に `Import Listing` なります。

1. については **[!UICONTROL Attribute That Contains Amazon Seller SKU]** 、 [!DNL Commerce] AMAZON 売り手 SKU 値に一致する属性を選択します。

1. **[!UICONTROL Attribute That Contains Amazon ASIN]**&#x200B;で、 [!DNL Commerce] 作成した属性を Amazon サインに合わせるように選択します。

   >[!NOTE]
   >このような [!DNL Commerce] amazon リストの属性を作成していない場合は、 [ amazon 照合用の属性の作成を参照してください ](./ob-creating-magento-attributes.md) 。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![サードパーティリスト](assets/amazon-third-party-listings.png)

| 名 | つい |
|---|---|
| [!UICONTROL Import Third Party Listings] | 必須。 オプション：<ul><li>**[!UICONTROL Import Listing]** -(デフォルト) Amazon リストの製品情報を製品カタログにインポートする場合は、このオプションを選択し [!DNL Commerce] ます。 </li><li>**[!UICONTROL Do Not Import Listing]** - [ 新規 _blank 製品を作成して、 ](https://docs.magento.com/user-guide/catalog/products.html) Amazon リストのカタログに手動で作成して割り当てる時期を選択し [!DNL Commerce] ます。</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | 「」に設定されている場合にのみアクティブに `Import Listing` なります。<br>[!DNL Commerce]Amazon 売り手 SKU の amazon 属性と一致するように属性を選択します。この属性が存在しない場合は、 [ Amazon 合致に使用する Amazon 製品属性の作成を参照してください ](./ob-creating-magento-attributes.md) 。 必要に応じて、属性を確認 [!DNL Commerce] [ し、 ](./managing-attributes.md) その Amazon データと一致するように属性を作成または編集してください。 |
| [!UICONTROL Attribute That Contains Amazon ASIN] | 「」に設定されている場合にのみアクティブに `Import Listing` なります。<br>[!DNL Commerce]Amazon アークサインの amazon 属性に一致する属性を選択します。この属性が存在しない場合は、 [ Amazon 合致に使用する Amazon 製品属性の作成を参照してください ](./ob-creating-magento-attributes.md) 。 必要に応じて、属性を確認 [!DNL Commerce] [ し、 ](./managing-attributes.md) その Amazon データと一致するように属性を作成または編集してください。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
