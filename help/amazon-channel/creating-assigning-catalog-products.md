---
title: Amazon Sales Channel の商品の作成と割り当て
description: Amazon Sales Channelは、次の機能を提供します [!UICONTROL New Third Party] Amazon リストで一致するCommerce カタログ商品を作成し、割り当てるのに役立つタブです。
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# 製品の作成と割り当て

表示中 _[!UICONTROL New Third Party]_タブで、次と一致させることができます [!DNL Commerce] 既存のAmazon リストへのカタログ製品。 このマッチングには 2 つのオプションがあります。 リストを既存のカタログ製品に割り当てることも、リストの情報を使用してカタログ製品を作成することもできます。 これらのオプションは、Amazonのリストがユーザーのリストと自動一致しない場合に役立ちます [!DNL Commerce] カタログ。

Amazonのセールスチャネルのすべての機能セットを使用するには、商品をAmazonのリストに一致させる（または割り当てる）必要があります。

Amazon リストからカタログ製品を作成する場合：

- この **ASIN** がになります [!DNL Commerce] SKU
- この **商品リスト名** はカタログリスト名になります
- この **価格** および **数量** は、Amazon リストから読み込まれます

その他の必要な設定は、 [!DNL Commerce] 作成時に選択した製品設定。

作成して一致させると、リストはから削除されます。 _[!UICONTROL New Third Party]_tab キーを押すと次の場所に表示されます_[!UICONTROL Active]_ タブ。

## 1 つのカタログ商品のAmazon リストへの割り当て

