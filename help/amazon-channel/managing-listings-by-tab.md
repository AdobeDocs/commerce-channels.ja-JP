---
title: ステータス/タブで製品リストを管理
description: Amazonのリストを管理する際に、ステータスに応じてアクションをリストに適用できます。
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# ステータス/タブで製品リストを管理

_[!UICONTROL Product Listings]_ページには、すべてのリストのステータスを表示し、製品をAmazonのリストに一致させるタブがいくつか含まれています。

各タブで使用できるリストタスクは少し異なりますが、[ワークスペースコントロール](./workspace-controls.md)は同じで、リストに表示するデータをカスタマイズできます。

**[!UICONTROL Actions]**&#x200B;の下のオプションは複数のリストにアクションを適用でき、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下のオプションは個々のリストにのみアクションを適用できます。

[アクション別のリストの管理](./managing-listings-by-action.md)も参照してください。

![製品リストタブ](assets/amazon-product-listings-tabs.png)

| タブ | 説明 | アクション |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 定義済みのリスト設定に一致するが、リストにAmazonで必要な情報が欠落している[!DNL Commerce]カタログ製品を表示します。<br><br>の設 _[!UICONTROL Automatic List Action]_定でがに設 `Automatically List Eligible Products` 定され [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) ている場合、項目はになります&#x200B;**[!UICONTROL In Progress Listings]**。 | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | [!DNL Commerce]カタログ内の製品と一致しない、(Amazonから受け取った情報に基づいて)既存のAmazonリストを表示します。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>自動一致の試行<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Amazonリストを作成する準備ができたが、ストアが新しいリストを自動的に公開しないように設定されているカタログ製品を表示します。 このタブは、新しいリストを手動で発行する場合に使用します。<br><br>の設 _[!UICONTROL Automatic List Action]_定でがに設 `Do Not Automatically List Eligible Products` 定され [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) ている場合、項目はになります&#x200B;**[!UICONTROL In Progress Listings]**。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Amazonに公開されたが、Amazonがアクティブステータスのリストを承認していないカタログ商品を表示します。 | [ Amazon/マーチャントが処理す](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>るAmazonSwitchのエンドリスト<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | [!DNL Commerce]カタログ内の製品と一致し、Amazonに公開され、AmazonによってアクティブステータスにされたAmazonのリストを表示します。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/商人が履行する<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 定義済みの上書きの条件を満たし、上書きが適用されたAmazonのリストを表示します。 上書きは、他のアカウント設定よりも優先されます。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 定義した[リスト設定](./listing-settings.md)に基づいて、不適格になった既存のAmazonリストを表示します。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/商人が履行する<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Amazonから手動で終了（削除）されたAmazonリストを表示します。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 製品リストへのアクセス

1. _管理_&#x200B;サイドバーで、**[!UICONTROL Marketing]** / _[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

1. ストアダッシュボードで、_[!UICONTROL Store Listings]_セクションの&#x200B;**[!UICONTROL Manage Listings]**をクリックします。
