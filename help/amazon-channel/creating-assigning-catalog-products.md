---
title: Amazon Sales Channel の商品の作成と割り当て
description: Amazon Sales Channelには、Amazonのリストに一致するCommerce カタログ製品を作成して割り当てるのに役立つ「[!UICONTROL New Third Party]」タブが用意されています。
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# 製品の作成と割り当て

タブ _[!UICONTROL New Third Party]_表示すると、[!DNL Commerce] のカタログ製品を既存のAmazon リストと一致させることができます。 このマッチングには 2 つのオプションがあります。 リストを既存のカタログ製品に割り当てることも、リストの情報を使用してカタログ製品を作成することもできます。 これらのオプションは、Amazonのリストが [!DNL Commerce] カタログと自動一致しない場合に役立ちます。

Amazonのセールスチャネルのすべての機能セットを使用するには、商品をAmazonのリストに一致させる（または割り当てる）必要があります。

Amazon リストからカタログ製品を作成する場合：

- **ASIN** が [!DNL Commerce] SKU になります
- **製品リスト名** がカタログリスト名になります
- **価格** および **数量** は、Amazonリストから読み込まれます

残りの必要な設定は、作成時に選択した [!DNL Commerce] の製品設定によって決まります。

作成して一致させると、リストは「_[!UICONTROL New Third Party]_」タブから削除され、「_[!UICONTROL Active]_」タブに表示されます。

## 1 つのカタログ商品のAmazon リストへの割り当て

1. 製品リストを [[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)] タブで表示します。

1. リストで割り当てるリストを見つけ、_[!UICONTROL Action]_の列の「**[!UICONTROL Select]**」をクリックし、「**[!UICONTROL Assign Catalog Product]**」をクリックします。

   このアクションにより、_[!UICONTROL Assign Magento Catalog Product]_ページが開きます。

1. [ ワークスペースコントロール ](./workspace-controls.md) を使用してリストを参照またはフィルタリングし、リストに一致する適切なカタログ製品を見つけます。

1. リストに正しい製品が表示されたら、_[!UICONTROL Action]_の列の&#x200B;**[!UICONTROL Assign Catalog Product]**をクリックします。

これで、製品とリストが一致しました。 Amazonのセールスチャネルは、商品およびリストデータをAmazonと共有し、リスト価格、発送価格、在庫/数量、注文情報、ステータスなどのリストとその情報を管理できるようになりました。

## Amazonのリスト情報を使用して、1 つのカタログ製品を作成する

1. 製品リストを [[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)] タブで表示します。

1. [!DNL Commerce] カタログで作成するリストを見つけ、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックして、**[!UICONTROL Create New Catalog Product]**をクリックします。

   このアクションにより、_[!UICONTROL Create Magento Catalog Product]_ページが開きます。

1. 商品のカタログ設定を入力します。

   - 切り替え **[!UICONTROL Enable Product(s)]**`Yes` または `No` に設定します（必須）。

     |はい|商品を [!DNL Commerce] ストアフロント販売の対象とするかどうかを選択します。|
|いいえ|[!DNL Commerce] ストアフロントの販売に対して、製品が不適格になるように選択します。|

   - **[!UICONTROL Categories]** しくは、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックしてカテゴリのチェックボックスを選択します。 終了したら「**[!UICONTROL Done]**」をクリックします。

   - **[!UICONTROL Website Ids]**：製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、[!DNL Commerce] [ ストア設定 ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) の設定によって異なります。

   - **[!UICONTROL Attribute Set Id]** （必須）の場合は、オプションを選択します。

     デフォルトの選択は `Default` です。 このリストのオプションは、設定した [!DNL Commerce] [ 属性セット ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) によって異なります。

   - **[!UICONTROL Visibility]** の場合は、新製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （デフォルト）|この商品は、別の商品のバリエーションとして利用できる場合がありますが、ストアフロントのリストには含まれていません。|
|**[!UICONTROL Catalog]**|商品がカタログ一覧に表示されます。|
|**[!UICONTROL Search]**|製品は検索操作に使用できます。|
|**[!UICONTROL Catalog and Search]**|製品はカタログ一覧に含まれ、検索操作に使用できます。|

   - **[!UICONTROL Assign Tax Class]** の場合は、製品のオプションを選択します。

     このリストに表示されるオプションは、設定した [ 税区分 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) によって異なります。

   - 完了したら、「**[!UICONTROL Create Catalog Products]**」をクリックします。

