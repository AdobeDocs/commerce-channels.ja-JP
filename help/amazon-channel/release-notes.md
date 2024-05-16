---
title: '''[!DNL Amazon Sales Channel] リリースノート'
description: すべてについて詳しくは、リリースノートを確認してください [!DNL Amazon Sales Channel] リリース。
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2010'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] リリースノート

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] Magento Open Source、Adobe Commerce、Adobe Commerceを備えたインスタンスに、クラウドインフラストラクチャバージョン 2.3.x および 2.4.x にインストールできます。この拡張機能は、Adobe Commerce 2.1、Magento 2.2、Magento Open Source 1 ではサポートされなくなりました。
> <br>サポート対象： [!DNL Amazon sales channel]  Adobe Commerce 2.3.x バージョンのみのバージョン 4.0.0 および 4.1.0。
> <br>[!DNL Amazon sales channel] バージョン 4.2.0 以降はAdobe Commerce 2.3.x バージョンと互換性がありますが、サポートはAdobe Commerce 2.4.x バージョンでのみ利用できます。
>

これらのリリースノートは、の初回リリースについて説明しています [!DNL Amazon sales channel] これには以下が含まれます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

参照： [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) （バージョン管理、サポート、互換性）。

参照： [製品の可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) この拡張機能をサポートしているAdobe Commerceのバージョンを確認するには、

## v4.5.0

*2023 年 8 月 30 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) MAGI から変更したAdobe.IO API ゲートウェイが追加され、認証セキュリティが向上しました。 `ServicesId` は、他と同様に、Adobe.IO 資格情報を管理する新しい UI を提供します [Adobe Commerce サービス](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>マーチャントは、次のことを確認する必要があります [秘密 API および公開 API キー](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) 実稼動用に更新されます。


![修正された問題](../assets/fix.svg) 設定の問題を特定し、注文作成フローを修正しました。

## v4.4.4

*2023 年 3 月 7 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正された問題](../assets/fix.svg) Adobe Commerce 2.4.6 および PHP 8.2 がサポートされるようになりました。

![修正された問題](../assets/fix.svg) ログのノイズを低減しました。

![修正された問題](../assets/fix.svg) 更新をプルする際の安定性が向上しました。

![修正された問題](../assets/fix.svg) 単一のアクションのようなプルの実行または CLI からの適用のプロセスを簡略化しました。

![修正された問題](../assets/fix.svg) の依存関係をアップグレードしました `magento/services-connector`.

![修正された問題](../assets/fix.svg) 国コードが無効な英国アカウントの同期の問題を修正しました。

![修正された問題](../assets/fix.svg) カタログMagentoエンティティの entity_type_id をハードコードすると、製品価格ソースで問題が発生します。

![修正された問題](../assets/fix.svg) バックエンドで別のインスタンスから削除されたアカウントが UI からも削除されない問題を修正しました。

![修正された問題](../assets/fix.svg) 一部の買い物かごルールで注文の読み込みが中断される問題を修正しました。

## v4.4.3

*2023 年 3 月 7 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正](../assets/fix.svg) Adobe Commerce 2.4.4 がサポートされるようになりました。

## v4.4.2

*2021 年 11 月 11 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正](../assets/fix.svg) 他の更新された拡張機能をサポートするように依存関係を更新しました。
![修正](../assets/fix.svg) PHP 8.1 のサポートを追加。

## v4.4.1

*2021 年 11 月 11 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正](../assets/fix.svg) Adobe Commerceがを受信する方法を変更しました _ユーザー名_ Amazonからのフィールド。 以前は、注文作成中に _ユーザー名_ フィールドに特殊文字が含まれています。 Adobe Commerceはを受信するようになりました。 _ユーザー名_ オーダーを正常に作成できるように、データを入力して特殊文字を除外します。

## v4.4.0

*2021 年 4 月 9 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) 設定に読み取り専用モードのサポートを追加しました。 参照： [販売チャネルの設定](sales-channel-settings.md).

![修正](../assets/fix.svg) データフローが変更されて、同じインスタンスの複数のコピーが更新を同時に取得できるようになりました。

![修正](../assets/fix.svg) アカウント情報を同期するための同期プロセスを変更しました。 リモートアカウントと同期する cron ジョブを追加し、同じ機能を CLI コマンドに追加しました。

![修正](../assets/fix.svg) より正確に制御するために、CLI コマンドの引数とフラグを追加しました。

![修正](../assets/fix.svg) システム設定のバックグラウンドタスク（cron）ソースを修正。

![修正](../assets/fix.svg) 国コードがプエルトリコ（PR）に設定されている場合に注文の作成が妨げられる問題を修正しました。

## v4.3.0

*2021 年 3 月 3 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正](../assets/fix.svg) <!--CHAN-xxxx-->この _注文の詳細_ 機能は再設計され、 _注文をインポート_ の設定値。 すべての注文の注文詳細がAmazon Sales Channelインターフェイスに表示されるようになりました。

![修正](../assets/fix.svg) が含まれる _[!UICONTROL Marketing]_管理者のメニュー、という名前が変更されました_[!UICONTROL Amazon]_ 対象： _[!UICONTROL Amazon Sales Channel]_.

![既知の問題](../assets/bug.svg) **重要**:Adobe Commerce 2.4.0 との互換性に関する既知の問題は、Adobe Commerce 2.4.1 リリースで解決されました。

- のAmazon cron プロセス `error` state
- データベースにストアを作成すると、Commerce 2.4.0 でのインストールが失敗する
- MSI のインストール時に製品の作成が失敗する

## v4.2.0

*2021 年 3 月 3 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

以前のバージョン [!DNL Amazon sales channel] インストールされているバージョン。Adobe Commerceをバージョン 2.4.0 に更新しようとすると、Adobe Commerceの更新を完了する前に、拡張機能を更新するよう求められます。

![既知の問題](../assets/bug.svg) 条件 [!DNL Amazon sales channel] 4.2.0 は、バージョン 2.4.0 および [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) を有効にすると、Commerce カタログに商品を追加できなくなる既知の問題が発生します。 この問題は、今後のCommerceのリリースで対処される予定です。

![新規](../assets/new.svg) [!DNL Amazon sales channel] は、テキストベースのアドレスデータを受け入れ、市区町村、都道府県、郵便番号などの標準化されたアドレス形式に一致させるように強化されました。 この更新により、住所エラーなしで注文データや配送データをAmazonと同期（同期）できます。<br/>例えば、買い物客が市区町村、都道府県、郵便番号をとして入力します `Escondido, californiA 92025-1501`. AmazonSales Channelは、次のようにデータを読み込んで標準フォーマットに一致させます。 `Escondido, CA 92025`を選択すると、標準化された形式でAmazonに同期し直されます。

![新規](../assets/new.svg) PHP 7.4 のサポートを追加。

![新規](../assets/new.svg) <!--CHAN-4334-->Adobe Commerce 2.4.x がサポートされるようになりました。以前のバージョンはCommerce 2.4.x と互換性がありますが、サポートされていません。 参照： [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) （バージョンの互換性のため）。 Adobe Commerce 2.4.0 のアップデートを完了するには、Amazon Sales Channelを 4.2.0 に更新する必要があります。

![修正](../assets/fix.svg) <!--CHAN-4431-->が発生する問題を修正しました _アクセス拒否_ 英国のお客様のエラー。

![修正](../assets/fix.svg) <!--CHAN-4394-->Amazonの出荷ステータスが対応するCommerce注文に同期されず、注文の出荷ステータスが次のように「ロック」されない問題を修正しました `Pending` Commerceのと `Unshipped` Amazonで。 新しい標準化された住所機能により、これらの配送状況エラーが解決されました。

![修正](../assets/fix.svg) <!--ticket#-->失敗した注文の読み込みを無視するように注文同期（同期）を更新しました。これにより、複数の同期試行が減り、後続の読み込みが処理され、注文同期要求が 5 分ごとに送信されるようになりました。 同期エラーはエラーログには記録されますが、さらにログを記録する機能を持たせるために「処理済み」とマークされます。 また、 [!DNL Amazon sales channel] Commerceで作成されなかった注文について収集された超過データを自動的に削除するようになりました。

![修正](../assets/fix.svg) 捕捉されていない例外および拡張機能の更新エラーに関する詳細を収集するように、エラーログを更新しました。

![修正](../assets/fix.svg) <!--ticket#-->の初期同期に起因する問題を修正しました _最低価格_ 欠落が原因で失敗するデータ _価格_ の値。

![修正](../assets/fix.svg) <!--CHAN-4410-->でフィルタリングエラーが発生する問題を修正しました _Amazonの注文_ 日付範囲フィールドが空白のままの場合に表示されます。

![修正](../assets/fix.svg) <!--CHAN-4439-->数量に関連する在庫およびフルフィルメント同期エラーが発生する問題を修正しました。 この拡張機能では、Amazonと同期する前に、小数として入力された数量値を切り捨てるようになりました。<br/> 例えば、マーチャントがの数量を手動で入力した場合などです `2.5`、拡張機能は値をに切り捨てます `2` 次に、更新された数量をAmazonと同期します。

## v4.1.0

*2020 年 5 月 7 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) <!--4247, 4230-->Commerceの注文要件に合わせて注文のインポートプロセスを変更しました。 これらの変更により、Commerceで読み込んだ注文に対応する注文を作成できない問題が修正されます。 参照： [注文の管理](managing-orders.md) オーダーブロッカーとソリューションについて説明します。

![新規](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->が更新されました _最近の注文_ ストアダッシュボードの「」セクションが追加され、新しい _すべての注文_ フィルターオプションや、より多くの注文を表示するためのページネーションを含む、すべてのAmazon注文を表示するビュー。 参照： [Amazon ストアダッシュボード](amazon-store-dashboard.md) および [Amazonの注文を表示](amazon-orders-all.md).

![新規](../assets/new.svg) さんがを追加しました _[!UICONTROL Order Notes]_再設計された列_[!UICONTROL Amazon Orders]_ 両方のテーブル _[!UICONTROL Recent Orders]_および_[!UICONTROL All Orders]_ ビュー。 _[!UICONTROL Order Notes]_注文の読み込みに問題があることをマーチャントに知らせます。 参照： [Amazonの注文を表示](amazon-orders-all.md).

![新規](../assets/new.svg) <!--CHAN-4013-->に合わせて製品条件パラメーターを更新しました [Amazonが更新されました](https://sell.amazon.com/programs/renewed) プログラム。 参照： [更新済み製品](renewed-products.md).

![新規](../assets/new.svg) <!--CHAN-3680-->更新日 [Amazon注文の詳細](amazon-order-details.md) Amazonで履行される注文に「汎用データ」を含める場合。 参照： [履行者](fulfilled-by.md).

![修正](../assets/fix.svg) <!--CHAN-4069-->ストアカードのアイコンがゆがむ問題を修正しました。

![修正](../assets/fix.svg) <!--CHAN-4165-->の妨げとなっているエラーを修正しました _ログイン_ セッションがタイムアウトした後に画面が表示されなくなります。

![修正](../assets/fix.svg) <!--CHAN-4211-->Amazonの注文の税額を新しいCommerceの注文に読み込めない問題を修正しました。

![修正](../assets/fix.svg) <!--CHAN-4234-->ストアダッシュボードに表示される収益合計に注文が含まれる問題を修正しました `Canceled` または `Error` ステータス。

![修正](../assets/fix.svg) <!--CHAN-4326-->を使用するサードパーティの拡張機能に関連する注文インポートエラーが発生する問題を修正しました。 _Magento Shipping_ オーダーを作成する方法。

![修正](../assets/fix.svg) <!--CHAN-4357-->Cron 同期の実行時にエラーが発生する問題を修正しました。 CLI コマンドにロックが追加され、2 つの cron ジョブが同時に同期できなくなりました。

![修正](../assets/fix.svg) Commerce バージョン 2.3.5 でのサポートを目的として、コンテンツセキュリティポリシーを更新しました。

## v4.0.0

*2020 年 3 月 25 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

>[!IMPORTANT]
>
>Amazon Sales Channel 4.0.0 は、Adobe Commerce 2.3.5 ではサポートされていません。Adobe Commerce 2.3.5 でのサポートについては、Amazon Sales Channel 4.1.0 にアップグレードしてください。

![新規](../assets/new.svg) 新しいが導入されました [AmazonSales Channel](amazon-sales-channel-home.md) ストア情報の「カード表示」が改善されたホームページ。

![新規](../assets/new.svg) 新しいが導入されました [ストアダッシュボード](amazon-store-dashboard.md) リスト、最近の注文、店舗設定情報が含まれます。

![新規](../assets/new.svg) よりシンプルで合理化された [オンボーディングプロセス](amazon-onboarding-home.md) および [デフォルトのストア設定](default-store-settings.md) を使用すると、ストアを迅速に統合できます。

![既知の問題](../assets/bug.svg) <!--CHAN-4102--> 条件 [属性の作成](managing-attributes.md) リストおよびリストから画像をインポートする場合 **ストアの表示** はに設定されています。 `All Store Views (Global)`には、画像をすべてのストアビューに読み込むことができない既知の問題があります。 の設定を変更した場合 **ビューの保存（値の読み込み先）** 特定のストアに対して、画像はそのストア用に読み込まれます。

## v3.0.1

*2019 年 11 月 11 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![修正](../assets/fix.svg) **数値フィールドの設定**: <!--CHAN-3779-->数値ベースの値を必要とするフィールドが、数値のみを受け入れるように更新されました。 例：「価格設定ルール設定」 > 「調整金額」フィールド

![修正](../assets/fix.svg) **ユーザーガイドのリンク**: <!--CHAN-3778-->不正確です _ユーザーガイド_ リンクが修正されました。

![修正](../assets/fix.svg) **Amazon Listings の複製**: <!--CHAN-3593-->以前に報告された、Amazonのリストが重複する問題を修正しました。 このリリース以前は、リストを読み込む際に、Amazon地域の国コードが SKU 値に追加されていました。 リストはカタログアイテムと一致しましたが、拡張機能により、追加の SKU を持つ新しい重複リストが作成されました。 このリリースでは、読み込まれたリストの SKU は拡張機能によって変更されず、既存のリストに対する変更はありません。 を使用できます [!UICONTROL End Listing(s)] （Amazonのオプション）をオンにして、重複したリストを削除します。

## v3.0.0

*2019 年 10 月 7 日（Pt）*

[!BADGE サポート]{type=Informative tooltip="サポート"}

![新規](../assets/new.svg) **Amazon UK Marketplace が利用可能になりました**:Commerce ストアの作成と統合に際して英国の Marketplace を選択できます。 この英国へのアップグレードには、以下のサポートが追加されています。

- [AmazonVAT 算定サービス](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} 情報。

![新規](../assets/new.svg) **ロギングの改善**: <!--CHAN-3642, 3672-->実装： **デバッグログを有効にする** トラブルシューティングが必要な場合に追加の同期データを収集する機能。 を参照してください。 [Sales Channel設定](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) トピックについては、設定リファレンスを参照してください。

![修正](../assets/fix.svg) **製品カタログ**: <!--CHAN-3687-->Amazon リストで読み込んだ画像が、対応するCommerce カタログ商品に適用されない問題を修正しました。

![修正](../assets/fix.svg) **オーダーの作成**: <!--CHAN-3708-->Commerce カタログ商品と一致しないCommerce注文に対してAmazonが注文を作成できない問題を修正しました。

![既知の問題](../assets/bug.svg) **Amazon Listings の複製**: <!--CHAN-3593-->この問題が原因で、カタログでは、読み込まれたリストの項目が、同じ SKU を使用して、最後に地域コードが追加されて作成されます。 次に、Amazonは、変更された SKU を新しい項目として処理し、リストを作成します。 この問題は、今後のリリースで対処される予定です。

## v2.0.0

[!BADGE サポート]{type=Informative tooltip="サポート"}

>[!NOTE]
>
>バージョン 1.0.0 は限定リリースでのみ入手可能でした。

![新規](../assets/new.svg)  **オンボーディングとメンテナンスの簡素化**：管理者を通じて入手可能な詳細な手順のプロセスを通じて、Amazonの販売者アカウントに追加して統合します。 1 つのダッシュボードで、ストア、アカウント、リストされた製品を管理します。

![新規](../assets/new.svg)  **複数アカウントのサポート**：管理者を通じて、複数のAmazon ブランドおよびマーケットプレイス地域を管理および監視します。

![新規](../assets/new.svg)  **インテリジェントな価格設定**：自動再価格設定ルールを設定して、誰でも欲しいBuy Boxのチャンスを増やします。 現在のBuy Box価格または競合他社の最低価格に合わせて動的に調整する価格を設定します。 マージンを保護するために、価格再設定の制限を設定します。

![新規](../assets/new.svg)  **リスト管理**：リストルールを使用して、製品のリストを自動化し、Commerce カタログをAmazon Marketplace に同期します。 特定の上書きを追加して、オファーを詳細に制御します。 管理者から直接、すべてのリストを監視および管理します。

![新規](../assets/new.svg)  **一貫したInventory management**:CommerceとAmazonの在庫数量を常に同期させます。

![新規](../assets/new.svg)  **オーダーとフルフィルメントの管理**：シームレスな通信と在庫更新を使用して、ダッシュボードを通じてAmazonの注文を追跡します。 Amazonで履行されたオーダー納入、履行された販売者または複数の方法の組合せを完了および追跡します。

![既知の問題](../assets/bug.svg)  製品数量の更新には、より長い待ち時間がかかる場合があります。 製品数量のアップデートは、同期に 2 時間ほどかかる場合があります。

![既知の問題](../assets/bug.svg)  インポートされた注文のタイプはです _Prime_ または _Premium_ オーダー。 これらの注文をAmazonの販売者アカウントで確認する必要があります。

![既知の問題](../assets/bug.svg)  不適格なバンドル製品は、Amazonでリストに適格と表示される場合があります。 バンドルされた製品内の製品の 1 つが対象でない可能性があります。 問題が発生した場合は、バンドルされた製品項目の実施要件ステータスを確認します。

![既知の問題](../assets/bug.svg)  Commerce 2.3.x でInventory managementを使用している場合、注文の作成時に部分的な在庫の再インデックスがトリガーされないことがあります。 販売可能数量は 1 時間ごとに再計算されるため、この更新期間中に売り越しが発生する可能性があります。
