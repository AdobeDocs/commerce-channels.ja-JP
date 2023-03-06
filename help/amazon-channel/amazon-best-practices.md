---
title: Amazonセールスチャネルのベストプラクティスと制限事項
description: Adobe CommerceとMagento Open SourceでAmazonセールスチャネルを使用する際のベストプラクティスと制限事項を確認します。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# AmazonSales Channelのベストプラクティスと制限事項

ベストプラクティスは次のとおりです。

- Amazonのセールスチャネルは、価格の増減、製品情報（利用可能な在庫を含む）の同期、リストの追加、更新、終了（削除）によってAmazonのリストに影響を与える可能性があります。 設定時にステータス別にリストを確認し、設定を調整します ([リスト設定](./listing-settings.md), [リストルール](./listing-rules.md), [価格ルール](./pricing-products.md), [上書き](./overrides.md)など ) を含めてからストアの設定を完了する必要があります。 これらの設定は、必要に応じて、設定後に変更することもできます。

- Amazonのセールスチャネルでは、上場価格を自動的に調整する価格ルールを設定できます。 自動価格保護には、 [価格](./floor-price.md) および [オプションの上限価格](./optional-ceiling-price.md) の特徴 [インテリジェントな価格変更ルール](./intelligent-repricing-rules.md). これらのセーフガードを使用すると、上場価格がコストを下回ったり、定義された価格を上回ったりしないようにすることができます。

- AmazonセールスチャネルとAmazon間のデータ同期は、 [[!DNL Commerce] cron](https://docs.magento.com/user-guide/system/cron.html){target="_blank"} 設定。 次の間の組み込みのスロットル： [!DNL Commerce] とAmazonは、スムーズで効率的なデータ転送を実現しますが、e コマースのトラフィックが多い時間帯（ブラックフライデーなど）には、Amazonのシステムの更新に通常よりも時間がかかる場合があります。 を [!DNL Commerce] cron は 5 分に 1 回実行します。

- Amazonのセールスチャネルは、Amazonの注文情報をインポートします。 AmazonセールスチャネルでAmazonの注文を管理するには、 [順序設定](./order-settings.md) は、対応する [!DNL Commerce] 各Amazon注文の注文。 定義されていない場合は、Amazonの注文情報のみ表示できます。 Amazonを通じた販売に関するすべての税金は、引き続き、 [!DNL Amazon Seller Central] アカウント 一部の州では、Amazonは自動的に税金を収集して送金する必要があります。 他の州の場合、販売者は、税金を手動または自動で計算するオプションがあります。 詳しくは、 [Amazon:税金ポリシー](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/){target="_blank"}. 場合によっては、 [!DNL Amazon Seller Central] Amazon税ポリシードキュメントを表示するアカウント

- 英国の地域の場合、に登録することがベストプラクティスです [AmazonVAT 計算サービス](https://sell.amazon.co.uk/learn/vat-resources/){target="_blank"} Amazonセールスチャネルをオンボーディングする前に


   >[!NOTE]
   >
   >Amazonが VAT 計算サービスアカウントを検証および有効化するまでに 10 ～ 14 日かかる場合があります。

制限事項は次のとおりです。

- バンドル、ギフトカード、およびグループ化された製品タイプが、 [!DNL Commerce] カタログは、AmazonセールスチャネルでAmazonにリストする際にはサポートされていません。

- Amazonセールスチャネルは、既存または以前のAmazonリストを持たない製品のリストを作成できません。 製品が [!DNL Amazon Seller Central] ASIN を使用する場合は、 [!DNL Amazon Seller Central] Amazonが製品を ASIN に割り当てられるようにするために使用します。 Amazonで製品が追加され、リストが作成されると、そのリストをAmazonセールスチャネルのカタログと照合し、同期できます。
