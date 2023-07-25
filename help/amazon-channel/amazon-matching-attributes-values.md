---
title: Amazon属性マッピングを表示
description: コマースとAmazonが正しく同期されるように、リンクされたコマース属性の値を検証します。
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Amazon属性マッピングを表示

Amazon属性を [!DNL Commerce] 属性、Amazonセールスチャネルは、すべてのAmazon値を追跡し、フィルタリング可能なリストを提供します。 このページを使用して、リンクされた [!DNL Commerce] 属性間で正しく同期 [!DNL Commerce] Amazon Amazon属性の同期値を確認できます。 [!DNL Commerce] 属性。 Amazon属性を作成または編集するには、 [属性の作成と編集](./creating-attributes.md).

この _Amazon値_ は、表示する属性タイプとAmazon属性に応じて異なります。 例えば、 `Label` はテキスト値ですが、 `AmazonListPrice` 数値になります。 ステータスは、Amazonの値が読み込まれたかどうかを示します。

## 属性値を表示する

1. の _[!UICONTROL Admin]_サイドバー、移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューで、Amazon属性を探し、 **[!UICONTROL Create]** または **[!UICONTROL Edit]** 内 _[!UICONTROL Action]_列。

1. 次をクリック： **[!UICONTROL Matching Attribute Values]** タブをクリックします。

   対応する [!DNL Commerce] カタログ商品は、 _[!UICONTROL Magento Product SKU]_列。 リンクをクリックすると、対応するカタログ製品の詳細ページが開きます。 製品の詳細ページでのAmazon属性の変更が、Amazonのセールスチャネルに同期されない。

>[!TIP]
>リストのマッピングを編集またはカタログ商品に割り当てるには、 [必要な情報を更新](./amazon-manually-update-incomplete-listing.md).

![属性値の表示](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | で定義された販売活動の地域 **[!DNL Amazon Marketplace]国** ストアの統合中に |
| [!UICONTROL Magento Product SKU] | を示します。 [!DNL Commerce] 製品がAmazonストアと同期されました。 値は、 [!DNL Commerce] カタログ内の商品にリンクされている。 で製品を開くには、以下を実行します。 [!DNL Commerce]、リンクをクリックします。 |
| [!UICONTROL ASIN] | Amazonが製品を識別するために製品に割り当てた、Amazon標準 ID 番号 (ASIN)10 文字の英数字の一意の ID を示します。 |
| [!UICONTROL Amazon Value] | 選択した属性の値を示します。 Amazon値は、属性タイプと表示するAmazon属性に応じて異なります。 例えば、 `Label` はテキスト値ですが、 `AmazonListPrice` 数値になります。 ステータスは、Amazonの値が読み込まれたかどうかを示します。 |
| [!UICONTROL Status] | 属性値が [!DNL Commerce] および [!DNL Commerce] 属性。 オプション： `Not Imported` / `Imported` |
