---
title: 非アクティブなAmazon リスト
description: Amazon セールスチャネルには、現在アクティブでないリストを監視するための「[!UICONTROL Inactive]」タ  [!DNL Amazon Marketplace]  が用意されています。
feature: Sales Channels, Products
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 非アクティブなAmazon リスト

「_[!UICONTROL Inactive]_」タブには、Amazonに公開されているが [!DNL Amazon Marketplace] ージ上でアクティブになっていない商品が表示されます。 リストは、いくつかの異なる理由で非アクティブになっている可能性があります。 例えば、その特定のブランドをリストする資格がない可能性があります。 非アクティブなリストは、Amazonのリスト標準規格と [!DNL Amazon Seller Central] アカウントの権限によって決まります。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL End Listing(s) on Amazon]**：選択したすべての一覧を [!DNL Amazon Marketplace] から削除します。 [Amazon リストの終了 ](./end-listings-manually.md) を参照してください。

- **[!UICONTROL Edit Listing Overrides]**: リストの優先設定の変更を選択します。 [ オーバーライド ](./overrides.md) または [ オーバーライドの編集または削除 ](./creating-editing-overrides.md#edit-override-single-listing) を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL View Details]**: [ リスト活動ログ ](./product-listing-details.md#listing-activity-log)、[Buy Box競合他社価格 ](./product-listing-details.md#buy-box-competitor-pricing)、および [ 最低競合他社価格 ](./product-listing-details.md#lowest-competitor-pricing) を含むリスト詳細を表示します。 このアクションは表示専用です。 リストの詳細は変更できません。 [ 詳細を表示 ](./product-listing-details.md) を参照してください。

- **[!UICONTROL Create Override]**：上書きを作成し、このリストに適用することを選択します。 [ 上書きの作成 ](./creating-editing-overrides.md) を参照してください。

- **[!UICONTROL Edit Assigned ASIN]**: カタログ製品に割り当てられた ASIN を変更します。 このアクションは、カタログ内の製品が誤った ASIN と一致した場合に使用されます。 [ 割り当てられた ASIN の編集 ](./edit-assigned-asin.md) を参照してください。

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ商品からAmazon リストを作成するために使用できるエイリアス SKU （Stock Keeping Unit）を作成することを選択します。 [Alias Seller SKU の作成 ](./create-alias-seller-sku.md) を参照してください。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：受注に関連付けられた履行方法の変更を選択します。 [ フルフィルメントの指定方法 ](./fulfilled-by.md#configure-fulfilled-by-settings) を参照してください。

- **[!UICONTROL End Listing]**: リストからリストを削除することを選択し [!DNL Amazon Marketplace] す。 [Amazon リストの終了 ](./end-listings-manually.md) を参照してください。

>[!NOTE]
>
>処理中のリストがある場合は、タブの上に、リスト数を示すメッセージが表示されます。

![ 非アクティブなAmazonの一覧 ](assets/amazon-inactive-listings.png){width="600" zoomable="yes"}

Amazon sales channel のホームページには、表示するデータをカスタマイズできる共通の [workspace コントロール ](./workspace-controls.md) がいくつか用意されています。

| 列 | 説明 |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は、Amazonの標準識別番号を表します。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | 商品の [ 条件 ](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazonには、非アクティブなリストの理由が必ずしも表示されるわけではありません。リストの問題を解決するには、カスタマーサポートにお問い合わせください。 場合によっては、Amazonから理由が通知されます。 これらの応答を表示するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL View Details]**をクリックします。 これらの問題が解決され、Amazonによってエラーが削除されると、商品は「_[!UICONTROL Active]_」タブに移動します。 |
| アクション | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、オプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
