---
title: 属性の管理
description: Amazon属性へのコマース製品属性のマッピングを管理して、システム間の正確な製品情報を確保できます。
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 属性の管理

Amazonと[!DNL Commerce]の両方は、製品の定義に使用される、属性と呼ばれる製品プロパティのシステムを使用します。 属性は、製品の説明、コンテンツ、画像、価格および様々なデータを定義します。

CommerceとAmazon間の通信を正常に行うには、[!DNL Commerce]属性を対応するAmazon属性に正しくマッピング（または一致）する必要があります。 Amazonとの統合時に、これらの属性をAmazon属性にマッピングします。 完了したら、[!DNL Commerce]はAmazonのリストを[!DNL Commerce]製品カタログと同期し、管理できます。

例えば、[!DNL Commerce]カタログとAmazonのリストに同じ項目があるとします。 商品の1つの属性は、品目の上場価格です。 [!DNL Commerce]の上場価格の名前は`Price`、Amazonの上場価格は`ListingPrice`にします。 Amazonと通信する際、[!DNL Commerce]属性`Price`はAmazon属性`ListingPrice`と同じであることを[!DNL Commerce]に指示する必要があります。 このプロセスは&#x200B;_属性の管理_&#x200B;と呼ばれ、新しい属性の作成や既存の属性の編集を含みます。 属性が正しく一致することを確認することで、[!DNL Commerce]とAmazonの間の正しい通信が保証されます。

属性マッピングが設定されている場合、[!DNL Commerce]は製品情報をAmazonとやり取りできます。 Amazonの製品リストがある場合、[!DNL Commerce]はAmazonの製品と詳細を[!DNL Commerce]カタログに読み込み、一元的に管理できる1つの製品カタログからAmazonのリストを管理できます。

Amazonの販売チャネルでは、必要に応じて、Amazonの販売チャネルホームページの&#x200B;[_[!UICONTROL Attributes]_ビュー](./attributes-view.md)で属性にアクセス、確認、作成および管理できます。 [!DNL Commerce]カタログに属性を追加する場合は、すべての製品でこれらの値を更新する必要が生じる可能性があります。

[!DNL Commerce]とAmazonの属性セットと値について詳しくは、次を参照してください。

- [属性の基本の管理](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;}
- [属性の作成](./creating-attributes.md#create-an-attribute)
- [既存の属性の編集](./creating-attributes.md#edit-an-attribute)
- [属性マッピングの表示](./amazon-matching-attributes-values.md)
- [属性マッピングの編集または作成](./amazon-manually-update-incomplete-listing.md)
