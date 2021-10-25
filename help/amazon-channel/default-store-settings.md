---
title: デフォルトのストア設定
description: デフォルトの Commerce 設定を変更して、ストアの Amazon 販売チャンネルをカスタマイズします。
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# デフォルトのストア設定

ストアが接続され、最初のリスティングルールが設定されると、Amazon とその間のデータ同期が開始され [!DNL Commerce] ます。 ストア設定にはいくつかの種類があります。これにより、必要に応じてストアをカスタマイズすることができます。 ストアの設定は、ストアのダッシュボードからアクセスされ [ ](./amazon-store-dashboard.md) ます。

ストア設定は以下のとおりです。

- [**[!UICONTROL Listing settings]**](./listing-settings.md) -製品カタログがにどのように作用するかを制御 [!DNL Amazon Marketplace] します。

- [**[!UICONTROL Order settings]**](./order-settings.md) -Amazon の注文を管理する方法を制御します。

- [**[!UICONTROL Listing rules]**](./listing-rules.md) -Amazon に記載されているカタログ製品を定義します。

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) -認定リストについて Amazon list 価格がどのように変更されるかを定義します。

- **[!UICONTROL Store reports]** - [ 競争価格の分析 ](./competitive-price-analysis.md) と [ リスト ](./listing-improvements.md) の改善

- **[!UICONTROL Logs]** - [ 変更および通信エラーの一覧を表示し ](./listing-changes-log.md) [ ](./communication-errors-log.md) ます。

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) -「管理者」で、電子メールと Amazon channel store name の設定を確認して [!DNL Commerce] ください。

## 重要な初期設定

| , | デフォルト | つい | 場所 |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | [!DNL Commerce]Amazon から新しい注文を受信したときに、対応する注文が作成されます。これを使用すると、注文が [[!DNL Commerce]  ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} ワークフローで管理されます。このようにすると `Disabled` 、Amazon によって注文情報がレビュー用にインポートされますが、注文は自分のアカウントで管理する必要があり [!DNL Amazon Seller Central] ます。 | [オーダー設定](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Amazon orders から取得された得意先データは、データベースにインポートされません [!DNL Commerce] 。 読み込んだ Amazon orders は、ゲストのチェックアウトとして処理されます。 顧客データベースを構築する場合は [!DNL Commerce] 、この設定をに変更する必要があり `Build New Customer Account` ます。 | [オーダー設定](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] amazon に自動的に公開し、Amazon リストを作成するカタログ製品 (Amazon の特典条件を満たします)。 製品を手動でレビューおよび公開する場合は、この設定をに変更する必要があり `Do Not Automatically List Eligible Products` ます。 手動でパブリッシュを待つ製品は、「 [_準備完了」タブに表示され_](./ready-to-list.md) ます。 | [製品リストのアクション](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Amazon リストのベースとして使用される「価格ソース」属性を定義します。 価格設定の基準となる基準価格に属性を使用しない場合は [!DNL Commerce] `Price` 、この設定を別の属性に変更する必要があります。 | [リスト価格](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | すべての注文は、商人によって履行されます。 Amazon による納品手続きを使用している場合、または複数のフルフィルメントメソッドを使用している場合は、この設定を変更する必要があります。 | [によって満たされる](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | すべての製品が同じ条件になっている場合は、Amazon 条件オプションのいずれかを選択して、すべての製品を表すことができます。 カタログに異なる条件の製品が含まれている場合 (新規、使用、修正など) は、この設定を変更して、その `Assign Condition Using Product Attribute` [!DNL Commerce] 条件属性を Amazon リスト条件に割り当てる必要があります。 | [製品のリスト表示条件](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | &quot; | Amazon 販売チャンネルが Amazon に公開する製品を決定するために使用するルールを定義します。 このルールには、製品一覧に製品を含めたり除外したりするために単純な複雑なルールを作成するためのオプションが数多く用意されています。 | [ルールの一覧表示](./listing-rules.md) |
| 価格ルール | &quot; | 出展価格で定義されているものとは異なる Amazon の一覧価格属性を定義 _[!UICONTROL Magento Price Source]_[ ](./listing-price.md) します。 設定した価格 (上または下) を設定して調整するに_[!UICONTROL Magento Price Source]_ は、ルールを作成します。 | [価格ルール](./pricing-products.md) |

詳しくは、ストア設定を参照してください [ ](./ob-store-review.md) 。
