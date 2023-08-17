---
title: Amazonの製品リストをステータス/タブ別に管理
description: Amazonの一覧を管理する際は、ステータスに応じて一覧にアクションを適用できます。
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Amazonの製品リストをステータス/タブ別に管理

The _[!UICONTROL Product Listings]_ページにはいくつかのタブが含まれており、このタブで、すべてのリストのステータスを表示し、製品をAmazonのリストに一致させることができます。

使用可能なリストタスクはタブごとに少し異なりますが、 [workspace コントロール](./workspace-controls.md) は同じで、お使いのリストに表示するデータをカスタマイズできます。

以下のオプション **[!UICONTROL Actions]** は複数のリストにアクションを適用でき、は以下のオプションです。 **[!UICONTROL Select]** （内） _[!UICONTROL Action]_「 」列は、個々のリストにのみアクションを適用します。

関連トピック [アクションごとにリストを管理](./managing-listings-by-action.md).

![「製品リスト」タブ](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| タブ | 説明 | アクション |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | 次の項目を表示： [!DNL Commerce] 定義済みのリスト設定を満たすが、リストにAmazonで必要な情報が不足しているカタログ製品。<br><br>次の場合 _[!UICONTROL Automatic List Action]_が `Automatically List Eligible Products` の [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Amazonから受け取った情報に基づいて、お使いの [!DNL Commerce] カタログ。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>自動一致を試みる<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Amazonリストを作成する準備ができたカタログ製品を表示しますが、ストアは新しいリストを自動的に公開しないように設定されています。 このタブは、新しいリストを手動で公開する場合に使用します。<br><br>次の場合 _[!UICONTROL Automatic List Action]_が `Do Not Automatically List Eligible Products` の [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定、これらの項目は&#x200B;**[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Amazonに公開されたカタログ製品が表示されますが、Amazonがアクティブステータスのリストを承認していません。 | [終了 Amazonでのリスト](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントが満たすに切り替え<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | お使いのAmazonの製品に一致する製品リストを表示します [!DNL Commerce] カタログを作成し、Amazonに公開された、Amazonからアクティブステータスに変更されたこと。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントが満たすに切り替え<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 定義済みの上書きの条件を満たし、上書きが適用されたAmazonのリストを表示します。 上書きは、他のアカウント設定よりも優先されます。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | 定義した内容に基づいて、適格でなくなった既存のAmazonリストを表示します [リスト設定](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/マーチャントが満たすに切り替え<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Amazonから手動で終了（削除）したAmazonリストを表示します。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 製品リストにアクセス

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL View Store]** をストアカードに貼り付けます。

1. ストアのダッシュボードで、 **[!UICONTROL Manage Listings]** （内） _[!UICONTROL Store Listings]_」セクションに入力します。
