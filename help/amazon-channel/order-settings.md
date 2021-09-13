---
title: 順序の設定
description: 注文の設定を使用して、Amazonの注文をコマースストアにインポートして処理する方法を決定します。
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# 順序の設定

注文の設定は、Amazonの注文を[!DNL Commerce]でインポートおよび処理するかどうかと方法を定義し、[ストアダッシュボード](./amazon-store-dashboard.md)でアクセスできるようにします。

注文のインポート設定はデフォルトで`Enabled`に設定されています。つまり、Amazonの注文がストアのダッシュボードに表示され、対応する[!DNL Commerce]注文が作成されます。 インポートされたオーダーは、[!DNL Commerce] [オーダー](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}ワークフローで管理できます。

>[!NOTE]
>
>注文の設定に関係なく、ストア統合前に存在していたAmazonの注文はインポートされません。

[ストア統合](./store-integration.md)が完了したら、注文の設定を変更できます。 注文の設定を`Disabled`に設定した場合、Amazonの注文はストアダッシュボードに表示されますが、[!DNL Amazon Seller Central]アカウントで管理する必要があります。

注文がAmazon上で作成されても、すぐに[!DNL Commerce]に読み込まれるわけではありません。 Amazonは、新しく作成された注文に`Pending`ステータスを割り当てます。 Amazonが注文と支払い方法を確認すると、注文のステータスが`Unshipped`に変更されます。 このステータスは、注文のインポートをトリガーし、[!DNL Commerce]は対応する順序を作成します。

Amazonからインポートされた注文は、[!DNL Commerce] [orders workflow](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}で管理できます。 [注文の管理](./managing-orders.md)も参照してください。

## 注文の設定 {#configure-order-settings}

1. ストアダッシュボードの「**[!UICONTROL Order Settings]**」をクリックします。

1. **[!UICONTROL Import Amazon Orders]**（必須）には、次のオプションを選択します。

   - `Disabled` - Amazonから新しい注文を受け取る際に、対応する注文をで作 [!DNL Commerce] 成しない場合に選択します。選択すると、このページ上の他のすべてのフィールドは無効になります。

   - `Enabled` - （デフォルト）Amazonから新しい注文を受け取った場合に、対応 [!DNL Commerce] する注文を作成するタイミングを選択します。[!DNL Commerce] オーダーは、Amazonのステータスと在庫レベルに基づいて作成されます。

      >[!NOTE]
      >
      >[!DNL Commerce] [orders](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}ワークフローでAmazonのオーダーを管理するには、Amazonのオーダーを`Enabled`に設定する必要があります。 `Disabled`に設定すると、Amazonの注文には対応する[!DNL Commerce]注文番号がなく、[!DNL Commerce]で管理できません。 これらの注文は[!DNL Amazon Seller Central]アカウントで管理します。

