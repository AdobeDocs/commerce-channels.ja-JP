---
title: のベストプラクティスと制限事項 [!DNL Amazon sales channel]
description: Adobe CommerceとMagento Open SourceにAmazonのセールスチャネルを使用する際のベストプラクティスと制限事項を確認します。
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# のベストプラクティスと制限事項 [!DNL Amazon sales channel]

ベストプラクティスは次のとおりです。

- Amazonのセールスチャネルは、価格の増減、商品情報（在庫を含む）、リストの追加、更新、終了（削除）を行うことで、Amazonのリストに影響を与える可能性があります。 セットアップ中にステータス別にリストを確認し、設定を調整します（[リスト設定](./listing-settings.md), [リストルール](./listing-rules.md), [価格ルール](./pricing-products.md), [上書き](./overrides.md)など）、ストアの設定を完了する前に実行します。 これらの設定は、必要に応じてセットアップ後に変更することもできます。

- Amazonのセールスチャネルでは、価格ルールを設定して、リスト価格を自動調整できます。 自動化された価格設定の保護には、次のものがあります [床価格](./floor-price.md) および [オプションの上限価格](./optional-ceiling-price.md) の機能 [インテリジェントな再価格設定ルール](./intelligent-repricing-rules.md). これらの安全策を使用すると、リスト価格がコストを下回ったり、定義された価格を超えたりしないようにすることができます。

- AmazonのセールスチャネルとAmazonの間のデータ同期は、 [[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 設定。 次の間の組み込みスロットル [!DNL Commerce] とAmazonは、データ転送をスムーズかつ効率的に行うのに役立ちますが、e コマースのトラフィックが多い時間（ブラックフライデーなど）は、Amazon システムの更新に通常より時間がかかる場合があります。 を設定 [!DNL Commerce] cron は 5 分に 1 回実行されます。

- Amazon販売チャネルは、Amazonの注文情報をインポートします。 AmazonのセールスチャネルでAmazonの注文を管理するには、次のことを確認する必要があります。 [オーダー設定](./order-settings.md) 対応するをインポートおよび作成するために定義されます [!DNL Commerce] Amazonの注文ごとに注文します。 定義されていない場合、Amazonの注文情報のみを表示できます。 Amazonを通じた売上に対するすべての税金は、引き続きお客様を通じて管理され、送金されます [!DNL Amazon Seller Central] アカウント。 一部の州では、Amazonは税金の自動徴収と送金を義務づけられています。 他の州では、売り手は手動または自動的に税金を計算するオプションがあります。 参照： [Amazon：税務ポリシー](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. にログインする必要がある場合があります。 [!DNL Amazon Seller Central] Amazon税ポリシードキュメントを表示するアカウント。

- イギリス地域の場合、 [AmazonVAT 算定サービス](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} Amazon セールスチャネルにオンボーディングする前に。

  >[!NOTE]
  >
  >Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

次のような制限があります。

- バンドル、ギフトカード、 [!DNL Commerce] カタログは、Amazon sales channel がAmazonへのリスト表示でサポートしていません。

- Amazonのセールスチャネルでは、既存または以前のAmazon リストがない商品のリストを作成することはできません。 製品がに存在しない場合 [!DNL Amazon Seller Central] asin を使用する場合は、に追加する必要があります。 [!DNL Amazon Seller Central] これにより、Amazonは商品に ASIN を割り当てることができます。 商品がAmazonに追加され、リストが作成されると、そのリストをAmazon sales channel のカタログと照合して同期できます。
