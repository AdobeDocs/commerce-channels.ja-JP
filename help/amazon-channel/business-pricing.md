---
title: “[!DNL (B2B) Business Price] Amazon listings の場合」
description: のリストを作成できます [!DNL Commerce] Amazonでビジネスを有効化して、Amazon Business （B2B）サイトに商品を保存 [!DNL Seller Central] アカウント。
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] Amazonのリストの場合

（B2B）ビジネス価格の設定は、ストアリスト設定の一部です。 リスト設定には、からアクセスできます [Amazon ストアダッシュボード](./amazon-store-dashboard.md).

[!DNL Amazon Business] は、Amazonの登録済みビジネスアカウント専用のマーケットプレイスで、米国、フランス、ドイツ、英国でのみ利用できます。 マーケットプレイスで B2B ビジネス価格が許可されている場合は、リスト設定内で編集できます。

[!DNL B2B Business Pricing] を使用すると、ビジネスアカウントを持つマーチャントは、Amazonのショッピングエクスペリエンスの期待されるパフォーマンスで相互に購入できます。 B2B ビジネスの価格を使用すると、企業は購入数量に基づいて段階的な価格を提供できます。

製品のリストを [!DNL Amazon Business (B2B)] サイトで、最初にビジネスを有効にする必要があります [!DNL Amazon Seller Central] アカウント。 B2B 機能について詳しくは、を参照してください。 [Amazon:B2B セントラル](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} （Seller Central ログインが必要です）。

## 設定 [!DNL (B2B) Business Price] 設定

1. クリック **[!UICONTROL Listing Settings]** ストアダッシュボードで、次の操作を行います。

1. を展開します。 _[!UICONTROL (B2B) Business Price]_セクション。

1. の場合 **[!UICONTROL Enable Business Pricing]**、オプションを選択します。

   - `Disabled` - （デフォルト） B2B 販売を有効にしない場合に選択します。 このセクションのその他のフィールドは、選択すると無効になります。

   - `Enabled` - B2B 販売を有効にするタイミングを選択します。 有効化すると、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 ビジネス価格は、有効な場合、web サイトの価格範囲に従います。 ビジネス価格を 1 ドル未満にすることはできません。

1. の場合 **[!UICONTROL Enable Tiered Pricing]**、オプションを選択します。

   - `Disabled` - （デフォルト）すべての受注数量に対して同じ上場価格が必要な場合に選択します。 選択した場合、すべて _[!UICONTROL Pricing Level]_このセクションのフィールドは無効です。

   - `Enabled`  – 注文数量に基づいて価格調整を有効にするタイミングを選択します。 選択した場合、 _[!UICONTROL Pricing Level]_フィールドが有効になっています。

1. を完了する **[!UICONTROL Pricing Level]** 設定。

   ビジネス一覧の階層価格を設定する数量/割引設定を最大 5 つ定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、と入力した場合、 `5` 先頭行の先頭フィールドに `5` 2 番目のフィールドでは、他の事業者が 5 つ以上の数量を購入した場合、価格に 5% のディスカウントが適用されます。

1. 完了したら、 **[!UICONTROL Save listing settings]**.

![Amazon Business Pricing （B2B）](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| フィールド | 説明 |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト） B2B 販売を有効にしない場合に選択します。 選択すると、このセクション内の他のすべてのフィールドが無効になります。</li><li>**[!UICONTROL Enabled]** - ビジネスからビジネスへの販売を有効にするタイミングを選択します。 選択すると、すべての価格ルールが適用された後、ビジネス価格が定価と等しく設定されます。 ビジネス価格は、有効な場合、web サイトの価格範囲に従います。 ビジネス価格を 1 ドル未満にすることはできません。</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | （必須）オプション： <ul><li>**[!UICONTROL Disabled]** - （デフォルト）すべての受注数量に対して同じ上場価格が必要な場合に選択します。 選択した場合、すべて _[!UICONTROL Pricing Level]_このセクションのフィールドは無効です。</li><li>**[!UICONTROL Enabled]**  – 注文数量に基づいて調整する価格設定を有効にするタイミングを選択します。 選択した場合、 _[!UICONTROL Pricing Level]_フィールドが有効になっています。</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | Tiered Pricing が有効化されている場合は、ビジネス・リストの階層価格を設定する数量/割引設定を最大 5 つ定義できます。 各行に、適用する数量しきい値と割引率を入力します。 例えば、と入力した場合、 `5` 先頭行の先頭フィールドに `5` 2 番目のフィールドでは、別の事業者が 5 つ以上の数量を購入した場合、価格は 5% の割引を適用します。 |

**クイックアクセス** - [!UICONTROL Listing Settings] セクション

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
