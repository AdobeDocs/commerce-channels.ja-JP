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

_[!UICONTROL Create Override]_アクションは、「_[!UICONTROL Inactive]_」、「_[!UICONTROL Active]_」、「_[!UICONTROL Ineligible]_」タブのリストを表示するときに使用できます。

1. _[!UICONTROL Products Listings]_ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_ タブ）でリストを表示します。

1. _[!UICONTROL Action]_列で、**[!UICONTROL Select]**/**[!UICONTROL Create Override]**をクリックして、製品リストの上書きページを開きます。

   ![Amazon リストの上書きの作成 ](assets/amazon-select-create-override.png){width="220"}

1. 正しいリストが表示されていることを確認するには、_[!UICONTROL Listing Details]_を確認します。

1. 作成する上書きのタイプを決定します。

   リストに対して、単一の上書きタイプまたは任意のタイプの組み合わせ（価格、処理時間、条件、販売者メモ）を定義できます。

   - **価格** - 「**[!UICONTROL Change Listing Price]**」をクリックして、**[!UICONTROL Price Override]** に定義した価格の値を入力します。
   - **時間の処理** - 「**[!UICONTROL Change Handling Time]**」をクリックして、**[!UICONTROL Handling Time Override]** に定義された時間の値（日数）を入力します。
   - **条件** - 「**[!UICONTROL Change Condition]**」をクリックして、**[!UICONTROL Condition Override]** ークフローに適したオプションを選択します。
   - **販売者メモ** - 「**[!UICONTROL Change Seller Notes]**」をクリックして、**[!UICONTROL Seller Notes Override]** のメモを入力します。

1. 「**[!UICONTROL Save Listing Override]**」をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「`Relist in Progress`」に変わります。 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 このリストは「_[!UICONTROL Overrides]_」タブにも追加されます。

次の例は、新しい価格の `$55`、新しい処理時間の `1 day`、新しい条件の `Used; Like New`、新しい販売者メモのテキストを定義するオーバーライドを示しています。

![Amazon リストの上書きの例 ](assets/amazon-overrides-edit.png){width="600" zoomable="yes"}

## 単一リストの上書きを編集または削除 {#edit-override-single-listing}

_[!UICONTROL Edit Overrides]_アクションは、「_[!UICONTROL Overrides]_」タブでリストを表示するときに使用できます。

1. リストを _[!UICONTROL Product Listings]_ページ（「_[!UICONTROL Overrides]_」タブ）で表示します。

1. 「_[!UICONTROL Action]_」列で、**[!UICONTROL Select]**/**[!UICONTROL Edit Overrides]**をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択 ](assets/amazon-select-edit-overrides.png){width="125"}

1. 正しいリストを上書きしていることを確認するには、_[!UICONTROL Listing Details]_を確認します。

1. _[!UICONTROL Override]_設定を編集するには、変更するタイプ（価格、処理時間、条件、販売者メモ）のセクションを定義します。

   上書きタイプを同じにするには、「`No Change To <override type>`」（デフォルト）を選択します。 この設定では、以前に定義したオーバーライド値は変更されません。

   - **価格** - 「**[!UICONTROL Change Listing Price]**」をクリックして、**[!UICONTROL Price Override]** に定義した価格の値を入力します。
   - **時間の処理** - 「**[!UICONTROL Change Handling Time]**」をクリックして、**[!UICONTROL Handling Time Override]** に定義された時間の値（日数）を入力します。
   - **条件** - 「**[!UICONTROL Change Condition]**」をクリックして、**[!UICONTROL Condition Override]** に対して正しいオプションを選択します。
   - **販売者メモ** - 「**[!UICONTROL Change Seller Notes]**」をクリックして、**[!UICONTROL Seller Notes Override]** のメモを入力します。

1. 上書きタイプを削除するには、削除するタイプごとに **削除** をクリックします。 削除しない場合、以前に定義した値はオーバーライドに残ります。

1. 「**[!UICONTROL Save Listing Override]**」をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「`Relist in Progress`」に変わります。 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 まだリストに表示されていない場合は、リストも「_[!UICONTROL Overrides]_」タブに追加されます。

_オーバーライドの作成_ の例を示します。 次の例では、以前に作成した上書きの編集を示します。この編集では、新しい価格の `$50` を定義し、処理時間の上書きを削除し、以前の条件と販売者のメモの上書きを保持します。

