---
title: 不適格なAmazonの一覧
description: Amazon セールスチャネルの主な機能は次のとおりです [!UICONTROL Ineligible] 現在のリストルールに基づいてリストとして適格でない項目の管理に役立つタブ。
feature: Sales Channels, Products
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 不適格なAmazonの一覧

この _[!UICONTROL Ineligible]_tab キーを押すと、現在Amazonで公開されているが、現在のリストルールに基づくリストとしては適格でないすべての商品のリストが表示されます。 以前の商品が適格で、リスト規則が変更されて不適格になった場合、商品に関連付けられた数量は 0 に低下し、その商品は次のようにマークされます_&#x200B;不適格な&#x200B;_. ただし、そのファイルは現在もユーザーに存在します [!DNL Amazon Seller Account].

から製品を移動するには _[!UICONTROL Ineligible]_タブから、以下を実行できます [リストルールの変更](./listing-rules.md) お使いの製品が対象となります。

で使用可能なアクション _[!UICONTROL Ineligible]_タブには次が含まれます。

次の下 _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**：選択したすべてのリストを [!DNL Amazon Marketplace]. 参照： [Amazon リストの終了](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**：リストの上書き設定の変更を選択します。 参照： [上書き](./overrides.md) または [上書きを編集または削除](./creating-editing-overrides.md#edit-override-single-listing).

次の下 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列：

- **[!UICONTROL View Details]**：次のようなリストの詳細を表示することを選択します [アクティビティログを一覧表示](./product-listing-details.md#listing-activity-log), [Buy Box競合他社価格](./product-listing-details.md#buy-box-competitor-pricing)、および [競合製品の最低価格](./product-listing-details.md#lowest-competitor-pricing). このアクションは表示専用です。 リストの詳細は変更できません。 参照： [詳細を表示](./product-listing-details.md).

- **[!UICONTROL Create Override]**：オーバーライドの作成を選択し、このリストに適用します。 参照： [上書きの作成](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**：カタログ製品に割り当てられた ASIN の変更を選択します。 このアクションは、カタログ内の製品が誤った ASIN と一致した場合に使用されます。 参照： [割り当てられた ASIN の編集](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ商品からAmazon リストを作成する際に使用できるエイリアス SKU を作成します。 参照： [Alias Seller SKU の作成](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：注文に関連付けられているフルフィルメント方法の変更を選択します。 参照： [フルフィルドの設定](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**：リストをから削除することを選択します [!DNL Amazon Marketplace]. 参照： [Amazon リストの終了](./end-listings-manually.md).

>[!NOTE]
>処理中のリストがある場合、リスト数はタブの上のメッセージに表示されます。

![不適格なAmazonの一覧](assets/amazon-ineligible-listings.png){width="600" zoomable="yes"}

Amazonのセールスチャネルのホームページには、いくつかの共通点があります [workspace コントロール](./workspace-controls.md) 表示するデータをカスタマイズできます。

## デフォルトの列

| 列 | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は AEM を表す [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | この [条件](./product-listing-condition.md) 商品の。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列を選択してオプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[上書きを作成](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
