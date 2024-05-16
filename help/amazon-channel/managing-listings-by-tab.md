---
title: ステータス/タブ別のAmazon製品リストの管理
description: Amazonのリストを管理する際に、ステータスに応じてリストにアクションを適用できます。
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# ステータス/タブ別のAmazon製品リストの管理

この _[!UICONTROL Product Listings]_ページには、すべての商品リストのステータスを確認したり、商品をAmazonのリストに一致させたりできるタブがいくつかあります。

使用可能なリストタスクはタブごとに少し異なりますが、 [workspace コントロール](./workspace-controls.md) 同じであり、リストに表示するデータをカスタマイズできます。

の下のオプション **[!UICONTROL Actions]** ではアクションを複数のリストに適用でき、ではオプションを適用できます。 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列は、個々のリストにのみアクションを適用します。

関連トピック [アクション別リストの管理](./managing-listings-by-action.md).

![製品リストタブ](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| タブ | 説明 | アクション |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | を表示 [!DNL Commerce] 定義済みのリスト設定に一致するが、Amazonでリストに必要な情報が欠落している製品をカタログに追加できます。<br><br>次の場合 _[!UICONTROL Automatic List Action]_はに設定されています。 `Automatically List Eligible Products` が含まれる [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Amazonから受信した情報に基づいて、の商品と一致しない既存のAmazonのリストを表示します [!DNL Commerce] カタログ。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>自動照合を試みます<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Amazonの一覧を作成する準備ができているカタログ商品を表示しますが、ストアは新しい一覧を自動的に公開しないように設定されています。 このタブは、新しいリストを手動で公開するために使用します。<br><br>次の場合 _[!UICONTROL Automatic List Action]_はに設定されています。 `Do Not Automatically List Eligible Products` が含まれる [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Amazonに公開されたが、Amazonがアクティブ ステータスのリストを承認していないカタログ製品を表示します。 | [終了 Amazonでのリスト](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントによるフルフィルメントに切り替える<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | の商品と一致したAmazonの一覧を表示します [!DNL Commerce] カタログがAmazonに公開され、Amazonからアクティブ ステータスで公開されています。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントによるフルフィルメントに切り替える<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 定義済みの上書きの条件を満たし、上書きが適用されたAmazonのリストを表示します。 上書きは、他のアカウント設定よりも優先されます。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Amazon定義済みの [リスト設定](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントによるフルフィルメントに切り替える<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Amazonから手動で終了（削除）したAmazonのリストを表示します。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 製品リストへのアクセス

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL View Store]** ストアカードに。

1. ストアダッシュボードで、 **[!UICONTROL Manage Listings]** が含まれる _[!UICONTROL Store Listings]_セクション。
