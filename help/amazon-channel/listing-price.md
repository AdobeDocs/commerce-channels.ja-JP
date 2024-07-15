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

[!UICONTROL Listing Price] の設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定は [!DNL Commerce] 価格ソースとして使用する価格設定属性を定義します。価格ソースは、Amazonリストのベース（デフォルト）の価格値です。 これらの設定は [ 価格ルール ](./pricing-rule-general-settings.md) で使用され、_[!UICONTROL Magento Price Source]_の値セットを基準にAmazonのリスト価格を自動調整します。

[ 価格範囲 ](./price-scope.md) をグローバルまたは web サイトとして設定できます。 価格範囲が `Global` に設定されている場合、すべての店舗/web サイトに単一の価格ソースがあります。 価格範囲が `Website` に設定されている場合、価格ソースでは、web サイト価格（使用可能な場合）のフォールバックロジックに続いてデフォルト（グローバル）価格が使用されます。

リストルールが複数の web サイトに適用されるように設定されている場合、web サイトの価格の使用順序は、[ リストルール ](./listing-rules.md) で定義されている web サイトの優先度設定によって決まります。 これらのルールを使用すると、カタログ全体の製品価格を定義できます。 Web サイトの価格範囲を使用しているかどうかを確認するには、[ カタログの価格範囲 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html) を参照してください。

_[!UICONTROL Magento Price Source]_、_[!UICONTROL Minimum Advertised Price (Map)]_、_[!UICONTROL Strike Through Price (MSRP)]_にリストされたオプションには、設定済みの価格設定属性が含まれます。 価格設定属性は、「店舗所有者のカタログ入力タイプ」の値が「`Price`」に設定された [!DNL Commerce] 品属性です。 [ 属性入力タイプ ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html) を参照してください。

## 上場価格設定の構成 {#configure-listing-price-settings}

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL Listing Price]_」セクションを展開します。

1. **[!UICONTROL Magento Price Source]** （必須）の場合は、オプションを選択します。

   デフォルトは `Price` です。 この設定により、Amazonのリストに使用される価格ソースが決まります。 [ 価格ルール ](./pricing-products.md) を作成すると、ここで選択した属性に対して定義された値にルールが適用されます。 任意の設定済み価格設定属性を選択できます。 ただし、商品に対して選択した属性が入力されていない場合、公開されているAmazonの上場価格を決定するための価格設定ルールが適用されると、商品の価格ソースがデフォルトで `Price` に戻ります。

1. **[!UICONTROL Minimum Advertised Price (MAP)**] の場合は、オプションを選択します。

   デフォルトでは、何も選択されていません。 この設定により、商品の最低広告価格（MAP）が有効になります。 価格設定属性を定義し、製品の上場価格が決定された最低価格（価格設定ソースおよびルールに基づく）を下回ると、この値はリストのマップになります。 この設定を使用すると、製品の最低価格を制御しながら [ 価格ルール ](./pricing-products.md) を実装できます。 リスト価格が低くなりすぎないようにするには、マップとして使用する価格設定属性を選択します。 ただし、選択した価格フィールドが製品に対して定義されていない場合、マップは使用されません。

1. **[!UICONTROL Strike Through Price (MSRP)]** の場合は、オプションを選択します。

   デフォルトでは、何も選択されていません。 この設定は、製品の製造元の推奨小売価格（MSRP）として使用される価格属性を決定します。 上場価格が定義された MSRP よりも低い場合、Amazonの上場は、上場価格が低い MSRP 価格のストライクスルーと、計算された「You Save」の金額およびパーセンテージで表示されます。 ただし、選択した価格フィールドが製品に対して定義されていない場合、MSRP は計算されません。

   >[!NOTE]
   >
   >この設定は、[Buy Box](./buy-box-competitor-pricing.md) の順位を獲得したリストにのみ適用されます。 Buy Boxは、FBA/Prime の配送、空室状況、売り手の業績などの他の要因と共に、通常は最高の価格でリストされた商品を持つ売り手にAmazonによって授与されます。

1. **付加価値税（VAT）の適用）** オプションを選択します。

   - `Disabled` - （デフォルト）上場価格に VAT を適用しない場合に選択します。

   - `Enabled` – 上場価格に VAT を適用するタイミングを選択します。 VAT は通常、ヨーロッパ諸国で消費税として使用され、Amazon内の最終的な上場価格に追加されます。 VAT は、インテリジェントな価格設定ルール内で使用されるリストの最終価格には適用されません。ただし、[ 最低価格 ](./floor-price.md) が当たっている場合は除きます。

   >[!NOTE]
   >
   >欧州連合（EU）の企業は、顧客が税金を送金できるように、ビジネスバイヤーに請求書を送信する必要があります。 これらの請求書を作成して自分で税金を計算するか、Amazonの VAT 計算サービスなどの税金計算サービスを使用できます。 Amazonでは、[Amazon VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;) に新規登録することをお勧めします。 別の方法を選択する場合は、VAT コンプライアンスに責任があります。>
   >
   >Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

1. **[!UICONTROL VAT Percentage]**: VAT レートの値を入力します。

   デフォルトは `0.00` です。 この値は、上場価格に追加される VAT 金額の計算に使用されます。 `10.2` を入力すると、10.20% の VAT がリスト価格に適用されます。 「付加価値税（VAT）の適用」フィールドが「`Disabled`」に設定されている場合、このフィールドは無効になります。

