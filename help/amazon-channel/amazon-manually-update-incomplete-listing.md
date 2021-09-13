---
title: 必須情報を更新（不完全なリスト）
description: Amazonのセールスチャネルには、Amazonで必要な情報が欠落しているコマースカタログ製品を監視する「不完全」タブが用意されています。
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# 必須情報を更新（不完全なリスト）

「_[!UICONTROL Incomplete]_」タブに表示されるリストには、リストルールで定義されたAmazonの適格要件を満たすが、リストする前にAmazonで必要な情報が欠落している[!DNL Commerce]カタログ製品が含まれます。

## 必要な情報を更新する(Amazonリストに割り当てられません) {#update-required-info-unable-to-assign-to-amazon-listing}

1. [リストの管理](./managing-product-listings.md)の「_[!UICONTROL Incomplete]_」タブでリストを表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazonリストと照合しようとしているカタログ製品情報（SKUと製品名）を確認します。

1. **[!UICONTROL Assign ASIN]**&#x200B;には、カタログ商品と照合するリストにAmazonが割り当てたASINを入力します。

1. 製品の一致を保存するには、**[!UICONTROL Save Listing Update]**&#x200B;をクリックします。

これで、リストがカタログと一致し、cronとリストの設定に基づいて、リストが更新されてAmazonに公開されます。 また、「_[!UICONTROL Incomplete]_」タブからも削除されます。

![リストに一致しないASINを手動で割り当てる](assets/amazon-listing-update-assign-asin.png)

## 必要な情報を更新（複数件の一致が見つかりました） {#update-required-info-multiple-matches-found}

1. [[!UICONTROL Manage Listings]](./managing-product-listings.md)の「_[!UICONTROL Incomplete]_」タブでリストを表示します。

1. _アクション_&#x200B;列で、****&#x200B;を選択し、**更新が必要な情報**&#x200B;をクリックします。

1. Amazonリストと照合しようとしているカタログ製品情報（SKUと製品名）を確認します。

1. **[!UICONTROL Select Correct Amazon Listing]**&#x200B;の場合は、この製品に一致するリストに対して正しいASINを選択します。

   ここに示すオプションには、一致すると見なされるカタログ製品が含まれます。 どのオプションも正しくない場合は、`Manually Enter Correct ASIN`を選択し、製品のASINを手動で入力できます。

1. ASINを手動で入力する場合は、**[!UICONTROL Manually Assign ASIN]**&#x200B;に正しいASINを入力します。

1. 製品の一致を保存するには、**[!UICONTROL Save Listing Update]**&#x200B;をクリックします。

![複数の一致候補からASINを手動で選択](assets/amazon-listing-update-multiple-matches.png)

## 必要な情報を更新（バリアントが含まれる） {#update-required-info-has-variants}

1. [[!UICONTROL Manage Listings]](./managing-product-listings.md)の「_[!UICONTROL Incomplete]_」タブでリストを表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazonリストと照合しようとしているカタログ製品情報（SKUと製品名）を確認します。

1. **[!UICONTROL Select Correct Amazon Listing]**&#x200B;の場合は、この製品に一致するリストに対して正しいASINを選択します。

   ここに示すオプションには、一致すると見なされるカタログ製品が含まれます。 どのオプションも正しくない場合は、`Manually Enter Correct ASIN`を選択し、製品のASINを手動で入力できます。

1. ASINを手動で入力する場合は、**[!UICONTROL Manually Assign ASIN]**&#x200B;に正しいASINを入力します。

1. 製品の一致を保存するには、**[!UICONTROL Save Listing Update]**&#x200B;をクリックします。

![可能なバリアント一致からASINを手動で選択](assets/amazon-listing-update-multiple-matches.png)

## 必要な情報を更新（条件が見つかりません） {#update-required-info-missing-condition}

1. [リストの管理](./managing-product-listings.md)の「_[!UICONTROL Incomplete]_」タブでリストを表示します。

1. _[!UICONTROL Action]_列で、更新するリストの&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**をクリックします。

1. Amazonリストと照合しようとしているカタログ製品情報（SKUと製品名）を確認します。

1. **[!UICONTROL Condition]**&#x200B;の場合、適切な条件を選択します。

   使用可能なオプションのリストは、[製品リスト条件](./product-listing-condition.md)の設定によって異なります。

1. 製品の一致を保存するには、「 **[!UICONTROL Save Listing Update]** 」をクリックします。

![不明な条件の手動更新](assets/amazon-update-listing-missing-condition.png)
