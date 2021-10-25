---
title: Amazon 価格の管理
description: このような Amazon リストの価格設定は、価格設定ルールを使用して、Amazon リストとは異なるように設定することができます。
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Amazon 価格の管理

Amazon sales channel を使用すると、価格設定ルールを設定することができます。これにより、掲載価格で定義されているものとは異なる、Amazon の表示価格を設定することができ **[!UICONTROL Magento Price Source]** [ ](./listing-price.md) ます。 また、複数のルールをスタックすることもできます。さらに、知的価格設定を使用して、競合企業の価格や競合他社の価格に基づいて、Amazon のリスト価格を調整することもでき [[!DNL Buy Box]](./buy-box-competitor-pricing.md) [ ](./lowest-competitor-pricing.md) ます。

価格設定ルールには、次の2つのタイプがあります。

- [標準価格設定ルール](./standard-price-rules.md)
- [インテリジェントな再価格ルール](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Amazon 地域が状態に設定されているとき `Inactive` は、オンになっているとしても、インテリジェントな価格設定ルールは正常に機能しません。 価格計算は、配達料金によって異なります。また、地域が Amazon よりも `Active` 出荷料金を同期するための状態である必要があります。
   >
   >Amazon account に含まれる地域の状態を更新するには、設定 > 取引先企業情報 > 休暇設定に移動してください。 [Amazon: 休暇の状態の一覧表示 ](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) {target = &quot;_blank&quot;} (売り手の中央ログインが必要) を参照してください。

この機能を使用すると、 [!DNL Commerce] [ カタログ価格ルール ](https://docs.magento.com/user-guide/catalog/pricing.html) {target = &quot;_blank&quot;} のような形式で、Amazon 価格を操作できます。 複雑なルールを作成して、特定の製品、特定のカテゴリ内の製品、または特定の属性に対して価格を変更することができます。

Amazon リストには価格設定ルールを追加することができます。 価格ルールを使用して、定義された一連の条件に基づいて、出展価格を自動的に調整することができます。 この製品が Amazon 上のリストに表示される前に、価格ルールがトリガーされ、調整価格が計算されます。

>[!NOTE]
>
>Amazon リストの価格ソースは、 **[!UICONTROL Magento Price Source]** 出展価格設定に定義されてい [ ](./listing-price.md) ます。 価格設定ルールで定義された調整計算は、開始値として価格ソースを使用します。

価格設定によって、Amazon の表示価格が **[!UICONTROL Magento Price Source]** 掲載価格の設定とは異なる設定ができ [ ](./listing-price.md) ます。 また、複数のルールを重ね合わせて、価格を調整することもできます。

価格設定と再設定ルールを設定するには、セットアップ中に3セットの情報セットが必要になります。

- [全般設定 ](./pricing-rule-general-settings.md) : ルールの名前、説明、アクティブな日付、優先度を定義し、その優先度の設定に基づいて、後続のルールの動作を設定します。
- [条件 ](./pricing-rule-conditions.md) : 価格ルールの対象となる製品を指定します。
- [アクション ](./pricing-rule-actions.md) : 価格ソースに適用される調整計算を定義して、定価を指定します。

[ ](./standard-price-rules.md) **[!UICONTROL Magento Price Source]** カタログ登録価格設定で選択されていることを基準にして、Amazon の一覧価格が自動的に調整される標準価格ルールを作成することができ [ ](./listing-price.md) ます。この機能を使用すると、 [!DNL Commerce] [ カタログ価格ルール ](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html) {target = &quot;_blank&quot;} のような形式で、Amazon 価格を操作できます。 複雑なルールを作成して、特定の製品、特定のカテゴリの製品、または特定の属性を持つ製品の価格を自動的に変更することができます。 このような場合は、従来の設定を入力して製品を再価格化することで、固定額または一定率に基づいて増加または減少させることができます。

もう1つの強力なツールは、 [ ](./intelligent-repricing-rules.md) 競合他社の [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格、または競合企業の最低価格に基づいて Amazon の一覧価格を調整するインテリジェントな再価格機能です [ ](./lowest-competitor-pricing.md) 。 [!DNL Commerce] [ カタログ価格ルールと同様に ](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html) {target = &quot;_blank&quot;}、この高度な機能を使用すると、複雑なルールを作成することによって、Amazon 価格を操作できます。ルールでは、特定の製品に対する価格変更のスコープ、特定のカテゴリに含まれる製品、さらには特定の製品属性を定義できます。

インテリジェントな再価格設定を使用して、競合企業の価格設定に基づいて、Amazon リスト価格を調整します。 Amazon 販売チャンネルには、マージンを保護するために設定したり、低フィードバックの値段に適合させないようにするための保護機能が組み込まれています。 インテリジェントな再価格設定を使用すると [ ](./intelligent-repricing-rules.md) 、Amazon の一覧価格は、固定量または割合 (上または下) として自動的に操作されるか、または、品目ごとに価格またはその下の競合価格に同期されるようになって [[!DNL Buy Box]](./buy-box-competitor-pricing.md) [ ](./lowest-competitor-pricing.md) います。 ルールをスタックすると、柔軟に制限することができます。

アクティブ/非アクティブ状態、web サイトの適格性、日付の範囲の指定、オプションの優先度 (ルールのスタックに使用) など、ルールの重要な側面を制御できます。

たとえば、条件が満たされたときに、Amazon に送信される前にリスト価格を自動的に調整する価格ルールの条件を定義して設定することができます。

もう1つの価格設定オプションは、 [ ](./overrides.md) 個々のリストレベルで設定される価格上書きです。 [価格設定を変更する ](./overrides.md) ことができます。上書きは、その他のすべてのデフォルト、設定およびルールに対して無視または適用されます。上書きは、 [ ](./overrides.md) 価格、手数料、条件、および販売店の注意を設定することができます。ただし、いくつかの例外はありません。

![価格ルール](assets/amazon-pricing-rules.png)

## デフォルトの列

| 段 | つい |
|---|---|
| [!UICONTROL Name] | 価格ルールの「一般設定」で設定されている価格ルールの名前 [](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | 価格ルールアクションに設定されたルールタイプ [ ](./pricing-rule-actions.md) (標準価格ルールまたはインテリジェント再価格ルール) |
| [!UICONTROL Is Active] | 「 [ 価格ルールの一般設定」で設定されているルールがアクティブかどうかを示します。](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | [価格ルールの「一般設定」で設定されたその他の価格条件の優先順位](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | このルールに該当する製品に対して、さらに価格ルールが処理されるかどうかを示します。「一般設定」で設定します。 [](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | ルールが有効になっている期間の開始 |
| [!UICONTROL To Date] | ルールが有効になっている期間の終わり |
| [!UICONTROL Action] | 特定のリストに適用できるすべてのアクションを一覧表示します。 アクションを適用するには、列内をクリックし **[!UICONTROL Select]** _[!UICONTROL Action]_ます。 オプション: `Edit Price Rule` / `Delete Price Rule` |
