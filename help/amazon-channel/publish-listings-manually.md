---
title: Amazon リストの手動公開
description: 必要に応じて、終了したAmazonのリストをCommerce管理者から手動で公開できます。
feature: Sales Channels, Products, Merchandising
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Amazon リストの手動公開

終了した 1 つ以上のAmazonのリストを手動で公開できます。

1. [ 製品リスト ](./managing-product-listings.md) ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_ または _[!UICONTROL Ineligible]_の各タブ）の_[!UICONTROL Ended]_ のタブで、1 つまたは複数のリストを表示します。

1. 左の列で、再公開する一覧をクリックして確認します。

1. [_[!UICONTROL Actions]_] で、[**[!UICONTROL Publish Product to Amazon]**] をクリックします。

1. 確認メッセージで「**[!UICONTROL OK]**」をクリックします。

   選択したリストがAmazonへの公開に向けて処理されていることを確認するメッセージが表示されます。

   Cron の設定に基づいて、リスト情報がAmazonに公開されます。 リスト情報は、次回のデータ同期時にAmazonに送信されます。 Amazonからリスト確認の返信が届くまで、手動で公開したリストは _リスト準備完了_ タブに残り、ステータスは `List in Progress` くなります。 Amazonからリストの確認を受信すると、リストは「_アクティブ_」タブに移動し、`Active` ステータスになります。
