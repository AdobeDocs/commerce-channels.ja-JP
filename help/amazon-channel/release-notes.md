---
title: '[!DNL Amazon Sales Channel] リリースノート'
description: すべてのリリースについて詳しくは、リリースノ  [!DNL Amazon Sales Channel]  トを参照してください。
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
> [!DNL Amazon sales channel] は、クラウドインフラストラクチャバージョン 2.3.x および 2.4.x 上の、Magento Open Source、Adobe Commerce、Adobe Commerceのインスタンスにインストールできます。この拡張機能は、Adobe Commerce 2.1、Magento 2.2、Magento Open Source 1 ではサポートされなくなりました。
> <br>Adobe Commerce 2.3.x バージョンでは、[!DNL Amazon sales channel] バージョン 4.0.0 および 4.1.0 でのみサポートされます。
> <br>[!DNL Amazon sales channel] バージョン 4.2.0 以降はAdobe Commerce 2.3.x バージョンと互換性がありますが、サポートはAdobe Commerce 2.4.x バージョンでのみ利用できます。
>

このリリースノートは、[!DNL Amazon sales channel] の初期リリースを説明するもので、次のものが含まれます。

![ 新機能 ](../assets/new.svg) 新機能
![ 修正された問題 ](../assets/fix.svg) 修正および改善
![ 既知の問題 ](../assets/bug.svg)

バージョン管理、サポート、互換性については、「[ 今後のリリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html)」を参照してください。

この拡張機能をサポートするAdobe Commerceのバージョンについては、[ 製品の可用性 ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) を参照してください。

## v4.5.0

*2023 年 8 月 30 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) MAGI から変更したAdobe.IO API ゲートウェイを追加し、認証セキュリティを向上しました。 `ServicesId` は、他の [Adobe Commerce サービス ](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) と同様に、Adobe.IO 資格情報を管理する新しい UI を提供します。

>[!NOTE]
>
>マーチャントは、[ プライベート API キーとパブリック API キー ](https://experienceleague.adobe.com/docs/commerce-admin/config/services/saas.html) が実稼動用に更新されていることを確認する必要があります。


![ 修正された問題 ](../assets/fix.svg) 設定の問題を特定し、注文作成フローを修正しました。

## v4.4.4

*2023 年 3 月 7 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正された問題 ](../assets/fix.svg)Adobe Commerce 2.4.6 および PHP 8.2 がサポートされるようになりました。

![ 修正された問題 ](../assets/fix.svg) ログのノイズが減少しました。

![ 修正された問題 ](../assets/fix.svg) 更新をプルする際の安定性が向上しました。

![ 問題を修正 ](../assets/fix.svg) 単一アクションのようなプルの実行または CLI からの適用のプロセスを簡略化しました。

![ 問題を修正しました ](../assets/fix.svg)`magento/services-connector` の依存関係をアップグレードしました。

![ 問題を修正 ](../assets/fix.svg) 国コードが無効な英国アカウントの同期の問題を修正しました。

![ 修正された問題 ](../assets/fix.svg) カタログMagentoエンティティの entity_type_id をハードコードすると、製品の価格Sourceで問題が発生します。

![ 修正された問題 ](../assets/fix.svg) バックエンドで別のインスタンスから削除されたアカウントが UI からも削除されない問題を修正しました。

![ 修正された問題 ](../assets/fix.svg) 一部の買い物かごルールで注文の読み込みが中断される問題を修正しました。

## v4.4.3

*2023 年 3 月 7 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正 ](../assets/fix.svg)Adobe Commerce 2.4.4 がサポートされるようになりました。

## v4.4.2

*2021 年 11 月 11 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正 ](../assets/fix.svg) 他の更新された拡張機能をサポートするために、依存関係を更新しました。
![ 修正 ](../assets/fix.svg)PHP 8.1 のサポートを追加しました。

## v4.4.1

