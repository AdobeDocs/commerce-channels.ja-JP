---
title: アクティブなAmazonの一覧
description: Amazonのセールスチャネルには、Adobe Commerce カタログ内の商品に一致したアクティブなAmazonのリストをモニタリングするための「アクティブ」タブが用意されています。
feature: Sales Channels, Products, Merchandising, Catalog Management
exl-id: c9105abc-74d6-442b-8d7a-e5aaea8872e4
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# アクティブなAmazonの一覧

_[!UICONTROL Active]_タブには、[!DNL Commerce] カタログ内の製品と一致した [!DNL Amazon Marketplace] ージのアクティブな一覧が表示されます。

「_[!UICONTROL Active]_」タブで使用できるアクションは次のとおりです。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL End Listing(s) on Amazon]**：選択したすべての一覧を [!DNL Amazon Marketplace] から削除します。 [Amazon リストの終了 ](./end-listings-manually.md) を参照してください。

- **[!UICONTROL Edit Listing Overrides]**: リストの優先設定の変更を選択します。 [ オーバーライド ](./overrides.md) または [ オーバーライドの編集または削除 ](./creating-editing-overrides.md#edit-override-single-listing) を参照してください。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL View Details]**: [ リスト活動ログ ](./product-listing-details.md#listing-activity-log)、[Buy Box競合他社価格 ](./product-listing-details.md#buy-box-competitor-pricing)、および [ 最低競合他社価格 ](./product-listing-details.md#lowest-competitor-pricing) を含むリスト詳細を表示します。 このアクションは表示専用です。 リストの詳細は変更できません。 [ 詳細を表示 ](./product-listing-details.md) を参照してください。

- **[!UICONTROL Create Override]**：上書きを作成し、このリストに適用することを選択します。 [ 上書きの作成 ](./creating-editing-overrides.md) を参照してください。

- **[!UICONTROL Edit Assigned ASIN]**: カタログ製品に割り当てられた ASIN を変更します。 カタログ内の製品が誤った ASIN と一致した場合に、このアクションを使用します。 [ 割り当てられた ASIN の編集 ](./edit-assigned-asin.md) を参照してください。

- **[!UICONTROL Create Alias Seller SKU]**：同じカタログ商品からAmazon リストを作成する際に使用できるエイリアス SKU を作成します。 [Alias Seller SKU の作成 ](./create-alias-seller-sku.md) を参照してください。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**：受注に関連付けられた履行方法の変更を選択します。 [ フルフィルメントの指定方法 ](./fulfilled-by.md#configure-fulfilled-by-settings) を参照してください。

- **[!UICONTROL End Listing]**: リストからリストを削除することを選択し [!DNL Amazon Marketplace] す。 [Amazon リストの終了 ](./end-listings-manually.md) を参照してください。

>[!NOTE]
>
>処理中のリストがある場合、リスト数はタブの上のメッセージに表示されます。

![ アクティブな一覧 ](assets/amazon-active-listings.png){width="700" zoomable="yes"}

Amazon sales channel のホームページには、表示するデータをカスタマイズできる共通の [workspace コントロール ](./workspace-controls.md) がいくつか用意されています。

| 列 | 説明 |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。 <br><br>ASIN は [!DNL Amazon Standard Identification Number] を表す。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | 商品の [ 条件 ](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブにリストされた後に利用可能な数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 |
| [!UICONTROL Buy Box Won] | 商品リストが [Buy Box](./buy-box-competitor-pricing.md) のポジションを獲得したかどうか。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックしてオプションを表示します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
