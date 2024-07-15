---
title: Amazonの必要な情報の更新
description: Amazonの営業チャネルには、Amazonで必要な情報が欠落しているCommerce カタログ商品をモニタリングするための「未完了」タブがあります。
feature: Sales Channels, Merchandising, Catalog Management, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 必須情報の更新（不完全なリスト）

「_[!UICONTROL Incomplete]_」タブに表示されるリストには、リストルールで定義したAmazonの実施要件を満たしているが、リスト前にAmazonで必要な情報が欠落している [!DNL Commerce] カタログ製品が含まれます。

## 必要な情報を更新します（Amazon リストに割り当てることができません） {#update-required-info-unable-to-assign-to-amazon-listing}

1. [ 一覧の管理 ](./managing-product-listings.md) の [_[!UICONTROL Incomplete]_] タブで一覧を表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. **[!UICONTROL Assign ASIN]**：カタログ商品と照合するリストに対して、Amazonによって割り当てられた ASIN を入力します。

1. 製品の一致を保存するには、「**[!UICONTROL Save Listing Update]**」をクリックします。

これで、リストがカタログと一致し、cron とリストの設定に基づいてリストが更新され、Amazonに公開されます。 また、「_[!UICONTROL Incomplete]_」タブからも削除されます。

![ リスト一致なしの ASIN を手動で割り当てる ](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## 必要な情報を更新します（複数の一致が見つかりました） {#update-required-info-multiple-matches-found}

1. [[!UICONTROL Manage Listings]](./managing-product-listings.md) の [_[!UICONTROL Incomplete]_] タブで一覧を表示します。

1. _アクション_ 列で、更新するリストの **選択**/**必須情報を更新** をクリックします。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. **[!UICONTROL Select Correct Amazon Listing]**：この製品に一致させるリストの正しい ASIN を選択します。

   ここに表示されるオプションには、一致する可能性があるものとして識別されるカタログ製品が含まれます。 どのオプションも正しくない場合は、`Manually Enter Correct ASIN` を選択して、製品の ASIN を手動で入力できます。

1. ASIN を手動で入力する場合は、**[!UICONTROL Manually Assign ASIN]** に正しい ASIN を入力します。

1. 製品の一致を保存するには、「**[!UICONTROL Save Listing Update]**」をクリックします。

![ 複数の一致候補から ASIN を手動で選択する ](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## 必要な情報を更新（バリアントあり） {#update-required-info-has-variants}

1. [[!UICONTROL Manage Listings]](./managing-product-listings.md) の [_[!UICONTROL Incomplete]_] タブで一覧を表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. **[!UICONTROL Select Correct Amazon Listing]**：この製品に一致させるリストの正しい ASIN を選択します。

   ここに表示されるオプションには、一致する可能性があるものとして識別されるカタログ製品が含まれます。 どのオプションも正しくない場合は、`Manually Enter Correct ASIN` を選択して、製品の ASIN を手動で入力できます。

1. ASIN を手動で入力する場合は、**[!UICONTROL Manually Assign ASIN]** に正しい ASIN を入力します。

1. 製品の一致を保存するには、「**[!UICONTROL Save Listing Update]**」をクリックします。

## 必要な情報の更新（条件がありません） {#update-required-info-missing-condition}

1. [ 一覧の管理 ](./managing-product-listings.md) の [_[!UICONTROL Incomplete]_] タブで一覧を表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. **[!UICONTROL Condition]** しくは、適切な条件を選択します。

   使用可能なオプションのリストは、「製品リストの条件 [ の設定によっ ](./product-listing-condition.md) 異なります。

1. 製品の一致を保存するには、「**[!UICONTROL Save Listing Update]**」をクリックします。

![ 見つからない条件を手動で更新 ](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
