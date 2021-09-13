---
title: リストへの準備完了
description: Amazonのセールスチャネルには、適格性を満たすが自動的にはリストされないコマース製品を確認するのに役立つ「リストに準備完了」タブが用意されています。
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

「_[!UICONTROL Ready to List]_」タブには、リスト設定を満たし、**新しい**リストとしてAmazonに公開する準備が整った、[!DNL Commerce]カタログ製品が表示されます。 他のリストタブとは異なり、このタブは[_[!UICONTROL Product Listings]_](./managing-product-listings.md)ページに常に表示されるわけではありません。

「_[!UICONTROL Ready to List]_」タブは、リスト設定の[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)が`Do Not Automatically List Eligible Products`に設定されている場合にのみ表示されます。 この設定は、新しいAmazonリストを手動で公開する必要があることをAmazonの販売チャネルに伝えます。

[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)を`Automatically List Eligible Products`に設定すると、Amazonの販売チャネルは適格なカタログ製品の新しいリストを自動的に公開します。 新しいリストは自動的に公開されるので、「_[!UICONTROL Ready to List]_」タブは表示されません。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Publish Product to Amazon]**:リストをに再公開する場合に選択しま [!DNL Amazon Marketplace]す。[Amazonリストの公開](./publish-listings-manually.md)を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL Publish On Amazon]**:リストをに再公開する場合に選択しま [!DNL Amazon Marketplace]す。[Amazonリストの公開](./publish-listings-manually.md)を参照してください。

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

新しいリストを手動で[Amazon](./publish-listings-manually.md)に公開する方法はいくつかあります。

>[!NOTE]
>リストが処理中の場合は、リストの数がタブの上にあるメッセージに表示されます。

![リストへの登録準備完了](assets/amazon-ready-to-list.png)

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格と送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた場合に使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス(Amazonで定義)。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### リストの準備完了の一般的な原因

- **[!UICONTROL Ready to List]**  — 製品はAmazon ASINに一致し、リストに登録される予定です。リスト設定で[**[!UICONTROL Automatic List Action]**](./product-listing-actions.md)が`Do Not Automatically List Eligible Products`に設定されている場合、このステータスは手動でリストする準備ができた製品を表します。

- **[!UICONTROL List in Progress]**  — 製品リストはAmazonに送信され、Amazonからの受け入れの確認を待機中です。
