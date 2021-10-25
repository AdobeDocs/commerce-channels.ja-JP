---
title: '「オンボード」: 「リストルールの作成」'
description: Amazon 販売チャンネルの開始時に、製品の Amazon リストを生成するための初期一覧表示ルールを作成し  [!DNL Commerce]  ます。
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# オンボード: リスティングルールの作成

リスティングルールは、オンボードの間に定義することもできますが、いつでも変更することができます。 オンにすると、ストアのダッシュボードの一覧表示ルールにアクセスでき [ ](./listing-rules.md) [ ](./amazon-store-dashboard.md) ます。

## オンボードでのリストルールの作成

1. ストアに接続した後、 **[!UICONTROL View Store]** 追加したストアをクリックします。

   [ ](./amazon-store-dashboard.md) メッセージと共にストアのダッシュボードが表示され `No products listed to Amazon` ます。

1. をクリックし **[!UICONTROL Preview and List Eligible Products]** ます。

   _[!UICONTROL Listing Rules]_ページが表示されます。

1. Amazon に一覧表示される製品の適格性に必要な条件を定義し、をクリックし **[!UICONTROL Preview changes]** ます。または、ここをクリックして、 **[!UICONTROL Preview changes]** この手順を省略します。

   [次の例を参照してください。条件を定義 ](./ob-define-condition-example.md) します。

1. リストのプレビューで次の項目を確認します。

   ![リストプレビュー](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** -このタブに一覧表示されている製品は、現在のリストルール設定に基づいて、Amazon リストの対象となりません。

      非不適合製品は、Amazon に公開されません。 対象外の製品が Amazon に既に一覧表示されている場合、Amazon の一覧をカタログ製品と一致させると、 [!DNL Commerce] amazon の一覧の表示が製品販売を防止するために変更され `0` ます。 Amazon からリストを手動で削除するには、「Amazon リスティングの終了」を参照してください [ ](./end-listings-manually.md) 。 Amazon の要件を満たしていない製品は、ここには表示されません。 それらの製品はタブに表示され [[!UICONTROL Inactive Listings] ](./inactive-listings.md) ます。

      一覧をリストに変更するには `Ineligible` `Eligible` 、この手順を繰り返してリストのルールを変更します。

   - **[!UICONTROL Eligible Listings]** -このタブに一覧表示されている製品は、現在のリスティングルール設定に基づいて Amazon の一覧を表示できます。また、Amazon の要件を満たしている必要があります。 このタブには、既に読み込まれている Amazon リストが表示されます (リスティング設定が設定されている場合 **[!UICONTROL Import Third Party Listings]** `Import Listing` [ ](./listing-settings.md) )。

   - **[!UICONTROL New Listings]** -このタブに一覧表示されている製品には、 [!DNL Commerce] 現在のリスティングルールの設定に基づいて、amazon リストを作成し、amazon リストを作成するために、新しいカタログ製品が追加されています。

1. 完了したら、をクリックし **[!UICONTROL Save and Close]** ます。

   ストアの [ ダッシュボード ](./amazon-store-dashboard.md) が表示されます。

1つのストアが完了すると、その後、Amazon の間に情報の同期が [!DNL Commerce] 開始されます。 Amazon リストがカタログ内の製品にインポートされ、 [!DNL Commerce] 一致し [!DNL Commerce] ます。

作成された Amazon の注文情報は、 _[!UICONTROL Recent Orders]_ストアダッシュボードのセクションに表示されます。 [ストアダッシュボード ](./amazon-store-dashboard.md) または [ 注文 ](./managing-orders.md) の管理を参照してください。

>[!IMPORTANT]
>
>ストアには、新しいストアにデフォルト値を持つ重要なストア設定 (一覧、価格、ルール、フルフィルメントなど) がいくつかあります。 ストアが特定のニーズに合わせて設定されていることを確認するには、ストア設定を参照してください [ ](./default-store-settings.md) 。

![次 ](assets/btn-next.png) [**のアイコンデフォルトのストア設定に進みます。**](./default-store-settings.md)
