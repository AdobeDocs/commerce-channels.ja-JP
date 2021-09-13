---
title: インテリジェントな価格変更ルール：ルールタイプを選択`
description: インテリジェントな価格変更ルールを作成し、競合相手の価格に従ってAmazonの上場価格を決定します。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# インテリジェントな再価格設定ルール：ルールタイプの選択

>[!IMPORTANT]
>
>Amazon地域が`Inactive`ステータスに設定されている場合、オンボーディング中と同様に、インテリジェントな価格変更ルールは正しく機能しません。 価格の計算は、配送料に応じて異なります。Amazonから同期するには、お住まいの地域の配送料が`Active`状態である必要があります。<br><br>
>
>Amazonアカウントの地域ステータスを更新するには、設定/アカウント情報/休暇の設定に移動します。 [Amazonを参照：休暇のステータスのリスト](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

インテリジェントな価格変更ルールでは、Amazonの競合他社の価格を使用して上場価格を決定します。 競合他社は、Amazonで同じ製品をリストする他の販売者です。

インテリジェントな価格変更ルールのセクションは次のとおりです。

- ルールタイプの選択
- [競合相手の条件の相違](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [下限価格](./floor-price.md)
- [オプションの上限価格](./optional-ceiling-price.md)

## ルールタイプの設定

_[!UICONTROL Select Rule Type]_セクションでルールタイプを定義します。

1. **[!UICONTROL Rule Type]**&#x200B;の場合は、`Intelligent repricing rule`を選択します。

   この設定により、_[!UICONTROL Competitor Price Source]_フィールドと、[_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md)、[_[!UICONTROL Floor Price]_](./floor-price.md)、[_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md)セクションが有効になります。

1. **[!UICONTROL Competitor Price Source]**&#x200B;の場合は、次のオプションを選択します。

   - **[!UICONTROL Use "Buy Box" Price]** - Amazonの販売価格に基づいてAmazonの価格を調整するタイミン [[!DNL Buy Box]](./buy-box-competitor-pricing.md) グを選択します。Amazonの複数の販売者が同じ製品を提供すると、[!DNL Buy Box]価格が存在します。 Amazonは、パフォーマンス要件に基づいて[!DNL Buy Box]販売者を定義します。 商人は、売り手のステータスを獲得し、製品リストを最大限に表示できるようにします。[!DNL Buy Box]

   - **[!UICONTROL Use Lowest Competitor Price]**  — 同じ製品の上場価格を競合他社の価格と比較して調整するタイミングを選択します。選択すると、_[!UICONTROL Minimum Positive Feedback]_フィールドと_[!UICONTROL Minimum Feedback Count]_&#x200B;フィールドが有効になります。

1. 有効にした場合、**[!UICONTROL Minimum Positive Feedback]**&#x200B;のオプションを選択します。

   - **[!UICONTROL All Competitor's Prices]**  — 同じ製品のすべての競合他社の価格に基づいて、価格を比較および調整するタイミングを選択します。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 同じ製品に対して価格を比較する競合相手を制限するタイミングを選択します。この設定は、最も低い価格ルールを適用する前に、選択した正のフィードバックの最小値をリストに含めることで、競合相手をさらに絞り込みます。

1. 有効にした場合は、**[!UICONTROL Minimum Feedback Count]**&#x200B;に数値を入力します。

   このオプションの数値は、競合価格をさらに絞り込みます。 例えば、商人の95%肯定的なフィードバック評価があり、フィードバック数が`20`のみの場合、価格を変更する競合他社ではない可能性があります。 ただし、値`1000`を入力する場合は、商人に95%の肯定的なフィードバックがあり、1,000人以上の商人レビューが必要です。

>[!NOTE]
>
>これらの競合他社の価格とフィードバックオプションを使用して、フィードバックが不十分で低品質の製品を販売している競合他社に対する価格設定を避けることができます。

![インテリジェントな再価格設定ルール — ルールタイプの選択](assets/ob-intelligent-price-rule-type.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Rule Type] | ルールタイプを選択します。 オプション：<ul><li>**[!UICONTROL Standard price rule]**  — このルールタイプを使用すると、Amazonの上場価格を、に対して特定の割合または固定ドル額で増減できま _[!UICONTROL Magento Price Source]_す。 </li><li>**[!UICONTROL Intelligent repricing rule]**  — このルールタイプを使用すると、競合相手の価格に基づいてAmazonの上場価格を調整できます。選択すると、_[!UICONTROL Minimum Positive Feedback]_フィールドと_[!UICONTROL Minimum Feedback Count]_&#x200B;フィールドが有効になります。</li></ul> |
| [!UICONTROL Competitor Price Source] | 目的の価格ソースを選択します。 オプション：<ul><li>**[!UICONTROL Use "Buy Box" Price]**  — このオプションは、Amazonの販売価格に基づいてAmazonの価格を調整する場合に選 [[!DNL Buy Box]](./buy-box-competitor-pricing.md) 択します。Amazonの複数の販売者が同じ製品を提供すると、[!DNL Buy Box]価格が存在します。 Amazonは、パフォーマンス要件に基づいて[!DNL Buy Box]販売者を定義します。 商人は、売り手のステータスを獲得し、製品リストを最大限に表示できるようにします。[!DNL Buy Box]</li><li>**[!UICONTROL Use Lowest Competitor Price]**  — 同じ製品の最も低い競合他社価格と比較して調整する場合は、こ [のオプ](./lowest-competitor-pricing.md) ションを選択します。選択すると、_[!UICONTROL Minimum Positive Feedback]_フィールドと_[!UICONTROL Minimum Feedback Count]_&#x200B;フィールドが有効になります。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | `Use Lowest Competitor Price`を選択した場合にのみ有効です。 オプション：<ul><li>**[!UICONTROL All Competitor's Prices]**  — 同じ製品のすべての競合他社の価格に基づいて、価格を比較および調整するタイミングを選択します。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]**  — 価格を比較および調整する競合相手を制限するタイミングを選択します。この設定は、選択した肯定的なフィードバックの最低割合をリストに含め、その他の競合相手のサブセットの最低価格を使用することで、競合相手をさらに絞り込みます。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | `Use Lowest Competitor Price`を選択した場合にのみ有効です。 このオプションの数値は、競合価格の比較をさらに絞り込みます。 例えば、商人の95%肯定的なフィードバック評価があり、フィードバック数が`20`のみの場合、価格を変更する競合他社ではない可能性があります。 ただし、値`1000`を入力する場合は、商人に95%の肯定的なフィードバックがあり、1,000人以上の商人レビューが必要です。 |
