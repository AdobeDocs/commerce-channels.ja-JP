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

この _[!UICONTROL Ready to List]_タブには、が表示されます [!DNL Commerce] リスト設定を満たし、Amazon as a に公開する準備ができている製品のカタログ&#x200B;**新規**リスト。 他のリストタブとは異なり、このタブは常に [_[!UICONTROL Product Listings]_](./managing-product-listings.md) ページ。

この _[!UICONTROL Ready to List]_タブが表示されるのは、 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) リストの設定はに設定されています。 `Do Not Automatically List Eligible Products`. この設定は、新しいAmazonの一覧を手動で公開する必要があることをAmazonの営業チャネルに伝えます。

条件 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) はに設定されています。 `Automatically List Eligible Products`を選択すると、Amazonセールスチャネルは、対象となるカタログ商品の新しいリストを自動的に公開します。 新しい一覧は自動的に公開されるため、 _[!UICONTROL Ready to List]_タブは表示されません。

次の下 _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**：リストの再公開を以下に選択します [!DNL Amazon Marketplace]. 参照： [Amazon リストの公開](./publish-listings-manually.md)

次の下 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列：

- **[!UICONTROL Publish On Amazon]**：リストの再公開を以下に選択します [!DNL Amazon Marketplace]. 参照： [Amazon リストの公開](./publish-listings-manually.md).

- **[!UICONTROL View Details]**：次のようなリストの詳細を表示することを選択します [アクティビティログを一覧表示](./product-listing-details.md#listing-activity-log), [Buy Box競合他社価格](./product-listing-details.md#buy-box-competitor-pricing)、および [競合製品の最低価格](./product-listing-details.md#lowest-competitor-pricing). このアクションは表示専用です。 リストの詳細は変更できません。 参照： [詳細を表示](./product-listing-details.md).

手動でいくつかのオプションがあります [Amazonへの新しいリストの公開](./publish-listings-manually.md).

>[!NOTE]
>処理中のリストがある場合、リスト数はタブの上のメッセージに表示されます。

![リストの準備完了](assets/amazon-ready-to-list.png){width="600" zoomable="yes"}

## デフォルトの列

| 列 | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は AEM を表す [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | この [条件](./product-listing-condition.md) 商品の。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列を選択してオプションを選択します。<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### リストへの準備完了リストの一般的な原因

- **[!UICONTROL Ready to List]**  – 商品はAmazon ASIN と照合され、リストに登録される予定です。 次の場合 [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) リストの設定はに設定されています。 `Do Not Automatically List Eligible Products`、このステータスは、手動でリストする準備ができた製品を表します。

- **[!UICONTROL List in Progress]**  – 商品リストがAmazonに送信され、Amazonからの承認の確認待ちです。
