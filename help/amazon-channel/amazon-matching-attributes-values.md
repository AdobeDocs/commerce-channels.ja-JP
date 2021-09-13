---
title: Amazon属性マッピングの表示
description: コマースとAmazonの間で正しく同期されるように、リンクされたコマース属性の値を確認します。
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Amazon属性マッピングの表示

Amazon属性を[!DNL Commerce]属性にマッピングすると、Amazonの販売チャネルはAmazonのすべての値を追跡し、フィルタリング可能なリストを提供します。 このページを使用して、リンクされた[!DNL Commerce]属性の値が[!DNL Commerce]とAmazonの間で正しく同期していることを確認します。 [!DNL Commerce]属性にリンクされている、または属性にリンクされていないAmazon属性の同期値を確認できます。 Amazon属性を作成または編集するには、[属性の作成と編集](./creating-attributes.md)を参照してください。

_Amazon値_&#x200B;は、表示する属性タイプとAmazon属性によって異なります。 例えば、`Label`に対してリストされているAmazon値はテキスト値で、`AmazonListPrice`は数値です。 「 」ステータスは、Amazon値が読み込まれたかどうかを示します。

## 属性値の表示

1. _[!UICONTROL Admin]_サイドバーで、**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**&#x200B;に移動します。

1. 左側のメニューで&#x200B;**[!UICONTROL Attributes]**&#x200B;をクリックし、Amazon属性を探して、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Create]**または&#x200B;**[!UICONTROL Edit]**をクリックします。

1. 「**[!UICONTROL Matching Attribute Values]**」タブをクリックします。

   対応する[!DNL Commerce]カタログ製品を持つリストの「_Magento製品のSKU_」列に、リンクされた値が表示されます。 リンクをクリックすると、対応するカタログ製品の詳細ページが開きます。 製品の詳細ページでのAmazon属性の変更が、Amazonの販売チャネルに同期されない。

>[!TIP]
>リストのマッピングを編集またはカタログ製品に割り当てるには、[必要な情報を更新](./amazon-manually-update-incomplete-listing.md)を参照してください。

![属性値の表示](assets/amazon-managing-attribute-values.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Region] | 店舗統合中の&#x200B;**[!DNL Amazon Marketplace]国**&#x200B;で定義された販売活動の地域。 |
| [!UICONTROL Magento Product SKU] | Amazonストアと同期された[!DNL Commerce]製品を示します。 値は、[!DNL Commerce]によって割り当てられ、カタログ内の製品にリンクされた製品IDです。 [!DNL Commerce]で製品を開くには、リンクをクリックします。 |
| [!UICONTROL ASIN] | Amazonが製品を識別するために製品に割り当てた、Amazon Standard ID番号(ASIN)10文字の英数字の一意の識別子を示します。 |
| [!UICONTROL Amazon Value] | 選択した属性の値を示します。 Amazonの値は、属性タイプと表示するAmazon属性によって異なります。 例えば、`Label`に対してリストされているAmazon値はテキスト値で、`AmazonListPrice`は数値です。 「 」ステータスは、Amazon値が読み込まれたかどうかを示します。 |
| [!UICONTROL Status] | 属性値が[!DNL Commerce]に読み込まれ、[!DNL Commerce]属性にリンクされているかどうかを示します。 オプション：`Not Imported` / `Imported` |
