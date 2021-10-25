---
title: アクションによる製品リストの管理
description: Amazon リストを管理する際に、1つまたは複数のリストにアクションを適用することができます。
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# アクションによる製品リストの管理

このページには、 _[!UICONTROL Product Listings]_すべての一覧の状態を表示し、製品を Amazon リストに適合するようにするためのタブがいくつか含まれています。

使用可能な一覧表示の内容はタブによって若干異なりますが、 [ ワークスペースコントロール ](./workspace-controls.md) は同じで、リストに表示するデータをカスタマイズすることができます。

「」のオプションは、 **[!UICONTROL Actions]** 複数のリストにアクションを適用することができますが、列の「オプション」で、その **[!UICONTROL Select]** _[!UICONTROL Action]_アクションは個別の一覧にのみ適用されます。

「 [ 状態/タブによる一覧の管理」も参照してください ](./managing-listings-by-tab.md) 。

| アクション | つい | タグ |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | これを使用して、一致していない製品の再検索を行います。 再び一致させるには、 [ リスティング ](./listing-settings.md) とカタログ検索の設定を変更して、 [ 自動一致を可能にする必要があり ](./catalog-search.md) ます。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | 検索条件に一致するリストを選択するか、一致するように追加するか、条件を満たしていない場合は、カタログ製品を Amazon リストとして手動で検索します。 | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | アクティブな製品についての追加情報を表示します。これには、個々の SKU/製品に対する変更が表示されます。 | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | [!DNL Commerce]Amazon リストに取り込んだ情報を使用して、カタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| 自動的に一致を試みる | [!DNL Commerce]検索条件の設定に基づいて、カタログと Amazon リストとの間で自動的に一致するようにします。再び一致させるには、 [ リスティング ](./listing-settings.md) とカタログ検索の設定を変更して、 [ 自動一致を可能にする必要があり ](./catalog-search.md) ます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | カタログ内の既存の製品を手動で選択して、 [!DNL Commerce] それを Amazon リストに割り当てます。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | [!DNL Commerce]Amazon リストに取り込んだ情報を使用して、カタログ製品を作成します。 | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (質量アクション)既に終了した出展をリストに追加したり、登録ルールの条件を満たす製品を手動で表示したりするために使用されますが、 _[!UICONTROL Product Listing Actions]_はに設定されていません `Automatically list new products` 。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (1 つの一覧の操作)終了したリストを再一覧表示するために使用されます。 このアクションを使用して、に設定されていない場合に、リスティングルールの条件を満たす製品を手動でリストすることもでき _[!UICONTROL Product Listing Actions]_`Automatically list new products` ます。 | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (質量アクション)Amazon に存在していた製品の一覧を手動で削除したり削除したりするために使用されます。 終了した番組一覧は、出展規則の条件を満たしていれば、再表示できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (質量アクション)個々の一覧について、価格、処理時間、条件、および販売単価を設定し、他のリストのデフォルト、設定、およびルールを無視して、既存の &quot;上書き&quot; を編集します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | 手動で作成した「上書き」を使用して、個々のリストについては価格、手数料、条件、および販売単価を設定します。これにより、他のリストのデフォルト、設定、ルールは無視されます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | カタログ製品に一致するアークサインを変更する必要がある場合に使用します (例: 製品が間違ったリスティングのアークと一致した場合)。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | では、 <br><br> カタログ製品と2つの Amazon リストとの間に一対多の関係を作成するために使用できる2つの機能が提供されています。 例: Amazon によって、この製品が異なるアーク値でリストされています。 1つのカタログ製品について、製品の両方の通しリストに一致させることができます。<br><br>では、様々な Amazon 地域の一覧を制御するために使用できます。 例: Amazon 地域に基づいて定義されている出荷方法が異なるカタログ製品がある場合 (米国地域では FBA、カナダは FBM)。 Stock/quantity を制御するには、エイリアス販売店 SKU を作成し、その地区 SKU とは異なる販売店 sku を使用して同じ製品をリストすることができます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | 使用している製品に関連付けられたフルフィルメント方法 (Amazon: FBA、またはマーチャント: FBM によって履行される方法) を変更します。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (1 つの一覧の操作)Amazon に存在していた製品の一覧を手動で削除したり削除したりするために使用されます。 終了した番組一覧は、出展規則の条件を満たしていれば、再表示できます。 | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (1 つの一覧の操作)個々の一覧について、価格、処理時間、条件、および販売単価を設定し、他のリストのデフォルト、設定、およびルールを無視して、既存の &quot;上書き&quot; を編集します。 | [[!UICONTROL Overrides]](./overrides.md) |

## 製品一覧へのアクセス

1. _管理_ サイドバーで、 **販促** > _チャンネル_ > **Amazon Sales Channel に移動** します。

1. 「 **** 店舗カードで表示」をクリックします。

1. Store のダッシュボードで、 **** ストアリストセクションにある「リストの管理」をクリックし __ ます。
