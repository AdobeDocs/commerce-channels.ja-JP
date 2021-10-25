---
title: Amazon 属性マッピングの表示
description: 関連付けられた Commerce 属性の値が、Commerce と Amazon との間で正しく同期されるようにします。
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Amazon 属性マッピングの表示

Amazon の属性を属性にマップすると [!DNL Commerce] 、amazon channel channel チャンネルによってすべての amazon 値がフィルタリング可能なリストに記録されます。 このページを使用して、リンクされた属性の値を確認し [!DNL Commerce] ます。と Amazon の両方が正しく同期さ [!DNL Commerce] れていません。 Amazon attribute によってリンクされた値、または属性にリンクされていない同期値を確認することができ [!DNL Commerce] ます。 Amazon 属性を作成または編集する方法については、 [ 属性の作成と編集を参照してください ](./creating-attributes.md) 。

Amazon の値は、 __ 属性の種類と、表示する Amazon attribute によって異なります。 例えば、表示される Amazon value にはテキスト値が含まれますが、これは数値になり `Label` `AmazonListPrice` ます。 この状態は、Amazon の値がインポートされたかどうかを示します。

## 属性値の表示

1. 傍注については _[!UICONTROL Admin]_、**[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > を参照して **[!UICONTROL Amazon Sales Channel]** ください。

1. **[!UICONTROL Attributes]**&#x200B;左側のメニューで「Amazon」という属性を探し、列内をクリックし **[!UICONTROL Create]** **[!UICONTROL Edit]** _[!UICONTROL Action]_ます。

1. タブをクリックし **[!UICONTROL Matching Attribute Values]** ます。

   カタログ製品が対応しているリスト [!DNL Commerce] では、Magento 製品 SKU 列にリンクされた値が表示さ __ れます。 リンクをクリックすると、対応するカタログ製品詳細ページが開きます。 製品の詳細ページで Amazon 属性を変更しても、Amazon sales channel に同期されません。

>[!TIP]
>カタログ製品に一覧のマッピングを編集または割り当てを行う方法については、「必要な情報を更新する」を参照してください [ ](./amazon-manually-update-incomplete-listing.md) 。

![属性値の表示](assets/amazon-managing-attribute-values.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Region] | **[!DNL Amazon Marketplace]店舗統合中に国で定義された営業活動の領域** です。 |
| [!UICONTROL Magento Product SKU] | [!DNL Commerce]Amazon store と同期された製品を示します。値は、によって割り当てられ、 [!DNL Commerce] カタログ内の製品にリンクされています。 で製品を開くには [!DNL Commerce] 、リンクをクリックします。 |
| [!UICONTROL ASIN] | Amazon によって製品 id として製品に割り当てられた10文字の英数字の一意の識別子 (Amazon) を示します。 |
| [!UICONTROL Amazon Value] | 選択された属性の値を示します。 Amazon の値は、属性の種類と、表示する Amazon attribute によって異なります。 例えば、表示される Amazon value にはテキスト値が含まれますが、これは数値になり `Label` `AmazonListPrice` ます。 この状態は、Amazon の値がインポートされたかどうかを示します。 |
| [!UICONTROL Status] | 属性値が属性にインポートされたかどうか、また属性にリンクしているかどうかを示し [!DNL Commerce] [!DNL Commerce] ます。 オプション: `Not Imported` / `Imported` |
