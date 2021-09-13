---
title: 価格優先ロジック
description: Amazonの販売チャネルは、Amazonの上場に掲載される価格の決定に優先順位付けを適用します。
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# 価格の優先度ロジック

次の例では、$31.99、$24.99、$27.99のどちらを公開するかが、システムによってどのように決まりますか？

![コマース価格の範囲](assets/amazon-price-scope.png)

製品が2つのWebサイト上にあり、Webサイトごとに異なる価格を持つ場合に、どの価格が使用されるかを判断するには、価格の優先順位ロジック（[並べ替え順](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}値で決定）を使用します。

ストアの並べ替え順を表示するには、_管理_&#x200B;サイドバーの&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL All Stores]**&#x200B;に移動します。 _[!UICONTROL Web Site]_列で、Webサイト名をクリックします。_[!UICONTROL Web Site Information]_&#x200B;ページには、Webサイトの優先度を決定する&#x200B;_[!UICONTROL Sort Order]_設定が表示されます。 値`1`は、最も高い優先順位を示します。

製品価格が`Use Default`に設定されている場合、Webサイトの価格ではなくデフォルトの価格に戻されます。

## 例1

|  | Webサイトの優先度 | 価格（Webサイト） | デフォルトを使用 |
|---|---|---|---|
| デフォルト | 0 | 31.99ドル | — |
| 店舗1 | 1 | 24.99ドル | いいえ |
| ストア2 | 2 | 27.99ドル | はい |

- **[!UICONTROL Magento Price Source]**（[Listing Price](./listing-price.md)で定義）は、`Price`属性に設定されます。
- Webサイトの優先度が最も高いWebサイトを見てください。Store 1 （[Sort Order](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}値で定義）
- Store 1はWebサイトの価格(Use Default = No)を使用するように設定されているので、公開価格は$24.99です。

## 例2

|  | Webサイトの優先度 | Price Website | デフォルトを使用 |
|---|---|---|---|
| デフォルト | 0 | 31.99ドル | — |
| 店舗1 | 1 | 24.99ドル | はい |
| ストア2 | 2 | 27.99ドル | いいえ |

- **[!UICONTROL Magento Price Source]**（[Listing Price](./listing-price.md)で定義）は、`Price`属性に設定されます。
- Webサイトの優先度が最も高いWebサイトを見てください。Store 1 （[並べ替え順](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}の値で定義）
- Store 1 **は、Webサイトの価格を使用するように設定されていない**&#x200B;ので(Use Default = Yes)、並べ替え順で次のWebサイトを確認します。
- Store 2 **は**&#x200B;でWebサイトの価格を使用するように設定されているので(Use Default = No)、公開価格は$27.99です。

## 例3

|  | Webサイトの優先度 | Price Website | デフォルトを使用 |
|---|---|---|---|
| デフォルト | 0 | 31.99ドル | 30.00ドル |
| 店舗1 | 1 | 24.99ドル | — |
| ストア2 | 2 | 27.99ドル | 20.00ドル |

次の例では、非価格の値を追加します。これは、_[!UICONTROL Magento Price Source_]（[Listing Price](./listing-price.md)設定で定義）に別の値を選択した場合に使用されます。 価格以外の値では、常に価格が代替価格として使用されます。

- **[!UICONTROL Magento Price Source]**（[[!UICONTROL Listing Price]](./listing-price.md)設定で定義）は`Non-Price`に設定されます。
- Webサイトの優先度が最も高いWebサイトを見ます。`Store 1`（[並べ替え順](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}の値で定義）
- Store 1 **は`Non-Price`属性を使用するように設定されていないので、並べ替え順で次のWebサイトを参照してください。**
- ストア2 **は**&#x200B;で`Non-Price`属性（非価格[Webサイト] = $20.00）を使用するように設定されているので、公開価格は$20.00です。
