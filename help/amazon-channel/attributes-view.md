---
title: Amazon リストの属性
description: Amazon Sales Channelは、次の機能を提供します [!UICONTROL Attributes] tab キーを使用して、AmazonとCommerceの属性のリストと、商品のマッチング用のマッピング方法をモニタリングします。
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Amazon リストの属性

この _[!UICONTROL Attributes]_表示は、Amazonおよびのリストを表示します。 [!DNL Commerce] 属性。 このリストには、製品のマッチング用にマッピングされた属性も示されます。 詳しくは、を参照してください [属性の管理](./managing-attributes.md).

![属性ビュー](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

から _[!UICONTROL Attributes]_を表示して、テーブルの属性設定を確認します。 [作成または編集](./creating-attributes.md) 属性。

## 属性リストの表示

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューでAmazon属性を見つけ、属性リストを確認します。

1. 必要に応じて、属性を作成または編集します。

   - 終了 [作成](./creating-attributes.md#create-an-attribute) を選択し、属性の一致する属性値を定義して、 **[!UICONTROL Create]**.

   - 非アクティブ化する [設定を編集](./creating-attributes.md#edit-an-attribute) または属性の属性値が一致する場合は、 **[!UICONTROL Edit]**.

     属性の編集には、製品のマッチング用の属性マッピングの変更が含まれます。

| フィールド | 説明 |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | で定義された販売活動の国  **[!DNL Amazon Marketplace]国** 次の期間 [ストアの統合](./store-integration.md). |
| [!UICONTROL ID] | によって生成された汎用属性値 [!DNL Commerce] 属性が作成されたとき。 |
| [!UICONTROL Amazon Attribute Name] | Amazonから読み込まれた属性の名前。 |
| [!UICONTROL Product Catalog Attribute Code] | マッピングされた場合、 [!DNL Commerce] にマッピングするために割り当てられた属性 _[!UICONTROL Amazon Attribute Name]_カタログの照合および製品の一覧表示。 |
| [!UICONTROL Overwrite Magento Values] | 属性がに設定されている場合 `Overwrite Existing Magento Values` 属性設定の表には、次の内容が表示されます `Enabled`. 有効にした場合、属性の商品情報の更新がAmazonから受信されると、新しい情報で商品の対応する情報が更新（上書き）されます [!DNL Commerce] カタログ。 また、にリストされている製品にも影響を与える可能性があります [!DNL Commerce] ストア。 |
| ステータス | 属性値がに読み込まれたかどうかを示します [!DNL Commerce] およびがマッピングされました [!DNL Commerce] 属性。 オプション： `Enabled` / `Disabled` |
| アクション | 属性で使用可能なタスクオプションを示します。 オプション： `Create` / `Edit` |
