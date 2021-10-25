---
title: 価格スコープ
description: Commerce の価格設定を使用して、複数の web サイトまたは世界で価格を管理します。
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# 価格スコープ

[!DNL Commerce] 価格設定についての設定を [ ](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price) 指定します。 {target = &quot;_blank&quot;} は or に設定され `Global` `Website` ます。 価格がに設定されている場合は `Global` 、すべての web サイトに対して1つの価格ソースがあります。 価格設定がに設定されている場合 `Website` 、web サイトでは、1つの割引価格とデフォルトの価格値を使用することができます。 [ ](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price) コア Commerce ユーザーガイドのカタログ価格 {target = &quot;_blank&quot;} を参照してください。

カタログ価格スコープをからに変更した場合 `Global` `Website` 、すべての価格タイプ属性もに変更さ `Website` れます。 Web サイトの追加を参照してください [ ](https://docs.magento.com/user-guide/stores/stores-all-create-website.html) {target = &quot;_blank 「}」を参照してください。

Web サイト価格を選択した場合は、次の2つの価格ソースがあります。

- Web サイト価格
- デフォルト (フォールバック) 価格

Amazon セールスチャネルとの統合については、リスティングのルールに基づいて、 [ ](./listing-rules.md) 複数の web サイトの製品を1つの国にマップでき [!DNL Amazon Marketplace] ます (ストア統合の際に定義され [ ](./store-integration.md) ます)。 ただし、このような対応付けによって、価格が異なる複数の web サイトに製品が存在する場合に価格がどのように公開されるかという問題が導入されます。
