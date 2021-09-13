---
title: 価格の範囲
description: 複数のWebサイトに従って、またはグローバルに価格を管理するには、コマースの価格範囲を使用します。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# 価格の範囲

[!DNL Commerce] は、価格スコー [プ](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;}をまたはに設定するための設定を提供 `Global` しま `Website`す。価格が`Global`に設定されている場合、すべてのWebサイトに1つの価格情報が提供されます。 価格が`Website`に設定されている場合、Webサイトの価格は異なる場合があり、フォールバックのデフォルト価格値も設定されます。 コアコマースユーザーガイドの[カタログ価格](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;}を参照してください。

カタログ価格の範囲を`Global`から`Website`に変更すると、すべての価格タイプ属性も`Website`に変更されます。 [Webサイトの追加](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target=&quot;_blank&quot;}を参照してください。

Webサイトの価格を選択すると、次の2つの価格ソースがあります。

- Webサイトの価格
- デフォルト（フォールバック）価格

Amazonの販売チャネル統合の場合、[リストルール](./listing-rules.md)に基づいて、複数のWebサイトの製品を1つの[!DNL Amazon Marketplace]国（[store integration](./store-integration.md)の間に定義）にマップできます。 ただし、このマッピングでは、価格が異なる複数のWebサイトに製品が存在する場合に、どの価格を公開するかという問題が生じます。
