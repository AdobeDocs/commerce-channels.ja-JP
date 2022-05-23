---
title: カタログ属性をマッピング
description: 一致する属性をマッピング [DNL! コマース ] 製品を既存の製品に [!DNL Walmart Marketplace] リストと同期，データ間 [!DNL Channel Manager] および [!DNL Walmart].
source-git-commit: dfe56db25bb569ad70fb1036d539797bbb126dd5
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# カタログ属性をマッピング

次の場所にリストを公開する前に： [!DNL Commerce] から [!DNL Walmart Marketplace]の場合、 [!DNL Commerce] カタログを Walmart から対応する ID に追加します。
この手順は、 [!DNL Commerce] 既存の製品 [!DNL Walmart] 製品データを次の間で同期する [!DNL Commerce] および [!DNL Walmart].

製品の照合を行うには、コマース製品に、で必要な次の製品識別子（製品 ID）のいずれかに一致する 1 つ以上の製品属性が必要です。 [!DNL Walmart].

**必要なウォルマート製品 ID**

| **許可されたタイプ** | **名前** | **目的** | **指定可能な桁数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 世界貿易品目 | 汎用、世界中で使用 | 14 桁 |
| ISBN | 国際標準書籍番号 | ペーパーバック、ハードカバー、電子書籍 | 10 桁または 13 桁 |
| ISSN | 国際標準シリアル番号 | 全てのメディアプリントや電子メディアに配信される雑誌、雑誌、新聞、雑誌を特定するのに使用される 8 桁のシリアル番号 | 8 桁 |
| UPC | ユニバーサル製品コード | 標準の小売トラッキングコード | 12 桁 |

カタログに、次のタイプのいずれかに一致する属性がない場合、 [既存のカタログ属性を追加または変換する](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## 一意の ID をマッピング

1. の [!UICONTROL Listings] セールスチャネルストアのページで、「 」を選択します。 **[!UICONTROL Settings]**.

   - マッピングする Walmart Marketplace 属性を見つけます。

   - 対応する属性を [!DNL Commerce] ストアカタログ。

      次の例では、Walmart Marketplace UPC 属性を商品カタログの UPC 属性にマップします。
   ![製品一致条件の属性をマッピング](assets/products-map-attributes-for-match.png)

   - 選択 **[!UICONTROL Save]**.


## マッピングされた属性設定を更新

マッピングされた属性設定を更新して、製品に一致する Commerce 製品識別子を変更します。

例えば、Commerce UPC の製品属性コードに基づいて製品を一致させる代わりに、SKU に基づいて製品を一致させることができます。 または、追加の属性をマッピングして、マッチングを改善します。

1. 次の **[!UICONTROL Listings]**&#x200B;を選択します。 **[!UICONTROL Settings]**.

1. Map 属性フォームで、必要に応じて、マッピングされた属性設定を変更します。
