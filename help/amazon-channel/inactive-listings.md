---
title: 非アクティブなリスト
description: Amazonの販売チャネルには、現在非アクティブな [!DNL Amazon Marketplace] リストを監視する「[!UICONTROL Inactive]」タブが用意されています。
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 非アクティブなリスト

「_[!UICONTROL Inactive]_」タブには、Amazonに公開されたが[!DNL Amazon Marketplace]でアクティブでない製品が表示されます。 リストは、いくつかの理由で非アクティブになる可能性があります。 例えば、特定のブランドをリストする資格がない場合があります。 非アクティブなリストは、Amazonのリスト標準と[!DNL Amazon Seller Central]アカウントの権限によって決まります。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL End Listing(s) on Amazon]**:選択したリストをからすべて削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

- **[!UICONTROL Edit Listing Overrides]**:を選択して、リストの上書き設定を変更します。[上書き](./overrides.md)または[上書き](./creating-editing-overrides.md#edit-override-single-listing)の編集または削除を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

- **[!UICONTROL Create Override]**：上書きを作成してこのリストに適用する場合に選択します。[上書きの作成](./creating-editing-overrides.md)を参照してください。

- **[!UICONTROL Edit Assigned ASIN]**：カタログ製品に割り当てられたASINを変更する場合に選択します。このアクションは、カタログ内の製品が誤ったASINと一致した場合に使用されます。 [割り当てられたASINの編集](./edit-assigned-asin.md)を参照してください。

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ製品からAmazonリストを作成するために使用できるエイリアスSKU（在庫管理単位）を作成する場合に選択します。[AliasセラーのSKU](./create-alias-seller-sku.md)の作成を参照してください。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：受注に関連付けられた履行方法を変更する場合に選択します。[「満たされたユーザーの設定](./fulfilled-by.md#configure-fulfilled-by-settings)」を参照してください。

- **[!UICONTROL End Listing]**:「 」を選択して、からリストを削除しま [!DNL Amazon Marketplace]す。[Amazonリストの終了](./end-listings-manually.md)を参照してください。

>[!NOTE]
>
>処理中のリストがある場合、タブの上にメッセージが表示され、リストの数が示されます。

![非アクティブなAmazonの一覧](assets/amazon-inactive-listings.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、Amazon Standard Identification Numberの略です。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格と送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた場合に使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス(Amazonで定義)。 |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazonは、必ずしも非アクティブなリストの理由を提供しているわけではなく、カスタマーサポートに連絡してリストの問題を解決することができます。 場合によっては、Amazonから理由が通知されることがあります。 これらの回答を表示するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL View Details]**をクリックします。 これらの問題が解決され、Amazonがエラーを取り除くと、製品は「_[!UICONTROL Active]_」タブに移動します。 |
| アクション | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、次のオプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
