---
title: Amazonセールスチャネル — 価格優先ロジック
description: Amazonセールスチャネルは、Amazon上場の公表価格を決定する際に優先順位付けを適用します。
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# 価格優先ロジック

次の例では、$31.99、$24.99、$27.99 のいずれを公開するかは、システムによってどのように決定されますか？

![コマース価格の範囲](assets/amazon-price-scope.png){width="400"}

2 つの Web サイト上にある製品の価格が Web サイトごとに異なる場合に、どの価格を使用するかを決定するには、価格の優先度ロジック ( [並べ替え順](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値 ) です。

店舗の並べ替え順を表示するには、次に移動します： **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** （内） _管理者_ サイドバー。 Adobe Analytics の _[!UICONTROL Web Site]_「 」列で、web サイト名をクリックします。 The_[!UICONTROL Web Site Information]_ ページに _[!UICONTROL Sort Order]_設定を使用します。この設定は、Web サイトの優先度を決定します。 値： `1` 最も高い優先度を示します。

製品価格が `Use Default`の場合は、Web サイトの価格値ではなくデフォルトの価格値にフォールバックされます。

## 例 1

|         | Web サイトの優先度 | 価格（Web サイト） | デフォルトを使用 |
|---------|------------------|-----------------|-------------|
| デフォルト | 0 | $31.99 | — |
| ストア 1 | 1 | $24.99 | いいえ |
| ストア 2 | 2 | $27.99 | はい |

- The **[!UICONTROL Magento Price Source]** ( [上場価格](./listing-price.md) が `Price` 属性。
- 最も優先度の高い Web サイトを見てください。Store 1 ( [並べ替え順](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値 ) です。
- Store 1 は Web サイトの価格 (Use Default = No) を使用するように設定されているので、公開価格は$24.99 です。

## 例 2

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | $31.99 | -- |
| ストア 1 | 1 | $24.99 | はい |
| ストア 2 | 2 | $27.99 | いいえ |

- The **[!UICONTROL Magento Price Source]** ( [上場価格](./listing-price.md) が `Price` 属性。
- 最も優先度の高い Web サイトを見てください。Store 1 ( [並べ替え順](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値 ) です。
- ストア 1 以降 **等しくない** Web サイトの価格を使用するように設定 (Use Default = Yes) した場合、並べ替え順で次の Web サイトを確認します。
- ストア 2 以降 **次に該当** Web サイトの価格を使用するように設定 (Use Default = No) した場合、公開価格は$27.99 です。

## 例 3

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | $31.99 | $30.00 |
| ストア 1 | 1 | $24.99 | -- |
| ストア 2 | 2 | $27.99 | $20.00 |

次の使用例は、非価格の値を追加します。これは、「_」に別の値を選択した場合に使用されます。[!UICONTROL Magento Price Source_] ( [上場価格](./listing-price.md) 設定 )。 価格以外の値では、常に価格が代替価格として使用されます。

- The **[!UICONTROL Magento Price Source]** ( で定義 [[!UICONTROL Listing Price]](./listing-price.md) 設定 ) が次の値に設定されている `Non-Price`.
- 最も優先度の高い Web サイト ( `Store 1`( [並べ替え順](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値 ) です。
- ストア 1 以降 **等しくない** を `Non-Price` 属性を指定し、並べ替え順で次の Web サイトを参照します。
- ストア 2 以降 **次に該当** を `Non-Price` 属性 ( 非価格 [Web サイト] = 20.00) の場合、公開価格は$20.00 です。
