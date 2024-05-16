---
title: Manage Listings
description: '''の販売チャネルリストの管理 [!DNL Commerce] Adobe CommerceとMagento Open Sourceのチャネルマネージャーを使用したストア。'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Manage Listings

の製品リストの管理 [!DNL Walmart Marketplace] チャネルマネージャー UI からの販売チャネル。

個々のリストのステータスは、製品の位置を示します [!DNL Channel Manager] 次の手順を決定し、エラーを解決するためのワークフローです。

![接続された販売チャネルのリストページ](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

リスト表示では、次のタスクを実行できます。

* 現在の一覧を表示する
* リストの並べ替えとフィルタリング
* 製品を追加
* 製品に一致
* リストステータスの追跡
* エラーステータスを含むリストのエラー説明を確認します

## 製品リストの表示

1. 管理者から、に移動します。 [!UICONTROL **Marketing** > **チャネルマネージャー**].

1. ストアリストで、ストアエントリ行の目のアイコンを選択して、ストア表示を開きます。

1. を選択 [!UICONTROL **Listings**].

1. を並べ替え *Listing* で任意の列見出しを選択して表示します。 *Listing* テーブル。

1. をフィルター *Listing* ステータス数カードの 1 つを選択して表示します。

1. 並べ替え順をリセットし、を選択してフィルターを削除します。 **製品の更新**.

## 追加 [!DNL Commerce] 製品をチャネルマネージャーに

の製品品揃えを作成します [!DNL Walmart Marketplace] 次のタスクを完了してチャネルを設定します。

* [からの製品の追加 [!DNL Commerce] 製品カタログの送信先 [!DNL Channel Manager]](add-products-to-channel-store.md)

* [カタログ属性のマッピング](map-catalog-attributes.md#configure-product-attribute-settings)

## 次の商品と一致 [!DNL Walmart]

製品オファーは、次の場所で作成できます [!DNL Walmart Marketplace] 製品のマッチングを使用するか、新しい製品の製品リストを手動でアップロードする。

* **[ウォルマートの商品を照合](connect-listings-to-marketplace.md)** – 製品リストをチャネルから接続します [!DNL Walmart Marketplace] 同じ製品を販売する既存のリストを更新する。 一致条件は、 [属性マッピング設定](map-catalog-attributes.md) チャネル用。

* **[新しい一覧を手動でアップロードする](connect-listings-to-marketplace.md#upload-new-product-listings)** – の既存のリストと一致しない製品の場合 [!DNL Walmart Marketplace]、を使用します [!DNL Walmart] 製品リストを一括アップロードするための製品カテゴリ Excel テンプレート。

## リスト・コントロールと列の説明

次の表では、で使用できるコントロールと列について説明します [!UICONTROL Listings].

**のコントロール[!UICONTROL Listings]**

| **制御** | **説明** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | を開きます [!UICONTROL Admin Product Catalog] ページをクリックして、に追加する製品を選択します [!DNL Walmart Marketplace] 品揃えまたはウォルマート・マーケットプレイスのリスト要件を満たすように製品属性を更新します。 |
| [!UICONTROL Match products on Walmart] | で 1 つ以上の製品を選択した後 [!UICONTROL Draft] ステータス、選択 [!UICONTROL Match products on Walmart] 既存のに追加できる製品オファーを確認するには： [!DNL Walmart Marketplace] リスト。 |
| [!UICONTROL Refresh products] | 最新のリストとステータスでディスプレイを更新します。 また、このコントロールは、リスト表示を既定の並べ替え順にリセットし、フィルタを削除します。 |
| [!UICONTROL Filter by *ステータス*] | リストテーブルの上にあるステータスカードの 1 つを選択して、特定のステータスのリストのみを表示します。 次を選択してフィルターを削除します **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | 任意の列ヘッダーを選択して、リストの並べ替え順を変更します。 |


**列の説明**

| **フィールド** | **説明** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | からの商品の名前 [!DNL Commerce] カタログを保存します。 |
| [!UICONTROL SKU (Unique ID)] | で製品に割り当てられた SKU [!DNL Commerce] カタログ。 |
| [!UICONTROL  Quantity] | Adobe CommerceまたはMagento Open Sourceで利用できる在庫の量。 |
| [!UICONTROL Price] | からの製品価格 [!DNL Commerce] カタログを保存します。 カタログ価格のアップデートはチャネルマネージャーに同期され、その後、に送信されます [!DNL Walmart Marketplace]  リストされた項目が現在の価格を示すように。 |
| [!UICONTROL Status] | 現在の注文ステータスを示します [!DNL Commerce] 注文ワークフロー。 製品をに正常に追加すると、ステータスが更新されます [!DNL Channel Manager] そして、マーケットプレイスで製品を照合する場合。 操作が失敗すると、リストにエラーステータスが表示されます。 エラーの修正後、 [!DNL Channel Manager] 操作を再試行し、ステータスを更新します。 |
| [!UICONTROL Error Description] | を持つ製品に関するエラー情報を追加します。 `[!DNL Error]` ステータス。 |

### リストのステータスについて

リストワークスペースでは、ステータス ラベルに商品の位置が表示されます [!DNL Channel Manager] 次の手順を決定し、エラーを解決するためのワークフローです。 リストには、次のステータスラベルを設定できます。

* **[!UICONTROL Draft]** – 実行されなかった製品を識別します。 [送信先 [!DNL Walmart] 照合する](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** – 照合の対象として送信された製品を [!DNL Walmart Marketplace]. 製品は次の場所に残ります *処理* ステータス終了： [!DNL Walmart] 一致が成功したかどうか、またはエラーが発生したかどうかを示す HTTP ステータスメッセージを返します。 で一致操作が完了するまで最大 30 分かかる場合があります。 [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** – で正常に一致した製品を識別します [!DNL Walmart].

  製品属性値（UPC コードなど）が既存の UPC 値と一致すると、一致が発生します [!DNL Walmart Marketplace] リスト。 商品が一致すると、Commerce商品オファーが既存のリストに追加されます。

  を確認します [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) 更新された製品リストを確認し、製品の詳細、価格および在庫数量を検証するためのダッシュボード。

* **[!UICONTROL Match - Match in Stage]** – にマッチした商品を識別する [!DNL Walmart] は、以下まで接続できません： [!DNL Walmart Marketplace] ストアはライブです。 このステータスを持つ製品は、 [!DNL Walmart Marketplace] ストアは運用開始します。

* **[!UICONTROL Error]** – 既存の製品と一致しなかった製品を識別します [!DNL Walmart Marketplace] リスト。

* **[!UICONTROL Error description]**- リストエラーに関する詳細情報を提供します。

  エラーを解決したら、一致させるために製品を再送信します。 参照： [製品一致エラーのトラブルシューティング](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