1. の製品リストを表示する [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブ。

1. 割り当てるリストをリストで見つけて、 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列を選択し、**[!UICONTROL Assign Catalog Product]**.

   このアクションにより、が開きます _[!UICONTROL Assign Magento Catalog Product]_ページ。

1. を使用してリストを参照またはフィルタリングする [workspace コントロール](./workspace-controls.md) リストに一致する適切なカタログ製品を見つけます。

1. リストに正しい製品が表示されたら、 **[!UICONTROL Assign Catalog Product]** が含まれる _[!UICONTROL Action]_列。

これで、製品とリストが一致しました。 Amazonのセールスチャネルは、商品およびリストデータをAmazonと共有し、リスト価格、発送価格、在庫/数量、注文情報、ステータスなどのリストとその情報を管理できるようになりました。

## Amazonのリスト情報を使用して、1 つのカタログ製品を作成する

1. の製品リストを表示する [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブ。

1. で作成するリストを見つけます [!DNL Commerce] カタログ、クリック **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列を選択し、**[!UICONTROL Create New Catalog Product]**.

   このアクションにより、が開きます _[!UICONTROL Create Magento Catalog Product]_ページ。

1. 商品のカタログ設定を入力します。

   - を設定 **[!UICONTROL Enable Product(s)]** 切り替え `Yes` または `No` （必須）。

     |はい|製品を自分の製品に対して適格にするための選択 [!DNL Commerce] ストアフロント販売。| |いいえ|お客様の製品を不適格にします [!DNL Commerce] ストアフロント販売。|

   - の場合 **[!UICONTROL Categories]**、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックしてカテゴリのチェックボックスを選択します。 クリック **[!UICONTROL Done]** 終了したとき。

   - の場合 **[!UICONTROL Website Ids]**：製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、 [!DNL Commerce] [ストアの設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定。

   - の場合 **[!UICONTROL Attribute Set Id]** （必須）、オプションを選択します。

     `Default` はデフォルトの選択です。 このリストのオプションは、 [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) が設定されました。

   - の場合 **[!UICONTROL Visibility]**、新製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （既定）|この商品は、別の商品のバリエーションとして利用できる可能性がありますが、ストアフロントの一覧には含まれていません。| |**[!UICONTROL Catalog]**|カタログの一覧に製品が表示されます。| |**[!UICONTROL Search]**|製品は検索操作に使用できます。| |**[!UICONTROL Catalog and Search]**|製品はカタログ一覧に含まれ、検索操作に使用できます。|

   - の場合 **[!UICONTROL Assign Tax Class]**、製品のオプションを選択します。

     このリストに表示されるオプションは、 [税クラス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) が設定されました。

   - 完了したら、 **[!UICONTROL Create Catalog Products]**.

カタログ製品がに作成されます。 [!DNL Commerce] カタログを作成し、作成元のAmazon リストに割り当てる。 リストが既存のAmazon リストと一致するようになったので、リストは _[!UICONTROL New Third Party]_tab キーを押して次に表示：_[!UICONTROL Active]_ タブ。

## Amazonのリスト情報を使用して、複数のカタログ製品を作成する

1. の製品リストを表示する [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブ。

1. カタログ製品を作成する一覧を選択します。

   左側の列で個々のチェックボックスを選択するか、左上の列の下向き矢印をクリックして選択します。 **[!UICONTROL Select All]** または **[!UICONTROL Select All on this Page]**.

1. 次の下 _[!UICONTROL Actions]_を選択し、**[!UICONTROL Create New Catalog Product(s)]**.

1. 確認メッセージを受け入れて、を開くには _[!UICONTROL Create Magento Catalog Product]_ページ、クリック&#x200B;**[!UICONTROL OK]**.

1. 製品のカタログ設定を入力します。

   >[!NOTE]
   >選択した複数の一覧に対してカタログ製品を作成する場合、入力した製品設定はすべての一覧に適用されます。

   - を設定 **[!UICONTROL Enable Product(s)]** 切り替え `Yes` または `No` （必須）。

     |はい|製品を自分の製品に対して適格にするための選択 [!DNL Commerce] ストアフロント販売。| |いいえ|お客様の製品を不適格にします [!DNL Commerce] ストアフロント販売。|

   - の場合 **[!UICONTROL Categories]**、製品のカテゴリを割り当てます（オプション）。

     製品のカテゴリを選択するには、下向き矢印をクリックしてカテゴリのチェックボックスを選択します。 クリック **完了** 終了したとき。

   - の場合 **[!UICONTROL Website Ids]**：製品を関連付ける web サイト（ストアフロント）を選択します。

     このリストのオプションは、 [!DNL Commerce] [ストアの設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定。

   - の場合 **[!UICONTROL Attribute Set Id]** （必須）、オプションを選択します。

     `Default` はデフォルトの選択です。 このリストのオプションは、 [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) が設定されました。

   - の場合 **[!UICONTROL Visibility]**、新製品のオプションを選択します。

     |**[!UICONTROL Not Visible Individually]** （既定）|この商品は、別の商品のバリエーションとして利用できる可能性がありますが、ストアフロントの一覧には含まれていません。| |**[!UICONTROL Catalog]**|カタログの一覧に製品が表示されます。| |**[!UICONTROL Search]**|製品は検索操作に使用できます。| |**[!UICONTROL Catalog and Search]**|製品はカタログ一覧に含まれ、検索操作に使用できます。|

   - の場合 **[!UICONTROL Assign Tax Class]**、製品のオプションを選択します。

     このリストに表示されるオプションは、 [税クラス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) が設定されました。

   - 完了したら、 **[!UICONTROL Create Catalog Products]**.

カタログ製品がに作成されます。 [!DNL Commerce] カタログを作成し、作成元のAmazon リストに割り当てる。 のリストが各Amazonのリストと一致した状態で、 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) tab キーを押して次に表示： [_[!UICONTROL Active]_](./active-listings.md) タブ。

![Commerce カタログ製品を作成](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | （必須）有効にすると、製品がユーザーに表示されます [!DNL Commerce] ストアフロント。 無効にした場合、製品はユーザーの [!DNL Commerce] ストアフロント。 |
| [!UICONTROL Categories] | 新しい製品のカテゴリ名を入力するか、下向き矢印をクリックしてオプションを表示してカテゴリを選択できます。 オプションは、 [カテゴリ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) 設定。 |
| [!UICONTROL Website Ids] | （必須）製品を関連付ける web サイト（ストアフロント）を選択します。 オプションは、 [!DNL Commerce] [ストアの設定](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) 設定 |
| 属性セット Id | 属性セットを選択します。 オプションは、設定したによって異なります [!DNL Commerce] [属性セット](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | オプション：<ul><li>**[!UICONTROL Not Visible Individually]**  – 製品がユーザーに表示されない [!DNL Commerce] ストアフロント（バリアント製品で最も一般的）。</li><li>**[!UICONTROL Catalog]**  – 製品が web サイト内で関連付けられているカテゴリを通じて製品にアクセスできるようにします。</li><li>**検索**  – 検索ツールでのみ見つけることができる製品を許可します。</li><li>**[!UICONTROL Catalog and Search]** - カテゴリ構造と検索ツールを使用して、商品にアクセスできます。</li></ul> |
| [!UICONTROL Assign Tax Class] | 新しい商品に税区分を割り当てます。 オプションは、設定したによって異なります [税クラス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
