---
user-guide-title: Amazon Sales Channel ユーザーガイド
user-guide-description: Adobe CommerceまたはMagento Open Sourceをお客様のアカウントと統合することにより、Amazonを通じて売上  [!DNL Amazon Seller Central]  創出します。
breadcrumb-title: Amazon セールスチャネル
role: Admin, User
feature: Sales Channels
recommendations: noDisplay
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---


# Amazon販売チャネル - Adobe Commerceの [!DNL channel manager] {#amazon}

- [Amazon Sales Channel ユーザーガイド](guide-overview.md)
- [Amazonのセールスチャネルの概要](overview.md)
- 入門 {#getting-started}
   - [Amazon Marketplace について](about-amazon-marketplace.md)
   - [AmazonとCommerce カタログ](about-listings-and-catalog.md)
   - [ベストプラクティスと制限事項](amazon-best-practices.md)
   - [拡張機能のインストール](install.md)
- Onboarding {#onboarding}
   - [オンボードAmazonセールスチャネル](amazon-onboarding-home.md)
   - [事前設定タスク](amazon-pre-setup-tasks.md)
   - [Amazonの属性  [!DNL Commerce]  作成](ob-creating-magento-attributes.md)
   - [Amazon API キーの確認](amazon-verify-api-key.md)
   - [ストアの統合](store-integration.md)
   - [リストルールの作成](ob-create-listing-rule.md)
   - [デフォルトのストア設定](default-store-settings.md)
- 販売チャネル {#manage} ータの管理
   - [ホームページ](amazon-sales-channel-home.md)
   - [Amazon ストア](managing-stores.md)
   - [Workspaceの制御](workspace-controls.md)
   - [学習と準備](learning-preparation.md)
   - 属性 {#attributes}
      - [属性を表示](attributes-view.md)
      - [属性の管理](managing-attributes.md)
      - [属性の作成と編集](creating-attributes.md)
      - [属性マッピングの表示](amazon-matching-attributes-values.md)
   - [販売チャネル管理設定](sales-channel-settings.md)
   - [Amazon ストアダッシュボード](amazon-store-dashboard.md)
   - [ストアの設定](ob-store-review.md)
- リスト設定 {#listing-settings}
   - [リスト設定の表示](listing-settings.md)
   - [製品リストのアクション](product-listing-actions.md)
   - [サードパーティのリスト](third-party-listing-settings.md)
   - [上場価格](listing-price.md)
   - [（B2B）ビジネスプライシング](business-pricing.md)
   - [在庫/数量](stock-quantity.md)
   - [履行者](fulfilled-by.md)
   - [カタログ検索](catalog-search.md)
   - [商品リストの条件](product-listing-condition.md)
   - [更新済み製品](renewed-products.md)
- [オーダー設定](order-settings.md)
- [ストア統合設定](store-integration-settings.md)
- リストおよび価格設定ルール {#rules}
   - [リストルール](listing-rules.md)
   - 価格ルール {#pricing-rules}
      - [価格の管理](pricing-products.md)
      - [新しい価格ルールを追加](add-pricing-rule.md)
      - [価格ルールの一般設定](pricing-rule-general-settings.md)
      - [価格ルール条件](pricing-rule-conditions.md)
      - [価格ルールアクション](pricing-rule-actions.md)
      - [標準価格ルール](standard-price-rules.md)
      - [インテリジェントな再価格設定ルール](intelligent-repricing-rules.md)
      - [競合他社条件付き差異](competitor-conditional-variances.md)
      - [価格調整](price-adjustment.md)
      - [フロアプライス](floor-price.md)
      - [オプションの上限価格](optional-ceiling-price.md)
      - [価格範囲](price-scope.md)
      - [価格優先度ロジック](price-priority-logic.md)
      - [Buy Boxの競合他社価格](buy-box-competitor-pricing.md)
      - [競合製品の最低価格](lowest-competitor-pricing.md)
   - {#rules-examples} の例
      - [条件の定義](ob-define-condition-example.md)
      - [価格ルールの例](price-rule-examples.md)
- レポートとログ {#reports-logs}
   - [ログとストアレポート](amazon-logs-reports.md)
   - レポート {#store-reports} 保存
      - [競争価格分析](competitive-price-analysis.md)
      - [リストの改善](listing-improvements.md)
   - Logs {#logs}
      - [変更ログのリスト](listing-changes-log.md)
      - [通信エラーログ](communication-errors-log.md)
- Manage listings {#admin-listings}
   - [Amazon リストの管理](managing-product-listings.md)
   - ステータス/タブ {#status-tab} 別
      - [ステータス/タブで管理](managing-listings-by-tab.md)
      - [不完全な一覧](incomplete-listings.md)
      - [新しいサード パーティの一覧](new-third-party-listings.md)
      - [リストの準備完了](ready-to-list.md)
      - [非アクティブな一覧](inactive-listings.md)
      - [アクティブな一覧](active-listings.md)
      - [上書き](overrides.md)
      - [不適格な一覧](ineligible-listings.md)
      - [終了した一覧](ended-listings.md)
   - アクション {#actions} 別
      - [アクションで管理](managing-listings-by-action.md)
      - [カタログ製品の作成と割り当て](creating-assigning-catalog-products.md)
      - [上書きの作成と編集](creating-editing-overrides.md)
      - [Alias Seller SKU の作成](create-alias-seller-sku.md)
      - [割り当てられた ASIN の編集](edit-assigned-asin.md)
      - [Amazon リストの終了](end-listings-manually.md)
      - [PublishとAmazonのリスト](publish-listings-manually.md)
      - [必要な情報を更新](amazon-manually-update-incomplete-listing.md)
      - [詳細を表示](product-listing-details.md)
- 注文の管理 {#admin-orders}
   - [注文の管理](managing-orders.md)
   - [Amazonの注文を表示](amazon-orders-all.md)
   - [Amazonの注文の詳細を表示](amazon-order-details.md)
   - [一般的なオーダー処理タスク](common-order-processing.md)
   - [フルフィルメントワークフロー](fulfillment-workflows.md)
   - [未出荷の注文のキャンセル](cancel-unshipped-order.md)
- [リリースノート](release-notes.md)
