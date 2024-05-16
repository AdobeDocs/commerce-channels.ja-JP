---
title: Listings をウォルマートに接続
description: '''次の一覧を接続 [!DNL Commerce] 製品から [!DNL Walmart Marketplace]売り出し始めます。'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Listings をウォルマートに接続

他のマーケットプレイスと同様、 [!DNL Walmart] を使用すると、サードパーティセラーは他のユーザーが販売した商品をリストできます。

- [!DNL Walmart Marketplace] では、UPC や GTIN などの製品識別子を使用して、製品を既存の製品と照合します [!DNL Walmart Marketplace] listings.

- 一致した製品の場合、Walmart Marketplace のリストが更新されて次が含まれます [!DNL Commerce] から製品を接続したときの製品オファー [!DNL Channel Manager].

- 通常、最も価格の低い製品オファーは、次の場所から最初に表示されます [!DNL Walmart Marketplace] リストに表示されますが、レビューなどの他の要因もプレースメントに影響します。

## 製品に一致

製品を一致させる場合、チャネルマネージャーは製品データをに送信します [!DNL Walmart Marketplace] マッピングされたに一致する属性値を持つ既存の一覧を検索するには [!DNL Commerce] 製品属性。 一致条件は、によって決定されます [属性マッピング設定](map-catalog-attributes.md) ストアチャネル用。

一致する製品が見つかった場合は、既存の製品リストが更新され、オファーが追加されます。

### 前提条件

製品を照合する前に、製品カタログの属性値がウォルマートの要件を満たしていることを確認し、製品属性設定を構成します。 参照： [カタログ属性のマッピング](map-catalog-attributes.md).

#### 製品の選択と一致

1. 連携した販売チャネルを開きます。

1. 送信元 **[!UICONTROL Listings]**、一致させる製品を選択します *[!UICONTROL Draft]* ステータス。

   ![Listings から商品を選択し、マッチング用に送信します](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. を選択 **[!UICONTROL Match Products]**.

   メッセージは、照合のために送信された製品の数を示します。

   選択した製品のステータスが「」に変更されます [!UICONTROL *処理*] 一致操作が完了するまで。 Walmart Marketplace がマッチ操作を完了するまでに最大 30 分かかる場合があります。

### 一致ステータスを確認

一致が完了したら、 **[!UICONTROL Refresh products]** をクリックして、現在の製品ステータスを表示します。 *次に一致* または *エラー*.

- **[!UICONTROL Match]** 商品が正常に一致したことを示します。 商品オファーは、既存のウォルマート マーケットプレイスのリストに接続されていました。 次の場合 [Marketplace ストアがアクティブではありません](walmart-requirements.md#walmart-marketplace-store-status), *[!UICONTROL Staged for Match]* はに表示されます。 *[!UICONTROL Status detail]* 列。 ステージングされた製品は、 [!DNL Walmart Marketplace] ストアがアクティブ化されました。

- **[!UICONTROL Error]** は、次のいずれかの問題が原因で一致操作が失敗したことを示します。

   - [!DNL Channel Manager] 接続の問題により、照合を送信できませんでした。

   - 一致する項目が見つかりませんでした。

   - 一致が見つかりましたが、以下の理由によりリストに接続できません [!DNL Walmart Marketplace] がエラーコードを返しました。 を参照してください。 **[!UICONTROL Error Description]** この問題に関する情報を。

### ウォルマートのリストを確認

製品を照合した後、更新された製品リストを確認し、から製品の詳細、価格、在庫数量を検証します [[!UICONTROL Walmart Marketplace Seller Account Items] dashboard](https://seller.walmart.com/items-and-inventory/manage-items) をクリックして、更新された製品を確認します。

### 製品一致エラーのトラブルシューティング

製品の一致操作がエラーで失敗した場合、エラーメッセージがに表示されます *[!UICONTROL Status detail]* 列： [!UICONTROL Channel Manager] 製品リスト。

返される一般的なエラーが、形式が正しくない製品 ID 値であるか、必要な属性がありません。

#### 製品 ID 値を修正

| タイプ | 説明 | 例 |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12：チェックディジットを含む 12 桁の数値。 </br></br>8 桁の UPC-E など、UPC の桁数が 12 桁未満の場合は、要件を満たすために末尾にゼロを追加します。 | 変更前 `45678912345` 対象： `045678912345` |
| GTIN | GTIN-14：チェックディジットを含む 14 桁の数値。 </br></br>GTIN の桁数が 14 桁未満の場合は、先頭に 0 を追加します </br>要件を満たすこと。 | 変更 `456789123456` 対象： `0045678912345` |
| EAN | GTIN-13：チェックディジットを含む 13 桁の数値。 </br></br>EAN の桁数が 13 桁未満の場合は、先頭のを追加します </br>要件を満たすゼロ。 | 変更前 `4567891234` 対象： `0004567891234` |

Walmart Marketplace のエラーコードについて詳しくは、 [ウォルマート販売者ヘルプ](https://sellerhelp.walmart.com/s/guide?article=000005844).

## 新しい製品リストのアップロード

Walmart Marketplace に一致しない製品の場合は、Walmart 製品カテゴリの Excel テンプレートを使用して、製品リストを一括アップロードします。 から書き出された製品カタログデータを使用して、ウォルマートテンプレートに入力します [!DNL Commerce] インスタンス。

新規商品リストについては、商品カタログを確認し、Walmart Marketplace で販売する予定の商品に、Walmart Marketplace の商品リストに必要な属性が含まれていることを確認してください。

**Walmart Marketplace listings – 属性要件**

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

- が満たされていることを確認します [ウォルマートの要件](walmart-requirements.md).

- あなたの [!DNL Commerce] 製品カタログ、Walmart Marketplace にリストする製品のカタログ設定に必要な属性がすべて含まれ、Walmart Marketplace のコンテンツガイドラインを満たしていることを確認します。

- エクスポート操作を完了するために cron ジョブが実行中であることを確認します。

   - オンプレミスインスタンスについては、を参照してください。 [Cron の設定と実行](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html).

   - Adobeクラウドインフラストラクチャについては、を参照してください。 [cron ジョブの設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html).

### アップロードする製品データファイルを作成します

1. から [ウォルマート販売者アカウント](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)、ウォルマート販売センターから製品リストテンプレートをダウンロードします。

   - 製品カタログ項目ページから、を選択します。 **[!UICONTROL Add Items]**. 次に、を選択します **[!UICONTROL Add items in bulk]**.

     ![Walmart Marketplace の項目設定の「一括で項目を追加」オプション](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - ダウンロードページで、次を選択します **[!UICONTROL Full Setup]**. 次に、項目カテゴリを選択し、カテゴリテンプレートをダウンロードします。

     ![ウォルマート Marketplace の品目設定の「カテゴリテンプレートをダウンロード」オプション](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - テンプレートに、製品リストへの登録に必要な属性と推奨される属性が含まれていることを確認します。

1. から [!DNL Commerce] 管理者が、Adobeから書き出す商品データを選択します [!DNL Commerce] サイト。

   - 管理者から、を選択します。 [!UICONTROL **システム** > データ転送 > **Export**].

   - 日 [!UICONTROL Export] 内のページ [!UICONTROL Entity Type] フィールド、選択 [!UICONTROL **製品**].

   - が含まれる [!UICONTROL Entity Attributes] テーブルでは、商品データの書き出しの選択条件を設定します。

     フィルターを使用して、自社で販売する製品カテゴリに適用する属性値を選択および設定します。 ウォルマートの必須属性と推奨属性を必ず含めてください。 （詳しくは、 [データを書き出し](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) Adobe内 [!DNL Commerce] 詳しい手順については、ユーザーガイドを参照してください）。

     書き出しから属性を省略するには、 [!UICONTROL **除外**] 行の先頭にあるチェックボックス。

1. 属性テーブルの末尾までスクロールし、を選択します。 [!UICONTROL **続行**] データの書き出しを開始します。

   CSV 書き出しファイルは、メッセージキューを介して cron ジョブで処理され、に保存されます。 `var/export/folder`. （詳しくは、 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) が含まれる *設定ガイド*.）

1. Walmart Marketplace 製品カテゴリの Excel テンプレートを開き、Excel マクロ機能を使用して、書き出された製品データを Excel テンプレートに結合します。

1. 書き出した製品データを含む Excel ファイルをアップロードします。

   - の製品カタログ項目ページに戻ります。 [ウォルマート・セラー・センター](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - を選択 [!UICONTROL **項目を追加** > **項目を一括で追加**].
   - 完成したスプレッドシートを「アップロード」セクションにドラッグします。
   - を選択 [!UICONTROL **Submit**].
   - 「」を選択します&#x200B;[!UICONTROL  **アクティビティフィード**] 進行状況を表示します。

手順について詳しくは、を参照してください [完全な項目仕様を使用した項目の一括追加](https://sellerhelp.walmart.com/s/guide?article=000007680) が含まれる [!DNL *ウォルマート販売者ヘルプ*].
