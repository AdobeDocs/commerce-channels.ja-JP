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

この _[!UICONTROL Product Listings]_ページには、すべての商品リストのステータスを確認したり、商品をAmazonのリストに一致させたりできるタブがいくつかあります。

使用可能なリストタスクはタブごとに少し異なりますが、 [workspace コントロール](./workspace-controls.md) 同じであり、リストに表示するデータをカスタマイズできます。

の下のオプション **[!UICONTROL Actions]** ではアクションを複数のリストに適用でき、ではオプションを適用できます。 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列は、個々のリストにのみアクションを適用します。

関連トピック [ステータス/タブ別リストの管理](./managing-listings-by-tab.md).

| アクション | 説明 | タブ |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 不完全な製品を照合プロセスを通じて戻すために使用されます。 再照合を行うには、 [Listing](./listing-settings.md) および [カタログ検索](./catalog-search.md) 自動マッチングの可能性を高めるための設定です。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 照合するリストを選択するか、照合する ASIN を入力するか、欠落条件を割り当てることにより、カタログ製品をAmazonのリストに手動で照合します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | 個々の SKU/製品の変更を示すリストアクティビティログなど、アクティブな製品に関する追加情報を表示します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | を作成 [!DNL Commerce] Amazon リストで読み込んだ情報を使用したカタログ製品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 自動照合を試みます | の間で自動照合を試みます [!DNL Commerce] 検索条件の設定に基づいたカタログおよびAmazonのリスト。 再照合を行うには、 [Listing](./listing-settings.md) および [カタログ検索](./catalog-search.md) 自動マッチングの可能性を高めるための設定です。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | で既存の製品を手動で選択する [!DNL Commerce] カタログを作成して、Amazon リストに割り当てます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | を作成 [!DNL Commerce] Amazon リストで読み込んだ情報を使用したカタログ製品。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （一括処理）終了したリストを再リスト表示したり、リスト・ルールの実施要件を満たす製品を手動でリスト表示するために使用しますが、 _[!UICONTROL Product Listing Actions]_はに設定されていません `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （単一リストアクション）終了したリストを再リストするために使用されます。 また、このアクションは、次の場合にリストルールの実施要件を満たす製品を手動でリストするためにも使用されます _[!UICONTROL Product Listing Actions]_はに設定されていません `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （一括処理）Amazon上に存在する商品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、再リストに登録できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （一括処理）個々のリストの価格、処理時間、条件および販売者のメモテキストを設定する既存の「上書き」を手動で編集し、他のリストのデフォルト、設定およびルールを無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 個々のリストの価格、処理時間、条件、販売者のメモテキストを設定する「上書き」を手動で作成し、他のリストのデフォルト、設定、ルールを無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | カタログ製品と一致する ASIN を変更する必要がある場合に使用します（例：製品が誤ったリスト ASIN と一致した場合）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 次の 2 つの関数を提供できます。<br><br>を使用すれば、カタログ商品と 2 つのAmazon リストとの間に 1 対 2 の関係を築くことができます。 例：Amazonに、異なる ASIN 値を持つ商品がリストされる。 1 つのカタログ製品を、製品の両方の ASIN リストに一致させることができます。<br><br>様々なAmazon リージョンでのリストの制御に使用できます。 例：Amazon地域（米国リージョンが FBA、カナダ リージョンが FBM）に基づいて異なる配送方法が定義されたカタログ商品があるとします。 在庫/数量を管理するには、エイリアスの販売者 SKU を作成し、その地域の同じ製品を別の販売者 SKU に再リストします。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 商品に関連するフルフィルメント方法を変更するために使用されます（フルフィルメントがAmazon: FBA またはマーチャント：FBM によって実行）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （単一のリストアクション）Amazonに存在する商品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、再リストに登録できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （単一リストのアクション）個々のリストの価格、処理時間、条件、販売者のメモテキストを設定する既存の「上書き」を手動で編集し、他のリストのデフォルト、設定、ルールを無視します。 | [[!UICONTROL Overrides]](./overrides.md) |

## 製品リストへのアクセス

1. 日 _Admin_ サイドバー、に移動 **Marketing** > _チャネル_ > **AmazonSales Channel**.

1. クリック **ストアを表示** ストアカードに。

1. ストアダッシュボードで、 **Manage Listings** が含まれる _ストアの一覧_ セクション。
