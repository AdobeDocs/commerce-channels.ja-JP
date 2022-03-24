---
title: チャネルストアに製品を追加
description: カタログから販売チャネルに製品を追加して、Marketplace での販売用の製品品揃えを作成します
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---


# チャネルストアに製品を追加

チャネルマネージャーで、 [!DNL Commerce] ウォルマートマーケットプレイスの販売カタログ

製品を販売チャネルに同期するには、選択した製品が次の属性設定を持っている必要があります。

- **[!UICONTROL Publish to Channel Manager]** 属性が有効になっている

- 1 つ以上の製品属性が [必須の Walmart Marketplace 属性](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

選択内容を保存すると、チャネルマネージャはチャネルに製品データを読み込みます。 この処理には最大 30 分かかる場合があります。

## セールスチャネルに製品を追加

1. チャネルマネージャーストアに関連付けられている製品カタログを開きます。

   接続されたセールスチャネルストアから、 **製品を追加**.

   ![接続されたチャネルに製品を追加](assets/add-initial-products-to-connected-channel.png)

   カタログが新しいタブで開きます。

1. カタログの製品グリッドから、Walmart Marketplace で販売する製品を選択します。

   ![接続されたチャネルに製品を送信](assets/select-products-from-catalog.png)

1. を有効にします。 **[!UICONTROL Publish to Channel Manager]** 属性を設定します。

   - 送信者 **[!UICONTROL Actions]**&#x200B;を選択します。 **[!UICONTROL Update attributes]**.

   - スクロールして **[!UICONTROL Publish to Channel Manager]** 属性を設定し、有効にします。

   - 製品属性に、必要なウォルマート製品 ID の 1 つ以上が含まれていることを確認します。

   - 選択 **[!UICONTROL Save]**.

   確認メッセージが表示されます。

   ![カタログから販売チャネルへの製品インポートの確認メッセージ](assets/product-import-from-catalog-confirmation.png)

   更新がスケジュールされたことを示すメッセージが表示された場合は、 [キュー:consumers:開始](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] コマンドを使用して、更新を直ちに処理できます。

   ```bash
   $ bin/magento queue:consumers:start product_action_attribute.update
   ```

1. 次の接続済みのセールスチャネルに戻る [!DNL Channel Manager].

   インポート操作が完了したら、次の製品を表示します： **[!UICONTROL Listings]**. 最初は、製品は *ドラフト* ステータス。 選択 [!UICONTROL Refresh products]**をクリックして、テーブルを更新します。

   ![接続済みセールスチャネルにインポートされた製品](assets/products-in-marketplace-sales-channel.png)
