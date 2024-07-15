---
title: Manage Listings
description: 'Adobe CommerceとMagento Open Sourceのチャネルマネージャーを使用して  [!DNL Commerce]  店舗のセールスチャネルリストを管理します。'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Manage Listings

チャネルマネージャー UI から [!DNL Walmart Marketplace] 販売チャネルの製品リストを管理します。

個々のリストのステータスは、製品が [!DNL Channel Manager] ワークフローのどこに存在するかを示しているので、次の手順を決定し、エラーを解決できます。

![ 接続された販売チャネルのリストページ ](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

リスト表示では、次のタスクを実行できます。

* 現在の一覧を表示する
* リストの並べ替えとフィルタリング
* 製品を追加
* 製品に一致
* リストステータスの追跡
* エラーステータスを含むリストのエラー説明を確認します

## 製品リストの表示

1. 管理者で、[!UICONTROL **マーケティング**/**チャネルマネージャー**] に移動します。

1. ストアリストで、ストアエントリ行の目のアイコンを選択して、ストア表示を開きます。

1. [!UICONTROL **Listings**] を選択します。

1. *リスト* テーブルの任意の列見出しを選択して、*リスト* ビューを並べ替えます。

1. ステータス数カードの 1 つを選択して、*リスト* 表示をフィルタリングします。

1. 並べ替え順をリセットし、「**製品を更新**」を選択してフィルターを削除します。

## チャネルマネージャーへの [!DNL Commerce] 製品の追加

次のタスクを完了して、[!DNL Walmart Marketplace] チャネルの製品品揃えを作成します。

* [製品カタログから  [!DNL Channel Manager] の  [!DNL Commerce]  うに製品を追加します。](add-products-to-channel-store.md)

* [カタログ属性のマッピング](map-catalog-attributes.md#configure-product-attribute-settings)

## [!DNL Walmart] で製品を照合

製品マッチングを使用するか、新しい製品の製品リストを手動でアップロードすることで、[!DNL Walmart Marketplace] ージ上で製品オファーを作成できます。

* **[Walmart で商品を照合](connect-listings-to-marketplace.md)** – 同じ商品を販売する既存のリストを更新することで、チャネルから [!DNL Walmart Marketplace] に商品リストを接続します。 一致条件は、チャネルの [ 属性マッピング設定 ](map-catalog-attributes.md) によって決定されます。

* **[新しい一覧を手動でアップロードする](connect-listings-to-marketplace.md#upload-new-product-listings)** - [!DNL Walmart Marketplace] の既存の一覧と一致しない製品については、[!DNL Walmart] 製品カテゴリの Excel テンプレートを使用して一覧を一括アップロードします。

## リスト・コントロールと列の説明

次の表に、[!UICONTROL Listings] で使用できるコントロールと列を示します。

**[!UICONTROL Listings]** 用コントロール

| **制御** | **説明** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | [!UICONTROL Admin Product Catalog] ページを開いて、[!DNL Walmart Marketplace] 品揃えに追加する製品を選択したり、Walmart Marketplace のリスト要件を満たすように製品属性を更新したりできます。 |
| [!UICONTROL Match products on Walmart] | ステータスで 1 つ以上の製品を選択 [!UICONTROL Draft] た後、「[!UICONTROL Match products on Walmart]」を選択して、既存の [!DNL Walmart Marketplace] 製品リストに追加できる製品オファーを確認します。 |
| [!UICONTROL Refresh products] | 最新のリストとステータスでディスプレイを更新します。 また、このコントロールは、リスト表示を既定の並べ替え順にリセットし、フィルタを削除します。 |
| [!UICONTROL Filter by *ステータス*] | リストテーブルの上にあるステータスカードの 1 つを選択して、特定のステータスのリストのみを表示します。 **[!UICONTROL Refresh products]** を選択してフィルターを削除します。 |
| [!UICONTROL Sort products] | 任意の列ヘッダーを選択して、リストの並べ替え順を変更します。 |


**列の説明**

| **フィールド** | **説明** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | [!DNL Commerce] ストアカタログからの商品の名前。 |
| [!UICONTROL SKU (Unique ID)] | [!DNL Commerce] カタログで製品に割り当てられた SKU。 |
| [!UICONTROL  Quantity] | Adobe CommerceまたはMagento Open Sourceで利用できる在庫の量。 |
| [!UICONTROL Price] | [!DNL Commerce] ストアカタログからの製品価格。 カタログ価格のアップデートはチャネルマネージャーに同期され、リストされた項目に現在の価格が表示されるように [!DNL Walmart Marketplace] に送信されます。 |
| [!UICONTROL Status] | 現在の注文ワークフローにおける現在の [!DNL Commerce] 注ステータスを示します。 [!DNL Channel Manager] に製品を正常に追加したとき、および Marketplace で製品を一致させたときに、ステータスが更新されます。 操作が失敗すると、リストにエラーステータスが表示されます。 エラーを修正した後、[!DNL Channel Manager] は操作を再試行し、ステータスを更新します。 |
| [!UICONTROL Error Description] | ステータスが `[!DNL Error]` の製品に関する追加のエラー情報を提供します。 |

### リストのステータスについて

リストワークスペースでは、ステータス ラベルに製品の [!DNL Channel Manager] ワークフロー内の位置が表示されるので、次の手順を判断してエラーを解決できます。 リストには、次のステータスラベルを設定できます。

* **[!UICONTROL Draft]** - [ マッチング用に送信された  [!DNL Walmart]  に送信されていない製品を識別 ](connect-listings-to-marketplace.md#match-products) ます。

* **[!UICONTROL Processing]** - [!DNL Walmart Marketplace] で照合するために送信された製品を識別します。 製品は、[!DNL Walmart] が、一致が成功したかどうか、またはエラーが発生したかどうかを示す HTTP ステータスメッセージを返すまで、*処理中* ステータスのままになります。 [!DNL Walmart Marketplace] ージで一致操作が完了するまで最大 30 分かかる場合があります。

* **[!UICONTROL Match]** - [!DNL Walmart] で正常に一致した製品を識別します。

  一致が発生するのは、製品属性値（UPC コードなど）が既存の [!DNL Walmart Marketplace] リストの UPC 値と一致した場合です。 商品が一致すると、Commerce商品オファーが既存のリストに追加されます。

  [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) ダッシュボードをチェックして、更新された製品リストを確認し、製品の詳細、価格、在庫数量を確認します。

* **[!UICONTROL Match - Match in Stage]** - [!DNL Walmart] で一致した製品のうち、[!DNL Walmart Marketplace] ストアがライブになるまで接続できないものを識別します。 このステータスを持つ製品は、[!DNL Walmart Marketplace] ストアが公開されると自動的に接続されます。

* **[!UICONTROL Error]** – 既存の [!DNL Walmart Marketplace] リストと一致しなかった製品を識別します。

* **[!UICONTROL Error description]** - リストのエラーに関する詳細情報を提供します。

  エラーを解決したら、一致させるために製品を再送信します。 [ 製品一致エラーのトラブルシューティング ](connect-listings-to-marketplace.md#troubleshoot-product-match-errors) を参照してください。