*2021 年 11 月 11 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正 ](../assets/fix.svg) Adobe CommerceがAmazonから _ユーザー名_ フィールドを受け取る方法を変更しました。 以前は、「ユーザー名 _フィールドに特殊文字が含まれている場合_、注文の作成中にエラーが発生していました。 Adobe Commerceは _ユーザー名_ データを受け取り、特殊文字を除外することで、注文を正常に作成できるようになりました。

## v4.4.0

*2021 年 4 月 9 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) 設定に読み取り専用モードのサポートを追加しました。 [ 販売チャネル設定 ](sales-channel-settings.md) を参照してください。

![ 修正 ](../assets/fix.svg) 同じインスタンスの複数のコピーが同時に更新を取得できるように、データフローを変更しました。

![ 修正 ](../assets/fix.svg) アカウント情報を同期するための同期プロセスを変更しました。 リモートアカウントと同期する cron ジョブを追加し、同じ機能を CLI コマンドに追加しました。

![ 修正 ](../assets/fix.svg) より正確に制御するために、CLI コマンドの引数とフラグを追加しました。

![ 修正 ](../assets/fix.svg) システム設定のバックグラウンドタスク（cron）Sourceを修正。

![ 修正 ](../assets/fix.svg) 国コードがプエルトリコ（PR）に設定されている場合に、注文を作成できない問題を修正しました。

## v4.3.0

*2021 年 3 月 3 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正 ](../assets/fix.svg) <!--CHAN-xxxx-->_注文の詳細_ 機能は再設計され、_注文をインポート_ 設定には依存しなくなりました。 すべての注文の注文詳細がAmazon Sales Channelインターフェイスに表示されるようになりました。

![ 修正 ](../assets/fix.svg) 管理画面の _[!UICONTROL Marketing]_メニューで、名前が_[!UICONTROL Amazon]_ から _[!UICONTROL Amazon Sales Channel]_に変更されました。

![ 既知の問題 ](../assets/bug.svg)**重要**:Adobe Commerce 2.4.0 の互換性に関する既知の問題は、Adobe Commerce 2.4.1 リリースで解決されました。

- `error` 状態のAmazon cron プロセス
- データベースにストアを作成すると、Commerce 2.4.0 でのインストールが失敗する
- MSI のインストール時に製品の作成が失敗する

## v4.2.0

*2021 年 3 月 3 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

以前の [!DNL Amazon sales channel] バージョンがインストールされている場合に、Adobe Commerceをバージョン 2.4.0 に更新しようとすると、Adobe Commerceの更新を完了する前に拡張機能を更新するよう求められます。

![ 既知の問題 ](../assets/bug.svg) [!DNL Amazon sales channel] 4.2.0 がバージョン 2.4.0 と統合され、[Inventory management](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=en) が有効になっている場合、Commerce カタログに商品を追加できない既知の問題があります。 この問題は、今後のCommerceのリリースで対処される予定です。

![ 新規 ](../assets/new.svg) [!DNL Amazon sales channel] テキストベースのアドレスデータを受け入れ、市区町村、都道府県、郵便番号などの標準化されたアドレス形式に照合するように強化されました。 この更新により、住所エラーなしで注文データや配送データをAmazonと同期（同期）できます。<br/> 例えば、買い物客が市区町村、都道府県、郵便番号を `Escondido, californiA 92025-1501` のように入力します。 AmazonSales Channelでは、データを読み込んで標準フォーマットに `Escondido, CA 92025` して照合し、標準化されたフォーマットでAmazonに同期します。

![ 新規 ](../assets/new.svg) PHP 7.4 のサポートを追加しました。

![ 新規 ](../assets/new.svg) <!--CHAN-4334-->Adobe Commerce 2.4.x がサポートされるようになりました。以前のバージョンはCommerce 2.4.x と互換性がありますが、サポートされていません。 バージョンの互換性については、[ 今後のリリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) を参照してください。 Adobe Commerce 2.4.0 のアップデートを完了するには、Amazon Sales Channelを 4.2.0 に更新する必要があります。

