---
title: Amazonの注文設定
description: 注文の設定を使用して、Amazonの注文をコマースストアにインポートして処理する方法を決定します。
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Amazonの注文設定

注文設定は、Amazonの注文をにインポートし、で処理する方法と方法を定義します [!DNL Commerce] また、 [ストアダッシュボード](./amazon-store-dashboard.md).

注文のインポート設定は次のように設定されています。 `Enabled` デフォルトでは、Amazonの注文がストアダッシュボードに表示され、対応する [!DNL Commerce] 注文。 インポートされた注文は、 [!DNL Commerce] [注文](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。

>[!NOTE]
>
>注文の設定に関係なく、ストア統合前に存在していたAmazonの注文はインポートされません。

後 [ストア統合](./store-integration.md) が完了したら、注文の設定を変更できます。 注文の設定を `Disabled`、Amazonの注文はストアダッシュボードに表示されますが、 [!DNL Amazon Seller Central] アカウント

注文がAmazonで作成された場合、 [!DNL Commerce]. Amazonが `Pending` 新しく作成された注文に対するステータス。 Amazonが注文と支払い方法を確認すると、注文のステータスが `Unshipped`. このステータス変更トリガーは、注文のインポート、および [!DNL Commerce] は、対応する順序に一致を作成します。

Amazonからインポートされた注文は、 [!DNL Commerce] [オーダーワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). 関連トピック [注文の管理](./managing-orders.md).

## 注文の設定 {#configure-order-settings}

1. クリック **[!UICONTROL Order Settings]** を選択します。

1. の場合 **[!UICONTROL Import Amazon Orders]** （必須）、次のオプションを選択します。

   - `Disabled`  — 対応する注文を [!DNL Commerce] Amazonから新しい注文を受け取ったとき。 このオプションを選択すると、このページ上の他のすべてのフィールドは無効になります。

   - `Enabled` - （デフォルト）対応する [!DNL Commerce] Amazonから新しい注文を受け取ったときの注文。 [!DNL Commerce] オーダーは、Amazonのステータスと在庫レベルに基づいて作成されます。

     >[!NOTE]
     >
     >Amazon注文のインポートは次のように設定する必要があります `Enabled` Amazonの注文を [!DNL Commerce] [注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。 に設定する場合 `Disabled`の場合、Amazonの注文に対応する [!DNL Commerce] 注文番号。で管理できません [!DNL Commerce]. これらの注文は、 [!DNL Amazon Seller Central] アカウント

1. の場合 **[!UICONTROL Import Amazon Orders Into Magento Store]**&#x200B;を選択します。 [!DNL Commerce] Amazonの注文が [!DNL Commerce].

   この設定のデフォルト値は、 [Amazonストアを追加しました](./store-integration.md). この設定を変更する場合は、オプションの一覧は [!DNL Commerce] には、設定で設定したが格納されます。 詳しくは、 [ストア](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. の場合 **[!UICONTROL Customer Creation]**、オプションを選択します。

   - `No Customer Creation (guest)` - （デフォルト） [!DNL Commerce] Amazon注文からインポートされた顧客データを使用する。 選択した場合、 [!DNL Commerce] は、でゲストのチェックアウトを処理するのと同じ方法で、読み込まれたAmazonの注文を処理します。 [!DNL Commerce].

   - `Build New Customer Account`  — で新しい顧客アカウントを作成するタイミングを選択します [!DNL Commerce] Amazonの注文でインポートされた顧客データを使用する。 このオプションは、Amazonの注文内容から顧客データベースを構築するのに役立ちます。

1. の場合 **[!UICONTROL Order Number Source]**、オプションを選択します。

   - `Build Using Magento Order Number` - （デフォルト）一意の [!DNL Commerce] 対応するAmazon注文の注文番号 [!DNL Commerce] オーダー ID を段階的に割り当てます。

   - `Build Using Amazon Order Number`  — いつ作成するかを選択します。 [!DNL Commerce] 対応するAmazon割り当ての注文番号を使用した注文番号。

   >[!NOTE]
   >
   >注文が読み込まれると、Amazonの注文番号が _[!UICONTROL Recent Orders]_リストを表示します。 この [!DNL Commerce] 注文番号は、 [!DNL Commerce] [注文](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペース。

1. の場合 **[!UICONTROL Order Status]** （必須）、次のオプションを選択します。

   - `Default Order Status` - （デフォルト）Amazonからインポートされた新しく作成されたオーダーに、新しいオーダーに対して定義されたデフォルトのオーダーステータスを割り当てる場合に選択します。 （新しい注文のカスタム注文ステータスを作成していない限り）新しい注文のデフォルトのステータスは、次のとおりです。 `Pending`. 詳しくは、 [注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Amazonから読み込まれた新しく作成されたオーダーに、デフォルト以外のステータスを割り当てる場合に選択します。

   - `Processing Order Status`  — 有効 **[!UICONTROL Order Status]** が `Custom Order Status`. Amazonからインポートされた新しく作成された注文に使用するステータスを選択します。 このフィールドのオプションは、 [!DNL Commerce]. 詳しくは、 [注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). カスタムの注文ステータスを作成して、ここに表示して選択することもできます。 カスタムの注文ステータスを作成するには、 [カスタム注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. 完了したら、「 **[!UICONTROL Save order settings]**.

![注文の設定](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | オプション：<ul><li>**[!UICONTROL Disabled]**  — 対応する注文を [!DNL Commerce] Amazonから新しい注文を受け取ったとき。 このオプションを選択すると、このページ上の他のすべてのフィールドは無効になります。</li><li>**[!UICONTROL Enabled]** - （デフォルト）対応する [!DNL Commerce] Amazonから新しい注文を受け取ったときの注文。 [!DNL Commerce] オーダーは、Amazonのステータスと在庫レベルに基づいて作成されます。</li></ul><br><br>`Enabled` でAmazonの注文を管理するために選択する必要があります [!DNL Commerce]. 条件 `Disabled` が選択されている場合、Amazonの注文はストアダッシュボードに表示されますが、注文は [!DNL Amazon Seller Central] アカウント |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 選択 [!DNL Commerce] Amazonの注文が [!DNL Commerce] [注文](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペース。 この設定のデフォルトは、 [!DNL Commerce] 選択された Web サイト [Amazonストアを追加しました](./store-integration.md). この設定を変更する場合は、オプションの一覧は [!DNL Commerce] には、設定で設定したが格納されます。 詳しくは、 [ストア](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | オプション：<ul><li>**[!UICONTROL No Customer Creation (guest)]** - （デフォルト） [!DNL Commerce] Amazon注文からインポートされた顧客データを使用する。 選択すると、このオプションはに通知します。 [!DNL Commerce] 読み込まれたAmazonの注文を、ゲストのチェックアウトの処理と同じ方法で処理する場合。</li><li>**[!UICONTROL Build New Customer Account]**  — 新しい顧客アカウントを作成するタイミングを [!DNL Commerce] Amazonの注文でインポートされた顧客データを使用する顧客データベース。 このオプションは、 [!DNL Commerce] Amazon注文の顧客データベース。</li></ul> |
| 注文番号のソース | オプション：<ul><li>**[!UICONTROL Build Using Magento Order Number]** - （デフォルト）一意の [!DNL Commerce] 対応するAmazon注文の注文番号 [!DNL Commerce] オーダー ID を段階的に割り当てます。 </li><li>**Amazon注文番号を使用してビルド**  — いつ作成するかを選択します。 [!DNL Commerce] 対応するAmazon割り当ての注文番号を使用した注文番号。</li></ul> |
| 保留中の注文 | オプション：<ul><li>**[!UICONTROL Do Not Reserve Quantity]**  — 不要な場合に選択 [!DNL Commerce] Amazonの注文の影響を受ける在庫数。 達成プロセス (FBA) にAmazonを使用する場合に選択します。 このオプションを選択してAmazonの注文を受け取った場合、注文された数量は [!DNL Commerce] 在庫数量。</li><li>**[!UICONTROL Reserve Quantity]** - Amazon注文の注文数量を「予約」するタイミングを [!DNL Commerce] 在庫数量。 選択され、Amazonの注文を受け取ると、注文された数量は、 [!DNL Commerce] 在庫数を防ぐために [!DNL Commerce] 「売り越し」からの在庫 「予約」数量は、 [!DNL Commerce] ストアフロント。</li></ul> |
| [!UICONTROL Order Status] | オプション：<ul><li>**[!UICONTROL Default Order Status]** - （デフォルト）Amazonからインポートされた新しく作成されたオーダーを、新しいオーダーのデフォルトのオーダーステータスに割り当てる場合に選択します。 （新しい注文のカスタム注文ステータスを作成していない限り）新しい注文のデフォルトのステータスは、次のとおりです。 `Pending`. 詳しくは、 [注文の処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** - Amazonから読み込まれた新しく作成されたオーダーに、デフォルト以外のステータスを割り当てる場合に選択します。 選択した場合、 **[!UICONTROL Processing Order Status]** では、Amazonからインポートされた新しく作成されたオーダーに使用するステータスを選択できます。</li></ul> |
| [!UICONTROL Processing Orders Status] | 有効： _[!UICONTROL Order Status]_が `Custom Order Status`. 新規受注に割り当てる受注ステータスを選択します。 このフィールドのオプションは、 [!DNL Commerce]. 詳しくは、 [注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). また、カスタムの注文ステータスを作成して、ここに表示することもできます。 カスタムの注文ステータスを作成するには、 [カスタム注文ステータス] |

## [!DNL Commerce] オーダーの作成

[!DNL Commerce] 注文は、次のステータスと在庫条件に基づいてAmazon注文に対して作成されます。

### Inventory managementでの注文作成

>[!NOTE]
>
>Adobe CommerceとMagento Open Source2.3.x の統合でのみサポートされます。

| 達成チャネル | [!DNL Commerce] 在庫ステータス | Amazon Order Status | [!UICONTROL Create Magento Order] 設定 | 予約済みの在庫 |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | 在庫<br>在庫切れ<br>管理しない | 保留中 | いいえ | いいえ |
| FBA | 在庫<br>在庫切れ<br>管理しない | PendingAvailability | いいえ | いいえ |
| FBA | 在庫<br>在庫切れ<br>管理しない | キャンセル | いいえ | いいえ |
| FBA | 在庫<br>在庫切れ<br>管理しない | エラー | いいえ | いいえ |
| FBA | 在庫<br>在庫切れ<br>管理しない | 未出荷 | いいえ | いいえ |
| FBA | 在庫<br>在庫切れ<br>管理しない | 部分的に出荷済み | いいえ | いいえ |
| FBA | 在庫<br>管理しない | 発送済み | はい | いいえ |
| FBA | 在庫切れ | 発送済み | いいえ | いいえ |
| FBM | 在庫<br>在庫切れ<br>管理しない | 保留中 | いいえ | いいえ |
| FBM | 在庫<br>在庫切れ<br>管理しない | PendingAvailability | いいえ | いいえ |
| FBM | 在庫<br>在庫切れ<br>管理しない | キャンセル | いいえ | いいえ |
| FBM | 在庫<br>在庫切れ<br>管理しない | エラー | いいえ | いいえ |
| FBM | 在庫<br>管理しない | 未出荷 | はい | はい |
| FBM | 在庫切れ | 未出荷 | いいえ | いいえ |
| FBM | 在庫<br>管理しない | 部分的に出荷済み | はい | はい |
| FBM | 在庫切れ | 部分的に出荷済み | いいえ | いいえ |
| FBM | 在庫<br>管理しない | 発送済み | はい | はい |
| FBM | 在庫切れ | 発送済み | いいえ | いいえ |

>[!NOTE]
>Amazonの注文が `Partially Shipped` または `Shipped` 「ステータス」の場合、作成される在庫予約は注文のすべての品目に対して行われます。 Amazonのセールスチャネルは、以前に出荷された品目を補正しません。
>
>注文がAmazon(FBA) で満たされたが、項目が `out of stock` ステータス [!DNL Commerce] は対応する注文を作成できません。 これは、Inventory management統合の制限です。
