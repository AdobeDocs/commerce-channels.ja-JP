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
>Amazon リージョンが `Inactive` ステータスに設定されている場合、オンボーディング中であるので、インテリジェントな価格の再設定ルールは適切に機能しません。 価格の計算は配送料によって異なり、Amazonから配送料を同期するには、お住まいの地域が `Active` ステータスである必要があります。<br><br>
>
>Amazon アカウントの地域ステータスを更新するには、[ 設定 ] > [ アカウント情報 ] > [ 休暇の設定 ] に移動します。 [Amazon：休暇のステータスの一覧表示を参照してください ](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

インテリジェントな価格再設定ルールでは、Amazonの競合他社の価格を使用して上場価格を決定します。 競合他社は、Amazonで同じ製品をリストするその他のセラーです。

インテリジェントな再価格設定ルールには、次のセクションが含まれます。

- ルールタイプを選択
- [競合他社条件付き差異](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [フロアプライス](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

## ルールタイプの設定

「_[!UICONTROL Select Rule Type]_」セクションでルールタイプを定義します。

1. **[!UICONTROL Rule Type]** の場合は、「`Intelligent repricing rule`」を選択します。

   この設定により、_[!UICONTROL Competitor Price Source]_フィールドと、[_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md)、[_[!UICONTROL Floor Price]_](./floor-price.md)、[_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) セクションが有効になります。

1. **[!UICONTROL Competitor Price Source]** の場合は、次のいずれかのオプションを選択します。

   - **[!UICONTROL Use "Buy Box" Price]** - Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) の販売者価格に基づいてAmazonの価格を調整するタイミングを選択します。 Amazon上の複数のセラーが同じ商品を提供する場合、[!DNL Buy Box] い価格が存在します。 Amazonは、パフォーマンス要件に基づいて [!DNL Buy Box] の販売者を定義します。 マーチャントは、[!DNL Buy Box] 売り手のステータスを獲得し、製品リストを最大限に可視化しようとしています。

   - **[!UICONTROL Use Lowest Competitor Price]** – 同じ製品の競合他社価格と上場価格を比較および調整するタイミングを選択します。 これを選択すると、「_[!UICONTROL Minimum Positive Feedback]_」フィールドと「_[!UICONTROL Minimum Feedback Count]_」フィールドが有効になります。

1. 有効な場合、**[!UICONTROL Minimum Positive Feedback]** のオプションを選択します。

   - **[!UICONTROL All Competitor's Prices]** – 同じ製品のすべての競合他社価格に基づいて価格を比較および調整するタイミングを選択します。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** – 同じ製品に対して価格を比較する競合他社を制限するタイミングを選択します。 この設定では、最低価格のルールを適用する前に、リストに対して選択した肯定的なフィードバックの割合を最小限に抑えることを要求することで、競合他社をさらに絞り込みます。

1. 有効な場合は、**[!UICONTROL Minimum Feedback Count]** に数値を入力します。

   このオプションの数値は、競争力のある価格をさらに絞り込みます。 例えば、マーチャントが 95% のポジティブフィードバック評価を持ち、フィードバック数が `20` のみである場合、価格を変更したい競合他社ではない可能性があります。 ただし、値 `1000` を入力した場合、マーチャントは 95% の肯定的なフィードバックを得て、1,000 件以上のマーチャントレビューを行う必要があります。

>[!NOTE]
>
>これらの競合他社価格オプションとフィードバック・オプションを使用して、フィードバックが低く、品質の低い製品を販売している競合製品に対する価格設定を回避できます。

![ インテリジェント再価格設定ルール – ルールタイプの選択 ](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | ルールタイプを選択します。 オプション：<ul><li>**[!UICONTROL Standard price rule]** – このルールタイプを使用すると、_[!UICONTROL Magento Price Source]_に対して特定の割合または固定ドル金額で、Amazonの上場価格を増減させることができます。 </li><li>**[!UICONTROL Intelligent repricing rule]** – このルールタイプを使用すると、競合他社の価格に基づいて、Amazonの上場価格を調整できます。 これを選択すると、「_[!UICONTROL Minimum Positive Feedback]_」フィールドと「_[!UICONTROL Minimum Feedback Count]_」フィールドが有効になります。</li></ul> |
| [!UICONTROL Competitor Price Source] | 目的の価格ソースを選択します。 オプション：<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Amazonの [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 売価格に基づいてAmazonの価格を調整する場合は、このオプションを選択します。 Amazon上の複数のセラーが同じ商品を提供する場合、[!DNL Buy Box] い価格が存在します。 Amazonは、パフォーマンス要件に基づいて [!DNL Buy Box] の販売者を定義します。 マーチャントは、[!DNL Buy Box] 売り手のステータスを獲得し、製品リストを最大限に可視化しようとしています。</li><li>**[!UICONTROL Use Lowest Competitor Price]** – 同じ製品の上場価格を [ 競合他社価格の最低価格 ](./lowest-competitor-pricing.md) と比較して調整する場合は、このオプションを選択します。 これを選択すると、「_[!UICONTROL Minimum Positive Feedback]_」フィールドと「_[!UICONTROL Minimum Feedback Count]_」フィールドが有効になります。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | `Use Lowest Competitor Price` が選択されている場合にのみアクティブです。 オプション：<ul><li>**[!UICONTROL All Competitor's Prices]** – 同じ製品のすべての競合他社価格に基づいて価格を比較および調整するタイミングを選択します。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** – 価格を比較および調整する競合他社を制限するタイミングを選択します。 この設定では、競合他社に対して選択した肯定的なフィードバックの割合を最小限に抑え、競合他社のそのサブセットの最低価格を使用するようリストに要求することで、競合他社をさらに絞り込みます。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | `Use Lowest Competitor Price` が選択されている場合にのみアクティブです。 このオプションの数値は、競争力のある価格比較をさらに絞り込みます。 例えば、マーチャントが 95% のポジティブフィードバック評価を持ち、フィードバック数が `20` のみである場合、価格を変更したい競合他社ではない可能性があります。 ただし、値 `1000` を入力した場合、マーチャントは 95% の肯定的なフィードバックを得て、1,000 件以上のマーチャントレビューを行う必要があります。 |
