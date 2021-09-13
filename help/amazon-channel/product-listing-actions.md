---
title: 製品リストのアクション
description: 「製品リストアクション」設定を使用して、コマースカタログとAmazonとのやり取りを定義します。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 製品リストアクション

製品リストアクション設定は、ストアリスト設定の一部です。 リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

これらの設定は、カタログとAmazonとのやり取りを定義します。 以下の設定を行います。

- Amazonの資格要件を満たす[!DNL Commerce]カタログ製品を、自動的に[!DNL Amazon Seller Central]アカウントに送信してリストを作成するかどうかを指定します。

- オーダーのデフォルトの処理時間を設定します。 この値は、注文の処理と発送に必要な日数を定義します。 例えば、誰かが2日間の送料を選択した場合、その送料は処理が完了し、パッケージが運送業者に渡されるまで開始されません。 合計配信時間は（処理時間+送信時間+休日）です。

## 設定を行う

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL Product Listing Actions]_セクションを展開します。

1. **[!UICONTROL Automatic List Action]**（必須）には、次のオプションを選択します。

   - `Automatically List Eligible Products` - （デフォルト）(Amazonの実施要件を満たすカタログ製 [!DNL Commerce] 品)をAmazonに自動的に公開し、Amazonリストを作成する場合に選択します。

   - `Do Not Automatically List Eligible Products`  — 適格なカタログ製品を手動で選択し、Amazonのリ [!DNL Commerce] ストを作成する場合に選択します。選択すると、リスト条件を満たし、必要な情報をすべて含むカタログ製品が「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブに表示され、Amazonに手動で公開されます。

1. **[!UICONTROL Default Handling Time]**（必須）には、出荷前のリードタイムに必要な日数を入力します。

   デフォルト値は`2`日です。

   >[!NOTE]
   >
   >このデフォルトの処理時間値は、Amazonの販売チャネルを通じて作成されたAmazonリストに対してのみ有効です。 [!DNL Amazon Seller Central]アカウントで作成されたAmazonのリストは、Amazonで設定されたデフォルトの処理時間を使用します。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![製品リストアクション](assets/amazon-product-listing-actions.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Automatic List Action] | オプション：<ul><li>**[!UICONTROL Automatically List Eligible Products]** - （推奨）(Amazonの適格性要件を満たすカタログ製 [!DNL Commerce] 品)をAmazonに自動的に公開してAmazonリストを作成するタイミングを選択します。選択すると、「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブは表示されません。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]**  — 適格なカタログ製品を手動で選択し、Amazonリス [!DNL Commerce] トを作成する場合に選択します。選択すると、リスト条件を満たし、必要な情報をすべて含むカタログ製品が、手動で公開するための「[_[!UICONTROL Ready to List]_](./ready-to-list.md)」タブに表示されます。</li></ul> |
| [!UICONTROL Default Handling Time] | 注文の処理と出荷に要する一般的な日数を表す数値。 デフォルト値は`2`です。 この値は、[!DNL Commerce]で作成され、Amazonに公開されるAmazonリストに使用されます。 [!DNL Commerce]と統合する前のAmazonリストのデフォルトの処理時間は、この設定の影響を受けません。<br><br>Amazon販売チャネルで定義された値は、既存のAmazonリストに定義されているデフォルトの処理時間を置き換えません。**[!UICONTROL Handling Time Override]**&#x200B;を有効にしてから削除すると、注文の処理時間はここで定義した値に戻ります。<br><br>処理時間が異なる製品がある場合は、製品固有のレベルで処理時間の上書きを作成できます。処理時間の上書きは「[_[!UICONTROL Overrides]_](./overrides.md)」タブで管理でき、柔軟に製品の受け渡しを管理できます。 製品の[!DNL Commerce]に処理時間の上書きがない場合、処理時間のデフォルト値はAmazonリストで定義された値になります。<br><br>「処理時間」は地域属性です。リストの値を変更すると、変更は、同じ地域に存在するすべてのAmazonストア内の[!DNL Amazon Seller SKU]を共有するすべてのリスト（[store integration](./store-integration.md)で定義）に影響します。 ただし、北米地域の共有[!DNL Amazon Seller SKU]の値を変更しても、定義された地域が異なる店舗にリストされている同じ製品には影響しません。 作成日が最も古い地域のストアが、「デフォルトの処理時間」設定の優先順位を制御します。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