![ 修正 ](../assets/fix.svg) <!--CHAN-4431--> 英国のお客様に _アクセスが拒否されました_ エラーが発生していた問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4394-->Amazonの配送ステータスが対応するCommerce注文に同期されず、CommerceとAmazonで `Pending` のように注文の配送ステータスが「ロック」されない問題を修正しまし `Unshipped`。 新しい標準化された住所機能により、これらの配送状況エラーが解決されました。

![ 修正 ](../assets/fix.svg)<!--ticket#--> 失敗した注文の読み込みを無視するように注文同期（同期）を更新しました。これにより、複数の同期試行が減り、後続の読み込みを処理できます。注文同期要求は 5 分ごとに送信されます。 同期エラーはエラーログには記録されますが、さらにログを記録する機能を持たせるために「処理済み」とマークされます。 また、Commerce[!DNL Amazon sales channel] 作成されなかった注文について収集された余分なデータを自動的に削除するようになりました。

![ 修正 ](../assets/fix.svg) 捕捉されていない例外および拡張機能の更新エラーに関する詳細を収集するために、エラーログを更新しました。

![ 修正 ](../assets/fix.svg) <!--ticket#-->_価格_ 値が見つからないために、_最低価格_ データの初期同期に失敗する問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4410--> 日付範囲フィールドが空白の場合に、_Amazon注文_ ビューでフィルタリングエラーが発生する問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4439--> 数量に関連する在庫およびフルフィルメント同期エラーが発生する問題を修正しました。 この拡張機能では、Amazonと同期する前に、小数として入力された数量値を切り捨てるようになりました。<br/> 例えば、マーチャントが `2.5` の数量を手動で入力すると、拡張機能は値を `2` に切り捨て、更新された数量をAmazonと同期します。

## v4.1.0

*2020 年 5 月 7 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) <!--4247, 4230-->Commerceの注文要件に合わせて注文インポートプロセスを変更しました。 これらの変更により、Commerceで読み込んだ注文に対応する注文を作成できない問題が修正されます。 注文ブロッカーとソリューションについて詳しくは、[ 注文の管理 ](managing-orders.md) を参照してください。

![ 新規 ](../assets/new.svg) <!--CHAN-CHAN-4167, 4297, 4311, 4312, 4324--> ストアダッシュボードの「_最近の注文_」セクションを更新し、より多くの注文を表示するためのフィルターオプションやページネーションなど、Amazonのすべての注文を表示する新しい _すべての注文_ ビューを追加しました。 [Amazon ストアダッシュボード ](amazon-store-dashboard.md) および [Amazon注文の表示 ](amazon-orders-all.md) を参照してください。

![ 新規 ](../assets/new.svg) 再設計された _[!UICONTROL Amazon Orders]_テーブルの_[!UICONTROL Order Notes]_ 列を _[!UICONTROL Recent Orders]_表示と_[!UICONTROL All Orders]_ 表示の両方に追加しました。 注文の読み込みに問題があることをマーチャントに知らせてくださ _[!UICONTROL Order Notes]_。 [Amazon注文の表示 ](amazon-orders-all.md) を参照してください。

