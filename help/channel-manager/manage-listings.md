---
title: リストの管理
description: '''次の項目のセールスチャネルリストを管理します： [!DNL Commerce] Channel Manager を使用してAdobe CommerceおよびMagento Open Sourceで保存。'
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# リストの管理

の製品リストを管理 [!DNL Walmart Marketplace] チャネルマネージャー UI からの sales チャネル

個々のリストのステータスは、製品が [!DNL Channel Manager] ワークフローを使用して、次の手順を決定し、エラーを解決できます。

![接続されたセールスチャネルのリストページ](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

リスト表示から、次のタスクを実行できます。

* 現在のリストを表示
* リストの並べ替えとフィルター
* 製品を追加
* 製品を一致させる
* リストステータスを追跡
* エラーステータスのリストのエラー説明を確認する

## 製品リストを表示

1. 管理者から、に移動します。 [!UICONTROL **マーケティング** > **チャネルマネージャ**].

1. 「ストア」リストで、ストアエントリ行の目のアイコンを選択して、ストアビューを開きます。

1. 選択 [!UICONTROL **リスト**].

1. 並べ替え *リスト* 表示するには、 *リスト* 表。

1. フィルター *リスト* 表示するには、いずれかのステータスカウントカードを選択します。

1. 並べ替え順をリセットし、「 」を選択してフィルターを削除します **製品を更新**.

## 追加 [!DNL Commerce] 製品をチャネルマネージャに

次の製品の品揃えを作成します： [!DNL Walmart Marketplace] 次のタスクを実行して、チャネルを生成します。

* [以下から製品を追加 [!DNL Commerce] 製品カタログ [!DNL Channel Manager]](add-products-to-channel-store.md)

* [カタログ属性をマッピング](map-catalog-attributes.md#configure-product-attribute-settings)

## 次の製品を照合： [!DNL Walmart]

製品オファーは、 [!DNL Walmart Marketplace] 製品のマッチングを使用するか、新しい製品の製品リストを手動でアップロードしてください。

* **[ウォルマートでの製品のマッチング](connect-listings-to-marketplace.md)** — チャネルからに製品リストを接続します [!DNL Walmart Marketplace] 同じ製品を販売する既存のリストを更新する。 一致条件は、 [attribute-mapping 設定](map-catalog-attributes.md) チャネルの

* **[新しいリストを手動でアップロード](connect-listings-to-marketplace.md#upload-new-product-listings)** — 上の既存のリストと一致しない製品の場合 [!DNL Walmart Marketplace]、 [!DNL Walmart] 製品カテゴリ製品リストを一括アップロードするための Excel テンプレート。

## リストコントロールと列の説明

次の表に、で使用できるコントロールと列を示します。 [!UICONTROL Listings].

**のコントロール[!UICONTROL Listings]**

| **制御** | **説明** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | を開きます。 [!UICONTROL Admin Product Catalog] に追加する製品を選択するページ [!DNL Walmart Marketplace] 品揃え、または製品属性を更新して Walmart Marketplace リストの要件を満たす。 |
| [!UICONTROL Match products on Walmart] | で 1 つ以上の製品を選択した後 [!UICONTROL Draft] ステータス、選択 [!UICONTROL Match products on Walmart] 既存の [!DNL Walmart Marketplace] リスト。 |
| [!UICONTROL Refresh products] | 最新のリストとステータスで表示を更新します。 また、このコントロールは、リスト表示をデフォルトの並べ替え順にリセットし、フィルターを削除します。 |
| [!UICONTROL Filter by *ステータス*] | リスト表の上にあるステータスカードの 1 つを選択して、特定のステータスを持つリストのみを表示します。 「 」を選択してフィルターを削除します。 **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | 列ヘッダーを選択して、リストの並べ替え順を変更します。 |


**列の説明**

| **フィールド** | **説明** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | からの製品名 [!DNL Commerce] ストアカタログ。 |
| [!UICONTROL SKU (Unique ID)] | 内の製品に割り当てられた SKU [!DNL Commerce] カタログ。 |
| [!UICONTROL  Quantity] | Adobe CommerceまたはMagento Open Sourceで使用可能な在庫の量。 |
| [!UICONTROL Price] | からの製品価格 [!DNL Commerce] ストアカタログ。 カタログ価格の更新は Channel Manager に同期され、次にに送信されます [!DNL Walmart Marketplace]  上場された項目が現在の価格を示すように |
| [!UICONTROL Status] | 現在の注文ステータスを [!DNL Commerce] 注文ワークフロー。 製品をに正常に追加すると、ステータスが更新されます。 [!DNL Channel Manager] とは、マーケットプレイスで製品を照合する場合に使用します。 操作が失敗した場合は、エラーステータスがリストに表示されます。 エラーを修正した後、 [!DNL Channel Manager] 操作を再試行し、ステータスを更新します。 |
| [!UICONTROL Error Description] | 製品に関する追加のエラー情報を、 `[!DNL Error]` ステータス。 |

### リストステータスについて

リストワークスペースで、ステータスラベルに製品が [!DNL Channel Manager] ワークフローを使用して、次の手順を決定し、エラーを解決できます。 リストには次のステータスラベルを設定できます。

* **[!UICONTROL Draft]** — 過去に [送信先 [!DNL Walmart] 照合](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** — で照合用に送信された製品を識別します。 [!DNL Walmart Marketplace]. 製品は *処理中* 次の日までのステータス： [!DNL Walmart] は、一致が成功したか、またはエラーが発生したかを示す HTTP ステータスメッセージを返します。 一致操作が [!DNL Walmart Marketplace].

* **[!UICONTROL Match]** — で正常に一致した製品を識別します。 [!DNL Walmart].

   製品属性値（UPC コードなど）が既存の UPC 値と一致する場合に一致が発生します [!DNL Walmart Marketplace] リスト。 製品が一致する場合、コマース製品オファーが既存のリストに追加されます。

   次を確認します。 [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) ダッシュボードを使用して、更新された製品リストを確認し、製品の詳細、価格、在庫数量を確認します。

* **[!UICONTROL Match - Match in Stage]** — 一致する製品を識別します。 [!DNL Walmart] それは次の時点まで接続できない [!DNL Walmart Marketplace] ストアはライブです。 このステータスの製品は、 [!DNL Walmart Marketplace] ストアがライブになります。

* **[!UICONTROL Error]** — 既存の製品と一致しない製品を識別します。 [!DNL Walmart Marketplace] リスト。

* **[!UICONTROL Error description]** — リストエラーに関する詳細情報を提供します。

   エラーを解決したら、製品を再提出して照合します。 詳しくは、 [製品一致エラーのトラブルシューティング](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
