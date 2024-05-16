---
title: Amazon sales channel – 製品リストアクション
description: 製品リストのアクション設定を使用して、Commerce カタログとAmazonとのやり取りを定義します。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 製品リストのアクション

製品リストのアクション設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、カタログとAmazonとのやり取りを定義します。 これらの設定：

- 次の条件を満たしているか [!DNL Commerce] Amazonの実施要件を満たすカタログ製品は、に自動的に送信されます [!DNL Amazon Seller Central] リストを作成するアカウント。

- 注文のデフォルトの処理時間を設定します。 この値は、注文の処理と発送に必要な日数を定義します。 例えば、誰かが 2 日間の配送を選択した場合、その配送時間は、処理が完了して荷物が運送業者に引き渡されるまで開始されません。 合計配信時間は（処理時間+輸送時間+任意の休日）です。

## 設定

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 _[!UICONTROL Product Listing Actions]_セクション。

1. の場合 **[!UICONTROL Automatic List Action]** （必須）、次のいずれかのオプションを選択します。

   - `Automatically List Eligible Products` - （デフォルト）使用するタイミングを選択します [!DNL Commerce] （Amazonの実施要件を満たす）カタログ製品をAmazonに自動公開し、Amazon リストを作成する。

   - `Do Not Automatically List Eligible Products`  – 実施要件を手動で選択するタイミングを選択します [!DNL Commerce] 製品カタログの作成とAmazon一覧の作成。 選択すると、リスト条件を満たし、必要な情報をすべて含んだカタログ製品が [_[!UICONTROL Ready to List]_](./ready-to-list.md) タブをクリックして、Amazonに手動で公開します。

1. の場合 **[!UICONTROL Default Handling Time]** （必須）出荷前のリード・タイムに必要な日数を入力します。

   デフォルト値はです `2` 日間。

   >[!NOTE]
   >
   >このデフォルトの処理時間の値は、Amazon sales channel を通じて作成されたAmazon リストに対してのみ有効です。 で作成されたAmazonの一覧 [!DNL Amazon Seller Central] アカウントでは、Amazonで設定されたデフォルトの処理時間を使用します。

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![製品リストのアクション](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | オプション：<ul><li>**[!UICONTROL Automatically List Eligible Products]** - （推奨）使用するタイミングを選択 [!DNL Commerce] （Amazonの実施要件を満たす）カタログ製品をAmazonに自動公開し、Amazon リストを作成する。 選択した場合、 [_[!UICONTROL Ready to List]_](./ready-to-list.md) タブは表示されません。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**  – 実施要件を手動で選択するタイミングを選択 [!DNL Commerce] 製品カタログの作成とAmazon一覧の作成。 選択すると、リスト条件を満たし、必要な情報をすべて含んだカタログ製品が [_[!UICONTROL Ready to List]_](./ready-to-list.md) タブをクリックして手動で公開します。</li></ul> |
| [!UICONTROL Default Handling Time] | 一般的に、注文の処理と発送に要する日数を表す数値。 デフォルト値はです `2`. この値は、で作成されたAmazonのリストに使用されます [!DNL Commerce] Amazonに公開されます。 をに統合する前のAmazon リストのデフォルトの処理時間 [!DNL Commerce] この設定の影響を受けません。<br><br>AmazonのAmazonで定義された値は、既存の Sales Channel のリストで定義されたデフォルトの処理時間を置き換えるものではありません。 条件 **[!UICONTROL Handling Time Override]** を有効にしてから削除すると、注文の処理時間が、ここで定義した値に戻ります。<br><br>処理時間が異なる製品がある場合、製品固有のレベルで処理時間の上書きを作成できます。 での時間の上書きの処理を管理できます。 [_[!UICONTROL Overrides]_](./overrides.md) タブを使用すると、製品のフルフィルメントを柔軟に管理できます。 で処理時間の上書きがない場合、 [!DNL Commerce] 商品の場合、処理時間のデフォルトは、Amazon リストで定義された値です。<br><br>処理時間は、地域の属性です。 リストの値が変更されると、その変更は以下を共有するすべてのリストに影響します。 [!DNL Amazon Seller SKU] 同じリージョンに存在するすべてのAmazon ストア （で定義） [ストアの統合](./store-integration.md)）に設定します。 ただし、共有の値は変更できません [!DNL Amazon Seller SKU] の北米地域では、別の定義済み地域の店舗にリストされている同じ製品には影響しません。 作成日が最も古いリージョンのストアが、[ 既定の処理時間 ] 設定の優先度を制御します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
