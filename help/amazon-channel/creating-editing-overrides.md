---
title: Amazon販売チャネルの上書きを作成および編集します
description: AmazonのSales Channelの上書きを使用すると、1 つのAmazon リストまたは複数のリストに変更内容を適用できます。
feature: Sales Channels, Products, Configuration
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 0%

---

# 上書きの作成と編集

リストの作成と上書き、またはリストに適用した上書きを編集または削除できます。 オーバーライドは、特定のリストに定義済みの値を設定します。

## 単一リストの上書きの作成

この _[!UICONTROL Create Override]_の一覧を表示しているときにアクションを利用できます_[!UICONTROL Inactive]_, _[!UICONTROL Active]_、および_[!UICONTROL Ineligible]_ タブ。

1. でリストを表示する _[!UICONTROL Products Listings]_ページ （_[!UICONTROL Inactive]_, _[!UICONTROL Active]_、および_[!UICONTROL Ineligible]_ タブ）。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Create Override]**製品リストの上書きページを開きます。

   ![Amazon リストの上書きの作成](assets/amazon-select-create-override.png){width="220"}

1. 正しいリストを表示していることを確認するには、 _[!UICONTROL Listing Details]_.

1. 作成する上書きのタイプを決定します。

   リストに対して、単一の上書きタイプまたは任意のタイプの組み合わせ（価格、処理時間、条件、販売者メモ）を定義できます。

   - **価格** - クリック **[!UICONTROL Change Listing Price]** およびに定義した価格の値を入力します **[!UICONTROL Price Override]**.
   - **処理時間** - クリック **[!UICONTROL Change Handling Time]** に定義された時間値（日数）を入力します **[!UICONTROL Handling Time Override]**.
   - **条件** - クリック **[!UICONTROL Change Condition]** を選択し、適切な **[!UICONTROL Condition Override]**.
   - **販売者メモ** - クリック **[!UICONTROL Change Seller Notes]** 次のメモ テキストを入力してください： **[!UICONTROL Seller Notes Override]**.

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「」に変わります。 `Relist in Progress`. 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 このリストはにも追加されます。_[!UICONTROL Overrides]_ タブ。

次の例は、新しい価格を定義するオーバーライドを示しています `$55`：の新しい処理時間 `1 day`、の新しい条件 `Used; Like New`、および新しい販売者メモのテキスト。

![Amazon リストの上書きの例](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## 単一リストの上書きを編集または削除 {#edit-override-single-listing}

この _[!UICONTROL Edit Overrides]_の一覧を表示しているときにアクションを利用できます_[!UICONTROL Overrides]_ タブ。

1. でリストを表示する _[!UICONTROL Product Listings]_ページ （_[!UICONTROL Overrides]_ タブ）。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   この _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択](assets/amazon-select-edit-overrides.png){width="125"}

1. 正しいリストを上書きしていることを確認するには、 _[!UICONTROL Listing Details]_.

1. を編集するには _[!UICONTROL Override]_設定を変更し、変更するタイプ（価格、処理時間、条件、販売者メモ）のセクションを定義します。

   上書きタイプを同じにするには、次を選択します `No Change To <override type>` （デフォルト）。 この設定では、以前に定義したオーバーライド値は変更されません。

   - **価格** - クリック **[!UICONTROL Change Listing Price]** およびに定義した価格の値を入力します **[!UICONTROL Price Override]**.
   - **処理時間** - クリック **[!UICONTROL Change Handling Time]** に定義された時間値（日数）を入力します **[!UICONTROL Handling Time Override]**.
   - **条件** - クリック **[!UICONTROL Change Condition]** 正しいオプションを選択 **[!UICONTROL Condition Override]**.
   - **販売者メモ** - クリック **[!UICONTROL Change Seller Notes]** 次のメモ テキストを入力してください： **[!UICONTROL Seller Notes Override]**.

1. 上書きタイプを削除するには、をクリックします **削除** 削除するタイプごとに調整します。 削除しない場合、以前に定義した値はオーバーライドに残ります。

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「」に変わります。 `Relist in Progress`. 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 まだリストに表示されていない場合は、リストも_[!UICONTROL Overrides]_ タブ。

