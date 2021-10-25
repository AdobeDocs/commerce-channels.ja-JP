---
title: ステータス/タブを使った製品リストの管理
description: Amazon リストを管理する際に、状態に応じてリストにアクションを適用することができます。
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# ステータス/タブを使った製品リストの管理

このページには、 _[!UICONTROL Product Listings]_すべての一覧の状態を表示し、製品を Amazon リストに適合するようにするためのタブがいくつか含まれています。

使用可能な一覧表示の内容はタブによって若干異なりますが、 [ ワークスペースコントロール ](./workspace-controls.md) は同じで、リストに表示するデータをカスタマイズすることができます。

「」のオプションは、 **[!UICONTROL Actions]** 複数のリストにアクションを適用することができますが、列の「オプション」で、その **[!UICONTROL Select]** _[!UICONTROL Action]_アクションは個別の一覧にのみ適用されます。

「 [ 操作別の一覧の管理」も参照してください ](./managing-listings-by-action.md) 。

![製品一覧タブ](assets/amazon-product-listings-tabs.png)

| タブ | つい | 活動 |
|--- |--- |--- |
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | は、 [!DNL Commerce] 定義されたリスティング設定に適合するが、Amazon によって一覧表示される必要がある情報が不足しているカタログ製品を示しています。<br><br>_[!UICONTROL Automatic List Action]_が「」に設定されている場合 `Automatically List Eligible Products` [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 、これらのアイテムはに設定されてい&#x200B;**[!UICONTROL In Progress Listings]**ます。 | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | カタログ内の製品に対応していない、Amazon から得た情報に基づいて、既存の Amazon リストが表示され [!DNL Commerce] ます。 | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>自動的に一致を試みる<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | では、Amazon リストを作成する準備ができているカタログ製品が表示されますが、ストアでは新しい一覧を自動的に公開するように設定されていません。 このタブを使用して、新しいリストを手動でパブリッシュします。<br><br>_[!UICONTROL Automatic List Action]_が「」に設定されている場合 `Do Not Automatically List Eligible Products` [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 、これらのアイテムはに設定されてい&#x200B;**[!UICONTROL In Progress Listings]**ます。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Amazon に公開されたカタログ製品を表示します。ただし、Amazon は、このリストをアクティブ状態にすることを許可されていません。 | [Amazon  ](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br> /商人によって処理されるように amazon の切り替え先リストが表示される<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | カタログ内の製品に一致した Amazon リストを表示し [!DNL Commerce] ます。 amazon に公開されており、amazon によって Active 状態が公開されています。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/商人によって履行されるように切り替え<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | 定義された上書きの条件を満たし、上書きが適用された Amazon リストが表示されます。 上書きは、その他のアカウント設定よりも優先されます。 | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | ここには、定義されたリスティング設定に基づいて、条件に該当しない既存の Amazon リストが表示され [ ](./listing-settings.md) ます。 | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Amazon/商人によって履行されるように切り替え<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | 手動で終了された Amazon、つまり手動で削除された Amazon リストが表示されます。 | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## 製品一覧へのアクセス

1. _管理者は_ 、> > を参照して **[!UICONTROL Marketing]** _[!UICONTROL Channels]_**[!UICONTROL Amazon Sales Channel]**ください。

1. **[!UICONTROL View Store]** Store カードをクリックします。

1. ストアのダッシュボードで、セクションをクリックし **[!UICONTROL Manage Listings]** _[!UICONTROL Store Listings]_ます。
