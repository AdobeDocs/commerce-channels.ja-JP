---
title: 上書きの作成と編集
description: AmazonSales Channelのオーバーライドを使用して、変更を 1 つのAmazonリストに適用するか、複数のリストに適用します。
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# 上書きの作成と編集

リストの作成と上書きを行ったり、リストに適用されている上書きを編集または削除したりできます。 オーバーライドは、特定のリストに対して定義された値を設定します。

## 単一リストに対する上書きの作成

この _[!UICONTROL Create Override]_アクションは、_[!UICONTROL Inactive]_, _[!UICONTROL Active]_、および_[!UICONTROL Ineligible]_ タブ

1. リストの表示： _[!UICONTROL Products Listings]_ページ (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_、および_[!UICONTROL Ineligible]_ 」タブ ) をクリックします。

1. 内 _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Create Override]**をクリックして、製品リストの上書きページを開きます。

   ![Amazonリストの上書きを作成](assets/amazon-select-create-override.png)

1. 正しいリストを表示していることを確認するには、 _[!UICONTROL Listing Details]_.

1. 作成するオーバーライドのタイプを決定します。

   1 つの上書きタイプを定義するか、リストに対する任意のタイプの組み合わせ（価格、処理時間、条件、販売者の注記）を定義できます。

   - **価格**  — クリック **[!UICONTROL Change Listing Price]** に定義した価格値を入力します。 **[!UICONTROL Price Override]**.
   - **処理時間**  — クリック **[!UICONTROL Change Handling Time]** を選択し、次の期間の定義済みの時間値（日数）を入力します。 **[!UICONTROL Handling Time Override]**.
   - **条件**  — クリック **[!UICONTROL Change Condition]** を選択し、 **[!UICONTROL Condition Override]**.
   - **販売者の注記**  — クリック **[!UICONTROL Change Seller Notes]** メモのテキストを入力します。 **[!UICONTROL Seller Notes Override]**.

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが `Relist in Progress`. 変更は、次回のデータ同期（cron 設定での設定に従って）と共にAmazonに公開されます。 リストも_[!UICONTROL Overrides]_ タブをクリックします。

次の例は、 `$55`、新しい処理時間 `1 day`新しい状態 `Used; Like New`、および新しい販売者注記テキスト。

![Amazonリストの上書きの例](assets/amazon-overrides-edit.png)

## 単一のリストに対する上書きの編集または削除 {#edit-override-single-listing}

この _[!UICONTROL Edit Overrides]_アクションは、_[!UICONTROL Overrides]_ タブをクリックします。

1. リストを _[!UICONTROL Product Listings]_ページ (_[!UICONTROL Overrides]_ 」タブ ) をクリックします。

1. 内 _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**.

   この _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazonリストの上書きを選択](assets/amazon-select-edit-overrides.png)

1. 正しいリストを上書きするには、 _[!UICONTROL Listing Details]_.

1. 次の手順で _[!UICONTROL Override]_設定で、変更するタイプのセクション（価格、処理時間、条件、販売者の注記）を定義します。

   上書きタイプを同じにするには、「 `No Change To <override type>` （デフォルト）。 この設定は、以前に定義した上書き値を変更しません。

   - **価格**  — クリック **[!UICONTROL Change Listing Price]** に定義した価格値を入力します。 **[!UICONTROL Price Override]**.
   - **処理時間**  — クリック **[!UICONTROL Change Handling Time]** を選択し、次の期間の定義済みの時間値（日数）を入力します。 **[!UICONTROL Handling Time Override]**.
   - **条件**  — クリック **[!UICONTROL Change Condition]** を選択し、 **[!UICONTROL Condition Override]**.
   - **販売者の注記**  — クリック **[!UICONTROL Change Seller Notes]** メモのテキストを入力します。 **[!UICONTROL Seller Notes Override]**.

1. 上書きタイプを削除するには、 **削除** を削除する各タイプに対して使用します。 削除されない場合、以前に定義した値は上書きに残ります。

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが `Relist in Progress`. 変更は、次回のデータ同期（cron 設定での設定に従って）と共にAmazonに公開されます。 リストがまだ表示されていない場合は、リストも_[!UICONTROL Overrides]_ タブをクリックします。

