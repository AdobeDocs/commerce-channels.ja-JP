---
title: 価格範囲
description: 複数の Web サイトまたはグローバルに従って価格を管理するには、コマースの価格範囲を使用します。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 価格範囲

[!DNL Commerce] は、 [価格の範囲](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} （コアコマースユーザーガイド）を参照してください。

カタログ価格の範囲を `Global` から `Website`に設定すると、すべての価格タイプ属性も `Website`. 詳しくは、 [Web サイトの追加](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

Web サイトの価格を選択すると、次の 2 つの価格ソースがあります。

- Web サイトの価格
- デフォルト（フォールバック）の価格

Amazonセールスチャネルの統合の場合、 [リストルール](./listing-rules.md)複数の Web サイトから単一の Web サイトに製品をマッピングできます [!DNL Amazon Marketplace] 国 ( [ストア統合](./store-integration.md)) をクリックします。 ただし、このマッピングでは、価格が異なる複数の Web サイトに製品が存在する場合に、どの価格を公開するかという問題が生じます。
