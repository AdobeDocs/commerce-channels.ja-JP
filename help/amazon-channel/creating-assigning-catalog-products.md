---
title: Amazonセールスチャネル用の製品の作成と割り当て
description: AmazonSales Channelが [!UICONTROL New Third Party] タブは、一致するコマースカタログ製品を作成し、Amazonリストに割り当てるのに役立ちます。
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# 製品の作成と割り当て

表示時 _[!UICONTROL New Third Party]_」タブで、 [!DNL Commerce] 製品を既存のAmazonリストにカタログ化します。 この照合には、2 つのオプションがあります。 既存のカタログ商品にリストを割り当てたり、リストの情報を使用してカタログ商品を作成したりできます。 これらのオプションは、Amazonのリストが [!DNL Commerce] カタログ。

Amazonセールスチャネルの完全な機能セットを使用するには、製品をAmazonリストに照合（または割り当て）する必要があります。

Amazonリストからカタログ商品を作成する場合：

- The **ASIN** が [!DNL Commerce] SKU
- The **製品リスト名** は「カタログリスト名」になります。
- The **価格** および **数量** をAmazon Listing から読み込む

残りの必要な設定は、 [!DNL Commerce] 作成時に選択する製品設定。

リストが作成され、一致すると、 _[!UICONTROL New Third Party]_タブに移動して、_[!UICONTROL Active]_ タブをクリックします。

## 1 つのカタログ製品をAmazonリストに割り当てる

1. 次の場所で製品リストを表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブをクリックします。

1. 割り当てるリストをリストで見つけ、 **[!UICONTROL Select]** （内） _[!UICONTROL Action]_列をクリックし、**[!UICONTROL Assign Catalog Product]**.

   このアクションを実行すると、 _[!UICONTROL Assign Magento Catalog Product]_ページに貼り付けます。

1. を使用してリストを参照するか、フィルターします。 [workspace コントロール](./workspace-controls.md) リストに一致する適切なカタログ製品を見つけます。

1. リストに正しい製品が表示されたら、 **[!UICONTROL Assign Catalog Product]** （内） _[!UICONTROL Action]_列。

これで、製品とリストが一致します。 Amazonのセールスチャネルは、Amazonと製品およびリストデータを共有し、リストとその情報（リスト価格、送料、在庫/数量、注文情報およびステータスなど）を管理できるようになりました。

## Amazonリスト情報を使用して、単一のカタログ製品を作成する

1. 次の場所で製品リストを表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブをクリックします。

1. に作成するリストを見つけます。 [!DNL Commerce] カタログ、クリック **[!UICONTROL Select]** （内） _[!UICONTROL Action]_列をクリックし、**[!UICONTROL Create New Catalog Product]**.

   このアクションを実行すると、 _[!UICONTROL Create Magento Catalog Product]_ページに貼り付けます。

