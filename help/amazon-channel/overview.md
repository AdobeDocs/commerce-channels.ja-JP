---
title: 「の概要  [!DNL Amazon Sales Channel]」
description: 「[!DNL Amazon Sales Channel] を使用すると、マーチャントは  [!DNL Amazon Marketplace] でシームレスに製品を販売できます」。
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] の概要

Adobe CommerceまたはMagento Open Sourceマーチャントの場合、[!DNL Amazon Sales Channel] 拡張機能を使用して、店舗を世界最大のグローバルインターネットショッピング先と統合できます。 この拡張機能により、[!DNL Commerce] と [!DNL Amazon Seller Central] アカウントを結び付け、カタログと注文データの自動化と同期の両方を提供することで、Amazonの販売が可能になります。 すべてのAmazonのリストを完全に管理し、シンプルまたはインテリジェントな価格ルールを導入し、1 つの [!DNL Commerce] ダッシュボードを介して注文と在庫を管理します。

[ オンボーディング ](./amazon-onboarding-home.md) 後、[!DNL Commerce] はAmazon ストアのAmazonのリスト、注文、在庫、価格を管理および制御する「中央コマンドセンター」になります。 [ ストア統合 ](./store-integration.md) は、[!DNL Commerce] インスタンスとAmazonを接続して、両方のプラットフォーム間でデータを同期します。 Amazonのセールスチャネルでは、次のことが可能です。

- [ オンボード ](./amazon-onboarding-home.md) し、1 つ以上の [!DNL Amazon Seller Central] アカウントをAdobe CommerceまたはMagento Open Sourceと統合します。

- 既存のAmazonのリストを読み込んで同期し、[!DNL Commerce] カタログ内の商品と一致させて、一元化された商品カタログを作成します。

- [!DNL Commerce] カタログ内の商品のAmazon リストを作成および管理します。

- [!DNL Commerce] とAmazonの注文を表示して履行（出荷）し、注文のステータス、支払い、払い戻しの情報を同期します。

- [ 競合価格 ](./competitive-price-analysis.md)、[ リストの変更 ](./listing-changes-log.md)、および [ コミュニケーションの問題 ](./communication-errors-log.md) の分析およびエラーのログを表示します。

Amazon ストアにアクセスして、Amazon セールスチャネル [ ホームページ ](./amazon-sales-channel-home.md) 上のこれらすべての機能、アカウント情報、リスト、注文などを表示および管理します。

## プロモーションと価格設定

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- Amazonのリスト価格 [!DNL Commerce] カタログ価格（または代替価格属性）に同期します。

