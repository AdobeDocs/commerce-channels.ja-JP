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

注文設定は、Amazonの注文を [!DNL Commerce] にインポートして処理するかどうかと、その方法を定義し、[ ストアダッシュボード ](./amazon-store-dashboard.md) からアクセスできるようにします。

注文の読み込み設定はデフォルトで `Enabled` に設定されています。つまり、Amazonの注文がストアダッシュボードに表示され、対応する [!DNL Commerce] 注文が作成されます。 読み込まれた注文は、[!DNL Commerce] [ 注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフローで管理できます。

>[!NOTE]
>
>注文設定に関係なく、ストアインテグレーションの前に存在したAmazonの注文は読み込まれません。

[ ストアの統合 ](./store-integration.md) が完了したら、注文設定を変更できます。 注文設定を `Disabled` に設定した場合、Amazon注文はストアダッシュボードに表示されますが、[!DNL Amazon Seller Central] アカウントで管理する必要があります。

Amazonで注文を作成しても、すぐには [!DNL Commerce] に読み込まれません。 Amazonは、新しく作成された注文に `Pending` ステータスを割り当てます。 Amazonが注文と支払い方法を確認すると、注文のステータスが `Unshipped` に変更されます。 このステータスの変化は、注文のインポートをトリガーし、一致 [!DNL Commerce] る対応する注文を作成します。

Amazonから読み込まれた注文は、[!DNL Commerce][ 注文ワークフロー ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) で管理できます。 [ 注文の管理 ](./managing-orders.md) も参照してください。

## 注文設定の指定 {#configure-order-settings}

1. ストアダッシュボードで「**[!UICONTROL Order Settings]**」をクリックします。

1. **[!UICONTROL Import Amazon Orders]** （必須）には、次のいずれかのオプションを選択します。

   - `Disabled` – 対応する注文をAmazonで作成しない場合 [!DNL Commerce]、新しい注文をから受け取る場合に選択します。 選択すると、このページのその他すべてのフィールドが無効になります。

   - `Enabled` - （デフォルト）Amazonから新しい注文を受け取ったときに、対応する [!DNL Commerce] 注文を作成するタイミングを選択します。 注文 [!DNL Commerce]、Amazonのステータスと在庫レベルに基づいて作成されます。

     >[!NOTE]
     >
     >Amazon注文のインポートは、[!DNL Commerce] [ 注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークフローでAmazon注文を管理するために `Enabled` に設定されている必要があります。 `Disabled` に設定すると、Amazon注文に対応する [!DNL Commerce] 注文番号が付かず、[!DNL Commerce] で管理できません。 これらの注文は [!DNL Amazon Seller Central] アカウントで管理します。

1. **[!UICONTROL Import Amazon Orders Into Magento Store]**：対応する注文が [!DNL Commerce] で作成されるときに、Amazonの注文が関連付けられている [!DNL Commerce] ージを選択します。

   この設定は、デフォルトでは、（Amazon ストアを追加した [ 際に選択した web サイトのストアビューにな ](./store-integration.md) ます。 この設定を変更する場合、オプションの一覧は、構成で設定した [!DNL Commerce] ストアによって異なります。 [ ストア ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) を参照してください。

1. **[!UICONTROL Customer Creation]** の場合は、次のいずれかのオプションを選択します。

   - `No Customer Creation (guest)` - （デフォルト）Amazon注文から読み込んだ顧客データを使用して [!DNL Commerce] で顧客アカウントを作成しない場合に選択します。 これを選択すると、読み込まれたAmazonの注文が、[!DNL Commerce] でのゲストのチェックアウトと同じように [!DNL Commerce] で処理されます。

   - `Build New Customer Account` - Amazonの注文で読み込んだ顧客データを使用して、[!DNL Commerce] で新しい顧客アカウントを作成するタイミングを選択します。 このオプションは、Amazonの注文からカスタマーデータベースを構築するのに役立ちます。

1. **[!UICONTROL Order Number Source]** の場合は、次のいずれかのオプションを選択します。

   - `Build Using Magento Order Number` - （デフォルト） [!DNL Commerce] の増分割り当て済み注文 ID を使用して、対応するAmazon注文に一意の [!DNL Commerce] 注番号を作成する場合に選択します。

   - `Build Using Amazon Order Number` – 対応するAmazonが割り当てた注文番号を使用して、[!DNL Commerce] 注番号を作成するタイミングを選択します。

   >[!NOTE]
   >
   >注文が読み込まれると、Amazonの注文番号がストアダッシュボードの _[!UICONTROL Recent Orders]_リストに表示されます。 [!DNL Commerce] [ 注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペースで注文の詳細を表示すると、[!DNL Commerce] 注番号が表示されます。

1. **[!UICONTROL Order Status]** （必須）には、次のいずれかのオプションを選択します。

   - `Default Order Status` - （デフォルト）Amazonからインポートされた新しく作成した注文を、新しい注文に対して定義されたデフォルトの注文ステータスに割り当てる場合に選択します。 新しい注文のデフォルトのステータスは `Pending` です（新しい注文のカスタム注文ステータスを作成した場合を除く）。 [ オーダーの処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) を参照してください。

   - `Custom Order Status` - Amazonから読み込んだ新しく作成した注文に、デフォルト以外のステータスを割り当てるタイミングを選択します。

   - `Processing Order Status` - **[!UICONTROL Order Status]** が `Custom Order Status` に設定されている場合に有効になります。 Amazonから読み込んだ新しく作成された注文に使用するステータスを選択します。 このフィールドのオプションは、[!DNL Commerce] のデフォルトステータスオプションに基づいています。 [ 注文ステータス ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html) を参照してください。 また、ここに表示されるカスタムの注文ステータスを作成して選択することもできます。 カスタム注文ステータスを作成するには、[ カスタム注文ステータス ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status) を参照してください。

1. 完了したら、「**[!UICONTROL Save order settings]**」をクリックします。

![ 順序設定 ](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | オプション：<ul><li>**[!UICONTROL Disabled]** – 対応する注文をAmazonで作成しない場合 [!DNL Commerce]、新しい注文をから受け取る場合に選択します。 選択すると、このページのその他すべてのフィールドが無効になります。</li><li>**[!UICONTROL Enabled]** - （デフォルト）Amazonから新しい注文を受け取ったときに、対応する [!DNL Commerce] 注文を作成するタイミングを選択します。 注文 [!DNL Commerce]、Amazonのステータスと在庫レベルに基づいて作成されます。</li></ul>Amazonの注文を [!DNL Commerce] で管理するために、<br><br>`Enabled` を選択する必要があります。 `Disabled` を選択すると、Amazonの注文がストアダッシュボードに表示されますが、注文は [!DNL Amazon Seller Central] アカウントで管理する必要があります。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Amazonの注文が [!DNL Commerce] [ 注文 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) ワークスペースで作成されたときに関連付けられている [!DNL Commerce] ージを選択します。 この設定は、デフォルトで、（Amazon ストアを追加した [ ときに選択した [!DNL Commerce] の web サイトのストアビュー ](./store-integration.md) なります。 この設定を変更する場合、オプションの一覧は、構成で設定した [!DNL Commerce] ストアによって異なります。 [ ストア ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html) を参照してください。 |
| [!UICONTROL Customer Creation] | オプション：<ul><li>**[!UICONTROL No Customer Creation (guest)]** - （デフォルト）Amazon注文から読み込んだ顧客データを使用して [!DNL Commerce] で顧客アカウントを作成しない場合に選択します。 これを選択すると、読み込 [!DNL Commerce] れたAmazon注文をゲストのチェックアウトと同じ方法で処理するように指示されます。</li><li>**[!UICONTROL Build New Customer Account]** - Amazonの注文で読み込んだ顧客データを使用して、[!DNL Commerce] 顧客データベースに新しい顧客アカウントを作成するタイミングを選択します。 このオプションは、Amazonの注文から [!DNL Commerce] 顧客データベースを作成するのに役立ちます。</li></ul> |
| 注文番号Source | オプション：<ul><li>**[!UICONTROL Build Using Magento Order Number]** - （デフォルト） [!DNL Commerce] の増分割り当て済み注文 ID を使用して、対応するAmazon注文に一意の [!DNL Commerce] 注番号を作成する場合に選択します。 </li><li>**Amazon注文番号を使用して作成** – 対応するAmazonに割り当てられた注文番号を使用して [!DNL Commerce] 注番号を作成する場合に選択します。</li></ul> |
| 保留中の注文 | オプション：<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Amazonの注文によって [!DNL Commerce] の在庫数に影響を与えたくない場合に選択します。 フルフィルメントプロセス（FBA）にAmazonを使用するかどうかを選択します。 このオプションを選択すると、Amazonの注文を受け取っても、注文数量は [!DNL Commerce] 入在庫数量に影響を与えません。</li><li>**[!UICONTROL Reserve Quantity]** - Amazon注文の注文数量を、[!DNL Commerce] しい在庫数量で「予約済み」にするタイミングを選択します。 このオプションを選択すると、Amazonの注文を受け取った場合、注文数量は [!DNL Commerce] の在庫数量で「予約」され、[!DNL Commerce] の在庫が「売り過ぎ」するのを防ぎます。 [!DNL Commerce] ストアフロントでは、「予約済み」の数量を購入できません。</li></ul> |
| [!UICONTROL Order Status] | オプション：<ul><li>**[!UICONTROL Default Order Status]** - （デフォルト）Amazonからインポートされた新しく作成した注文を、新しい注文のデフォルトの注文ステータスに割り当てるタイミングを選択します。 新しい注文のデフォルトのステータスは `Pending` です（新しい注文のカスタム注文ステータスを作成した場合を除く）。 [ オーダーの処理 ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) を参照してください。</li><li>**[!UICONTROL Custom Order Status]** - Amazonから読み込んだ新しく作成した注文に、デフォルト以外のステータスを割り当てるタイミングを選択します。 これを選択す **[!UICONTROL Processing Order Status]** と、Amazonから読み込んだ、新しく作成された注文に使用するステータスを選択できます。</li></ul> |
| [!UICONTROL Processing Orders Status] | _[!UICONTROL Order Status]_が `Custom Order Status` に設定されている場合に有効になります。 新しい注文に割り当てる注文ステータスを選択します。 このフィールドのオプションは、[!DNL Commerce] のデフォルトステータスオプションによって異なります。 [ 注文ステータス ](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html) を参照してください。 ここに表示するカスタムの注文ステータスを作成することもできます。 カスタム注文ステータスを作成するには、[ カスタム注文ステータス ] を参照してください |

## [!DNL Commerce] 注文の作成

Amazonの注文に対する [!DNL Commerce] の注文は、次のステータスと在庫条件に基づいて作成されます。

### Inventory managementでのオーダー作成

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Source 2.3.x 統合でのみサポートされます。

| フルフィルメントチャネル | [!DNL Commerce] 在庫ステータス | Amazon注文ステータス | [!UICONTROL Create Magento Order] 設定 | 予約済み在庫 |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | 保留中 | 不可 | 不可 |
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | PendingAvailability | 不可 | 不可 |
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | キャンセル済み | 不可 | 不可 |
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | エラー | 不可 | 不可 |
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | 未出荷 | 不可 | 不可 |
| FBA | 在庫 <br> 在庫切れ <br> 管理しない | 一部出荷済み | 不可 | 不可 |
| FBA | 在庫中 <br> 管理しない | 出荷済み | はい | 不可 |
| FBA | 在庫切れ | 出荷済み | 不可 | 不可 |
| FBM | 在庫 <br> 在庫切れ <br> 管理しない | 保留中 | 不可 | 不可 |
| FBM | 在庫 <br> 在庫切れ <br> 管理しない | PendingAvailability | 不可 | 不可 |
| FBM | 在庫 <br> 在庫切れ <br> 管理しない | キャンセル済み | 不可 | 不可 |
| FBM | 在庫 <br> 在庫切れ <br> 管理しない | エラー | 不可 | 不可 |
| FBM | 在庫中 <br> 管理しない | 未出荷 | はい | はい |
| FBM | 在庫切れ | 未出荷 | 不可 | 不可 |
| FBM | 在庫中 <br> 管理しない | 一部出荷済み | はい | はい |
| FBM | 在庫切れ | 一部出荷済み | 不可 | 不可 |
| FBM | 在庫中 <br> 管理しない | 出荷済み | はい | はい |
| FBM | 在庫切れ | 出荷済み | 不可 | 不可 |

>[!NOTE]
>Amazonの注文が `Partially Shipped` または `Shipped` ステータスでインポートされた場合、作成される在庫引当は、注文に含まれるすべての品目に対して行われます。 Amazonの営業チャネルは、以前に出荷された商品を補償しません。
>
>注文がAmazon（FBA）によって履行されているが、品目ステータスが `out of stock` の場合、対応す [!DNL Commerce] 注文を作成することはできません。 これは、Inventory management統合の制限事項です。