1. 製品のカタログ設定を完了します。

   - 設定 **[!UICONTROL Enable Product(s)]** 切り替える `Yes` または `No` （必須）。

     |はい|製品を適格な製品にする [!DNL Commerce] ストアフロントの販売。| |いいえ|製品を不適格にするように選択します [!DNL Commerce] ストアフロントの販売。|

   - の場合 **[!UICONTROL Categories]**、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックして、カテゴリのチェックボックスを選択します。 クリック **[!UICONTROL Done]** 終了したとき。

   - の場合 **[!UICONTROL Website Ids]**」で、製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、 [!DNL Commerce] [ストア設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定。

   - の場合 **[!UICONTROL Attribute Set Id]** （必須）」で、オプションを選択します。

     `Default` はデフォルトの選択です。 このリストのオプションは、 [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) 設定済みです。

   - の場合 **[!UICONTROL Visibility]**」で、新しい製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （デフォルト）|製品は、別の製品のバリエーションとして使用できる場合がありますが、ストアフロントのリストには含まれていません。| |**[!UICONTROL Catalog]**|カタログリストに商品が表示されます。| |**[!UICONTROL Search]**|製品は検索操作に使用できます。| |**[!UICONTROL Catalog and Search]**|商品はカタログ一覧に含まれており、検索操作に使用できます。|

   - の場合 **[!UICONTROL Assign Tax Class]**」で、製品のオプションを選択します。

     このリストに表示されるオプションは、 [税制](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) 設定済みです。

   - 完了したら、「 **[!UICONTROL Create Catalog Products]**.

カタログ製品が [!DNL Commerce] カタログに割り当てられ、作成元のAmazonリストに割り当てられます。 現在は、リストが既存のAmazonリストと一致するので、リストは _[!UICONTROL New Third Party]_」タブに移動して、_[!UICONTROL Active]_ タブをクリックします。

## Amazonリスト情報を使用して複数のカタログ製品を作成する

1. 次の場所で製品リストを表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブをクリックします。

1. カタログ商品を作成するリストを選択します。

   左側の列で個々のチェックボックスを選択するか、左上の列の下矢印をクリックしてを選択します。 **[!UICONTROL Select All]** または **[!UICONTROL Select All on this Page]**.

1. の下 _[!UICONTROL Actions]_をクリックし、**[!UICONTROL Create New Catalog Product(s)]**.

1. 確認メッセージを受け入れて、 _[!UICONTROL Create Magento Catalog Product]_ページ、クリック&#x200B;**[!UICONTROL OK]**.

1. 製品のカタログ設定を完了します。

   >[!NOTE]
   >選択した複数のリストに対してカタログ商品を作成する場合、入力した商品設定がすべてのリストに適用されます。

   - 設定 **[!UICONTROL Enable Product(s)]** 切り替える `Yes` または `No` （必須）。

     |はい|製品を適格な製品にする [!DNL Commerce] ストアフロントの販売。| |いいえ|製品を不適格にするように選択します [!DNL Commerce] ストアフロントの販売。|

   - の場合 **[!UICONTROL Categories]**、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックして、カテゴリのチェックボックスを選択します。 クリック **完了** 終了したとき。

   - の場合 **[!UICONTROL Website Ids]**」で、製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、 [!DNL Commerce] [ストア設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定。

   - の場合 **[!UICONTROL Attribute Set Id]** （必須）」で、オプションを選択します。

     `Default` はデフォルトの選択です。 このリストのオプションは、 [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) 設定済みです。

   - の場合 **[!UICONTROL Visibility]**」で、新しい製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （デフォルト）|製品は、別の製品のバリエーションとして使用できる場合がありますが、ストアフロントのリストには含まれていません。| |**[!UICONTROL Catalog]**|カタログリストに商品が表示されます。| |**[!UICONTROL Search]**|製品は検索操作に使用できます。| |**[!UICONTROL Catalog and Search]**|商品はカタログ一覧に含まれており、検索操作に使用できます。|

   - の場合 **[!UICONTROL Assign Tax Class]**」で、製品のオプションを選択します。

     このリストに表示されるオプションは、 [税制](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) 設定済みです。

   - 完了したら、「 **[!UICONTROL Create Catalog Products]**.

カタログ製品は、 [!DNL Commerce] カタログに割り当てられ、作成元のAmazonリストに割り当てられます。 現在は、リストがそれぞれのAmazonリストと一致し、リストは [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) 」タブに移動して、 [_[!UICONTROL Active]_](./active-listings.md) タブをクリックします。

![コマースカタログ製品を作成](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | （必須）有効にすると、製品が [!DNL Commerce] ストアフロント。 無効にすると、製品は [!DNL Commerce] ストアフロント。 |
| [!UICONTROL Categories] | 新しい製品のカテゴリの名前を入力するか、下向き矢印をクリックしてオプションを表示してカテゴリを選択できます。 オプションは、 [カテゴリ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) 設定。 |
| [!UICONTROL Website Ids] | （必須）製品を関連付ける Web サイト（ストアフロント）を選択します。 オプションは、 [!DNL Commerce] [ストア設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定 |
| 属性セット ID | 属性セットを選択します。 オプションは、設定に応じて異なります [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | オプション：<ul><li>**[!UICONTROL Not Visible Individually]**  — 製品が [!DNL Commerce] storefront （バリアント製品で最も一般的）。</li><li>**[!UICONTROL Catalog]** - Web サイト内で関連付けられているカテゴリを通じて製品にアクセスできます。</li><li>**検索**  — 検索ツールを通じてのみ製品を検索できるようにします。</li><li>**[!UICONTROL Catalog and Search]**  — カテゴリ構造を使用し、検索ツールを使用して製品にアクセスできます。</li></ul> |
| [!UICONTROL Assign Tax Class] | 新しい製品に税区分を割り当てます。 オプションは、設定に応じて異なります [税制](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
