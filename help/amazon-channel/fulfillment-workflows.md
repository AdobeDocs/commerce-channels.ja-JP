---
title: Amazon フルフィルメントのワークフロー
description: Amazon リストに記載された注文のフルフィルメントは、注文送信から出荷への特定の順序に従います。
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon フルフィルメントのワークフロー

## 例: マーチャントによって履行される

| バイ | つい |
|----|----|
| raid-1 | **このような場合、Amazon には商人の注文が適用されます。** Amazon `Pending` は、顧客のクレジットカード情報が確認されるまでの状態を割り当てます。 注文 `Pending` 状況は、Amazon 販売チャンネルに自動的に読み込まれますが、タブには表示されません _[!UICONTROL Orders]_。 |
| pplx-2 | **この順序は、Amazon によって確認されます。** 確認すると、Amazon によっての状態がに変更さ `Unshipped` れます。 この状態が変更されると、Amazon sales チャンネル内の注文が更新され、タブに表示され _[!UICONTROL Orders]_ます。 |
| 3-d | **受注明細が更新されました。** Amazon sales チャンネルにより、注文明細が価格、顧客の電子メール、および顧客名で更新されます。 この更新中に、Amazon order によって [!DNL Commerce] 注文管理ページに対応する注文が作成されます。 注文 [!DNL Commerce] 番号は、注文情報と共にタブに表示され _[!UICONTROL Orders]_ます。 |
| 4.0 | **新しい顧客 id が作成されます。** 注文設定で設定されていて、ユーザーがデータベース内に存在しない場合は [!DNL Commerce] 、 [!DNL Commerce] Amazon の注文に記載されている顧客情報を使用して、データベースに新しい顧客が作成されます。 注文の設定で選択した場合は、 `No Customer Creation (guest)` ゲストプロセスに従う必要が [!DNL Commerce] あります。また、顧客はデータベースに作成されません。 この時点で、システムが ERP、OMS、または WMS と統合されている場合は、新しい注文が配置され、内部に作成されるときに、 [!DNL Commerce] 注文が選択され [!DNL Commerce] ます。 |
| . | **注文が出荷されます。** 注文 [!DNL Commerce] 処理ページから、注文が出荷され、追跡ナンバーが追加されます。 すべてのアイテムが状態でマークされている場合 `Shipped` :<ul><li>注文の状態が [!DNL Commerce] に変更され `Complete` ます。</li><li>Amazon 販売チャンネルの注文の状態がに変更され `Shipped` ます。</li><li>トラッキング番号が Amazon に同期され、Amazon 上の注文の状態がに変更され `Shipped` ます。</li><li>送付通知が Amazon によって顧客に送られるのは、amazon によって行われ [!DNL Commerce] ます (amazon のポリシーによって異なります)。 |

## 例: Amazon によって履行される (FBA)

| バイ | つい |
|---|---|
| raid-1 | **Amazon から満たされた注文が amazon によって行われます。** |
| pplx-2 | **注文がインポートされます。** この順序は、 `Shipped` amazon によってステータスが割り当てられるまでは、amazon sales channel にインポートされません。 Amazon によってこの製品のインベントリが作成されるため、ユーザーの倉庫/在庫管理の妨害にはなりません。 |
| 3-d | **受注明細が更新されました。** 注文設定で設定されている場合は [ ](./order-settings.md) 、Amazon order により、対応する注文が作成され、 [!DNL Commerce] のステータスがの注文として作成され `Complete` ます。 |
