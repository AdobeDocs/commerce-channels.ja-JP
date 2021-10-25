---
title: 価格優先度ロジック
description: Amazon channel channel には、Amazon リスティングの公開価格を決定するために、優先順位が適用されます。
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# 価格優先度ロジック

次の例では、$31.99、$24.99、または $27.99 を公開するかどうかはシステムによって決定されます。

![コマース価格スコープ](assets/amazon-price-scope.png)

1つの製品が2つの web サイトにいて、1つの web サイトに対して多様な価格が設定されている場合にどの価格を使用するかを決定するには、価格の優先ロジックを使用 [ ](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) します ({target = &quot;_blank&quot;} 値によって決まります)。

ストアの並べ替え順序を表示するには、 **[!UICONTROL Stores]** 管理サイドバーの > に移動 **[!UICONTROL All Stores]** __ します。 列で、 _[!UICONTROL Web Site]_web サイト名をクリックします。 Web サイトの_[!UICONTROL Web Site Information]_ 設定がページに表示され _[!UICONTROL Sort Order]_ます。これにより、web サイトの重要度が決まります。 値は、 `1` 優先順位が最も高いことを示します。

製品価格がに設定されている場合は `Use Default` 、web サイトの価格値ではなく、既定の価格値に戻ります。

## 例1

|  | Web サイトの優先度 | 価格 (Web サイト) | デフォルトの使用 |
|---|---|---|---|
| デフォルト | raid-0 | $31.99 | -- |
| ストア1 | raid-1 | $24.99 | 違います |
| Store 2 | pplx-2 | $27.99 | うん |

- **[!UICONTROL Magento Price Source]**「出展価格」の定義 [ ](./listing-price.md) は属性に設定されてい `Price` ます。
- Web サイトの優先度が最も高い web サイト (ストア 1 [ ](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) ) ({target = &quot;_blank&quot;} value によって定義されています) を確認してください。
- Store 1 は web サイト価格を使用するように設定されているので、公表価格は $24.99 になります。

## 例2

|  | Web サイトの優先度 | 価格 Web サイト | デフォルトの使用 |
|---|---|---|---|
| デフォルト | raid-0 | $31.99 | -- |
| ストア1 | raid-1 | $24.99 | うん |
| Store 2 | pplx-2 | $27.99 | 違います |

- **[!UICONTROL Magento Price Source]**「出展価格」の定義 [ ](./listing-price.md) は属性に設定されてい `Price` ます。
- Web サイトの優先度が最も高い web サイト (ストア 1 [ ](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) ) ({target = &quot;_blank&quot;} value によって定義されています) を確認してください。
- Store 1 **は** web サイトの価格を使用するように設定されていないので (デフォルトの「はい」を使用します)、並べ替え順にある次の web サイトを参照してください。
- ストア 2 **は** web サイト価格を使用するように設定されているので (デフォルト = No)、公表価格は $27.99 になります。

## 例3

|  | Web サイトの優先度 | 価格 Web サイト | デフォルトの使用 |
|---|---|---|---|
| デフォルト | raid-0 | $31.99 | $30.00 |
| ストア1 | raid-1 | $24.99 | -- |
| Store 2 | pplx-2 | $27.99 | $20.00 |

この例では、「_」 [!UICONTROL Magento Price Source_] (リスト価格設定で定義されています) に別の値を選択した場合に使用される価格以外の値を追加し [ ](./listing-price.md) ます。 価格の値がない場合は、常に価格が代替価格となります。

- **[!UICONTROL Magento Price Source]**(設定で定義されている [[!UICONTROL Listing Price]](./listing-price.md) ) が「」に設定されてい `Non-Price` ます。
- Web サイトで、最も高い web サイトの優先度を確認し `Store 1` ます。これは (並べ替え順によって [ ](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) {target = &quot;_blank&quot;} 値で定義されています)。
- Store 1 **はこの属性を** 使用するように設定されていないので `Non-Price` 、ソート順で次の web サイトを参照してください。
- Store 2 **はこの** 属性を使用するように設定されている `Non-Price` (プライス以外の [ web サイト ] = $20.00) ため、パブリッシュされた値段は $20.00 になります。