カタログ製品が [!DNL Commerce] カタログ内に作成され、作成元のAmazon リストに割り当てられます。 リストが既存のAmazon リストと一致した状態で、リストは「_[!UICONTROL New Third Party]_」タブから削除され、「_[!UICONTROL Active]_」タブに表示されます。

## Amazonのリスト情報を使用して、複数のカタログ製品を作成する

1. 製品リストを [[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)] タブで表示します。

1. カタログ製品を作成する一覧を選択します。

   左側の列で個々のチェックボックスを選択するか、左上の列の下向き矢印をクリックして「**[!UICONTROL Select All]**」または「**[!UICONTROL Select All on this Page]**」を選択します。

1. [_[!UICONTROL Actions]_] で、[**[!UICONTROL Create New Catalog Product(s)]**] をクリックします。

1. 確認メッセージを受け入れて _[!UICONTROL Create Magento Catalog Product]_ページを開くには、「**[!UICONTROL OK]**」をクリックします。

1. 製品のカタログ設定を入力します。

   >[!NOTE]
   >選択した複数の一覧に対してカタログ製品を作成する場合、入力した製品設定はすべての一覧に適用されます。

   - 切り替え **[!UICONTROL Enable Product(s)]**`Yes` または `No` に設定します（必須）。

     |はい|商品を [!DNL Commerce] ストアフロント販売の対象とするかどうかを選択します。|
|いいえ|[!DNL Commerce] ストアフロントの販売に対して、製品が不適格になるように選択します。|

   - **[!UICONTROL Categories]** しくは、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックしてカテゴリのチェックボックスを選択します。 終了したら、「**完了**」をクリックします。

   - **[!UICONTROL Website Ids]**：製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、[!DNL Commerce] [ ストア設定 ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) の設定によって異なります。

   - **[!UICONTROL Attribute Set Id]** （必須）の場合は、オプションを選択します。

     デフォルトの選択は `Default` です。 このリストのオプションは、設定した [!DNL Commerce] [ 属性セット ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) によって異なります。

   - **[!UICONTROL Visibility]** の場合は、新製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （デフォルト）|この商品は、別の商品のバリエーションとして利用できる場合がありますが、ストアフロントのリストには含まれていません。|
|**[!UICONTROL Catalog]**|商品がカタログ一覧に表示されます。|
|**[!UICONTROL Search]**|製品は検索操作に使用できます。|
|**[!UICONTROL Catalog and Search]**|製品はカタログ一覧に含まれ、検索操作に使用できます。|

   - **[!UICONTROL Assign Tax Class]** の場合は、製品のオプションを選択します。

     このリストに表示されるオプションは、設定した [ 税区分 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) によって異なります。

   - 完了したら、「**[!UICONTROL Create Catalog Products]**」をクリックします。

カタログ製品は [!DNL Commerce] カタログ内に作成され、作成元のAmazon リストに割り当てられます。 リストがそれぞれのAmazon リストに一致するようになったので、リストは「[_[!UICONTROL New Third Party]_](./new-third-party-listings.md)」タブから削除され、「[_[!UICONTROL Active]_](./active-listings.md)」タブに表示されます。

![Commerce カタログ製品の作成 ](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | （必須）有効になっている場合、製品は [!DNL Commerce] ストアフロントに表示されます。 無効にした場合、製品は [!DNL Commerce] ストアフロントに表示されません。 |
| [!UICONTROL Categories] | 新しい製品のカテゴリ名を入力するか、下向き矢印をクリックしてオプションを表示してカテゴリを選択できます。 オプションは、[ カテゴリ ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) 設定によって異なります。 |
| [!UICONTROL Website Ids] | （必須）製品を関連付ける web サイト（ストアフロント）を選択します。 オプションは、[!DNL Commerce] の [ ストア設定 ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定によって異なります |
| 属性セット Id | 属性セットを選択します。 オプションは、設定した [!DNL Commerce] [ 属性セット ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) によって異なります。 |
| [!UICONTROL Visibility] | オプション：<ul><li>**[!UICONTROL Not Visible Individually]** – 製品が [!DNL Commerce] ストアフロントに表示されません（バリアント製品で最も一般的）。</li><li>**[!UICONTROL Catalog]** – 製品が web サイト内で関連付けられているカテゴリを通じて製品にアクセスできるようにします。</li><li>**検索** – 検索ツールでのみ見つけることができる製品を許可します。</li><li>**[!UICONTROL Catalog and Search]** - カテゴリ構造を通じて、および検索ツールを使用して、製品にアクセスできるようにします。</li></ul> |
| [!UICONTROL Assign Tax Class] | 新しい商品に税区分を割り当てます。 オプションは、設定した [ 税金クラス ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) によって異なります。 |
