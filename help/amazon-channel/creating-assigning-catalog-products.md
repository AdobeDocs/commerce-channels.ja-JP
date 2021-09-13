---
title: 製品の作成と割り当て
description: AmazonSales Channelには、一致するコマースカタログ製品を作成し、Amazonリストに割り当てるのに役立つ「[!UICONTROL New Third Party]」タブが用意されています。
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# 製品の作成と割り当て

「_[!UICONTROL New Third Party]_」タブを表示する場合、[!DNL Commerce]カタログ製品を既存のAmazonリストと照合できます。 この一致には、2つのオプションがあります。 既存のカタログ商品にリストを割り当てたり、リストの情報を使用してカタログ商品を作成したりできます。 これらのオプションは、Amazonのリストが[!DNL Commerce]カタログと自動的に一致しない場合に役立ちます。

Amazon Sales Channelの完全な機能セットを使用するには、製品をAmazonのリストに照合（または割り当て）する必要があります。

Amazonリストからカタログ商品を作成する場合：

- **ASIN**&#x200B;が[!DNL Commerce] SKUになります
- **製品リスト名**&#x200B;は、カタログリスト名になります。
- **Price**&#x200B;と&#x200B;**Quantity**&#x200B;がAmazon Listingからインポートされます

残りの必要な設定は、作成時に選択した[!DNL Commerce]製品設定によって決まります。

リストが作成され、一致すると、_[!UICONTROL New Third Party]_タブから削除され、_[!UICONTROL Active]_&#x200B;タブに表示されます。

## 1つのカタログ製品のAmazonリストへの割り当て

1. [_[!UICONTROL New Third Party]_](./new-third-party-listings.md)タブで製品リストを表示します。

1. 割り当てるリストをリストで探し、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックして、**[!UICONTROL Assign Catalog Product]**をクリックします。

   この操作により、_[!UICONTROL Assign Magento Catalog Product]_ページが開きます。

1. [ワークスペースコントロール](./workspace-controls.md)を使用してリストを参照またはフィルターし、リストに一致する適切なカタログ製品を見つけます。

1. リストに正しい製品が表示されたら、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Assign Catalog Product]**をクリックします。

これで、製品とリストが一致します。 Amazonの販売チャネルは、Amazonと製品とリストデータを共有し、リストとその情報（リスト価格、出荷価格、在庫/数量、注文情報、ステータスなど）を管理できるようになりました。

## Amazonリスト情報を使用した単一カタログ製品の作成

1. [_[!UICONTROL New Third Party]_](./new-third-party-listings.md)タブで製品リストを表示します。

1. [!DNL Commerce]カタログで作成するリストを見つけ、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックして、**[!UICONTROL Create New Catalog Product]**をクリックします。

   この操作により、_[!UICONTROL Create Magento Catalog Product]_ページが開きます。

1. 製品のカタログ設定を入力します。

   - **[!UICONTROL Enable Product(s)]**&#x200B;トグルを`Yes`または`No`（必須）に設定します。

      |はい|[!DNL Commerce]ストアフロントの販売に適した製品を選択します。|
|いいえ|[!DNL Commerce]ストアフロントの販売に対して、製品を不適格にする場合に選択します。|

   - **[!UICONTROL Categories]**&#x200B;の場合、製品のカテゴリを割り当てます（オプション）。

      製品のカテゴリを選択するには、下向き矢印をクリックし、カテゴリのチェックボックスを選択します。 終了したら&#x200B;**[!UICONTROL Done]**&#x200B;をクリックします。

   - **[!UICONTROL Website Ids]**&#x200B;の場合、製品を関連付けるWebサイト（ストアフロント）を選択します。

      このリストのオプションは、[!DNL Commerce] [ストア設定](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}の設定によって異なります。

   - **[!UICONTROL Attribute Set Id]**（必須）には、オプションを選択します。

      `Default` はデフォルトの選択です。このリストのオプションは、設定した[!DNL Commerce] [属性セット](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}によって異なります。

   - **[!UICONTROL Visibility]**&#x200B;の場合は、新製品のオプションを選択します。

      |**[!UICONTROL Not Visible Individually]**（デフォルト）|ストアフロントのリストには製品が含まれていませんが、他の製品のバリエーションとして使用できます。|
|**[!UICONTROL Catalog]**|商品がカタログリストに表示されます。|
|**[!UICONTROL Search]**|製品は検索操作に使用できます。|
|**[!UICONTROL Catalog and Search]**|商品はカタログリストに含まれ、検索操作に使用できます。|

   - **[!UICONTROL Assign Tax Class]**&#x200B;の場合、製品のオプションを選択します。

      このリストに表示されるオプションは、設定した[tax classes](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}によって異なります。

   - 完了したら、「**[!UICONTROL Create Catalog Products]**」をクリックします。