- Amazonのリストで MSRP[ ストライクスルー価格 ](./listing-price.md#configure-listing-price-settings) を有効にして、お客様の価値提案を高めます。

- Amazon リストで [ 最小広告価格（MAP） ](./listing-price.md#configure-listing-price-settings) を有効にして管理します。

- Amazonの価格で追加の [VAT 税 ](./listing-price.md#configure-listing-price-settings) を設定します。

- Amazonのリストに表示して買い手の緊急度を高めるには、[ 在庫/数量の設定 ](./stock-quantity.md#configure-stock--quantity-settings) で「利用可能数量」のカスタム値を設定します。

## 価格ルール

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 積み重ねが可能で、柔軟性があり、複雑な [ 価格ルール ](./pricing-products.md) を作成して、Amazonの価格を管理し、毎日のセールや季節的なプロモーションに対応します。

- [floor](./floor-price.md) および [ceiling](./optional-ceiling-price.md) 価格を作成して、最低価格と最高価格を保護します。

- Amazonの他の競合製品 [ 競合製品の中で最も低い価格 ](./intelligent-repricing-rules.md) と [Buy Boxの価格 [）を基準に製品の価格を自動調整する ](./lowest-competitor-pricing.md) インテリジェントな価格 ](./buy-box-competitor-pricing.md) ルール）を作成および管理します。

## カタログフィードの管理

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 既存のAmazonのリスト（商品）を読み込み、[!DNL Commerce] カタログで既存の商品と一致するか商品を作成します。

- [!DNL Commerce] の商品をAmazonにPublishして、Amazonのリストを作成します。

- 個々の価格、処理時間、条件、販売者のメモメッセージを設定する [ 上書き ](./creating-editing-overrides.md) を作成します。

- Amazonのリストから商品 [ 属性 ](./attributes-view.md) を読み込んでマッピングし、[!DNL Commerce] カタログの商品と自動的に一致させます。

- 複数の検索パラメーターを設定して、Amazonのリストを [!DNL Commerce] カタログに一致させます。

- [ リストルール ](./listing-rules.md) を定義して、Amazonにリストできる [!DNL Commerce] 製品を決定します。

- 新しいAmazon リストにデフォルトの [ 処理時間 ](./product-listing-actions.md) を設定します。

- [!DNL Commerce] 属性に基づいてリスト条件に一致させます。

- 条件タイプごとに販売者メモを追加します（オプション）。

- Amazonのリストを [!DNL Commerce] カタログに読み込む際に、数量のしきい値を実装します。

- 推奨される [ リストの改善 ](./listing-improvements.md) を表示します。

## 注文管理とカスタマーサービス

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- Amazonおよび [!DNL Commerce] での注文のサポートと処理。

- Amazonの注文を [!DNL Commerce] に [ 読み込み ](./order-settings.md#configure-order-settings) るか、Amazonに残します。

- 注文の読み込みと管理のために、Amazonの注文に関連付ける [!DNL Commerce] web サイトストアを定義します。

- [ フルフィルメント設定 ](./fulfilled-by.md) に応じて、[!DNL Commerce] またはAmazonから注文を表示、キャンセル、出荷できます。

- Amazonの注文ステータスを [!DNL Commerce] 内のカスタムステータスにマッピングします（オプション）。

- 注文エラーを表示および管理して、問題を解決し、顧客とつながります。

- 注文トラッキングデータを [!DNL Amazon Seller Central] アカウントに送信します。

- [ 注文をキャンセル ](./cancel-unshipped-order.md) し、理由応答を選択します。

- Amazonの注文に関する [ 最近の注文 ](./amazon-store-dashboard.md) 情報を表示します。

## 報告書

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次の内容に関するレポート情報を確認できます。

- 有効、無効、適格および未完了のステータス別のリスト。

- 出荷待ちの注文。

- 最新の注文。

- Amazon[ 変更ログの一覧表示 ](./listing-changes-log.md) を使用して、商品やフィードの変更（価格や数量など）を確認できます。

- 商品 [Buy Box](./buy-box-competitor-pricing.md) 競合他社価格データ。

- 製品 [ 競合他社価格の最低 ](./lowest-competitor-pricing.md) データ。

## グローバル・セールスのサポート

[!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 複数の [!DNL Amazon Marketplace] 地域（国）を管理します。

- [Commerce通貨設定ツール ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html) を使用して複数通貨をサポートします。

- 商品拠点およびAmazonフルフィルメントセンターからの配送を管理します。

## 顧客管理

Amazonの注文に関連付けられた [ 顧客データの読み込み ](./order-settings.md#configure-order-settings) を行って、[!DNL Commerce] しい顧客データベースを作成します。 [!DNL Amazon Marketplace] のリストやストアフロントを通じて、顧客のリストを拡大し、マーケティングの可能性 [!DNL Commerce] 高めます。


使い始めるのは簡単です。 簡単なオンボーディングプロセスのガイドに従って、[!DNL Amazon Seller Central] アカウントを作成し、Amazon セールスチャネルストアや [!DNL Commerce] カタログと統合して、Amazonのリスト、注文、在庫、フルフィルメントを管理できます。 中央のダッシュボードには、Amazonのセールスチャネルストアにおけるすべての統合とAmazonのリストに関するステータス更新が表示されます。 新しいシステムの導入にかかるコストと労力を最小限に抑え、プロセスのシンプル化と自動化を実現することで、グローバル [!DNL Amazon Marketplace] ースの新規顧客にリーチします。

[!DNL Amazon Seller Central] アカウントを統合した後、[!DNL Amazon Sales Channel] 拡張機能を使用すると、アカウントを管理し、[!DNL Commerce] とAmazonの間でデータを同期できます。 [!DNL Commerce] Admin を介して、リストの作成、プロモーションの管理、価格の設定、在庫とフルフィルメントの管理を直接行うことができます。 これらのオプションには、同じ商品のAmazonの価格をモニタリングし、より競争力のある価格になるように自動的に調整する価格ルールが含まれます。

