---
title: 不適合リスト
description: Amazon 販売チャンネルのタブには、アイテムを管理するための [!UICONTROL Ineligible] タブが表示されます。これは、現在のリストルールに基づいたリストの対象にはなりません。
exl-id: ae63898d-ff5c-43eb-b759-5bc80829d4d4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 不適合リスト

このタブには、 _[!UICONTROL Ineligible]_Amazon に現在パブリッシュされているすべての製品の一覧が表示されますが、現在のリスティングルールに基づくリストとしては使用できません。 前の製品が条件に適合し、リストルールが適用されていない場合は、その製品に関連付けられた量が0になり、製品が対象外とマークされ_ _ます。 ただし、はに表示され [!DNL Amazon Seller Account] ます。

タブの外に製品を移動するには _[!UICONTROL Ineligible]_、 [ ](./listing-rules.md) 対象となる製品が表示されるようにリストルールを変更することができます。

タブに表示されるアクションは以下のとおり _[!UICONTROL Ineligible]_です。

_[!UICONTROL Actions]_以下に示します。

- **[!UICONTROL End Listing(s) on Amazon]**: 選択したすべてのリストをから削除することを選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リスティングの終了」を参照してください ](./end-listings-manually.md) 。

- **[!UICONTROL Edit Listing Overrides]**: リストの上書き設定を変更するかどうかを選択します。 [ ](./overrides.md) [ 上書き、編集、または削除を参照してください ](./creating-editing-overrides.md#edit-override-single-listing) 。

**[!UICONTROL Select]**&#x200B;列で、 _[!UICONTROL Action]_次のようになります。

- **[!UICONTROL View Details]**: 一覧表示された [ 利用状況ログ、購入ボックスの価格、競合企業の価格が表示さ ](./product-listing-details.md#listing-activity-log) [ ](./product-listing-details.md#buy-box-competitor-pricing) [ ](./product-listing-details.md#lowest-competitor-pricing) れます。 このアクションは、表示専用です。 一覧の詳細に変更を加えることはできません。 [詳しくは、詳細の表示を参照してください ](./product-listing-details.md) 。

- **[!UICONTROL Create Override]**: 上書きを作成して、このリストに適用することを選択します。 上書きの作成を参照してください [ ](./creating-editing-overrides.md) 。

- **[!UICONTROL Edit Assigned ASIN]**△: カタログ製品に割り当てられたアークサインを変更する場合に選択します。 このアクションは、カタログ内の製品が間違ったアークサインに一致した場合に使用されます。 [割り当てられたサインの編集を参照してください ](./edit-assigned-asin.md) 。

- **[!UICONTROL Create Alias Seller SKU]**: 同じカタログ製品から Amazon リストを作成するために使用できるエイリアス SKU を作成することを選択します。 販売担当者 [ SKU の作成を参照してください ](./create-alias-seller-sku.md) 。

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: 注文に関連付けられたフルフィルメント方法を変更する場合に選択します。 「 [ 設定によるフルフィルメントの設定」を参照してください ](./fulfilled-by.md#configure-fulfilled-by-settings) 。

- **[!UICONTROL End Listing]**: リストをから削除するように選択し [!DNL Amazon Marketplace] ます。 「 [ Amazon リスティングの終了」を参照してください ](./end-listings-manually.md) 。

>[!NOTE]
>リストが作成されている場合は、タブの上のメッセージに一覧の数が表示されます。

![不適格となる Amazon リスト](assets/amazon-ineligible-listings.png)

Amazon セールスチャンネルのホームページ [ ](./workspace-controls.md) は、表示されるデータをカスタマイズするための一般的なワークスペースコントロールの一部を共有しています。

## デフォルトの列

| 段 | つい |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>「アーク」は、 [!DNL Amazon Standard Identification Number] . アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Condition] | [ ](./product-listing-condition.md) 製品の状態。 |
| [!UICONTROL Landed Price] | 製品のリスト価格とその配送価格を示します。 |
| [!UICONTROL Amazon Quantity] | この製品が Amazon に積極的に一覧表示されるときに使用可能な数量です。 |
| [!UICONTROL Action] | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、列内をクリックし、 **[!UICONTROL Select]** _[!UICONTROL Action]_オプションを選択します。<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[上書きの作成](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
