---
title: オーダー設定
description: 注文設定を使用して、Amazon の注文が Commerce ストアにどのようにインポートされ、処理されるかを指定します。
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# オーダー設定

注文設定によって、Amazon の注文がでどのようにインポートおよび処理され、 [!DNL Commerce] ストアのダッシュボードでアクセスできるかを定義し [ ](./amazon-store-dashboard.md) ます。

注文のインポート設定は、 `Enabled` 初期設定では、その Amazon の注文がストアのダッシュボードに表示され、対応する注文が作成され [!DNL Commerce] ます。 インポートされた注文は、 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} という注文で管理できます。

>[!NOTE]
>
>注文の設定にかかわらず、store 統合前に存在していた Amazon の注文はインポートされません。

[ストアの統合 ](./store-integration.md) が完了したら、注文の設定を変更することができます。オーダー設定をに設定した場合 `Disabled` は、Amazon orders が store ダッシュボードに表示されますが、自分のアカウントで管理されている必要があり [!DNL Amazon Seller Central] ます。

Amazon によって注文が作成されたときに、その注文がに直ちに読み込まれることはありません [!DNL Commerce] 。 Amazon は、 `Pending` 新しく作成された注文に状態を割り当てます。 Amazon によって注文と支払方法が確認されると、注文のステータスがに変更され `Unshipped` ます。 この状態変更により、注文のインポートが開始され、 [!DNL Commerce] 対応する注文が作成されます。

Amazon からインポートされた注文は、 [!DNL Commerce] [ orders workflow ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} で管理できます。 「 [ 注文の管理」も参照してください ](./managing-orders.md) 。

## 注文設定の設定 {#configure-order-settings}

1. **[!UICONTROL Order Settings]** Store のダッシュボードのをクリックします。

1. **[!UICONTROL Import Amazon Orders]**(必須) には、次のいずれかのオプションを選択します。

   - `Disabled` -Amazon から新しい注文を受け取る際に、対応する注文を作成しない場合に選択し [!DNL Commerce] ます。 この設定を選択すると、このページの他のフィールドはすべて無効になります。

   - `Enabled` -(デフォルト) [!DNL Commerce] Amazon から新しい注文を受け取る際に、対応する注文を作成するかどうかを選択します。 [!DNL Commerce] 注文は、Amazon の状態と在庫レベルに基づいて作成されます。

      >[!NOTE]
      >
      >Amazon Orders のインポートは `Enabled` 、 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} という注文の amazon orders を管理するように設定されている必要があります。 に設定されている場合 `Disabled` 、Amazon orders には対応する注文番号がなく、 [!DNL Commerce] で管理することはできません [!DNL Commerce] 。 これらの注文は、 [!DNL Amazon Seller Central] 取引先企業で管理します。

1. については **[!UICONTROL Import Amazon Orders Into Magento Store]** 、 [!DNL Commerce] で、対応する注文を作成したときに Amazon 注文が関連付けられる店舗を選択 [!DNL Commerce] します。

   この設定は、Amazon Store を追加したときに選択された web サイトのストアビューにデフォルト設定され [ ](./store-integration.md) ます。 この設定を変更する必要がある場合は、設定に設定されているストアによってオプションの一覧が表示され [!DNL Commerce] ます。 [ストア ](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view) {target = &quot;_blank&quot;} を参照してください。

1. **[!UICONTROL Customer Creation]**&#x200B;で、次のいずれかのオプションを選択します。

   - `No Customer Creation (guest)` -(デフォルト) [!DNL Commerce] Amazon の注文からインポートされた顧客データを使用して、ユーザーアカウントを作成しない場合は、このオプションを選択します。 選択すると、 [!DNL Commerce] 読み込まれた Amazon 命令は、でゲストのチェックアウトを処理するのと同じように処理さ [!DNL Commerce] れます。

   - `Build New Customer Account` - [!DNL Commerce] Amazon の注文によって読み込まれたカスタマーデータを使用して、で新しい顧客アカウントを作成する場合に選択します。 このオプションを選択すると、Amazon の注文から顧客データベースを構築するのに役立ちます。

1. **[!UICONTROL Order Number Source]**&#x200B;で、次のいずれかのオプションを選択します。

   - `Build Using Magento Order Number` -(デフォルト) [!DNL Commerce] インクリメンタルに割り当てられた注文 ID を使用して、対応する Amazon 注文に対して固有の注文番号を作成する場合に選択し [!DNL Commerce] ます。

   - `Build Using Amazon Order Number` -対応する Amazon i によっ [!DNL Commerce] て割り当てられた注文番号を使用して、注文番号を作成する場合に選択します。
   >[!NOTE]
   >
   >注文のインポートが完了すると、Amazon の注文番号が store のダッシュボードのリストに表示され _[!UICONTROL Recent Orders]_ます。 注文 [!DNL Commerce] 番号が表示されるときに、注文の詳細が [!DNL Commerce] [ ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} ワークスペースに表示されます。

