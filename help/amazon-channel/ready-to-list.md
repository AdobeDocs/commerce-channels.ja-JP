---
title: Amazon販売チャネル - [!UICONTROL Ready to List]
description: Amazon セールスチャネルには「リストに準備完了」タブが用意されており、適格要件を満たしているが自動的にはリストに登録されないCommerce製品を確認するのに役立ちます。
feature: Sales Channels, Products, Merchandising
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

「_[!UICONTROL Ready to List]_」タブには、リスト設定を満たし、（新規&#x200B;**リストとしてAmazonに公開する準備が整った [!DNL Commerce] カタログ商品が表示**れます。 他のリストタブとは異なり、このタブは必ずしも [_[!UICONTROL Product Listings]_](./managing-product-listings.md) ページに表示されるわけではありません。

「_[!UICONTROL Ready to List]_」タブは、リスト設定の [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) が `Do Not Automatically List Eligible Products` に設定されている場合にのみ表示されます。 この設定は、新しいAmazonの一覧を手動で公開する必要があることをAmazonの営業チャネルに伝えます。

[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) を `Automatically List Eligible Products` に設定すると、Amazon sales channel は対象となるカタログ商品の新しいリストを自動的に公開します。 新しい一覧は自動的に公開されるため、[_[!UICONTROL Ready to List]_] タブは表示されません。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Publish Product to Amazon]**: リストを [!DNL Amazon Marketplace] に再公開することを選択します。 [PublishとAmazonのリストを参照してください ](./publish-listings-manually.md)

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL Publish On Amazon]**: リストを [!DNL Amazon Marketplace] に再公開することを選択します。 [Publish an Amazonのリスト ](./publish-listings-manually.md) を参照してください。

- **[!UICONTROL View Details]**: [ リスト活動ログ ](./product-listing-details.md#listing-activity-log)、[Buy Box競合他社価格 ](./product-listing-details.md#buy-box-competitor-pricing)、および [ 最低競合他社価格 ](./product-listing-details.md#lowest-competitor-pricing) を含むリスト詳細を表示します。 このアクションは表示専用です。 リストの詳細は変更できません。 [ 詳細を表示 ](./product-listing-details.md) を参照してください。

手動で [ 新しいリストをAmazonに公開する ](./publish-listings-manually.md) 方法はいくつかあります。

>[!NOTE]
>処理中のリストがある場合、リスト数はタブの上のメッセージに表示されます。

![ リストへの準備完了 ](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## デフォルトの列

| 列 | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は [!DNL Amazon Standard Identification Number] を表す。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | 商品の [ 条件 ](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、オプションを選択します。<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### リストへの準備完了リストの一般的な原因

- **[!UICONTROL Ready to List]** – 商品がAmazon ASIN と照合され、リストに登録される予定です。 リスト設定の [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) が `Do Not Automatically List Eligible Products` に設定されている場合、このステータスは、手動でリストする準備が整った製品を表します。

- **[!UICONTROL List in Progress]** – 商品リストがAmazonに送信され、Amazonからの承認の確認待ちです。
