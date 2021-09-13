---
title: Amazon販売チャネルのベストプラクティスと制限事項
description: AmazonのセールスチャネルをAdobeのコマースとMagento Open Sourceに使用する際のベストプラクティスと制限事項を確認します。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Amazon販売チャネルのベストプラクティスと制限事項

ベストプラクティスは次のとおりです。

- Amazonの販売チャネルは、価格の増減、製品情報（利用可能な在庫を含む）の同期、リストの追加、更新、終了（削除）によってAmazonのリストに影響を与える可能性があります。 設定時に状況に応じてリストを確認し、設定を調整してから（[リスト設定](./listing-settings.md)、[リストルール](./listing-rules.md)、[価格ルール](./pricing-products.md)、[オーバーライド](./overrides.md)など）、ストア設定を完了します。 これらの設定は、必要に応じて、設定後に変更することもできます。

- Amazonのセールスチャネルでは、価格ルールを設定して、上場価格を自動的に調整できます。 自動価格保証には、[下限価格](./floor-price.md)と[オプションの上限価格](./optional-ceiling-price.md)機能[インテリジェントな再価格設定ルール](./intelligent-repricing-rules.md)が含まれます。 これらのセーフガードを使用することで、上場価格がコストを下回ったり、定義された価格を上回ったりしないようにすることができます。

- Amazonの販売チャネルとAmazonの間のデータ同期は、[[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}設定で制御します。 [!DNL Commerce]とAmazonの間に組み込まれているスロットリングは、スムーズで効率的なデータ送信に役立ちますが、eコマースのトラフィックが多い時間帯（ブラックフライデーなど）に、Amazonのシステムの更新に通常より長い時間がかかる場合があります。 [!DNL Commerce] cronを5分に1回実行するように設定します。

- Amazonの販売チャネルは、Amazonの注文情報をインポートします。 Amazonの販売チャネルでAmazonの注文を管理するには、Amazonの各注文をインポートし、対応する[!DNL Commerce]注文を作成するように[注文設定](./order-settings.md)を定義する必要があります。 定義されていない場合は、Amazonの注文情報のみを表示できます。 Amazonを通じた販売に関する税金は、引き続き[!DNL Amazon Seller Central]アカウントを通じて管理および送金されます。 一部の州では、Amazonは自動的に税金を収集して送金する必要があります。 他の州の場合、販売者は、手動または自動で税金を計算するオプションがあります。 [Amazon:税ポリシー](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target=&quot;_blank&quot;}。 Amazonの税務ポリシーに関するドキュメントを表示するには、[!DNL Amazon Seller Central]アカウントにログインする必要が生じる場合があります。

- 英国の地域では、Amazonの販売チャネルをオンボーディングする前に、[Amazon VAT計算サービス](https://sell.amazon.co.uk/learn/vat-resources/){target=&quot;_blank&quot;}に登録することをお勧めします。


   >[!NOTE]
   >
   >AmazonがVAT計算サービスのアカウントを確認して有効化するまでに10 ～ 14日かかる場合があります。

制限事項は次のとおりです。

- [!DNL Commerce]カタログの一部であるバンドル、ギフトカード、グループ化された製品タイプは、Amazonへのリスト用のAmazon販売チャネルではサポートされていません。

- Amazonの販売チャネルは、既存のまたは以前のAmazonリストを持たない製品のリストを作成できません。 製品がASINを持つ[!DNL Amazon Seller Central]に存在しない場合、Amazonが製品にASINを割り当てられるように、[!DNL Amazon Seller Central]に追加する必要があります。 製品がAmazonに追加され、リストが作成されると、そのリストはAmazonの販売チャネルのカタログと一致し、同期されます。
