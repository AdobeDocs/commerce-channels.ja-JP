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

Amazonと [!DNL Commerce] どちらも、製品の定義に使用される製品プロパティのシステム（属性と呼ばれます）を使用します。 属性は、製品の説明、コンテンツ、画像、価格および様々なデータを定義します。

CommerceとAmazonの間で通信を成功させるには、次の要件が必要です [!DNL Commerce] 属性は、対応するAmazon属性に正しくマッピング（または一致）されます。 Amazonと統合する際に、これらの属性をAmazon属性にマッピングします。 完了すると、 [!DNL Commerce] Amazonのリストをと同期して管理できます [!DNL Commerce] 商品カタログ。

例えば、に同じ項目があるとします [!DNL Commerce] カタログおよびAmazonのリスト。 商品の属性の 1 つに、商品の上場価格があります。 での上場価格の名前 [!DNL Commerce] という名前かもしれません `Price`の場合、Amazonの上場価格という名前が付いている場合があります `ListingPrice`. 次を指示する必要があります [!DNL Commerce] Amazonと通信する場合、 [!DNL Commerce] という名前の属性 `Price` という名前のAmazon属性と同じです `ListingPrice`. このプロセスはと呼ばれます _属性の管理_&#x200B;これには、新しい属性の作成と既存の属性の編集が含まれます。 属性が正しく一致していることを確認すると、間で正しく通信できます [!DNL Commerce] とAmazon。

属性マッピングを設定すると、 [!DNL Commerce] Amazonと商品情報を行き来できます。 Amazon製品リストがある場合、 [!DNL Commerce] Amazonの製品および詳細をに読み込むことができます [!DNL Commerce] カタログを使用すると、1 つの製品カタログを一元管理してAmazonのリストを管理できます。

Amazon セールスチャネルでは、必要に応じて、の属性にアクセス、確認、作成、管理できます。 [_[!UICONTROL Attributes]_表示](./attributes-view.md) Amazon sales channel のホームページに移動します。 に属性を [!DNL Commerce] カタログが存在しない場合、すべての製品でそれらの値を更新する必要が生じる可能性があります。

詳しくは、 [!DNL Commerce] およびAmazonの属性セットと値については、以下を参照してください。

- [属性の管理の基本](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [属性の作成](./creating-attributes.md#create-an-attribute)
- [既存の属性を編集](./creating-attributes.md#edit-an-attribute)
- [属性マッピングの表示](./amazon-matching-attributes-values.md)
- [属性マッピングを編集または作成](./amazon-manually-update-incomplete-listing.md)
