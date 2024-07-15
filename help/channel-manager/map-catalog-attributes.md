---
title: カタログ属性のマッピング
description: '一致する属性をマッピング [DNL! Commerce] products to existing [!DNL Walmart Marketplace] listings and synchronizing data between [!DNL Channel Manager] and [!DNL Walmart].'
feature: Sales Channels, Merchandising, Products
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# カタログ属性のマッピング

リストを [!DNL Commerce] から [!DNL Walmart Marketplace] に接続する前に、[!DNL Commerce] カタログの 1 つ以上の一意の ID を、ウォルマートの対応する ID にマッピングする必要があります。

この手順は、[!DNL Commerce] 製品を既存の [!DNL Walmart] リストと照合し、[!DNL Commerce] と [!DNL Walmart] の間で製品データを同期するために必要です。 [!DNL Commerce] 製品には、[!DNL Walmart] に必要な次の製品識別子（製品 ID）のいずれかに一致する製品属性が少なくとも 1 つ必要です。

**製品 ID[!DNL Walmart] 必須**

| **許可されたタイプ** | **名前** | **目的** | **使用可能な数字** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 国際貿易品目 | 世界中で使用される汎用 | 14 桁 |
| ISBN | 国際標準簿番号 | ペーパーバック、ハードカバー及び電子書籍 | 10 桁または 13 桁 |
| ISSN | 国際標準シリアル番号 | 8 桁のシリアル番号。雑誌、雑誌、新聞、あらゆる種類の定期刊行物を識別するために使用されます。印刷および電子 | 8 桁 |
| UPC | ユニバーサル製品コード | 標準小売追跡コード | 12 桁 |

カタログに一致する属性がない場合は、[ 既存のカタログ属性を追加または変換 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) します。

## 一意の識別子のマッピング

1. 営業チャネル・ストアの **[!UICONTROL Listings]** ページまたは **[!UICONTROL Orders]** ページから、「**[!UICONTROL Channel Settings]**」を選択します。

1. **[!UICONTROL Channel Settings]** で「**[!UICONTROL Map Attributes]**」を選択します。

   - マッピングする [!DNL Walmart Marketplace] 属性を見つけます。

   - 対応する属性を [!DNL Commerce] ストアカタログから選択します。

     次の例では、[!UICONTROL Walmart Marketplace UPC] 属性を製品カタログの UPC 属性にマッピングします。

     ![ 製品一致条件の属性のマッピング ](assets/products-map-attributes-for-match.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Save]**」を選択します。