カタログ商品が[!DNL Commerce]カタログに作成され、作成元のAmazonリストに割り当てられます。 既存のAmazonのリストと一致するようになったリストでは、リストは「_[!UICONTROL New Third Party]_」タブから削除され、「_[!UICONTROL Active]_」タブに表示されます。

## Amazonリスト情報を使用した複数のカタログ製品の作成

1. [_[!UICONTROL New Third Party]_](./new-third-party-listings.md)タブで製品リストを表示します。

1. カタログ商品を作成する一覧を選択します。

   左側の列の個々のチェックボックスを選択するか、左上の列の下向き矢印をクリックして&#x200B;**[!UICONTROL Select All]**&#x200B;または&#x200B;**[!UICONTROL Select All on this Page]**&#x200B;を選択します。

1. _[!UICONTROL Actions]_の下で、**[!UICONTROL Create New Catalog Product(s)]**をクリックします。

1. 確認メッセージを受け入れて&#x200B;_[!UICONTROL Create Magento Catalog Product]_ページを開くには、**[!UICONTROL OK]**をクリックします。

1. 製品のカタログ設定を完了します。

   >[!NOTE]
   >選択した複数のリスト用にカタログ製品を作成する場合、入力した製品設定はすべてのリストに適用されます。

   - **[!UICONTROL Enable Product(s)]**&#x200B;トグルを`Yes`または`No`（必須）に設定します。

      |はい|[!DNL Commerce]ストアフロントの販売に適した製品を選択します。|
|いいえ|[!DNL Commerce]ストアフロントの販売に対して、製品を不適格にする場合に選択します。|

   - **[!UICONTROL Categories]**&#x200B;の場合、製品のカテゴリを割り当てます（オプション）。

      製品のカテゴリを選択するには、下向き矢印をクリックし、カテゴリのチェックボックスを選択します。 終了したら「**完了**」をクリックします。

   - **[!UICONTROL Website Ids]**&#x200B;の場合、製品を関連付けるWebサイト（ストアフロント）を選択します。

      このリストのオプションは、[!DNL Commerce] [ストア設定](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}の設定によって異なります。

   - **[!UICONTROL Attribute Set Id]**（必須）には、オプションを選択します。

      `Default` はデフォルトの選択です。このリストのオプションは、設定した[!DNL Commerce] [属性セット](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}によって異なります。

   - **[!UICONTROL Visibility]**&#x200B;の場合は、新製品のオプションを選択します。

      |**[!UICONTROL Not Visible Individually]**（デフォルト）|ストアフロントのリストには製品が含まれていませんが、他の製品のバリエーションとして使用できます。|
|**[!UICONTROL Catalog]**|商品がカタログリストに表示されます。|
|**[!UICONTROL Search]**|製品は検索操作に使用できます。|
|**[!UICONTROL Catalog and Search]**|商品はカタログリストに含まれ、検索操作に使用できます。|

   - **[!UICONTROL Assign Tax Class]**&#x200B;の場合、製品のオプションを選択します。

      このリストに表示されるオプションは、設定した[tax classes](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}によって異なります。

   - 完了したら、「**[!UICONTROL Create Catalog Products]**」をクリックします。

カタログ商品は[!DNL Commerce]カタログに作成され、作成元のAmazonリストに割り当てられます。 現在は、リストが対応するAmazonのリストと一致するので、リストは[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)タブから削除され、[_[!UICONTROL Active]_](./active-listings.md)タブに表示されます。

![コマースカタログ製品の作成](assets/amazon-magento-catalog-product.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Enable Product(s)] | （必須）有効にすると、製品が[!DNL Commerce]ストアフロントに表示されます。 無効にすると、製品は[!DNL Commerce]ストアフロントに表示されません。 |
| [!UICONTROL Categories] | 新しい製品のカテゴリの名前を入力するか、下向き矢印をクリックしてカテゴリを選択してオプションを表示できます。 オプションは、[categories](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}の設定によって異なります。 |
| [!UICONTROL Website Ids] | （必須）製品を関連付けるWebサイト（ストアフロント）を選択します。 オプションは、[!DNL Commerce] [ストア設定](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}設定によって異なります |
| 属性セットID | 属性セットを選択します。 オプションは、設定した[!DNL Commerce] [属性セット](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}によって異なります。 |
| [!UICONTROL Visibility] | オプション：<ul><li>**[!UICONTROL Not Visible Individually]**  — 製品はストアフロントに表示されま [!DNL Commerce] せん（バリアント製品で最も一般的）。</li><li>**[!UICONTROL Catalog]** - Webサイト内で関連付けられているカテゴリを通じて製品にアクセスできます。</li><li>**検索**  — 検索ツールを使用した場合にのみ製品を検索できます。</li><li>**[!UICONTROL Catalog and Search]**  — カテゴリ構造を使用し、検索ツールを使用して製品にアクセスできます。</li></ul> |
| [!UICONTROL Assign Tax Class] | 新しい製品に税区分を割り当てます。 オプションは、設定した[tax classes](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}によって異なります。 |
