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

に表示されるリスト _[!UICONTROL Incomplete]_タブに次を含める [!DNL Commerce] リストルールで定義したAmazonの実施要件を満たしているが、リスト前にAmazonで必要な情報が欠落している製品のカタログを作成します。

## 必要な情報を更新します（Amazon リストに割り当てることができません） {#update-required-info-unable-to-assign-to-amazon-listing}

1. の一覧を表示する _[!UICONTROL Incomplete]_タブ [Manage Listings](./managing-product-listings.md).

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**を更新するリストに追加します。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. の場合 **[!UICONTROL Assign ASIN]**&#x200B;を選択し、カタログ商品と照合するリストに、Amazonによって割り当てられた ASIN を入力します。

1. 製品の一致を保存するには、をクリックします **[!UICONTROL Save Listing Update]**.

これで、リストがカタログと一致し、cron とリストの設定に基づいてリストが更新され、Amazonに公開されます。 また、からも削除されます。 _[!UICONTROL Incomplete]_タブ。

![リスト一致なしの ASIN を手動で割り当てる](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## 必要な情報を更新します（複数の一致が見つかりました） {#update-required-info-multiple-matches-found}

1. の一覧を表示する _[!UICONTROL Incomplete]_タブ [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. が含まれる _アクション_ 列、クリック **を選択** > **必要な情報を更新** を更新するリストに追加します。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. の場合 **[!UICONTROL Select Correct Amazon Listing]**&#x200B;を選択し、この製品に一致させるリストの正しい ASIN を選択します。

   ここに表示されるオプションには、一致する可能性があるものとして識別されるカタログ製品が含まれます。 どのオプションも正しくない場合は、次のいずれかを選択できます `Manually Enter Correct ASIN` 製品の ASIN を手動で入力します。

1. ASIN を手動で入力する場合は、 **[!UICONTROL Manually Assign ASIN]**.

1. 製品の一致を保存するには、をクリックします **[!UICONTROL Save Listing Update]**.

![複数の一致候補から ASIN を手動で選択](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## 必要な情報を更新（バリアントあり） {#update-required-info-has-variants}

1. の一覧を表示する _[!UICONTROL Incomplete]_タブ [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**を更新するリストに追加します。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. の場合 **[!UICONTROL Select Correct Amazon Listing]**&#x200B;を選択し、この製品に一致させるリストの正しい ASIN を選択します。

   ここに表示されるオプションには、一致する可能性があるものとして識別されるカタログ製品が含まれます。 どのオプションも正しくない場合は、次を選択できます。 `Manually Enter Correct ASIN` 製品の ASIN を手動で入力します。

1. ASIN を手動で入力する場合は、 **[!UICONTROL Manually Assign ASIN]**.

1. 製品の一致を保存するには、をクリックします **[!UICONTROL Save Listing Update]**.

## 必要な情報の更新（条件がありません） {#update-required-info-missing-condition}

1. の一覧を表示する _[!UICONTROL Incomplete]_タブ [Manage Listings](./managing-product-listings.md).

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**を更新するリストに追加します。

1. Amazon リストと照合しようとしているカタログ商品情報（SKU と商品名）を確認します。

1. の場合 **[!UICONTROL Condition]**、適切な条件を選択します。

   使用できるオプションのリストは、の環境によって異なります [商品リストの条件](./product-listing-condition.md) 設定。

1. 製品の一致を保存するには、をクリックします **[!UICONTROL Save Listing Update]** .

![見つからない条件を手動で更新](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
