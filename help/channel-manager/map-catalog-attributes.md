---
title: カタログ属性をマッピング
description: '''一致する属性をマッピング [DNL! コマース ] 製品を既存の製品に [!DNL Walmart Marketplace] リストと同期，データ間 [!DNL Channel Manager] および [!DNL Walmart].`'
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# カタログ属性をマッピング

次のリストに接続する前に： [!DNL Commerce] から [!DNL Walmart Marketplace]の場合、 [!DNL Commerce] カタログを Walmart から対応する ID に追加します。

この手順は、 [!DNL Commerce] 既存の製品 [!DNL Walmart] 製品データを次の間で同期する [!DNL Commerce] および [!DNL Walmart]. この [!DNL Commerce] 製品には、で必要な次の製品識別子（製品 ID）の 1 つに一致する製品属性が少なくとも 1 つ必要です。 [!DNL Walmart].

**必須 [!DNL Walmart] 製品 ID**

| **許可されたタイプ** | **名前** | **目的** | **指定可能な桁数** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | 世界貿易品目 | 汎用、世界中で使用 | 14 桁 |
| ISBN | 国際標準書籍番号 | ペーパーバック、ハードカバー、電子書籍 | 10 桁または 13 桁 |
| ISSN | 国際標準シリアル番号 | 全てのメディアプリントや電子メディアに配信される雑誌、雑誌、新聞、雑誌を特定するのに使用される 8 桁のシリアル番号 | 8 桁 |
| UPC | ユニバーサル製品コード | 標準の小売トラッキングコード | 12 桁 |

カタログに一致する属性がない場合、 [既存のカタログ属性を追加または変換する](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## 一意の ID をマッピング

1. 次の **[!UICONTROL Listings]** または **[!UICONTROL Orders]** セールスチャネルストアのページで、「 」を選択します。 **[!UICONTROL Channel Settings]**.

1. オン **[!UICONTROL Channel Settings]**&#x200B;を選択します。 **[!UICONTROL Map Attributes]**.

   - 次を検索： [!DNL Walmart Marketplace] マップする属性。

   - 対応する属性を [!DNL Commerce] ストアカタログ。

      次の例では、 [!UICONTROL Walmart Marketplace UPC] 属性を製品カタログの UPC 属性に設定します。

      ![製品一致条件の属性をマッピング](assets/products-map-attributes-for-match.png)

   - 選択 **[!UICONTROL Save]**.
