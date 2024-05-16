---
title: Amazonの順序設定
description: 注文設定を使用して、Amazonの注文をCommerce ストアに読み込んで処理する方法を指定します。
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Amazonの順序設定

注文設定は、Amazonの注文をに読み込むかどうかと、どのように処理するかを定義するものです [!DNL Commerce] とにアクセスできます [ストアダッシュボード](./amazon-store-dashboard.md).

注文の読み込み設定がに設定されています。 `Enabled` デフォルトでは、Amazon注文がストアダッシュボードに表示され、対応するを作成します [!DNL Commerce] オーダー。 読み込まれた注文は、で管理できます。 [!DNL Commerce] [注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。

>[!NOTE]
>
>注文設定に関係なく、ストアインテグレーションの前に存在したAmazonの注文は読み込まれません。

後 [ストアの統合](./store-integration.md) が完了しました。注文の設定を変更できます。 注文設定をに設定した場合 `Disabled`、Amazonの注文はストアダッシュボードに表示されますが、 [!DNL Amazon Seller Central] アカウント。

Amazonで注文を作成しても、すぐには読み込まれません [!DNL Commerce]. Amazonがを割り当てる `Pending` 新しく作成された注文へのステータス。 Amazonが注文と支払い方法を確認すると、注文のステータスがに変更されます `Unshipped`. このステータスの変更は、注文のインポートをトリガーします。 [!DNL Commerce] 一致する、対応する順序を作成します。

Amazonから読み込んだ注文は、 [!DNL Commerce] [注文ワークフロー](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). 関連トピック [注文の管理](./managing-orders.md).

## 注文設定の指定 {#configure-order-settings}

1. クリック **[!UICONTROL Order Settings]** ストアダッシュボードで、次の操作を行います。

1. の場合 **[!UICONTROL Import Amazon Orders]** （必須）、次のいずれかのオプションを選択します。

   - `Disabled`  – 対応する注文をで作成しない場合に選択します [!DNL Commerce] Amazonから新しい注文を受け取った場合。 選択すると、このページのその他すべてのフィールドが無効になります。

   - `Enabled` - （デフォルト）対応するを作成するタイミングを選択します [!DNL Commerce] 注文：Amazonから新しい注文を受け取った場合。 [!DNL Commerce] 注文は、Amazonのステータスと在庫レベルに基づいて作成されます。

     >[!NOTE]
     >
     >Amazon注文のインポートはに設定する必要があります。 `Enabled` でAmazonの注文を管理するには [!DNL Commerce] [注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフロー。 に設定されている場合 `Disabled`に対応するAmazon注文がありません [!DNL Commerce] 注文番号で、で管理することはできません [!DNL Commerce]. これらの注文は以下で管理します [!DNL Amazon Seller Central] アカウント。

1. の場合 **[!UICONTROL Import Amazon Orders Into Magento Store]**、次から選択 [!DNL Commerce] 対応する注文がで作成されたときに関連付けられているAmazon注文を保存します。 [!DNL Commerce].

   この設定は、次の場合に選択した web サイトのストア表示をデフォルトとして指定します。 [がAmazon ストアを追加しました](./store-integration.md). この設定を変更する場合、オプションの一覧は [!DNL Commerce] 設定で設定したストア。 参照： [ストア](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. の場合 **[!UICONTROL Customer Creation]**、次のいずれかのオプションを選択します。

   - `No Customer Creation (guest)` - （デフォルト）で顧客アカウントを作成しない場合に選択します [!DNL Commerce] Amazon注文から読み込んだ顧客データを使用します。 選択した場合、 [!DNL Commerce] 読み込まれたAmazon注文の処理は、でのゲストチェックアウトの処理と同じです [!DNL Commerce].

   - `Build New Customer Account`  – で新しい顧客アカウントを作成するタイミングを選択します [!DNL Commerce] Amazonの注文で読み込んだ顧客データを使用します。 このオプションは、Amazonの注文からカスタマーデータベースを構築するのに役立ちます。

1. の場合 **[!UICONTROL Order Number Source]**、次のいずれかのオプションを選択します。

   - `Build Using Magento Order Number` - （デフォルト）一意のを作成するタイミングを選択します [!DNL Commerce] を使用した、対応するAmazon注文の注文番号 [!DNL Commerce] 増分的に割り当てられた注文 ID。

   - `Build Using Amazon Order Number`  – 作成するタイミングを選択します [!DNL Commerce] 注文番号：対応するAmazonが割り当てた注文番号を使用します。

   >[!NOTE]
   >
   >注文が読み込まれると、Amazonの注文番号がに表示されます _[!UICONTROL Recent Orders]_ストアダッシュボードに表示されます。 この [!DNL Commerce] で注文の詳細を表示すると、注文番号が表示される [!DNL Commerce] [注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペース。

1. の場合 **[!UICONTROL Order Status]** （必須）、次のいずれかのオプションを選択します。

   - `Default Order Status` - （デフォルト）Amazonからインポートされた新しく作成した注文を、新しい注文に対して定義したデフォルトの注文ステータスに割り当てる場合に選択します。 新しい注文のデフォルトのステータス（新しい注文のカスタム注文ステータスを作成した場合を除く）は、です。 `Pending`. 参照： [オーダーの処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Amazonから読み込まれた、新しく作成された注文に、デフォルト以外のステータスを割り当てる場合に選択します。

   - `Processing Order Status`  – 次の場合に有効 **[!UICONTROL Order Status]** はに設定されています。 `Custom Order Status`. Amazonから読み込んだ新しく作成された注文に使用するステータスを選択します。 このフィールドのオプションは、のデフォルトステータスオプションに基づいています [!DNL Commerce]. 参照： [注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). また、ここに表示されるカスタムの注文ステータスを作成して選択することもできます。 カスタム注文ステータスを作成するには、以下を参照してください [カスタム注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. 完了したら、 **[!UICONTROL Save order settings]**.

![オーダー設定](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | オプション：<ul><li>**[!UICONTROL Disabled]**  – 対応する注文をで作成しない場合に選択します [!DNL Commerce] Amazonから新しい注文を受け取った場合。 選択すると、このページのその他すべてのフィールドが無効になります。</li><li>**[!UICONTROL Enabled]** - （デフォルト）対応するを作成するタイミングを選択します [!DNL Commerce] 注文：Amazonから新しい注文を受け取った場合。 [!DNL Commerce] 注文は、Amazonのステータスと在庫レベルに基づいて作成されます。</li></ul><br><br>`Enabled` でAmazon注文を管理するように選択する必要があります [!DNL Commerce]. 条件 `Disabled` を選択すると、Amazonの注文がストアダッシュボードに表示されますが、注文は [!DNL Amazon Seller Central] アカウント。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | 次を選択 [!DNL Commerce] に作成された際に、関連付けられているAmazon注文を保存 [!DNL Commerce] [注文件数](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペース。 この設定は、デフォルトで次のストア表示になります。 [!DNL Commerce] 次の場合に選択された web サイト [がAmazon ストアを追加しました](./store-integration.md). この設定を変更する場合、オプションの一覧は [!DNL Commerce] 設定で設定したストア。 参照： [ストア](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | オプション：<ul><li>**[!UICONTROL No Customer Creation (guest)]** - （デフォルト）で顧客アカウントを作成しない場合に選択します [!DNL Commerce] Amazon注文から読み込んだ顧客データを使用します。 選択した場合、このオプションは次のように動作します [!DNL Commerce] 読み込んだAmazon注文をゲストチェックアウトと同じように処理するには：</li><li>**[!UICONTROL Build New Customer Account]**  – で新しい顧客アカウントを作成するタイミングを選択します [!DNL Commerce] Amazonの注文で読み込んだカスタマーデータを使用したカスタマーデータベース。 このオプションは、 [!DNL Commerce] Amazon注文の顧客データベース。</li></ul> |
| オーダー番号ソース | オプション：<ul><li>**[!UICONTROL Build Using Magento Order Number]** - （デフォルト）一意のを作成するタイミングを選択します [!DNL Commerce] を使用した、対応するAmazon注文の注文番号 [!DNL Commerce] 増分的に割り当てられた注文 ID。 </li><li>**Amazonの注文番号を使用してビルド**  – 作成するタイミングを選択します [!DNL Commerce] 注文番号：対応するAmazonが割り当てた注文番号を使用します。</li></ul> |
| 保留中の注文 | オプション：<ul><li>**[!UICONTROL Do Not Reserve Quantity]**  – 使用しないタイミングを選択します [!DNL Commerce] Amazonの注文の影響を受ける在庫数。 フルフィルメントプロセス（FBA）にAmazonを使用するかどうかを選択します。 このオプションを選択すると、Amazonの注文を受け取っても、注文数量はユーザーに影響しません [!DNL Commerce] 在庫数。</li><li>**[!UICONTROL Reserve Quantity]** - Amazon注文の注文数量をユーザーの「予約済み」にするタイミングを選択します [!DNL Commerce] 在庫数。 このオプションを選択すると、Amazonからのご注文を受け取った際に、ご注文の数量が「予約」されます [!DNL Commerce] を防ぐための在庫数 [!DNL Commerce] 「オーバーセラー」からの在庫。 「予約済み」の数量は、を通じて購入することはできません [!DNL Commerce] ストアフロント。</li></ul> |
| [!UICONTROL Order Status] | オプション：<ul><li>**[!UICONTROL Default Order Status]** - （デフォルト）Amazonからインポートされた新しく作成した注文を、新しい注文のデフォルトの注文ステータスに割り当てるタイミングを選択します。 新しい注文のデフォルトのステータス（新しい注文のカスタム注文ステータスを作成した場合を除く）は、です。 `Pending`. 参照： [オーダーの処理](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** - Amazonから読み込まれた、新しく作成された注文に、デフォルト以外のステータスを割り当てる場合に選択します。 選択した場合、 **[!UICONTROL Processing Order Status]** を使用すると、Amazonから読み込まれた新しく作成された注文に使用するステータスを選択できます。</li></ul> |
| [!UICONTROL Processing Orders Status] | 有効な条件 _[!UICONTROL Order Status]_はに設定されています。 `Custom Order Status`. 新しい注文に割り当てる注文ステータスを選択します。 このフィールドのオプションは、のデフォルトステータスオプションによって異なります [!DNL Commerce]. 参照： [注文ステータス](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). ここに表示するカスタムの注文ステータスを作成することもできます。 カスタム注文ステータスを作成するには、以下を参照してください [カスタム注文ステータス] |

## [!DNL Commerce] オーダーの作成

[!DNL Commerce] 注文は、次のステータスと在庫条件に基づいて、Amazon注文に対して作成されます。

### Inventory managementでのオーダー作成

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source 2.3.x 統合でのみサポートされます。

| フルフィルメントチャネル | [!DNL Commerce] 在庫ステータス | Amazon注文ステータス | [!UICONTROL Create Magento Order] 設定 | 予約済み在庫 |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | 在庫<br>在庫切れ<br>管理しない | 保留中 | 不可 | 不可 |
| FBA | 在庫<br>在庫切れ<br>管理しない | PendingAvailability | 不可 | 不可 |
| FBA | 在庫<br>在庫切れ<br>管理しない | キャンセル済み | 不可 | 不可 |
| FBA | 在庫<br>在庫切れ<br>管理しない | エラー | 不可 | 不可 |
| FBA | 在庫<br>在庫切れ<br>管理しない | 未出荷 | 不可 | 不可 |
| FBA | 在庫<br>在庫切れ<br>管理しない | 一部出荷済み | 不可 | 不可 |
| FBA | 在庫<br>管理しない | 出荷済み | はい | 不可 |
| FBA | 在庫切れ | 出荷済み | 不可 | 不可 |
| FBM | 在庫<br>在庫切れ<br>管理しない | 保留中 | 不可 | 不可 |
| FBM | 在庫<br>在庫切れ<br>管理しない | PendingAvailability | 不可 | 不可 |
| FBM | 在庫<br>在庫切れ<br>管理しない | キャンセル済み | 不可 | 不可 |
| FBM | 在庫<br>在庫切れ<br>管理しない | エラー | 不可 | 不可 |
| FBM | 在庫<br>管理しない | 未出荷 | はい | はい |
| FBM | 在庫切れ | 未出荷 | 不可 | 不可 |
| FBM | 在庫<br>管理しない | 一部出荷済み | はい | はい |
| FBM | 在庫切れ | 一部出荷済み | 不可 | 不可 |
| FBM | 在庫<br>管理しない | 出荷済み | はい | はい |
| FBM | 在庫切れ | 出荷済み | 不可 | 不可 |

>[!NOTE]
>Amazon注文がに読み込まれる場合 `Partially Shipped` または `Shipped` ステータス。作成される在庫引当は、注文のすべての品目に対して行われます。 Amazonの営業チャネルは、以前に出荷された商品を補償しません。
>
>注文がAmazon（FBA）で履行されたが、品目が次の場所にある場合 `out of stock` ステータス、 [!DNL Commerce] 対応する注文を作成できません。 これは、Inventory management統合の制限事項です。
