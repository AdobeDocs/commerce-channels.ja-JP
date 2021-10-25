---
title: リスト価格
description: リスト価格の設定を使用して、Amazon リストの価格設定と基本 (デフォルト) 価格値を指定します。
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1509'
ht-degree: 0%

---

# リスト価格

[!UICONTROL Listing Price] 設定は、ストア一覧の設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

これらの設定で [!DNL Commerce] は、Amazon リストの基礎 (デフォルト) 価格値である価格のソースとして使用する価格設定の属性を定義します。 これらの設定は、の価格設定によって、 [ ](./pricing-rule-general-settings.md) の設定値を基準とした Amazon リスト価格が自動的に調整され _[!UICONTROL Magento Price Source]_ます。

価格設定は、 [ ](./price-scope.md) グローバルまたは web サイトに設定することができます。 価格設定がに設定されている場合は `Global` 、すべての店舗または web サイトに対して価格ソースが1つあります。 価格設定がに設定されている場合 `Website` 、価格ソースは、web サイト価格のフォールバックロジック (利用可能な場合) を使用し、その後にデフォルトの (グローバル) 価格が使用されます。

リストルールが複数の web サイトに適用されるように設定されている場合、web サイト価格が使用される順序は、リスティングルールで定義されている web サイトの優先順位設定によって決まり [ ](./listing-rules.md) ます。 これらのルールを使用して、カタログ全体の製品価格を定義することができます。 Web サイトの価格スコープを使用しているかどうかを確認するには、「カタログ価格のスコープ」を参照してください ( [ ](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html) {target = &quot;_blank&quot;})。

に一覧表示されているオプションは、に設定されている _[!UICONTROL Magento Price Source]__[!UICONTROL Minimum Advertised Price (Map)]_ _[!UICONTROL Strike Through Price (MSRP)]_価格属性を含みます。 価格属性は [!DNL Commerce] 、「Store Owner」の値が「」に設定されたカタログ入力タイプの製品属性です `Price` 。 「属性入力の種類」を参照してください [ ](https://docs.magento.com/user-guide/stores/attributes-input-types.html) 。 {target = &quot;_blank&quot;} のようになります。

## リスト価格設定の設定 {#configure-listing-price-settings}

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL Listing Price]_ます。

1. **[!UICONTROL Magento Price Source]**(必須) には、いずれかのオプションを選択します。

   初期設定では、と `Price` なります。 この設定によって、Amazon リストに使用される価格ソースが決まります。 [価格設定ルールを作成すると、 ](./pricing-products.md) ここで選択した属性に定義されている値にルールが適用されます。設定可能な価格属性を選択できます。 ただし、選択された属性が製品に入力されていない場合は、表示される `Price` Amazon のリスト価格を決定するために価格ルールが適用されたときに、製品の価格ソースが初期設定に戻ります。

1. * * の場合は [!UICONTROL Minimum Advertised Price (MAP)**] 、オプションを選択します。

   初期設定では選択されていません。 この設定によって、製品の最小限の広告価格 (マップ) が有効になります。 価格属性を定義したときに、製品の出展価格が、価格設定ソースとルールに基づいて特定の最低価格よりも下回ると、この値がリストのマップになります。 この設定を行うと [ ](./pricing-products.md) 、製品の最低価格を管理しながら、価格設定ルールを実装することができます。 出展価格が低すぎないようにするには、マップとして使用する価格設定属性を選択します。 ただし、選択されている価格フィールドが製品に定義されていない場合は、マップは使用されません。

1. **[!UICONTROL Strike Through Price (MSRP)]**&#x200B;では、オプションを選択します。

   初期設定では選択されていません。 この設定によって、メーカーによって製品に提示される小売り価格 (MSRP) として使用される価格属性が決まります。 登録価格が定義された MSRP よりも小さい場合は、Amazon の一覧が、「保存した」という計算結果と共に、MSRP 価格が付いた打ち消し線で表示されます。 ただし、選択されている価格フィールドが製品に定義されていない場合、MSRP は計算されません。

   >[!NOTE]
   >
   >この設定は、「購入」ボックスの位置が勝ったリストにのみ適用さ [ ](./buy-box-competitor-pricing.md) れます。 この「購入」ボックスには、Amazon によって、その製品が最も最適な価格で通常最適な価格で販売されています。さらに、FBA、素数、その他の要因 (FBA、素数、販売店のパフォーマンスなど) も利用できます。

