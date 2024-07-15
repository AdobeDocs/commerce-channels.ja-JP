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

[!DNL Commerce] は、`Global` または `Website` に設定する [ 価格範囲 ](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) の設定を提供します。 価格が `Global` に設定されている場合、すべての web サイトに対して 1 つの価格ソースがあります。 価格が `Website` に設定されている場合、Web サイトの価格は間で異なる可能性があり、フォールバックのデフォルトの価格値もあります（[ 価格範囲 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html) を参照）。

カタログの価格範囲を `Global` から `Website` に変更すると、すべての価格タイプ属性も `Website` に変更されます。 [Web サイトの追加 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites) を参照してください。

Web サイトの価格を選択した場合、次の 2 つの価格ソースがあります。

- Web サイトの価格
- デフォルト（フォールバック）の価格

Amazonのセールスチャネル統合の場合、[ リストルール ](./listing-rules.md) に基づいて、複数の web サイトの商品を 1 つの [!DNL Amazon Marketplace] 国にマッピングできます（[ ストア統合 ](./store-integration.md) で定義）。 ただし、このマッピングでは、価格が異なる複数の web サイトに製品が存在する場合に、価格を公開する必要がある問題が発生します。
