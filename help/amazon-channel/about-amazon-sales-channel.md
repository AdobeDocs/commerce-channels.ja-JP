---
title: Amazon sales チャネルについて
description: Amazon 販売チャンネル拡張機能を使用すると、Amazon 売り手の中央アカウントを使用して、Adobe 経済または Magento オープンソースをシームレスに統合できます。
exl-id: 11752491-d0da-4ff7-a0a7-d17d4fa1bfc9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Amazon sales チャネルについて

Adobe Commerce 用の channel manager は、Amazon sales channel 拡張機能を提供します。これにより、 [!DNL Commerce] 管理者が自分のアカウントとシームレスに統合さ [!DNL Amazon Seller Central] れます。 オンボードの後は [ ](./amazon-onboarding-home.md) 、amazon [!DNL Commerce] store の amazon リスト、注文、インベントリ、および価格設定を管理および制御するための「中央コマンドセンター」になります。

[ストア統合 ](./store-integration.md) により、 [!DNL Commerce] インスタンスと Amazon が両方のプラットフォーム間でデータを同期するために接続されます。 Amazon 販売チャンネルを使用すると、次のことができます。

- [](./amazon-onboarding-home.md)1 つまたは複数 [!DNL Amazon Seller Central] のアカウントを Adobe Commerce または Magento オープンソースを使用して統合します。

- 既存の Amazon リストを読み込み、同期して、カタログ内の製品に適合させ [!DNL Commerce] 、一元化された製品カタログを作成します。

- カタログ内の製品の Amazon リストを作成および管理し [!DNL Commerce] ます。

- [!DNL Commerce]Amazon、Amazon、注文状況、支払、払い戻し情報を同期する注文を表示して履行 (出荷) することができます。

- 競争価格の分析とエラー [ 、変更の一覧、および通信に関する問題について、記録を表示し ](./competitive-price-analysis.md) [ ](./listing-changes-log.md) [ ](./communication-errors-log.md) ます。

このような機能、取引先企業情報、番組表、注文、その他のすべての機能を表示および管理するには、amazon 店にアクセスします。このページには、Amazon 販売チャンネルのホームページが表示さ [ ](./amazon-sales-channel-home.md) れます。

## プロモーションと価格設定

拡張機能を使用して [!DNL Amazon Sales Channel] 、次の操作を実行できます。

- Amazon の一覧価格を [!DNL Commerce] カタログ価格に同期します (または、代替価格属性)。

