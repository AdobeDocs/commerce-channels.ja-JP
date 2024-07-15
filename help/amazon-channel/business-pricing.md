---
title: "Amazon listings の [!DNL (B2B) Business Price]"
description: Amazon [!DNL Commerce]  アカウントでビジネスを有効にすると、Amazon Business （B2B）サイトにストア商品をリス  [!DNL Seller Central]  できます。
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Amazonの一覧の [!DNL (B2B) Business Price]

（B2B）ビジネス価格の設定は、ストアリスト設定の一部です。 リスト設定は、[Amazon ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスできます。

[!DNL Amazon Business] は、Amazonの登録済みビジネスアカウント専用のマーケットプレイスで、米国、フランス、ドイツ、英国でのみ利用できます。 マーケットプレイスで B2B ビジネス価格が許可されている場合は、リスト設定内で編集できます。

[!DNL B2B Business Pricing] を使用すると、ビジネスアカウントを持つマーチャントは、Amazonのショッピングエクスペリエンスの期待されるパフォーマンスで相互に購入できます。 B2B ビジネスの価格を使用すると、企業は購入数量に基づいて段階的な価格を提供できます。

製品を [!DNL Amazon Business (B2B)] サイトに一覧表示するには、まず [!DNL Amazon Seller Central] アカウントでビジネスを有効にする必要があります。 B2B 機能の詳細については、[Amazon:B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} を参照してください（セラーの Central ログインが必要です）。

## [!DNL (B2B) Business Price] の設定

1. ストアダッシュボードで「**[!UICONTROL Listing Settings]**」をクリックします。

1. 「_[!UICONTROL (B2B) Business Price]_」セクションを展開します。

1. **[!UICONTROL Enable Business Pricing]** の場合は、オプションを選択します。

   - `Disabled` - （デフォルト） B2B 販売を有効にしない場合に選択します。 このセクションのその他のフィールドは、選択すると無効になります。

   - `Enabled` - B2B セールスを有効にするタイミングを選択します。 有効化すると、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 ビジネス価格は、有効な場合、web サイトの価格範囲に従います。 ビジネス価格を 1 ドル未満にすることはできません。

1. **[!UICONTROL Enable Tiered Pricing]** の場合は、オプションを選択します。

   - `Disabled` - （デフォルト）すべての受注数量に同じ上場価格を設定する場合に選択します。 選択すると、このセクション内 _[!UICONTROL Pricing Level]_すべてのフィールドが無効になります。

   - `Enabled` – 注文数量に基づいて価格調整を有効にするタイミングを選択します。 これを選択すると、_[!UICONTROL Pricing Level]_のフィールドが有効になります。

1. **[!UICONTROL Pricing Level]** の設定を完了します。

   ビジネス一覧の階層価格を設定する数量/割引設定を最大 5 つ定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、1 行目の 1 番目のフィールドに「`5`」と入力し、2 行目のフィールドに「`5`」と入力した場合、別の事業者が 5 つ以上の数量を購入すると、価格には 5% の割引が適用されます。

1. 完了したら、「**[!UICONTROL Save listing settings]**」をクリックします。

![Amazon Business Pricing （B2B） ](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト） B2B 販売を有効にしない場合に選択します。 選択すると、このセクション内の他のすべてのフィールドが無効になります。</li><li>**[!UICONTROL Enabled]** - ビジネスからビジネスへの販売を有効にするタイミングを選択します。 選択すると、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 ビジネス価格は、有効な場合、web サイトの価格範囲に従います。 ビジネス価格を 1 ドル未満にすることはできません。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必須）オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）すべての受注数量に同じ上場価格を設定する場合に選択します。 選択すると、このセクション内 _[!UICONTROL Pricing Level]_すべてのフィールドが無効になります。</li><li>**[!UICONTROL Enabled]** – 受注数量に基づいて調整される価格設定を使用可能にするタイミングを選択します。 これを選択すると、_[!UICONTROL Pricing Level]_のフィールドが有効になります。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | Tiered Pricing が有効化されている場合は、ビジネス・リストの階層価格を設定する数量/割引設定を最大 5 つ定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、1 行目の 1 番目のフィールドに「`5`」と入力し、2 行目のフィールドに「`5`」と入力した場合、別の事業者が 5 つ以上の数量を購入すると、価格には 5% の割引が適用されます。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