1. **[!UICONTROL Order Status]**(必須) には、次のいずれかのオプションを選択します。

   - `Default Order Status` -(デフォルト) Amazon から新しく作成された注文に、新しい注文の定義済みのデフォルトの注文状態が割り当てられるようにするには、このオプションを選択します。 新しい注文のデフォルトの状態 (新しい注文の注文状況を独自に作成している場合を除きます) が表示され `Pending` ます。 「 [ 注文処理 ](https://docs.magento.com/user-guide/sales/order-processing.html) {target = &quot;_blank&quot;}」を参照してください。

   - `Custom Order Status` -Amazon から新しく作成された注文にデフォルト以外の状態が割り当てられるようにする場合に選択します。

   - `Processing Order Status` -「」 **[!UICONTROL Order Status]** に設定されている場合は有効になり `Custom Order Status` ます。 Amazon からインポートされた、新しく作成された注文に使用する状態を選択します。 このフィールドのオプションは、のデフォルトのステータスオプションに基づいてい [!DNL Commerce] ます。 「 [ 注文状況」を参照してください ](https://docs.magento.com/user-guide/sales/order-status.html) 。 ここに選択した場合は、独自の注文状況を作成することもできます。 注文状況を独自に設定する方法については、「カスタム注文状況」を参照してください ( [ ](https://docs.magento.com/user-guide/sales/order-status-custom.html) {target = &quot;_blank&quot;})。

1. 完了したら、をクリックし **[!UICONTROL Save order settings]** ます。

![オーダー設定](assets/amazon-order-settings.png)

| 名 | つい |
|---|---|
| [!UICONTROL Import Amazon Orders] | オプション：<ul><li>**[!UICONTROL Disabled]** -Amazon から新しい注文を受け取る際に、対応する注文を作成しない場合に選択し [!DNL Commerce] ます。 この設定を選択すると、このページの他のフィールドはすべて無効になります。</li><li>**[!UICONTROL Enabled]** -(デフォルト) [!DNL Commerce] Amazon から新しい注文を受け取る際に、対応する注文を作成するかどうかを選択します。 [!DNL Commerce] 注文は、Amazon の状態と在庫レベルに基づいて作成されます。</li></ul><br><br>`Enabled` で Amazon 命令を管理するために選択する必要があり [!DNL Commerce] ます。 `Disabled`を選択した場合は、Amazon の注文が store のダッシュボードに表示されますが、注文は自分のアカウントで管理する必要があり [!DNL Amazon Seller Central] ます。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | このような場合は、 [!DNL Commerce] Amazon orders が [!DNL Commerce] [ 注文 ](https://docs.magento.com/user-guide/sales/orders.html) {target = &quot;_blank&quot;} ワークスペースで作成されたときにどのストアに関連付けられるかを選択します。 この設定は、Amazon Store を追加したときに選択された web サイトのストアビューにデフォルト設定 [!DNL Commerce] され [ ](./store-integration.md) ます。 この設定を変更する必要がある場合は、設定に設定されているストアによってオプションの一覧が表示され [!DNL Commerce] ます。 [ストア ](https://docs.magento.com/user-guide/stores/stores-all-stores.html) {target = &quot;_blank&quot;} を参照してください。 |
| [!UICONTROL Customer Creation] | オプション：<ul><li>**[!UICONTROL No Customer Creation (guest)]** -(デフォルト) [!DNL Commerce] Amazon の注文からインポートされた顧客データを使用して、ユーザーアカウントを作成しない場合は、このオプションを選択します。 このオプションを選択すると、 [!DNL Commerce] ゲストのチェックアウトを処理するのと同じように、読み込まれた Amazon 注文が処理されます。</li><li>**[!UICONTROL Build New Customer Account]** - [!DNL Commerce] Amazon の注文によって読み込まれたカスタマーデータを使用して、顧客データベースに新しい顧客アカウントを作成する場合に選択します。 このオプション [!DNL Commerce] を選択すると、Amazon の注文から顧客データベースを構築するのに役立ちます。</li></ul> |
| 注文番号ソース | オプション：<ul><li>**[!UICONTROL Build Using Magento Order Number]** -(デフォルト) [!DNL Commerce] インクリメンタルに割り当てられた注文 ID を使用して、対応する Amazon 注文に対して固有の注文番号を作成する場合に選択し [!DNL Commerce] ます。 </li><li>**Amazon Order Number を使用して構築** - [!DNL Commerce] 対応する Amazon i によって割り当てられた注文番号を使用して注文番号を作成する場合に選択します。</li></ul> |
| 受注待ち | オプション：<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - [!DNL Commerce] Amazon の注文によって在庫数が対象とならない場合に選択します。 利用手続き (FBA) に Amazon を使用するかどうかを選択します。 この設定を選択すると、Amazon の注文を受信したときに注文数が手持ち在庫数に影響することはありません [!DNL Commerce] 。</li><li>**[!UICONTROL Reserve Quantity]** このオプションを選択すると、その在庫量に Amazon の注文数量を &quot;引当&quot; することができ [!DNL Commerce] ます。 この設定を選択すると、Amazon の注文を受信したときに、注文数が在庫量に「予約」され、「販売超過」が発生し [!DNL Commerce] ないようにすることができ [!DNL Commerce] ます。 「予約」数量は、店頭で購入することはできません [!DNL Commerce] 。</li></ul> |
| [!UICONTROL Order Status] | オプション：<ul><li>**[!UICONTROL Default Order Status]** -(デフォルト) Amazon から新しく作成された注文に、新しい注文のデフォルトの注文状態が割り当てられるようにするには、このオプションを選択します。 新しい注文のデフォルトの状態 (新しい注文の注文状況を独自に作成している場合を除きます) が表示され `Pending` ます。 「注文処理」を参照してください [ ](https://docs.magento.com/user-guide/sales/order-processing.html) 。</li><li>> **[!UICONTROL Custom Order Status]** -Amazon から新しく作成された注文にデフォルト以外の状態が割り当てられるようにするには、「選択」を選択します。 このオプションを選択すると、Amazon によって **[!UICONTROL Processing Order Status]** 読み込まれる新しく作成された注文に使用する状態を選択できます。</li></ul> |
| [!UICONTROL Processing Orders Status] | 「」 _[!UICONTROL Order Status]_に設定されている場合、有効になり `Custom Order Status` ます。 新しい注文に割り当てる注文状態を選択します。 このフィールドのオプションは、のデフォルトの状態オプションによって異なり [!DNL Commerce] ます。 オーダー状態を確認してください ( [ ](https://docs.magento.com/user-guide/sales/order-status.html) {target = &quot;_blank&quot;})。 ここに表示されるカスタム注文状態を作成することもできます。 注文状況を独自に設定する方法については、「カスタム注文状況」を参照してください ( [ ](https://docs.magento.com/user-guide/sales/order-status-custom.html) {target = &quot;_blank&quot;})。 |

## [!DNL Commerce] 注文の作成

[!DNL Commerce] 次の状態とインベントリ条件に基づいて、Amazon の注文用に注文が作成されます。

### 在庫管理を使用した注文作成

>[!NOTE]
>
>Adobe Commerce および Magento Open Source 2.3 x 統合のみがサポートされています。

| フルフィルメントチャネル | [!DNL Commerce] インベントリの状態 | Amazon の注文状況 | [!UICONTROL Create Magento Order] , | 予約されたインベントリ |
|---|---|---|---|---|
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | 状態 | 違います | 違います |
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | PendingAvailability | 違います | 違います |
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | キャンセルされ | 違います | 違います |
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | 中 | 違います | 違います |
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | 未出荷 | 違います | 違います |
| FBA | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | PartiallyShipped | 違います | 違います |
| FBA | 在庫 <br> 管理なし | 付属 | うん | 違います |
| FBA | 在庫切れ | 付属 | 違います | 違います |
| FBM | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | 状態 | 違います | 違います |
| FBM | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | PendingAvailability | 違います | 違います |
| FBM | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | キャンセルされ | 違います | 違います |
| FBM | 在庫不足の在庫 <br> 管理機能が <br> ありません。 | 中 | 違います | 違います |
| FBM | 在庫 <br> 管理なし | 未出荷 | うん | うん |
| FBM | 在庫切れ | 未出荷 | 違います | 違います |
| FBM | 在庫 <br> 管理なし | PartiallyShipped | うん | うん |
| FBM | 在庫切れ | PartiallyShipped | 違います | 違います |
| FBM | 在庫 <br> 管理なし | 付属 | うん | うん |
| FBM | 在庫切れ | 付属 | 違います | 違います |

>[!NOTE]
>Amazon の注文がまたは状態でインポートされた場合は、 `Partially Shipped` `Shipped` 作成される在庫引当は、注文内のすべてのアイテムに対して作成されます。 Amazon 販売チャンネルは、既に出荷されている品目については補正しません。
>
>Amazon (FBA) によって注文が満たされているにもかかわらず、そのアイテムが状態になっていると `out of stock` 、それ [!DNL Commerce] に対応する順序を作成することができません。 これは、在庫管理統合の制限事項です。
