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

_[!UICONTROL Product Listings]_のページには、すべてのリストのステータスを確認し、商品をAmazonのリストに一致させるタブがいくつか含まれています。

使用可能なリストタスクはタブごとに少し異なりますが、[ ワークスペースコントロール ](./workspace-controls.md) は同じであり、リストに表示するデータをカスタマイズできます。

**[!UICONTROL Actions]** の下のオプションは複数のリストにアクションを適用できますが、_[!UICONTROL Action]_の列の&#x200B;**[!UICONTROL Select]**の下のオプションは個々のリストにのみアクションを適用します。

[ アクション別の一覧の管理 ](./managing-listings-by-action.md) も参照してください。

![ 製品リストタブ ](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| タブ | 説明 | アクション |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 定義済みのリスト設定を満たしているが、Amazonでリストの作成に必要な情報が欠落している [!DNL Commerce] カタログ商品を表示します。<br><br>[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定で _[!UICONTROL Automatic List Action]_が `Automatically List Eligible Products` に設定されている場合、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**です。 | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | [!DNL Commerce] カタログ内の商品と一致しない既存のAmazon リストを表示します（Amazonから受信した情報に基づく）。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br> 自動照合を試行 <br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Amazonの一覧を作成する準備ができているカタログ商品を表示しますが、ストアは新しい一覧を自動的に公開しないように設定されています。 このタブは、新しいリストを手動で公開するために使用します。<br><br>[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定で _[!UICONTROL Automatic List Action]_が `Do Not Automatically List Eligible Products` に設定されている場合、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**です。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Amazonに公開されたが、Amazonがアクティブ ステータスのリストを承認していないカタログ製品を表示します。 | [ 終了 Amazon/マーチャントによるフルフィルメント ](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br> 切り替えに対するAmazonでのリスト <br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | [!DNL Commerce] カタログの商品と一致し、Amazonに公開され、Amazonからアクティブのステータスを取得したAmazonのリストを表示します。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントによるフルフィルメントに切り替え <br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 定義済みの上書きの条件を満たし、上書きが適用されたAmazonのリストを表示します。 上書きは、他のアカウント設定よりも優先されます。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 定義済みの [ リスト設定 ](./listing-settings.md) に基づいて、実施要件を満たさなくなった既存のAmazonのリストを表示します。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントによるフルフィルメントに切り替え <br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Amazonから手動で終了（削除）したAmazonのリストを表示します。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 製品リストへのアクセス

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. ストアカードの **[!UICONTROL View Store]** をクリックします。

1. ストアダッシュボードで、「_[!UICONTROL Store Listings]_」セクションの「**[!UICONTROL Manage Listings]**」をクリックします。
