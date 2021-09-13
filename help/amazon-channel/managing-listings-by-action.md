---
title: アクション別の製品リストの管理
description: Amazonのリストを管理する際に、個々のリストまたは複数のリストにアクションを適用できます。
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# アクション別の製品リストの管理

_[!UICONTROL Product Listings]_ページには、すべてのリストのステータスを表示し、製品をAmazonのリストに一致させるタブがいくつか含まれています。

各タブで使用できるリストタスクは少し異なりますが、[ワークスペースコントロール](./workspace-controls.md)は同じで、リストに表示するデータをカスタマイズできます。

**[!UICONTROL Actions]**&#x200B;の下のオプションは複数のリストにアクションを適用でき、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下のオプションは個々のリストにのみアクションを適用できます。

[ステータス別にリストを管理/タブ](./managing-listings-by-tab.md)も参照してください。

| アクション | 説明 | タブ |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | 不完全な製品を一致プロセスに戻すために使用します。 再一致を試みるには、[リスト](./listing-settings.md)と[カタログ検索](./catalog-search.md)の設定を変更して、自動一致の可能性を高める必要があります。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 一致するリストを選択するか、一致するASINを入力するか、見つからない条件を割り当てることで、カタログ商品をAmazonのリストに手動で照合します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | アクティブな製品に関する追加情報を表示します（「アクティビティログを表示」など）。このログには、個々のSKU /製品に対する変更が表示されます。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Amazonリストで読み込んだ情報を使用して、[!DNL Commerce]カタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 自動一致の試行 | 検索条件の設定に基づいて、[!DNL Commerce]カタログとAmazonの一覧の自動一致を試みます。 再一致を試みるには、[リスト](./listing-settings.md)と[カタログ検索](./catalog-search.md)の設定を変更して、自動一致の可能性を高める必要があります。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | [!DNL Commerce]カタログ内の既存の製品を手動で選択し、Amazonリストに割り当てます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Amazonリストで読み込んだ情報を使用して、[!DNL Commerce]カタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | （一括操作）終了したリストを再リストするか、リストルールの実施要件を満たす製品を手動でリストするために使用しますが、_[!UICONTROL Product Listing Actions]_は`Automatically list new products`に設定されません。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | （単一のリストアクション）終了したリストを再リストするために使用します。 このアクションは、_[!UICONTROL Product Listing Actions]_が`Automatically list new products`に設定されていない場合に、リストルールの実施要件を満たす製品を手動でリストする場合にも使用します。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | （一括操作）Amazonに存在する製品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、リリストできます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | （一括操作）個々のリストに対する価格、処理時間、条件、販売者のメモのテキストを設定し、他のリストのデフォルト、設定、ルールを無視する既存の「上書き」を手動で編集します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 個々のリストに対する価格、処理時間、条件、販売者のメモのテキストを設定する「上書き」を手動で作成し、他のリストのデフォルト、設定、ルールを無視します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | カタログ製品と一致するASINを変更する必要がある場合に使用します(例：（製品が正しくないASINリストに一致した場合）。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | 2つの機能を提供できます。<br><br>カタログ製品と2つのAmazonリストの間に1対2の関係を作成するために使用できます。 例：Amazonには、異なるASIN値を持つ製品がリストされています。 1つのカタログ製品を、両方のASINリストに一致させることができます。<br><br>様々なAmazon地域のリストを制御するために使用できます。例：Amazon地域に基づいて異なる出荷方法が定義されたカタログ製品がある（米国地域はFBA、カナダ地域はFBM）。 在庫/数量を制御するには、エイリアス販売者SKUを作成し、その地域の同じ製品を別の販売者SKUに再リストします。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 製品に関連付けられた履行方法(Amazonで履行)の変更に使用：FBA又は商人が履行するものFBM)。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | （単一のリストアクション）Amazonに存在する製品のリストを手動で終了および削除するために使用します。 終了したリストは、リストルールの実施要件を満たしている限り、リリストできます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | （単一のリストアクション）個々のリストに対する価格、処理時間、条件、販売者のメモのテキストを設定し、他のリストのデフォルト、設定、ルールを無視する既存の「上書き」を手動で編集します。 | [[!UICONTROL Overrides]](./overrides.md) |

## 製品リストへのアクセス

1. _管理_&#x200B;サイドバーで、**マーケティング** / _チャネル_ / **AmazonSales Channel**&#x200B;に移動します。

1. ストアカードの「**View Store**」をクリックします。

1. ストアダッシュボードで、「_ストアリスト_」セクションの「**リストの管理**」をクリックします。
