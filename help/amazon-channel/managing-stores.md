---
title: Amazon Storesビュー
description: Amazonストアビューに移動して、各Amazonストアの基本的な統計をすばやく確認し、管理オプションにアクセスします。
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon Storesビュー

Amazon販売チャネルのホームページを表示すると、デフォルトで&#x200B;_Amazonストア_&#x200B;ビューが開きます。

![Amazon Storesビュー](assets/amazon-sales-channel-home-tabs.png)

_[!UICONTROL Amazon Stores]_ビューには、Amazonの各ストアの「ストアカード」と、いくつかの基本的な統計と管理オプションが表示されます。 各カードに表示される概要情報には、各店舗ステータス、作成日、最終更新日、注意が必要なリスト(例：不完全なリスト)と割り当てられた[!DNL Commerce] Webサイト。

_[!UICONTROL Amazon Store]_ビューを表示すると、各ストアカードで次の操作が可能になります。

- ストア[ダッシュボード](./amazon-store-dashboard.md)を開くには、**[!UICONTROL View Store]**&#x200B;をクリックします。

- ストアのステータスを変更したり、ストアを削除したりするには、**[!UICONTROL Action]**&#x200B;をクリックし、次の操作を選択します。

   - **[!UICONTROL Activate]** /  **[!UICONTROL Deactivate]**  — ストアのステータスをそれぞれまたはに変 `Active` 更す `Inactive`る場合に選択します。

      `Inactive`ストアを`Active`ステータスに変更すると、店舗の現在の店舗設定（リスト設定、価格ルール、上書きなど）を使用して、店舗のリストと注文アクティビティが有効化されます。

      ストアのステータスを`Active`から`Inactive`に変更すると、ストアのリストと注文アクティビティが中断されます。 非アクティブなストアは、すべてのストア設定とリストを保持しますが、ストアのステータスが`Active`に戻るまで、価格、数量、注文管理の同期を一時的に停止します。 この機能を使用すると、Amazonストアを再作成または再統合したり、過去の注文や販売データを失うことなく、地域レベルでストアアクティビティを制御できます。

   - **[!UICONTROL Delete]**  — 不要になったストアを削除するように選択します。

      既存のAmazonストアとその[!DNL Amazon Seller Central]アカウントとの統合設定を削除するタイミングを選択します。 アカウントを削除すると、Amazonの販売チャネルに加えて、このストアに関連するすべてのアカウント設定、リスト、ログ、その他の情報も削除されます。 削除後にストアを取得できません。新しいストアを作成する必要があります。

>[!NOTE]
>統合時にストアに割り当てられたWebサイトを変更するには、ストアを削除し、ストア統合時に定義された別のWebサイトを使用してストアを再度追加する必要があります。

| ストアカード | 説明 |
|--- |--- |
| 上部セクション | 以下を含みます。<br>ストアの領域アイコン。[ストア統合](./store-integration.md)の間に定義されます。<br> 割り当て済 _[!UICONTROL Magento Website]_み（ストア統合時に定義）。<br>ストア_[!UICONTROL Status]_ の。オプション：**[!UICONTROL Active]** — ストア統合が完了し、Amazonで検証され、販売活動に利用できます。 **[!UICONTROL Inactive]**  — ストアの統合は完了しましたが、使用されていないか、販売活動に使用できません。`Inactive`の時点で、Amazonの販売は一時停止します。 `Active`の場合、販売売上高と追加設定が保存され、有効化する前に更新されます。<br>Amazonス *[!UICONTROL Last Updated]* トア設定に対する最新の変更日。<br>Amazon *[!UICONTROL Created]* ストアがAmazon販売チャネルで作成された日付。 |
| 中央のセクション | 過去30日間の店舗アクティビティの概要グラフが含まれ、注意が必要なリストが含まれ、アラートが表示されます。 |
| 下部セクション | ビューストアとアクションのオプションが含まれます。<br>ストアダッシュボードを開くに [は、](./amazon-store-dashboard.md)をクリックしま **[!UICONTROL View Store]**&#x200B;す。<br>ストアをアクティブ化、非アクティブ化、または削除するには、をクリックしま **[!UICONTROL Actions]**&#x200B;す。 |
