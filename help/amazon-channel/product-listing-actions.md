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

製品リストのアクション設定は、ストアリスト設定の一部です。 リスト設定は、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスします。

これらの設定は、カタログとAmazonとのやり取りを定義します。 これらの設定：

- Amazonの実施要件を満たす [!DNL Commerce] カタログ商品が、リストを作成するために [!DNL Amazon Seller Central] アカウントに自動的に送信されるかどうかを指定します。

- 注文のデフォルトの処理時間を設定します。 この値は、注文の処理と発送に必要な日数を定義します。 例えば、誰かが 2 日間の配送を選択した場合、その配送時間は、処理が完了して荷物が運送業者に引き渡されるまで開始されません。 合計配信時間は（処理時間+輸送時間+任意の休日）です。

## 設定

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL Product Listing Actions]_」セクションを展開します。

1. **[!UICONTROL Automatic List Action]** （必須）には、次のいずれかのオプションを選択します。

   - `Automatically List Eligible Products` - （デフォルト） [!DNL Commerce] カタログ商品（Amazonの実施要件を満たす）をAmazonに自動公開し、Amazon リストを作成するタイミングを選択します。

   - `Do Not Automatically List Eligible Products` – 実施要件を満たす [!DNL Commerce] カタログ商品を手動で選択し、Amazonのリストを作成するタイミングを選択します。 これを選択すると、リスト条件を満たし、必要な情報がすべて含まれているカタログ製品が、Amazonに手動で公開するために「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブに表示されます。

1. **[!UICONTROL Default Handling Time]** （必須）には、出荷前のリード・タイムに必要な日数を入力します。

   デフォルト値は `2` 日です。

   >[!NOTE]
   >
   >このデフォルトの処理時間の値は、Amazon sales channel を通じて作成されたAmazon リストに対してのみ有効です。 [!DNL Amazon Seller Central] アカウントで作成されたAmazonのリストでは、Amazonで設定されたデフォルトの処理時間が使用されます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![ 製品リストのアクション ](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | オプション：<ul><li>**[!UICONTROL Automatically List Eligible Products]** - （推奨） [!DNL Commerce] カタログ商品（Amazonの実施要件を満たす）をAmazonに自動公開し、Amazon リストを作成するタイミングを選択します。 これを選択すると、「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブは表示されなくなります。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** – 実施要件を満たす [!DNL Commerce] カタログ商品を手動で選択し、Amazon リストを作成するタイミングを選択します。 これを選択すると、リスト条件を満たし、必要な情報がすべて含まれているカタログ製品が、手動公開用の「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブに表示されます。</li></ul> |
| [!UICONTROL Default Handling Time] | 一般的に、注文の処理と発送に要する日数を表す数値。 デフォルト値は `2` です。 この値は、[!DNL Commerce] で作成され、Amazonに公開されるAmazonのリストに使用されます。 Amazonのリストを [!DNL Commerce] と統合するまでのデフォルトの処理時間は、この設定の影響を受けません。<br><br>AmazonのAmazonで定義された値は、既存の Sales Channel のリストで定義されたデフォルトの処理時間を置き換えるものではありません。 **[!UICONTROL Handling Time Override]** を有効にして削除すると、注文の処理時間が、ここで定義した値に戻ります。<br><br> 処理時間が異なる製品がある場合、製品固有のレベルで処理時間の上書きを作成できます。 「[_[!UICONTROL Overrides]_](./overrides.md)」タブで時間の上書きの処理を管理すると、商品の受け渡しを柔軟に管理できます。 商品の [!DNL Commerce] に処理時間の上書きがない場合、処理時間のデフォルトは、Amazon リストで定義された値です。<br><br> 時間の処理は地域の属性です。 リストの値が変更されると、同じリージョンに存在するすべてのAmazon ストアで [!DNL Amazon Seller SKU] を共有するすべてのリストに影響します（[ ストア統合 ](./store-integration.md) で定義）。 ただし、北米地域で共有 [!DNL Amazon Seller SKU] の値を変更しても、別の定義済み地域のストアにリストされている同じ製品には影響しません。 作成日が最も古いリージョンのストアが、[ 既定の処理時間 ] 設定の優先度を制御します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