Piggybacking on the _オーバーライドの作成_ 例： 次の例は、新しい価格を定義する、前に作成した上書きの編集を示しています。 `$50`をクリックすると、[ 処理時間 ] の上書きが削除され、前の [ 条件 ] と [ 販売者注記 ] の上書きが保持されます。

![オーバーライドの編集または削除](assets/amazon-overrides-edit-2.png)
__

## 複数のリストの上書きを編集または削除する {#edit-override-multiple-listings}

この _[!UICONTROL Edit Listing Overrides]_アクションは、_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_、および _[!UICONTROL Ineligible]_タブ

>[!NOTE]
>
>複数のリストの上書きを変更するので、 _[!UICONTROL Listing Details]_セクションは、単一のリストを変更する場合とは異なり、表示されません。

1. リストを _[!UICONTROL Products Listings]_ページ (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_、および _[!UICONTROL Ineligible]_」タブ ) をクリックします。

1. 変更する各リストの左側の列のチェックボックスをオンにします。

1. の下 _[!UICONTROL Actions]_をクリックし、**[!UICONTROL Edit Listing Overrides]**.

   この _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazonリストの上書きを選択](assets/amazon-actions-edit-listing-overrides.png)

1. 次の手順で _[!UICONTROL Override]_設定で、変更するタイプのセクション（価格、処理時間、条件、販売者の注記）を定義します。

   上書きを同じにするには、 `No Change To <override type>` （デフォルト）。 この設定は、以前に定義した上書き値を変更しません。

   - **価格**  — クリック **[!UICONTROL Change Listing Price]** に定義した価格値を入力します。 **[!UICONTROL Price Override]**.
   - **処理時間**  — クリック **[!UICONTROL Change Handling Time]** を選択し、次の期間の定義済みの時間値（日数）を入力します。 **[!UICONTROL Handling Time Override]**.
   - **条件**  — クリック **[!UICONTROL Change Condition]** を選択し、 **[!UICONTROL Condition Override]**.
   - **販売者の注記**  — クリック **[!UICONTROL Change Seller Notes]** メモのテキストを入力します。 **[!UICONTROL Seller Notes Override]**.

1. 上書きタイプを削除するには、 **[!UICONTROL Remove]** を削除する各タイプに対して使用します。 削除されない場合、以前に定義した値は上書きに残ります。

1. クリック **[!UICONTROL Save Listing Override]**.

   この _[!UICONTROL Product Listing Overrides]_ページが閉じます。 一覧のステータスは `Relist in Progress`. 変更は、次回のデータ同期（cron 設定での設定に従って）と共にAmazonに公開されます。 リストがまだ表示されていない場合は、リストも_[!UICONTROL Overrides]_ タブをクリックします。

### タイプを上書き

| 上書き | 説明 |
|--- |--- |
| [!UICONTROL Price Override] | 価格の上書きは、上場の価格を定義します。 この上書きは、上書きが削除されるまで、すべての自動設定よりも優先されます。<br><br>製品の価格を上書きするには、 **[!UICONTROL Change Listing Price]** 新しい価格を入力します。 **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | 処理時間の上書きは、製品の処理と出荷に要する時間（日数）を定義します。 処理時間の上書きは、上書きが削除されるまで、自動化およびデフォルトの処理時間設定よりも優先されます。<br><br>に存在する値 _[!UICONTROL Handling Time Override]_ボックスは、 [リスト設定](./listing-settings.md) または定義した上書き処理時間。 処理時間の上書きを削除すると、リストの設定で定義された処理時間がデフォルトで表示されます。<br><br>処理時間の上書きを定義するには、「 」を選択します。**[!UICONTROL Change Handling Time]**次の新しい処理時間（日数）を入力します：**[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | リスト条件を上書きするには、 **[!UICONTROL Change Condition]** 次の中から新しい条件を選択します。 **条件の上書き**. |
| [!UICONTROL Seller Notes Override] | カタログ内の製品で、 `New`を使用すると、販売者向けのメモを追加して、製品とその条件を購入者に対して詳しく説明できます。 売り手形の上書きを `New` 条件製品ですが、Amazonにはメモは表示されません。<br><br>販売者の注記を上書きするには、 **[!UICONTROL Change Seller Notes]** 新しいメモを入力します。 **[!UICONTROL Seller Notes Override]**. |
