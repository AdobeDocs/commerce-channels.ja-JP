---
title: Amazon セールスチャネル – 価格優先ロジック
description: Amazonのセールスチャネルでは、Amazon リストの公開価格を決定する際に優先順位付けを適用します。
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 2%

---

# 価格優先度ロジック

次の例では、$31.99、$24.99、または$27.99 を公開する必要があるかどうかをシステムはどのように判断しますか？

![Commerceの価格範囲 ](assets/amazon-price-scope.png){width="400"}

製品が 2 つの web サイトにあり、web サイトごとに異なる価格がある場合に使用される価格を判断するには、価格優先度ロジック（[ 並べ替え順 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値によって決定）を使用します。

ストアの並べ替え順を表示するには、_管理_ サイドバーの **[!UICONTROL Stores]**/**[!UICONTROL All Stores]** に移動します。 「_[!UICONTROL Web Site]_」列で、web サイト名をクリックします。_[!UICONTROL Web Site Information]_ ページには、web サイトの優先度を決定する、web サイトの _[!UICONTROL Sort Order]_設定が表示されます。 値 `1` は最も優先度が高いことを示します。

製品価格が `Use Default` に設定されている場合、web サイトの価格値ではなくデフォルトの価格値にフォールバックします。

## 例 1

|         | Web サイトの優先度 | 価格（Web サイト） | デフォルトを使用 |
|---------|------------------|-----------------|-------------|
| デフォルト | 0 | 31.99 ドル | — |
| ストア 1 | 1 | 24.99 ドル | 不可 |
| ストア 2 | 2 | 27.99 ドル | はい |

- **[!UICONTROL Magento Price Source]** （[ 上場価格で定義 ](./listing-price.md) は、`Price` 属性に設定されています。
- Web サイトの優先順位が最も高い Web サイト、つまりストア 1 を見てみましょう（このストアは [ 並べ替え順 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値で定義されます）。
- Store 1 は Web サイトの価格（Use Default = No）を使用するように設定されているので、公開価格は$24.99 です。

## 例 2

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | 31.99 ドル | — |
| ストア 1 | 1 | 24.99 ドル | はい |
| ストア 2 | 2 | 27.99 ドル | 不可 |

- **[!UICONTROL Magento Price Source]** （[ 上場価格で定義 ](./listing-price.md) は、`Price` 属性に設定されています。
- Web サイトの優先順位が最も高い Web サイト、つまりストア 1 を確認します（[ 並べ替え順 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値で定義されます）。
- Store 1 **は Web サイトの価格を使用するように設定されているため（Use Default = Yes**、並べ替え順で次の Web サイトを確認します。
- Store 2 **is** は Web サイトの価格を使用するように設定されているので（Use Default = No）、公開価格は 27.99 ドルです。

## 例 3

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | 31.99 ドル | 3000 ドル |
| ストア 1 | 1 | 24.99 ドル | — |
| ストア 2 | 2 | 27.99 ドル | 2000 ドル |

この例では、非価格の値を追加します。これは、_[!UICONTROL Magento Price Source_] に対して別の値（「価格の一覧表示 [ 設定で定義されている）を選択した場合に使用 ](./listing-price.md) れます。 非価格値では、常にフォールバック価格として価格が使用されます。

- **[!UICONTROL Magento Price Source]** （[[!UICONTROL Listing Price]](./listing-price.md) 設定で定義）は `Non-Price` に設定されます。
- Web サイトの優先度が最も高い Web サイト（`Store 1` （[ 並べ替え順 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) の値で定義）を確認します。
- ストア 1 **は `Non-Price` 属性を使用するように設定されてい** ので、並べ替え順の次の web サイトを確認します。
- ストア 2 **is** は `Non-Price` 属性（非価格 [Website] = $20.00）を使用するように設定されているので、公開価格は$20.00 です。
