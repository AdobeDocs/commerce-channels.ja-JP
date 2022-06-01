---
title: 「概要 [!DNL Channel Manager]"
description: インストールと使用方法 [!DNL Channel Manager] Adobe CommerceとMagento Open Sourceストアをサードパーティのマーケットプレイスと統合し、Marketplace のリスト、価格、在庫、販売をコマース管理者からシームレスに管理するためのセールスチャネルを作成します。
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: ae3d95fd0da6ee5013a19d7ac7ed5ef87e4a1325
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---


# について [!DNL Channel Manager]

[!DNL Channel Manager] は、Adobe CommerceまたはMagento Open Sourceの製品カタログを [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] 拡張機能の管理ビュー](assets/channel-manager-home.png)

チャネルマネージャーは、Adobe Commerceまたはで販売したいMagento Open Source販売者をサポートします [!DNL Walmart Marketplace].

をインストールして設定した後 [!DNL Channel Manager]、 [!DNL Commerce] 管理者が拡張され、 [!DNL Walmart Marketplace] 営業運営はコマース環境からシームレスに行えます。

* **リスト管理** — 製品リストを、 [!DNL Commerce] 既存の [!DNL Walmart Marketplace] リスト

* **Inventory management** — 正確な在庫レベルを確保するために、マーチャントの Marketplace セラーアカウントの品目は、コマースから自動的に同期および更新されます。

* **価格の更新** — 自動価格同期を使用して、マーケットプレイスリストの正確な価格を維持します。 Adobe Commerceで価格が変更されると、変更が Marketplace に 10 分以内に反映されます。

* **注文管理** — マーケットプレイスで新しい注文が作成されると、チャネルマネージャーは注文をAdobe Commerceと同期し、注文確認をマーケットプレイスに送信して、在庫が各注文で確保されるようにします。

* **出荷管理** — 注文がAdobe Commerceで出荷済みとマークされると、出荷の更新が [!DNL Walmart Marketplace]. この通知により、販売者は達成 SLA の要件を満たし、顧客は現在の注文の出荷更新通知を受け取ることができます。

* **キャンセル**- Adobe Commerceで注文がキャンセルされると、Channel Manager は更新された注文情報をマーケットプレイスに送信し、対応する Marketplace 注文のアクションをレプリケートします。

## Channel Manager の操作で予想される遅延

次の間のデータ同期プロセス： [!DNL Channel Manager] リンクされた [!DNL Walmart Marketplace] ストアが完了するまでにしばらく時間が必要です。 次の予定処理時間を確認 [!DNL Channel Manager] 営業チャネルの運用を計画する際に役立つ操作です。

**Channel Manager 操作の推定待ち時間**

| **操作** | **説明** | **予想される遅延** |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| チャネルマネージャーへの製品の追加 | コマース製品カタログから製品を選択し、チャネルマネージャに読み込みます。 | **最大 5 分** — 製品カタログ全体など、多数の製品を選択した場合、読み込み処理に時間がかかります。 |
| 次の製品を照合：[!DNL Walmart Marketplace] | チャネルマネージャで製品リストを選択し、ウォルマートに送信して照合します。 | **最大 30 分** — 多数の製品を選択した場合、選択した数量に応じて、照合の処理に時間がかかります。 |
| 在庫の更新 | Commerce で在庫数量が変更された場合、 [!DNL Channel Manager] は、Walmart への更新を同期します。 | **最大 10 分** |
| 価格の更新 | 製品価格が変更されると、Channel Manager は Walmart に更新を同期します。 | **最大 5 分** |
| ウォルマートからコマースへの同期の注文 | お客様がウォルマートマーケットプレイスでコマース製品を注文します。 ウォルマートが注文をチャネルマネージャに送信します。 注文は注文ダッシュボードに表示されます。 | **最大 30 分** |
| Commerce Order Management で作成された注文 | Channel Manager は、ウォルマート注文からコマース注文を作成し、注文ダッシュボードを更新してコマース注文番号を含めます。 | **最大 5 分** |

