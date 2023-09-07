---
title: '''[!DNL Amazon Sales Channel] リリースノート'
description: すべての [!DNL Amazon Sales Channel] リリース。
feature: Sales Channels, Release Notes
exl-id: 792782e0-9097-42f7-9fc0-509ece02e407
source-git-commit: df8bbec23d34b53a0e694c924aca5b1ed41e4d08
workflow-type: tm+mt
source-wordcount: '2024'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] リリースノート

>[!IMPORTANT]
>
> [!DNL Amazon sales channel] Magento Open Source、Adobe Commerce、Adobe Commerceの各クラウドインフラストラクチャバージョン 2.3.x および 2.4.x を使用するインスタンスにインストールできます。拡張機能は、Adobe Commerce 2.1、Magento Open Source2.2、またはMagento1 ではサポートされなくなりました。
> <br>次の場合にサポートを利用できます： [!DNL Amazon sales channel]  バージョン 4.0.0 および 4.1.0(Adobe Commerce 2.3.x バージョンのみ )。
> <br>[!DNL Amazon sales channel] バージョン 4.2.0 以降はAdobe Commerce 2.3.x バージョンと互換性がありますが、サポートはAdobe Commerce 2.4.x バージョンでのみ利用できます。
>

以下のリリースノートでは、 [!DNL Amazon sales channel] およびを含めます。

![新規](../assets/new.svg) 新機能
![修正された問題](../assets/fix.svg) 修正点および改善点
![既知の問題](../assets/bug.svg) 既知の問題

詳しくは、 [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) バージョン管理、サポートおよび互換性については、を参照してください。

詳しくは、 [製品の可用性](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) を参照して、この拡張機能をサポートしているAdobe Commerceバージョンを確認してください。

## v4.5.0

*2023 年 8 月 31 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) 認証のセキュリティを強化するために、Adobe.IO API ゲートウェイが MAGI から変更されるようになりました。 `ServicesId` は、他の UI と同様に、Adobe.IO 資格情報を管理する新しい UI を提供します。 [Adobe Commerce Services](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html).

>[!NOTE]
>
>商人は [非公開および公開 API キー](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) が実稼動用に更新されました。


![修正された問題](../assets/fix.svg) 設定の問題を特定し、注文作成フローを修正しました。

## v4.4.4

*2023 年 3 月 8 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正された問題](../assets/fix.svg) Adobe Commerce 2.4.6 および PHP 8.2 のサポートを追加しました。

![修正された問題](../assets/fix.svg) ログのノイズを低減。

![修正された問題](../assets/fix.svg) 更新を取り込む際の安定性が向上しました。

![修正された問題](../assets/fix.svg) 単一のアクションのプルまたは CLI からの適用を実行するプロセスを簡素化。

![修正された問題](../assets/fix.svg) 依存関係をアップグレードしました： `magento/services-connector`.

![修正された問題](../assets/fix.svg) 無効な国コードを含む英国のアカウントの同期の問題を修正しました。

![修正された問題](../assets/fix.svg) カタログ商品エンティティの entity_type_id をハードコードすると、Magento価格ソースに問題が発生します。

![修正された問題](../assets/fix.svg) 別のインスタンスからバックエンドで削除されたアカウントが UI からも削除されない問題を修正しました。

![修正された問題](../assets/fix.svg) 一部の買い物かごルールで注文のインポートが壊れていた問題を修正しました。

## v4.4.3

*2023 年 3 月 8 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正点](../assets/fix.svg) Adobe Commerce 2.4.4 のサポートを追加しました。

## v4.4.2

*2021 年 11 月 12 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正点](../assets/fix.svg) 依存関係を更新して、他の更新された拡張機能をサポートしました。
![修正点](../assets/fix.svg) PHP 8.1 のサポートを追加しました。

## v4.4.1

*2021 年 11 月 12 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正点](../assets/fix.svg) Adobe Commerceが _ユーザー名_ Amazonのフィールド。 以前は、 _ユーザー名_ フィールドに特殊文字が含まれていました。 Adobe Commerceが _ユーザー名_ 順序を正しく作成できるよう、データとフィルターで特殊文字を除外します。

## v4.4.0

*2021 年 4 月 10 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) 設定に読み取り専用モードのサポートを追加しました。 詳しくは、 [セールスチャネル設定](sales-channel-settings.md).

![修正点](../assets/fix.svg) 同じインスタンスの複数のコピーで更新を同時に取得できるようにデータフローを変更しました。

![修正点](../assets/fix.svg) アカウント情報を同期するための同期プロセスを変更しました。 リモートアカウントと同期する cron ジョブを追加し、CLI コマンドに同じ機能を追加しました。

![修正点](../assets/fix.svg) より正確に制御するために、CLI コマンドの引数とフラグを追加しました。

![修正点](../assets/fix.svg) システム設定のバックグラウンドタスク (cron) ソースを修正しました。

![修正点](../assets/fix.svg) 国コードがプエルトリコ (PR) に設定された場合に注文を作成できなかった問題を修正しました。

## v4.3.0

*2021 年 3 月 4 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正点](../assets/fix.svg) <!--CHAN-xxxx-->The _注文の詳細_ 機能は再設計され、現在はに依存していません _注文のインポート_ 設定。 注文の詳細が、すべての注文に対してAmazonSales Channelインターフェイスに表示されるようになりました。

![修正点](../assets/fix.svg) Adobe Analytics の _[!UICONTROL Marketing]_メニューの「 」が、_[!UICONTROL Amazon]_ から _[!UICONTROL Amazon Sales Channel]_.

![既知の問題](../assets/bug.svg) **重要**:Adobe Commerce 2.4.0 の互換性に関する既知の問題は、Adobe Commerce 2.4.1 リリースで解決されました。

- でのAmazon cron プロセス `error` state
- データベースにストアを作成する際に、Commerce 2.4.0 を使用したインストールが失敗する
- MSI がインストールされていると、製品の作成に失敗します

## v4.2.0

*2021 年 3 月 4 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

以前の [!DNL Amazon sales channel] バージョンがインストールされ、Adobe Commerceのバージョン 2.4.0 への更新を試みると、Adobe Commerceのアップデートを完了する前に、拡張機能を更新するよう求められます。

![既知の問題](../assets/bug.svg) 条件 [!DNL Amazon sales channel] 4.2.0 は、バージョン 2.4.0 およびと統合されています。 [Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) が有効になっている場合、コマースカタログに商品を追加できない既知の問題があります。 この問題は、今後の Commerce リリースで対処される予定です。

![新規](../assets/new.svg) [!DNL Amazon sales channel] は、テキストベースのアドレスデータを受け取り、市区町村、都道府県、郵便番号などの標準化されたアドレス形式に一致させるように強化されました。 この更新により、注文および配送先のデータを、住所のエラーなしにAmazonと同期（同期）できます。<br/>例えば、買い物客が市区町村、都道府県、郵便番号を `Escondido, californiA 92025-1501`. AmazonSales Channelは、データを読み込み、標準形式にマッチングします。 `Escondido, CA 92025`を呼び出し、この標準化された形式でAmazonに同期します。

![新規](../assets/new.svg) PHP 7.4 のサポートを追加しました。

![新規](../assets/new.svg) <!--CHAN-4334-->Adobe Commerce 2.4.x のサポートを追加しました。以前のバージョンは Commerce 2.4.x と互換性がある場合がありますが、サポートされていません。 詳しくは、 [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) バージョンの互換性のため。 AmazonSales Channelは、Adobe Commerce 2.4.0 の更新を完了する前に、4.2.0 に更新する必要があります。

![修正点](../assets/fix.svg) <!--CHAN-4431-->次の問題を修正しました： _アクセス拒否_ エラーが発生しました。

![修正点](../assets/fix.svg) <!--CHAN-4394-->Amazonの配送ステータスが対応するコマースの注文と同期されなかった問題を修正し、注文の配送ステータスが「ロック」されていた問題を `Pending` ( コマースおよび `Unshipped` Amazonで 新しく標準化された住所機能により、これらの発送ステータスのエラーが解決されました。

![修正点](../assets/fix.svg) <!--ticket#-->注文の同期（同期）を更新し、失敗した注文のインポートを無視するようにしました。したがって、同期の試行が複数回減り、以降のインポートが処理されるようになりました。注文の同期要求は 5 分ごとに送信されます。 同期エラーは引き続きエラーログに記録されますが、「処理済み」とマークされ、さらにログ機能を使用できるようになります。 また、 [!DNL Amazon sales channel] コマースで作成に失敗した注文に対して収集された超過データを自動的に削除するようになりました。

![修正点](../assets/fix.svg) エラーログを更新し、キャッチされない例外および拡張機能の更新エラーに関する詳細情報を収集しました。

![修正点](../assets/fix.svg) <!--ticket#-->の初期同期で発生していた問題を修正しました。 _最低価格_ 欠落により失敗するデータ _価格_ の値です。

![修正点](../assets/fix.svg) <!--CHAN-4410-->フィルターエラーが発生した問題を修正しました。 _Amazon注文_ 日付範囲フィールドが空白のままの場合に表示します。

![修正点](../assets/fix.svg) <!--CHAN-4439-->数量関連の在庫および達成の同期エラーが発生していた問題を修正しました。 拡張機能では、Amazonとの同期の前に、10 進数として入力された数量値を切り捨てるようになりました。<br/> 例えば、商人が数量を手動で入力する場合、 `2.5`の場合、拡張機能は値をに切り捨てます。 `2` その後、更新された数量をAmazonと同期します。

## v4.1.0

*2020 年 5 月 8 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) <!--4247, 4230-->コマースの注文要件に合わせて注文の読み込みプロセスを変更しました。 これらの変更により、Commerce でインポートした注文に対応する注文を作成できない問題が修正されました。 詳しくは、 [注文の管理](managing-orders.md) を参照してください。

![新規](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324-->更新された _最近の注文_ 」セクションに追加され、 _すべての注文_ フィルターオプションや、より多くの注文を表示するためのページネーションを含む、Amazonのすべての注文を表示するビュー。 詳しくは、 [Amazon Store ダッシュボード](amazon-store-dashboard.md) および [Amazon注文の表示](amazon-orders-all.md).

![新規](../assets/new.svg) 追加された _[!UICONTROL Order Notes]_再設計された列_[!UICONTROL Amazon Orders]_ 両方のテーブル _[!UICONTROL Recent Orders]_および_[!UICONTROL All Orders]_ ビュー。 _[!UICONTROL Order Notes]_商人に注文の輸入に問題があることを知らせます。 詳しくは、 [Amazon注文の表示](amazon-orders-all.md).

![新規](../assets/new.svg) <!--CHAN-4013-->製品条件パラメーターを更新し、 [Amazon更新](https://sell.amazon.com/programs/renewed) プログラム。 詳しくは、 [更新された製品](renewed-products.md).

![新規](../assets/new.svg) <!--CHAN-3680-->更新済み [Amazon注文の詳細](amazon-order-details.md) を追加しました。これは、Amazonが満たす注文に対して「汎用データ」を含めます。 詳しくは、 [実行者](fulfilled-by.md).

![修正点](../assets/fix.svg) <!--CHAN-4069-->ストアカードのアイコンにゆがみが生じる問題を修正しました。

![修正点](../assets/fix.svg) <!--CHAN-4165-->エラーが修正され、 _ログイン_ セッションがタイムアウトした後に画面が表示されないようにします。

![修正点](../assets/fix.svg) <!--CHAN-4211-->Amazonの注文税額が新しいコマース注文にインポートできなかった問題を修正しました。

![修正点](../assets/fix.svg) <!--CHAN-4234-->店舗ダッシュボードに表示される売上高合計に、 `Canceled` または `Error` ステータス。

![修正点](../assets/fix.svg) <!--CHAN-4326-->を使用するサードパーティの拡張機能に関連する注文のインポートエラーが発生する問題を修正しました。 _Magento Shipping_ オーダーを作成するメソッド。

![修正点](../assets/fix.svg) <!--CHAN-4357-->cron 同期の実行時にエラーが発生する問題を修正しました。 CLI コマンドにロックが追加され、2 つの cron ジョブが同時に同期されなくなりました。

![修正点](../assets/fix.svg) コマースバージョン 2.3.5 でのサポートに対してコンテンツセキュリティポリシーを更新しました。

## v4.0.0

*2020 年 3 月 26 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

>[!IMPORTANT]
>
>AmazonSales Channel4.0.0 は、Adobe Commerce 2.3.5 ではサポートされていません。Adobe Commerce 2.3.5 のサポートについては、AmazonSales Channel4.1.0 にアップグレードしてください。

![新規](../assets/new.svg) 新しい [AmazonSales Channel](amazon-sales-channel-home.md) ストア情報の「カード表示」が改善されたホームページ。

![新規](../assets/new.svg) 新しい [ストアダッシュボード](amazon-store-dashboard.md) リスト、最近の注文、およびストア設定情報を含む。

![新規](../assets/new.svg) シンプルで合理化された [オンボーディングプロセス](amazon-onboarding-home.md) および [デフォルトのストア設定](default-store-settings.md) ストアをより迅速に統合するため。

![既知の問題](../assets/bug.svg) <!--CHAN-4102--> 条件 [属性の作成](managing-attributes.md) 画像をインポートする場合は、および **ストアビュー数** が `All Store Views (Global)`既知の問題により、画像をすべてのストア表示に読み込めませんでした。 次の設定を変更した場合： **ビューを保存（値の読み込み先）** 特定のストアに対して、画像はそのストアに対して読み込まれます。

## v3.0.1

*2019 年 11 月 12 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![修正点](../assets/fix.svg) **数値フィールド設定**: <!--CHAN-3779-->数値ベースの値を必要とするフィールドが更新され、数値文字のみを受け入れるようになりました。 例： 「価格設定ルール設定」 > 「調整金額」フィールド

![修正点](../assets/fix.svg) **ユーザーガイドリンク**: <!--CHAN-3778-->誤った _ユーザーガイド_ リンクが修正されました。

![修正点](../assets/fix.svg) **重複するAmazon一覧**: <!--CHAN-3593-->以前に報告された問題で、Amazonのリストが重複する原因となっていた問題が修正されました。 このリリース以前は、リストのインポート時に、拡張機能によってAmazon地域の国コードが SKU 値に追加されていました。 リストがカタログ項目と一致したが、拡張機能によって、追加された SKU を含む新しい重複リストが作成されました。 このリリースでは、拡張機能で読み込んだリストの SKU が変更されることはなく、既存のリストは変更されません。 以下を使用すると、 [!UICONTROL End Listing(s)] 重複するリストを削除するAmazonオプション。

## v3.0.0

*2019 年 10 月 8 日*

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

![新規](../assets/new.svg) **Amazon UK Marketplace が利用可能**：ユーザーは、コマースストアを作成および統合する際に、英国マーケットプレイスを選択できます。 この英国のアップグレードには、次の追加サポートが含まれます。

- [AmazonVAT 計算サービス](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [製品税コード](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} 情報。

![新規](../assets/new.svg) **ログ機能の向上**: <!--CHAN-3642, 3672-->を実装する **デバッグログを有効にする** トラブルシューティングが必要な場合に追加の同期データを収集する機能。 詳しくは、 [Sales Channel設定](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) 」のトピックを参照してください。

![修正点](../assets/fix.svg) **商品カタログ**: <!--CHAN-3687-->Amazonのリストで読み込まれた画像が、対応するコマースカタログ製品に適用されなかった問題を修正しました。

![修正点](../assets/fix.svg) **注文の作成**: <!--CHAN-3708-->コマースカタログ製品と一致しないAmazonの注文を作成できなかった問題を修正しました。

![既知の問題](../assets/bug.svg) **重複するAmazon一覧**: <!--CHAN-3593-->この問題により、カタログは読み込まれたリストに対して、同じ SKU を使用し、しかし、最後に地域コードが追加された品目を作成します。 次に、Amazonが変更された SKU を新しい項目として処理し、リストを作成します。 この問題は、今後のリリースで対処する予定です。

## v2.0.0

[!BADGE サポート対象]{type=Informative tooltip="サポート対象"}

>[!NOTE]
>
>バージョン 1.0.0 は、限定的なリリースでのみ使用可能でした。

![新規](../assets/new.svg)  **シンプルなオンボーディングとメンテナンス**：手順を追ったプロセスと管理者から利用できる詳細な手順を通じて、Amazonセラーアカウントに追加して統合します。 1 つのダッシュボードを使用して、店舗、アカウント、および一覧表示された製品を保守します。

![新規](../assets/new.svg)  **複数のアカウントのサポート**：管理ツールを使用して、複数のAmazonブランドおよび Marketplace 地域を管理および監視します。

![新規](../assets/new.svg)  **インテリジェントな価格**：自動価格変更ルールを設定して、コベート対象のBuy Boxの機会を増やします。 価格を設定して、現在のBuy Box価格、または競合相手の最低価格に動的に調整します。 利益を保護するために、価格を変更する制限を設定します。

![新規](../assets/new.svg)  **リスト管理**：製品リストを自動化し、リストルールを使用してコマースカタログをAmazon Marketplace に同期します。 特定の上書きを追加して、オファーを細かく制御します。 管理者から直接、すべてのリストを監視および管理します。

![新規](../assets/new.svg)  **一貫したInventory management**：コマースとAmazonの在庫数を一定に同期させます。

![新規](../assets/new.svg)  **受注および履行管理**：シームレスなコミュニケーションと在庫の更新を使用して、Amazonの注文をダッシュボードで追跡します。 Amazon、商人が満たした注文出荷、または複数の方法の組み合わせに従って、完了し、追跡します。

![既知の問題](../assets/bug.svg)  製品の数量を更新するのに、待ち時間が長くなる場合があります。 製品数量の更新を同期するには、約 2 時間かかる場合があります。

![既知の問題](../assets/bug.svg)  インポートされた注文のタイプは _Prime_ または _Premium_ 注文。 これらの注文は、Amazonセラーアカウントで確認する必要があります。

![既知の問題](../assets/bug.svg)  不適格なバンドル製品は、Amazonでのリストへの登録に適格と表示される場合があります。 バンドルされた製品内の製品の 1 つが適格でない可能性があります。 問題が発生した場合は、バンドルされた製品項目の適格性ステータスを確認してください。

![既知の問題](../assets/bug.svg)  Inventory management for Commerce 2.3.x を使用している場合、注文の作成時に、部分的な在庫再インデックスがトリガーしないことがあります。 売り上げ可能な数量は 1 時間ごとに再計算され、この更新間隔中にオーバーセルが発生する可能性があります。
