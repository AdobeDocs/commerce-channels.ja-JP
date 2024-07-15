---
title: アクション別のAmazon製品リストの管理
description: Amazonのリストを管理する際に、個々または複数のリストにアクションを適用できます。
feature: Sales Channels, Products
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# アクション別のAmazon製品リストの管理

_[!UICONTROL Product Listings]_のページには、すべてのリストのステータスを確認し、商品をAmazonのリストに一致させるタブがいくつか含まれています。

使用可能なリストタスクはタブごとに少し異なりますが、[ ワークスペースコントロール ](./workspace-controls.md) は同じであり、リストに表示するデータをカスタマイズできます。

**[!UICONTROL Actions]** の下のオプションは複数のリストにアクションを適用できますが、_[!UICONTROL Action]_の列の&#x200B;**[!UICONTROL Select]**の下のオプションは個々のリストにのみアクションを適用します。

[ ステータス/タブによるリストの管理 ](./managing-listings-by-tab.md) も参照してください。

| アクション | 説明 | タブ |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 不完全な製品を照合プロセスを通じて戻すために使用されます。 再一致を試みるには、[ リスト ](./listing-settings.md) および [ カタログ検索 ](./catalog-search.md) 設定を変更して、自動一致の可能性を高める必要があります。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 照合するリストを選択するか、照合する ASIN を入力するか、欠落条件を割り当てることにより、カタログ製品をAmazonのリストに手動で照合します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | 個々の SKU/製品の変更を示すリストアクティビティログなど、アクティブな製品に関する追加情報を表示します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Amazon リストで読み込んだ情報を使用して、[!DNL Commerce] しいカタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 自動照合を試みます | 検索条件の設定に基づいて、[!DNL Commerce] カタログとAmazonのリストを自動一致させます。 再一致を試みるには、[ リスト ](./listing-settings.md) および [ カタログ検索 ](./catalog-search.md) 設定を変更して、自動一致の可能性を高める必要があります。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | [!DNL Commerce] カタログ内の既存の商品を手動で選択し、Amazon リストに割り当てます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Amazon リストで読み込んだ情報を使用して、[!DNL Commerce] しいカタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （一括処理）終了したリストの再リスト化や、リスト・ルールの実施要件を満たしているが、_[!UICONTROL Product Listing Actions]_が `Automatically list new products` に設定されていない製品の手動リスト化に使用します。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （単一リストアクション）終了したリストを再リストするために使用されます。 また、このアクションは、_[!UICONTROL Product Listing Actions]_が `Automatically list new products` に設定されていない場合に、リストルールの実施要件を満たす製品を手動でリストする場合にも使用されます。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （一括処理）Amazon上に存在する商品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、再リストに登録できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （一括処理）個々のリストの価格、処理時間、条件および販売者のメモテキストを設定する既存の「上書き」を手動で編集し、他のリストのデフォルト、設定およびルールを無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 個々のリストの価格、処理時間、条件、販売者のメモテキストを設定する「上書き」を手動で作成し、他のリストのデフォルト、設定、ルールを無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | カタログ製品と一致する ASIN を変更する必要がある場合に使用します（例：製品が誤ったリスト ASIN と一致した場合）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 2 つの機能を提供できます。<br><br> カタログ商品と 2 つのAmazon リストの間に 1 対 2 の関係を作成するために使用できます。 例：Amazonに、異なる ASIN 値を持つ商品がリストされる。 1 つのカタログ製品を、製品の両方の ASIN リストに一致させることができます。<br><br> 様々なAmazon リージョンでのリストを制御するために使用できます。 例：Amazon地域（米国リージョンが FBA、カナダ リージョンが FBM）に基づいて異なる配送方法が定義されたカタログ商品があるとします。 在庫/数量を管理するには、エイリアスの販売者 SKU を作成し、その地域の同じ製品を別の販売者 SKU に再リストします。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 商品に関連するフルフィルメント方法を変更するために使用されます（フルフィルメントがAmazon: FBA またはマーチャント：FBM によって実行）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （単一のリストアクション）Amazonに存在する商品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、再リストに登録できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （単一リストのアクション）個々のリストの価格、処理時間、条件、販売者のメモテキストを設定する既存の「上書き」を手動で編集し、他のリストのデフォルト、設定、ルールを無視します。 | [[!UICONTROL Overrides]](./overrides.md) |

## 製品リストへのアクセス

1. _管理者_ サイドバーで、**マーケティング**/_チャネル_/**AmazonSales Channel** に移動します。

1. ストアカードの **ストアを表示** をクリックします。

1. ストアダッシュボードで、「**ストアの一覧** セクションの _一覧の管理_ をクリックします。