ピギーバッキング _上書きの作成_ 例えば、のようになります。 次の例は、以前に作成した上書きに対して、の新しい価格を定義する編集を示しています。 `$50`、処理時間の上書きを削除し、以前の条件および販売者メモの上書きを保持します。

![上書きの編集または削除](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## 複数の一覧の上書きを編集または削除します {#edit-override-multiple-listings}

この _[!UICONTROL Edit Listing Overrides]_アクションはで利用できます_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_、および _[!UICONTROL Ineligible]_タブ。

>[!NOTE]
>
>複数の一覧に対する優先設定を修正しているため、 _[!UICONTROL Listing Details]_単一のリストを変更する場合とは異なり、セクションは表示されません。

1. でリストを表示する _[!UICONTROL Products Listings]_ページ （_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_、および _[!UICONTROL Ineligible]_タブ）。

1. 変更する各一覧の左側の列にあるチェックボックスをオンにします。

1. 次の下 _[!UICONTROL Actions]_を選択し、**[!UICONTROL Edit Listing Overrides]**.

   この _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. を編集するには _[!UICONTROL Override]_設定を変更し、変更するタイプ（価格、処理時間、条件、販売者メモ）のセクションを定義します。

   上書きを同じにするには、次を選択します `No Change To <override type>` （デフォルト）。 この設定では、以前に定義したオーバーライド値は変更されません。

   - **価格** - クリック **[!UICONTROL Change Listing Price]** およびに定義した価格の値を入力します **[!UICONTROL Price Override]**.
   - **処理時間** - クリック **[!UICONTROL Change Handling Time]** に定義された時間値（日数）を入力します **[!UICONTROL Handling Time Override]**.
   - **条件** - クリック **[!UICONTROL Change Condition]** 正しいオプションを選択 **[!UICONTROL Condition Override]**.
   - **販売者メモ** - クリック **[!UICONTROL Change Seller Notes]** 次のメモ テキストを入力してください： **[!UICONTROL Seller Notes Override]**.

1. 上書きタイプを削除するには、をクリックします **[!UICONTROL Remove]** 削除するタイプごとに調整します。 削除しない場合、以前に定義した値はオーバーライドに残ります。

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「」に変わります。 `Relist in Progress`. 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 まだリストに表示されていない場合は、リストも_[!UICONTROL Overrides]_ タブ。

### タイプを上書き

| 上書き | 説明 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | 価格の上書きは、リストの価格を定義します。 このオーバーライドは、オーバーライドが削除されるまで、すべての自動設定よりも優先されます。<br><br>製品の価格を上書きするには、次を選択します **[!UICONTROL Change Listing Price]** に新しい価格を入力します **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | 処理時間の上書きでは、製品の処理および出荷に要する時間（日数）を定義します。 処理時間のオーバーライドは、オーバーライドが削除されるまで、自動化されたすべてのデフォルトの処理時間設定よりも優先されます。<br><br>に存在する値 _[!UICONTROL Handling Time Override]_ボックスは、で定義されたデフォルトの処理時間です [リスト設定](./listing-settings.md) または定義済みのオーバーライドの処理時間。 処理時間の上書きを削除すると、リストのデフォルトは、リスト設定で定義した処理時間になります。<br><br>処理時間の上書きを定義するには、を選択します&#x200B;**[!UICONTROL Change Handling Time]**に新しい処理時間（日数）を入力します&#x200B;**[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | リスト条件を上書きするには、を選択します **[!UICONTROL Change Condition]** から新しい条件を選択します。 **条件の上書き**. |
| [!UICONTROL Seller Notes Override] | 以外の条件で定義されたカタログ内の製品 `New`、販売者メモを追加して、製品とその状態を潜在的な購入者に詳しく説明できます。 に販売者注記の上書きを入力できます `New` 商品を条件付けするが、Amazonにメモが表示されない。<br><br>販売者メモを上書きするには、次を選択します **[!UICONTROL Change Seller Notes]** に新しいメモを入力します **[!UICONTROL Seller Notes Override]**. |
