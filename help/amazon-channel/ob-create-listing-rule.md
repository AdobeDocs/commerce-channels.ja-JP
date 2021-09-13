---
title: '''オンボーディング：リストルールの作成`'
description: Amazonの販売チャネルのオンボーディングプロセスを完了する際に、 [!DNL Commerce] 製品のAmazonリストを生成するための最初のリストルールを作成します。
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# オンボーディング：リストルールの作成

リストルールはオンボーディング時に定義できますが、いつでも変更できます。 オンボーディング後、ストア[ダッシュボード](./amazon-store-dashboard.md)の[リストルール](./listing-rules.md)にアクセスできます。

## オンボーディング時のリストルールの作成

1. ストアに接続したら、追加したストアの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

   ストア[ダッシュボード](./amazon-store-dashboard.md)が`No products listed to Amazon`メッセージと共に表示されます。

1. **[!UICONTROL Preview and List Eligible Products]**&#x200B;をクリックします。

   _[!UICONTROL Listing Rules]_ページが表示されます。

1. Amazonに表示する製品の適格性に関する必要な条件を定義して「**[!UICONTROL Preview changes]**」をクリックするか、「**[!UICONTROL Preview changes]**」をクリックしてこの手順をスキップします。

   [例：条件](./ob-define-condition-example.md)を定義します。

1. リストプレビューでリストを確認します。

   ![リストのプレビュー](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]**  — このタブに表示される製品は、現在のリストルール設定に基づくAmazonリストには適用されません。

      不適格な製品は、Amazonに公開されません。 不適格な製品がAmazonに既にリストされ、Amazonリストが[!DNL Commerce]カタログ製品と一致する場合、Amazonリストの数量は`0`に変わり、製品の販売を防ぎます。 Amazonからリストを手動で削除するには、[Amazonリストの終了](./end-listings-manually.md)を参照してください。 Amazonの要件を満たさない製品は、ここに記載されていません。 これらの製品は[[!UICONTROL Inactive Listings]タブ](./inactive-listings.md)に一覧表示されます。

      `Ineligible`リストを`Eligible`リストに変更するには、この手順を繰り返し、リストルールを変更します。

   - **[!UICONTROL Eligible Listings]**  — このタブに表示される製品は、現在のリストルールの設定に基づいてAmazonリストに登録され、Amazonの要件に従います。このタブには、読み込まれた既存のAmazonリストが含まれます（[リスト設定](./listing-settings.md)で&#x200B;**[!UICONTROL Import Third Party Listings]**&#x200B;が`Import Listing`に設定されている場合）。

   - **[!UICONTROL New Listings]**  — このタブに一覧表示される商品に [!DNL Commerce] は、現在のリストルール設定に基づいて新しくAmazonリストに登録されるカタログ商品と、Amazonリストの作成が含まれます。

1. 完了したら、「**[!UICONTROL Save and Close]**」をクリックします。

   ストア[ダッシュボード](./amazon-store-dashboard.md)が開きます。

ストアのオンボーディングが完了すると、[!DNL Commerce]とAmazonの間の情報同期が開始されます。 Amazonのリストが[!DNL Commerce]に読み込まれ、[!DNL Commerce]カタログの製品との照合が試みられます。

Amazonの注文情報は、ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションで確認できます。 [Store Dashboard](./amazon-store-dashboard.md)または[Manage Orders](./managing-orders.md)を参照してください。

>[!IMPORTANT]
>
>新しいストアのデフォルト値を持つ重要なストア設定（リスト、価格、ルール、フルフィルメントなど）がいくつかあります。 ストアが特定のニーズに合わせて設定されていることを確認するには、 [ストア設定](./default-store-settings.md)を確認します。

![次のアイ](assets/btn-next.png) [**コン「デフォルトのストア設定に続行」**](./default-store-settings.md)