![ 新規 ](../assets/new.svg)<!--CHAN-4013--> 更新された製品条件パラメーターは、[Amazonの更新済み ](https://sell.amazon.com/programs/renewed) プログラムに沿ったものになっています。 詳しくは、[ 更新済み製品 ](renewed-products.md) を参照してください。

Amazonによって履行された注文の「一般的なデータ」を含むように ![ 新規 ](../assets/new.svg) <!--CHAN-3680--> 更新された [Amazon注文の詳細 ](amazon-order-details.md)。 [ 履行期限 ](fulfilled-by.md) を参照してください。

![ 修正 ](../assets/fix.svg)<!--CHAN-4069--> ストアカードのアイコンが乱れる問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4165--> セッションがタイムアウトした後、_ログイン_ 画面が表示されないエラーを修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4211-->Amazonの注文の税額を新しいCommerceの注文に読み込めない問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4234--> ストアダッシュボードに表示される売上高の合計に `Canceled` または `Error` ステータスの注文が含まれる問題を修正しました。

![ 修正 ](../assets/fix.svg) <!--CHAN-4326-->_Magento Shipping_ 方式を使用して注文を作成するサードパーティの拡張機能に関連する注文インポートエラーの問題を修正しました。

![ 修正 ](../assets/fix.svg)<!--CHAN-4357-->cron 同期の実行時にエラーが発生する問題を修正しました。 CLI コマンドにロックが追加され、2 つの cron ジョブが同時に同期できなくなりました。

![ 修正 ](../assets/fix.svg) Commerce バージョン 2.3.5 でサポートするように、コンテンツセキュリティポリシーを更新しました。

## v4.0.0

*2020 年 3 月 25 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

>[!IMPORTANT]
>
>Amazon Sales Channel 4.0.0 は、Adobe Commerce 2.3.5 ではサポートされていません。Adobe Commerce 2.3.5 でのサポートについては、Amazon Sales Channel 4.1.0 にアップグレードしてください。

![ 新規 ](../assets/new.svg) 店舗情報の「カード表示」が改善された新しい ](amazon-sales-channel-home.md)2}Amazon Sales Channel} ホームページが導入されました。[

![ 新規 ](../assets/new.svg) リスト、最近の注文、店舗設定情報を含む新しい [ ストアダッシュボード ](amazon-store-dashboard.md) が導入されました。

![ 新規 ](../assets/new.svg) よりシンプルで合理化された [ オンボーディングプロセス ](amazon-onboarding-home.md) および [ デフォルトのストア設定 ](default-store-settings.md) が導入されて、ストアをより迅速に統合できるようになりました。

![ 既知の問題 ](../assets/bug.svg) <!--CHAN-4102--> リストから画像をインポートする [ 属性の作成 ](managing-attributes.md) および **ストアビュー** が `All Store Views (Global)` に設定されている場合、すべてのストアビューに画像をインポートできないという既知の問題があります。 **ストアビュー（値の読み込み先）** の設定を特定のストアに変更すると、画像はそのストアに読み込まれます。

## v3.0.1

*2019 年 11 月 11 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 修正 ](../assets/fix.svg) **数値フィールドの設定**:<!--CHAN-3779--> 数値ベースの値が必要なフィールドが、数値のみを受け入れるように更新されました。 例：「価格設定ルール設定」 > 「調整金額」フィールド

![ 修正 ](../assets/fix.svg)**ユーザーガイドのリンク**:<!--CHAN-3778--> 誤った _ユーザーガイド_ リンクが修正されました。

![ 修正 ](../assets/fix.svg) **重複するAmazonの一覧**: <!--CHAN-3593--> 以前に報告された、Amazonの一覧が重複する問題を修正しました。 このリリース以前は、リストを読み込む際に、Amazon地域の国コードが SKU 値に追加されていました。 リストはカタログアイテムと一致しましたが、拡張機能により、追加の SKU を持つ新しい重複リストが作成されました。 このリリースでは、読み込まれたリストの SKU は拡張機能によって変更されず、既存のリストに対する変更はありません。 「Amazonで [!UICONTROL End Listing(s)] 用」オプションを使用すると、重複したリストを削除できます。

## v3.0.0

*2019 年 10 月 7 日*

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

![ 新規 ](../assets/new.svg) **Amazon英国マーケットプレイスが利用可能になりました**:Commerceストアの作成および統合時に、英国のマーケットプレイスを選択できます。 この英国へのアップグレードには、以下のサポートが追加されています。

