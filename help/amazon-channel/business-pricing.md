---
title: 商取引会社価格
description: アカウントのリストを作成することができ  [!DNL Commerce] store products on the Amazon Business (B2B) site by enabling business in your Amazon [!DNL Seller Central]  ます。
redirect_from: /sales-channels/asc/ob-business-pricing.html
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# 商取引会社価格

商取引会社価格設定は、ストア一覧設定に含まれています。 一覧の設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

[!DNL Amazon Business] は、Amazon のみを含む marketplace で、登録された取引先企業のみを提供します。これは、アメリカ合衆国、フランス、ドイツ、英国でのみ利用できます。 Marketplace で B2B のビジネス用価格を使用できる場合は、カタログ登録設定で編集できます。

[!DNL B2B Business Pricing] 電子取引先企業との間で、Amazon ショッピング体験の期待されるパフォーマンスを利用して、互いに購入することを許可します。 B2B の業務用価格を使用すると、購入量に基づいて段階的な価格設定を行うことができます。

製品がサイトに表示されるようにするには [!DNL Amazon Business (B2B)] 、まず、取引先企業の会社を有効にする必要があり [!DNL Amazon Seller Central] ます。 B2B 機能について詳しくは、 [ Amazon: B2B セントラル ](https://sellercentral.amazon.com/gp/help/G202161480/) {target = &quot;_blank&quot;} を参照してください (販売店の中央ログインが必要です)。

## (B2B) ビジネス価格設定の設定

1. **[!UICONTROL Listing Settings]** Store のダッシュボードのをクリックします。

1. セクションを展開し _[!UICONTROL (B2B) Business Price]_ます。

1. **[!UICONTROL Enable Business Pricing]**&#x200B;では、オプションを選択します。

   - `Disabled` -(デフォルト) 企業間販売を有効にする必要がない場合に選択します。 選択すると、このセクション内の他のすべてのフィールドが無効化されます。

   - `Enabled` -企業間販売を有効にする場合に選択します。 有効にすると、すべての価格設定ルールが適用された後に、定価と同じ値が会社価格に設定されます。 Web サイトの価格設定が有効になっている場合、その企業価格はその価格設定に従います。 会社価格を $1 未満にすることはできません。

1. **[!UICONTROL Enable Tiered Pricing]**&#x200B;では、オプションを選択します。

   - `Disabled` (デフォルト) すべての注文数量について同じ表示価格を指定する場合に選択します。 このオプションを選択すると、 _[!UICONTROL Pricing Level]_このセクション内のすべてのフィールドが無効化されます。

   - `Enabled` -注文数に基づいて価格調整を有効にする場合に選択します。 選択すると、 _[!UICONTROL Pricing Level]_フィールドが有効になります。

1. 設定を完了 **[!UICONTROL Pricing Level]** します。

   業務用の価格設定については、最大5つの数量/割引設定を定義できます。 各行に、適用する数量のしきい値と割引率を入力します。 例えば、最初の行の最初のフィールドに入力した場合、 `5` `5` 2 番目のフィールドには、別の企業が5個以上の数量を購入した場合には、5% の割引が適用されます。

1. 完了したら、をクリックし **[!UICONTROL Save listing settings]** ます。

![Amazon の会社の料金 (B2B)](assets/amazon-business-pricing.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Enable Business Pricing] | オプション： <ul><li>**[!UICONTROL Disabled]** -(デフォルト) 会社間販売を有効にしない場合に選択します。 このオプションを選択すると、このセクションにある他のすべてのフィールドが無効化されます。</li><li>**[!UICONTROL Enabled]** -勤務先へのビジネスのセールスを有効にする場合に選択します。 この設定を選択すると、すべての価格ルールが適用された後に、定価と同じ値が会社価格に設定されます。 Web サイトの価格設定が有効になっている場合、その企業価格はその価格設定に従います。 会社価格を $1 未満にすることはできません。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | 必要オプション： <ul><li>**[!UICONTROL Disabled]** (デフォルト) すべての注文数量について同じ表示価格を指定する場合に選択します。 このオプションを選択すると、 _[!UICONTROL Pricing Level]_このセクション内のすべてのフィールドが無効化されます。</li><li>**[!UICONTROL Enabled]** -注文数に基づいて調整する価格設定を有効にする場合に選択します。 選択すると、 _[!UICONTROL Pricing Level]_フィールドが有効になります。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | 段階的な価格設定が有効になっている場合は、お客様のビジネスリストの階層価格設定を行うための最大5つの数量/割引設定を定義することができます。 各行に、適用する数量のしきい値と割引率を入力します。 例えば、最初の行の最初のフィールドに入力した場合、 `5` `5` 2 番目のフィールドには5% の割引が適用されます。これにより、他の企業が5以上の数量を購入した場合に、5% の割引率が適用されます。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
