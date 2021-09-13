---
title: アクティブなリスト
description: Amazonのセールスチャネルには、アクティブなAmazonリストを監視する「アクティブ」タブがあり、Adobeコマースカタログ内の製品と一致します。
exl-id: c9105abc-74d6-442b-8d7a-e5aaea8872e4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# アクティブなリスト

「_[!UICONTROL Active]_」タブには、[!DNL Amazon Marketplace]でアクティブで、[!DNL Commerce]カタログ内の製品と一致するAmazonリストが表示されます。

「_[!UICONTROL Active]_」タブで使用できるアクションは次のとおりです。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL End Listing(s) on Amazon]**:選択したリストをからすべて削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

- **[!UICONTROL Edit Listing Overrides]**:を選択して、リストの上書き設定を変更します。[上書き](./overrides.md)または[上書き](./creating-editing-overrides.md#edit-override-single-listing)の編集または削除を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

- **[!UICONTROL Create Override]**：上書きを作成してこのリストに適用する場合に選択します。[上書きの作成](./creating-editing-overrides.md)を参照してください。

- **[!UICONTROL Edit Assigned ASIN]**：カタログ製品に割り当てられたASINを変更する場合に選択します。カタログ内の製品が誤ったASINと一致する場合は、このアクションを使用します。 [割り当てられたASINの編集](./edit-assigned-asin.md)を参照してください。

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ製品からAmazonリストを作成するために使用できるAlias SKUを作成する場合に選択します。[AliasセラーのSKU](./create-alias-seller-sku.md)の作成を参照してください。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：受注に関連付けられた履行方法を変更する場合に選択します。[「満たされたユーザーの設定](./fulfilled-by.md#configure-fulfilled-by-settings)」を参照してください。

- **[!UICONTROL End Listing]**:「 」を選択して、からリストを削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

>[!NOTE]
>
>リストが処理中の場合は、タブの上にあるメッセージにリスト数が表示されます。

![アクティブなリスト](assets/amazon-active-listings.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。 <br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格と送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた後に使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス(Amazonで定義)。 |
| [!UICONTROL Buy Box Won] | 製品リストが[Buy Box](./buy-box-competitor-pricing.md)の位置を獲得したかどうか。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックしてオプションを表示します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