1. 付加 **価値税 (VAT) を適用するには** 、次のいずれかのオプションを選択します。

   - `Disabled` -(デフォルト) VAT を登録価格に適用しない場合は、次のいずれかのオプションを選択します。

   - `Enabled` -出展価格に VAT を適用する場合に選択します。 一般に、欧州諸国では VAT が売上税として使用され、Amazon 内の最終的な定価に加算されます。 VAT は、フロア価格がわからない場合を除き、知的価格設定で使用されるリストに対しては最終的な価格には適用されません [ ](./floor-price.md) 。
   >[!NOTE]
   >
   >欧州連合 (EU) の企業は、請求書を企業購入者に送信する必要があります。これにより、顧客は税金を送金することができます。 請求書を生成して税金を独自に計算することも、Amazon の VAT 計算サービスのような tax 計算サービスを使用することもできます。 Amazon [ VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;) {target = &quot;_blank&quot;} にサインアップすることが推奨されます。 別の方法を選択した場合は、VAT コンプライアンスが担当されます。 >
   >
   >Amazon が VAT 計算サービスアカウントを確認し、アクティブ化するのに10-14 時間がかかる場合があります。

1. **[!UICONTROL VAT Percentage]**「」に、VAT レートの値を入力します。

   初期設定では、と `0.00` なります。 この値は、定価に追加する VAT 金額を計算するために使用されます。 `10.2`が入力されると、10.20% VAT がリスト価格に適用されます。このフィールドは、付加価値税 (VAT) フィールドがに設定されている場合は使用できませ `Disabled` ん。

1. **(英国ストアのみ)****[!UICONTROL Amazon Product Tax Code (PTC)]**&#x200B;で、次のいずれかのオプションを選択します。

   - `Do Not Manage PTC` -(デフォルト) サードパーティーの税計算サービスを使用している場合、または、既に口座に税金計算が設定されている場合に選択し [!DNL Amazon Seller Central] ます。 選択すると、Amazon sales チャンネルによって製品の税コード情報が口座に送信されません [!DNL Amazon Seller Central] 。

   - `Set Default PTC` -すべての製品に使用するユニバーサル製品税コード (PTC) があるかどうかを選択します。 この設定を選択した場合は、完了する必要があり _[!UICONTROL Default PTC]_ます。

      - **[!UICONTROL Default PTC]**「」には、すべての適格な Amazon リストに使用されるデフォルトの PTC を入力します。デフォルトの PTC がアカウントに設定されている場合は [!DNL Amazon Seller Central] 、このフィールドを空白のままにします。 このフィールドに変更を加えても、既存の Amazon リストには影響しません。 既存の一覧のデフォルトの PTC を変更するには、リストを [ 終了して、新しいカタログを作成する必要があり ](./end-listings-manually.md) ます。
   >[!NOTE]
   >
   >Amazon の VAT 計算サービスを使用する場合は、製品の税カテゴリについて理解しておく必要があります。 PTC は、EU の B2B 購入用の Amazon の税務分別税コードを示しています。 [Amazon の製品税コードについては ](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US) 、{target = &quot;_blank&quot;} を参照してください。

