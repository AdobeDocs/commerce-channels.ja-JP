---
title: 製品のリスト表示条件
description: 製品一覧の条件設定を使用して、Commerce 製品を Amazon 製品条件 (「新規」や「修理」など) にマップします。
redirect_from: /sales-channels/asc/ob-product-listing-condition.html
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# 製品のリスト表示条件

製品一覧の条件設定は、ストア一覧の設定に含まれています。 一覧の設定には、ストアのダッシュボードにアクセスでき [ ](./amazon-store-dashboard.md) ます。

Amazon には、製品リストの条件が定義されている必要があります。 すべての製品が同じ条件になっている場合は、Amazon condition オプションのいずれかを選択して、すべての製品をグローバル条件の値として表すことができます。 標準的な Amazon 条件は、次のとおりです。

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>書き換えられた製品を販売する場合は、に登録する必要があり [!DNL Amazon Renewed Program] ます。 「 [ 製品の更新」を参照してください ](./renewed-products.md) 。

ただし、カタログに異なる条件の製品が含まれている場合は (新規、使用、調整など)、を選択する必要があり **[!UICONTROL Assign Condition Using Product Attribute]** ます。 この設定によって、 [!DNL Commerce] 条件の属性と値を Amazon の一覧の条件にマップすることができます。

事前設定タスクの実行中に [ ](./amazon-pre-setup-tasks.md) 、 [!DNL Commerce] 製品の状態に製品属性を作成することをお勧めします。 様々な条件で製品を提供していて、条件属性を作成していない場合は、 [ で product 属性を作成するを参照してください  [!DNL Commerce]](./ob-creating-magento-attributes.md) 。 条件属性を作成した後は、カタログ内の各製品に条件値を割り当てることができ [!DNL Commerce] ます。

## 設定の構成

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し **[!UICONTROL Product Listing Condition]** ます。

1. **[!UICONTROL Listing Product Condition]**&#x200B;では、オプションを選択します。

   すべての出展について、グローバル条件の値について標準的な Amazon 条件のうちの1つを選択します。 デフォルトの設定は `New` です。

   条件が異なる製品またはリストがある場合は、 `Assign Condition Using Product Attribute` 表示される追加フィールドで製品条件設定を定義するように選択します。

1. **「条件」属性では、** 標準の [!DNL Commerce] Amazon 条件属性の値をマップするために属性を選択します。

   Or 条件に製品が含まれていても、さらに詳しくはわからない場合は、 `Used` `Collectible` 単一 `Used` または Amazon の条件にマップ `Collectible` し、他のユーザーは空白のままにしておくことができます。 この方法では、すべての `Used` or `Collectible` 条件が単一の Amazon によって使用されるか、収集された状態にマップされます。

   例えば、製品に対して1つの条件を設定するとし `Used` ます。 マッピングする場合は、Amazon 条件、、、またはにマップするかどうかを選択し `Used; Like New` `Used; Very Good` `Used; Good` `Used; Acceptable` ます。 目的の Amazon 条件のフィールドだけを入力し、その他の `Used` オプションはに設定したままに `--Select Option--` します。 この例のイメージで [!DNL Commerce] は、条件に含まれるすべての製品 `Used` が Amazon 条件にマップされてい `Used; Very Good` ます。

   ただし、条件の内容を示すテキストを入力することもでき `New` ます。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![製品のリスト表示条件](assets/amazon-product-listing-condition.png)

| 名 | つい |
|---|---|
| [!UICONTROL Listing Product Condition] | 製品リストの状態です。 オプション。 `New` `Refurbished` 単一の `Used: Like New` `Used: Very Good` `Used: Good` `Used: Acceptable` `Collectible: Like New` `Collectible: Very Good` `Collectible: Good` `Collectible: Acceptable` `Assign Condition Using Product Attribute`<br><br> 製品条件を販売する場合は、標準の Amazon 条件のいずれかを選択します。 カタログに [!DNL Commerce] 製品が多様な条件に含まれている場合は、「」を選択し `Assign Condition Using Product Attribute` ます。 |
| [!UICONTROL Condition Attribute] | [!DNL Commerce]製品の条件を定義する属性です。作成したマグネトー属性を選択し、Amazon condition 属性にマップします。 この例では、 [ ](./ob-creating-magento-attributes.md) この名前に名前を付けることをお勧めし `Amazon Condition` ます。 選択すると、標準の Amazon 条件のマッピング用に追加のフィールドが表示されます。 |
| [!UICONTROL Additional Condition fields] | 標準的な Amazon 条件ごとに、対応する条件を選択します。 オプションには、Amazon condition 属性を作成したときに追加した条件ラベルが表示され [ ](./ob-creating-magento-attributes.md) ます。<br><br>Or 条件に製品が含まれていても、さらに詳しくはわからない場合は、 `Used` `Collectible` 単一 `Used` または Amazon の条件にマップ `Collectible` し、他のユーザーは空白のままにしておくことができます。 この方法 `Used` では、すべてまたは `Collectible` 条件が、単一の Amazon が使用されているか、収集された状態にマップされます |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
