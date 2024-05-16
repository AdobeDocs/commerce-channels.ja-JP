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

Amazon セールスチャネルでは、Amazonのリスト価格を定義済みの価格とは異なる価格ルールを設定できます **[!UICONTROL Magento Price Source]** が含まれる [上場価格](./listing-price.md). また、複数のルールをスタックし、インテリジェントな価格設定を使用して、競合他社の価格に基づいてAmazonのリスト価格を調整することもできます [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格又は [競合他社最低価格](./lowest-competitor-pricing.md).

次の 2 種類の価格設定ルールがあります。

- [標準価格ルール](./standard-price-rules.md)
- [インテリジェント再価格設定ルール](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >Amazonリージョンがに設定されている場合、インテリジェントな価格再設定ルールが正しく機能しません `Inactive` ステータス（オンボーディング中の場合） 価格の計算は配送料によって異なり、お住まいの地域は `Active` Amazonから同期する配送料のステータス。
  >
  >Amazon アカウントの地域ステータスを更新するには、[ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] に移動します。 こちらを参照してください [Amazon：休暇のステータスの一覧表示](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) （販売者中央ログインが必要です）

この機能を使用すると、Amazonの価格を [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). 特定の製品、特定のカテゴリ内の製品、または特定の属性を使用して価格を変更できる複雑なルールを作成できます。

Amazon リストの価格ルールを追加できます。 価格ルールを使用すると、定義された一連の条件に基づいてリスト価格を自動的に調整できます。 価格ルールがトリガーされ、商品がAmazonにリストされる前に調整済みの価格が計算されます。

>[!NOTE]
>
>Amazon リストの価格ソースは、に対して定義されます。 **[!UICONTROL Magento Price Source]** が含まれる [上場価格](./listing-price.md) 設定。 価格設定ルールで定義された調整計算では、開始値として価格ソースが使用されます。

価格ルールを使用すると、Amazonのリスト価格を独自の価格とは異なる価格に設定できます **[!UICONTROL Magento Price Source]** が含まれる [上場価格](./listing-price.md) 設定。 また、複数のルールを積み重ねて、価格を調整することもできます。

価格設定/再価格設定ルールの設定時には、次の 3 つの情報セットが必要です。

- [一般設定](./pricing-rule-general-settings.md)：ルールの名前、説明、アクティブな日付、優先度を定義し、その優先度設定に基づいて後続のルールの動作を設定します。
- [条件](./pricing-rule-conditions.md)：価格ルールの対象となる製品を決定します。
- [アクション](./pricing-rule-actions.md)：上場価格を決定するために価格ソースに適用される調整計算を定義します。

次を作成できます [標準価格ルール](./standard-price-rules.md) これにより、選択したを基準としてAmazonのリスト価格が自動調整されます **[!UICONTROL Magento Price Source]** が含まれる [上場価格](./listing-price.md) 設定。 この機能を使用すると、Amazonの価格を [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). 特定の製品、特定のカテゴリ内の製品、特定の属性を持つ製品の価格を自動的に変更する複雑なルールを作成できます。 従来の設定を完了し、製品の価格を変更して、固定金額または割合に基づいて増減させることができます。

もう 1 つの強力なツールは、 [Intelligent Repricing](./intelligent-repricing-rules.md) 競合他社に基づいてAmazonのリスト価格を調整する機能 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格若しくは [競合製品の最低価格](./lowest-competitor-pricing.md). 類似 [!DNL Commerce] [カタログ価格ルール](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html)この高度な機能を使用すると、複雑なルールを作成してAmazonの価格を操作できます。 ルールでは、特定の製品、特定のカテゴリ内の製品、特定の製品属性を使用した製品に対して、価格変更の範囲を定義できます。

インテリジェントな価格再設定を利用して、競合他社の価格に基づいてAmazonの上場価格を調整します。 Amazon セールスチャネルには、マージンを保護したり、マーチャントの価格とフィードバックの低い価格を一致させたりしないように設定するための保護策が組み込まれています。 使用 [インテリジェントな価格の変更ルール](./intelligent-repricing-rules.md)Amazonの上場価格は、固定またはパーセンテージの金額（上下）として自動的に操作することも、 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 価格若しくは [競合製品の最低価格](./lowest-competitor-pricing.md) 品目ごとに表示されます。 ルールを積み重ねて、無制限の柔軟性を提供することもできます。

アクティブ/非アクティブのステータス、web サイトの実施要件、オプションの日付範囲、オプションの優先度レベル（ルールスタッキングに使用される）など、ルールの重要な側面を制御できます。

例えば、価格ルールの条件を定義および設定できます。この条件が満たされると、Amazonに送信される前に上場価格が自動調整されます。

もう 1 つの価格オプションは、 [価格上書き](./overrides.md)（個々のリストレベルで設定されます）。 A [価格上書き](./overrides.md) 設定可能で、オーバーライドは、他のすべてのデフォルト、設定、ルールを無視または優先します。 An [上書き](./overrides.md) 価格、処理時間、条件および販売者メモ （いくつかの例外を除く）に対して設定できます。

![価格ルール](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## デフォルトの列

| 列 | 説明 |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | で設定された価格ルールの名前 [価格設定ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | に設定されているルールタイプ [価格設定ルール処理](./pricing-rule-actions.md) （標準価格ルールまたはインテリジェント再価格設定ルール） |
| [!UICONTROL Is Active] | で設定されているように、ルールがアクティブであるかどうか [価格設定ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | で設定されている、他の価格条件よりも優先されます。 [価格設定ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | このルールの対象となる製品でさらに価格ルールが処理されるかどうかを示します（例：） [価格設定ルールの一般設定](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | ルールがアクティブである期間の始まり |
| [!UICONTROL To Date] | ルールがアクティブである期間の終わり |
| [!UICONTROL Action] | 特定のリストに適用できるすべてのアクションをリストします。 アクションを適用するには、 **[!UICONTROL Select]** が含まれる _[!UICONTROL Action]_列。 オプション： `Edit Price Rule` / `Delete Price Rule` |
