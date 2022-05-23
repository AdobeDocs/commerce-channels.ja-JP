---
title: セールスチャネルストアに製品を追加
description: 次の製品の品揃えを作成 [!DNL Walmart Marketplace] カタログから販売チャネルに製品を追加する販売
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 76aa7451c9df83fbb7ea808fc14ef2d306235da2
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# セールスチャネルストアに製品を追加

製品を Walmart Marketplace セールスチャネルに同期するには、 [!DNL Commerce] 製品カタログを作成し、チャネルマネージャに読み込みます。 選択した製品には、次の属性設定が必要です。

- **[!UICONTROL Publish to Channel Manager]** 属性が有効になっている

- 1 つ以上の製品属性が [必須の Walmart Marketplace 属性](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

製品のインポート元のプロセス [!DNL Commerce] 選択した製品の数に応じて、Channel Manager への接続に最大 30 分以上かかる場合があります。

## 製品を追加

1. 接続されたセールスチャネルストアから、 **製品を追加** をクリックして、製品カタログを開きます。

   ![セールスチャネルストアに製品を追加](assets/add-initial-products-to-connected-channel.png)

   カタログが新しいタブで開きます。

1. カタログ製品グリッドから、販売する製品を選択します [!DNL Walmart Marketplace].

   ![製品をセールスチャネルストアに送信](assets/select-products-from-catalog.png)

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

1. 読み込み操作が完了したら、に戻って、追加された製品を確認します。 [!DNL Channel Manager] および選択 **[!UICONTROL Listings]**.

   ![接続済みセールスチャネルにインポートされた製品](assets/products-in-marketplace-sales-channel.png)

   最初は、製品は *ドラフト* ステータス。 選択 **[!UICONTROL Refresh products]** をクリックして、テーブルを更新します。

