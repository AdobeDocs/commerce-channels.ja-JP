---
title: '「インテリジェントな価格設定のルール: ルールタイプを選択します。'
description: インテリジェントな再価格ルールを作成して、競合企業による価格設定に基づいて、Amazon のリスト価格を決定します。
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 0%

---

# インテリジェントな再価格ルール: ルールタイプを選択します。

>[!IMPORTANT]
>
>Amazon 地域が状態に設定されているとき `Inactive` は、オンになっているとしても、インテリジェントな価格設定ルールは正常に機能しません。 価格計算は、配達料金によって異なります。また、地域が Amazon よりも `Active` 出荷料金を同期するための状態である必要があります。<br><br>
>
>Amazon account に含まれる地域の状態を更新するには、設定 > 取引先企業情報 > 休暇設定に移動してください。 [Amazon: 休暇の状態の一覧表示を参照してください。](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

インテリジェントな再価格ルールでは、Amazon の競合企業による価格設定によって、掲載価格が決定されます。 ライバルには、Amazon の対象と同じ製品がリストされている他の売り手もいます。

インテリジェントな「価格設定」ルールのセクションには、次のものが含まれます。

- ルールタイプを選択します。
- [競合企業の条件付き差異](./competitor-conditional-variances.md)
- [価格調整](./price-adjustment.md)
- [フロア価格](./floor-price.md)
- [オプションの天井価格](./optional-ceiling-price.md)

## ルールタイプを設定します。

セクションでルールタイプを定義し _[!UICONTROL Select Rule Type]_ます。

1. について **[!UICONTROL Rule Type]** は、を選択 `Intelligent repricing rule` します。

   この設定によって、フィールドと、、、 _[!UICONTROL Competitor Price Source]_およびおよびセクションが有効になり [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md) [_[!UICONTROL Floor Price]_](./floor-price.md) [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md) ます。

1. **[!UICONTROL Competitor Price Source]**&#x200B;で、次のいずれかのオプションを選択します。

   - **[!UICONTROL Use "Buy Box" Price]** -Amazon 販売価格に基づいて Amazon 価格を調整する場合は、このオプションを選択し [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ます。 [!DNL Buy Box]Amazon 上の複数の売り手が同じ製品を提供している場合は、価格があります。Amazon は、 [!DNL Buy Box] パフォーマンスの要件に基づいて販売者を定義します。 商人は、売り手の状態に勝ち、その製品リストを最大限に活用できるようにし [!DNL Buy Box] ています。

   - **[!UICONTROL Use Lowest Competitor Price]** -リスト価格を比較して、同じ製品の競合他社価格に合わせて調整する場合に選択します。 選択すると、 _[!UICONTROL Minimum Positive Feedback]_and_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になります。

1. 有効にした場合は、のオプションを選択し **[!UICONTROL Minimum Positive Feedback]** ます。

   - **[!UICONTROL All Competitor's Prices]** -同じ製品について、競合企業のあらゆる価格に基づいて価格を比較し、調整する場合に選択します。

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** -同じ製品について価格が比較される競合企業を制限する場合に選択します。 この設定では、最低価格ルールを適用する前に、その出展について、選択されたポジティブフィードバックのうち最低限の割合を持つ必要があることで、競合企業がさらに詳しくなります。

1. 有効にした場合は、の数値を入力し **[!UICONTROL Minimum Feedback Count]** ます。

   この数値は、競争における価格をさらに絞り込むことができます。 例えば、商人に95% 肯定的なフィードバックレートが設定されていても、フィードバック数が1つのみの場合は、 `20` その価格設定を変更したい競合先ではない可能性があります。 「」の値を入力した場合は、 `1000` 商人に95% 陽性のフィードバックと、最低でも1000のマーチャントレビューが含まれている必要があります。

>[!NOTE]
>
>このような競合他社の価格設定とフィードバックオプションを使用すると、フィードバックが不足している競合企業に対する価格設定が、より低品質の製品を販売していることを防ぐことができます。

![インテリジェントな再価格ルールタイプを選択します。](assets/ob-intelligent-price-rule-type.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Rule Type] | ルールタイプを選択します。 オプション：<ul><li>**[!UICONTROL Standard price rule]** -この種類のルールでは、Amazon の一覧表示価格を、特定のパーセントまたは1を基準にした一定金額に拡大または縮小することができ _[!UICONTROL Magento Price Source]_ます。 </li><li>**[!UICONTROL Intelligent repricing rule]** -この種類のルールでは、競合企業の価格設定に基づいて、Amazon の一覧価格を調整することができます。 選択すると、 _[!UICONTROL Minimum Positive Feedback]_and_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になります。</li></ul> |
| [!UICONTROL Competitor Price Source] | 目的の価格ソースを選択します。 オプション：<ul><li>**[!UICONTROL Use "Buy Box" Price]** -Amazon の価格に基づいて Amazon の価格設定を変更する場合は、このオプションを選択し [[!DNL Buy Box]](./buy-box-competitor-pricing.md) ます。 [!DNL Buy Box]Amazon 上の複数の売り手が同じ製品を提供している場合は、価格があります。Amazon は、 [!DNL Buy Box] パフォーマンスの要件に基づいて販売者を定義します。 商人は、売り手の状態に勝ち、その製品リストを最大限に活用できるようにし [!DNL Buy Box] ています。</li><li>**[!UICONTROL Use Lowest Competitor Price]** -同じ製品について、出展価格を比較して、 [ 競合企業が最も少ない価格に変更する場合は、このオプションを選択し ](./lowest-competitor-pricing.md) ます。 選択すると、 _[!UICONTROL Minimum Positive Feedback]_and_[!UICONTROL Minimum Feedback Count]_ フィールドが有効になります。</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | 選択されている場合のみ `Use Lowest Competitor Price` 、アクティブになります。 オプション：<ul><li>**[!UICONTROL All Competitor's Prices]** -同じ製品について、競合企業のあらゆる価格に基づいて価格を比較し、調整する場合に選択します。</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** -価格設定を比較して調整する対象となる競合企業を制限する場合に選択します。 この設定によって、対戦リストには最低でも選択されている肯定的なフィードバックを少なくし、そのサブセットの最低価格を使用することで、競合企業をさらに絞り込むことができます。</li></ul> |
| [!UICONTROL Minimum Feedback Count] | 選択されている場合のみ `Use Lowest Competitor Price` 、アクティブになります。 この数値を指定すると、競争価格の比較結果を絞り込むことができます。 例えば、商人に95% 肯定的なフィードバックレートが設定されていて、そのフィードバック数はフィードバック件数が限られている場合は、 `20` 価格設定を変更したい競合先ではない可能性があります。 「」の値を入力した場合は、 `1000` 商人に95% 陽性のフィードバックと、最低でも1000のマーチャントレビューが含まれている必要があります。 |
