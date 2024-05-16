---
title: の概要 [!DNL Amazon Sales Channel]“
description: “[!DNL Amazon Sales Channel] を使用すると、マーチャントはで製品をシームレスに販売できます [!DNL Amazon Marketplace].」と入力します。
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# の概要 [!DNL Amazon Sales Channel]

Adobe CommerceまたはMagento Open Sourceマーチャントは、を使用できます [!DNL Amazon Sales Channel] 店舗を世界最大のグローバルインターネットショッピング先と統合するための拡張機能。 この拡張機能は、次の接続によりAmazonのセールスを実現します [!DNL Commerce] （を使用） [!DNL Amazon Seller Central] アカウントとカタログと注文データの自動化と同期の両方を提供します。 Amazonのすべてのリストを完全に管理し、シンプルまたはインテリジェントな価格設定ルールを導入し、1 つのルールで注文と在庫を管理します [!DNL Commerce] ダッシュボード。

後 [オンボーディング](./amazon-onboarding-home.md), [!DNL Commerce] は、Amazon ストアのAmazonのリスト、注文、在庫、価格を管理および制御する「中央コマンドセンター」になります。 [ストアの統合](./store-integration.md) を接続 [!DNL Commerce] インスタンスとAmazon：両方のプラットフォーム間でデータを同期します。 Amazonのセールスチャネルでは、次のことが可能です。

- [Onboard](./amazon-onboarding-home.md) および 1 つ以上の統合 [!DNL Amazon Seller Central] Adobe CommerceまたはMagento Open Sourceのアカウント。

- 既存のAmazon リストを読み込んで同期し、内の商品と一致させる [!DNL Commerce] カタログ、一元化された製品カタログを作成します。

- の商品のAmazon リストの作成と管理 [!DNL Commerce] カタログ。

- 注文の表示と履行（出荷） [!DNL Commerce] Amazonとの間で、注文ステータス、支払い、払い戻しに関する情報を同期できます。

- の分析とエラーのログを表示 [競争力のある価格](./competitive-price-analysis.md), [リストの変更](./listing-changes-log.md)、および [コミュニケーションの問題](./communication-errors-log.md).

Amazon ストアにアクセスして、Amazon セールスチャネル上のこれらすべての機能、アカウント情報、リスト、注文などを表示および管理します [ホームページ](./amazon-sales-channel-home.md).

## プロモーションと価格設定

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- Amazon リストの価格を次の値に同期させる [!DNL Commerce] カタログ価格（または代替価格属性）。

