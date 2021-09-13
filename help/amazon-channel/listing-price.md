---
title: 上場価格
description: Listing Price設定を使用して、価格のソースとAmazon Listingsの基準（デフォルト）価格を決定します。
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# 上場価格

[!UICONTROL Listing Price] 設定は、ストアリスト設定の一部です。リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定は、価格ソースとして使用する[!DNL Commerce]価格属性を定義します。これは、Amazonリストの基準（デフォルト）価格値です。 これらの設定は、[の価格ルール](./pricing-rule-general-settings.md)で使用され、_[!UICONTROL Magento Price Source]_に設定された値に対してAmazonの上場価格を自動的に調整します。

[価格範囲](./price-scope.md)は、グローバルまたはWebサイトとして設定できます。 価格の範囲が`Global`に設定されている場合、すべての店舗/Webサイトに対して1つの価格のソースが存在します。 価格範囲が`Website`に設定されている場合、価格ソースは、Webサイト価格（利用可能な場合）のフォールバックロジックに続いて、デフォルト（グローバル）価格を使用します。

複数のWebサイトに対してリストルールを適用するように設定した場合、Webサイト価格が使用される順序は、[リストルール](./listing-rules.md)で定義されたWebサイトの優先度設定によって決まります。 これらのルールを使用すると、カタログ全体で製品の価格を定義できます。 Webサイトの価格範囲を使用しているかどうかを確認するには、[カタログ価格範囲](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}を参照してください。

_[!UICONTROL Magento Price Source]_、_[!UICONTROL Minimum Advertised Price (Map)]_&#x200B;および&#x200B;_[!UICONTROL Strike Through Price (MSRP)]_に示すオプションには、設定済みの価格属性が含まれます。 価格属性は[!DNL Commerce]製品属性で、「店舗所有者」の「カタログ入力タイプ」が`Price`に設定されています。 [属性入力タイプ](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}を参照してください。

## 定価の設定 {#configure-listing-price-settings}

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL Listing Price]_セクションを展開します。

1. **[!UICONTROL Magento Price Source]**（必須）には、オプションを選択します。

   デフォルトは`Price`です。 この設定は、Amazonリストに使用する価格のソースを決定します。 [価格ルール](./pricing-products.md)を作成した場合、ここで選択した属性に定義された値にルールが適用されます。 任意の設定済み価格属性を選択できます。 ただし、選択した属性が製品に対して入力されていない場合は、公開されているAmazonの価格を決定するために価格ルールが適用されると、製品の価格ソースがデフォルトで`Price`に戻ります。

1. **[!UICONTROL Minimum Advertised Price (MAP)**]の場合は、オプションを選択します。

   デフォルトは選択なしです。 この設定は、製品に対して最小アドバタイズ価格(MAP)を有効にします。 価格属性を定義し、製品の上場価格が（価格設定のソースとルールに基づいて）決定された最小価格を下回る場合、この値がリストのMAPになります。 この設定を使用すると、[価格ルール](./pricing-products.md)を実装しながら、製品の最小価格を引き続き制御できます。 上場価格が低くなりすぎないようにするには、MAPとして使用する価格属性を選択します。 ただし、選択した価格フィールドが製品に対して定義されていない場合、MAPは使用されません。

1. **[!UICONTROL Strike Through Price (MSRP)]**&#x200B;の場合は、オプションを選択します。

   デフォルトは選択なしです。 この設定により、製造元の製品の推奨小売価格(MSRP)として使用される価格属性が決定されます。 上場価格が定義されたMSRPより小さい場合、Amazonのリストには、MSRP価格のストライクスルーと共に、計算された「保存済み」金額と割合が表示されます。 ただし、選択した価格フィールドが製品に対して定義されていない場合、MSRPは計算されません。

   >[!NOTE]
   >
   >この設定は、[Buy Box](./buy-box-competitor-pricing.md)の位置を獲得したリストにのみ適用されます。 Buy Boxは、通常は最高の価格でリストされる製品を持つ販売者にAmazonが与え、FBA/Prime出荷の提供、可用性、販売者のパフォーマンスなどの他の要因と共に与えられます。

1. **付加価値税(VAT)**&#x200B;の適用には、次のオプションを選択します。

   - `Disabled` - （デフォルト）VATを上場価格に適用しない場合に選択します。

   - `Enabled`  — 上場価格にVATを適用するタイミングを選択します。VATは、通常、ヨーロッパの国々で消費税として使用され、Amazon内の最終上場価格に追加されます。 VATは、[下限価格](./floor-price.md)がヒットしない限り、インテリジェント価格ルール内で使用されるリストの最終価格には適用されません。
   >[!NOTE]
   >
   >欧州連合(EU)の企業は、顧客が税金を支払えるように、ビジネスバイヤーに請求書を送信する必要があります。 これらの請求書を生成して税金を自分で計算するか、AmazonのVAT計算サービスなどの税金計算サービスを使用できます。 Amazonは、[Amazon VAT計算サービス](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}に新規登録することをお勧めします。 別の方法を選択する場合は、VATコンプライアンスに対する責任を負います。>
   >
   >AmazonがVAT計算サービスのアカウントを確認して有効化するまでに10 ～ 14日かかる場合があります。

1. **[!UICONTROL VAT Percentage]**&#x200B;には、VAT率の値を入力します。

   デフォルトは`0.00`です。 この値は、上場価格に追加するVAT金額の計算に使用されます。 `10.2`を入力すると、10.20%のVATが上場価格に適用されます。 「付加価値税(VAT)を適用」フィールドが`Disabled`に設定されている場合、このフィールドは無効になります。

