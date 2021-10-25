---
title: Amazon sales チャンネルのベストプラクティスと制限
description: Adobe Commerce および Magento Open Source の Amazon sales チャンネルを使用した場合のベストプラクティスと制限について検討してください。
exl-id: 7f7faae1-7aa7-413c-b534-1039e6a35173
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Amazon sales チャンネルのベストプラクティスと制限

ベストプラクティスは以下のとおりです。

- Amazon 販売チャンネルが amazon リストに反映されるのは、価格の増減、製品情報の同期 (利用可能な在庫を含む)、および一覧の追加、更新、および削除です。 セットアップ中に状態を表示してリストを確認し、設定を変更し [ ます (一覧表示 ](./listing-settings.md) 、登録、 [ ](./listing-rules.md) [ 価格ルール ](./pricing-products.md) 、 [ 上書き ](./overrides.md) など)。 これらの設定は、必要に応じて、セットアップ後に変更することもできます。

- Amazon sales channel を使用すると、価格設定ルールを設定して、出展価格を自動的に調整することができます。 自動価格保護対策には、「 [ フロア価格」 ](./floor-price.md) および「 [ ](./optional-ceiling-price.md) 高度な再価格設定の最高価格機能」が含まれて [ ](./intelligent-repricing-rules.md) います。 このような保護対策を使用すると、出展価格がコストを下回ることや、定義された価格を超えないようにすることができます。

- Amazon 販売チャンネルと Amazon 間のデータ同期は、 [[!DNL Commerce]  cron ](https://docs.magento.com/user-guide/system/cron.html) {target = &quot;_blank&quot;} 設定によって制御されます。 との間では [!DNL Commerce] 、円滑かつ効率的なデータ伝送が保証されるように機能が制限されていますが、電子商取引のトラフィックにかかる時間 (Black 金曜など) では、Amazon のシステムによって更新に通常より時間がかかる場合があります。 [!DNL Commerce]5 分ごとに cron を実行するように設定します。

- Amazon sales チャンネルによって、Amazon の注文情報が取り込まれます。 Amazon 販売チャンネルの Amazon 注文を管理するには、注文設定が定義されていることを確認し、 [ ](./order-settings.md) 各 amazon 注文に対応する注文を設定しておく必要があり [!DNL Commerce] ます。 定義されていない場合は、Amazon の注文情報のみ表示されます。 Amazon による販売に関するすべての税は、お客様のアカウントを使用して管理および送金され [!DNL Amazon Seller Central] ます。 一部の状況において、税額を自動的に収集して送金するように Amazon が必要な場合があります。 その他の状況については、売り手は手動または自動で税額計算を行うことができます。 [Amazon: Tax Policies and &quot; ](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=200405820&amp;language=en_US/) _blank&quot;} を参照してください。必要に応じて、アカウントにログインして、Amazon 税務署のマニュアルを表示することができ [!DNL Amazon Seller Central] ます。

- UK の地域については、amazon [ VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources/) {target = &quot;_blank&quot;} に登録した後で、amazon 販売チャンネルをオンの状態にすることをお勧めします。


   >[!NOTE]
   >
   >Amazon が VAT 計算サービスアカウントを確認し、アクティブ化するのに10-14 時間がかかる場合があります。

次のような制限があります。

- カタログに含まれているバンドル、ギフトカードおよびグループ化された製品の種類 [!DNL Commerce] は、amazon の一覧表示のために amazon channel channel によってサポートされていません。

- Amazon sales channel は、既にまたは前の Amazon リストがない製品の一覧を作成することはできません。 製品がアーク上に存在しない場合は [!DNL Amazon Seller Central] 、によって追加されたので、Amazon によって製品がアークサインされるようにする必要があり [!DNL Amazon Seller Central] ます。 リストが作成された後、Amazon に製品が追加されると、リストが Amazon sales チャネルのカタログと一致し、同期されます。
