---
title: Amazonセールスチャネル — 価格範囲
description: 複数の Web サイトまたはグローバルに従って価格を管理するには、コマースの価格範囲を使用します。
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 価格の範囲

[!DNL Commerce] は、 [価格の範囲](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) 設定する `Global` または `Website`. 価格が `Global`の場合、すべての Web サイトに対して 1 つの価格ソースがあります。 価格が `Website`を使用すると、Web サイトの価格はによって異なる場合があり、代替のデフォルト価格値 ( [価格の範囲](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)) をクリックします。

カタログ価格の範囲を `Global` から `Website`に設定すると、すべての価格タイプ属性も `Website`. 詳しくは、 [Web サイトの追加](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

Web サイトの価格を選択すると、次の 2 つの価格ソースがあります。

- Web サイトの価格
- デフォルト（フォールバック）の価格

Amazonセールスチャネルの統合の場合、 [リストルール](./listing-rules.md)複数の Web サイトから単一の Web サイトに製品をマッピングできます。 [!DNL Amazon Marketplace] 国 ( 次の期間に定義： [ストア統合](./store-integration.md)) をクリックします。 ただし、このマッピングでは、価格が異なる複数の Web サイトに製品が存在する場合に、どの価格を公開するかという問題が生じます。
