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

![Commerceの価格範囲](assets/amazon-price-scope.png){width="400"}

製品が 2 つの web サイト上にあり、web サイトごとに異なる価格がある場合に使用される価格を判断するには、価格優先ロジック（ [並べ替え順序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 値）。

店舗の並べ替え順を表示するには、次に移動してください： **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** が含まれる _Admin_ サイドバー。 が含まれる _[!UICONTROL Web Site]_列で、web サイト名をクリックします。 この_[!UICONTROL Web Site Information]_ このページには、 _[!UICONTROL Sort Order]_web サイトの優先度を決定する、web サイトの設定。 値 `1` 優先順位が最も高いことを示します。

製品価格が `Use Default`つまり、web サイトの価格値ではなくデフォルトの価格値にフォールバックします。

## 例 1

|         | Web サイトの優先度 | 価格（Web サイト） | デフォルトを使用 |
|---------|------------------|-----------------|-------------|
| デフォルト | 0 | 31.99 ドル | — |
| ストア 1 | 1 | 24.99 ドル | 不可 |
| ストア 2 | 2 | 27.99 ドル | はい |

- この **[!UICONTROL Magento Price Source]** （で定義） [上場価格](./listing-price.md) はに設定されています。 `Price` 属性。
- Web サイトの優先度が最も高い Web サイト、つまり Store 1 （で定義）を確認します。 [並べ替え順序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 値）。
- Store 1 は Web サイトの価格（Use Default = No）を使用するように設定されているので、公開価格は$24.99 です。

## 例 2

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | 31.99 ドル | — |
| ストア 1 | 1 | 24.99 ドル | はい |
| ストア 2 | 2 | 27.99 ドル | 不可 |

- この **[!UICONTROL Magento Price Source]** （で定義） [上場価格](./listing-price.md) はに設定されています。 `Price` 属性。
- Web サイトの優先度が最も高い Web サイト、つまり Store 1 （で定義）を確認します。 [並べ替え順序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 値）。
- ストア 1 以降 **等しくない** web サイトの価格を使用するように設定（デフォルトを使用=はい）し、並べ替え順の次の web サイトを確認します。
- ストア 2 以降 **等しい** web サイトの価格を使用するように設定すると（デフォルトを使用=いいえ）、公開価格は 27.99 ドルです。

## 例 3

|         | Web サイトの優先度 | Price Website | デフォルトを使用 |
|---------|------------------|---------------|-------------|
| デフォルト | 0 | 31.99 ドル | 3000 ドル |
| ストア 1 | 1 | 24.99 ドル | — |
| ストア 2 | 2 | 27.99 ドル | 2000 ドル |

この例では、非価格値を追加します。これは、_に別の値を選択した場合に使用されます[!UICONTROL Magento Price Source_] （で定義） [上場価格](./listing-price.md) 設定）。 非価格値では、常にフォールバック価格として価格が使用されます。

- この **[!UICONTROL Magento Price Source]** （定義場所 [[!UICONTROL Listing Price]](./listing-price.md) settings）がに設定されています。 `Non-Price`.
- Web サイトの優先順位が最も高い、次の Web サイトを調べます。 `Store 1`（によって定義 [並べ替え順序](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) 値）。
- ストア 1 以降 **等しくない** を使用するようにを設定 `Non-Price` 属性で、並べ替え順の次の web サイトを確認します。
- ストア 2 以降 **等しい** を使用するようにを設定 `Non-Price` 属性（非価格） [Web サイト] = 20.00 ドル）、公開価格は 20.00 ドル。
