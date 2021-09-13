---
title: Amazon Fulfillment Workflows
description: Amazonのリストからの注文の受け渡しは、注文の送信から出荷までの特定の順序に従います。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazonフルフィルメントワークフロー

## 例：商人が果たす

| 手順 | 説明 |
|----|----|
| 1 | **商人が成就した命令がAmazonに下る。** Amazonは、顧客のクレジットカ `Pending` ード情報が確認されるまで、のステータスを割り当てます。「`Pending`」ステータスの注文は、Amazonの販売チャネルに自動的にインポートされますが、「_[!UICONTROL Orders]_」タブには表示されません。 |
| 2 | **注文はAmazonで確認される。** 検証が完了すると、Amazonはステータスをに変更しま `Unshipped`す。このステータスの変更により、注文はAmazonの販売チャネルで更新され、「_[!UICONTROL Orders]_」タブに表示されます。 |
| 1 | **注文の詳細が更新されます。** Amazonの販売チャネルは、注文の詳細を価格、顧客のEメール、顧客名で更新します。この更新中、Amazonの注文により、注文管理ページに対応する[!DNL Commerce]の注文が作成されます。 [!DNL Commerce]の注文番号が&#x200B;_[!UICONTROL Orders]_タブに注文情報と共に表示されます。 |
| 4 | **新しい顧客アカウントが作成されます。** 注文の設定で顧客がデータベースに存在しない場合、Amazon注文の対応する顧客情報を使用して新しい顧客がデータベースに作成されま [!DNL Commerce]  [!DNL Commerce] す。注文設定で`No Customer Creation (guest)`を選択した場合、注文は[!DNL Commerce]ゲストプロセスに従い、データベースに顧客を作成しません。 この時点で、[!DNL Commerce]システムがERP/OMS/WMSと統合されている場合、注文は、配置され、[!DNL Commerce]内に作成される新しい注文の統合に基づいて取得されます。 |
| 5 | **注文が発送されました。** 注文処理ペ [!DNL Commerce] ージから、注文を発送し、追跡番号を追加します。すべての項目が`Shipped`ステータスに設定された場合：<ul><li>[!DNL Commerce]順序のステータスが`Complete`に変わります。</li><li>Amazon販売チャネルの注文のステータスが`Shipped`に変わります。</li><li>トラッキング番号はAmazonに同期され、Amazonの注文のステータスは`Shipped`に変わります。</li><li>送料通知は、(Amazonのポリシーに従って)[!DNL Commerce]からではなく、Amazonを介してお客様に送信されます。 |

## 例：Amazon(FBA)によって達成される

| 手順 | 説明 |
|---|---|
| 1 | **Amazonが成就した命令がAmazonに置かれる。** |
| 2 | **注文がインポートされます。** 注文は、Amazonによってステータスが割り当てられるまで、Amazonの販売チャネルに `Shipped` インポートされません。Amazonにはこの製品の在庫があるので、倉庫や在庫管理への干渉を防ぎます。 |
| 1 | **注文の詳細が更新されます。** 注文の設定で [設定](./order-settings.md)した場合、Amazonの注文は対応する注文を作成 [!DNL Commerce] し、ステータスが「 」の注文として作成されま `Complete`す。 |
