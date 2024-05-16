---
title: Amazon販売チャネル – 価格範囲
description: Commerceの価格範囲を使用すると、複数の web サイトに従って、または世界中で価格を管理できます。
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# 価格範囲

[!DNL Commerce] は、に設定を提供します [価格範囲](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) に設定されています `Global` または `Website`. 価格設定が次のように設定されている場合： `Global`、すべての web サイトに単一の価格ソースがあります。 価格設定が次のように設定されている場合： `Website`を使用すると、web サイトの価格は様々で、フォールバックのデフォルト価格値もあります（を参照） [価格範囲](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)）に設定します。

カタログの価格範囲をから変更した場合 `Global` 対象： `Website`すべての価格タイプ属性もに変更されます。 `Website`. 参照： [Web サイトの追加](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Web サイトの価格を選択した場合、次の 2 つの価格ソースがあります。

- Web サイトの価格
- デフォルト（フォールバック）の価格

Amazonのセールスチャネル統合の場合、に基づきます [リストルール](./listing-rules.md)複数の web サイトの製品を 1 つの web サイトにマッピングできます [!DNL Amazon Marketplace] 国（次の期間で定義） [ストアの統合](./store-integration.md)）に設定します。 ただし、このマッピングでは、価格が異なる複数の web サイトに製品が存在する場合に、価格を公開する必要がある問題が発生します。
