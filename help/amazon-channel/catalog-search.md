---
title: カタログでのAmazonリストの検索
description: 適格なコマースカタログ製品をAmazonリストにマッピングするのに役立つ属性の照合を設定するには、カタログ検索設定を更新します。
feature: Sales Channels, Search, Catalog Management, Products, Configuration
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# カタログでのAmazonリストの検索

_カタログ検索_ 設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定を使用すると、対象をマッピングするのに役立つ属性のマッチングを設定できます [!DNL Commerce] Amazonリストに含まれる製品。 マッピングが完了すると、Amazonは、価格、数量、上書き、注文および製品の同期に関連するアクションを有効化します。

これらのマッピング値を定義すると、完全一致の可能性が高まり、製品リストを手動で照合する必要が最小限に抑えられます。 属性を [事前設定タスク](./amazon-pre-setup-tasks.md)Amazonセールスチャネルは、Amazonとの間で製品データのオンボーディングおよび同期をおこなう際に、製品を自動的に照合する可能性が高くなります [!DNL Commerce].

Amazon ASIN 属性のみを作成する場合（製品ごとに ASIN 値を追加しない場合）、 [!DNL Commerce] 製品は、Amazonのリストと自動的に一致しない場合があります。 以下が可能です。 [手動で割り当て](./creating-assigning-catalog-products.md) お使いの製品。 ただし、手動での照合では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>製品を手動で照合し、製品の ASIN、UPC、または他のデータ要素を更新する場合は、2 か所でデータを更新する必要があります。 を更新します。 [!DNL Commerce] カタログと、Amazonのリスト [!DNL Amazon Seller Central] アカウント。

これらの属性と値をマッピングする（使用可能な場合）ことをお勧めします。 このマッピングを完了する必要はありませんが、製品の照合に役立ち、Amazonとの間で適切なカタログ同期をおこなうために必要な場合に役立ちます。 [!DNL Commerce].

属性を追加する場合は、 [Amazon照合用の製品属性の作成](./ob-creating-magento-attributes.md).

## 設定 [!UICONTROL Catalog Search] 設定

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL Catalog Search]_」セクションに入力します。

1. の場合 **[!UICONTROL ASIN]**「 」で、Amazon ASIN 値用に作成した製品属性を選択します。

   ASIN ([!DNL Amazon Standard Identification Number]) は、項目を識別する 10 文字または数字の一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合は、アイテムがカタログにアップロードされると新しい ASIN が作成されます。 ASIN は、Amazonの製品の詳細ページに、その品目に関する詳細と共に表示されます。

1. の場合 **[!UICONTROL EAN]**&#x200B;で、 Amazon EAN 値用に作成した製品属性を選択します。

   欧州記事番号 (EAN) は、バーコード規格で、12 桁または 13 桁の製品 ID コードです。 各 EAN は、製品、製造元およびその属性を一意に識別します。通常、EAN は、バーコードとして製品ラベルまたはパッケージに印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるために EAN コードが必要です。 EAN は製造元から入手できます。

1. の場合 **[!UICONTROL GCID]**「 」で、 Amazon GCIN 値用に作成した製品属性を選択します。

   グローバルカタログ識別子 (GCID) は、UPC コードまたは ISBN を持たない製品の ID です。 Amazon Brand Registry を使用すると、ブランド所有者として登録し、製品の一意の ID を作成できます。

1. の場合 **[!UICONTROL ISBN]**「 」で、Amazon ISBN 値用に作成した製品属性を選択します。

   International Standard Book Number(ISBN) は、一意の商用書籍識別子バーコードです。 各 ISBN コードは、本を一意に識別します。 ISBN は 10 桁か 13 桁です。 2007 年 1 月 1 日以降に割り当てられた ISBN はすべて 13 桁です。

1. の場合 **[!UICONTROL UPC]**&#x200B;で、 Amazon UPC 値用に作成した製品属性を選択します。

   ユニバーサル製品コード (UPC) は、米国の小売パッケージに広く使用される 12 桁のバーコードです。

1. の場合 **[!UICONTROL General Search]**」で、一般検索の一致に使用する製品属性を選択します。

   この属性は、一致するように選択できる属性です [!DNL Commerce] 製品を適切なAmazonリストに追加する。 一般検索では、カタログからのキーワード検索を使用します。 そのため、 [!DNL Commerce] 製品 SKU や製品名など、関連するキーワードを含む属性。 一般検索では、考えられる多くの一致が返される場合があります。その場合は、考えられる一致の中から適切なAmazonリストを選択できます。 このフィールドの一般的な選択肢は次のとおりです。 `Product Name`.

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![カタログ検索](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL ASIN] | アイテムを識別する 10 文字または数字の一意のブロック。<br><br>ASIN は、 [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字の一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合は、アイテムがカタログにアップロードされると新しい ASIN が作成されます。 ASIN は、Amazonの製品の詳細ページに、その品目に関する詳細と共に表示されます。 |
| [!UICONTROL EAN (European Article Number)] | 12 桁または 13 桁の製品識別コード。 欧州記事番号 (EAN) は、バーコード規格で、12 桁または 13 桁の製品 ID コードです。 各 EAN は、製品、製造元およびその属性を一意に識別します。通常、EAN は、バーコードとして製品ラベルまたはパッケージに印刷されます。 Amazonでは、検索結果の品質とカタログの品質を向上させるために EAN コードが必要です。 EAN は製造元から入手できます。 |
| [!UICONTROL GCID (Global Catalog Identifier)] | グローバルカタログ識別子 (GCID) は、UPC コードまたは ISBN を持たない製品の ID です。 Amazonの Brand Registry を使用すると、ブランド所有者として登録し、UPC または ISBN を持たない可能性のある製品に対して一意の ID を作成できます。 |
| [!UICONTROL ISBN (International Standard Book Number)] | 10 桁または 13 桁の一意の商用書籍識別子バーコード。 International Standard Book Number(ISBN) は、一意の商用書籍識別子バーコードです。 各 ISBN コードは、本を一意に識別します。 ISBN は 10 桁か 13 桁です。 2007 年 1 月 1 日以降に割り当てられた ISBN はすべて 13 桁です。 |
| UPC （ユニバーサル製品コード） | 12 桁のバーコード。 ユニバーサル製品コード (UPC) は、米国の小売パッケージに広く使用される 12 桁のバーコードです。 |
| [!UICONTROL General Search] | 属性を選択します。 この属性は、一致するように選択できる属性です [!DNL Commerce] 製品を適切なAmazonリストに追加する。 一般検索では、カタログからのキーワード検索を使用します。 そのため、 [!DNL Commerce] 製品 SKU や製品名など、関連するキーワードを含む属性。 一般検索では、考えられる多くの一致が返される場合があります。その場合は、考えられる一致の中から適切なAmazonリストを選択できます。 このフィールドの一般的な選択肢は次のとおりです。 `Product Name`. |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
