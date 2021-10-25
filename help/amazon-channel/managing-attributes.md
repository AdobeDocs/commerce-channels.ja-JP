---
title: 属性の管理
description: Commerce 製品の属性を Amazon 属性にマップすることで、システム間の正確な製品情報を確認できます。
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 属性の管理

Amazon と [!DNL Commerce] その両方は、製品を定義するために使用される「属性」という製品プロパティのシステムを使用しています。 属性には、製品の説明、内容、画像、価格、および様々なデータが定義されています。

Commerce と Amazon の間の通信を正常 [!DNL Commerce] に行うには、対応する Amazon attribute に属性が正しくマップされている (または一致している) 必要があります。 Amazon との統合により、これらの属性を Amazon 属性にマップします。 完了すると、 [!DNL Commerce] Amazon リストを同期して、ご使用の製品カタログで管理することができ [!DNL Commerce] ます。

例として、カタログや Amazon リストに同じアイテムが含まれている [!DNL Commerce] とします。 製品の1つの属性は、品目の出展価格になる場合があります。 のリスト価格の名前には名前が [!DNL Commerce] 付けられていますが、Amazon の定価には名前が `Price` 付いて `ListingPrice` います。 [!DNL Commerce]Amazon との通信を行うときは、と [!DNL Commerce] いう名前の `Price` amazon 属性と同じ属性を指定する必要があり `ListingPrice` ます。この処理は _、「属性の管理」と呼ばれ_ 、既存の属性を作成して編集することもできます。 属性が適切に一致するかどうかを確認すると、その通信と Amazon にとって適切な通信が可能になり [!DNL Commerce] ます。

属性マッピングが設定されていると、 [!DNL Commerce] Amazon によって製品情報をやり取りすることができます。 Amazon 製品リストに含まれている場合は、 [!DNL Commerce] amazon 製品や詳細情報をカタログに取り込むことができます。これにより、 [!DNL Commerce] amazon リストは、1つの総合カタログから製品を管理することができます。

Amazon sales channel を使用すると、必要に応じて、 [_[!UICONTROL Attributes]_](./attributes-view.md) amazon sales channel のホームページのビューに、属性へのアクセス、確認、作成および管理を行うことができます。 カタログに属性を追加する場合は [!DNL Commerce] 、すべての製品についてそれらの値を更新する必要があります。

[!DNL Commerce]属性セットと属性値について詳しくは、次を参照してください。

- [属性の管理の基礎 ](https://docs.magento.com/user-guide/catalog/product-attributes.html) {target = &quot;_blank&quot;}
- [属性の作成](./creating-attributes.md#create-an-attribute)
- [既存の属性の編集](./creating-attributes.md#edit-an-attribute)
- [属性マッピングの表示](./amazon-matching-attributes-values.md)
- [属性マッピングの編集または作成](./amazon-manually-update-incomplete-listing.md)
