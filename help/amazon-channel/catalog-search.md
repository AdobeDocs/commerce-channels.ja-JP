---
title: カタログ検索
description: 適格なコマースカタログ製品をAmazonリストにマッピングするのに役立つ属性マッチングを設定するには、「カタログ検索」設定を更新します。
redirect_from: /sales-channels/asc/ob-catalog-search.html
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%

---

# カタログ検索

_カタログ_ 検索設定は、ストアリスト設定の一部です。リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定を使用すると、対象となる[!DNL Commerce]製品をAmazonのリストにマッピングするのに役立つ属性の照合を設定できます。 マッピングされると、Amazonは、価格、数量、上書き、注文と製品の同期に関連するアクションを有効化します。

これらのマッピング値を定義すると、完全一致の可能性が高まり、製品リストを手動で照合する必要が最小限に抑えられます。 [事前設定タスク](./amazon-pre-setup-tasks.md)に属性を追加すると、Amazonの販売チャネルは、オンボーディング中に製品を自動的に照合し、Amazonと[!DNL Commerce]の間で製品データを同期する可能性が高くなります。

Amazon ASIN属性のみを作成する場合（製品ごとにASIN値を追加しない場合）、[!DNL Commerce]製品はAmazonのリストと自動的に一致しない可能性があります。 製品を[手動で割り当てることができます。](./creating-assigning-catalog-products.md) ただし、手動での一致では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>製品を手動で照合し、製品のASIN、UPC、またはその他のデータ要素を更新する場合は、2か所でデータを更新する必要があります。 [!DNL Commerce]カタログと[!DNL Amazon Seller Central]アカウントのAmazonリストで更新します。

これらの属性と値をマッピングする（可能な場合）ことをお勧めします。 このマッピングを完了する必要はありませんが、製品のマッチングに役立ち、Amazonと[!DNL Commerce]の間で適切なカタログを同期するために必要です。

属性を追加する場合は、[Amazonのマッチング用の製品属性の作成](./ob-creating-magento-attributes.md)を参照してください。

## [!UICONTROL Catalog Search]設定を構成します

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL Catalog Search]_セクションを展開します。

1. **[!UICONTROL ASIN]**&#x200B;の場合、Amazon ASIN値用に作成した製品属性を選択します。

   ASIN([!DNL Amazon Standard Identification Number])は、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。

1. **[!UICONTROL EAN]**&#x200B;の場合、Amazon EAN値用に作成した製品属性を選択します。

   欧文記事番号(EAN)は、バーコード標準で、12桁または13桁の製品識別コードです。 各EANは、製品、製造元およびその属性を一意に識別します。通常、EANは、製品ラベルまたはパッケージにバーコードとして印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるためにEANコードが必要です。 EANは製造元から入手できます。

1. **[!UICONTROL GCID]**&#x200B;の場合、Amazon GCIN値用に作成した製品属性を選択します。

   グローバルカタログ識別子(GCID)は、UPCコードまたはISBNを持たない製品のIDです。 Amazon Brand Registryを使用すると、ブランド所有者として登録し、製品の一意のIDを作成できます。

1. **[!UICONTROL ISBN]**&#x200B;の場合、Amazon ISBN値用に作成した製品属性を選択します。

   International Standard Book Number(ISBN)は、一意の商用書籍識別子バーコードです。 各ISBNコードは、本を一意に識別します。 ISBNは10桁か13桁です。 2007年1月1日以降に割り当てられたISBNはすべて13桁です。

1. **[!UICONTROL UPC]**&#x200B;の場合、Amazon UPC値用に作成した製品属性を選択します。

   ユニバーサル製品コード(UPC)は、米国で小売パッケージに広く使用される12桁のバーコードです。

1. **[!UICONTROL General Search]**&#x200B;の場合、一般検索の一致に使用する製品属性を選択します。

   この属性は、[!DNL Commerce]製品を適切なAmazonリストに一致させるために選択できる属性です。 一般検索では、カタログのキーワード検索が使用されます。 したがって、製品のSKUや製品名など、関連するキーワードを含む[!DNL Commerce]属性を使用することをお勧めします。 一般検索では、考えられる多くの一致が返される場合があり、その場合は、考えられる一致の中から適切なAmazonリストを選択できます。 このフィールドの一般的な選択は`Product Name`です。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![カタログ検索](assets/amazon-catalog-search.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL EAN (European Article Number)] | 12桁または13桁の製品識別コード。 欧文記事番号(EAN)は、バーコード標準で、12桁または13桁の製品識別コードです。 各EANは、製品、製造元およびその属性を一意に識別します。通常、EANは、製品ラベルまたはパッケージにバーコードとして印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるためにEANコードが必要です。 EANは製造元から入手できます。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | グローバルカタログ識別子(GCID)は、UPCコードまたはISBNを持たない製品のIDです。 AmazonのBrand Registryを使用すると、ブランド所有者として登録し、UPCまたはISBNを持たない可能性のある製品の一意のIDを作成できます。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10桁または13桁の一意の商業帳簿識別子バーコード。 International Standard Book Number(ISBN)は、一意の商用書籍識別子バーコードです。 各ISBNコードは、本を一意に識別します。 ISBNは10桁か13桁です。 2007年1月1日以降に割り当てられたISBNはすべて13桁です。 |
| UPC（ユニバーサル製品コード） | 12桁のバーコード。 ユニバーサル製品コード(UPC)は、米国で小売パッケージに広く使用される12桁のバーコードです。 |
| [!UICONTROL General Search] | 属性を選択します。 この属性は、[!DNL Commerce]製品を適切なAmazonリストに一致させるために選択できる属性です。 一般検索では、カタログのキーワード検索が使用されます。 したがって、製品のSKUや製品名など、関連するキーワードを含む[!DNL Commerce]属性を使用することをお勧めします。 一般検索では、考えられる多くの一致が返される場合があり、その場合は、考えられる一致の中から適切なAmazonリストを選択できます。 このフィールドの一般的な選択は`Product Name`です。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
