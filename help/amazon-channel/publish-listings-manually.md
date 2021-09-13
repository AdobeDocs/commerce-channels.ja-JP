---
title: 手動でのAmazon一覧の公開
description: 必要に応じて、終了したAmazonのリストをコマース管理者から手動で公開できます。
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Amazonリストの手動公開

終了した1つ以上のAmazonリストを手動で公開できます。

1. [製品リスト](./managing-product-listings.md)ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_の各タブ）の「_[!UICONTROL Ended]_」タブで、1つ以上のリストを表示します。

1. 左側の列で、をクリックして、再公開する各リストを確認します。

1. _[!UICONTROL Actions]_の下で、**[!UICONTROL Publish Product to Amazon]**をクリックします。

1. 確認メッセージの&#x200B;**[!UICONTROL OK]**&#x200B;をクリックします。

   選択したリストがAmazonに公開するために処理されていることを確認するメッセージが表示されます。

   リスト情報は、Cronの設定に基づいてAmazonに公開されます。 リスト情報は、次回のデータ同期時にAmazonに送信されます。 Amazonがリストの確認を返すまで、手動で公開したリストは「_リストの準備完了_」タブにステータス`List in Progress`で表示されます。 Amazonからリストの確認を受け取ると、リストはステータス`Active`の「_アクティブ_」タブに移動します。
