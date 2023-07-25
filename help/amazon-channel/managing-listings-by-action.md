---
title: Amazonの製品リストをアクション別に管理
description: Amazonのリストを管理する際に、個々のリストまたは複数のリストにアクションを適用できます。
feature: Sales Channels, Products
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Amazonの製品リストをアクション別に管理

この _[!UICONTROL Product Listings]_ページにはいくつかのタブが含まれており、このタブで、すべてのリストのステータスを表示し、製品をAmazonのリストに一致させることができます。

使用可能なリストタスクはタブごとに少し異なりますが、 [workspace コントロール](./workspace-controls.md) は同じで、お使いのリストに表示するデータをカスタマイズできます。

以下のオプション **[!UICONTROL Actions]** は複数のリストにアクションを適用できますが、オプションは **[!UICONTROL Select]** 内 _[!UICONTROL Action]_「 」列は、個々のリストにのみアクションを適用します。

関連トピック [ステータス別リストを管理/タブ](./managing-listings-by-tab.md).

| アクション | 説明 | タブ |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 不完全な製品を一致プロセスを通じて戻すために使用します。 再一致を試みるには、 [リスト](./listing-settings.md) および [カタログ検索](./catalog-search.md) 自動一致の可能性を高める設定です。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 一致するリストを選択するか、一致する ASIN を入力するか、見つからない条件を割り当てることで、カタログ製品をAmazonリストに手動で照合します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | アクティビティログの一覧表示を含む、アクティブな製品に関する追加情報を表示します。このログには、個々の SKU /製品の変更が表示されます。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | の作成 [!DNL Commerce] Amazonリストで読み込まれた情報を使用したカタログ製品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 自動一致を試みる | 自動一致を試みます ( [!DNL Commerce] 検索条件の設定に基づくカタログとAmazonのリスト。 再一致を試みるには、 [リスト](./listing-settings.md) および [カタログ検索](./catalog-search.md) 自動一致の可能性を高める設定です。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | 既存の製品を [!DNL Commerce] カタログを作成し、Amazonリストに割り当てます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | の作成 [!DNL Commerce] Amazonリストで読み込まれた情報を使用したカタログ製品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （一括処理）終了したリストを再リストする場合、またはリストルールの適格要件を満たす製品を手動でリストする場合に、 _[!UICONTROL Product Listing Actions]_が次の値に設定されていません： `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （単一のリストアクション）終了したリストを再リストするために使用します。 また、このアクションは、次の場合に、リストルールの実施要件を満たす製品を手動でリストする場合にも使用します。 _[!UICONTROL Product Listing Actions]_が次の値に設定されていません： `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （一括操作）Amazonに存在する製品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、リリストできます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （一括操作）個々のリストに対する価格、処理時間、条件、販売者の注記テキストを設定する既存の「上書き」を手動で編集し、他のリストのデフォルト、設定、ルールは無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 個々のリストに対する価格、処理時間、条件、販売者の注記のテキストを設定する「上書き」を手動で作成し、他のリストのデフォルト、設定、ルールは無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | カタログ商品と一致する ASIN を変更する必要がある場合に使用します ( 例：( 製品が正しくないリスト (ASIN) と一致した場合 )。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 次の 2 つの機能を提供できます。<br><br>カタログ製品と 2 つのAmazonリストの間に 1 対 2 の関係を作成するために使用できます。 例：Amazonには、異なる ASIN 値を持つ製品がリストされています。 1 つのカタログ製品を、製品の両方の ASIN リストに一致させることができます。<br><br>様々なAmazon地域のリストを制御するために使用できます。 例：Amazon地域に基づいて異なる発送方法が定義されたカタログ製品があります（米国地域は FBA、カナダ地域は FBM）。 在庫/数量を制御するには、エイリアスの販売者 SKU を作成し、その地域の同じ製品を別の販売者 SKU で再リストします。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 製品に関連付けられた達成方法 (Amazonで満たす ) の変更に使用：FBA または商人が満たすもの：FBM) を参照してください。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （単一のリストアクション）Amazonに存在する製品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、リリストできます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （単一リストアクション）個々のリストに対する価格、処理時間、条件、販売者のメモのテキストを設定し、他のリストのデフォルト、設定、ルールを無視する既存の「上書き」を手動で編集します。 | [[!UICONTROL Overrides]](./overrides.md) |

## 製品リストにアクセス

1. の _管理者_ サイドバー、移動 **マーケティング** > _チャネル_ > **AmazonSales Channel**.

1. クリック **ストアを表示** をストアカードに貼り付けます。

1. ストアダッシュボードで、 **リストの管理** 内 _ストア一覧_ 」セクションに入力します。
