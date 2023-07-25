---
title: Amazonセールスチャネル — [!UICONTROL Listing Price]
description: 「Listing Price」設定を使用して、価格のソースおよびAmazonの定価の基準（デフォルト）値を決定します。
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] 設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定で定義される [!DNL Commerce] 価格属性を価格ソースとして使用します。価格属性は、Amazonリストの基準（デフォルト）価格値です。 これらの設定は、 [価格ルール](./pricing-rule-general-settings.md) Amazonの定価を _[!UICONTROL Magento Price Source]_.

次の項目を設定します。 [価格の範囲](./price-scope.md) グローバルまたは web サイトとして。 価格設定範囲が `Global`の場合、すべてのストア/Web サイトに対して 1 つの価格ソースがあります。 価格設定範囲が `Website`の場合、価格ソースは、web サイト価格（利用可能な場合）のフォールバックロジックを使用し、その後にデフォルト（グローバル）価格が続きます。

複数の Web サイトに適用するリストルールが設定されている場合、Web サイトの価格が使用される順序は、 [リストルール](./listing-rules.md). これらのルールを使用すると、カタログ全体で製品の価格を定義できます。 Web サイトの価格範囲を使用しているかどうかを確認するには、 [カタログ価格範囲](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

次に示すオプション _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_、および _[!UICONTROL Strike Through Price (MSRP)]_設定した価格属性を含めます。 価格設定属性は、 [!DNL Commerce] 「ストア所有者」の「カタログ入力タイプ」が「 `Price`. 詳しくは、 [属性入力タイプ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## 定価の設定 {#configure-listing-price-settings}

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL Listing Price]_」セクションに入力します。

1. の場合 **[!UICONTROL Magento Price Source]** （必須）」で、オプションを選択します。

   デフォルトはです。 `Price`. この設定は、Amazonの一覧表に使用する価格のソースを決定します。 次の場合、 [価格ルール](./pricing-products.md)の場合、ここで選択した属性に対して定義された値にルールが適用されます。 設定済みの価格設定属性を選択できます。 ただし、選択した属性が製品に対して入力されない場合、製品の価格ソースはデフォルトでに戻ります。 `Price` 公開されているAmazon上場価格を決定するために価格ルールを適用する場合。

1. **[!UICONTROL Minimum Advertised Price (MAP)**]、「 」オプションを選択します。

   デフォルトは選択なしです。 この設定は、製品の最小アドバタイズ価格 (MAP) を有効にします。 価格属性を定義し、製品の上場価格が（価格設定ソースおよびルールに基づいて）決定された最小価格を下回る場合、この値はリストの MAP になります。 この設定を使用すると、 [価格ルール](./pricing-products.md)を使用します。 上場価格が低すぎないようにするには、MAP として使用する価格属性を選択します。 ただし、選択した価格設定フィールドが製品に対して定義されていない場合、MAP は使用されません。

1. の場合 **[!UICONTROL Strike Through Price (MSRP)]**、「 」オプションを選択します。

   デフォルトは選択なしです。 この設定により、製造元が製品に対して提案する小売価格 (MSRP) として使用する価格属性が決定されます。 上場価格が定義された MSRP より小さい場合、Amazonのリストには、MSRP 価格の打ち消し線と共に、より低い上場価格が表示されます。また、計算された「保存済み」金額と割合も表示されます。 ただし、選択した価格フィールドが製品に対して定義されていない場合、MSRP は計算されません。

   >[!NOTE]
   >
   >この設定は、次の条件を満たすリストにのみ適用されます： [Buy Box](./buy-box-competitor-pricing.md) 位置。 Buy Boxは、通常最高の価格でリストされる製品を持つ販売者にAmazonが与え、FBA/Prime 出荷の提供、可用性、販売者のパフォーマンスなどの他の要因と共に。

1. の場合 **付加価値税 (VAT) の適用**、オプションを選択します。

   - `Disabled` - （デフォルト）VAT を定価に適用しない場合に選択します。

   - `Enabled`  — 上場価格に VAT を適用するタイミングを選択します。 VAT は通常、ヨーロッパ諸国で消費税として使用され、Amazon内の最終上場価格に追加されます。 VAT は、インテリジェント価格ルール内で使用されるリストの最終価格には適用されません。ただし、 [価格](./floor-price.md) がヒットされた。

   >[!NOTE]
   >
   >EU（欧州連合）の企業は、顧客が税金を送金できるように、ビジネスバイヤーに請求書を送信する必要があります。 これらの請求書を生成して税金を自分で計算するか、Amazonの VAT 計算サービスなどの税金計算サービスを使用できます。 Amazonは [AmazonVAT 計算サービス](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). 別の方法を選択する場合は、VAT コンプライアンスに対する責任を負います。>
   >
   >Amazonが VAT 計算サービスアカウントを検証および有効化するまでに 10 ～ 14 日かかる場合があります。

1. の場合 **[!UICONTROL VAT Percentage]**」に、VAT 率の値を入力します。

   デフォルトはです。 `0.00`. この値は、上場価格に追加される VAT 金額の計算に使用されます。 If `10.2` を入力した場合、10.20%VAT が上場価格に適用されます。 「付加価値税 (VAT) の適用」フィールドが「 `Disabled`.

1. **（英国店舗のみ）** の場合 **[!UICONTROL Amazon Product Tax Code (PTC)]**、オプションを選択します。

   - `Do Not Manage PTC` - （デフォルト）サード・パーティの税金計算サービスを使用している場合、またはすべての税金計算を [!DNL Amazon Seller Central] アカウント 選択すると、Amazonの販売チャネルは製品税コード情報を [!DNL Amazon Seller Central] アカウント

   - `Set Default PTC`  — すべての製品に使用するユニバーサル製品税コード (PTC) がある場合に選択します。 選択した場合は、 _[!UICONTROL Default PTC]_.

      - の場合 **[!UICONTROL Default PTC]**」に、すべての適格なAmazonリストに使用するデフォルトの PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウントの場合、このフィールドは空白のままにします。 このフィールドに加えた変更は、既存のAmazonリストには影響しません。 既存のリストのデフォルト PTC を変更するには、リストが [終了](./end-listings-manually.md) と新しいリストが作成されました。

   >[!NOTE]
   >
   >Amazonの VAT 計算サービスを使用する場合は、製品の税金カテゴリを把握しておく必要があります。 PTC は、Amazonでの B2B 購入に対する EU での税金カテゴリ ID コードです。 詳しくは、 [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. の場合 **[!UICONTROL Currency Conversion]**、「 」オプションを選択します。

   デフォルトはです。 `Disabled`. これらのオプションは、 [!DNL Commerce] [通貨](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) 設定。 使用できるオプションがない場合は、通貨設定を指定します。

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![上場価格](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Amazonの一覧を作成する際に使用する価格ソースを決定します。 デフォルトはです。 `Price`. 別の属性 ( `Amazon Price` または `Special Price`の場合、属性の定義された値がAmazonのリストに使用されます。 ただし、選択した属性が定義されていない場合、 `Price` が使用されます。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | この [!DNL Commerce] MAP 価格設定の属性。 「MAP」オプションを選択すると、Amazonリストが MAP 価格より小さい場合は、MAP 価格に自動的に設定されます。 |
| [!UICONTROL Strike Through Price (MSRP)] | この [!DNL Commerce] MSRP 価格を表す属性。 Amazonの上場価格が MSRP より小さい場合は、MSRP 価格と上場価格のストライクスルーが表示されます。 この設定は、「保存中」の金額と割合の計算にも使用されますが、この機能は、 [Buy Box](./buy-box-competitor-pricing.md) 位置。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | VAT は、EU で販売者によって使用されます。<br><br>選択 `Disabled` 上場価格に VAT を追加したくない場合。<br><br>選択 `Enabled` 次に、VAT を上場価格に適用するための VAT 割合を入力します。 |
| [!UICONTROL VAT Percentage] | Amazon一覧の価格表に追加される VAT 金額の計算に使用する割合を定義します。 <br><br>次を入力すると、 `5`の場合、すべての価格設定ルールが適用された後、最終的な上場価格に 5%の VAT が適用されます。 VAT 税は、インテリジェント価格ルール内で使用されるリストの最終価格には適用されません。ただし、 [floor](./floor-price.md) または [ceiling](./optional-ceiling-price.md) がヒットされた。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | （UK Stores 専用） Amazonの販売チャネルが製品税コード情報を [!DNL Amazon Seller Central] アカウント <br><br>選択 **PTC を管理しない** サードパーティの税金計算サービスを使用している場合、またはすべての税金計算が [!DNL Amazon Seller Central] アカウント このオプションに設定すると、Amazonの販売チャネルは製品税コード情報を [!DNL Amazon Seller Central] アカウント<br><br>選択 **デフォルト PTC を設定** すべての製品に使用するユニバーサル製品税コードがある場合。<br><br>詳しくは、 [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | 次の場合にのみ表示されます **Amazon製品税コード (PTC)** が `Set Default PTC`. すべての適格なAmazon・リストに使用するデフォルト PTC を入力します。 デフォルトの PTC が [!DNL Amazon Seller Central] アカウントの場合、このフィールドは空白のままにします。 <br><br>このフィールドに対して行った変更は、既存のリストには影響しません。 リストは [終了](./end-listings-manually.md) 変更を有効にするために新しいリストが作成されました。 |
| [!UICONTROL Currency Conversion] | 次の条件を満たす [!DNL Commerce] storefront のデフォルト通貨を使用して、リスト価格を適切な通貨で公開するために、デフォルトのAmazon通貨に正確に変換します。 通貨換算は、常に [!DNL Commerce] デフォルトの通貨。<br><br>デフォルトの [!DNL Commerce] 他の通貨が使用可能な場合はAmazonの通貨 デフォルトの [!DNL Commerce] 通貨はデフォルトのAmazon通貨と一致し、通貨コンバージョンは無効のままにします。<br><br>例えば、 [!DNL Commerce] デフォルトの通貨は CAD（カナダドル）で、Amazonのデフォルトの通貨は USD です。通貨換算を有効にし、換算レート CAD から USD を選択する必要があります。 表示されるオプションは、組み込みの [!DNL Commerce] 通貨換算。 探しているオプションが表示されない場合は、 [通貨を設定する [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
