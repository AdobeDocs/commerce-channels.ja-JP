---
title: 不完全なAmazonの一覧
description: Amazon セールスチャネルには、不完全なAmazon リストの実施要件を特定して満たすのに役立つ「[!UICONTROL Incomplete]」タブが用意されています。
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# 不完全なAmazonの一覧

「_[!UICONTROL Incomplete]_」タブには、Amazonの実施要件（[ リストルール ](./listing-rules.md) で定義）を満たしているが、Amazonで必要な情報（Amazon ASIN や定義済みの商品条件など）が欠落している [!DNL Commerce] カタログ商品が一覧表示されます。

不完全なリストには 4 つの原因が考えられ、それぞれがステータスによって識別されます。

| ステータス | 理由 | アクション |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 条件がありません | Amazonでは、様々な条件（_新規_、_再生済み_、_使用中：新規など_）のリストを使用できます。リストには定義済みの条件が必要です。 | 必須情報を更新し、リストに手動で [ 条件を割り当て ](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) ます。 |
| Amazon リストに割り当てることができない | このリストとカタログの自動照合に失敗しました。 一致するものが見つからない場合、Amazon Sales Channelではリストを管理できません | 必要な情報を更新し、カタログ製品に手動で [ASIN を割り当て ](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) て、リストとの照合を行います。 |
| 複数の一致が見つかりました | このリストとカタログの自動照合に失敗しました。 一致する可能性のあるものが複数見つかった場合は、製品に対して正しい一致を選択する必要があります。 | 製品およびリストに関して、必要な情報を更新し、手動で [ 製品の一致を選択 ](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) します。 |
| バリアントあり | 商品に様々なサイズや色の T シャツなどのバリエーションがある場合、カタログでそのバリエーションを選択して、正しく割り当てリストに一致させる必要があります | 必要な情報を更新し、手動で [ 正しいバリアントを選択 ](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) して、このリストに割り当てて一致させます。 |

>[!NOTE]
>不完全なリストがカタログ商品に正しく一致すると、リストは「_[!UICONTROL Incomplete]_」タブから移動し、[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 定した設定に基づいてAmazonに公開されます。

「_[!UICONTROL Incomplete]_」タブで使用できるアクションは次のとおりです。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Amazonのリストデータを [!DNL Commerce] カタログに一致させるための自動プロセスを開始します。 製品が自動的に一致しない場合は、リストのレッティングで [_[!UICONTROL Catalog Search]_](./catalog-search.md) のオプションを再確認します。 _[!UICONTROL Catalog Search]_のオプションを更新した後、リストが自動的に一致しない場合は、[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) のアクションで製品を手動で一致させることができます。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL Update Required Info]**：一覧がカタログと自動的に一致しない場合に選択します。 カタログ製品を手動で [ リストに一致させる ](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)、カタログの一致に手動で [ASIN を割り当てる ](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)、またはリストに対して [ 見つからない条件を割り当てる ](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) を実行できます。

- **[!UICONTROL View Details]**: [ リスト活動ログ ](./product-listing-details.md#listing-activity-log)、[Buy Box競合他社価格 ](./product-listing-details.md#buy-box-competitor-pricing)、および [ 最低競合他社価格 ](./product-listing-details.md#lowest-competitor-pricing) を含むリスト詳細を表示します。 このアクションは表示専用です。 リストの詳細は変更できません。 [ 詳細を表示 ](./product-listing-details.md) を参照してください。

>[!NOTE]
>
>処理中のリストがある場合、リストの数はタブの上のメッセージに表示されます。

![ 不完全なAmazonの一覧 ](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Amazon sales channel のホームページには、表示するデータをカスタマイズできる共通の [workspace コントロール ](./workspace-controls.md) がいくつか用意されています。

| 列 | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 商品、オプション、価格、製造元を識別するためにAmazonによって商品に割り当てられた SKU （最小在庫管理単位）。 |
| [!UICONTROL ASIN] | 項目を識別する 10 文字または数字、あるいはその両方の一意のブロック。<br><br>ASIN は [!DNL Amazon Standard Identification Number] を表す。 ASIN は、項目を識別する 10 文字または数字（あるいはその両方）で構成される一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合、カタログにアイテムがアップロードされると新しい ASIN が作成されます。 Amazonの商品詳細ページで、商品に関する詳細と共に商品 ASIN を見つけることができます。 |
| [!UICONTROL Product Listing Name] | 商品の名前。 |
| [!UICONTROL Condition] | 商品の [ 条件 ](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその出荷価格。 |
| [!UICONTROL Amazon Quantity] | 商品がAmazonにアクティブに一覧表示されている場合に利用できる数量。 |
| [!UICONTROL Status] | Amazonで定義される、リストのステータス。 前述のステータステーブルを参照してください。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、オプションを選択します。<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
