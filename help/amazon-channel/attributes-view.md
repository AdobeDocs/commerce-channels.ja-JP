---
title: Amazon リストの属性
description: Amazon Sales Channelでは、Amazon属性とCommerce属性のリスト、および商品のマッチング用のマッピング方法をモニタリングする「[!UICONTROL Attributes]」タブが用意されています。
feature: Sales Channels, Products, Configuration
exl-id: fc08cd6e-eef9-4e71-82b1-5443e14800ce
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Amazon リストの属性

_[!UICONTROL Attributes]_ビューには、Amazonと [!DNL Commerce] 属性のリストが表示されます。 このリストには、製品のマッチング用にマッピングされた属性も示されます。 詳しくは、[ 属性の管理 ](./managing-attributes.md) を参照してください。

![ 属性ビュー ](assets/amazon-attributes-view.png){width="600" zoomable="yes"}

_[!UICONTROL Attributes]_ビューから、テーブルの属性設定と属性の [ 作成または編集 ](./creating-attributes.md) を確認します。

## 属性リストの表示

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューで **[!UICONTROL Attributes]** をクリックし、Amazon属性を見つけて、属性リストを確認します。

1. 必要に応じて、属性を作成または編集します。

   - 属性の一致する属性値を [ 作成 ](./creating-attributes.md#create-an-attribute) および定義するには、「**[!UICONTROL Create]**」をクリックします。

   - 属性の属性をディアクティベートまたは [ 設定を編集 ](./creating-attributes.md#edit-an-attribute) または一致させる属性値を編集するには、[**[!UICONTROL Edit]**] をクリックします。

     属性の編集には、製品のマッチング用の属性マッピングの変更が含まれます。

| フィールド | 説明 |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Country] | [ 店舗の統合 ](./store-integration.md) 中に **[!DNL Amazon Marketplace]国で定義され** 販売活動の国。 |
| [!UICONTROL ID] | 属性の作成時に [!DNL Commerce] で生成される汎用属性値。 |
| [!UICONTROL Amazon Attribute Name] | Amazonから読み込まれた属性の名前。 |
| [!UICONTROL Product Catalog Attribute Code] | マッピングされる場合、カタログの照合および製品のリスト表示のために _[!UICONTROL Amazon Attribute Name]_にマッピングされる [!DNL Commerce] 属性。 |
| [!UICONTROL Overwrite Magento Values] | 属性設定で属性が `Overwrite Existing Magento Values` に設定されている場合、テーブルには `Enabled` が表示されます。 有効にした場合、属性の商品情報の更新がAmazonから受け取ると、新しい情報によって、[!DNL Commerce] カタログの商品に対応する情報が更新（上書き）されます。 また、[!DNL Commerce] ストアにリストされている製品にも影響を与える可能性があります。 |
| ステータス | 属性値が [!DNL Commerce] にインポートされ、[!DNL Commerce] 属性にマップされているかどうかを示します。 オプション：`Enabled` / `Disabled` |
| アクション | 属性で使用可能なタスクオプションを示します。 オプション：`Create` / `Edit` |
