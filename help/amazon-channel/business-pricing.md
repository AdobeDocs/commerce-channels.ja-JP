---
title: '"[!DNL (B2B) Business Price] Amazon・リスト向け」'
description: 次の項目をリストできます： [!DNL Commerce] Amazonでビジネスを有効にして、Amazonビジネス (B2B) サイトに製品を保存する [!DNL Seller Central] アカウント。
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] Amazonリスト用

(B2B) ビジネス価格設定は、ストアリスト設定の一部です。 リスト設定には、 [Amazonストアダッシュボード](./amazon-store-dashboard.md).

[!DNL Amazon Business] は、Amazonの登録済みビジネスアカウント専用のマーケットプレイスで、米国、フランス、ドイツ、英国でのみ利用できます。 Marketplace で B2B ビジネス向けの価格設定が許可されている場合は、リスト設定内で編集できます。

[!DNL B2B Business Pricing] では、ビジネスアカウントを持つマーチャントがAmazonのショッピングエクスペリエンスの期待されるパフォーマンスで互いに購入できます。 B2B ビジネス向けの価格設定を使用すると、企業は購入数量に基づいて段階的な価格設定を提供できます。

製品を [!DNL Amazon Business (B2B)] サイトで、最初に [!DNL Amazon Seller Central] アカウント。 B2B 機能について詳しくは、 [Amazon: B2B セントラル](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} （セラーセントラルログインが必要です）。

## 設定 [!DNL (B2B) Business Price] 設定

1. クリック **[!UICONTROL Listing Settings]** を選択します。

1. を展開します。 _[!UICONTROL (B2B) Business Price]_」セクションに入力します。

1. の場合 **[!UICONTROL Enable Business Pricing]**、「 」オプションを選択します。

   - `Disabled` - （デフォルト）B2B のセールスを有効にしない場合に選択します。 このセクションのその他のフィールドは、選択すると無効になります。

   - `Enabled` - B2B セールスを有効にするタイミングを選択します。 有効にすると、すべての価格設定ルールが適用された後、定価と同じ価格が設定されます。 有効にした場合、ビジネス価格は Web サイトの価格範囲に従います。 ビジネス価格は$1 以上にする必要があります。

1. の場合 **[!UICONTROL Enable Tiered Pricing]**、「 」オプションを選択します。

   - `Disabled` - （デフォルト）すべての注文数量に同じ上場価格を求める場合に選択します。 選択すると、すべて _[!UICONTROL Pricing Level]_このセクションのフィールドは無効です。

   - `Enabled`  — オーダー数量に基づく価格設定調整を有効にする場合に選択します。 選択すると、 _[!UICONTROL Pricing Level]_フィールドが有効になっている。

1. 次を完了： **[!UICONTROL Pricing Level]** 設定。

   ビジネスリストの階層価格を設定する数量/割引設定を 5 つまで定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、 `5` を最初の行の最初のフィールドに追加し、 `5` 2 番目のフィールドでは、別の企業が数量 5 以上を購入した場合に、価格が 5%の割引を適用します。

1. 完了したら、「 **[!UICONTROL Save listing settings]**.

![Amazon Business Pricing (B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）ビジネスのセールスに対してビジネスを有効にしない場合に選択します。 このオプションを選択すると、このセクション内の他のすべてのフィールドは無効になります。</li><li>**[!UICONTROL Enabled]**  — ビジネスのセールスを可能にするタイミングを選択します。 選択すると、すべての価格設定ルールが適用された後、ビジネス価格が定価と同じに設定されます。 有効にした場合、ビジネス価格は Web サイトの価格範囲に従います。 ビジネス価格は$1 以上にする必要があります。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必須）オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）すべての注文数量に同じ上場価格を求める場合に選択します。 選択すると、すべて _[!UICONTROL Pricing Level]_このセクションのフィールドは無効です。</li><li>**[!UICONTROL Enabled]**  — 受注数量に基づいて調整される価格設定を有効にする場合に選択します。 選択すると、 _[!UICONTROL Pricing Level]_フィールドが有効になっている。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | 階層型価格が有効な場合は、最大 5 つの数量/割引設定を定義して、ビジネスリストに対する階層型価格を設定できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、 `5` を最初の行の最初のフィールドに追加し、 `5` 2 番目のフィールドでは、別の企業が数量 5 以上を購入した場合に、価格が 5%の割引を適用します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