- MSRP を有効にする [取り消し価格](./listing-price.md#configure-listing-price-settings) Amazonのリストに追加して、お客様への価値提案を高める。

- 有効化と管理 [最小広告価格（MAP）](./listing-price.md#configure-listing-price-settings) Amazonのリストで。

- 追加の設定 [付加価値税](./listing-price.md#configure-listing-price-settings) Amazonの価格で。

- で「利用可能数量」にカスタム値を設定 [在庫/数量の設定](./stock-quantity.md#configure-stock--quantity-settings) Amazonのリストに表示して、購入者の緊急度を高めます。

## 価格ルール

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 積み重ね可能、柔軟、複雑を実現 [価格ルール](./pricing-products.md) 日常のセールや季節ごとのプロモーションに対応するAmazonの価格を管理します。

- 作成 [floor](./floor-price.md) および [上限](./optional-ceiling-price.md) 最低価格と最高価格を保護するための価格。

- の作成と管理 [インテリジェントな価格の変更ルール](./intelligent-repricing-rules.md) Amazonの他の競合製品と比較して、製品の価格を自動的に調整する方法を説明します（[競合他社の最低値](./lowest-competitor-pricing.md) および [Buy Box](./buy-box-competitor-pricing.md) 価格）。

## カタログフィードの管理

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 既存のAmazon リスト（商品）を読み込んで、既存のものと一致させたり、 [!DNL Commerce] カタログ。

- を公開 [!DNL Commerce] Amazon リストを作成するためのAmazonへの製品です。

- 作成 [上書き](./creating-editing-overrides.md) 個々の価格、処理時間、条件および販売者のメモ メッセージを設定します。

- 製品の読み込みとマッピング [属性](./attributes-view.md) をAmazonのリストから選択して、内の製品と自動的に一致させる [!DNL Commerce] カタログ。

- 複数の検索パラメーターを設定して、Amazonのリストをの [!DNL Commerce] カタログ。

- 定義 [リストルール](./listing-rules.md) どちらを選択するかを決定するには [!DNL Commerce] 製品は、Amazonに掲載することが可能です。

- デフォルトを設定 [処理時間](./product-listing-actions.md) 新しいAmazonのリスト用。

- に基づいてリスト条件を一致 [!DNL Commerce] 属性。

- 条件タイプごとに販売者メモを追加します（オプション）。

- Amazonのリストをお客様に読み込む際に、数量のしきい値を実装する [!DNL Commerce] カタログ。

- 推奨を表示 [リストの改善](./listing-improvements.md).

## 注文管理とカスタマーサービス

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- Amazonおよびでの注文のサポートと処理 [!DNL Commerce].

- [インポート](./order-settings.md#configure-order-settings) Amazonからのご注文 [!DNL Commerce] または、Amazonに残します。

- を定義する [!DNL Commerce] 注文の読み込みと管理のためにAmazonの注文に関連付ける web サイトストア。

- 注文の表示、キャンセル、出荷元 [!DNL Commerce] やAmazon（状況に応じて） [フルフィルメント設定](./fulfilled-by.md).

- Amazonの注文ステータスの内でのカスタムステータスへのマッピング [!DNL Commerce] （オプション）。

- 注文エラーを表示および管理して、問題を解決し、顧客とつながります。

- への注文トラッキングデータの送信 [!DNL Amazon Seller Central] アカウント。

- [注文をキャンセル](./cancel-unshipped-order.md) 理由の応答を選択します。

- を表示する [最近の注文](./amazon-store-dashboard.md) Amazonの注文に関する情報。

## 報告書

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次の項目に関するレポート情報を確認できます。

- 有効、無効、適格および未完了のステータス別のリスト。

- 出荷待ちの注文。

- 最新の注文。

- Amazon [変更ログのリスト](./listing-changes-log.md) 製品/リストのフィード変更（価格や数量など）をレビューする場合。

- 製品 [Buy Box](./buy-box-competitor-pricing.md) 競合他社価格データ。

- 製品 [競合製品の最低価格](./lowest-competitor-pricing.md) データ。

## グローバル・セールスのサポート

（を使用） [!DNL Amazon Sales Channel] 拡張機能を使用すると、次のことができます。

- 複数のを管理 [!DNL Amazon Marketplace] 地域（国）

- を使用した多通貨のサポート [Commerce通貨設定ツール](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- 商品拠点およびAmazonフルフィルメントセンターからの配送を管理します。

## 顧客管理

を作成 [!DNL Commerce] 顧客データベース基準 [顧客データのインポート](./order-settings.md#configure-order-settings) Amazonの注文に関連付けます。 を通じて顧客のリストを拡大し、マーケティングの可能性を高めます。 [!DNL Amazon Marketplace] listings と [!DNL Commerce] ストアフロント。


使い始めるのは簡単です。 簡単なオンボーディングプロセスのガイドに従って、 [!DNL Amazon Seller Central] Amazonのセールスチャネルストアとの連携および [!DNL Commerce] Amazonのリスト、注文、在庫およびフルフィルメントを管理するためのカタログ。 中央のダッシュボードには、Amazonのセールスチャネルストアにおけるすべての統合とAmazonのリストに関するステータス更新が表示されます。 グローバルで新規顧客にリーチ [!DNL Amazon Marketplace] プロセスのシンプル化と自動化により、新しいシステムのセットアップにかかるコストと労力を最小限に抑えることができます。

統合した後 [!DNL Amazon Seller Central] アカウント、 [!DNL Amazon Sales Channel] 拡張機能を使用すると、アカウントを管理し、間でデータを同期できます [!DNL Commerce] とAmazon。 これにより、リストの作成、プロモーションの管理、価格の設定、在庫とフルフィルメントの管理を [!DNL Commerce] 管理者。 これらのオプションには、同じ商品のAmazonの価格をモニタリングし、より競争力のある価格になるように自動的に調整する価格ルールが含まれます。

