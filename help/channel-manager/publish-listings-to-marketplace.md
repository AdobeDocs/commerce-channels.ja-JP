---
title: ウォルマートにリストを発行
description: コマース製品のリストを次に公開 [!DNL Walmart Marketplace]売り出しを始める
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: fffbdac54443b7b9bed8854eba8341446e78cc80
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 0%

---

# ウォルマートにリストを発行

他の市場と同じように [!DNL Walmart] では、サードパーティ販売者は、他のユーザーが販売した品目をリストできます。

プラットフォームは、UPC や GTIN などの製品識別子を使用して、既存の [!DNL Walmart Marketplace] リスト
一致する製品の場合、製品を公開する際に Commerce 製品オファーを含めるための更新が Walmart Marketplace に一覧表示されます。 [!DNL Channel Manager].

通常、最も価格が低い製品オファーは、 [!DNL Walmart Marketplace] リストに加え、レビューなどの他の要因も配置に影響を与えます。

## 製品を一致させる

製品が一致すると、チャネルマネージャーは製品データをに送信します。 [!DNL Walmart Marketplace] をクリックして、マッピングされた Commerce 製品属性に一致する属性値を持つ既存のリストを検索します。 一致条件は、 [attribute-mapping 設定](map-catalog-attributes.md) （ストアチャネル用）。

一致する製品が見つかった場合は、既存の製品リストが更新され、オファーが追加されます。

### 前提条件

製品を照合する前に、製品カタログ属性値がウォルマートの要件を満たしていることを確認し、製品属性設定を構成します。 詳しくは、 [カタログ属性をマッピング](map-catalog-attributes.md).

#### 製品の選択と照合

1. 接続されたセールスチャネルを開きます。

1. 送信者 **[!UICONTROL Listings]**、 *[!UICONTROL Draft]* ステータス。

   ![リストから製品を選択し、照合用に送信](assets/products-in-marketplace-sales-channel.png)

1. 選択 **[!UICONTROL Match Products]**.

   メッセージは、照合用に送信された製品の数を示します。

   ![接続されたセールスチャネルに製品を送信](assets/products-submitted-for-matching.png)

   選択した製品のステータスは、 [!UICONTROL *処理中*] 一致操作が完了するまで。 Walmart Marketplace がマッチング処理を完了するまでに最大 30 分かかる場合があります。

### 一致ステータスを確認

1. 選択 **製品を更新** 現在の製品ステータスを表示します。

1. 製品のステータスを確認します。

一致が完了すると、ステータスは次のようになります。 *一致* または *エラー*.

