---
title: Amazon販売チャネルについて
description: Amazonのセールスチャネル拡張機能を使用して、AdobeのコマースまたはMagento Open SourceをAmazonのセラーセントラルアカウントとシームレスに統合します。
exl-id: 11752491-d0da-4ff7-a0a7-d17d4fa1bfc9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Amazon販売チャネルについて

Adobeコマース用のChannel Managerは、Amazonセールスチャネル拡張機能を提供し、[!DNL Commerce]管理者を[!DNL Amazon Seller Central]アカウントとシームレスに統合します。 [オンボーディング](./amazon-onboarding-home.md)後、[!DNL Commerce]は、AmazonストアのAmazonリスト、注文件数、在庫数、価格を管理および制御する「中央コマンドセンター」になります。

[ストア統](./store-integration.md) 合は、インスタン [!DNL Commerce] スとAmazonを接続して、両方のプラットフォーム間でデータを同期します。Amazon sales channelでは、次のことが可能です。

- [](./amazon-onboarding-home.md) 1つ以上のアカウントをオンボードし、 [!DNL Amazon Seller Central] AdobeコマースまたはMagento Open Sourceと統合します。

- 既存のAmazonのリストを読み込んで同期し、[!DNL Commerce]カタログ内の製品に一致させて、一元化された製品カタログを作成します。

- [!DNL Commerce]カタログ内の製品のAmazonリストを作成および管理します。

- [!DNL Commerce]とAmazonで注文を表示し、履行（出荷）し、注文ステータス、支払い、返金情報を同期します。

- [競合価格](./competitive-price-analysis.md)、[リスト変更](./listing-changes-log.md)、[通信の問題](./communication-errors-log.md)の分析とエラーを表示します。

Amazonストアにアクセスして、Amazonセールスチャネル[のホームページ](./amazon-sales-channel-home.md)でこれらの機能、アカウント情報、リスト、注文などをすべて表示および管理します。

## プロモーションと価格

拡張子[!DNL Amazon Sales Channel]を使用すると、次のことが可能になります。

- Amazonの上場価格を[!DNL Commerce]カタログ価格（または代替価格属性）に同期します。

- AmazonのリストでMSRP [ストライクスルー価格](./listing-price.md#configure-listing-price-settings)を有効にして、顧客の価値提案を増やします。

- Amazonのリストで[Minimum Advertised Price(MAP)](./listing-price.md#configure-listing-price-settings)を有効にして管理します。

- Amazonの価格で追加の[VAT税](./listing-price.md#configure-listing-price-settings)を設定します。

- [在庫/数量の設定](./stock-quantity.md#configure-stock--quantity-settings)で「利用可能な数量」のカスタム値を設定し、Amazonのリストに表示して、購入者の緊急性を高めます。

## 価格ルール

拡張子[!DNL Amazon Sales Channel]を使用すると、次のことが可能になります。

- スタック可能で柔軟で複雑な[価格ルール](./pricing-products.md)を作成して、日々の販売や季節ごとのプロモーションに関するAmazonの価格を管理します。

- [floor](./floor-price.md)と[ceiling](./optional-ceiling-price.md)の価格を作成し、最安値と最高値を保護します。

- Amazonの他の競合相手([最も低い競合相手](./lowest-competitor-pricing.md)および[Buy Box](./buy-box-competitor-pricing.md)価格)と比較して、製品の価格を自動的に調整する[インテリジェントな再価格設定ルール](./intelligent-repricing-rules.md)を作成および管理します。

## カタログフィードの管理

拡張子[!DNL Amazon Sales Channel]を使用すると、次のことが可能になります。

- 既存のAmazonのリスト（製品）を読み込み、[!DNL Commerce]カタログの既存の製品に一致させるか、製品を作成します。

- [!DNL Commerce]製品をAmazonに公開して、Amazonリストを作成します。

- [overrides](./creating-editing-overrides.md)を作成して、個々の価格を設定し、時間、条件、販売者のメモメッセージを処理します。

- Amazonのリストから製品[属性](./attributes-view.md)を読み込んでマッピングし、[!DNL Commerce]カタログ内の製品と自動的に一致させます。

- Amazonのリストを[!DNL Commerce]カタログに一致させるには、複数の検索パラメーターを設定します。

- [リストルール](./listing-rules.md)を定義して、Amazonにリストする[!DNL Commerce]製品を決定します。

- 新しいAmazonリストの処理時間[をデフォルトに設定します。](./product-listing-actions.md)

- [!DNL Commerce]属性に基づく一致リスト条件。

- 各条件タイプに販売者向けのメモを追加します（オプション）。

- [!DNL Commerce]カタログにAmazonリストを読み込む際に、数量のしきい値を実装します。

- 推奨[リストの改善](./listing-improvements.md)を表示します。

## 注文管理と顧客サービス

拡張子[!DNL Amazon Sales Channel]を使用すると、次のことが可能になります。

- Amazonと[!DNL Commerce]での注文のサポートと処理。

- [](./order-settings.md#configure-order-settings) Amazonの注文をにインポ [!DNL Commerce] ートするか、Amazonに残します。

- [!DNL Commerce] Webサイトのどれを、注文のインポートと管理のためにAmazonの注文に関連付けるかを定義します。

- [履行設定](./fulfilled-by.md)に応じて、[!DNL Commerce]やAmazonからの注文を表示、取り消し、出荷します。

- [!DNL Commerce]内でAmazonの注文ステータスをカスタムステータスにマッピングします（オプション）。

- 注文エラーを表示および管理して問題を解決し、顧客と接続します。

- [!DNL Amazon Seller Central]アカウントに注文の追跡データを送信します。

- [オーダー](./cancel-unshipped-order.md) をキャンセルし、理由応答を選択します。

- Amazonの注文に関する[最近の注文](./amazon-store-dashboard.md)情報を表示します。

## レポート

拡張子[!DNL Amazon Sales Channel]を使用すると、次の情報に関するレポート情報を確認できます。

- アクティブ、非アクティブ、適格および不完全のステータス別のリスト。

- 出荷待ちの注文。

- 最新の注文。

- Amazon [製品/リストフィードの変更（価格や数量など）を確認するための変更ログ](./listing-changes-log.md)をリストします。

- 製品[Buy Box](./buy-box-competitor-pricing.md)競合相手の価格データ。

- 製品[競合他社の最低価格の価格](./lowest-competitor-pricing.md)データ。

## グローバル販売のサポート

拡張子[!DNL Amazon Sales Channel]を使用すると、次のことが可能になります。

- 複数の[!DNL Amazon Marketplace]地域（国）を管理します。

- [[!DNL Commerce] 通貨換算ツール](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}を使用して複数の通貨をサポートします。

- 製品の保管場所とAmazonのフルフィルメントセンターからの出荷を管理します。

## 顧客管理

[顧客データ](./order-settings.md#configure-order-settings)をインポートして、Amazonの注文に関連付けられた顧客データを[!DNL Commerce]顧客データベースを構築します。 [!DNL Amazon Marketplace]リストと[!DNL Commerce]ストアフロントを通じて、顧客のリストを拡張し、マーケティングの可能性を高めます。
