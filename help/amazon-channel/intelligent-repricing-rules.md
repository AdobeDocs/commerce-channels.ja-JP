---
title: '''インテリジェントな価格変更ルール：ルールタイプを選択`'
description: インテリジェントな価格変更ルールを作成して、競合相手の価格に従ってAmazonの上場価格を決定します。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# インテリジェントな価格変更ルール：ルールタイプを選択

>[!IMPORTANT]
>
>Amazon地域が `Inactive` ステータス（オンボーディング中） 価格の計算は送料によって異なり、地域は `Active` Amazonから同期する送料のステータス。<br><br>
>
>Amazonアカウントで地域のステータスを更新するには、設定/アカウント情報/休暇の設定に移動します。 参照： [Amazon:休暇のステータスのリスト](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

インテリジェントな価格変更ルールでは、Amazonの競合他社の価格を使用して、上場価格を決定します。 競合他社は、Amazonで同じ製品をリストする他の販売者です。

インテリジェントな価格変更ルールのセクションは次のとおりです。

- ルールタイプを選択
- [競合相手の条件付き相違](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [下限価格](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

## ルールタイプの設定

ルールタイプを _[!UICONTROL Select Rule Type]_」セクションに入力します。

1. の場合 **[!UICONTROL Rule Type]**&#x200B;選択 `Intelligent repricing rule`.

   この設定により、 _[!UICONTROL Competitor Price Source]_フィールドと [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md)、および [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) セクション。

1. の場合 **[!UICONTROL Competitor Price Source]**、オプションを選択します。

   - **[!UICONTROL Use "Buy Box" Price]** - Amazonに基づいてAmazonの価格を調整する場合を選択します [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 販売価格。 A [!DNL Buy Box] 価格は、Amazonの複数の販売者が同じ製品を提供した場合に存在します。 Amazonは [!DNL Buy Box] 売り手はパフォーマンス要件に基づいています。 商人は勝ち目を求める [!DNL Buy Box] 販売者のステータスと製品リストの最大表示を提供します。

   - **[!UICONTROL Use Lowest Competitor Price]**  — 同じ製品の競合他社の価格と比較して調整する場合に選択します。 選択すると、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっている。

1. 有効な場合は、 **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]**  — 同じ製品のすべての競合他社の価格に基づいて、価格を比較および調整する場合を選択します。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 同じ製品で価格を比較する競合相手を制限する場合に選択します。 この設定は、最も低い価格ルールを適用する前に、選択した肯定的なフィードバックの最低割合をリストに含める必要があるので、競合他社をさらに絞り込みます。

1. 有効な場合は、 **[!UICONTROL Minimum Feedback Count]**.

   このオプションの数値により、競合価格がさらに絞り込まれます。 例えば、商人の 95%の肯定的なフィードバック評価があり、フィードバック数は `20`の場合は、価格を変更したくない競合相手である可能性があります。 ただし、 `1000`の場合、商人が 95%の肯定的なフィードバックを持ち、少なくとも 1000 の商人のレビューを持つ必要があります。

>[!NOTE]
>
>これらの競合相手の価格とフィードバックオプションを使用して、フィードバックが不十分で低品質の製品を販売している競合相手に対する価格設定を避けることができます。

![インテリジェントな価格変更ルール — ルールタイプの選択](assets/ob-intelligent-price-rule-type.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Type] | ルールタイプを選択します。 オプション：<ul><li>**[!UICONTROL Standard price rule]**  — このルールタイプを使用すると、Amazonの上場価格を、 _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]**  — このルールタイプを使用すると、競合相手の価格に基づいてAmazonの上場価格を調整できます。 選択すると、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっている。</li></ul> |
| [!UICONTROL Competitor Price Source] | 目的の価格のソースを選択します。 オプション：<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Amazonに基づいてAmazonの価格を調整する場合は、このオプションを選択します [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 販売価格。 A [!DNL Buy Box] 価格は、Amazonの複数の販売者が同じ製品を提供した場合に存在します。 Amazonは [!DNL Buy Box] 売り手はパフォーマンス要件に基づいています。 商人は勝ち目を求める [!DNL Buy Box] 販売者のステータスと製品リストの最大表示を提供します。</li><li>**[!UICONTROL Use Lowest Competitor Price]**  — このオプションは、 [最も低い競合他社価格](./lowest-competitor-pricing.md) 同じ製品の 選択すると、 _[!UICONTROL Minimum Positive Feedback]_および_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になっている。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 次の場合にのみ有効 `Use Lowest Competitor Price` が選択されます。 オプション：<ul><li>**[!UICONTROL All Competitor's Prices]**  — 同じ製品のすべての競合他社の価格に基づいて、価格を比較および調整する場合を選択します。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 価格を比較および調整する競合相手を制限するタイミングを選択します。 この設定は、選択した肯定的なフィードバックの最低限の割合をリストに含め、その他の競合他社のサブセットの最低価格を使用することで、競合他社をさらに絞り込みます。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 次の場合にのみ有効 `Use Lowest Competitor Price` が選択されます。 このオプションの数値により、競合価格の比較がさらに絞り込まれます。 例えば、商人の 95%の肯定的なフィードバック評価があり、フィードバック数は `20`の場合は、価格を変更したくない競合相手である可能性があります。 ただし、 `1000`の場合、商人が 95%の肯定的なフィードバックを持ち、少なくとも 1000 の商人のレビューを持つ必要があります。 |
