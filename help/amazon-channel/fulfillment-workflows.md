---
title: Amazon フルフィルメントワークフロー
description: Amazonリストからの注文のフルフィルメントは、注文の送信から出荷までの特定の順序に従います。
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon フルフィルメントワークフロー

## 例：販売者による履行

| ステップ | 説明 |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **マーチャントが履行した注文はAmazonで行われます。Amazon**、顧客のクレジットカード情報が確認されるまで、`Pending` のステータスを割り当てます。 `Pending` ステータスの注文は、Amazon販売チャネルに自動的にインポートされますが、「_[!UICONTROL Orders]_」タブには表示されません。 |
| 2 | **注文はAmazonで検証されています。** 検証されると、Amazonのステータスが `Unshipped` に変わります。 このステータスが変更されると、注文がAmazon sales channel で更新され、「_[!UICONTROL Orders]_」タブに表示されます。 |
| 3 | **注文の詳細が更新されます。Amazon セールスチャネル**、価格、お客様のメールアドレス、お客様名で注文の詳細を更新します。 この更新中、Amazonの受注によって、対応する [!DNL Commerce] 受注が「受注管理」ページに作成されます。 [!DNL Commerce] 注文番号は、[_[!UICONTROL Orders]_] タブの注文情報と共に表示されます。 |
| 4 | **新しい顧客アカウントが作成されます。** 注文設定で指定したが、[!DNL Commerce] データベースに顧客が存在しない場合、Amazon注文の対応する顧客情報を使用して、[!DNL Commerce] データベースに新しい顧客が作成されます。 注文設定で `No Customer Creation (guest)` を選択した場合、注文は [!DNL Commerce] のゲストプロセスに従い、データベースに顧客は作成されません。 この時点で、[!DNL Commerce] システムが ERP/OMS/WMS と統合されている場合、[!DNL Commerce] 内に配置および作成される新しい注文の統合に従って注文が取得されます。 |
| 5 | **注文は出荷されます。** [!DNL Commerce] の注文処理ページから、注文を発送し、追跡番号を追加します。 すべての項目が `Shipped` の状態でマークされた場合：<ul><li>[!DNL Commerce] 注文のステータスが「`Complete`」に変わります。</li><li>Amazonの販売チャネル注文のステータスが「`Shipped`」に変わります。</li><li>トラッキング番号がAmazonに同期され、Amazonでの注文のステータスが `Shipped` に変わります。</li><li>出荷通知は、（Amazonのポリシーに従って） [!DNL Commerce] からではなく、Amazonを介してお客様に送信されます。 |

## 例：Amazon（FBA）によるフルフィルメント

| ステップ | 説明 |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **Amazonで受け渡された注文はAmazonで行われます。** |
| 2 | **注文が読み込まれます。** 注文がAmazonによって `Shipped` ステータスに割り当てられるまで、注文はAmazon販売チャネルにインポートされません。 Amazonはこの商品の在庫を保有しているので、倉庫/在庫管理への干渉を防ぎます。 |
| 3 | **注文の詳細が更新されます。** [ 注文設定 ](./order-settings.md) で設定した場合、Amazon注文は対応する [!DNL Commerce] 注注文を作成し、ステータスが `Complete` の注文として作成されます。 |
