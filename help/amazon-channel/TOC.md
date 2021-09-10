---
user-guide-title: AmazonSales Channelユーザーガイド
user-guide-description: Amazonを通じてAdobeコマースまたはMagento Open Sourceを [!DNL Amazon Seller Central] アカウントと統合し、販売を創出します。
breadcrumb-title: コマース用チャネルマネージャー
source-git-commit: 52f2dd0f5a722af337be72a5d556f3780aad6548
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# AmazonAdobe- [!DNL channel manager] （販売コマース用） {#amazon}

- [Amazon販売チャネル](overview.md)
- はじめに{#getting-started}
   - [Amazon販売チャネルについて](about-amazon-sales-channel.md)
   - [Amazon Marketplaceについて](about-amazon-marketplace.md)
   - [Amazonとコマースカタログについて](about-listings-and-catalog.md)
   - [ベストプラクティスと制限事項](amazon-best-practices.md)
   - [拡張機能のインストール](install.md)
- オンボーディング{#onboarding}
   - [Amazonの販売チャネルのオンボーディング](amazon-onboarding-home.md)
   - [事前設定タスク](amazon-pre-setup-tasks.md)
   - [Amazonの [!DNL Commerce] 属性を作成します](ob-creating-magento-attributes.md)
   - [Amazon APIキーの検証](amazon-verify-api-key.md)
   - [ストア統合](store-integration.md)
   - [リストルールの作成](ob-create-listing-rule.md)
   - [デフォルトのストア設定](default-store-settings.md)
- 販売チャネル{#manage}を管理します
   - [ホームページ](amazon-sales-channel-home.md)
   - [Amazon店](managing-stores.md)
   - [Workspaceのコントロール](workspace-controls.md)
   - [学習と準備](learning-preparation.md)
   - 属性{#attributes}
      - [属性の表示](attributes-view.md)
      - [属性の管理](managing-attributes.md)
      - [属性の作成と編集](creating-attributes.md)
      - [属性マッピングの表示](amazon-matching-attributes-values.md)
   - [販売チャネル管理者の設定](sales-channel-settings.md)
   - [Amazon Storeダッシュボード](amazon-store-dashboard.md)
   - [ストア設定](ob-store-review.md)
- リスト設定{#listing-settings}
   - [リスト設定の表示](listing-settings.md)
   - [製品リストアクション](product-listing-actions.md)
   - [サードパーティ製品表](third-party-listing-settings.md)
   - [上場価格](listing-price.md)
   - [(B2B)ビジネス価格](business-pricing.md)
   - [在庫/数量](stock-quantity.md)
   - [履行者](fulfilled-by.md)
   - [カタログ検索](catalog-search.md)
   - [製品リスト条件](product-listing-condition.md)
   - [更新された製品](renewed-products.md)
- [順序の設定](order-settings.md)
- [ストア統合設定](store-integration-settings.md)
- リストと価格のルール{#rules}
   - [ルールの一覧](listing-rules.md)
   - 価格ルール{#pricing-rules}
      - [価格の管理](pricing-products.md)
      - [新しい価格ルールの追加](add-pricing-rule.md)
      - [価格ルールの一般設定](pricing-rule-general-settings.md)
      - [価格ルール条件](pricing-rule-conditions.md)
      - [価格ルールのアクション](pricing-rule-actions.md)
      - [標準価格ルール](standard-price-rules.md)
      - [インテリジェントな価格変更ルール](intelligent-repricing-rules.md)
      - [競合相手の条件の相違](competitor-conditional-variances.md)
      - [価格調整](price-adjustment.md)
      - [下限価格](floor-price.md)
      - [オプションの上限価格](optional-ceiling-price.md)
      - [価格の範囲](price-scope.md)
      - [価格の優先度ロジック](price-priority-logic.md)
      - [Buy Box競合他社の価格](buy-box-competitor-pricing.md)
      - [競合企業の最も低い価格](lowest-competitor-pricing.md)
   - 例{#rules-examples}
      - [条件の定義](ob-define-condition-example.md)
      - [価格ルールの例](price-rule-examples.md)
- レポートとログ{#reports-logs}
   - [ログとストアレポート](amazon-logs-reports.md)
   - ストアレポート{#store-reports}
      - [競合価格の分析](competitive-price-analysis.md)
      - [リストの改善点](listing-improvements.md)
   - ログ{#logs}
      - [変更ログのリスト](listing-changes-log.md)
      - [通信エラーログ](communication-errors-log.md)
- リストの管理{#admin-listings}
   - [Amazon一覧の管理](managing-product-listings.md)
   - ステータス/タブ別{#status-tab}
      - [ステータス/タブで管理](managing-listings-by-tab.md)
      - [不完全なリスト](incomplete-listings.md)
      - [新しいサードパーティのリスト](new-third-party-listings.md)
      - [リストへの登録準備完了](ready-to-list.md)
      - [非アクティブなリスト](inactive-listings.md)
      - [アクティブなリスト](active-listings.md)
      - [上書き](overrides.md)
      - [不適格なリスト](ineligible-listings.md)
      - [終了した一覧](ended-listings.md)
   - アクション別{#actions}
      - [アクションで管理](managing-listings-by-action.md)
      - [カタログ製品の作成と割り当て](creating-assigning-catalog-products.md)
      - [上書きの作成と編集](creating-editing-overrides.md)
      - [Alias販売者SKUの作成](create-alias-seller-sku.md)
      - [割り当てられたASINの編集](edit-assigned-asin.md)
      - [Amazonリストの終了](end-listings-manually.md)
      - [Amazonリストの公開](publish-listings-manually.md)
      - [必要な情報を更新](amazon-manually-update-incomplete-listing.md)
      - [詳細の表示](product-listing-details.md)
- 注文の管理{#admin-orders}
   - [注文の管理](managing-orders.md)
   - [Amazon注文の表示](amazon-orders-all.md)
   - [Amazon注文の詳細の表示](amazon-order-details.md)
   - [一般的な注文処理タスク](common-order-processing.md)
   - [フルフィルメントワークフロー](fulfillment-workflows.md)
   - [未出荷注文のキャンセル](cancel-unshipped-order.md)