- [Amazon VAT 計算サービス ](https://sell.amazon.co.uk/learn/vat-resources){target="_blank"}

- [ 製品税コード ](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"} 情報。

![ 新規 ](../assets/new.svg) **ログの改善**: <!--CHAN-3642, 3672-->**デバッグログを有効にする** 機能を実装して、トラブルシューティングが必要な場合に追加の同期データを収集できるようになりました。 『構成リファレンス』の [Sales Channel](https://experienceleague.adobe.com/docs/commerce-admin/config/sales-channels.html) のトピックを参照してください。

![ 修正 ](../assets/fix.svg)**商品カタログ**:<!--CHAN-3687-->Commerce リストを使用して読み込んだ画像が、対応するAmazon カタログ商品に適用されない問題を修正しました。

![ 修正 ](../assets/fix.svg)**注文の作成**:<!--CHAN-3708-->Commerce カタログ商品と一致しないAmazon注文に対してCommerceが注文を作成できない問題を修正しました。

![ 既知の問題 ](../assets/bug.svg)**Amazonのリスティングが重複**:<!--CHAN-3593--> この問題が原因で、カタログでは、読み込まれたリストの項目が、同じ SKU を使用して、最後に地域コードが追加されて作成されます。 次に、Amazonは、変更された SKU を新しい項目として処理し、リストを作成します。 この問題は、今後のリリースで対処される予定です。

## v2.0.0

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}

>[!NOTE]
>
>バージョン 1.0.0 は限定リリースでのみ入手可能でした。

![ 新規 ](../assets/new.svg) **シンプルなオンボーディングとメンテナンス**：管理者を通じて提供される詳細な手順を含む段階的なプロセスを通じて、Amazonの販売者アカウントを追加し、統合します。 1 つのダッシュボードで、ストア、アカウント、リストされた製品を管理します。

![ 新規 ](../assets/new.svg)**複数アカウントのサポート**：管理を通じて、複数のAmazonのブランドやマーケットプレイスのリージョンを管理およびモニタリングします。

![ 新規 ](../assets/new.svg)**インテリジェントな価格設定**：自動再価格設定ルールを設定して、誰もが欲しがるBuy Boxのチャンスを増やします。 現在のBuy Box価格または競合他社の最低価格に合わせて動的に調整する価格を設定します。 マージンを保護するために、価格再設定の制限を設定します。

![ 新規 ](../assets/new.svg) リスト管理 ****：リストルールを使用して、商品のリストを自動化し、Commerce カタログをAmazon Marketplace に同期します。 特定の上書きを追加して、オファーを詳細に制御します。 管理者から直接、すべてのリストを監視および管理します。

![ 新規 ](../assets/new.svg)**一貫性のあるInventory management**:CommerceとAmazonの在庫数量を常に同期させます。

![ 新規 ](../assets/new.svg) 注文と受け渡しの管理 **：シ** ムレスなコミュニケーションと在庫更新により、ダッシュボードを通じてAmazonの注文を追跡します。 Amazonで履行されたオーダー納入、履行された販売者または複数の方法の組合せを完了および追跡します。

![ 既知の問題 ](../assets/bug.svg) 製品数量の更新に時間がかかる場合があります。 製品数量のアップデートは、同期に 2 時間ほどかかる場合があります。

![ 既知の問題 ](../assets/bug.svg) 読み込まれた注文には、タイプが _Prime_ または _Premium_ の場合があります。 これらの注文をAmazonの販売者アカウントで確認する必要があります。

![ 既知の問題 ](../assets/bug.svg) 不適格なバンドル製品は、Amazonにリストへの適格と表示される場合があります。 バンドルされた製品内の製品の 1 つが対象でない可能性があります。 問題が発生した場合は、バンドルされた製品項目の実施要件ステータスを確認します。

![ 既知の問題 ](../assets/bug.svg)Commerce 2.3.x 用のInventory managementを使用している場合、注文の作成時に部分的な在庫の再インデックスがトリガーされないことがあります。 販売可能数量は 1 時間ごとに再計算されるため、この更新期間中に売り越しが発生する可能性があります。