1. **（英国の店舗のみ）** の場合、 **[!UICONTROL Amazon Product Tax Code (PTC)]**&#x200B;次のオプションを選択します。

   - `Do Not Manage PTC` - （デフォルト）サードパーティの税金計算サービスを使用している場合、またはすべての税金計算をアカウントで設定済みの場合に選択 [!DNL Amazon Seller Central] します。選択すると、Amazonの販売チャネルは製品税コード情報を[!DNL Amazon Seller Central]アカウントに送信しません。

   - `Set Default PTC`  — すべての製品で使用するユニバーサル製品税コード(PTC)がある場合に選択します。選択した場合は、_[!UICONTROL Default PTC]_を完了する必要があります。

      - **[!UICONTROL Default PTC]**&#x200B;の場合は、対象となるすべてのAmazon・リストに使用するデフォルトのPTCを入力します。 デフォルトのPTCが[!DNL Amazon Seller Central]アカウントに設定されている場合は、このフィールドを空白のままにします。 このフィールドに対して行った変更は、既存のAmazonのリストには影響しません。 既存のリストのデフォルトPTCを変更するには、リストを[終了](./end-listings-manually.md)し、新しいリストを作成する必要があります。
   >[!NOTE]
   >
   >AmazonのVAT計算サービスを使用する場合は、製品の税金カテゴリを把握する必要があります。 PTCは、AmazonでのB2B購入の税カテゴリIDコードです。 [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}を参照してください。

1. **[!UICONTROL Currency Conversion]**&#x200B;の場合は、オプションを選択します。

   デフォルトは`Disabled`です。 これらのオプションは、[!DNL Commerce] [currency](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}の設定によって異なります。 使用できるオプションがない場合は、通貨設定を行います。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![上場価格](assets/amazon-listing-price.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Magento Price Source] | Amazonリストを作成する際に使用する価格ソースを決定します。 デフォルトは`Price`です。 `Amazon Price`や`Special Price`など、別の属性を選択した場合は、その属性に対して定義された値がAmazonのリストに使用されます。 ただし、選択した属性が定義されていない場合は、`Price`が使用されます。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | MAP価格の[!DNL Commerce]属性。 「MAP」オプションを選択すると、AmazonリストがMAP価格より小さい場合は、MAP価格に自動的に設定されます。 |
| [!UICONTROL Strike Through Price (MSRP)] | MSRP価格を表す[!DNL Commerce]属性。 Amazonの上場価格がMSRPより小さい場合は、MSRP価格と上場価格のストライクスルーが表示されます。 この設定は、「保存」の金額と割合の計算にも使用されますが、この機能は[Buy Box](./buy-box-competitor-pricing.md)の位置を獲得したリストにのみ適用されます。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | VATは欧州連合の販売者によって使用されます。<br><br>上場 `Disabled` 価格にVATを追加しない場合は、を選択します。<br><br>「 」を `Enabled` 選択し、VATを上場価格に適用するためのVATパーセンテージを入力します。 |
| [!UICONTROL VAT Percentage] | Amazonの一覧表示価格に追加するVAT金額の計算に使用する割合を定義します。 <br><br>を入力する `5`と、すべての価格ルールが適用された後、最終上場価格に5%のVATが適用されます。VAT税は、[floor](./floor-price.md)または[ceiling](./optional-ceiling-price.md)がヒットしない限り、インテリジェント価格ルール内で使用されるリストの最終価格には適用されません。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (UK Stores Only) Amazonの販売チャネルから[!DNL Amazon Seller Central]アカウントに製品税コード情報を送信するかどうかを指定します。 <br><br>サード **パーティの税金計算サ** ービスを使用している場合、またはすべての税金計算を既にアカウントで設定している場合は、「PTCを管理しない」を選択 [!DNL Amazon Seller Central] します。このオプションを設定すると、Amazonの販売チャネルは製品税コード情報を[!DNL Amazon Seller Central]アカウントに送信しません。<br><br>すべての **製品に** 使用するユニバーサル製品税コードがある場合は、「デフォルトPTCを設定」を選択します。<br><br> [Amazonの製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}を参照してください。 |
| [!UICONTROL Default PTC] | **Amazon Product Tax Code (PTC)**&#x200B;が`Set Default PTC`に設定されている場合にのみ表示されます。 有効なすべてのAmazon・リストに使用するデフォルトのPTCを入力します。 デフォルトのPTCが[!DNL Amazon Seller Central]アカウントに設定されている場合は、このフィールドを空白のままにします。 <br><br>このフィールドに加えた変更は、既存のリストには影響しません。リストは[終了](./end-listings-manually.md)し、変更を有効にするために新しいリストを作成する必要があります。 |
| [!UICONTROL Currency Conversion] | [!DNL Commerce]ストアフロントのデフォルト通貨を、デフォルトのAmazon通貨に正確に変換して、リスト価格を適切な通貨で公開できるようにします。 通貨換算は、常に[!DNL Commerce]デフォルトの通貨に基づいておこなわれます。<br><br>他の通貨が使用可能な場合でも、デ [!DNL Commerce] フォルトの通貨とAmazonの通貨を表示できます。デフォルトの[!DNL Commerce]通貨がAmazonのデフォルトの通貨と一致する場合、「通貨換算」は無効のままにします。<br><br>例えば、デフォルト通貨がCAD(カナダ [!DNL Commerce] ドル)で、Amazonのデフォルト通貨がUSDの場合、「通貨換算」を有効にして、「換算レートCADからUSD」を選択する必要があります。表示されるオプションは、組み込みの[!DNL Commerce]通貨換算に基づいています。 目的のオプションが表示されない場合は、[ [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}で通貨を設定します。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
