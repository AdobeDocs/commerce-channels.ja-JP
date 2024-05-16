---
title: Amazonのリストルールの作成
description: Amazon セールスチャネルのオンボーディングプロセスを完了する際に、Amazonのリストを生成するための最初のリストルールを作成します [!DNL Commerce] 製品。
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Amazonのリストルールの作成

リストルールはオンボーディング時に定義できますが、いつでも変更できます。 オンボーディング後、にアクセスできます [リストルール](./listing-rules.md) 店舗で [dashboard](./amazon-store-dashboard.md).

## オンボーディング中のリストルールの作成

1. ストアが接続されたら、 **[!UICONTROL View Store]** 追加したストアの場合。

   ストア [dashboard](./amazon-store-dashboard.md) が「」と共に表示されます `No products listed to Amazon` メッセージ。

1. クリック **[!UICONTROL Preview and List Eligible Products]**.

   この _[!UICONTROL Listing Rules]_ページが表示されます。

1. Amazonに一覧表示される商品の実施要件を指定し、をクリックします。 **[!UICONTROL Preview changes]**&#x200B;を選択するか、 **[!UICONTROL Preview changes]** この手順をスキップする場合は、をクリックします。

   参照： [例：条件の定義](./ob-define-condition-example.md).

1. リストのプレビューでリストを確認します。

   ![リストのプレビュー](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]**  – このタブにリストされている商品は、現在のリストルール設定に基づいてAmazonにリスト表示できません。

     不適格な製品はAmazonに公開されません。 不適格な製品がAmazonに既にリストされていて、Amazonのリストをのリストと一致させる場合 [!DNL Commerce] カタログ商品、Amazonリストの数量が「」に変わります `0` 商品の販売を防止する。 リストをAmazonから手動で削除するには、を参照してください。 [Amazon リストの終了](./end-listings-manually.md). Amazonの要件の対象とならない商品は、ここに表示されていません。 その製品は [[!UICONTROL Inactive Listings] タブ](./inactive-listings.md).

     を変更するには `Ineligible` へのリスト `Eligible` リスト化するには、このプロセスを繰り返して、リストルールを変更します。

   - **[!UICONTROL Eligible Listings]**  – このタブにリストされた製品は、現在のリストルールの設定に基づいてAmazonのリストへの登録が可能で、Amazonの要件で適格になります。 このタブには、読み込まれた既存のAmazonのリストが表示されます（次がある場合） **[!UICONTROL Import Third Party Listings]** をに設定 `Import Listing` が含まれる [リスト設定](./listing-settings.md)）に設定します。

   - **[!UICONTROL New Listings]**  – このタブに表示される製品には、 [!DNL Commerce] 現在のリストルールの設定に基づいて新しくAmazon リストの対象となるカタログ製品と、Amazon リストの作成。

1. 完了したら、 **[!UICONTROL Save and Close]**.

   ストア [dashboard](./amazon-store-dashboard.md) が開きます。

ストアのオンボーディングが完了すると、情報は次の間で同期されます [!DNL Commerce] Amazonが開始されます。 Amazonのリストは、に読み込まれます。 [!DNL Commerce] を検索し、の中の製品と照合します [!DNL Commerce] カタログ。

Amazonの注文情報は、 _[!UICONTROL Recent Orders]_ストアダッシュボードの「」セクション。 参照： [ストアダッシュボード](./amazon-store-dashboard.md) または [注文の管理](./managing-orders.md).

>[!IMPORTANT]
>
>重要なストア設定（リスト、価格、ルール、フルフィルメントなど）には、新しいストアのデフォルト値があります。 ストアが特定のニーズに合わせて設定されていることを確認するには、 [ストアの設定](./default-store-settings.md) .

![次へアイコン](assets/btn-next.png) [**デフォルトのストア設定を続行**](./default-store-settings.md)
