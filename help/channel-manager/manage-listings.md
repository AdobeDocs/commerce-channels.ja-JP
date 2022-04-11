---
title: リストの管理
description: 次の項目のセールスチャネルリストを管理します [!DNL Commerce] ストアを Channel Manager(Adobe CommerceとMagento Open Source) で保存します。
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 41a6afec60edbb23492627bd8e80632d3c952caf
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# リストの管理

次の場所から接続チャネルの製品リストを管理 [!UICONTROL Listings] （チャネルストア表示）。

以下を使用： *[!UICONTROL Listings]* 管理するワークスペース [!DNL Commerce] ウォルマート・マーケットプレイスで販売される製品。 個々のリストのステータスは、製品が [!DNL Channel Manager] ワークフローを使用して、次の手順を決定し、エラーを解決できます。

![接続されたセールスチャネルのリストページ](assets/products-submit-for-matching.png)

## リストを表示

1. 管理者から、に移動します。 [!UICONTROL **マーケティング** /チャネル/ **チャネルマネージャ**].

1. 「チャネルストア」リストで、ストアエントリ行の鉛筆アイコンを選択して、ストアビューを開きます。

1. 選択 [!UICONTROL **リスト**].

## チャネルマネージャーへのコマース製品の追加

次のタスクを実行して、Walmart Marketplace チャネル用の製品品揃えを作成します。

* [コマース製品カタログからチャネルマネージャーへの製品の追加](add-products-to-connected-channel.md)

* [製品の照合の設定](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## ウォルマートに製品を発行

製品のマッチングを使用するか、新しい製品の製品リストを手動でアップロードすることで、Walmart Marketplace で製品オファーを作成できます。 手順については、 [Walmart Marketplace へのリストの公開](publish-listings-to-marketplace.md) 次のトピックで説明するように：

* **[ウォルマートでの製品のマッチング](publish-listings-to-marketplace.md)** — チャネルからに製品リストを公開します [!DNL Walmart Marketplace] 同じ製品を販売する既存のリストを更新する。 一致条件は、 [属性マッピング設定](map-product-attributes-for-matching.md) チャネルの

* **[新しいリストを手動でアップロード](publish-listings-to-marketplace.md#upload-new-product-listings)-**-Walmart Marketplace の既存のリストと一致しない製品の場合は、Walmart 製品カテゴリ Excel テンプレートを使用して製品リストを一括アップロードします。

## リストコントロールと列の説明

次の表に、で使用できるコントロールと列を示します。 [!UICONTROL Listings].

**のコントロール[!UICONTROL Listings]**

| **制御** | **説明** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Refresh products] | 最新のリストとステータスで表示を更新します。 |
| [!UICONTROL Add Products] | を開きます。 [!UICONTROL Admin Product Catalog] に追加する製品を選択するページ [!DNL Walmart Marketplace] 品揃え、または製品属性を更新して Walmart Marketplace リストの要件を満たす。 |
| [!UICONTROL Match products on Walmart] | 「ドラフト」ステータスで 1 つ以上の製品を選択した後、「ウォルマートで製品を照合」を選択して、既存のに追加できる製品オファーがないかを確認します [!DNL Walmart Marketplace] リスト。 |


**列の説明**

| **フィールド** | **説明** |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | からの製品名 [!DNL Commerce] ストアカタログ。 |
| [!UICONTROL SKU (Unique ID)] | マーケットプレイスで製品の照合に使用される、マッピングされた属性。 このフィールド名は、 [!DNL Channel Manager] リスト この場合、製品照合操作では、 [!DNL Commerce] 検索するカタログ [!DNL Walmart Marketplace]  SKU 値が [!DNL Commerce] 製品属性。 |
| [!UICONTROL  Quantity] | Adobe CommerceまたはMagento Open Sourceで使用可能な在庫の量。 |
| [!UICONTROL Price] | からの製品価格 [!DNL Commerce] ストアカタログ。 カタログ価格の更新は Channel Manager に同期され、次にに送信されます [!DNL Walmart Marketplace]  上場された項目が現在の価格を示すように |
| [!UICONTROL Status] | 現在の注文ステータスを [!DNL Commerce] 注文ワークフロー。 製品をに正常に追加すると、ステータスが更新されます。 [!DNL Channel Manager] とは、マーケットプレイスで製品を照合する場合に使用します。 操作が失敗した場合は、エラーステータスがリストに表示されます。 エラーを修正した後、 [!DNL Channel Manager] 操作を再試行し、ステータスを更新します。 |


### リストステータスについて

リストワークスペースで、ステータスラベルに製品が [!DNL Channel Manager] ワークフローを使用して、次の手順を決定し、エラーを解決できます。 リストには次のステータスラベルを設定できます。

* **[!UICONTROL Draft]** — 過去に [送信先 [!DNL Walmart] 照合](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**- [!DNL Walmart Marketplace]. 製品は *処理中* 次の日までのステータス： [!DNL Walmart] は、一致が成功したか、またはエラーが発生したかを示す HTTP ステータスメッセージを返します。 一致操作が [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** — で正常に一致した製品を識別します。 [!DNL Walmart].

   製品属性値 — UPC コード例えば、既存の[!DNL Walmart Marketplace] リスト。 製品が一致すると、コマース製品オファーが既存のウォルマートリストに追加されます。

   次を確認します。 [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) ダッシュボードを使用して、更新された製品リストを確認し、製品の詳細、価格、在庫数量を確認します。


* **[!UICONTROL Error]** — 既存の製品と一致しない製品を識別します [!DNL Walmart Marketplace] リスト。 エラーの詳細を表示するには、 *エラー* ステータスラベル

   エラーを解決したら、製品を再提出して照合します。 詳しくは、 [製品一致エラーのトラブルシューティング](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]** — に一致する製品を識別します [!DNL Walmart] それは、 [!DNL Walmart Marketplace] ストアはライブです。 このステータスの製品は、 [!DNL Walmart Marketplace] ストアがライブになります。
