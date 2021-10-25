---
title: カタログ検索
description: 検索対象の Commerce カタログ製品を Amazon リストにマップするために使用できる属性の一致を設定するには、カタログ検索の設定を更新します。
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# カタログ検索

_カタログ検索_ 設定は、ストアリストの設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

これらの設定を使用して、Amazon リストを含む適格な製品に適合するように属性の一致を設定することができ [!DNL Commerce] ます。 マップされた場合、Amazon は価格、数量、オーバーライド、および注文と製品の同期に関するアクションがアクティブになります。

このマッピング値を定義すると、完全に一致する可能性が高くなります。これにより、製品リストを手動で検索する必要がなくなります。 属性を事前設定タスクの一部として追加すると [ ](./amazon-pre-setup-tasks.md) 、amazon sales channel は、オンボードの間に製品を自動的に照合し、Amazon と. 間の製品データを同期する可能性が高くなり [!DNL Commerce] ます。

Amazon の「サインオフ」属性を作成するのは、製品ごとの値を追加するのではなく、製品 [!DNL Commerce] が amazon リストに自動的に一致しない場合があります。 製品は [ 手動で割り当てることができ ](./creating-assigning-catalog-products.md) ます。 ただし、手動で比較を行っても、製品データを共有および同期するために必要なデータエレメントは作成されません。

>[!IMPORTANT]
>
>製品に手動で一致した場合に、その製品のアーク、UPC、またはその他のデータ要素を更新するには、2つの場所でデータを更新する必要があります。 使用しているカタログと Amazon リストに含まれている情報をご利用 [!DNL Commerce] [!DNL Amazon Seller Central] ください。

このような属性と値は、必要に応じてマップすることをお勧めします。 このマッピングは必須ではありませんが、これは製品の照合に役立ちますが、Amazon と. との間で適切なカタログを同期するために必要です [!DNL Commerce] 。

属性を追加するには、「 [ Amazon 照合用の製品属性の作成」を参照してください ](./ob-creating-magento-attributes.md) 。

## 設定の構成 [!UICONTROL Catalog Search]

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL Catalog Search]_ます。

1. については **[!UICONTROL ASIN]** 、Amazon アークサイン値用に作成した製品属性を選択します。

   アーク ( [!DNL Amazon Standard Identification Number] ) は、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。

1. については **[!UICONTROL EAN]** 、AMAZON EAN 値用に作成した製品属性を選択します。

   欧州欧州の記事番号 (EAN) は、12桁または13桁の製品識別コードで、バーコード規格です。 各 EAN は、製品、メーカー、および属性を一意に識別します。通常、EAN は製品ラベルに印刷されるか、バーコードとしてパッケージ化されます。 Amazon を使用するには、検索結果の品質を向上させるための EAN コードとカタログの質が必要になります。 EANs は製造元から入手できます。

1. については **[!UICONTROL GCID]** 、AMAZON GCIN 値用に作成した製品属性を選択します。

   グローバルカタログ識別子 (GCID) は、UPC コードまたは ISBN を持たない製品の ID です。 Amazon のブランドレジストリを使用すると、ブランド名として登録し、製品の一意の ID を作成することができます。

1. については **[!UICONTROL ISBN]** 、AMAZON ISBN 値用に作成した製品属性を選択します。

   国際標準ブック番号 (ISBN) は、一意の商用ブック id バーコードです。 各 ISBN コードは、本のを一意に識別します。 ISBN には、10または13桁の数字が含まれています。 2007年1月1日以降、すべての ISBN に13桁が割り当てられています。

1. については **[!UICONTROL UPC]** 、AMAZON UPC 値用に作成した製品属性を選択します。

   Universal Product Code (UPC) は、米国での小売用パッケージに幅広く使用されている12桁のバーコードです。

1. には **[!UICONTROL General Search]** 、一般的な検索に使用する製品属性を選択します。

   この属性は [!DNL Commerce] 、製品を適切な Amazon リストに適合するように選択することができます。 一般的な検索では、カタログのキーワード検索が使用されます。 そのため、 [!DNL Commerce] 製品 SKU や製品名など、関連するキーワードを含む属性を使用することをお勧めします。 一般的な検索では、一致するアイテムの数が多くなる場合があります。このような場合は、一致するアイテムから適切な Amazon リストを選択することができます。 このフィールドには、一般的に「」が選択されてい `Product Name` ます。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![カタログ検索](assets/amazon-catalog-search.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>「アーク」は、 [!DNL Amazon Standard Identification Number] . アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL EAN (European Article Number)] | 12または13桁のプロダクト id コード。 欧州欧州の記事番号 (EAN) は、12桁または13桁の製品識別コードで、バーコード規格です。 各 EAN は、製品、メーカー、および属性を一意に識別します。通常、EAN は製品ラベルに印刷されるか、バーコードとしてパッケージ化されます。 Amazon を使用するには、検索結果の品質を向上させるための EAN コードとカタログの質が必要になります。 EANs は製造元から入手できます。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | グローバルカタログ識別子 (GCID) は、UPC コードまたは ISBN を持たない製品の ID です。 Amazon のブランドレジストリを使用すると、ブランドの所有者として登録し、UPC や ISBN がない製品用に一意の ID を作成することができます。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 1桁または13桁の一意の民間書籍コードバーコード。 国際標準ブック番号 (ISBN) は、一意の商用ブック id バーコードです。 各 ISBN コードは、本のを一意に識別します。 ISBN には、10または13桁の数字が含まれています。 2007年1月1日以降、すべての ISBN に13桁が割り当てられています。 |
| UPC (Universal Product Code) | 12桁のバーコード。 Universal Product Code (UPC) は、米国での小売用パッケージに幅広く使用されている12桁のバーコードです。 |
| [!UICONTROL General Search] | 属性を選択します。 この属性は [!DNL Commerce] 、製品を適切な Amazon リストに適合するように選択することができます。 一般的な検索では、カタログのキーワード検索が使用されます。 そのため、 [!DNL Commerce] 製品 SKU や製品名など、関連するキーワードを含む属性を使用することをお勧めします。 一般的な検索では、一致するアイテムの数が多くなる場合があります。このような場合は、一致するアイテムから適切な Amazon リストを選択することができます。 このフィールドには、一般的に「」が選択されてい `Product Name` ます。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
