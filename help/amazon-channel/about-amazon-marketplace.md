---
title: Amazon Marketplace について
description: アドビシステムズ社の製品カタログを、Amazon Marketplace の一覧として活用して、Adobe Commerce や Magento のオープンソースストアの対象を拡大します。
exl-id: d4943d40-773e-4635-aca4-ae40f8ada7bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# に関しては [!DNL Amazon Marketplace]

[[!DNL Amazon Marketplace]](https://sell.amazon.com/){target = &quot;_blank&quot;} は、Amazon によって運営および運営されている電子商取引プラットフォームです。これにより、サードパーティの売り手が新製品または使用済み製品を販売できるようになります。 [!DNL Amazon Marketplace]サードパーティの使用により、Amazon のワールドワイド全体のユーザーベースにアクセスすることができます。Amazon に含まれている、アドビシステムズ社の製品をリストする商人は、Adobe Commerce や Magento のオープンソースユーザーも含め、Amazon によって「サードパーティの売り手」と定義されています。

いかなるサイズのサードパーティの売り手も、 [!DNL Amazon Seller Central] アカウントを作成し、を使用して [!DNL Amazon Marketplace] Amazon のグローバルユーザーベースに到達できます。 取引先企業が作成され、有効になると、売り手は、販売用製品の追加と一覧作成、注文と在庫の管理、注文を実行することができます。

## Amazon の一覧

Amazon リストには **、製品情報およびリスティング情報という2種類の情報が含まれ** て **** います。

### 製品情報

製品情報には、Amazon に一覧表示された同じ製品のすべてのインスタンスに共通のデータが含まれています。 例えば、一部の売り手は、Amazon についての特定のブランドのズボンを一覧表示します。 製品についての全般的な詳細情報 (名前やモデル番号など) は、製品がリストされるたびに同じになります。 複数の売り手が製品にデータを提供すると、Amazon は製品の詳細ページにどの販売店の情報が表示されるかが判別されます。

### リスト情報

リスト情報には、製品に関する販売者向け情報が記載されています。 このような詳細情報は、多くの場合、同じ製品の他の売り手のリストとは異なります。 例えば、ある出荷 ga が別の販売者と同じに販売されていても、その品目番号、条件、価格、送付方法は異なる場合があります。 このような詳細情報は、製品の出展によって異なります。

製品情報を contribute に追加する必要がある場合、または製品詳細ページの誤り情報を修正する場合は、 [ Amazon: Product detail ](https://sellercentral.amazon.com/gp/help/external/200335450) {target = &quot;_blank&quot;} を参照してください。

## Amazon フルフィルメント

Amazon は、注文の履行と出荷について2つのオプションを提供します。

- **マーチャントによって履行される (FBM)** : サードパーティの売り手が、独自の在庫を格納します。 顧客が注文を行った場合、売り手は、顧客へのパッケージ化と出荷を行います。 このオプションを使用すると、Adobe Commerce および Magento Open Source またはその他のサードパーティを通じて出荷を完了することができます。

- **Amazon (FBA) によって** 実行されるサードパーティの売り手は、amazon のフルフィルメントセンターで世界各地に在庫を保管します。 ユーザーが注文を行ったときに、Amazon はパッケージ化および出荷をユーザーに対して行います。 注文の詳細およびステータスは、Adobe Commerce または Magento Open Source に送信されます。

拡張機能では、 [!DNL Amazon Sales Channel] これらの注文の受信と追跡の両方のオプションがサポートされています。 手続きが完了すると、注文のステータスは自動的に更新されます。 [フルフィルメントのワークフロー ](./fulfillment-workflows.md) を参照してください。

## Amazon について販売を開始する前に

Amazon は、一連のポリシーおよびワークフローに従い、すべての売り手や製品が指定したガイドラインに従うようにしています。 製品およびアカウントが承認され、出展の対象となることを確認するには、次の Amazon に関する情報とポリシーを確認する必要があります。

- [Amazon 売り手のヘルプ ](https://sellercentral.amazon.com/gp/help/external/help-page.html?itemID=2&amp;language=en_US/) {target = &quot;_blank&quot;}
- [出荷ポリシー ](https://sellercentral.amazon.com/gp/help/external/201901620?language=en-US) {target = &quot;_blank&quot;}
- [プログラムポリシー ](https://sellercentral.amazon.com/gp/help/external/521?language=en-US) {target = &quot;_blank&quot;}
- [販売方針と倫理規範 ](https://sellercentral.amazon.com/gp/help/external/1801?language=en-US) {target = &quot;_blank&quot;}
- [Amazon ](https://sell.amazon.com/programs/renewed) {target = &quot;_blank&quot;} の更新された製品 (調整済み、プレオーナー、およびオープンボックス) 製品の一覧を表示します。
