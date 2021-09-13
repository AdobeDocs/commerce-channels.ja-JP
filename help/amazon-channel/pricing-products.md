---
title: Amazon価格の管理
description: 価格ルールを使用して、Amazonの価格をコマースストアと異なる価格に設定できます。
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Amazon価格の管理

Amazonの販売チャネルを使用すると、価格ルールを設定できます。これにより、[上場価格](./listing-price.md)で定義した&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;とは異なるAmazonの上場価格を設定できます。 また、複数のルールを積み重ね、インテリジェントな価格を使用して、競合相手の[[!DNL Buy Box]](./buy-box-competitor-pricing.md)価格または[最も低い競合相手の価格](./lowest-competitor-pricing.md)に基づいてAmazonの上場価格を調整することもできます。

価格設定ルールには、次の2つのタイプがあります。

- [標準価格設定ルール](./standard-price-rules.md)
- [インテリジェントな価格変更ルール](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Amazon地域が`Inactive`ステータスに設定されている場合、オンボーディング中と同様に、インテリジェントな価格変更ルールは正しく機能しません。 価格の計算は送料によって異なります。Amazonから同期するには、お住まいの地域のステータスが`Active`である必要があります。
   >
   >Amazonアカウントの地域ステータスを更新するには、設定/アカウント情報/休暇の設定に移動します。 [Amazonを参照：Vacations](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){:target=&quot;_blank&quot;}のリストステータス（セラーの中央ログインが必要）。

この機能を使用すると、Amazonの価格を[!DNL Commerce] [カタログ価格ルール](https://docs.magento.com/user-guide/catalog/pricing.html){:target=&quot;_blank&quot;}に似た方法で操作できます。 特定の製品、特定のカテゴリ内の製品、または特定の属性を持つ製品の価格を変更できる複雑なルールを作成できます。

価格ルールは、Amazonのリストに追加できます。 価格ルールを使用して、定義済みの条件に基づいて、上場価格を自動的に調整できます。 価格ルールがトリガーされ、製品がAmazonに表示される前に調整された価格が計算されます。

>[!NOTE]
>
>Amazonリストの価格のソースは、[リスト価格](./listing-price.md)設定の&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;に対して定義されます。 価格設定ルールで定義された調整計算では、価格ソースが開始値として使用されます。

価格ルールを使用すると、Amazonの定価を[定価](./listing-price.md)設定の&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;とは異なる値に設定できます。 また、複数のルールを積み重ねて、価格を調整することもできます。

価格設定/再価格設定ルールでは、設定時に3組の情報が必要です。

- [一般設定](./pricing-rule-general-settings.md):ルールの名前、説明、アクティブな日付、優先度を定義し、優先度の設定に基づいて後続のルールの動作を設定します。
- [条件](./pricing-rule-conditions.md):価格ルールに適格な製品を決定します。
- [アクション](./pricing-rule-actions.md):価格ソースに適用される調整計算を定義して、上場価格を決定します。

[標準の価格ルール](./standard-price-rules.md)を作成して、[リスト価格](./listing-price.md)設定で選択した&#x200B;**[!UICONTROL Magento Price Source]**&#x200B;に対して、Amazonのリスト価格を自動的に調整できます。 この機能を使用すると、Amazonの価格を[!DNL Commerce] [カタログ価格ルール](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}に似た方法で操作できます。 特定の製品、特定のカテゴリ内の製品、または特定の属性を持つ製品の価格を自動的に変更する複雑なルールを作成できます。 従来の設定を完了し、一定の金額または割合に基づいて商品を増減させるための価格を再設定できます。

もう1つの強力なツールは、[インテリジェントリプライシング](./intelligent-repricing-rules.md)機能です。この機能は、競合相手の[[!DNL Buy Box]](./buy-box-competitor-pricing.md)価格または[競合相手の最低価格](./lowest-competitor-pricing.md)に基づいてAmazonの上場価格を調整します。 [!DNL Commerce] [カタログ価格ルール](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){:target=&quot;_blank&quot;}と同様に、この高度な機能を使用すると、複雑なルールを作成してAmazonの価格を操作できます。 ルールは、特定の製品、特定のカテゴリ内の製品、または特定の製品属性を含む製品に対する価格変更の範囲を定義できます。

インテリジェントな価格変更を使用して、競合相手の価格に基づいてAmazonの上場価格を調整します。 Amazonの販売チャネルは、マージンを保護したり、低いフィードバックで商人の価格と一致しないように設定するためのセーフガードを組み込んでいます。 [インテリジェントな再価格設定ルール](./intelligent-repricing-rules.md)を使用すると、Amazonの上場価格を固定金額または割合（上下）として自動的に操作したり、品目単位で[[!DNL Buy Box]](./buy-box-competitor-pricing.md)価格や[Lowest Competitor Price](./lowest-competitor-pricing.md)に同期させたりできます。 ルールを積み重ねることで、柔軟性も無制限になります。

アクティブ/非アクティブなステータス、Webサイトの実施要件、日付範囲、オプションの優先度レベル（ルールの積み重ねに使用）など、ルールの重要な側面を制御できます。

例えば、Amazonに送信する前に、条件が満たされた場合に表示価格を自動的に調整する価格ルールの条件を定義し、設定できます。

もう1つの価格オプションは、[価格の上書き](./overrides.md)で、個々の上場レベルで設定されます。 [価格の上書き](./overrides.md)を設定でき、上書きは、他のすべてのデフォルト、設定、ルールよりも優先されます。 [override](./overrides.md)は、価格、処理時間、条件、販売者向けのメモに設定できます（一部の例外を除く）。

![価格ルール](assets/amazon-pricing-rules.png)

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Name] | [価格ルールの一般設定](./pricing-rule-general-settings.md)で設定された、価格ルールの名前 |
| [!UICONTROL Rule Type] | [価格ルールアクション](./pricing-rule-actions.md)（標準価格ルールまたはインテリジェント再価格ルール）で設定されたルールタイプ |
| [!UICONTROL Is Active] | [価格ルールの一般設定](./pricing-rule-general-settings.md)で設定されたように、ルールがアクティブかどうか |
| [!UICONTROL Priority] | [価格ルールの一般設定](./pricing-rule-general-settings.md)で設定されている、他の価格条件よりも優先度 |
| [!UICONTROL Stop Further Rules Processing] | [価格ルールの一般設定](./pricing-rule-general-settings.md)で設定されているように、このルールに該当する製品に対して追加の価格ルールが処理されるかどうかを示します。 |
| [!UICONTROL From Date] | ルールがアクティブな期間の開始 |
| [!UICONTROL To Date] | ルールがアクティブな期間の終わり |
| [!UICONTROL Action] | 特定のリストに適用できるすべてのアクションをリストします。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックします。 オプション：`Edit Price Rule` / `Delete Price Rule` |
