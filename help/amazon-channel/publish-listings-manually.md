---
title: 手動でのAmazonリストの公開
description: 必要に応じて、終了したAmazonのリストをコマース管理者から手動で公開できます。
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 手動でのAmazonリストの公開

終了した 1 つ以上のAmazonリストを手動で公開できます。

1. 1 つ以上のリストを _[!UICONTROL Ended]_タブ [製品リスト](./managing-product-listings.md) ページ (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_または_[!UICONTROL Ineligible]_ 」タブ ) をクリックします。

1. 左の列で、をクリックして、再公開する各リストを確認します。

1. の下 _[!UICONTROL Actions]_をクリックし、**[!UICONTROL Publish Product to Amazon]**.

1. クリック **[!UICONTROL OK]** をクリックします。

   選択したリストが処理されてAmazonに公開されることを確認するメッセージが表示されます。

   リスト情報は、cron 設定に基づいてAmazonに公開されます。 リスト情報は、次回のデータ同期時にAmazonに送信されます。 Amazonがリストの確認を返すまで、手動で公開したリストは _リストへの登録準備完了_ タブと `List in Progress` ステータス。 リストの確認がAmazonから受け取られると、リストは、 _アクティブ_ タブに `Active` ステータス。
