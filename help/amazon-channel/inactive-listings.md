---
title: 非アクティブな一覧
description: Amazon sales channel タブには、 [!UICONTROL Inactive] 現在使用されていないリストが表示され  [!DNL Amazon Marketplace]  ます。
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 非アクティブな一覧

このタブには、 _[!UICONTROL Inactive]_Amazon に公開されてもアクティブではない製品が表示され [!DNL Amazon Marketplace] ます。 リストが非アクティブになる理由はいくつか考えられます。 例えば、特定のブランドのリストを作成することはできません。 非アクティブな番組は、Amazon のリスティング規格およびアカウントのアクセス許可によって決まり [!DNL Amazon Seller Central] ます。

_[!UICONTROL Actions]_以下に示します。

- **[!UICONTROL End Listing(s) on Amazon]**: 選択したすべてのリストをから削除することを選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リスティングの終了」を参照してください ](./end-listings-manually.md) 。

- **[!UICONTROL Edit Listing Overrides]**: リストの上書き設定を変更するかどうかを選択します。 [ ](./overrides.md) [ 上書き、編集、または削除を参照してください ](./creating-editing-overrides.md#edit-override-single-listing) 。

**[!UICONTROL Select]**&#x200B;列で、 _[!UICONTROL Action]_次のようになります。

- **[!UICONTROL View Details]**: 一覧表示された [ 利用状況ログ、購入ボックスの価格、競合企業の価格が表示さ ](./product-listing-details.md#listing-activity-log) [ ](./product-listing-details.md#buy-box-competitor-pricing) [ ](./product-listing-details.md#lowest-competitor-pricing) れます。 このアクションは、表示専用です。 一覧の詳細に変更を加えることはできません。 [詳しくは、詳細の表示を参照してください ](./product-listing-details.md) 。

- **[!UICONTROL Create Override]**: 上書きを作成して、このリストに適用することを選択します。 上書きの作成を参照してください [ ](./creating-editing-overrides.md) 。

- **[!UICONTROL Edit Assigned ASIN]**△: カタログ製品に割り当てられたアークサインを変更する場合に選択します。 このアクションは、カタログ内の製品が間違ったアークサインに一致した場合に使用されます。 [割り当てられたサインの編集を参照してください ](./edit-assigned-asin.md) 。

- **[!UICONTROL Create Alias Seller SKU]**: 同じカタログ製品から Amazon リストを作成するために使用できるエイリアス SKU (stock 保持ユニット) を作成することを選択します。 販売担当者 [ SKU の作成を参照してください ](./create-alias-seller-sku.md) 。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: 注文に関連付けられたフルフィルメント方法を変更する場合に選択します。 「 [ 設定によるフルフィルメントの設定」を参照してください ](./fulfilled-by.md#configure-fulfilled-by-settings) 。

- **[!UICONTROL End Listing]**: リストをから削除するように選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リスティングの終了」を参照してください ](./end-listings-manually.md) 。

>[!NOTE]
>
>リストが進行中の場合は、リストの数を示すタブの上にメッセージが表示されます。

![非アクティブな Amazon リスト](assets/amazon-inactive-listings.png)

Amazon セールスチャンネルのホームページ [ ](./workspace-controls.md) は、表示されるデータをカスタマイズするための一般的なワークスペースコントロールの一部を共有しています。

| 段 | つい |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>アークは、Amazon 標準の Id 番号を表します。 アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Condition] | [ ](./product-listing-condition.md) 製品の状態。 |
| [!UICONTROL Landed Price] | 製品のリスト価格とその配送価格を示します。 |
| [!UICONTROL Amazon Quantity] | この製品が Amazon に積極的に一覧表示されるときに使用可能な数量です。 |
| [!UICONTROL Status] | Amazon によって定義される一覧の状態。 |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazon では、無効な一覧が表示されるわけではありません。また、ユーザーサポートに連絡して、リストに関する問題を解決することもできます。 状況によっては、Amazon によって理由が通知されます。 このような応答を表示するには、列内をクリックし **[!UICONTROL View Details]** _[!UICONTROL Action]_ます。 このような問題が解決され、Amazon によってエラーが削除された場合は、製品はタブに移動し_[!UICONTROL Active]_ ます。 |
| アクション | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、列内をクリックし、 **[!UICONTROL Select]** _[!UICONTROL Action]_次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
