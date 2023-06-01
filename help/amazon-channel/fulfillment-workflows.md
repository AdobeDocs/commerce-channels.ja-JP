---
title: Amazon fulfillment workflows
description: Amazonのリストからの注文の受け渡しは、注文の送信から出荷までの特定の順序に従います。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon fulfillment workflows

## 例：商人が果たす

| 手順 | 説明 |
|----|----|
| 1 | **商人が成就した命令がAmazonに置かれる。** Amazonが `Pending` 顧客のクレジットカード情報が確認されるまで。 注文件数 `Pending` ステータスはAmazonセールスチャネルに自動的にインポートされますが、 _[!UICONTROL Orders]_タブをクリックします。 |
| 2 | **順序はAmazonで検証されます。** 検証が完了すると、Amazonはステータスを `Unshipped`. このステータスが変更されると、注文はAmazonセールスチャネルで更新され、 _[!UICONTROL Orders]_タブをクリックします。 |
| 3 | **注文の詳細が更新されます。** Amazonセールスチャネルは、注文の詳細を、価格、顧客の E メール、顧客名で更新します。 この更新の間、Amazonの注文によって、対応する [!DNL Commerce] 注文を並べ替えることができます。 この [!DNL Commerce] 注文番号は、 _[!UICONTROL Orders]_タブをクリックします。 |
| 4 | **新しい顧客アカウントが作成されます。** 注文の設定で、顧客が [!DNL Commerce] データベースの場合、新しい顧客が [!DNL Commerce] データベースで、Amazon注文の対応する顧客情報を使用します。 次を選択した場合： `No Customer Creation (guest)` 順序の設定では、順序は [!DNL Commerce] ゲストプロセスのみを使用します。 この時点で、 [!DNL Commerce] システムは ERP/OMS/WMS と統合され、新しい注文が配置され、内部で作成される統合に従って受注が取得されます [!DNL Commerce]. |
| 5 | **注文が発送されます。** 次の [!DNL Commerce] 注文処理ページで、注文を発送し、追跡番号を追加します。 すべての項目が `Shipped` ステータス：<ul><li>のステータス [!DNL Commerce] 注文変更 `Complete`.</li><li>Amazonセールスチャネルの注文のステータスは、 `Shipped`.</li><li>トラッキング番号がAmazonに同期され、Amazonのオーダーのステータスが `Shipped`.</li><li>発送通知は、Amazon経由で顧客に送信されます。 [!DNL Commerce] (Amazonのポリシーに従って ) |

## 例：Amazon(FBA) で実現

| 手順 | 説明 |
|---|---|
| 1 | **Amazonが満たした命令がAmazonに置かれます。** |
| 2 | **注文がインポートされます。** 注文が割り当てられるまで、注文はAmazon販売チャネルにインポートされません `Shipped` Amazon別のステータス。 Amazonはこの製品の在庫を持つので、倉庫や在庫管理との干渉を防ぎます。 |
| 3 | **注文の詳細が更新されます。** が [順序設定](./order-settings.md)の場合、Amazonの順序は [!DNL Commerce] 注文として作成され、ステータスが `Complete`. |