1. **[!UICONTROL Import Amazon Orders Into Magento Store]**&#x200B;の場合、[!DNL Commerce]内に対応する注文が作成されたときに、Amazon注文を関連付ける[!DNL Commerce]を選択します。

   この設定のデフォルト値は、Amazonストア](./store-integration.md)を[追加したときに選択したWebサイトのストア表示です。 この設定を変更する場合、オプションのリストは、設定した[!DNL Commerce]ストアによって異なります。 [ストア](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}を参照してください。

1. **[!UICONTROL Customer Creation]**&#x200B;の場合は、次のオプションを選択します。

   - `No Customer Creation (guest)` - （デフォルト） Amazonの注文からインポートした顧客データを使用してで顧客ア [!DNL Commerce] カウントを作成しない場合に選択します。選択すると、[!DNL Commerce]は、[!DNL Commerce]でのゲストチェックアウトの処理と同じ方法で、インポートされたAmazonの注文を処理します。

   - `Build New Customer Account` - Amazonの注文でインポートした顧客データを使用して、で新し [!DNL Commerce] い顧客アカウントを作成するタイミングを選択します。このオプションは、Amazonの注文内容から顧客データベースを作成するのに役立ちます。

1. **[!UICONTROL Order Number Source]**&#x200B;の場合は、次のオプションを選択します。

   - `Build Using Magento Order Number` - （デフォルト）増分的に割り当てられた注文IDを使用して、対応するAmazon [!DNL Commerce] 注文に対して一意の注文番号を作成する [!DNL Commerce] 場合に選択します。

   - `Build Using Amazon Order Number`  — 対応するAmazon割り当ての注文番号を使 [!DNL Commerce] 用して注文番号を作成する場合に選択します。
   >[!NOTE]
   >
   >注文が読み込まれると、Amazonの注文番号がストアダッシュボードの&#x200B;_[!UICONTROL Recent Orders]_リストに表示されます。 [!DNL Commerce]注文番号は、[!DNL Commerce] [注文](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}ワークスペースで注文の詳細を表示する際に表示されます。

1. **[!UICONTROL Order Status]**（必須）には、次のオプションを選択します。

   - `Default Order Status`  — （デフォルト）Amazonからインポートされた新規作成オーダーに、新規オーダーに対して定義済のデフォルトオーダー・ステータスを割り当てる場合に選択します。（新しい注文のカスタム注文ステータスを作成していない限り）新しい注文のデフォルトのステータスは`Pending`です。 [処理注文](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}を参照してください。

   - `Custom Order Status` - Amazonから読み込まれた新しく作成された注文にデフォルト以外のステータスを割り当てる場合に選択します。

   - `Processing Order Status`  — がに設定されてい **[!UICONTROL Order Status]** る場合は有効で `Custom Order Status`す。Amazonからインポートされた新しく作成された注文に使用するステータスを選択します。 このフィールドのオプションは、[!DNL Commerce]のデフォルトのステータスオプションに基づいています。 [注文ステータス](https://docs.magento.com/user-guide/sales/order-status.html)を参照してください。 また、カスタムの注文ステータスを作成して、ここで選択用に表示することもできます。 カスタム注文ステータスを作成するには、[カスタム注文ステータス](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}を参照してください。

1. 完了したら、「**[!UICONTROL Save order settings]**」をクリックします。

![順序の設定](assets/amazon-order-settings.png)

| フィールド | 説明 |
|---|---|
| [!UICONTROL Import Amazon Orders] | オプション：<ul><li>**[!UICONTROL Disabled]** - Amazonから新しい注文を受け取る際に、対応する注文をで作 [!DNL Commerce] 成しない場合に選択します。選択すると、このページ上の他のすべてのフィールドは無効になります。</li><li>**[!UICONTROL Enabled]** - （デフォルト）Amazonから新しい注文を受け取った場合に、対応 [!DNL Commerce] する注文を作成するタイミングを選択します。[!DNL Commerce] オーダーは、Amazonのステータスと在庫レベルに基づいて作成されます。</li></ul><br><br>`Enabled` でAmazonの注文を管理するために、を選択する必要があり [!DNL Commerce]ます。`Disabled`を選択すると、Amazonの注文はストアダッシュボードに表示されますが、注文は[!DNL Amazon Seller Central]アカウントで管理する必要があります。 |
| [!UICONTROL Import Amazon Orders Into Magento Store] | [!DNL Commerce] [注文](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}ワークスペースで作成されたときに、Amazon注文を保存する[!DNL Commerce]を選択します。 この設定のデフォルトは、[Amazonストア](./store-integration.md)を追加したときに選択された[!DNL Commerce] Webサイトのストア表示です。 この設定を変更する場合、オプションのリストは、設定した[!DNL Commerce]ストアによって異なります。 [ストア](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}を参照してください。 |
| [!UICONTROL Customer Creation] | オプション：<ul><li>**[!UICONTROL No Customer Creation (guest)]** - （デフォルト） Amazonの注文からインポートした顧客データを使用してで顧客ア [!DNL Commerce] カウントを作成しない場合に選択します。このオプションを選択すると、[!DNL Commerce]は、ゲストのチェックアウトを処理するのと同じ方法で、インポートされたAmazonの注文を処理するように指示します。</li><li>**[!UICONTROL Build New Customer Account]** - Amazon注文でインポートした顧客データを使用して、顧客データベ [!DNL Commerce] ースに新しい顧客アカウントを作成するタイミングを選択します。このオプションは、Amazonの注文内容から[!DNL Commerce]顧客データベースを作成するのに役立ちます。</li></ul> |
| 注文番号のソース | オプション：<ul><li>**[!UICONTROL Build Using Magento Order Number]** - （デフォルト）増分的に割り当てられた注文IDを使用して、対応するAmazon [!DNL Commerce] 注文に対して一意の注文番号を作成する [!DNL Commerce] 場合に選択します。 </li><li>**Amazonの注文番号を使用してビルド**  — 対応するAmazonに割り当てられた注文番号を使用して注 [!DNL Commerce] 文番号を作成する場合に選択します。</li></ul> |
| 保留中の注文 | オプション：<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Amazonの注文によって在庫数が影響を受け [!DNL Commerce] ないようにする場合に選択します。履行プロセス(FBA)にAmazonを使用する場合に選択します。 選択され、Amazonの注文を受け取った場合、注文された数量は[!DNL Commerce]在庫数に影響を与えません。</li><li>**[!UICONTROL Reserve Quantity]** - Amazon注文の注文数量を在庫数量で「予約」するタイミングを選 [!DNL Commerce] 択します。選択され、Amazonの注文を受け取ると、[!DNL Commerce]の在庫が「過剰販売」されるのを防ぐために、注文された数量が[!DNL Commerce]の在庫数に「予約」されます。 [!DNL Commerce]ストアフロントでは、「予約」数量は購入できません。</li></ul> |
| [!UICONTROL Order Status] | オプション：<ul><li>**[!UICONTROL Default Order Status]** - （デフォルト）Amazonからインポートされた新しく作成されたオーダーに、新しいオーダーのデフォルトのオーダーステータスを割り当てる場合に選択します。（新しい注文のカスタム注文ステータスを作成していない限り）新しい注文のデフォルトのステータスは`Pending`です。 [処理順序](https://docs.magento.com/user-guide/sales/order-processing.html)を参照してください。</li><li>>**[!UICONTROL Custom Order Status]** - Amazonから読み込まれた新しく作成された注文に、デフォルト以外のステータスを割り当てる場合に選択します。 選択すると、**[!UICONTROL Processing Order Status]**&#x200B;で、Amazonからインポートされた新しく作成された注文に使用するステータスを選択できます。</li></ul> |
| [!UICONTROL Processing Orders Status] | _[!UICONTROL Order Status]_が`Custom Order Status`に設定されている場合に有効になります。 新規受注に割り当てる受注ステータスを選択します。 このフィールドのオプションは、[!DNL Commerce]のデフォルトのステータスオプションによって異なります。 [注文ステータス](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}を参照してください。 また、ここに表示するカスタム注文ステータスを作成することもできます。 カスタム注文ステータスを作成するには、[カスタム注文ステータス](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}を参照してください。 |

## [!DNL Commerce] オーダー作成

[!DNL Commerce] オーダーは、次のステータスと在庫条件に基づいてAmazonオーダーに対して作成されます。

### 在庫管理を使用したオーダー作成

>[!NOTE]
>
>AdobeコマースおよびMagento Open Source2.3.xの統合でのみサポートされます。

| フルフィルメントチャネル | [!DNL Commerce] 在庫ステータス | Amazon注文ステータス | [!UICONTROL Create Magento Order] 設定 | 予約在庫 |
|---|---|---|---|---|
| FBA | 在庫中<br>在庫切れ<br>管理しない | 保留中 | いいえ | いいえ |
| FBA | 在庫中<br>在庫切れ<br>管理しない | PendingAvailability | いいえ | いいえ |
| FBA | 在庫中<br>在庫切れ<br>管理しない | キャンセル済み | いいえ | いいえ |
| FBA | 在庫中<br>在庫切れ<br>管理しない | エラー | いいえ | いいえ |
| FBA | 在庫中<br>在庫切れ<br>管理しない | 未出荷 | いいえ | いいえ |
| FBA | 在庫中<br>在庫切れ<br>管理しない | PartiallyShipped | いいえ | いいえ |
| FBA | 在庫内<br>管理しない | 発送済み | はい | いいえ |
| FBA | 在庫切れ | 発送済み | いいえ | いいえ |
| FBM | 在庫中<br>在庫切れ<br>管理しない | 保留中 | いいえ | いいえ |
| FBM | 在庫中<br>在庫切れ<br>管理しない | PendingAvailability | いいえ | いいえ |
| FBM | 在庫中<br>在庫切れ<br>管理しない | キャンセル済み | いいえ | いいえ |
| FBM | 在庫中<br>在庫切れ<br>管理しない | エラー | いいえ | いいえ |
| FBM | 在庫内<br>管理しない | 未出荷 | はい | はい |
| FBM | 在庫切れ | 未出荷 | いいえ | いいえ |
| FBM | 在庫内<br>管理しない | PartiallyShipped | はい | はい |
| FBM | 在庫切れ | PartiallyShipped | いいえ | いいえ |
| FBM | 在庫内<br>管理しない | 発送済み | はい | はい |
| FBM | 在庫切れ | 発送済み | いいえ | いいえ |

>[!NOTE]
>Amazonの注文が`Partially Shipped`または`Shipped`のステータスでインポートされた場合、作成される在庫予約はその注文のすべての品目に対して行われます。 Amazonの販売チャネルは、以前に出荷された品目を補償しません。
>
>注文がAmazon(FBA)で処理され、項目のステータスが`out of stock`の場合、[!DNL Commerce]は対応する注文を作成できません。 これは、在庫管理統合の制限です。
