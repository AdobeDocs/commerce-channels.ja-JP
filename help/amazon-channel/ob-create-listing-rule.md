---
title: Amazonのリストルールの作成
description: Amazon セールスチャネルのオンボーディングプロセスを完了する際に、商品のAmazon リストを生成するための最初のリストルール  [!DNL Commerce]  作成します。
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Amazonのリストルールの作成

リストルールはオンボーディング時に定義できますが、いつでも変更できます。 オンボーディング後、ストア [ ダッシュボード ](./listing-rules.md) で [ リストルール ](./amazon-store-dashboard.md) にアクセスできます。

## オンボーディング中のリストルールの作成

1. ストアが接続されたら、追加したストアの「**[!UICONTROL View Store]**」をクリックします。

   ストア [ ダッシュボード ](./amazon-store-dashboard.md) が表示され、`No products listed to Amazon` のメッセージが示されます。

1. 「**[!UICONTROL Preview and List Eligible Products]**」をクリックします。

   _[!UICONTROL Listing Rules]_ページが表示されます。

1. Amazonに一覧表示される商品の実施要件に必要な条件を指定して「**[!UICONTROL Preview changes]**」をクリックするか、「**[!UICONTROL Preview changes]**」をクリックしてこの手順をスキップします。

   [ 例：条件を定義 ](./ob-define-condition-example.md) を参照してください。

1. リストのプレビューでリストを確認します。

   ![ プレビューを一覧表示 ](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** – このタブにリストされた製品は、現在のリストルール設定に基づいてAmazonに一覧表示することはできません。

     不適格な製品はAmazonに公開されません。 不適格な商品が既にAmazonにリストされていて、Amazonのリストを [!DNL Commerce] カタログの商品と一致させる場合は、商品の売り上げを防ぐために、Amazonのリストの数量が `0` に変わります。 リストをAmazonから手動で削除するには、[Amazon リストの終了 ](./end-listings-manually.md) を参照してください。 Amazonの要件の対象とならない商品は、ここに表示されていません。 これらの製品は「[[!UICONTROL Inactive Listings]」タブに表示され ](./inactive-listings.md) す。

     `Ineligible` リストを `Eligible` リストに変更するには、このプロセスを繰り返し、リストルールを変更します。

   - **[!UICONTROL Eligible Listings]** – このタブにリストされる製品は、現在のリストルールの設定に基づいてAmazonに適格であり、Amazonの要件で適格になります。 このタブには、読み込まれた既存のAmazonのリストが含まれます（[ リスト設定 ](./listing-settings.md) で `Import Listing` に設定して **[!UICONTROL Import Third Party Listings]** る場合）。

   - **[!UICONTROL New Listings]** – このタブにリストされる製品には、現在のリストルールの設定に基づいて新しくAmazon Amazon リストに登録できる [!DNL Commerce] カタログ製品が含まれます。

1. 完了したら、「**[!UICONTROL Save and Close]**」をクリックします。

   ストア [ ダッシュボード ](./amazon-store-dashboard.md) が開きます。

ストアのオンボーディングが完了すると、[!DNL Commerce] とAmazonの間の情報同期が開始されます。 Amazonのリストは [!DNL Commerce] に読み込まれ、[!DNL Commerce] カタログ内の商品と照合されます。

Amazonの注文情報は、ストアダッシュボードの「_[!UICONTROL Recent Orders]_」セクションに表示されます。 [ ストアダッシュボード ](./amazon-store-dashboard.md) または [ 注文の管理 ](./managing-orders.md) を参照してください。

>[!IMPORTANT]
>
>重要なストア設定（リスト、価格、ルール、フルフィルメントなど）には、新しいストアのデフォルト値があります。 ストアが特定のニーズに合わせて設定されていることを確認するには、[ ストアの設定 ](./default-store-settings.md) を確認してください。

![ 次へアイコン ](assets/btn-next.png)[**デフォルトのストア設定を続行**](./default-store-settings.md)
