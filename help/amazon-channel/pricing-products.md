---
title: Amazonの価格の管理
description: 価格設定ルールを使用することで、Amazonのリストの価格をCommerce ストアとは異なる価格に設定できます。
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Amazonの価格の管理

Amazon セールスチャネルでは、Amazonの上場価格を [ 上場価格 ](./listing-price.md) で定義された **[!UICONTROL Magento Price Source]** と異なる価格ルールを設定できます。 また、複数のルールを積み重ね、インテリジェントな価格を使用して、競合他社の [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格または [ 最も低い競合他社価格 ](./lowest-competitor-pricing.md) に基づいてAmazonのリスト価格を調整することもできます。

次の 2 種類の価格設定ルールがあります。

- [標準価格ルール](./standard-price-rules.md)
- [インテリジェント再価格設定ルール](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >Amazon リージョンが `Inactive` ステータスに設定されている場合、オンボーディング中であるので、インテリジェントな価格の再設定ルールは適切に機能しません。 価格の計算は配送料によって異なり、Amazonから配送料を同期するには、お住まいの地域が `Active` ステータスである必要があります。
  >
  >Amazon アカウントの地域ステータスを更新するには、[ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] に移動します。 「[Amazon：休暇のステータスの一覧表示 ](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620)」（Seller Central へのログインが必要）を参照してください。

この機能を使用すると、[!DNL Commerce] カタログ価格ルール [ に似た方法でAmazonの価格を操作でき ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html) す。 特定の製品、特定のカテゴリ内の製品、または特定の属性を使用して価格を変更できる複雑なルールを作成できます。

Amazon リストの価格ルールを追加できます。 価格ルールを使用すると、定義された一連の条件に基づいてリスト価格を自動的に調整できます。 価格ルールがトリガーされ、商品がAmazonにリストされる前に調整済みの価格が計算されます。

>[!NOTE]
>
>Amazonのリストの価格ソースは、「リスト価格 [ 設定で **[!UICONTROL Magento Price Source]** に対して定義され ](./listing-price.md) す。 価格設定ルールで定義された調整計算では、開始値として価格ソースが使用されます。

価格ルールを使用すると、「価格 [ 設定でAmazonの **[!UICONTROL Magento Price Source]** 示価格を自分のオファーとは異なる価格に設定 ](./listing-price.md) きます。 また、複数のルールを積み重ねて、価格を調整することもできます。

価格設定/再価格設定ルールの設定時には、次の 3 つの情報セットが必要です。

- [ 一般設定 ](./pricing-rule-general-settings.md)：ルールの名前、説明、アクティブな日付、優先度を定義し、優先度設定に基づいて後続のルールの動作を設定します。
- [ 条件 ](./pricing-rule-conditions.md)：価格ルールの対象となる製品を決定します。
- [ 処理 ](./pricing-rule-actions.md)：上場価格を決定するために価格ソースに適用される調整計算を定義します。

[ 表示価格 ](./standard-price-rules.md) 設定の選択された **[!UICONTROL Magento Price Source]** を基準として、Amazonの表示価格を自動的に調整する [ 標準価格ルール ](./listing-price.md) を作成できます。 この機能を使用すると、[!DNL Commerce] カタログ価格ルール [ に似た方法でAmazonの価格を操作でき ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) す。 特定の製品、特定のカテゴリ内の製品、特定の属性を持つ製品の価格を自動的に変更する複雑なルールを作成できます。 従来の設定を完了し、製品の価格を変更して、固定金額または割合に基づいて増減させることができます。

もう 1 つの強力なツールは、競合他社価格または [ 最低の競合他社価格 ](./intelligent-repricing-rules.md) に基づいてAmazonのリスト価格を調整する [ インテリジェントな再 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価 ](./lowest-competitor-pricing.md) 機能です。 [!DNL Commerce] [ カタログ価格ルール ](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) と同様に、この高度な機能を使用すると、複雑なルールを作成してAmazonの価格を操作できます。 ルールでは、特定の製品、特定のカテゴリ内の製品、特定の製品属性を使用した製品に対して、価格変更の範囲を定義できます。

インテリジェントな価格再設定を利用して、競合他社の価格に基づいてAmazonの上場価格を調整します。 Amazon セールスチャネルには、マージンを保護したり、マーチャントの価格とフィードバックの低い価格を一致させたりしないように設定するための保護策が組み込まれています。 [ インテリジェント再価格設定ルール ](./intelligent-repricing-rules.md) を使用すると、Amazonの上場価格は、品目ごとに固定またはパーセンテージの金額（上下）として自動的に操作することも、[[!DNL Buy Box]](./buy-box-competitor-pricing.md) 定価格または [ 競合他社最低価格 ](./lowest-competitor-pricing.md) に同期することもできます。 ルールを積み重ねて、無制限の柔軟性を提供することもできます。

アクティブ/非アクティブのステータス、web サイトの実施要件、オプションの日付範囲、オプションの優先度レベル（ルールスタッキングに使用される）など、ルールの重要な側面を制御できます。

例えば、価格ルールの条件を定義および設定できます。この条件が満たされると、Amazonに送信される前に上場価格が自動調整されます。

もう 1 つの価格オプションは、個々のリストレベルで設定される [ 価格の上書き ](./overrides.md) です。 [ 価格の上書き ](./overrides.md) を設定できます。上書きはその他すべてのデフォルト、設定およびルールを無視または優先します。 [ オーバーライド ](./overrides.md) は、価格、処理時間、条件および販売者メモに対して設定できます（一部の例外を除く）。

![ 価格決定ルール ](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## デフォルトの列

| 列 | 説明 |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | [ 価格設定ルールの一般設定 ](./pricing-rule-general-settings.md) で設定された価格設定ルールの名前 |
| [!UICONTROL Rule Type] | [ 価格設定ルール処理 ](./pricing-rule-actions.md) （標準価格ルールまたはインテリジェント再価格設定ルール）で設定されたルール・タイプ |
| [!UICONTROL Is Active] | [ 価格設定ルール一般設定 ](./pricing-rule-general-settings.md) で設定したルールがアクティブかどうか |
| [!UICONTROL Priority] | [ 価格設定ルール一般設定 ](./pricing-rule-general-settings.md) で設定されている、他の価格設定条件に対する優先度 |
| [!UICONTROL Stop Further Rules Processing] | [ 価格ルールの一般設定 ](./pricing-rule-general-settings.md) で設定されているように、このルールの対象となる製品でさらに価格ルールが処理されるかどうかを示します。 |
| [!UICONTROL From Date] | ルールがアクティブである期間の始まり |
| [!UICONTROL To Date] | ルールがアクティブである期間の終わり |
| [!UICONTROL Action] | 特定のリストに適用できるすべてのアクションをリストします。 アクションを適用するには、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Select]**をクリックします。 オプション：`Edit Price Rule` / `Delete Price Rule` |
