---
title: «の概要 [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] 商人が [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# の概要 [!DNL Amazon Sales Channel]

Adobe CommerceまたはMagento Open Sourceの商人は、 [!DNL Amazon Sales Channel] 店舗と世界最大のインターネットショッピング先を統合する拡張機能。 この拡張機能は、Amazonの販売を可能にする [!DNL Commerce] を [!DNL Amazon Seller Central] アカウントを作成し、カタログと注文データの自動化と同期の両方を提供します。 すべてのAmazonのリストを完全に管理し、シンプルまたはインテリジェントな価格ルールを実装し、1 つの [!DNL Commerce] ダッシュボード。

後 [オンボーディング](./amazon-onboarding-home.md), [!DNL Commerce] は、AmazonストアのAmazonリスト、注文、在庫、価格を管理および制御するための「中央コマンドセンター」になります。 [ストア統合](./store-integration.md) を [!DNL Commerce] インスタンスとAmazonを使用して、両方のプラットフォーム間でデータを同期します。 Amazon sales channel では、次のことができます。

- [オンボード](./amazon-onboarding-home.md) および [!DNL Amazon Seller Central] Adobe CommerceまたはMagento Open Sourceのアカウント

- 既存のAmazonリストを読み込んで同期し、 [!DNL Commerce] カタログ、一元化された製品カタログの作成

- お客様の [!DNL Commerce] カタログ。

- での（出荷）オーダーの表示および履行 [!DNL Commerce] とAmazon、注文ステータス、支払い、返金情報の同期。

- 次の分析およびエラーのログを表示 [競争価格](./competitive-price-analysis.md), [リストの変更](./listing-changes-log.md)、および [通信の問題](./communication-errors-log.md).

Amazonストアにアクセスして、Amazonセールスチャネルのこれらの機能、アカウント情報、リスト、注文件数などをすべて表示および管理します [ホームページ](./amazon-sales-channel-home.md).

## プロモーションと価格

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の操作を実行できます。

- Amazon上場価格の同期先 [!DNL Commerce] カタログ価格（または代替の価格属性）。

- MSRP を有効にする [ストライクスルー価格](./listing-price.md#configure-listing-price-settings) (Amazonリスト内 ) を参照して、顧客の価値提案を増やします。

- 有効化と管理 [最小広告価格 (MAP)](./listing-price.md#configure-listing-price-settings) (Amazonのリスト内 )

- 追加の設定 [VAT 税](./listing-price.md#configure-listing-price-settings) Amazonの価格。

- の「使用可能な数量」にカスタム値を設定します [在庫/数量設定](./stock-quantity.md#configure-stock--quantity-settings) をAmazonのリストに表示して、購入者の緊急度を高めます。

## 価格ルール

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の操作を実行できます。

- 積み重ね可能で柔軟性が高く、複雑な環境を構築 [価格ルール](./pricing-products.md) を使用して、毎日の販売や季節のプロモーションに関するAmazonの価格を管理できます。

- 作成 [floor](./floor-price.md) および [ceiling](./optional-ceiling-price.md) 最低価格と最高価格を保護するための価格。

- 作成と管理 [インテリジェントなリプライシングルール](./intelligent-repricing-rules.md) 他のAmazonの競合他社 ([最も低い競争相手](./lowest-competitor-pricing.md) および [Buy Box](./buy-box-competitor-pricing.md) 価格 )。

## カタログフィード管理

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の操作を実行できます。

- 既存のAmazonリスト（製品）を読み込み、 [!DNL Commerce] カタログ。

- の公開 [!DNL Commerce] Amazonリストを作成するためのAmazonへの製品。

- 作成 [上書き](./creating-editing-overrides.md) 個々の価格を設定し、時間、条件、販売者の注記メッセージを処理します。

- 製品の読み込みとマッピング [属性](./attributes-view.md) Amazonのリストから、 [!DNL Commerce] カタログ。

- Amazonの一覧を [!DNL Commerce] カタログ。

- 定義 [リストルール](./listing-rules.md) どちらを選ぶか [!DNL Commerce] 製品はAmazonにリストされる資格があります。

- デフォルトを設定 [処理時間](./product-listing-actions.md) 新しいAmazonの一覧

- 次に基づく一致リスト条件： [!DNL Commerce] 属性。

- 各条件タイプに販売者向けメモを追加します（オプション）。

- 数量しきい値の実装は、Amazonリストを [!DNL Commerce] カタログ。

- 推奨を表示 [リストの改善点](./listing-improvements.md).

## 注文管理とカスタマーサービス

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の操作を実行できます。

- Amazonおよびでのサポートと処理のオーダー [!DNL Commerce].

- [インポート](./order-settings.md#configure-order-settings) Amazonの注文 [!DNL Commerce] Amazonに残す

- 次のいずれかを定義します。 [!DNL Commerce] Amazonの注文と関連付ける web サイトストア。注文のインポートと管理に使用します。

- 注文の表示、キャンセル、出荷元 [!DNL Commerce] および/またはAmazonに応じて、 [達成設定](./fulfilled-by.md).

- Amazonの注文ステータスを、 [!DNL Commerce] （オプション）。

- 注文エラーを表示および管理して、問題を解決し、顧客と連携します。

- に注文トラッキングデータを送信 [!DNL Amazon Seller Central] アカウント

- [注文をキャンセル](./cancel-unshipped-order.md) をクリックし、理由の応答を選択します。

- 次を表示： [最近の注文](./amazon-store-dashboard.md) Amazonの注文に関する情報。

## レポート

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の項目に関するレポート情報を確認できます。

- アクティブ、非アクティブ、適格および不完全なステータス別のリスト。

- 注文は出荷待ちです。

- 最新の注文。

- Amazon [変更ログの一覧表示](./listing-changes-log.md) をクリックして、製品/リストへのフィードの変更（価格や数量など）を確認します。

- 製品 [Buy Box](./buy-box-competitor-pricing.md) 競合相手の価格データ。

- 製品 [競合他社の最低価格](./lowest-competitor-pricing.md) データ。

## グローバルセールスのサポート

を使用 [!DNL Amazon Sales Channel] 拡張機能では、次の操作を実行できます。

- 複数管理 [!DNL Amazon Marketplace] 地域（国）。

- を使用して複数の通貨をサポート [コマース通貨設定ツール](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- 製品の保管場所やAmazonフルフィルメントセンターからの出荷を管理します。

## 顧客管理

のビルド [!DNL Commerce] 顧客データベース別 [顧客データのインポート](./order-settings.md#configure-order-settings) Amazonの注文に関連付けられている。 お客様の [!DNL Amazon Marketplace] リストと [!DNL Commerce] ストアフロント。


はじめには簡単です。 短いオンボーディングプロセスが、 [!DNL Amazon Seller Central] Amazonセールスチャネルストアとのアカウントと統合 [!DNL Commerce] Amazonの一覧、注文、在庫、および達成を管理するカタログ。 中央のダッシュボードには、すべてのAmazonセールスチャネルストア統合とAmazonリストのステータス更新が表示されます。 グローバルで新しいお客様にリーチ [!DNL Amazon Marketplace] シンプルで自動化されたプロセスにより、新しいシステムの設定にかかるコストと労力をほとんど、あるいはまったく負担しなくて済みます。

統合後 [!DNL Amazon Seller Central] アカウント、 [!DNL Amazon Sales Channel] 拡張機能を使用すると、アカウントを管理し、 [!DNL Commerce] Amazon これにより、リストの作成、プロモーションの管理、価格の設定、在庫と達成の管理を [!DNL Commerce] 管理者。 これらのオプションには、同じ品目のAmazonの価格を監視し、価格を自動的に調整して競争力を高める価格設定ルールが含まれます。

