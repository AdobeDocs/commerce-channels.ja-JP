---
title: Amazonリストの属性の管理
description: コマース製品属性とAmazon属性のマッピングを管理して、システム間の正確な製品情報を確保できます。
feature: Sales Channels, Products, Configuration
exl-id: 6f9ded2d-292e-4b7e-8c10-48f478a4383e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Amazonリストの属性の管理

Amazonと [!DNL Commerce] 両方とも、製品の定義に使用される製品プロパティのシステム（属性と呼ばれる）を使用します。 属性は、製品の説明、コンテンツ、画像、価格および様々なデータを定義します。

コマースとAmazon間の通信を成功させるには、 [!DNL Commerce] 属性が、対応するAmazon属性に正しくマッピング（または一致）される。 Amazonと統合する場合、これらの属性をAmazon属性にマッピングします。 完了したら、 [!DNL Commerce] Amazonの一覧を [!DNL Commerce] 商品カタログ。

例えば、 [!DNL Commerce] カタログとAmazonの一覧 商品の属性の 1 つは、品目の上場価格です。 の定価の名前 [!DNL Commerce] はという名前になります `Price`Amazonの上場価格は `ListingPrice`. 次を指示する必要があります。 [!DNL Commerce] Amazonと通信する際に、 [!DNL Commerce] 属性名 `Price` は、以下の名前を持つAmazon属性と同じです。 `ListingPrice`. このプロセスは、 _属性の管理_&#x200B;には、新しい属性の作成や既存の属性の編集が含まれます。 属性が適切に一致することで、 [!DNL Commerce] Amazon

属性マッピングが設定されている場合、 [!DNL Commerce] は、Amazonとの間で製品情報を相互に伝達できます。 Amazonの製品リストがある場合は、 [!DNL Commerce] Amazonの製品と詳細を [!DNL Commerce] カタログ。一元的に管理できる単一のAmazon製品カタログから、製品リストを管理できます。

Amazonセールスチャネルでは、必要に応じて、属性のアクセス、確認、作成、管理を行うことができます。 [_[!UICONTROL Attributes]_表示](./attributes-view.md) (Amazonセールスチャネルホームページ ) 属性を [!DNL Commerce] カタログを使用する場合、すべての製品でこれらの値を更新する必要が生じる場合があります。

詳しくは、 [!DNL Commerce] とAmazonの属性セットと値は、次を参照してください。

- [属性の基本を管理](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html)
- [属性の作成](./creating-attributes.md#create-an-attribute)
- [既存の属性の編集](./creating-attributes.md#edit-an-attribute)
- [属性マッピングを表示](./amazon-matching-attributes-values.md)
- [属性マッピングの編集または作成](./amazon-manually-update-incomplete-listing.md)
