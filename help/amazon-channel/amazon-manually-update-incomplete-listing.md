---
title: 「必要な情報を更新」
description: Amazon 販売チャンネルは、Amazon によって要求される情報が不足している Commerce カタログ製品を監視するために、未完のタブが提供されます。
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# 「必要な情報を更新」

このタブに表示されるリストに _[!UICONTROL Incomplete]_は、 [!DNL Commerce] リスティングルールで定義されているように amazon の必要条件に合致するもののカタログ製品が含まれていますが、amazon によって一覧表示される前に必要な情報は失われます。

## 必要な情報を更新する (Amazon リストに割り当てられることはできません) {#update-required-info-unable-to-assign-to-amazon-listing}

1. 「リストの管理」のタブに表示されている一覧が表示さ _[!UICONTROL Incomplete]_[ ](./managing-product-listings.md) れます。

1. 列に表示されているリストを更新するには、 _[!UICONTROL Action]_「>」をクリックし&#x200B;**[!UICONTROL Select]****[!UICONTROL Update Required Info]**ます。

1. Amazon リストに一致するカタログ製品情報 (SKU と製品名) を確認してください。

1. **[!UICONTROL Assign ASIN]**「」には、Amazon によって、カタログ製品に適合させるリストに割り当てられたアークサインを入力します。

1. 製品の検索結果を保存するには、をクリックし **[!UICONTROL Save Listing Update]** ます。

リストがカタログと一致するようになり、一覧が更新され、Amazon に公開されます。 cron とリスティングの設定に基づいています。 タブからも削除され _[!UICONTROL Incomplete]_ます。

![リストに合わせる対象のアークサインなしの手動割り当て](assets/amazon-listing-update-assign-asin.png)

## 「必要な情報を更新」 (複数の一致が見つかりました) {#update-required-info-multiple-matches-found}

1. のタブに一覧を表示 _[!UICONTROL Incomplete]_[[!UICONTROL Manage Listings]](./managing-product-listings.md) します。

1. _「アクション」_ 列で、 **「** 更新したい情報を > に更新」をクリックし **** ます。

1. Amazon リストに一致するカタログ製品情報 (SKU と製品名) を確認してください。

1. については **[!UICONTROL Select Correct Amazon Listing]** 、この製品に適合させたいリストの適切なサインを選択してください。

   ここに一覧表示されているオプションには、一致している可能性があるカタログ製品が含まれています。 適切なオプションがない場合は、その `Manually Enter Correct ASIN` 製品のアークサインを選択し、手動で入力します。

1. 手動で入力した場合は、に対して正しいアークサインを入力し **[!UICONTROL Manually Assign ASIN]** ます。

1. 製品の検索結果を保存するには、をクリックし **[!UICONTROL Save Listing Update]** ます。

![複数の検索候補からのアークサインの手動選択](assets/amazon-listing-update-multiple-matches.png)

## 「必要な情報を更新」 (バリエーションあり) {#update-required-info-has-variants}

1. のタブに一覧を表示 _[!UICONTROL Incomplete]_[[!UICONTROL Manage Listings]](./managing-product-listings.md) します。

1. 列に表示されているリストを更新するには、 _[!UICONTROL Action]_「>」をクリックし&#x200B;**[!UICONTROL Select]****[!UICONTROL Update Required Info]**ます。

1. Amazon リストに一致するカタログ製品情報 (SKU と製品名) を確認してください。

1. については **[!UICONTROL Select Correct Amazon Listing]** 、この製品に適合させたいリストの適切なサインを選択してください。

   ここに一覧表示されているオプションには、一致している可能性があるカタログ製品が含まれています。 適切なオプションがない場合は、製品のアークサインを選択し、手動で入力することができ `Manually Enter Correct ASIN` ます。

1. 手動で入力した場合は、に対して正しいアークサインを入力し **[!UICONTROL Manually Assign ASIN]** ます。

1. 製品の検索結果を保存するには、をクリックし **[!UICONTROL Save Listing Update]** ます。

![使用可能なバリエーションからのアークサインの手動選択](assets/amazon-listing-update-multiple-matches.png)

## 「必要な情報を更新」 (条件がありません) {#update-required-info-missing-condition}

1. 「リストの管理」のタブに表示されている一覧が表示さ _[!UICONTROL Incomplete]_[ ](./managing-product-listings.md) れます。

1. 列に表示されているリストを更新するには、 _[!UICONTROL Action]_「>」をクリックし&#x200B;**[!UICONTROL Select]****[!UICONTROL Update Required Info]**ます。

1. Amazon リストに一致するカタログ製品情報 (SKU と製品名) を確認してください。

1. については **[!UICONTROL Condition]** 、適切な条件を選択します。

   使用可能なオプションの一覧は、製品の一覧表示条件設定によって異なり [ ](./product-listing-condition.md) ます。

1. 製品の検索結果を保存するには、をクリックし **[!UICONTROL Save Listing Update]** ます。

![見つからない条件の手動更新](assets/amazon-update-listing-missing-condition.png)
