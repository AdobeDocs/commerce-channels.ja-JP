---
title: (B2B)ビジネス価格
description: ' [!DNL Commerce] store products on the Amazon Business (B2B) site by enabling business in your Amazon [!DNL Seller Central] アカウントを一覧表示できます。'
redirect_from: /sales-channels/asc/ob-business-pricing.html
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# (B2B)ビジネス価格

(B2B)ビジネス価格設定は、ストアリスト設定の一部です。 リスト設定は、[ストアダッシュボード](./amazon-store-dashboard.md)からアクセスします。

[!DNL Amazon Business] は、Amazonの登録ビジネスアカウント専用のマーケットプレイスで、米国、フランス、ドイツ、英国でのみ利用できます。B2Bビジネス向けの価格設定がMarketplaceで許可されている場合は、リスト設定内で編集できます。

[!DNL B2B Business Pricing] では、ビジネスアカウントを持つ商人がAmazonのショッピングエクスペリエンスのパフォーマンスを期待してお互いに購入できます。B2Bビジネス向けの価格設定を使用すると、購入数量に基づいて階層型の価格設定を提供できます。

製品を[!DNL Amazon Business (B2B)]サイトに表示するには、まず[!DNL Amazon Seller Central]アカウントでビジネスを有効にする必要があります。 B2B機能の詳細については、[Amazon:B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target=&quot;_blank&quot;} （セラーセントラルログインが必要）。

## (B2B)ビジネス価格の設定

1. ストアダッシュボードの「**[!UICONTROL Listing Settings]**」をクリックします。

1. _[!UICONTROL (B2B) Business Price]_セクションを展開します。

1. **[!UICONTROL Enable Business Pricing]**&#x200B;の場合は、オプションを選択します。

   - `Disabled` - （デフォルト） Business-to-Businessの販売を有効にしない場合に選択します。このセクションのその他のフィールドは、選択すると無効になります。

   - `Enabled` - B2Bの販売を有効にするタイミングを選択します。有効にすると、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 有効にした場合、ビジネス価格はWebサイトの価格範囲に従います。 ビジネス価格は1ドル以下にはできません。

1. **[!UICONTROL Enable Tiered Pricing]**&#x200B;の場合は、オプションを選択します。

   - `Disabled` - （デフォルト）すべての注文数量に同じ上場価格を設定する場合に選択します。選択すると、このセクションの&#x200B;_[!UICONTROL Pricing Level]_フィールドはすべて無効になります。

   - `Enabled`  — 注文数量に基づいて価格調整を有効にする場合に選択します。選択すると、_[!UICONTROL Pricing Level]_フィールドが有効になります。

1. **[!UICONTROL Pricing Level]**&#x200B;設定を完了します。

   ビジネスリストに対して層別価格を設定する、最大5つの数量/割引設定を定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、1行目のフィールドに`5`、2行目のフィールドに`5`と入力した場合、別の企業が数量5以上を購入すると、価格によって5%の割引が適用されます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![Amazon Business Pricing(B2B)](assets/amazon-business-pricing.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Enable Business Pricing] | オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）ビジネス向けの販売を有効にしない場合に選択します。選択すると、このセクション内の他のすべてのフィールドは無効になります。</li><li>**[!UICONTROL Enabled]**  — ビジネスの販売を可能にするタイミングを選択します。選択した場合、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 有効にした場合、ビジネス価格はWebサイトの価格範囲に従います。 ビジネス価格は1ドル以下にはできません。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必須）オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）すべての注文数量に同じ上場価格を設定する場合に選択します。選択すると、このセクションの&#x200B;_[!UICONTROL Pricing Level]_フィールドはすべて無効になります。</li><li>**[!UICONTROL Enabled]**  — 注文数量に基づいて調整される価格設定を有効にする場合に選択します。選択すると、_[!UICONTROL Pricing Level]_フィールドが有効になります。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | 階層型価格を有効にすると、ビジネス・リストに対して階層型価格を設定する最大5つの数量/割引設定を定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、1行目のフィールドに`5`、2行目のフィールドに`5`と入力した場合、別のビジネスが5個以上の数量を購入すると、価格が5%の割引を適用します。 |

**クイックアクセス**  — セク [!UICONTROL Listing Settings] ション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
