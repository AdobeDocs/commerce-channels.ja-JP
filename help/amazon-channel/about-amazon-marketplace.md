---
title: 「情報  [!DNL Amazon Marketplace]」
description: Amazon Marketplace のリストとしてMagento Open Sourceカタログを活用することで、Adobe Commerceや商品ストアのリーチを広げることができます。
role: Leader, Admin, User
feature: Sales Channels, Tools and External Services
exl-id: d4943d40-773e-4635-aca4-ae40f8ada7bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# [!DNL Amazon Marketplace] について

[[!DNL Amazon Marketplace]](https://sell.amazon.com/){target="_blank"} は、Amazonが所有および運営する e コマースプラットフォームで、サードパーティのセラーが新製品や中古製品を販売できるようにします。 [!DNL Amazon Marketplace] を使用すると、サードパーティセラーはAmazonのワールドワイドなカスタマーベースにアクセスできます。 Adobe CommerceやMagento Open Sourceユーザーなど、Amazon上で販売用に商品をリストするマーチャントは、Amazonで「サードパーティセラー」と定義されています。

あらゆる規模のサードパーティセラーは、[!DNL Amazon Seller Central] アカウントを作成し、[!DNL Amazon Marketplace] を使用してAmazonのグローバルカスタマーベースにアクセスできます。 アカウントを作成してアクティブにすると、セラーは販売用の製品を追加してリストし、注文と在庫を管理し、注文をフルフィルメントできます。

## Amazonの一覧

Amazonのリストには、**product information** と **listing information** の 2 つのカテゴリがあります。

### 商品情報

商品情報は、Amazonに一覧表示される同じ商品のすべてのインスタンスに共通のデータを提供します。 例えば、いくつかのセラーがAmazonで特定のヨガパンツをリストしているかもしれません。 名前やモデル番号など、製品の一般的な詳細は、製品がリストされるたびに同じです。 複数の販売者が商品にデータを提供する場合、Amazonは、商品の詳細ページに表示される販売者の商品情報を決定します。

### リスト情報

リスト情報は、製品に関する販売者固有の情報を提供します。 これらの詳細は、多くの場合、同じ製品の他のセラーのリストとは異なります。 例えば、他の販売者と同じヨガパンツを販売する場合がありますが、商品番号、条件、価格、配送方法/時間は異なる場合があります。 これらの詳細は、製品のリストに固有です。

商品の詳細ページに商品の情報を提供したり、誤った情報を修正したりする場合は、[Amazon：商品の詳細 ](https://sellercentral.amazon.com/gp/help/external/200335450){target="_blank"} を参照してください。

## Amazon フルフィルメント

Amazonには、注文のフルフィルメントと配送の 2 つのオプションがあります。

- **マーチャント（FBM）によって履行**：第三者の売り手は自分の在庫を保管します。 お客様が注文すると、売り手はお客様への包装と出荷を処理します。 このオプションを使用すると、Adobe CommerceとMagento Open Source、または他のサードパーティを通じて出荷を完了できます。

- **Amazon（FBA）で履行**：サードパーティのセラーは、世界中のAmazonのフルフィルメントセンターに在庫を保管します。 お客様が注文を行うと、Amazonはパッケージ化と配送をお客様に対して処理します。 注文の詳細とステータスは、Adobe CommerceまたはMagento Open Sourceに送信されます。

[!DNL Amazon Sales Channel] 拡張機能は、これらの注文の受信と追跡の両方のオプションをサポートしています。 フルフィルメントを完了すると、注文ステータスが自動的に更新されます。 [ フルフィルメントワークフロー ](./fulfillment-workflows.md) を参照してください。

## Amazonで販売する前に

Amazonは、すべてのセラーと商品が特定のガイドラインに準拠するよう、一連のポリシーとワークフローに従います。 商品とアカウントが承認され、リストへの登録が可能であることを確認するには、次のAmazonの情報とポリシーを確認してください。

- [Amazon セラーのヘルプ ](https://sellercentral.amazon.com/gp/help/external/help-page.html?itemID=2&amp;language=en_US/){target="_blank"}
- [ 運送約款 ](https://sellercentral.amazon.com/gp/help/external/201901620?language=en-US){target="_blank"}
- [ プログラムポリシー ](https://sellercentral.amazon.com/gp/help/external/521?language=en-US){target="_blank"}
- [ 販売方針及び行動規範 ](https://sellercentral.amazon.com/gp/help/external/1801?language=en-US){target="_blank"}
- [Amazonで更新済み（再生済み、中古、およびオープンボックス）の製品を一覧表示する ](https://sell.amazon.com/programs/renewed){target="_blank"}