![ オーバーライドの編集または削除 ](assets/amazon-overrides-edit-2.png){width="600" zoomable="yes"}
__

## 複数の一覧の上書きを編集または削除します {#edit-override-multiple-listings}

_[!UICONTROL Edit Listing Overrides]_アクションは、「_[!UICONTROL Inactive]_」、「_[!UICONTROL Active]_」、「_[!UICONTROL Overrides]_」、「_[!UICONTROL Ineligible]_」の各タブで使用できます。

>[!NOTE]
>
>複数の一覧に対する優先設定を修正しているため、単一の一覧を修正する場合のように、_[!UICONTROL Listing Details]_のセクションは表示されません。

1. リストを _[!UICONTROL Products Listings]_ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Overrides]_、_[!UICONTROL Ineligible]_の各タブ）で表示します。

1. 変更する各一覧の左側の列にあるチェックボックスをオンにします。

1. [_[!UICONTROL Actions]_] で、[**[!UICONTROL Edit Listing Overrides]**] をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択 ](assets/amazon-actions-edit-listing-overrides.png){width="200"}

1. _[!UICONTROL Override]_設定を編集するには、変更するタイプ（価格、処理時間、条件、販売者メモ）のセクションを定義します。

   上書きを同じにするには、「`No Change To <override type>`」（デフォルト）を選択します。 この設定では、以前に定義したオーバーライド値は変更されません。

   - **価格** - 「**[!UICONTROL Change Listing Price]**」をクリックして、**[!UICONTROL Price Override]** に定義した価格の値を入力します。
   - **時間の処理** - 「**[!UICONTROL Change Handling Time]**」をクリックして、**[!UICONTROL Handling Time Override]** に定義された時間の値（日数）を入力します。
   - **条件** - 「**[!UICONTROL Change Condition]**」をクリックして、**[!UICONTROL Condition Override]** に対して正しいオプションを選択します。
   - **販売者メモ** - 「**[!UICONTROL Change Seller Notes]**」をクリックして、**[!UICONTROL Seller Notes Override]** のメモを入力します。

1. 上書きタイプを削除するには、削除する各タイプの **[!UICONTROL Remove]** をクリックします。 削除しない場合、以前に定義した値はオーバーライドに残ります。

1. 「**[!UICONTROL Save Listing Override]**」をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが「`Relist in Progress`」に変わります。 変更内容は、次回のデータ同期と共に（cron 設定で指定したとおりに）Amazonに公開されます。 まだリストに表示されていない場合は、リストも「_[!UICONTROL Overrides]_」タブに追加されます。

### タイプを上書き

| 上書き | 説明 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Override] | 価格の上書きは、リストの価格を定義します。 このオーバーライドは、オーバーライドが削除されるまで、すべての自動設定よりも優先されます。<br><br> 商品の価格を上書きするには、「**[!UICONTROL Change Listing Price]**」を選択し、**[!UICONTROL Price Override]** の新しい価格を入力します。 |
| [!UICONTROL Handling Time Override] | 処理時間の上書きでは、製品の処理および出荷に要する時間（日数）を定義します。 処理時間のオーバーライドは、オーバーライドが削除されるまで、自動化されたすべてのデフォルトの処理時間設定よりも優先されます。<br><br>_[!UICONTROL Handling Time Override]_ボックスに存在する値は、「リスト [ 設定で定義したデフォルトの処理時間か ](./listing-settings.md) 定義したオーバーライド処理時間です。 処理時間の上書きを削除すると、リストのデフォルトは、リスト設定で定義した処理時間になります。<br><br> 処理時間の上書きを定義するには、「**[!UICONTROL Change Handling Time]**」を選択し、**[!UICONTROL Handling Time Override]**に新しい処理時間（日数）を入力します。 |
| [!UICONTROL Condition Override] | リスト条件を上書きするには、「**[!UICONTROL Change Condition]**」を選択し、「条件の上書き **から新しい条件を選択し** す。 |
| [!UICONTROL Seller Notes Override] | カタログ内の商品が `New` 以外の条件で定義されている場合、販売者メモを追加して、商品とその条件について、潜在的な購入者に対してさらに詳細に説明することができます。 `New` しい条件の商品に対して販売者メモの上書きを入力できますが、Amazonにはメモが表示されません。<br><br> 販売者メモを上書きするには、**[!UICONTROL Change Seller Notes]** を選択し、**[!UICONTROL Seller Notes Override]** に新しいメモを入力します。 |
