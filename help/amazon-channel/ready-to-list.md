---
title: リストの準備ができました
description: Amazon 販売チャンネルの「リストへ」タブでは、受給条件を満たすが、自動的に一覧に表示されない Commerce 製品を確認することができます。
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

このタブには、 _[!UICONTROL Ready to List]_[!DNL Commerce] リスティング設定に適合し、Amazon に新しい出展情報としてパブリッシュする準備ができたカタログ製品が表示され&#x200B;****ます。 他のリストタブとは異なり、このタブはページに必ずしも表示されるわけではありません [_[!UICONTROL Product Listings]_](./managing-product-listings.md) 。

この _[!UICONTROL Ready to List]_タブは、 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) リスティング設定がに設定されている場合にのみ表示され `Do Not Automatically List Eligible Products` ます。 この設定によって、Amazon 販売チャンネルについて、新しい Amazon リストを手動で公開する必要があることが通知されます。

[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)がに設定されていると `Automatically List Eligible Products` 、Amazon 販売チャンネルは、対象となるカタログ製品の新しい一覧を自動的に公開します。新しいリストは自動的に公開されるので、この _[!UICONTROL Ready to List]_タブは表示されません。

_[!UICONTROL Actions]_以下に示します。

- **[!UICONTROL Publish Product to Amazon]**: リストをに再パブリッシュすることを選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リストの公開」を参照してください。](./publish-listings-manually.md)

**[!UICONTROL Select]**&#x200B;列で、 _[!UICONTROL Action]_次のようになります。

- **[!UICONTROL Publish On Amazon]**: リストをに再パブリッシュすることを選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リスティングのパブリッシュ」を参照してください ](./publish-listings-manually.md) 。

- **[!UICONTROL View Details]**: 一覧表示された [ 利用状況ログ、購入ボックスの価格、競合企業の価格が表示さ ](./product-listing-details.md#listing-activity-log) [ ](./product-listing-details.md#buy-box-competitor-pricing) [ ](./product-listing-details.md#lowest-competitor-pricing) れます。 このアクションは、表示専用です。 一覧の詳細に変更を加えることはできません。 [詳しくは、詳細の表示を参照してください ](./product-listing-details.md) 。

Amazon に新しい一覧を手動でパブリッシュするには、いくつかの方法があり [ ](./publish-listings-manually.md) ます。

>[!NOTE]
>リストが作成されている場合は、タブの上のメッセージに一覧の数が表示されます。

![リストの準備ができました](assets/amazon-ready-to-list.png)

## デフォルトの列

| 段 | つい |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>「アーク」は、 [!DNL Amazon Standard Identification Number] . アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Condition] | [ ](./product-listing-condition.md) 製品の状態。 |
| [!UICONTROL Landed Price] | 製品のリスト価格とその配送価格を示します。 |
| [!UICONTROL Amazon Quantity] | この製品が Amazon に積極的に一覧表示されるときに使用可能な数量です。 |
| [!UICONTROL Status] | Amazon によって定義される一覧の状態。 |
| [!UICONTROL Action] | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、列内をクリックし、次のいずれ **[!UICONTROL Select]** _[!UICONTROL Action]_かのオプションを選択します。<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### リスト一覧表示の一般的な原因

- **[!UICONTROL Ready to List]** -製品が Amazon アークに適合し、リストの掲載が予定されています。 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)リスティング設定がに設定されている場合は `Do Not Automatically List Eligible Products` 、手動で一覧表示する準備ができている製品がこの状態になります。

- **[!UICONTROL List in Progress]** -製品リストが Amazon に送信され、Amazon からの受諾を確認することができます。
