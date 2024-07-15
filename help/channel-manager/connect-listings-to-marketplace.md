---
title: Listings をウォルマートに接続
description: '販売を開始するには  [!DNL Commerce]  製品の一覧を接続  [!DNL Walmart Marketplace] てください。'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Listings をウォルマートに接続

他のマーケットプレイスと同様、[!DNL Walmart] を使用すると、サードパーティセラーは他のユーザーが販売する項目をリストできます。

- [!DNL Walmart Marketplace] では、UPC や GTIN などの製品識別子を使用して、製品を既存の [!DNL Walmart Marketplace] ータリストと照合します。

- 一致した製品の場合、Walmart Marketplace のリストが更新され、[!DNL Channel Manager] から製品を接続すると [!DNL Commerce] の製品オファーが含まれます。

- 通常、最も価格が低い製品オファーは [!DNL Walmart Marketplace] のリストの最初に表示されますが、レビューなどの他の要因もプレースメントに影響します。

## 製品に一致

製品を一致させると、チャネルマネージャーは製品データを [!DNL Walmart Marketplace] に送信し、マッピングされた製品 [!DNL Commerce] 属性に一致する属性値を持つ既存のリストを検索します。 一致条件は、ストアチャネルの [ 属性マッピング設定 ](map-catalog-attributes.md) によって決定されます。

一致する製品が見つかった場合は、既存の製品リストが更新され、オファーが追加されます。

### 前提条件

製品を照合する前に、製品カタログの属性値がウォルマートの要件を満たしていることを確認し、製品属性設定を構成します。 [ カタログ属性のマッピング ](map-catalog-attributes.md) を参照してください。

#### 製品の選択と一致

1. 連携した販売チャネルを開きます。