1. **[!UICONTROL Currency Conversion]**&#x200B;では、オプションを選択します。

   初期設定では、と `Disabled` なります。 このオプションは、お客様の通貨の種類によって異なり [!DNL Commerce] [ ](https://docs.magento.com/user-guide/configuration/general/currency-setup.html) ます。 {target = &quot;_blank&quot;} 設定によって異なります。 オプションが使用できない場合は、通貨設定を設定します。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![リスト価格](assets/amazon-listing-price.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Magento Price Source] | Amazon リストを作成するときに使用する価格設定を指定します。 初期設定では、と `Price` なります。 またはなどの別の属性を選択した場合は `Amazon Price` `Special Price` 、属性に定義されている値が Amazon リストに使用されます。 ただし、「selected」属性が定義されていない場合 `Price` は、が使用されます。 |
| [!UICONTROL Minimum Advertised Price (MAP)] | [!DNL Commerce]マップ価格の属性です。「MAP」オプションを選択すると、リストプライスがマップ価格より少ない場合に、Amazon の一覧が自動的にマップ価格に設定されます。 |
| [!UICONTROL Strike Through Price (MSRP)] | [!DNL Commerce]MSRP 価格を表す属性です。Amazon のリスト価格が MSRP より少ない場合は、MSRP 価格と出展価格の取り消し線が表示されます。 この設定を使用して「保存」の金額と比率を計算することもできますが、この機能は、「購入」ボックスの位置にあるリストにのみ適用され [ ](./buy-box-competitor-pricing.md) ます。 |
| [!UICONTROL Apply Value Added Tax (VAT)] | VAT は欧州連合の売り手によって使用されます。<br><br>`Disabled`VAT をリスト価格に追加する必要がない場合に選択します。<br><br>`Enabled`リスト価格に vat を適用する場合は、次のいずれかを選択し、vat の割合を入力します。 |
| [!UICONTROL VAT Percentage] | Amazon リストの表示価格に追加される VAT の金額を計算するために使用される割合を指定します。 <br><br>「」と入力すると、 `5` すべての価格設定ルールが適用された後の最終的な一覧価格に5% の VAT が適用されます。 VAT 税は、 [ フロア ](./floor-price.md) または [ 天井に達していない限り、インテリジェントな価格ルールで使用される一覧の最終価格には適用されません ](./optional-ceiling-price.md) 。 |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (UK ストアについてのみ表示されます)Amazon sales チャンネルが製品税コード情報を取引先企業に送信するかどうかを指定し [!DNL Amazon Seller Central] ます。 <br><br>**** サードパーティの税計算サービスを使用している場合、または口座ですべての税計算が設定されている場合は、「PTC を管理しない」を選択し [!DNL Amazon Seller Central] ます。このオプションを設定した場合、Amazon sales チャンネルには製品税コード情報が口座に送信されません [!DNL Amazon Seller Central] 。<br><br>**** すべての製品に使用する汎用製品税コードがある場合は、「デフォルトの PTC に設定」を選択します。<br><br>[Amazon の製品税コードについては ](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US) 、{target = &quot;_blank&quot;} を参照してください。 |
| [!UICONTROL Default PTC] | このメッセージは **、Amazon の製品税コード (PTC) がに設定されている場合にのみ表示され** `Set Default PTC` ます。 すべての適格な Amazon リストに使用されるデフォルトの PTC を入力します。 デフォルトの PTC がアカウントに設定されている場合は [!DNL Amazon Seller Central] 、このフィールドを空白のままにします。 <br><br>このフィールドに変更を加えても、既存のリストには影響しません。 変更を有効にするには、このリストを [ 終了 ](./end-listings-manually.md) して新しいリストを作成する必要があります。 |
| [!UICONTROL Currency Conversion] | 現在の会社のデフォルト通貨を、適切な Amazon currency に変更して [!DNL Commerce] 、適切な通貨でパブリッシュすることができます。 為替換算は、常にデフォルトの通貨に基づいてい [!DNL Commerce] ます。<br><br>[!DNL Commerce]他の通貨が使用可能になったときにも、デフォルトと Amazon の通貨を表示することができます。デフォルトの通貨が、デフォルトの Amazon の通貨と一致している場合は [!DNL Commerce] 、為替換算が無効化されたままになります。<br><br>例えば、 [!DNL Commerce] デフォルトの通貨が CAD (カナダ) の場合は、通貨換算を有効にして、その為替レートの cad を usd に選択する必要があります。 表示されるオプションは、組み込まれている為替換算に基づいてい [!DNL Commerce] ます。 目的のオプションが表示されない場合は、 [  [!DNL Commerce] ](https://docs.magento.com/user-guide/stores/currency-configuration.html) {target = &quot;_blank&quot;} に通貨を設定します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
