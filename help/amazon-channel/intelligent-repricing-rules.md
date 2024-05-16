---
title: 「インテリジェント再価格設定ルール：ルールタイプの選択」
description: インテリジェントな価格再設定ルールを作成して、競合他社の価格に応じてAmazonの上場価格を決定します。
feature: Sales Channels, Products, Price Rules
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# インテリジェント再価格設定ルール：ルール・タイプの選択

>[!IMPORTANT]
>
>Amazonリージョンがに設定されている場合、インテリジェントな価格再設定ルールが正しく機能しません `Inactive` ステータス（オンボーディング中の場合） 価格の計算は配送料によって異なり、お住まいの地域は `Active` Amazonから同期する配送料のステータス。<br><br>
>
>Amazon アカウントの地域ステータスを更新するには、[ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] に移動します。 こちらを参照してください [Amazon：休暇のステータスの一覧表示](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

インテリジェントな価格再設定ルールでは、Amazonの競合他社の価格を使用して上場価格を決定します。 競合他社は、Amazonで同じ製品をリストするその他のセラーです。

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- ルールタイプを選択
- [競合他社条件付き差異](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [フロアプライス](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

## ルールタイプの設定

でのルールタイプの定義 _[!UICONTROL Select Rule Type]_セクション。

1. の場合 **[!UICONTROL Rule Type]**、を選択 `Intelligent repricing rule`.

   この設定は、 _[!UICONTROL Competitor Price Source]_フィールドと [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)、および [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) セクション。

1. の場合 **[!UICONTROL Competitor Price Source]**、次のいずれかのオプションを選択します。

   - **[!UICONTROL Use "Buy Box" Price]** - Amazonに基づいてAmazonの価格を調整するタイミングを選択します [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 売り手の価格。 A [!DNL Buy Box] 価格は、Amazon上の複数のセラーが同じ商品を提供する場合に存在します。 Amazonはを定義します [!DNL Buy Box] 業績要件に基づく販売者。 商人は勝つために模索 [!DNL Buy Box] 販売者のステータスとオファーの製品リストの最大の可視性。

   - **[!UICONTROL Use Lowest Competitor Price]**  – 同じ製品の競合他社価格と上場価格を比較および調整するタイミングを選択します。 選択した場合、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっています。

1. 有効な場合、次のオプションを選択 **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]**  – 同じ製品のすべての競合他社価格に基づいて価格を比較および調整するタイミングを選択します。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  – 同じ製品に対して価格を比較する競合他社を制限する場合を選択します。 この設定では、最低価格のルールを適用する前に、リストに対して選択した肯定的なフィードバックの割合を最小限に抑えることを要求することで、競合他社をさらに絞り込みます。

1. 有効な場合は、数値を入力 **[!UICONTROL Minimum Feedback Count]**.

   このオプションの数値は、競争力のある価格をさらに絞り込みます。 例えば、マーチャントのポジティブフィードバックの評価が 95% で、フィードバック数がの場合などです `20`ただし、価格を変更したい競合他社ではない可能性があります。 ただし、の値を入力した場合は、 `1000`その場合、マーチャントは 95% の肯定的なフィードバックを得て、少なくとも 1,000 件のマーチャントレビューを行う必要があります。

>[!NOTE]
>
>これらの競合他社価格オプションとフィードバック・オプションを使用して、フィードバックが低く、品質の低い製品を販売している競合製品に対する価格設定を回避できます。

![インテリジェント再価格設定ルール：ルール・タイプの選択](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | ルールタイプを選択します。 オプション：<ul><li>**[!UICONTROL Standard price rule]** Amazon – このルールタイプを使用すると、 _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]**  – このルールタイプを使用すると、競合他社の価格に基づいて、Amazonの上場価格を調整できます。 選択した場合、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっています。</li></ul> |
| [!UICONTROL Competitor Price Source] | 目的の価格ソースを選択します。 オプション：<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Amazonに基づいてAmazonの価格を調整する場合は、このオプションを選択します [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 売り手の価格。 A [!DNL Buy Box] 価格は、Amazon上の複数のセラーが同じ商品を提供する場合に存在します。 Amazonはを定義します [!DNL Buy Box] 業績要件に基づく販売者。 商人は勝つために模索 [!DNL Buy Box] 販売者のステータスとオファーの製品リストの最大の可視性。</li><li>**[!UICONTROL Use Lowest Competitor Price]**  – 上場価格を以下と比較して調整する場合は、このオプションを選択します [競合製品の最低価格](./lowest-competitor-pricing.md) （同じ製品の場合）。 選択した場合、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっています。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 次の場合のみアクティブ `Use Lowest Competitor Price` が選択されました。 オプション：<ul><li>**[!UICONTROL All Competitor's Prices]**  – 同じ製品のすべての競合他社価格に基づいて価格を比較および調整するタイミングを選択します。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  – 価格を比較および調整する競合他社を制限するタイミングを選択します。 この設定では、競合他社に対して選択した肯定的なフィードバックの割合を最小限に抑え、競合他社のそのサブセットの最低価格を使用するようリストに要求することで、競合他社をさらに絞り込みます。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 次の場合のみアクティブ `Use Lowest Competitor Price` が選択されました。 このオプションの数値は、競争力のある価格比較をさらに絞り込みます。 例えば、マーチャントのポジティブフィードバック評価が 95% で、フィードバック数がの場合などです `20`ただし、価格を変更したい競合他社ではない可能性があります。 ただし、の値を入力した場合は、 `1000`その場合、マーチャントは 95% の肯定的なフィードバックを得て、少なくとも 1,000 件のマーチャントレビューを行う必要があります。 |
