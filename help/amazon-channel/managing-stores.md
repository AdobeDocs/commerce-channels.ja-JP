---
title: Amazon Stores ビュー
description: Amazon stores view を参照して、Amazon stores に関する基本的な統計情報と、アクセス管理オプションをすばやく確認できます。
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon Stores ビュー

Amazon sales channel のホームページが表示されると、 __ デフォルトで amazon Stores ビューが開きます。

![Amazon Stores ビュー](assets/amazon-sales-channel-home-tabs.png)

このビューには、 _[!UICONTROL Amazon Stores]_Amazon stores に含まれる「保管カード」と共に、基本的な統計情報および管理オプションが表示されます。 各カードに表示される概要情報には、各ストアの状態、作成日、最終更新日、注意が必要なリスト (例: 完成されていないリスト)、割り当てられている web サイトが含まれてい [!DNL Commerce] ます。

ビューを表示すると _[!UICONTROL Amazon Store]_、各ストアカードで次の操作を実行できます。

- ストアのダッシュボードを開くには [ ](./amazon-store-dashboard.md) 、をクリックし **[!UICONTROL View Store]** ます。

- ストアの状態を変更したり、ストアを削除するには、をクリックし **[!UICONTROL Action]** て次のいずれかのオプションを選択します。

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** -ストアの状態を変更する `Active` か、またはそのいずれかを選択し `Inactive` ます。

      ストアが状態に変更されると、ストア `Inactive` `Active` の出展とオーダーが有効になり、ストアの現在のストア設定が保存されます (リストの設定、価格ルール、上書きなど)。

      ストアの状態を「状態」から「 `Active` 状態」に変更する `Inactive` と、ストアの一覧およびオーダーが停止されます。 非アクティブなストアでは、すべてのストア設定および一覧が保持されますが、価格、数量、注文管理の同期は、ストアがステータスに戻るまで一時的に停止され `Active` ます。 この機能を使用すると、Amazon の内容を再作成または再統合することなく、地域レベルで保存することができます。

   - **[!UICONTROL Delete]** -不要になったストアを削除する場合に選択します。

      既存の Amazon store とその統合設定をアカウントと共に削除するタイミングを選択し [!DNL Amazon Seller Central] ます。 取引先企業を削除すると、Amazon sales channel からストアが削除され、すべてのアカウント設定、番組一覧、ログ、その他の情報がこのストアに関連付けられます。 ストアは、削除した後で取得することはできません。新しいストアを作成する必要があります。

>[!NOTE]
>統合中にストアに割り当てられた web サイトを変更するには、ストアを削除して、ストア統合時に定義された別の web サイトにストアを再追加する必要があります。

| ストアカード | つい |
|--- |--- |
| トップセクション | 含まれる内容は、ストア <br> の統合時に定義された地域のアイコンです [ ](./store-integration.md) 。<br>_[!UICONTROL Magento Website]_ストア統合時に定義された割り当て。<br>_[!UICONTROL Status]_&#x200B;お客様のストアに保存されています。オプション: 「 **[!UICONTROL Active]** ストアの統合」が Amazon によって検証され、セールス活動に使用できるようになりました。 **[!UICONTROL Inactive]** -Store の統合が完了しましたが、使用されていないか、営業活動で使用できません。 これに `Inactive` より、Amazon の販売が一時停止されます。 いつ `Active` でもアクティブ化する前に、販売収益と追加設定が更新されるようになります。<br>*[!UICONTROL Last Updated]* Amazon store の設定に最後に変更した日付です。<br>*[!UICONTROL Created]* Amazon store が amazon sales チャネルで作成された日付。 |
| 中央のセクション | には、過去30日間のストアの利用状況に関するチャートが含まれています。これには、注意が必要な出展が含まれています。 |
| 下部セクション | ビューストアとアクションオプションが含まれています。<br>ストアのダッシュボードを開くには [ ](./amazon-store-dashboard.md) 、をクリックし **[!UICONTROL View Store]** ます。<br>ストアをアクティブ化、非アクティブ化、または削除するには、をクリックし **[!UICONTROL Actions]** ます。 |
