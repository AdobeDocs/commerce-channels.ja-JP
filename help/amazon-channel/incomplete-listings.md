---
title: 不完全なリスト
description: Amazonのセールスチャネルには、不完全なAmazonリストの実施要件を特定し、満たすのに役立つ「[!UICONTROL Incomplete]」タブが用意されています。
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# 不完全なリスト

「_[!UICONTROL Incomplete]_」タブには、Amazonの適格性要件（[リストルール](./listing-rules.md)で定義）を満たすが、Amazonで必要な情報(Amazon ASINや定義済みの製品条件など)が欠落しているカタログ製品が一覧表示されます。[!DNL Commerce]

リストが不完全な場合は、4つの原因が考えられます。それぞれがステータスによって識別されます。

| ステータス | 理由 | アクション |
|--- |--- |--- |
| 見つからない条件 | Amazonは、様々な条件（_新しい_、_改装済み_、_使用済みなど）でリストを受け入れます。「新規_」のように)リストには、定義済みの条件が必要です。 | 必要な情報を更新し、リストに条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)を手動で割り当てます。[ |
| Amazonリストに割り当てられない | このリストをカタログに自動的に一致させられませんでした。 一致が見つからない場合、リストはAmazonSales Channelで管理できません | 必要な情報を更新し、リストに一致するようにASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)をカタログ製品に手動で[割り当てます。 |
| 複数件の一致が見つかりました | このリストをカタログに自動的に一致させられませんでした。 一致する結果が複数見つかった場合は、製品に合った正しい一致を選択する必要があります。 | 必要な情報を更新し、製品とリストに対して[製品の一致](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)を手動で選択します。 |
| バリアントを含む | サイズや色が異なるTシャツなど、製品にバリエーションがある場合は、カタログ内のバリアントを正しく割り当ててリストに一致させるように選択する必要があります | 必要な情報を更新し、手動で[正しいバリアント](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants)を選択して、このリストに割り当て、一致させます。 |

>[!NOTE]
>不完全なリストがカタログ商品と正しく一致する場合、リストは「_[!UICONTROL Incomplete]_」タブから移動し、[_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)の設定に基づいてAmazonに公開されます。

「_[!UICONTROL Incomplete]_」タブで使用できるアクションは次のとおりです。

_[!UICONTROL Actions]_の下：

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**:Amazonリストのデータをカタログに照合する自動処理を開始する場合に選択 [!DNL Commerce] します。商品が自動的に一致しない場合は、リスト設定の[_[!UICONTROL Catalog Search]_](./catalog-search.md)オプションを再度選択してください。 _[!UICONTROL Catalog Search]_オプションの更新後にリストが自動的に一致しない場合は、[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)アクションで製品を手動で照合できます。

_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**の下：

- **[!UICONTROL Update Required Info]**:カタログに一覧が自動的に一致しない場合に選択します。カタログ商品を手動でリスト](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)に[照合するか、手動で[ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing)をカタログ照合に割り当てるか、リストに[足りない条件](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition)を割り当てます。

- **[!UICONTROL View Details]**:「リスト・アクティビティ・ログ」、「 [Buy Box競合相手の価格設定](./product-listing-details.md#listing-activity-log)」、「最低競合相手の価格設定 [」など、リストの詳細を表示する](./product-listing-details.md#buy-box-competitor-pricing) [](./product-listing-details.md#lowest-competitor-pricing)ように選択します。このアクションは表示専用です。 リスト内の詳細は変更できません。 [詳細を表示](./product-listing-details.md)を参照してください。

>[!NOTE]
>
>リストが処理中の場合は、タブの上にあるメッセージにリストの数が表示されます。

![不完全なAmazonリスト](assets/amazon-incomplete-listings.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、を表しま [!DNL Amazon Standard Identification Number]す。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | 製品の[条件](./product-listing-condition.md)。 |
| [!UICONTROL Landed Price] | 商品の上場価格と送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされた場合に使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス(Amazonで定義)。 上記のステータス表を参照してください。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックし、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
