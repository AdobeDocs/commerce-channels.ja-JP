---
title: Amazon リストの属性の管理
description: Commerce製品属性とAmazon属性のマッピングを管理して、システム間の製品情報を正確に把握できます。
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Amazon リストの属性の管理

Amazonと [!DNL Commerce] の両方で、製品の定義に使用される属性と呼ばれる製品プロパティシステムを使用します。 属性は、製品の説明、コンテンツ、画像、価格および様々なデータを定義します。

CommerceとAmazon間の通信に成功するには、[!DNL Commerce] の属性が対応するAmazon属性に正しくマッピング（または一致）されている必要があります。 Amazonと統合する際に、これらの属性をAmazon属性にマッピングします。 完了 [!DNL Commerce] たら、Amazonのリストを [!DNL Commerce] の商品カタログと同期して管理できます。

例えば、[!DNL Commerce] カタログとAmazonのリストに同じ項目があるとします。 商品の属性の 1 つに、商品の上場価格があります。 [!DNL Commerce] の上場価格の名前は `Price` のように指定し、Amazonの上場価格は `ListingPrice` のように指定します。 Amazonと通信する際は、`Price` という名前の [!DNL Commerce] 属性が `ListingPrice` という名前のAmazon属性と同じであることを [!DNL Commerce] に指示する必要があります。 このプロセスは _属性の管理_ と呼ばれ、新しい属性の作成と既存の属性の編集が含まれます。 属性が正しく一致していることを確認することで、[!DNL Commerce] とAmazonの間で正しくやりとりが行われます。

属性マッピングが設定されると、商品情報 [!DNL Commerce]Amazonと相互にやり取りできます。 Amazonの商品リストがある場 [!DNL Commerce]、Amazonの商品や詳細を [!DNL Commerce] カタログに読み込むと、1 つの商品カタログで一元的にAmazonのリストを管理できます。

Amazon sales channel を使用すると、必要に応じて、Amazon sales channel ホームページの [_[!UICONTROL Attributes]_ビューで属性にアクセス ](./attributes-view.md) 確認、作成および管理できます。 [!DNL Commerce] カタログに属性を追加した場合、すべての製品でそれらの値を更新する必要が生じる可能性があります。

[!DNL Commerce] およびAmazonの属性セットと値について詳しくは、以下を参照してください。

- [ 属性の管理の基本 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [属性の作成](./creating-attributes.md#create-an-attribute)
- [既存の属性を編集](./creating-attributes.md#edit-an-attribute)
- [属性マッピングの表示](./amazon-matching-attributes-values.md)
- [属性マッピングを編集または作成](./amazon-manually-update-incomplete-listing.md)