- MSRP 取り消し線を使用して [ ](./listing-price.md#configure-listing-price-settings) 、Amazon リストの価格が改善され、お客様のバリュープロポジションを向上させることができます。

- [Amazon リストに記載されている最低公表価格 (マップ) を有効にして管理し ](./listing-price.md#configure-listing-price-settings) ます。

- [ ](./listing-price.md#configure-listing-price-settings) Amazon 価格の追加 VAT 税を設定します。

- 購入者の [ ](./stock-quantity.md#configure-stock--quantity-settings) 緊急性を高めるために、Amazon リストに表示するには、stock/quantity 設定に「有効な量」にカスタム値を設定します。

## 価格ルール

拡張機能を使用して [!DNL Amazon Sales Channel] 、次の操作を実行できます。

- 、積み重ね可能な、柔軟、複雑な各 [ 価格ルール ](./pricing-products.md) を作成して、その Amazon 価格を日常的なセールや季節による宣伝の価格設定に対応させることができます。

- [ ](./floor-price.md) [ ](./optional-ceiling-price.md) 最低および最高価格を保護するために、フロア価格と天井価格を作成することができます。

- [ ](./intelligent-repricing-rules.md) 他の Amazon 競合企業を基準として製品価格が自動的に調整されるインテリジェントな価格設定ルールを作成および管理 [ します (競合企業 ](./lowest-competitor-pricing.md) と [ 購入ボックスの価格が低く ](./buy-box-competitor-pricing.md) なります)。

## カタログフィードの管理

拡張機能を使用して [!DNL Amazon Sales Channel] 、次の操作を実行できます。

- 既存の Amazon リスト (製品) を読み込んで、カタログ内の既存の製品または製品を作成し [!DNL Commerce] ます。

- 製品を Amazon に公開して、 [!DNL Commerce] amazon リストを作成します。

- [個別の ](./creating-editing-overrides.md) 価格、取扱時間、条件、および販売店の注意メッセージを設定する上書きを作成します。

- 作成し [ ](./attributes-view.md) た Amazon リストの製品属性は、カタログ内の製品と自動的に一致させることが [!DNL Commerce] できます。

- Amazon リストをカタログに合わせるように、複数の検索パラメーターを設定 [!DNL Commerce] します。

- [リストルール ](./listing-rules.md) を定義して、Amazon の対象となる製品を特定し [!DNL Commerce] ます。

- [新しい Amazon リストのデフォルト処理時間を設定 ](./product-listing-actions.md) します。

- 属性に基づいて一覧表示条件を一致させ [!DNL Commerce] ます。

- 各条件タイプに対して「販売者」ノートを追加します (オプション)。

- Amazon リストをカタログにインポートする場合は、quantity しきい値 [!DNL Commerce] を実装します。

- 推奨される [ 一覧 ](./listing-improvements.md) の改善を表示します。

## 注文管理およびカスタマーサービス

拡張機能を使用して [!DNL Amazon Sales Channel] 、次の操作を実行できます。

- Amazon および. での注文のサポートおよび処理を行い [!DNL Commerce] ます。

- [Amazon ](./order-settings.md#configure-order-settings) から amazon の注文を読み込む [!DNL Commerce] か、またはそのままにします。

- [!DNL Commerce]注文のインポートと管理を行うために、Amazon 注文に関連付けられた web サイトストアを定義します。

- フルフィルメント設定によっては、Amazon からの注文や Amazon からの注文、 [!DNL Commerce] またはその両方を設定することが [ ](./fulfilled-by.md) できます。

- Amazon の注文状況をカスタム状態にマップ [!DNL Commerce] します (オプション)。

- 問題を解決し、顧客に関連付けて、注文エラーを表示して管理します。

- 取引先企業に注文追跡データを送信 [!DNL Amazon Seller Central] します。

- [注文 ](./cancel-unshipped-order.md) をキャンセルし、理由応答を選択します。

- [ ](./amazon-store-dashboard.md) Amazon の注文に関する最新の注文情報を表示します。

## 書

拡張機能を使用して [!DNL Amazon Sales Channel] 、次のようなレポート情報を確認できます。

- 一覧は、状態 (アクティブ、非アクティブ、適格、未完) によって一覧されます。

- 出荷待ちの注文です。

- 最新の注文です。

- Amazon [ が表示されたときに、その変更がログに記録さ ](./listing-changes-log.md) れます。製品について (価格、数量など)

- 製品 [ 購入ボックス ](./buy-box-competitor-pricing.md) 競合企業の価格データです。

- 製品 [ の最も低い競合企業価格 ](./lowest-competitor-pricing.md) データです。

## グローバルなセールス向けのサポート

拡張機能を使用して [!DNL Amazon Sales Channel] 、次の操作を実行できます。

- マルチ [!DNL Amazon Marketplace] リージョン (国) を管理します。

- 通貨換算ツールを使用した複数の通貨のサポート [[!DNL Commerce]  ](https://docs.magento.com/user-guide/stores/currency-configuration.html) {target = &quot;_blank&quot;}。

- 製品の出荷先および Amazon フルフィルメントセンターからの出荷を管理します。

## 顧客管理

Amazon の [!DNL Commerce] [ ](./order-settings.md#configure-order-settings) 注文に関連付けられた顧客データをインポートすることによって、顧客データベースを構築します。 このように展開された顧客リストを利用して、マーケティング可能な [!DNL Amazon Marketplace] エリアをリストおよび店頭に拡大 [!DNL Commerce] できます。