1. **[!UICONTROL Listings]** から、ステータスが「*[!UICONTROL Draft]*」の照合する製品を選択します。

   ![ リストから商品を選択し、マッチング用に送信 ](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. 「**[!UICONTROL Match Products]**」を選択します。

   メッセージは、照合のために送信された製品の数を示します。

   一致操作が完了するまで、選択した製品のステータスは [!UICONTROL *処理中*] に変わります。 Walmart Marketplace がマッチ操作を完了するまでに最大 30 分かかる場合があります。

### 一致ステータスを確認

一致が完了したら、**[!UICONTROL Refresh products]** を選択して、現在の製品ステータスを表示します。 *一致* または *エラー*。

- **[!UICONTROL Match]** は、商品が正常に一致したことを示します。 商品オファーは、既存のウォルマート マーケットプレイスのリストに接続されていました。 [Marketplace ストアがアクティブではない ](walmart-requirements.md#walmart-marketplace-store-status) 場合、*[!UICONTROL Staged for Match]* が *[!UICONTROL Status detail]* 列に表示されます。 ステージングされた製品は、[!DNL Walmart Marketplace] ストアがアクティブ化されると自動的に接続されます。

- **[!UICONTROL Error]** は、次のいずれかの問題が原因で一致操作が失敗したことを示します。

   - 接続の問題により、[!DNL Channel Manager] を照合に送信できませんでした。

   - 一致する項目が見つかりませんでした。

   - 一致が見つかりましたが、[!DNL Walmart Marketplace] がエラーコードを返したため、リストに接続できません。 この問題について詳しくは、**[!UICONTROL Error Description]** を参照してください。

### ウォルマートのリストを確認

製品を照合した後、更新された製品リストを確認し、製品の詳細、価格および在庫数量を [[!UICONTROL Walmart Marketplace Seller Account Items] ダッシュボードから確認して ](https://seller.walmart.com/items-and-inventory/manage-items) 更新された製品を確認します。

### 製品一致エラーのトラブルシューティング

製品の一致操作がエラーで失敗した場合は、エラーメッセージが [!UICONTROL Channel Manager] 製品リストの *[!UICONTROL Status detail]* 列に表示されます。

返される一般的なエラーが、形式が正しくない製品 ID 値であるか、必要な属性がありません。

#### 製品 ID 値を修正

| タイプ | 説明 | 例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12：チェックディジットを含む 12 桁の数値。 </br></br>8 桁の UPC-E など、UPC の桁数が 12 桁未満の場合は、要件を満たすために末尾にゼロを追加します。 | `45678912345` から `045678912345` への変更 |
| GTIN | GTIN-14：チェックディジットを含む 14 桁の数値。 </br></br>GTIN の桁数が 14 桁未満の場合は、要件を満たすために先頭に 0 を追加 </br> します。 | `456789123456` を `0045678912345` に変更 |
| EAN | GTIN-13：チェックディジットを含む 13 桁の数値。 </br></br>EAN の桁数が 13 桁未満の場合は、要件を満たすために先頭に </br> ゼロを追加します。 | `4567891234` から `0004567891234` への変更 |

Walmart Marketplace のエラーコードについて詳しくは、[Walmart Seller Help](https://sellerhelp.walmart.com/s/guide?article=000005844) を参照してください。

## 新しい製品リストのアップロード

Walmart Marketplace に一致しない製品の場合は、Walmart 製品カテゴリの Excel テンプレートを使用して、製品リストを一括アップロードします。 [!DNL Commerce] インスタンスから書き出した製品カタログデータを使用して、ウォルマートテンプレートに入力します。

新規商品リストについては、商品カタログを確認し、Walmart Marketplace で販売する予定の商品に、Walmart Marketplace の商品リストに必要な属性が含まれていることを確認してください。

**Walmart Marketplace listings-Attribute requirements**

| **属性** | **要件レベル** |
|--------------------------|-----------------------|
| SKU | 必須 |
| 製品名 | 必須 |
| 商品 ID タイプ | 必須 |
| 商品 ID | 必須 |
| ブランド | 必須 |
| 簡単な説明 | 必須 |
| 販売価格 | 必須 |
| サイトの説明 | 必須 |
| メイン画像の URL | 必須 |
| 送料の重量 | 必須 |
| 主な機能 | 推奨 |
| モデル番号 | 推奨 |
| 製造元名 | 推奨 |
| 製造元部品番号 | 推奨 |
| サイズ | 推奨 |
| カラー | 推奨 |
| メイン画像の URL | オプション |
| 追加の画像 URL | オプション |
| 製造元 | オプション |

### 前提条件

- [ ウォルマートの要件 ](walmart-requirements.md) を満たしていることを確認します。

- [!DNL Commerce] の製品カタログで、Walmart Marketplace にリストする製品のカタログ設定に必要な属性がすべて含まれており、Walmart Marketplace のコンテンツガイドラインを満たしていることを確認します。

- エクスポート操作を完了するために cron ジョブが実行中であることを確認します。

   - オンプレミスインスタンスの場合は、[cron の設定と実行 ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) を参照してください。

   - Adobeのクラウドインフラストラクチャについては、[cron ジョブの設定 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) を参照してください。

### アップロードする製品データファイルを作成します

1. [ ウォルマート販売者アカウント ](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller) から、ウォルマート販売者センターから製品リストテンプレートをダウンロードします。

   - 製品カタログ項目ページから、「**[!UICONTROL Add Items]**」を選択します。 次に、「**[!UICONTROL Add items in bulk]**」を選択します。

     ![Walmart Marketplace の項目設定の「一括で項目を追加」オプション ](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - ダウンロードページで、「**[!UICONTROL Full Setup]**」を選択します。 次に、項目カテゴリを選択し、カテゴリテンプレートをダウンロードします。

     ![ ウォルマート Marketplace の項目設定の「カテゴリテンプレートをダウンロード」オプション ](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - テンプレートに、製品リストへの登録に必要な属性と推奨される属性が含まれていることを確認します。

1. [!DNL Commerce] Admin で、Adobe[!DNL Commerce] サイトから書き出す商品データを選択します。

   - 管理者から、[!UICONTROL **システム**/データ転送/**書き出し**] を選択します。

   - [!UICONTROL Export] ページの「[!UICONTROL Entity Type]」フィールドで「[!UICONTROL **製品**]」を選択します。

   - [!UICONTROL Entity Attributes] のテーブルで、商品データの書き出しの選択条件を設定します。

     フィルターを使用して、自社で販売する製品カテゴリに適用する属性値を選択および設定します。 ウォルマートの必須属性と推奨属性を必ず含めてください。 （手順について詳しくは、『Adobe[!DNL Commerce] ーザーガイド』の [ データの書き出し ](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) を参照してください。）

     書き出しから属性を削除するには、行の先頭にある [!UICONTROL **除外**] チェックボックスを選択します。

1. 属性テーブルの最後までスクロールし、「[!UICONTROL **続行**]」を選択してデータの書き出しを開始します。

   CSV 書き出しファイルは、cron ジョブを使用してメッセージキューを介して処理され、`var/export/folder` に保存されます。 （[ 設定ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) の「*メッセージキューの管理* を参照。）

1. Walmart Marketplace 製品カテゴリの Excel テンプレートを開き、Excel マクロ機能を使用して、書き出された製品データを Excel テンプレートに結合します。

1. 書き出した製品データを含む Excel ファイルをアップロードします。

   - [ ウォルマート販売者センター ](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller) の商品カタログ商品ページに戻ります。

   - [!UICONTROL **項目を追加**/**項目を一括で追加**] を選択します。
   - 完成したスプレッドシートを「アップロード」セクションにドラッグします。
   - [!UICONTROL **送信**] を選択します。
   - [!UICONTROL  **アクティビティフィード**] を選択して、進行状況を表示します。

手順について詳しくは、[ ウォルマート販売者ヘルプ [!DNL *の ](https://sellerhelp.walmart.com/s/guide?article=000007680) 完全な項目仕様を使用した項目の一括追加*] を参照してください。
