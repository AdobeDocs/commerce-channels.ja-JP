---
title: 不適格なリスト
description: Amazonのセールスチャネルには、現在のリストルールに基づくリストとして項目を管理するのに役立つ「[!UICONTROL Ineligible]」タブが用意されています。
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 不適格なリスト

「 _[!UICONTROL Ineligible]_」タブには、現在Amazonで公開されているが、現在のリストルールに基づくリストとして使用できないすべての製品のリストが表示されます。 以前の製品が適格で、リストルールが変更されて不適格となった場合、製品に関連付けられた数量は0になり、製品は_ ineligible _とマークされます。 ただし、[!DNL Amazon Seller Account]にはまだ存在します。

_[!UICONTROL Ineligible]_タブから製品を移動するには、[リストルール](./listing-rules.md)を変更して、製品の実施要件を満たすようにします。

「_[!UICONTROL Ineligible]_」タブで使用できるアクションは次のとおりです。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL End Listing(s) on Amazon]**:選択したリストをからすべて削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

- **[!UICONTROL Edit Listing Overrides]**:を選択して、リストの上書き設定を変更します。[上書き](./overrides.md)または[上書き](./creating-editing-overrides.md#edit-override-single-listing)の編集または削除を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

- **[!UICONTROL Create Override]**：上書きを作成してこのリストに適用する場合に選択します。[上書きの作成](./creating-editing-overrides.md)を参照してください。

- **[!UICONTROL Edit Assigned ASIN]**：カタログ製品に割り当てられたASINを変更する場合に選択します。このアクションは、カタログ内の製品が誤ったASINと一致した場合に使用されます。 [割り当てられたASINの編集](./edit-assigned-asin.md)を参照してください。

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ製品からAmazonリストを作成するために使用できるAlias SKUを作成する場合に選択します。[AliasセラーのSKU](./create-alias-seller-sku.md)の作成を参照してください。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：受注に関連付けられた履行方法を変更する場合に選択します。[「満たされたユーザーの設定](./fulfilled-by.md#configure-fulfilled-by-settings)」を参照してください。

- **[!UICONTROL End Listing]**:「 」を選択して、からリストを削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

>[!NOTE]
>リストが処理中の場合は、タブの上にあるメッセージにリスト数が表示されます。

![不適格なAmazon一覧](assets/amazon-ineligible-listings.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

## デフォルトの列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格と送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた場合に使用可能な数量。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[上書きを作成](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
