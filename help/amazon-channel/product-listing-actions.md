---
title: 製品リストのアクション
description: 「製品リストアクション」設定を使用して、Commerce カタログが Amazon とどのように作用するかを定義します。
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 製品リストのアクション

製品一覧のアクションの設定は、ストア一覧の設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

この設定によって、Amazon に対するカタログのやり取りが定義されます。 これらの設定:

- [!DNL Commerce]Amazon の必要条件を満たすカタログ製品が、リストを作成するために自動的にお客様のアカウントに送信されるかどうかを指定 [!DNL Amazon Seller Central] します。

- 注文のデフォルトの処理時間を設定します。 この値は、注文を処理および出荷するために必要な日数を定義します。 例えば、配達員が2日配達を選択した場合、送料は、処理が完了するまで開始されず、パッケージがキャリアに渡されます。 配送時間の合計は、処理時間 + 輸送時間 + 祝日) です。

## 設定の構成

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL Product Listing Actions]_ます。

1. **[!UICONTROL Automatic List Action]**(必須) には、次のいずれかのオプションを選択します。

   - `Automatically List Eligible Products` (デフォルト) 必要に応じて、 [!DNL Commerce] amazon の特典条件に適合するカタログ製品を自動的に amazon に公開して、Amazon リストを作成するかどうかを選択します。

   - `Do Not Automatically List Eligible Products` -適格なカタログ製品を手動で選択し、Amazon リストを作成する場合に選択し [!DNL Commerce] ます。 選択すると、 [_[!UICONTROL Ready to List]_](./ready-to-list.md) Amazon に対する手動のパブリッシュ用に、登録条件に適合し、すべての必要な情報を含むカタログ製品がタブに表示されます。

1. **[!UICONTROL Default Handling Time]**(必須) には、出荷前のリードタイムに必要な日数を入力します。

   デフォルト値は「 `2` 日」です。

   >[!NOTE]
   >
   >このデフォルトの経過時間の値は、Amazon sales channel 経由で作成された Amazon リストについてのみ有効です。 ユーザーのアカウントで作成された Amazon リストに [!DNL Amazon Seller Central] は、amazon に設定されたデフォルトの処理時間が使用されます。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![製品リストのアクション](assets/amazon-product-listing-actions.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Automatic List Action] | オプション：<ul><li>**[!UICONTROL Automatically List Eligible Products]** -(推奨) amazon [!DNL Commerce] に対する特典条件を満たしているカタログ製品を自動的に amazon に公開し、Amazon リストを作成する場合に選択します。 選択すると、 [_[!UICONTROL Ready to List]_](./ready-to-list.md) タブは表示されません。 </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** -対象となるカタログ製品を手動で選択し、Amazon リストを作成する場合に選択し [!DNL Commerce] ます。 この項目を選択すると、カタログ製品が登録条件に適合して、必要なすべての情報がタブに表示され、 [_[!UICONTROL Ready to List]_](./ready-to-list.md) 手動によるパブリッシュを行うことができます。</li></ul> |
| [!UICONTROL Default Handling Time] | 通常は、注文の処理と出荷にかかる時間を表す数値です (通常は、これを行うことができません)。 デフォルト値は `2` です。 この値は、によって作成され、Amazon に公開された Amazon リストに使用され [!DNL Commerce] ます。 統合前の Amazon リストのデフォルト処理時間 [!DNL Commerce] は、この設定には反映されません。<br><br>Amazon sales チャンネルで定義されている値は、既存の Amazon リスティングに定義されているデフォルトの処理時間を置き換えません。 **[!UICONTROL Handling Time Override]**&#x200B;が有効になり、削除されると、ここで定義された値に注文の処理時間が戻ります。<br><br>取扱時間が異なる製品を使用している場合は、取扱時間の上書きを製品固有のレベルで作成することができます。 タブで処理時間の上書きを管理し [_[!UICONTROL Overrides]_](./overrides.md) て、製品のフルフィルメントを管理するための柔軟な機能を提供できます。 製品に対する処理時間の上書きが含まれていない場合、 [!DNL Commerce] 処理時間のデフォルトは、Amazon リストに定義されている値になります。<br><br>取扱時間は地域別属性です。 一覧の値が変更されると、その変更は、 [!DNL Amazon Seller SKU] ストア統合で定義されている同じ地域に存在するすべての Amazon stores ストアでが共有されているすべての一覧に反映され [ ](./store-integration.md) ます。 ただし、北米地域の共有の値を変更しても、ストアとは [!DNL Amazon Seller SKU] 別に定義された地域と同じ製品には影響しません。 作成日付が最も古い領域のストアによって、デフォルトの手数料設定の優先順位が制御されます。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
