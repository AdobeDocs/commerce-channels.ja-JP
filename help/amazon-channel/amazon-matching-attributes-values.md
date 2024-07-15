---
title: Amazon属性マッピングの表示
description: リンクされたCommerce属性の値を検証して、CommerceとAmazonを正しく同期させます。
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Amazon属性マッピングの表示

Amazonの属性を [!DNL Commerce] の属性にマッピングすると、Amazon Amazon チャネルは、すべての Sales Channel 値のフィルタリング可能なリストを追跡し提供します。 このページを使用して、リンクされた [!DNL Commerce] 属性の値が [!DNL Commerce] とAmazonの間で正しく同期されていることを検証します。 リンクされているAmazon属性またはリンクされていない属性の同期された値を確認で [!DNL Commerce] ます。 Amazon属性を作成または編集するには、[ 属性の作成および編集 ](./creating-attributes.md) を参照してください。

_Amazon値_ は、属性タイプと表示するAmazon属性によって異なります。 例えば、`Label` のリストされたAmazon値はテキスト値になり、`AmazonListPrice` は数値になります。 「」ステータスは、Amazonの値がインポートされたかどうかを示します。

## 属性値の表示

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]** に移動します。

1. 左側のメニューで「**[!UICONTROL Attributes]**」をクリックし、Amazon属性を見つけて、_[!UICONTROL Action]_列内の「**[!UICONTROL Create]**」または「**[!UICONTROL Edit]**」をクリックします。

1. 「**[!UICONTROL Matching Attribute Values]**」タブをクリックします。

   対応する [!DNL Commerce] カタログ製品を持つ一覧は、_[!UICONTROL Magento Product SKU]_列にリンクされた値を示します。 リンクをクリックすると、対応するカタログ製品の詳細ページが開きます。 製品詳細ページのAmazon属性に加えた変更は、Amazon セールスチャネルに同期されません。

>[!TIP]
>リストのマッピングを編集したり、カタログ製品に割り当てたりする方法については、[ 必須情報を更新 ](./amazon-manually-update-incomplete-listing.md) を参照してください。

![ 属性値を表示 ](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | 店舗の統合中に国で定義された販売活動 **[!DNL Amazon Marketplace]リージョ**。 |
| [!UICONTROL Magento Product SKU] | Amazon ストアと同期される [!DNL Commerce] 製品を示します。 値は、[!DNL Commerce] によって割り当てられ、カタログ内の製品にリンクされている製品 ID です。 製品を [!DNL Commerce] で開くには、リンクをクリックします。 |
| [!UICONTROL ASIN] | 商品 ID のためにAmazonによって商品に割り当てられた 10 文字の英数字の一意の ID （Amazon標準識別番号（ASIN））を示します。 |
| [!UICONTROL Amazon Value] | 選択した属性の値を示します。 Amazonの値は、表示する属性タイプとAmazon属性によって異なります。 例えば、`Label` のリストされたAmazon値はテキスト値になり、`AmazonListPrice` は数値になります。 「」ステータスは、Amazonの値がインポートされたかどうかを示します。 |
| [!UICONTROL Status] | 属性値が [!DNL Commerce] にインポートされ、[!DNL Commerce] 属性にリンクされているかどうかを示します。 オプション：`Not Imported` / `Imported` |