* **[!UICONTROL Match]** 製品が正常に一致したことを示します。 製品のオファーが既存の Walmart Marketplace リストに公開されました。 この [Marketplace ストアがアクティブではありません](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* が *[!UICONTROL Status detail]* 列。 ステージングされた製品は、 [!DNL Walmart Marketplace] ストアがアクティブ化されています。

* **[!UICONTROL Error]** は、次のいずれかの問題が原因で一致操作が失敗したことを示します。

   * [!DNL Channel Manager] 接続の問題が原因で、照合用に送信できませんでした。

   * 一致するものが見つかりませんでした。

   * 一致が見つかりましたが、次の理由でリストを公開できません： [!DNL Walmart Marketplace] はエラーコードを返しました。 詳しくは、 *ステータスの詳細** ：エラーの説明。

### ウォルマートのリストを確認

製品を照合した後、更新された製品リストをレビューし、製品の詳細、価格、在庫数量を [[!UICONTROL Walmart Marketplace Seller Account Items] dashboard](https://seller.walmart.com/items-and-inventory/manage-items) をクリックして、更新された製品を確認します。

### 製品一致エラーのトラブルシューティング

製品一致操作がエラーで失敗した場合、エラーメッセージは *[!UICONTROL Status detail]* 列 [!UICONTROL Channel Manager] 製品リスト。

返される一般的なエラーで、製品 ID 値の形式が正しくないか、必須の属性が見つかりません。

#### 製品 ID の値を修正

| タイプ | 説明 | 例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12：チェックデジットを含む 12 桁の数値。 </br></br>UPC の桁数が 12 桁未満の場合（UPC-E が 8 桁の場合など）は、要件を満たすために末尾のゼロを追加します。 | 変更前 `45678912345` から `045678912345` |
| GTIN | GTIN-14:14 桁の数値（チェックデジットを含む）。 </br></br>GTIN の桁数が 14 桁未満の場合は、先頭にゼロを追加します </br>要件を満たすために。 | 変更 `456789123456` から `0045678912345` |
| EAN | GTIN-13：チェックデジットを含む 13 桁の数値。 </br></br>EAN の桁数が 13 桁未満の場合は、先頭にを追加します </br>0 を指定して要件を満たします。 | 変更前 `4567891234` から `0004567891234` |

Walmart Marketplace のエラーコードについて詳しくは、 [Walmart Seller ヘルプ](https://sellerhelp.walmart.com/s/guide?article=000005844).

## 新しい製品リストをアップロード

Walmart Marketplace に一致しない製品の場合は、Walmart 製品カテゴリ Excel テンプレートを使用して製品リストを一括アップロードします。 Walmart テンプレートは、Commerce インスタンスから書き出された製品カタログデータを使用して入力します。

新しい製品リストについては、製品カタログをチェックし、Walmart Marketplace で販売する予定の製品が Walmart Marketplace 製品リストに必要な属性を持っていることを確認します。

**Walmart Marketplace のリスト — 属性の要件**

| **属性** | **要件レベル** |
|--------------------------|-----------------------|
| SKU | 必須 |
| 製品名 | 必須 |
| 製品 ID タイプ | 必須 |
| 製品 ID | 必須 |
| ブランド | 必須 |
| 短い説明 | 必須 |
| 販売価格 | 必須 |
| サイトの説明 | 必須 |
| メイン画像 URL | 必須 |
| 発送重量 | 必須 |
| 主な機能 | 推奨 |
| モデル番号 | 推奨 |
| 製造元名 | 推奨 |
| 製造元の部品番号 | 推奨 |
| サイズ | 推奨 |
| カラー | 推奨 |
| メイン画像 URL | オプション |
| 追加の画像 URL | オプション |
| 製造元 | オプション |

### 前提条件

* 次に示す [ウォルマートの要件](walmart-requirements.md).

* Commerce 製品カタログで、Walmart Marketplace にリストする製品のカタログ設定に必要な属性がすべて含まれ、Walmart Marketplace コンテンツガイドラインを満たしていることを確認します。

* 書き出し操作を完了するには、cron ジョブが実行中であることを確認します。

   * オンプレミスのインスタンスの場合は、 [cron の設定と実行](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   * Adobeクラウドインフラストラクチャについては、 [Cron ジョブの設定](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### アップロードする製品データファイルを作成します

1. お使いの [Walmart Seller アカウント](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)をクリックし、Walmart Seller Center から製品リストテンプレートをダウンロードします。

   * 「商品カタログ品目」ページで、「 **[!UICONTROL Add Items]**. 次に、 **[!UICONTROL Add items in bulk]**.

      ![Walmart Marketplace 項目設定の「Add items in bulk」オプション](assets/walmart-seller-account-add-items-bulk.png)

   * ダウンロードページで、「 」を選択します。 **[!UICONTROL Full Setup]**. 次に、項目カテゴリを選択し、カテゴリテンプレートをダウンロードします。

      ![Walmart Marketplace 項目設定の「カテゴリテンプレートをダウンロード」オプション](assets/walmart-seller-account-full-setup-download.png)

   * 製品リストに必要な属性と推奨属性がテンプレートに含まれていることを確認します。

1. 次の [!DNL Commerce] 管理者は、Adobe Commerceサイトから書き出す製品データを選択します。

   * 管理者から、 [!UICONTROL **システム** /データ転送 > **書き出し**].

   * の [!UICONTROL Export] ページの [!UICONTROL Entity Type] フィールド、選択 [!UICONTROL **製品**].

   * 内 [!UICONTROL Entity Attributes] 表で、製品データの書き出しの選択基準を設定します。
   ![での製品データページの書き出し [!UICONTROL Commerce Admin]](assets/walmart-seller-account-full-setup-download.png)

   フィルターを使用して、販売する製品カテゴリに適用する属性値を選択および設定します。 Walmart の必須属性と推奨属性を必ず含めてください ( [データを書き出し](https://docs.magento.com/user-guide/system/data-export.html) ( 詳しい手順については、『 Adobe Commerceユーザーガイド』を参照 )。

   書き出しの対象から属性を省略するには、 [!UICONTROL **除外**] 」チェックボックスを使用して、データを書き出すことができます。

1. 属性テーブルの最後までスクロールし、「 」を選択します。 [!UICONTROL **続行**] をクリックして、データのエクスポートを開始します。

   CSV 書き出しファイルは、cron ジョブを使用してメッセージキューで処理され、 `var/export/folder`. ( [メッセージキューの管理](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) 内 *コマース開発者ガイド*.)

1. Walmart Marketplace 製品カテゴリの Excel テンプレートを開き、Excel マクロ機能を使用して、エクスポートされた製品データを Excel テンプレートに結合します。

1. 書き出した製品データを含む Excel ファイルをアップロードします。

   * の製品カタログ項目ページに戻ります。 [ウォルマートセラーセンター](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   * 選択 [!UICONTROL **項目を追加** > **項目を一括で追加**].
   * 完成したスプレッドシートを「アップロード」セクションにドラッグします。
   * 選択 [!UICONTROL **送信**].
   * を選択します。[!UICONTROL  **アクティビティフィード**] をクリックして、進行状況を表示します。

詳しい手順については、 [完全なアイテム仕様を使用してアイテムを一括で追加](https://sellerhelp.walmart.com/s/guide?article=000007680) 内 [!DNL *Walmart Seller ヘルプ*].