1. **（英国ストアのみ）****[!UICONTROL Amazon Product Tax Code (PTC)]** の場合は、次のいずれかのオプションを選択します。

   - `Do Not Manage PTC` - （デフォルト）サードパーティの税金計算サービスを使用しているか、既にすべての税金計算が [!DNL Amazon Seller Central] ーザーのアカウントで設定されている場合を選択します。 これを選択すると、Amazonの営業チャネルから [!DNL Amazon Seller Central] アカウントに商品税コード情報が送信されなくなります。

   - `Set Default PTC` – すべての製品に使用するユニバーサル製品税コード（PTC）があるかどうかを選択します。 選択した場合、_[!UICONTROL Default PTC]_を完了する必要があります。

      - **[!UICONTROL Default PTC]** の場合、すべての適格なAmazonリストに使用されるデフォルトの PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウントに設定されている場合は、このフィールドを空白のままにします。 このフィールドに加えた変更は、既存のAmazonのリストには影響しません。 既存のリストのデフォルト PTC を変更するには、リストを [ 終了 ](./end-listings-manually.md) し、新しいリストを作成する必要があります。

   >[!NOTE]
   >
   >Amazonの VAT 計算サービスを使用する場合は、商品の税分類を知っておく必要があります。 PTC は、EU での B2B 購入に対するAmazonの税分類 ID コードです。 [Amazonの製品税コード ](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} を参照してください。

1. **[!UICONTROL Currency Conversion]** の場合は、オプションを選択します。

   デフォルトは `Disabled` です。 これらのオプションは、[!DNL Commerce][ 通貨 ](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) 設定によって異なります。 使用できるオプションがない場合は、通貨設定を指定します。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ 上場価格 ](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Amazonのリストを作成する際に使用する価格ソースを指定します。 デフォルトは `Price` です。 `Amazon Price` や `Special Price` などの別の属性を選択した場合、属性に対して定義された値は、Amazonのリストに使用されます。 ただし、選択した属性が定義されていない場合、`Price` が使用されます。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | MAP 価格の [!DNL Commerce] 属性。 リスト価格が MAP 価格より低い場合、MAP オプションを選択すると、Amazon リストが MAP 価格に自動的に設定されます。 |
| [!UICONTROL Strike Through Price (MSRP)] | MSRP 価格を表す [!DNL Commerce] 属性。 Amazonの上場価格が MSRP よりも低い場合は、MSRP 価格と上場価格のストライクスルーが表示されます。 この設定は、「You Save」の金額とパーセンテージの計算にも使用されますが、この機能は、[Buy Box](./buy-box-competitor-pricing.md) の順位を獲得したリストにのみ適用されます。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | VAT は EU の売り手によって使用されます。<br><br> リスト価格に VAT を追加しない場合は、`Disabled` を選択します。<br><br> 「`Enabled`」を選択し、VAT 率を入力して、上場価格に VAT を適用します。 |
| [!UICONTROL VAT Percentage] | Amazon一覧の一覧価格に追加される VAT 金額の計算に使用する割合を指定します。 <br><br>`5` を入力すると、すべての価格ルールが適用された後、最終的な上場価格に 5% の VAT が適用されます。 VAT 税は、インテリジェントな価格設定ルール内で使用されるリストの最終価格には適用されません。ただし、[floor](./floor-price.md) または [ceiling](./optional-ceiling-price.md) が当たっている場合は除きます。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （英国の店舗にのみ表示されます）Amazonのセールスチャネルから [!DNL Amazon Seller Central] アカウントに商品税コード情報を送信するかどうかを指定します。 <br><br> サードパーティの税金計算サービスを使用している場合、または [!DNL Amazon Seller Central] アカウントですべての税金計算が設定されている場合は、「**PTC を管理しない**」を選択します。 このオプションを選択すると、Amazon営業チャネルから [!DNL Amazon Seller Central] アカウントに商品税コード情報が送信されません。<br><br> すべての製品に使用するユニバーサル製品税コードがある場合は、「**デフォルト PTC を設定**」を選択します。<br><br>[Amazonの商品税コードを参照してください ](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}。 |
| [!UICONTROL Default PTC] | **Amazon Product Tax Code （PTC）** が `Set Default PTC` に設定されている場合にのみ表示されます。 すべての適格なAmazonのリストで使用されるデフォルトの PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウントに設定されている場合は、このフィールドを空白のままにします。 <br><br> このフィールドに加えた変更は、既存のリストには影響しません。 リストを [ 終了 ](./end-listings-manually.md) し、変更を有効にするために新しいリストを作成する必要があります。 |
| [!UICONTROL Currency Conversion] | [!DNL Commerce] ストアフロントのデフォルト通貨を使用して、デフォルトのAmazon通貨に正確に変換し、適切な通貨でリスト価格を公開できます。 通貨換算は、常に [!DNL Commerce] のデフォルト通貨に基づきます。<br><br> 他の通貨が使用可能な場合でも、デフォルトの [!DNL Commerce] およびAmazonの通貨を表示できます。 デフォルトの [!DNL Commerce] 通貨がデフォルトのAmazon通貨と一致する場合は、通貨換算を無効のままにします。<br><br> 例えば、[!DNL Commerce] のデフォルト通貨が CAD （カナダドル）で、Amazonのデフォルト通貨が USD の場合、「通貨換算」を使用可能にし、「換算レート CAD」を USD に選択する必要があります。 表示されるオプションは、組み込みの [!DNL Commerce] 通貨コンバージョンに基づいています。 探しているオプションが表示されない場合は、[ 通貨の設定  [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html) を行います。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
