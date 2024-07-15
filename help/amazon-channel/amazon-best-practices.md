---
title: ベストプラクティスと制限事項  [!DNL Amazon sales channel]
description: Adobe CommerceとMagento Open SourceにAmazonのセールスチャネルを使用する際のベストプラクティスと制限事項を確認します。
role: Leader, Admin, User
feature: Sales Channels, Best Practices
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# [!DNL Amazon sales channel] のベストプラクティスと制限事項

ベストプラクティスは次のとおりです。

- Amazonのセールスチャネルは、価格の増減、商品情報（在庫を含む）、リストの追加、更新、終了（削除）を行うことで、Amazonのリストに影響を与える可能性があります。 設定中にステータス別にリストを確認し、ストアの設定を完了する前に設定（[ リスト設定 ](./listing-settings.md)、[ リストルール ](./listing-rules.md)、[ 価格ルール ](./pricing-products.md)、[ 上書き ](./overrides.md) など）を調整します。 これらの設定は、必要に応じてセットアップ後に変更することもできます。

- Amazonのセールスチャネルでは、価格ルールを設定して、リスト価格を自動調整できます。 自動価格設定のセーフガードには、[ インテリジェントな再価格設定ルール ](./floor-price.md) の [ フロア価格 ](./optional-ceiling-price.md) および [ オプションの天井価格 ](./intelligent-repricing-rules.md) 機能が含まれます。 これらの安全策を使用すると、リスト価格がコストを下回ったり、定義された価格を超えたりしないようにすることができます。

- AmazonのセールスチャネルとAmazonの間のデータ同期は、[[!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) 設定によって制御されます。 [!DNL Commerce] とAmazonの間に組み込まれたスロットリングにより、データ転送をスムーズかつ効率的に行うことができますが、e コマースのトラフィックが多い時間（ブラックフライデーなど）は、Amazon システムの更新に通常より時間がかかる場合があります。 [!DNL Commerce] cron を 5 分に 1 回実行するように設定します。

- Amazon販売チャネルは、Amazonの注文情報をインポートします。 AmazonのセールスチャネルでAmazonの注文を管理するには、Amazonの注文ごとに対応する [!DNL Commerce] 注書をインポートして作成するように [ 注文設定 ](./order-settings.md) が定義されていることを確認する必要があります。 定義されていない場合、Amazonの注文情報のみを表示できます。 Amazonを通じた売上に対するすべての税金は、引き続き [!DNL Amazon Seller Central] アカウントを通じて管理され、送金されます。 一部の州では、Amazonは税金の自動徴収と送金を義務づけられています。 他の州では、売り手は手動または自動的に税金を計算するオプションがあります。 [Amazon：税務ポリシー ](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"} を参照してください。 Amazonの税務ポリシードキュメントを表示するには、[!DNL Amazon Seller Central] アカウントにログインする必要が生じる場合があります。

- 英国の場合、Amazonのセールスチャネルにオンボーディングする前に、[Amazon VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} に登録することをお勧めします。

  >[!NOTE]
  >
  >Amazonが VAT Calculation Service アカウントを確認して有効化するまで、10～14 日かかる場合があります。

次のような制限があります。

- [!DNL Commerce] カタログの一部であるバンドル、ギフトカード、グループ化された製品タイプは、AmazonにリストするAmazon セールスチャネルではサポートされていません。

- Amazonのセールスチャネルでは、既存または以前のAmazon リストがない商品のリストを作成することはできません。 商品が ASIN を使用して [!DNL Amazon Seller Central] に存在しない場合は、Amazonがその商品を ASIN に割り当てることができるように、[!DNL Amazon Seller Central] に追加する必要があります。 商品がAmazonに追加され、リストが作成されると、そのリストをAmazon sales channel のカタログと照合して同期できます。
