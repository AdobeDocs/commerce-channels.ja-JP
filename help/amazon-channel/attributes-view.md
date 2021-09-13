---
title: 属性
description: AmazonSales Channelには、Amazon属性とコマース属性のリストと、それらが製品の照合のためにどのようにマッピングされているかを監視する[!UICONTROL Attributes]タブが用意されています。
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 属性

_[!UICONTROL Attributes]_ビューには、Amazonと[!DNL Commerce]属性のリストが表示されます。 リストには、製品の照合用にマッピングされた属性も示されます。 詳しくは、[属性の管理](./managing-attributes.md)を参照してください。

![属性ビュー](assets/amazon-attributes-view.png)

_[!UICONTROL Attributes]_ビューから、テーブルの属性設定を確認し、[属性を作成または編集](./creating-attributes.md)します。

## 属性リストの表示

1. _管理_&#x200B;サイドバーで、**[!UICONTROL Marketing]** / _[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューの&#x200B;**[!UICONTROL Attributes]**&#x200B;をクリックし、Amazon属性を探して、属性リストを確認します。

1. 必要に応じて、属性を作成または編集します。

   - [](./creating-attributes.md#create-an-attribute)を作成し、属性の「一致する属性値」を定義するには、**[!UICONTROL Create]**&#x200B;をクリックします。

   - 属性の設定](./creating-attributes.md#edit-an-attribute)または一致する属性値を非アクティブ化または[編集するには、**[!UICONTROL Edit]**&#x200B;をクリックします。

      属性の編集には、製品マッチングのための属性マッピングの変更が含まれます。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Country] | [ストア統合](./store-integration.md)の間に&#x200B;**[!DNL Amazon Marketplace]国**&#x200B;で定義された販売活動の国。 |
| [!UICONTROL ID] | 属性の作成時に[!DNL Commerce]によって生成される汎用属性値。 |
| [!UICONTROL Amazon Attribute Name] | Amazonから読み込まれた属性の名前。 |
| [!UICONTROL Product Catalog Attribute Code] | マッピングされた場合、[!DNL Commerce]属性が&#x200B;_[!UICONTROL Amazon Attribute Name]_に割り当てられ、カタログと商品の一覧表示に対応します。 |
| [!UICONTROL Overwrite Magento Values] | 属性設定で属性が`Overwrite Existing Magento Values`に設定されている場合、表に`Enabled`と表示されます。 「有効」は、属性の更新された製品情報をAmazonから受け取ると、新しい情報が[!DNL Commerce]カタログ内の製品に対応する情報を更新（上書き）することを意味します。 また、[!DNL Commerce]ストアにリストされている製品に影響を与える場合もあります。 |
| ステータス | 属性値が[!DNL Commerce]に読み込まれ、[!DNL Commerce]属性にマッピングされたかどうかを示します。 オプション：`Enabled` / `Disabled` |
| アクション | 属性で使用可能なタスクオプションを示します。 オプション：`Create` / `Edit` |
