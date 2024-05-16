---
title: Amazon販売チャネル - [!UICONTROL Listing Price]
description: Amazon一覧の価格ソースと基本価格（デフォルト）値を決めるには、「一覧価格」設定を使用します。
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] 設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、次を定義します [!DNL Commerce] 価格ソースとして使用する価格設定属性。これは、Amazon一覧の基本価格（デフォルト）値です。 これらの設定は、で使用されます [価格ルール](./pricing-rule-general-settings.md) に設定した値を基準にAmazonのリスト価格を自動調整するには： _[!UICONTROL Magento Price Source]_.

を設定できます [価格範囲](./price-scope.md) グローバルまたは web サイトとして。 価格範囲がに設定されている場合 `Global`、すべてのストア/web サイトに単一の価格ソースがあります。 価格範囲がに設定されている場合 `Website`の場合、価格ソースでは web サイト価格（使用可能な場合）のフォールバックロジックに続いてデフォルト（グローバル）価格が使用されます。

リストルールが複数の web サイトに適用されるように設定されている場合、web サイトの価格の使用順序は、で定義されている web サイトの優先度設定によって決まります。 [リストルール](./listing-rules.md). これらのルールを使用すると、カタログ全体の製品価格を定義できます。 Web サイトの価格範囲を使用しているかどうかを確認するには、を参照してください。 [カタログの価格スコープ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

にリストされているオプション _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_、および _[!UICONTROL Strike Through Price (MSRP)]_設定済の価格設定属性を含めます。 価格設定属性は次のとおりです [!DNL Commerce] 「店舗所有者」の値が「カタログ入力タイプ」に設定されている製品属性 `Price`. 参照： [属性入力タイプ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## 上場価格設定の構成 {#configure-listing-price-settings}

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 _[!UICONTROL Listing Price]_セクション。

1. の場合 **[!UICONTROL Magento Price Source]** （必須）、オプションを選択します。

   デフォルトはです `Price`. この設定により、Amazonのリストに使用される価格ソースが決まります。 を作成する場合 [価格ルール](./pricing-products.md)ルールは、ここで選択した属性に対して定義された値に適用されます。 任意の設定済み価格設定属性を選択できます。 ただし、選択した属性が製品に入力されていない場合、製品の価格ソースはデフォルトでに戻ります `Price` 公開されたAmazonの上場価格を決定するために価格ルールが適用される場合。

1. **用[!UICONTROL Minimum Advertised Price (MAP)**]、オプションを選択します。

   デフォルトでは、何も選択されていません。 この設定により、商品の最低広告価格（MAP）が有効になります。 価格設定属性を定義し、製品の上場価格が決定された最低価格（価格設定ソースおよびルールに基づく）を下回ると、この値はリストのマップになります。 この設定を使用すると、を実装できます [価格ルール](./pricing-products.md)製品の最低価格を制御しながら。 リスト価格が低くなりすぎないようにするには、マップとして使用する価格設定属性を選択します。 ただし、選択した価格フィールドが製品に対して定義されていない場合、マップは使用されません。

1. の場合 **[!UICONTROL Strike Through Price (MSRP)]**、オプションを選択します。

   デフォルトでは、何も選択されていません。 この設定は、製品の製造元の推奨小売価格（MSRP）として使用される価格属性を決定します。 上場価格が定義された MSRP よりも低い場合、Amazonの上場は、上場価格が低い MSRP 価格のストライクスルーと、計算された「You Save」の金額およびパーセンテージで表示されます。 ただし、選択した価格フィールドが製品に対して定義されていない場合、MSRP は計算されません。

   >[!NOTE]
   >
   >この設定は、を獲得したリストにのみ適用されます [Buy Box](./buy-box-competitor-pricing.md) 位置。 Buy Boxは、FBA/Prime の配送、空室状況、売り手の業績などの他の要因と共に、通常は最高の価格でリストされた商品を持つ売り手にAmazonによって授与されます。

1. の場合 **付加価値税（VAT）の適用**、次のいずれかのオプションを選択します。

   - `Disabled` - （デフォルト）上場価格に VAT を適用しない場合に選択します。

   - `Enabled`  – 上場価格に VAT を適用する時期を選択します。 VAT は通常、ヨーロッパ諸国で消費税として使用され、Amazon内の最終的な上場価格に追加されます。 VAT は、インテリジェント価格ルール内で使用されるリストの最終価格には適用されません。ただし、 [床価格](./floor-price.md) がヒットした。

   >[!NOTE]
   >
   >欧州連合（EU）の企業は、顧客が税金を送金できるように、ビジネスバイヤーに請求書を送信する必要があります。 これらの請求書を作成して自分で税金を計算するか、Amazonの VAT 計算サービスなどの税金計算サービスを使用できます。 Amazonでは、に新規登録することをお勧めします [AmazonVAT 算定サービス](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). 別の方法を選択する場合は、VAT コンプライアンスに責任があります。>
   >
   >Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

1. の場合 **[!UICONTROL VAT Percentage]** VAT レートの値を入力してください。

   デフォルトはです `0.00`. この値は、上場価格に追加される VAT 金額の計算に使用されます。 次の場合 `10.2` を入力すると、10.20% の VAT がリスト価格に適用されます。 「付加価値税（VAT）の適用」フィールドが次のように設定されている場合、このフィールドは無効になります `Disabled`.

1. **（英国店舗のみ）** の場合 **[!UICONTROL Amazon Product Tax Code (PTC)]**、次のいずれかのオプションを選択します。

   - `Do Not Manage PTC` - （デフォルト）サードパーティの税金計算サービスを使用しているか、既にすべての税金計算をユーザーに設定しているかを選択します [!DNL Amazon Seller Central] アカウント。 これを選択すると、Amazonの営業チャネルから商品の税コードに関する情報が [!DNL Amazon Seller Central] アカウント。

   - `Set Default PTC`  – すべての製品に使用するユニバーサル製品税コード（PTC）があるかどうかを選択します。 選択した場合、完了する必要があります _[!UICONTROL Default PTC]_.

      - の場合 **[!UICONTROL Default PTC]**&#x200B;を選択し、適格なすべてのAmazonのリストで使用されるデフォルトの PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウント。このフィールドは空白のままにします。 このフィールドに加えた変更は、既存のAmazonのリストには影響しません。 既存のリストのデフォルト PTC を変更するには、リストを [ended](./end-listings-manually.md) 新しいリストが作成されました。

   >[!NOTE]
   >
   >Amazonの VAT 計算サービスを使用する場合は、商品の税分類を知っておく必要があります。 PTC は、EU での B2B 購入に対するAmazonの税分類 ID コードです。 参照： [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. の場合 **[!UICONTROL Currency Conversion]**、オプションを選択します。

   デフォルトはです `Disabled`. これらのオプションは、 [!DNL Commerce] [通貨](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) 設定。 使用できるオプションがない場合は、通貨設定を指定します。

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![上場価格](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Amazonのリストを作成する際に使用する価格ソースを指定します。 デフォルトはです `Price`. 次のような別の属性を選択した場合： `Amazon Price` または `Special Price`を指定した場合は、属性に定義された値がAmazonのリストに使用されます。 ただし、選択した属性が定義されていない場合、 `Price` が使用されます。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | この [!DNL Commerce] マップ価格の属性。 リスト価格が MAP 価格より低い場合、MAP オプションを選択すると、Amazon リストが MAP 価格に自動的に設定されます。 |
| [!UICONTROL Strike Through Price (MSRP)] | この [!DNL Commerce] msrp 価格を表す属性です。 Amazonの上場価格が MSRP よりも低い場合は、MSRP 価格と上場価格のストライクスルーが表示されます。 この設定は、「You Save」の金額とパーセンテージの計算にも使用されますが、この機能は、 [Buy Box](./buy-box-competitor-pricing.md) 位置。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | VAT は EU の売り手によって使用されます。<br><br>を選択 `Disabled` リスト価格に VAT を追加したくない場合。<br><br>を選択 `Enabled` 次に、VAT 率を入力して、リスト価格に VAT を適用します。 |
| [!UICONTROL VAT Percentage] | Amazon一覧の一覧価格に追加される VAT 金額の計算に使用する割合を指定します。 <br><br>次のように入力します `5`その後、5% の VAT がすべての価格ルールが適用された後、最終上場価格に適用されます。 VAT 税は、インテリジェントな価格設定ルール内で使用されるリストの最終価格には適用されません（次の場合を除く） [floor](./floor-price.md) または [上限](./optional-ceiling-price.md) がヒットした。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （英国の店舗にのみ表示）Amazonのセールスチャネルから商品の税コード情報を [!DNL Amazon Seller Central] アカウント。 <br><br>を選択 **PTC を管理しない** サードパーティの税金計算サービスを使用している場合、またはで既にすべての税金計算を設定している場合 [!DNL Amazon Seller Central] アカウント。 このオプションを選択すると、Amazonの営業チャネルから商品の税コード情報が [!DNL Amazon Seller Central] アカウント。<br><br>を選択 **デフォルトの PTC を設定** すべての製品に使用するユニバーサル製品税コードがある場合。<br><br>参照： [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | 次の場合にのみ表示： **Amazon製品税コード（PTC）** はに設定されています。 `Set Default PTC`. すべての適格なAmazonのリストで使用されるデフォルトの PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウント。このフィールドは空白のままにします。 <br><br>このフィールドに加えた変更は、既存の一覧には影響しません。 リストは、 [ended](./end-listings-manually.md) 新しいリストが作成され、変更が反映されます。 |
| [!UICONTROL Currency Conversion] | さんがを許可 [!DNL Commerce] ストアフロントのデフォルト通貨Amazonのデフォルト通貨に正確に変換して、適切な通貨でリスト価格を公開します。 通貨換算は、常にユーザーの [!DNL Commerce] デフォルトの通貨。<br><br>デフォルトの設定は引き続き表示されます [!DNL Commerce] 他の通貨が使用可能な場合はおよびAmazonの通貨。 デフォルトの [!DNL Commerce] 通貨はデフォルトのAmazon通貨と一致します。通貨換算は無効のままにします。<br><br>例えば、次のような場合 [!DNL Commerce] デフォルト通貨は CAD （カナダ・ドル）で、Amazonのデフォルト通貨は USD です。「通貨換算」を使用可能にし、「換算レート CAD」から「USD」を選択する必要があります。 表示されるオプションは、ビルトインに基づいています [!DNL Commerce] 通貨換算。 探しているオプションが表示されない場合は、 [通貨の設定： [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
