---
title: Amazonセールスチャネル — 製品リストアクション
description: 「製品リストアクション」設定を使用して、コマースカタログとAmazonとのやり取りを定義します。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 製品リストアクション

「製品リストアクション」設定は、ストアリスト設定の一部です。 リスト設定には、 [ストアダッシュボード](./amazon-store-dashboard.md).

これらの設定は、カタログとAmazonとのやり取りを定義します。 以下の設定を行います。

- 次の項目を指定します。 [!DNL Commerce] Amazonの適格要件を満たすカタログ製品は、 [!DNL Amazon Seller Central] アカウントを使用してリストを作成します。

- オーダーのデフォルトの処理時間を設定します。 この値は、注文の処理と出荷に必要な日数を定義します。 例えば、誰かが 2 日間の送料を選択した場合、その送料の送料は処理が完了し、パッケージが運送業者に引き渡されるまで開始されません。 合計配信時間は（処理時間+通過時間+休日）です。

## 設定を構成

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL Product Listing Actions]_」セクションに入力します。

1. の場合 **[!UICONTROL Automatic List Action]** （必須）、次のオプションを選択します。

   - `Automatically List Eligible Products` - （デフォルト） [!DNL Commerce] Amazonに自動的に公開してAmazonリストを作成するための (Amazonの適格要件を満たす ) カタログ製品。

   - `Do Not Automatically List Eligible Products`  — 適格なを手動で選択するタイミングを選択します [!DNL Commerce] 商品をカタログ化し、Amazonリストを作成します。 選択すると、リストの条件を満たし、必要な情報をすべて含むカタログ製品が [_[!UICONTROL Ready to List]_](./ready-to-list.md) 「 」タブを使用して、Amazonに手動で公開できます。

1. の場合 **[!UICONTROL Default Handling Time]** （必須）出荷前のリード・タイムに必要な日数を入力します。

   デフォルト値は `2` 日。

   >[!NOTE]
   >
   >このデフォルトの処理時間の値は、Amazonセールスチャネルを通じて作成されたAmazonリストに対してのみ有効です。 お使いの [!DNL Amazon Seller Central] アカウントは、Amazonで設定されたデフォルトの処理時間を使用します。

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![製品リストアクション](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Automatic List Action] | オプション：<ul><li>**[!UICONTROL Automatically List Eligible Products]** - （推奨）いつ、 [!DNL Commerce] Amazonに自動的に公開してAmazonリストを作成するための (Amazonの適格要件を満たす ) カタログ製品。 選択すると、 [_[!UICONTROL Ready to List]_](./ready-to-list.md) 」タブは表示されません。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**  — 実施要件を手動で選択する場合に選択します [!DNL Commerce] 商品をカタログ化し、Amazon Listings を作成します。 選択すると、リストの条件を満たし、必要な情報をすべて含むカタログ製品が [_[!UICONTROL Ready to List]_](./ready-to-list.md) タブを使用して手動で公開できます。</li></ul> |
| [!UICONTROL Default Handling Time] | 注文の処理と出荷に要する一般的な日数を表す数値です。 デフォルト値は `2`. この値は、で作成されたAmazonリストに使用されます。 [!DNL Commerce] Amazonに公開されました。 との統合前のAmazonリストのデフォルトの処理時間 [!DNL Commerce] はこの設定の影響を受けません。<br><br>Amazonセールスチャネルで定義された値は、既存のAmazonリストで定義されたデフォルトの処理時間を置き換えません。 When a **[!UICONTROL Handling Time Override]** が有効になって削除されると、注文の「処理時間」がここで定義した値に戻ります。<br><br>処理時間の異なる製品がある場合は、製品固有のレベルで処理時間上書きを作成できます。 処理時間の上書きは、 [_[!UICONTROL Overrides]_](./overrides.md) タブを使用して、製品の達成を柔軟に管理できます。 で処理時間の上書きがない場合は、次のようにします。 [!DNL Commerce] 製品の場合、処理時間のデフォルトは、Amazonリストで定義された値です。<br><br>[ 処理時間 ] は地域の属性です。 リストの値を変更すると、この変更は、 [!DNL Amazon Seller SKU] は、同じ地域に存在するすべてのAmazonストア（で定義） [ストア統合](./store-integration.md)) をクリックします。 ただし、共有の値を変更する [!DNL Amazon Seller SKU] 北米地域では、異なる定義済みの地域を持つストアにリストされている同じ製品には影響しません。 作成日が最も古い地域のストアが、「デフォルトの処理時間」設定の優先度を制御します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
