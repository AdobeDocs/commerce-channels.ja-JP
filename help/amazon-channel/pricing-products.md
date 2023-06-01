---
title: Amazon価格の管理
description: 価格ルールを使用して、Amazonの一覧の価格をコマースストアと異なる値に設定できます。
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Amazon価格の管理

Amazonセールスチャネルを使用すると、価格ルールを設定できます。このルールでは、定義された価格とは異なるAmazonの定価を設定できます **[!UICONTROL Magento Price Source]** の [上場価格](./listing-price.md). また、複数のルールを積み重ねたり、インテリジェント価格を使用して、競合相手の [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格または [最低競争価格](./lowest-competitor-pricing.md).

価格設定ルールには次の 2 種類があります。

- [標準価格ルール](./standard-price-rules.md)
- [インテリジェントな価格変更ルール](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Amazon地域が `Inactive` ステータス（オンボーディング中） 価格の計算は送料によって異なり、地域は `Active` Amazonから同期する送料のステータス。
   >
   >Amazonアカウントで地域のステータスを更新するには、設定/アカウント情報/休暇の設定に移動します。 参照： [Amazon:休暇のステータスのリスト](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) （販売者の中央ログインが必要です）。

この機能を使用すると、Amazonの価格を [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). 複雑なルールを作成して、特定の製品、特定のカテゴリ内の製品、または特定の属性を持つ製品の価格を変更できます。

価格ルールは、Amazonの一覧に追加できます。 価格ルールは、定義された条件に基づいて、自動的に上場価格を調整するために使用できます。 価格ルールがトリガーされ、製品がAmazonに表示される前に調整済みの価格が計算されます。

>[!NOTE]
>
>Amazonリストの価格情報は、 **[!UICONTROL Magento Price Source]** の [上場価格](./listing-price.md) 設定。 価格設定ルールで定義された調整計算では、価格ソースが開始値として使用されます。

価格ルールを使用すると、Amazonの定価を **[!UICONTROL Magento Price Source]** の [上場価格](./listing-price.md) 設定。 また、複数のルールを積み重ねて、価格を調整することもできます。

価格設定/価格変更ルールでは、設定時に次の 3 セットの情報が必要です。

- [一般設定](./pricing-rule-general-settings.md):ルールの名前、説明、アクティブな日付、優先度を定義し、優先度の設定に基づいて後続のルールの動作を設定します。
- [条件](./pricing-rule-conditions.md):価格ルールに適した製品を決定します。
- [アクション](./pricing-rule-actions.md):価格ソースに適用する調整計算を定義して、上場価格を決定します。

次の項目を作成できます。 [標準価格ルール](./standard-price-rules.md) 選択した **[!UICONTROL Magento Price Source]** の [上場価格](./listing-price.md) 設定。 この機能を使用すると、Amazonの価格を [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). 特定の製品、特定のカテゴリ内の製品、または特定の属性を持つ製品の価格を自動的に変更する複雑なルールを作成できます。 従来の設定を完了し、一定の金額または割合に基づいて製品を増減させるための価格を再設定できます。

もう 1 つの強力なツールは、 [インテリジェントな価格変更](./intelligent-repricing-rules.md) 競合他社に基づいてAmazonの定価を調整する機能 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格または [最も低い競合他社価格](./lowest-competitor-pricing.md). 次に類似 [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)この高度な機能を使用すると、複雑なルールを作成してAmazonの価格を操作できます。 ルールは、特定の製品、特定のカテゴリ内の製品、または特定の製品属性を持つ製品に対する価格変更の範囲を定義できます。

インテリジェントな価格設定を使用して、競合相手の価格に基づいてAmazonの上場価格を調整します。 Amazonのセールスチャネルは、マージンを保護したり、低いフィードバックで商人の価格と一致しないように設定するためのセーフガードを組み込んでいます。 使用 [インテリジェントなリプライシングルール](./intelligent-repricing-rules.md)、Amazonの上場価格は、固定金額や割合（上下）として自動的に操作したり、 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格または [最も低い競合他社価格](./lowest-competitor-pricing.md) 項目ごとに。 ルールを積み重ねることもでき、柔軟性に制限なく対応できます。

アクティブ/非アクティブステータス、Web サイトの適格性、オプションの日付範囲、オプションの優先度レベル（ルールの積み重ねに使用）など、ルールの重要な側面を制御できます。

例えば、価格ルールの条件を定義および設定して、条件が満たされた場合、Amazonに送信する前に掲載価格を自動的に調整できます。

もう 1 つの価格オプションは、 [価格の上書き](./overrides.md)：個々のリストレベルで設定されます。 A [価格の上書き](./overrides.md) を設定でき、上書きは、その他すべてのデフォルト、設定、ルールよりも無視または優先されます。 An [上書き](./overrides.md) は、価格、取り扱い時間、条件、販売者向けのメモに設定できます（一部の例外を除く）。

![価格ルール](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Name] | 価格ルールの名前 ( [価格ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | ルールタイプ（で設定） [価格設定ルールの処理](./pricing-rule-actions.md) （標準価格ルールまたはインテリジェント再価格ルール） |
| [!UICONTROL Is Active] | ルールがアクティブかどうか ( [価格ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | 他の価格条件に対する優先度 ( [価格ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | このルールに該当する製品に対して、それ以上の価格ルールが処理されるかどうかを示します ( [価格ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | ルールがアクティブな期間の開始 |
| [!UICONTROL To Date] | ルールがアクティブな期間の終わり |
| [!UICONTROL Action] | 特定のリストに適用できるすべてのアクションをリストします。 アクションを適用するには、 **[!UICONTROL Select]** 内 _[!UICONTROL Action]_列。 オプション： `Edit Price Rule` / `Delete Price Rule` |
