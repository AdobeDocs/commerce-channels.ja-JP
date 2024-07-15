---
title: Amazon リストのカタログ検索
description: 対象となるCommerce カタログ商品をAmazonのリストにマッピングするのに役立つ属性のマッチングを設定するには、カタログ検索設定を更新します。
feature: Sales Channels, Search, Catalog Management, Products, Configuration
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# Amazon リストのカタログ検索

_カタログ検索_ 設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定を使用すると、対象となる [!DNL Commerce] 製品をAmazon リストにマッピングするのに役立つ属性のマッチングを設定できます。 マッピングされると、Amazonでは価格設定、数量、オーバーライド、注文と商品の同期に関連するアクションがアクティブになります。

これらのマッピング値を定義すると、完全一致の可能性が高まり、製品リストを手動で一致させる必要性を最小限に抑えることができます。 [ 事前設定タスク ](./amazon-pre-setup-tasks.md) の一部として属性を追加すると、Amazon セールスチャネルは、オンボーディング中に商品を自動的に照合し、Amazonと [!DNL Commerce] の間で商品データを同期する可能性が高くなります。

Amazonの ASIN 属性のみを作成する（商品ごとの ASIN 値を追加しない）場合、[!DNL Commerce] の商品がAmazonのリストと自動的に一致しない可能性があります。 製品は [ 手動で割り当て ](./creating-assigning-catalog-products.md) ることができます。 ただし、手動での照合では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>製品を手動で一致させ、製品の ASIN、UPC、またはその他のデータ要素を更新する場合、データを 2 か所で更新する必要があります。 [!DNL Commerce] カタログと、[!DNL Amazon Seller Central] アカウントのAmazon リストで更新します。

これらの属性と値をマッピングするのがベストプラクティスです（使用可能な場合）。 このマッピングを完了する必要はありませんが、商品のマッチングに役立ち、Amazonと [!DNL Commerce] の間で適切にカタログを同期する必要があります。

属性を追加する場合は、[Amazon マッチングの製品属性の作成 ](./ob-creating-magento-attributes.md) を参照してください。

## [!UICONTROL Catalog Search] の設定

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL Catalog Search]_」セクションを展開します。

1. **[!UICONTROL ASIN]**:Amazonの ASIN 値に対して作成した製品属性を選択します。

   ASIN （[!DNL Amazon Standard Identification Number]）は、項目を識別する 10 個の文字や数字で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。

1. **[!UICONTROL EAN]**:Amazon EAN 値として作成した product 属性を選択します。

   欧州商品番号（EAN）は、バーコード規格で、12 桁または 13 桁の製品識別コードです。 各 EAN は、製品、製造元およびその属性を一意に識別します。通常、EAN はバーコードとして製品ラベルまたはパッケージに印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるために EAN コードが必要です。 EAN は製造元から入手できます。

1. **[!UICONTROL GCID]**:Amazon GCIN 値に対して作成した product 属性を選択します。

   グローバルカタログ識別子（GCID）は、UPC コードや ISBN を持たない製品の ID です。 Amazonのブランドレジストリを使用すると、ブランドオーナーとして登録し、商品の一意の ID を作成できます。

1. **[!UICONTROL ISBN]**:Amazonの ISBN 値に対して作成した product 属性を選択します。

   国際標準書籍番号（ISBN）は、独自の商業書籍識別子バーコードです。 各 ISBN コードは、ブックを一意に識別します。 ISBN は 10 桁または 13 桁の数字を持ちます。 2007 年 1 月 1 日以降に割り当てられたすべての ISBN は 13 桁です。

1. **[!UICONTROL UPC]** しくは、Amazonの UPC 値に対して作成した製品属性を選択します。

   Universal Product Code （UPC）は、米国で小売用のパッケージに広く使用されている 12 桁のバーコードです。

1. **[!UICONTROL General Search]**：一般的な検索一致に使用する製品属性を選択します。

   この属性は、製品を適切なAmazon リストに一致 [!DNL Commerce] せるために選択できます。 一般検索では、カタログからのキーワード検索を使用します。 そのため、製品 SKU や製品名など、関連するキーワードを持つ [!DNL Commerce] 属性を使用することをお勧めします。 一般検索では、多くの一致候補が返される場合があります。このような場合は、一致候補から適切なAmazonのリストを選択できます。 このフィールドの一般的な選択肢は `Product Name` です。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ カタログ検索 ](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は [!DNL Amazon Standard Identification Number] を表す。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL EAN (European Article Number)] | 12 桁または 13 桁の製品識別コード。 欧州商品番号（EAN）は、バーコード規格で、12 桁または 13 桁の製品識別コードです。 各 EAN は、製品、製造元およびその属性を一意に識別します。通常、EAN はバーコードとして製品ラベルまたはパッケージに印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるために EAN コードが必要です。 EAN は製造元から入手できます。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | グローバルカタログ識別子（GCID）は、UPC コードや ISBN を持たない製品の ID です。 Amazonのブランドレジストリを使用すると、ブランドオーナーとして登録し、UPC または ISBN を持たない商品の一意の ID を作成できます。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10 または 13 桁の一意の商業帳簿識別子バーコード。 国際標準書籍番号（ISBN）は、独自の商業書籍識別子バーコードです。 各 ISBN コードは、ブックを一意に識別します。 ISBN は 10 桁または 13 桁の数字を持ちます。 2007 年 1 月 1 日以降に割り当てられたすべての ISBN は 13 桁です。 |
| UPC （ユニバーサル製品コード） | 12 桁のバーコード。 Universal Product Code （UPC）は、米国で小売用のパッケージに広く使用されている 12 桁のバーコードです。 |
| [!UICONTROL General Search] | 属性を選択します。 この属性は、製品を適切なAmazon リストに一致 [!DNL Commerce] せるために選択できます。 一般検索では、カタログからのキーワード検索を使用します。 そのため、製品 SKU や製品名など、関連するキーワードを持つ [!DNL Commerce] 属性を使用することをお勧めします。 一般検索では、多くの一致候補が返される場合があります。このような場合は、一致候補から適切なAmazonのリストを選択できます。 このフィールドの一般的な選択肢は `Product Name` です。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
