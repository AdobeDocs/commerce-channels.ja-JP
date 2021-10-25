---
title: 不完全な一覧
description: Amazon sales channel タブは、 [!UICONTROL Incomplete] 不完全な Amazon リストに使用される特典を確認し、条件を満たすために役立ちます。
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# 不完全な一覧

このタブには、amazon の _[!UICONTROL Incomplete]_[!DNL Commerce] 資格情報 (リストルールで定義されています) に適合するカタログ製品が一覧表示 [ されますが、amazon ](./listing-rules.md) によって要求される情報が不足しています (amazon または定義された製品条件など)。

不完全なリストについては、それぞれの状態によって識別される4つの原因が考えられます。

| 現状 | ため | アクション |
|--- |--- |--- |
| 条件がありません | Amazon は、様々な条件でリストを __ 使用できます (新規、新機能 __ 、 _使用: 新機能など)。リストに_ は条件が定義されている必要があります。 | 必要な情報を更新し、 [ リストに手動で条件を割り当て ](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) ます。 |
| Amazon の一覧に割り当てられることができません | この一覧のカタログへの自動的な一致は失敗しました。 一致するものが見つからない場合は、リストを Amazon Sales Channel によって管理することはできません。 | 必要な情報を更新し、リストと一致させるために手動で [ ](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) 差し込み製品に &quot;アーク」を割り当てます。 |
| 複数の一致が見つかりました | この一覧のカタログへの自動的な一致は失敗しました。 一致するアイテムが複数見つかった場合は、製品に適したものを選択する必要があります。 | 必要な情報を更新し、製品 [ とリストに一致する製品を選択し ](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) ます。 |
| バリアントが含まれます | 使用する製品に、サイズや色の異なる t シャツなどのバリエーションが含まれている場合は、カタログ内の変形を選択して、そのバリエーションが表示されます。 | 必要な情報を更新し、手動で [ ](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) 指定して、このリストと一致させます。 |

>[!NOTE]
>カタログ製品に不完全な一覧が表示されると、その一覧はタブから移動し、 _[!UICONTROL Incomplete]_設定に基づいて Amazon に公開され [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) ます。

タブに表示されるアクションは以下のとおり _[!UICONTROL Incomplete]_です。

_[!UICONTROL Actions]_以下に示します。

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Amazon リストデータをカタログに一致させるための自動プロセスを開始するように選択し [!DNL Commerce] ます。 製品が自動的に一致しない場合は、リスト lettings に表示されているオプションを再利用 [_[!UICONTROL Catalog Search]_](./catalog-search.md) してください。 オプションを更新した後に一覧が自動的に一致しない場合は _[!UICONTROL Catalog Search]_、そのアクションに手動で製品を適合させることができ [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) ます。

**[!UICONTROL Select]**&#x200B;列で、 _[!UICONTROL Action]_次のようになります。

- **[!UICONTROL Update Required Info]**: リストが自動的にカタログに一致しない場合に選択します。 カタログ製品を一覧に手動で対応させることができ [ ます。また、電話帳に手動で電話をかけることができ ](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) [ ](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) [ ます。また、見つからない条件をリストに割り当てることもでき ](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) ます。

- **[!UICONTROL View Details]**: 一覧表示された [ 利用状況ログ、購入ボックスの価格、競合企業の価格が表示さ ](./product-listing-details.md#listing-activity-log) [ ](./product-listing-details.md#buy-box-competitor-pricing) [ ](./product-listing-details.md#lowest-competitor-pricing) れます。 このアクションは、表示専用です。 一覧の詳細に変更を加えることはできません。 [詳しくは、詳細の表示を参照してください ](./product-listing-details.md) 。

>[!NOTE]
>
>リストが作成されている場合は、タブの上のメッセージに一覧の数が表示されます。

![不完全な Amazon リスト](assets/amazon-incomplete-listings.png)

Amazon セールスチャンネルのホームページ [ ](./workspace-controls.md) は、表示されるデータをカスタマイズするための一般的なワークスペースコントロールの一部を共有しています。

| 段 | つい |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>「アーク」は、 [!DNL Amazon Standard Identification Number] . アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Condition] | [ ](./product-listing-condition.md) 製品の状態。 |
| [!UICONTROL Landed Price] | 製品のリスト価格とその配送価格を示します。 |
| [!UICONTROL Amazon Quantity] | この製品が Amazon に積極的に一覧表示されるときに使用可能な数量です。 |
| [!UICONTROL Status] | Amazon によって定義される一覧の状態。 上の状態テーブルを参照してください。 |
| [!UICONTROL Action] | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、列内をクリックし、 **[!UICONTROL Select]** _[!UICONTROL Action]_オプションを選択します。<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
