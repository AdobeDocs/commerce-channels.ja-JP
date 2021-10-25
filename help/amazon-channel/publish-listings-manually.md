---
title: Amazon リストの手動公開
description: 必要に応じて、終了した Amazon リストを Commerce 管理ツールから手動でパブリッシュできます。
exl-id: ca3f674e-d93a-44a6-8c06-b417694a0f1e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Amazon リストの手動公開

終了した1つ以上の Amazon リストを手動でパブリッシュすることができます。

1. _[!UICONTROL Ended]_[ 製品リスト ](./managing-product-listings.md) ページ (_[!UICONTROL Inactive]_ 、、 _[!UICONTROL Active]_、またはタブ) のタブに表示さ_[!UICONTROL Ineligible]_ れている1つまたは複数のリストを表示します。

1. 「左側」列で、再パブリッシュする各一覧をクリックしてチェックボックスをオンにします。

1. _[!UICONTROL Actions]_でをクリックし&#x200B;**[!UICONTROL Publish Product to Amazon]**ます。

1. **[!UICONTROL OK]**&#x200B;確認メッセージ内をクリックします。

   選択されているリストが、Amazon に公開するために処理されていることを確認するメッセージが表示されます。

   リスト情報は、cron の設定に基づいて Amazon に公開されます。 リスト情報は、次のデータ同期時に Amazon に送信されます。 このリストが表示されていると、Amazon が応答するまでは、手動でパブリッシュされた出展は状態の「 _リスト_ 」タブに残り `List in Progress` ます。 リスト確認が Amazon から受信されると、リストがアクティブな tab に移動してステータスが表示され __ `Active` ます。
