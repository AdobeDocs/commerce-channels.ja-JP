---
title: オーバーライドの作成と編集
description: Amazon 販売チャンネルの上書きを使用して、1つの Amazon リストに変更を適用するか、複数の一覧に変更を適用します。
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# オーバーライドの作成と編集

リスティングに適用された上書きを編集または削除するには、その一覧を作成してオーバーライドします。 特定のリストに対して定義された値を設定しません。

## 1つのリストの上書きの作成

このアクションは、、、、 _[!UICONTROL Create Override]_およびタブの一覧を表示しているときに使用でき_[!UICONTROL Inactive]_ _[!UICONTROL Active]__[!UICONTROL Ineligible]_ ます。

1. _[!UICONTROL Products Listings]_ページ (、、およびタブ) のリストを表示_[!UICONTROL Inactive]_ _[!UICONTROL Active]__[!UICONTROL Ineligible]_ します。

1. 列の _[!UICONTROL Action]_「>」をクリックして、「**[!UICONTROL Select]****[!UICONTROL Create Override]**製品リストの無効化」ページを表示します。

   ![Amazon リスティングの上書きの作成](assets/amazon-select-create-override.png)

1. 適切なリストが表示されていることを確認するには、「」を確認してください _[!UICONTROL Listing Details]_。

1. 作成する上書きの種類を指定します。

   1つの上書きタイプまたはリストのタイプ (価格、処理時間、条件、売り手 Notes) の任意の組み合わせを定義できます。

   - **価格をクリックして、** **[!UICONTROL Change Listing Price]** 定義されている価格値を入力し **[!UICONTROL Price Override]** ます。
   - **処理時間を** クリック **[!UICONTROL Change Handling Time]** して、定義された時間値 (日数) を入力し **[!UICONTROL Handling Time Override]** ます。
   - **条件** -クリック **[!UICONTROL Change Condition]** して、の適切なオプションを選択し **[!UICONTROL Condition Override]** ます。
   - **販売者のノート** : 「 **[!UICONTROL Change Seller Notes]** 」をクリックして、コメントテキストを入力し **[!UICONTROL Seller Notes Override]** ます。

1. をクリックし **[!UICONTROL Save Listing Override]** ます。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。一覧の状態がに変更され `Relist in Progress` ます。 この変更は、Amazon に、次のデータ同期 (cron 設定に設定されている) でパブリッシュされます。 このリストはタブにも追加され_[!UICONTROL Overrides]_ ます。

次の例は、新規価格 `$55` 、新しい処理時間、新条件、および新しい販売者の音符テキストを定義する上書きを示して `1 day` `Used; Like New` います。

![Amazon リスティングの上書きの例](assets/amazon-overrides-edit.png)

## 1つのリストの上書きの編集または削除 {#edit-override-single-listing}

この _[!UICONTROL Edit Overrides]_アクションは、タブ上の一覧を表示しているときに使用でき_[!UICONTROL Overrides]_ ます。

1. ページに一覧を表示し _[!UICONTROL Product Listings]__[!UICONTROL Overrides]_ ます (tab キー)。

1. 列で _[!UICONTROL Action]_、「>」をクリックし&#x200B;**[!UICONTROL Select]****[!UICONTROL Edit Overrides]**ます。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択します。](assets/amazon-select-edit-overrides.png)

1. 適切なリスティングが上書きされていることを確認するには、「」を確認してください _[!UICONTROL Listing Details]_。

1. 設定を編集するには _[!UICONTROL Override]_、変更するタイプの断面 (価格、処理時間、条件、販売者の音符) を定義します。

   上書きの種類を変更しない場合は、「」 `No Change To <override type>` (デフォルト) を選択します。 この設定によって、以前に定義されていた上書き値はそのまま残ります。

   - **価格をクリックして、** **[!UICONTROL Change Listing Price]** 定義されている価格値を入力し **[!UICONTROL Price Override]** ます。
   - **処理時間を** クリック **[!UICONTROL Change Handling Time]** して、定義された時間値 (日数) を入力し **[!UICONTROL Handling Time Override]** ます。
   - **コンディション** : **[!UICONTROL Change Condition]** 「」をクリックして、の適切なオプションを選択し **[!UICONTROL Condition Override]** ます。
   - **販売者のノート** : 「 **[!UICONTROL Change Seller Notes]** 」をクリックして、コメントテキストを入力し **[!UICONTROL Seller Notes Override]** ます。

1. 上書きタイプを削除するには **、** 削除する各タイプについて「削除」をクリックします。 削除されていない場合は、以前に定義されていた値が上書きに残ります。

1. をクリックし **[!UICONTROL Save Listing Override]** ます。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。一覧の状態がに変更され `Relist in Progress` ます。 この変更は、Amazon に、次のデータ同期 (cron 設定に設定されている) でパブリッシュされます。 リストが表示されていない場合は、「タブ」にもリストが追加され_[!UICONTROL Overrides]_ ます。

