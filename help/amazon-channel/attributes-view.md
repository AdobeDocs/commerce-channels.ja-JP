---
title: Amazon listings の属性
description: AmazonSales Channelが [!UICONTROL Attributes] 「 」タブを使用して、Amazonおよびコマース属性のリストと、それらが製品の照合にどのようにマッピングされているかを監視します。
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Amazon listings の属性

この _[!UICONTROL Attributes]_表示には、Amazonと [!DNL Commerce] 属性。 また、このリストは、製品の照合用にマッピングされた属性も示します。 詳しくは、 [属性を管理](./managing-attributes.md).

![属性ビュー](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

次の _[!UICONTROL Attributes]_テーブルで属性設定を表示し、確認し、 [作成または編集](./creating-attributes.md) 属性。

## 属性リストを表示

1. の _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューでAmazon属性を探し、属性リストを確認します。

1. 必要に応じて、属性を作成または編集します。

   - 宛先 [作成](./creating-attributes.md#create-an-attribute) をクリックし、属性の一致する属性値を定義して、 **[!UICONTROL Create]**.

   - 非アクティブ化または非アクティブ化するには [設定を編集](./creating-attributes.md#edit-an-attribute) または属性値の一致を選択し、 **[!UICONTROL Edit]**.

     属性の編集には、製品マッチングの属性マッピングの変更が含まれます。

| フィールド | 説明 |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | で定義された販売活動の国  **[!DNL Amazon Marketplace]国** 期間 [ストア統合](./store-integration.md). |
| [!UICONTROL ID] | 生成された汎用属性値 [!DNL Commerce] 属性が作成されたとき。 |
| [!UICONTROL Amazon Attribute Name] | Amazonから読み込まれた属性の名前。 |
| [!UICONTROL Product Catalog Attribute Code] | マッピングされた場合、 [!DNL Commerce] マップに割り当てられた属性 _[!UICONTROL Amazon Attribute Name]_カタログとリスト商品の照合。 |
| [!UICONTROL Overwrite Magento Values] | 属性が `Overwrite Existing Magento Values` 「属性設定」(Attribute Settings) で、テーブルにが表示されます。 `Enabled`. 「有効」は、属性の更新された製品情報をAmazonから受け取ると、新しい情報が [!DNL Commerce] カタログ。 また、 [!DNL Commerce] ストア。 |
| ステータス | 属性値が [!DNL Commerce] および [!DNL Commerce] 属性。 オプション： `Enabled` / `Disabled` |
| アクション | 属性で使用可能なタスクオプションを示します。 オプション： `Create` / `Edit` |
