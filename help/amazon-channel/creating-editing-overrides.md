---
title: 上書きの作成と編集
description: AmazonSales Channelの上書きを使用して、変更を1つのAmazonリストまたは複数のリストに適用します。
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# 上書きの作成と編集

リストの作成と上書き、またはリストに適用された上書きの編集または削除を行うことができます。 上書きは、特定のリストに対して定義された値を設定します。

## 単一リストに対する上書きの作成

_[!UICONTROL Create Override]_アクションは、_[!UICONTROL Inactive]_、_[!UICONTROL Active]_および_[!UICONTROL Ineligible]_&#x200B;の各タブのリストを表示する際に使用できます。

1. _[!UICONTROL Products Listings]_ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_&#x200B;タブ）のリストを表示します。

1. _[!UICONTROL Action]_列で、**[!UICONTROL Select]**/**[!UICONTROL Create Override]**をクリックして、製品リストの上書きページを開きます。

   ![Amazonリストの上書きの作成](assets/amazon-select-create-override.png)

1. 正しいリストを表示していることを確認するには、_[!UICONTROL Listing Details]_を確認します。

1. 作成する上書きのタイプを決定します。

   1つの上書きタイプまたはリスト用の任意のタイプの組み合わせを定義できます（価格、処理時間、条件、販売者のメモ）。

   - **価格**  — をクリック **[!UICONTROL Change Listing Price]** し、に定義した価格値を入力し **[!UICONTROL Price Override]**&#x200B;ます。
   - **処理時間**  — をクリック **[!UICONTROL Change Handling Time]** し、に対して定義した時間値（日単位）を入力し **[!UICONTROL Handling Time Override]**&#x200B;ます。
   - **条件**  — をクリック **[!UICONTROL Change Condition]** し、に対して正しいオプションを選択し **[!UICONTROL Condition Override]**&#x200B;ます。
   - **販売者向けメモ**  — をクリック **[!UICONTROL Change Seller Notes]** し、にメモのテキストを入力し **[!UICONTROL Seller Notes Override]**&#x200B;ます。

1. **[!UICONTROL Save Listing Override]**&#x200B;をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが`Relist in Progress`に変わります。 変更は、次回のデータ同期（cron設定での設定に従って）と共にAmazonに公開されます。 リストは_[!UICONTROL Overrides]_&#x200B;タブにも追加されます。

次の例は、新しい価格`$55`、新しい処理時間`1 day`、新しい条件`Used; Like New`、新しい売り手票テキストを定義する上書きを示しています。

![Amazonリストの上書きの例](assets/amazon-overrides-edit.png)

## 単一のリストの上書きの編集または削除 {#edit-override-single-listing}

_[!UICONTROL Edit Overrides]_アクションは、_[!UICONTROL Overrides]_&#x200B;タブのリストを表示する際に使用できます。

1. _[!UICONTROL Product Listings]_ページ（「_[!UICONTROL Overrides]_」タブ）でリストを表示します。

1. _[!UICONTROL Action]_列で、**[!UICONTROL Select]**>**[!UICONTROL Edit Overrides]**をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazonリストの上書きの選択](assets/amazon-select-edit-overrides.png)

1. 正しいリストを上書きするには、_[!UICONTROL Listing Details]_を確認します。

1. _[!UICONTROL Override]_設定を編集するには、変更するタイプのセクション（価格、取り扱い時間、条件、販売者向けメモ）を定義します。

   上書きタイプを同じにするには、`No Change To <override type>`（デフォルト）を選択します。 この設定は、以前に定義した上書き値を変更しません。

   - **価格**  — をクリック **[!UICONTROL Change Listing Price]** し、に定義した価格値を入力し **[!UICONTROL Price Override]**&#x200B;ます。
   - **処理時間**  — をクリック **[!UICONTROL Change Handling Time]** し、に対して定義した時間値（日単位）を入力し **[!UICONTROL Handling Time Override]**&#x200B;ます。
   - **条件**  — をクリック **[!UICONTROL Change Condition]** し、に対して正しいオプションを選択し **[!UICONTROL Condition Override]**&#x200B;ます。
   - **販売者向けメモ**  — をクリック **[!UICONTROL Change Seller Notes]** し、にメモのテキストを入力し **[!UICONTROL Seller Notes Override]**&#x200B;ます。

1. 上書きタイプを削除するには、削除する各タイプの&#x200B;**削除**&#x200B;をクリックします。 削除しない場合、以前に定義した値は上書きに残ります。

1. **[!UICONTROL Save Listing Override]**&#x200B;をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが`Relist in Progress`に変わります。 変更は、次回のデータ同期（cron設定での設定に従って）と共にAmazonに公開されます。 リストがまだ表示されていない場合は、リストも_[!UICONTROL Overrides]_&#x200B;タブに追加されます。

_Override_&#x200B;の例にピギーバックを入れます。 次の例は、前に作成した上書きの編集を示しています。この編集により、新しい価格`$50`が定義され、処理時間の上書きが削除され、前の条件と販売者のメモの上書きが保持されます。

![上書きの編集または削除](assets/amazon-overrides-edit-2.png)
__

## 複数のリストの上書きの編集または削除 {#edit-override-multiple-listings}

_[!UICONTROL Edit Listing Overrides]_アクションは、_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Overrides]_&#x200B;および&#x200B;_[!UICONTROL Ineligible]_の各タブで使用できます。

>[!NOTE]
>
>複数のリストの上書きを変更するので、_[!UICONTROL Listing Details]_セクションは、1つのリストを変更する場合とは異なり、表示されません。

1. _[!UICONTROL Products Listings]_ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Overrides]_、および&#x200B;_[!UICONTROL Ineligible]_タブ）でリストを表示します。

1. 変更する各リストの左側の列にあるチェックボックスを選択します。

1. _[!UICONTROL Actions]_の下で、**[!UICONTROL Edit Listing Overrides]**をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazonリストの上書きの選択](assets/amazon-actions-edit-listing-overrides.png)

1. _[!UICONTROL Override]_設定を編集するには、変更するタイプのセクション（価格、取り扱い時間、条件、販売者向けメモ）を定義します。

   上書きを同じにするには、`No Change To <override type>`（デフォルト）を選択します。 この設定は、以前に定義した上書き値を変更しません。

   - **価格**  — をクリック **[!UICONTROL Change Listing Price]** し、に定義した価格値を入力し **[!UICONTROL Price Override]**&#x200B;ます。
   - **処理時間**  — をクリック **[!UICONTROL Change Handling Time]** し、に対して定義した時間値（日単位）を入力し **[!UICONTROL Handling Time Override]**&#x200B;ます。
   - **条件**  — をクリック **[!UICONTROL Change Condition]** し、に対して正しいオプションを選択し **[!UICONTROL Condition Override]**&#x200B;ます。
   - **販売者向けメモ**  — をクリック **[!UICONTROL Change Seller Notes]** し、にメモのテキストを入力し **[!UICONTROL Seller Notes Override]**&#x200B;ます。

1. 上書きタイプを削除するには、削除する各タイプの&#x200B;**[!UICONTROL Remove]**&#x200B;をクリックします。 削除しない場合、以前に定義した値は上書きに残ります。

1. **[!UICONTROL Save Listing Override]**&#x200B;をクリックします。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。 リストのステータスが`Relist in Progress`に変わります。 変更は、次回のデータ同期（cron設定での設定に従って）と共にAmazonに公開されます。 リストがまだ表示されていない場合は、リストも_[!UICONTROL Overrides]_&#x200B;タブに追加されます。

### タイプの上書き

| 上書き | 説明 |
|--- |--- |
| [!UICONTROL Price Override] | 価格の上書きは、上場の価格を定義します。 この上書きは、上書きが削除されるまで、すべての自動設定よりも優先されます。<br><br>製品の価格を上書きするには、「 」を選択 **[!UICONTROL Change Listing Price]** し、の新しい価格を入力し **[!UICONTROL Price Override]**&#x200B;ます。 |
| [!UICONTROL Handling Time Override] | 処理時間の上書きは、製品の処理と出荷にかかる時間（日数）を定義します。 処理時間の上書きは、上書きが削除されるまで、自動化およびデフォルトの処理時間設定よりも優先されます。<br><br>ボックスに存在する値は、リ _[!UICONTROL Handling Time Override]_スト設定で定義されたデフォルトの処理時間か、定義された上 [書き](./listing-settings.md) 処理時間のいずれかになります。処理時間の上書きを削除すると、リスト設定で定義された処理時間がデフォルトで表示されます。<br><br>処理時間の上書きを定義するに&#x200B;**[!UICONTROL Change Handling Time]**は、「 」を選択し、の新しい処理時間（日単位）を入力しま&#x200B;**[!UICONTROL Handling Time Override]**す。 |
| [!UICONTROL Condition Override] | リスト条件を上書きするには、**[!UICONTROL Change Condition]**&#x200B;を選択し、**条件の上書き**&#x200B;から新しい条件を選択します。 |
| [!UICONTROL Seller Notes Override] | `New`以外の条件で定義されたカタログ内の製品の場合は、販売者向けのメモを追加して、製品とその条件を購入者に対してさらに詳しく説明できます。 `New`条件商品に対して販売者向けのメモの上書きを入力できますが、Amazonではメモは表示されません。<br><br>販売者ノートを上書きするには、を選択 **[!UICONTROL Change Seller Notes]** し、に新しいメモを入力しま **[!UICONTROL Seller Notes Override]**&#x200B;す。 |
