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

Amazon属性を次にマッピングする場合 [!DNL Commerce] Amazonのセールスチャネルが追跡および提供する属性は、すべてのAmazon値のフィルタリング可能なリストです。 このページを使用して、リンクの値を検証します [!DNL Commerce] 属性間で正しく同期 [!DNL Commerce] とAmazon。 リンクされているAmazon属性またはリンクされていない属性の同期された値を確認できます [!DNL Commerce] 属性。 Amazon属性を作成または編集するには、を参照してください。 [属性の作成と編集](./creating-attributes.md).

この _Amazon値_ 表示する属性タイプとAmazon属性によって異なります。 例えば、のリストされているAmazon値です。 `Label` はテキスト値ですが、 `AmazonListPrice` は数値の値になります。 「」ステータスは、Amazonの値がインポートされたかどうかを示します。

## 属性値の表示

1. 日 _[!UICONTROL Admin]_サイドバー、に移動&#x200B;**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューでAmazon属性を見つけて、次のいずれかをクリックします **[!UICONTROL Create]** または **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 「」をクリックします **[!UICONTROL Matching Attribute Values]** タブ。

   対応するがあるリスト [!DNL Commerce] カタログ製品の「」タブにリンクされた値が表示される _[!UICONTROL Magento Product SKU]_列。 リンクをクリックすると、対応するカタログ製品の詳細ページが開きます。 製品詳細ページのAmazon属性に加えた変更は、Amazon セールスチャネルに同期されません。

>[!TIP]
>リストのマッピングを編集またはカタログ製品に割り当てるには、を参照してください。 [必要な情報を更新](./amazon-manually-update-incomplete-listing.md).

![属性値の表示](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | で定義された販売活動の地域 **[!DNL Amazon Marketplace]国** ストアの統合中。 |
| [!UICONTROL Magento Product SKU] | は、 [!DNL Commerce] Amazon ストアと同期された製品。 値は、によって割り当てられた製品 ID です。 [!DNL Commerce] カタログ内の製品にリンクされています。 で製品を開くには [!DNL Commerce]を選択し、リンクをクリックします。 |
| [!UICONTROL ASIN] | 商品 ID のためにAmazonによって商品に割り当てられた 10 文字の英数字の一意の ID （Amazon標準識別番号（ASIN））を示します。 |
| [!UICONTROL Amazon Value] | 選択した属性の値を示します。 Amazonの値は、表示する属性タイプとAmazon属性によって異なります。 例えば、のリストされているAmazon値です。 `Label` はテキスト値ですが、 `AmazonListPrice` は数値の値になります。 「」ステータスは、Amazonの値がインポートされたかどうかを示します。 |
| [!UICONTROL Status] | 属性値がに読み込まれたかどうかを示します [!DNL Commerce] およびがにリンクされています [!DNL Commerce] 属性。 オプション： `Not Imported` / `Imported` |
