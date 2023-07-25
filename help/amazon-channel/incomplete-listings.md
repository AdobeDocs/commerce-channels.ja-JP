---
title: 不完全なAmazonリスト
description: Amazonセールスチャネルが [!UICONTROL Incomplete] タブを使用すると、不完全なAmazonリストの実施要件を特定して満たすのに役立ちます。
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 不完全なAmazonリスト

この _[!UICONTROL Incomplete]_タブには、 [!DNL Commerce] Amazonの適格要件を満たすカタログ製品 ( [リストルール](./listing-rules.md)) ですが、Amazonで必要な情報 (Amazon ASIN や定義された製品条件など ) が欠落しています。

リストが不完全な場合は、4 つの原因が考えられます。それぞれがステータスによって識別されます。

| ステータス | 理由 | アクション |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 条件がありません | Amazonは様々な条件 ( _新規_, _改装済み_, _使用済み：新規に類似_) リストには定義済みの条件が必要です。 | 必要な情報を更新し、手動で行う [条件の割り当て](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) をリストに追加します。 |
| Amazonリストに割り当てられません | このリストをカタログに自動的に一致させることができませんでした。 一致が見つからない場合、リストはAmazonSales Channelで管理できません | 必要な情報を更新し、手動で行う [ASIN を割り当てる](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) をカタログ商品に追加して、リストに一致させます。 |
| 複数件の一致が見つかりました | このリストをカタログに自動的に一致させることができませんでした。 一致するものが複数見つかった場合は、製品に適した一致を選択する必要があります。 | 必要な情報を更新し、手動で行う [製品の一致を選択](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) を参照してください。 |
| バリアントあり | 異なるサイズや色で使用できる T シャツなどのバリエーションが製品に含まれている場合は、カタログ内のバリエーションを正しく割り当ててリストに一致させるために選択する必要があります | 必要な情報を更新し、手動で行う [正しいバリアントを選択する](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) を追加して、このリストに割り当てて照合します。 |

>[!NOTE]
>不完全なリストがカタログ製品と適切に一致する場合、リストは _[!UICONTROL Incomplete]_」タブに表示され、 [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) 設定。

に対して使用可能なアクション _[!UICONTROL Incomplete]_タブには次が含まれます。

の下 _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**:Amazonの一覧データを [!DNL Commerce] カタログ。 製品が自動的に一致しない場合は、 [_[!UICONTROL Catalog Search]_](./catalog-search.md) オプションを使用します。 更新後にリストが自動的に一致しない場合 _[!UICONTROL Catalog Search]_オプションを使用すると、 [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) アクション。

の下 **[!UICONTROL Select]** 内 _[!UICONTROL Action]_列：

- **[!UICONTROL Update Required Info]**:カタログに一覧が自動的に一致しない場合に選択します。 手動で [カタログ商品をリストに一致させる](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)手動 [ASIN を割り当てる](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) カタログのマッチング、または [欠落した条件を割り当て](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) を参照してください。

- **[!UICONTROL View Details]**：リストの詳細 ( [アクティビティログのリスト](./product-listing-details.md#listing-activity-log), [Buy Box競合他社の価格](./product-listing-details.md#buy-box-competitor-pricing)、および [競合他社の最低価格](./product-listing-details.md#lowest-competitor-pricing). このアクションは表示専用です。 リストの詳細は変更できません。 詳しくは、 [詳細を表示](./product-listing-details.md).

>[!NOTE]
>
>処理中のリストがある場合は、タブの上のメッセージにリストの数が表示されます。

![不完全なAmazonリスト](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Amazonセールスチャネルのホームページは、いくつかの共通を共有します [workspace コントロール](./workspace-controls.md) を使用すると、表示されるデータをカスタマイズできます。

| 列 | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | 製品、オプション、価格および製造元を識別するために、Amazonが製品に割り当てた SKU(Stock Keeping Unit)。 |
| [!UICONTROL ASIN] | アイテムを識別する 10 文字または数字の一意のブロック。<br><br>ASIN は、 [!DNL Amazon Standard Identification Number]. ASIN は、項目を識別する 10 文字または数字の一意のブロックです。 書籍の場合、ASIN は ISBN 番号と同じですが、他のすべての製品の場合は、アイテムがカタログにアップロードされると新しい ASIN が作成されます。 ASIN は、Amazonの製品の詳細ページに、その品目に関する詳細と共に表示されます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Condition] | この [条件](./product-listing-condition.md) 製品の。 |
| [!UICONTROL Landed Price] | 商品の上場価格とその送料。 |
| [!UICONTROL Amazon Quantity] | 製品がAmazonに積極的にリストされたときに使用可能な数量。 |
| [!UICONTROL Status] | リストのステータス (Amazonで定義 )。 上記のステータス表を参照してください。 |
| [!UICONTROL Action] | 特定のリストに適用できる使用可能なアクションのリスト。 アクションを適用するには、 **[!UICONTROL Select]** 内 _[!UICONTROL Action]_列を選択し、次のオプションを選択します。<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