Piggybacking を _作成_ します。 次の例では、以前に作成した上書きに対して、新規価格を定義し、 `$50` 手数料の上書きを削除して、前の条件と販売者のメモをオーバーライドしたままにしています。

![上書き ](assets/amazon-overrides-edit-2.png) の編集または削除
__

## 複数のリストの上書きの編集または削除 {#edit-override-multiple-listings}

アクションは、、、、 _[!UICONTROL Edit Listing Overrides]_およびタブで使用でき_[!UICONTROL Inactive]_ _[!UICONTROL Active]__[!UICONTROL Overrides]_ _[!UICONTROL Ineligible]_ます。

>[!NOTE]
>
>複数の一覧の上書きを変更しているので、 _[!UICONTROL Listing Details]_1 つの一覧を変更したときのように、セクションが表示されません。

1. _[!UICONTROL Products Listings]_ページ (、、、_[!UICONTROL Inactive]_ _[!UICONTROL Active]__[!UICONTROL Overrides]_ およびタブ) のリストを表示し _[!UICONTROL Ineligible]_ます。

1. 修正する各リストの左側の列にあるチェックボックスをオンにします。

1. _[!UICONTROL Actions]_でをクリックし&#x200B;**[!UICONTROL Edit Listing Overrides]**ます。

   _[!UICONTROL Product Listing Overrides]_ページが開きます。

   ![Amazon リストの上書きを選択します。](assets/amazon-actions-edit-listing-overrides.png)

1. 設定を編集するには _[!UICONTROL Override]_、変更するタイプの断面 (価格、処理時間、条件、販売者の音符) を定義します。

   上書きを維持するには、「 `No Change To <override type>` (初期設定)」を選択します。 この設定によって、以前に定義されていた上書き値はそのまま残ります。

   - **価格をクリックして、** **[!UICONTROL Change Listing Price]** 定義されている価格値を入力し **[!UICONTROL Price Override]** ます。
   - **処理時間を** クリック **[!UICONTROL Change Handling Time]** して、定義された時間値 (日数) を入力し **[!UICONTROL Handling Time Override]** ます。
   - **コンディション** : **[!UICONTROL Change Condition]** 「」をクリックして、の適切なオプションを選択し **[!UICONTROL Condition Override]** ます。
   - **販売者のノート** : 「 **[!UICONTROL Change Seller Notes]** 」をクリックして、コメントテキストを入力し **[!UICONTROL Seller Notes Override]** ます。

1. オーバーライドタイプを削除するには、 **[!UICONTROL Remove]** 削除する各タイプに対してをクリックします。 削除されていない場合は、以前に定義されていた値が上書きに残ります。

1. をクリックし **[!UICONTROL Save Listing Override]** ます。

   _[!UICONTROL Product Listing Overrides]_ページが閉じます。一覧の状態がに変更され `Relist in Progress` ます。 この変更は、Amazon に、次のデータ同期 (cron 設定に設定されている) でパブリッシュされます。 リストが表示されていない場合は、「タブ」にもリストが追加され_[!UICONTROL Overrides]_ ます。

### タイプの上書き

| トラッピング | つい |
|--- |--- |
| [!UICONTROL Price Override] | 価格設定によって、リストの価格が定義されます。 この上書きが削除されるまでは、自動的に設定される設定よりも優先されます。<br><br>製品価格を変更するには、新しい価格を選択して **[!UICONTROL Change Listing Price]** 入力し **[!UICONTROL Price Override]** ます。 |
| [!UICONTROL Handling Time Override] | 処理時間の上書きは、製品の処理と出荷にかかる時間 (日数) を定義します。 処理時間のオーバーライドは、そのオーバーライドが削除されるまで、自動およびデフォルトの処理時間設定よりも優先されます。<br><br>ボックス内の値は、 _[!UICONTROL Handling Time Override]_リスティングの設定で定義されているデフォルトの処理時間、 [ ](./listing-settings.md) または定義された上書き処理時間のいずれかです。 手数料の上書きを削除すると、リストのデフォルト値として設定されている処理時間が表示されます。<br><br>手数料の上書きを定義するには、**[!UICONTROL Change Handling Time]**新しい処理時間 (日数) を選択して入力し&#x200B;**[!UICONTROL Handling Time Override]**ます。 |
| [!UICONTROL Condition Override] | リスティング条件をオーバーライドするには、「 **[!UICONTROL Change Condition]** 条件の上書き」から新しい条件を選択して選択し **** ます。 |
| [!UICONTROL Seller Notes Override] | 以外の条件が定義されているカタログ内の製品については `New` 、製品とその条件について詳細な情報を購入者に示します。 条件製品に対して販売者のメモの上書きを入力することはでき `New` ますが、そのノートは、Amazon には表示されません。<br><br>販売者のメモを上書きするには、の新しいノートを選択 **[!UICONTROL Change Seller Notes]** して入力し **[!UICONTROL Seller Notes Override]** ます。 |
