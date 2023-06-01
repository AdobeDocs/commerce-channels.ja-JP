---
title: 「概要 [!DNL Amazon Marketplace]"
description: 製品カタログをAmazon Marketplace のリストとして活用して、Adobe CommerceまたはMagento Open Sourceストアのリーチを拡大します。
exl-id: d4943d40-773e-4635-aca4-ae40f8ada7bd
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# について [!DNL Amazon Marketplace]

[[!DNL Amazon Marketplace]](https://sell.amazon.com/){target="_blank"} は、Amazonが所有および運営する e コマースプラットフォームで、サードパーティの販売者が新しい製品や中古製品を販売できるようにします。 使用 [!DNL Amazon Marketplace]、サードパーティ販売者は、Amazonの世界規模の顧客ベースにアクセスできます。 Adobe CommerceやMagento Open Sourceのユーザーを含む、Amazonで販売する商品をリストする商人は、Amazonによって「サードパーティの販売者」と定義されます。

任意のサイズのサードパーティ販売者は、 [!DNL Amazon Seller Central] アカウントと [!DNL Amazon Marketplace] Amazonのグローバルカスタマーベースに到達する アカウントを作成してアクティブにした後、販売者は、販売用に製品の追加とリスト作成、注文と在庫の管理、注文の履行をおこなうことができます。

## Amazon Listings

Amazonの一覧には、次の 2 つのカテゴリの情報が含まれます。 **製品情報** および **リスト情報**.

### 製品情報

製品情報は、Amazonにリストされている同じ製品のすべてのインスタンスに共通のデータを提供します。 例えば、複数の販売者がAmazonで特定のブランドのヨガパンツをリストする場合があります。 製品の一般的な詳細（名前やモデル番号など）は、製品がリストされるたびに同じです。 複数の販売者が製品にデータを提供する場合、Amazonは、製品の詳細ページに表示される販売者の製品情報を特定します。

### リスト情報

リスト情報は、製品に関する販売者固有の情報を提供します。 これらの詳細は、多くの場合、同じ製品に関する他の販売者のリストとは異なります。 例えば、他の販売者と同じヨガパンツを販売する場合がありますが、商品番号、条件、価格、輸送方法/時間は異なる場合があります。 これらの詳細は、製品のリストに固有です。

製品情報の投稿や、製品の詳細ページでの誤った情報の修正を行う場合は、 [Amazon:製品の詳細](https://sellercentral.amazon.com/gp/help/external/200335450){target="_blank"}.

## Amazon達成

Amazonは、注文の受け渡しと配送の 2 つのオプションを提供します。

- **商人 (FBM) によって実行される**:サードパーティの販売者は、自分の在庫を保存します。 顧客が注文を行うと、販売者は顧客に対して包装と出荷を処理する。 このオプションを使用すると、Adobe Commerce、Magento Open Source、または別のサードパーティを通じて出荷を完了できます。

- **Amazon(FBA) で実現**:サードパーティの販売者は、世界中のAmazonのフルフィルメントセンターに在庫を保存します。 お客様が注文すると、Amazonはパッケージを処理し、お客様への発送を処理します。 注文の詳細とステータスは、Adobe CommerceまたはMagento Open Sourceに送信されます。

この [!DNL Amazon Sales Channel] 拡張機能は、これらの注文の受信と追跡の両方のオプションをサポートしています。 達成が完了すると、オーダーのステータスが自動的に更新されます。 詳しくは、 [達成ワークフロー](./fulfillment-workflows.md).

## Amazonで販売する前に

Amazonは、すべての販売者と製品が指定されたガイドラインに従うよう、一連のポリシーとワークフローに従います。 お使いの製品とアカウントが承認され、リストに登録できることを確認するには、次のAmazonの情報およびポリシーを確認する必要があります。

- [Amazon販売者向けヘルプ](https://sellercentral.amazon.com/gp/help/external/help-page.html?itemID=2&amp;language=en_US/){target="_blank"}
- [発送ポリシー](https://sellercentral.amazon.com/gp/help/external/201901620?language=en-US){target="_blank"}
- [プログラムポリシー](https://sellercentral.amazon.com/gp/help/external/521?language=en-US){target="_blank"}
- [販売ポリシーと行動規範](https://sellercentral.amazon.com/gp/help/external/1801?language=en-US){target="_blank"}
- [Amazonで更新（リフュース済み、事前所有、オープンボックス）された製品のリスト](https://sell.amazon.com/programs/renewed){target="_blank"}
