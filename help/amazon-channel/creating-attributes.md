---
title: 属性の作成と編集
description: Amazon Sales Channel には、現在の Amazon 属性とリンクされた Commerce 属性を確認するための属性ビューが用意されています。
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# 属性の作成と編集

[!DNL Commerce]Amazon を通じて販売するときと、ストアを更新する際に、属性を作成または更新します。[!DNL Commerce] [_[!UICONTROL Attributes]_](./attributes-view.md) Amazon sales channel のホームページの表示を使用して、現在の amazon 属性とリンクされた属性を確認します。この列には、_[!UICONTROL Action]_ 属性に対して実行可能なアクションが表示されます。 リンク解除された Amazon 属性に対して新しい属性を作成してマップするか [!DNL Commerce] 、既存の [!DNL Commerce] 属性とそのマッピングを Amazon 属性に対して編集することができます。

属性を作成および更新する際に、および Amazon 製品の属性値を検証する必要がある場合があり [!DNL Commerce] ます。 Amazon から値を同期およびインポートしていない場合は、これらの値が異なる場合があります。 このような属性の Amazon の値を確認するには、「Amazon Attribute Mapping の再検討」を参照してください [ ](./amazon-matching-attributes-values.md) 。 これらの値を変更する場合は、 [ ](./amazon-manually-update-incomplete-listing.md) Amazon と. 間のマッピングを編集または作成することができ [!DNL Commerce] ます。

## 属性の作成 {#create-an-attribute}

以下の手順では、属性を作成 [!DNL Commerce] し、Amazon attribute にマップします。 設定によっては、値がカタログ間で同期を開始することがあります。

1. _管理者は_ 、> > を参照して **[!UICONTROL Marketing]** _[!UICONTROL Channels]_**[!UICONTROL Amazon Sales Channel]**ください。

1. **[!UICONTROL Attributes]**&#x200B;左側のメニューで「Amazon」属性をクリックし、 **[!UICONTROL Create Attribute]** 列内をクリックし _[!UICONTROL Action]_ます。

1. Amazon 値とリンクされた属性との同期を有効にするには [!DNL Commerce] 、「」に設定し **[!UICONTROL Is Active]** `Yes` ます。

   「」に設定されている場合、 `Yes` 設定に応じて値が同期されます。

1. 「For」を選択 `Create New Magento Attribute` **[!UICONTROL Select Magento Product Attribute]** します。

   属性は、によって選択されたにマップされ **[!UICONTROL Amazon Attribute Name]** ます。

1. 「」と入力し **[!UICONTROL Magento Product Attribute Name]** ます。

1. 「」と入力し **[!UICONTROL Magento Product Attribute Code]** ます。

   この値は空白なしでもすべて小文字にする必要があります。

1. の場合は **[!UICONTROL Attribute Set Ids]** 、割り当てる属性セットを選択します。

   属性は属性セットに含まれます。色の属性には、青、緑、黄、赤などの属性が設定されています。

1. では、 **[!UICONTROL Type]** テキストや数字など、属性値のタイプを選択します。

   このオプションは属性に指定できる値に影響します。

1. の場合は **[!UICONTROL Use for Promo Rule Conditions]** 、 `Yes` プロモーション条件内のパラメーターに属性を使用できるように設定します。

1. **[!UICONTROL Used in Search]**&#x200B;では、で `Yes` 属性と値を製品検索に使用できるかどうかを設定します。

1. については **[!UICONTROL Comparable on Storefront]** 、 `Yes` 属性値を Amazon の &quot;比較&quot; 機能に使用できるかどうかを設定します。

1. [!DNL Commerce] [ ](https://docs.magento.com/user-guide/configuration/scope.html) 属性のスコープ {target = &quot;_blank&quot;} を選択してから、Amazon 値の読み込み先となるストアビューを選択します。

   スコープがに設定されている場合は、 `Global` _[!UICONTROL Store View]_属性の作成後にを変更することはできません。

   このオプションを選択する `All Store Views (Global)` と、すべての Amazon store ビューに値が同期されて保存されます。 特定のストアビューに値を同期する必要があるのは1つだけです。

1. 完了したら、をクリックし **[!UICONTROL Save Attribute Settings]** ます。

保存した後は、属性を編集して設定を確認し、その属性の値と一致する値を確認することもでき [!DNL Commerce] ます。 Amazon の値によって値が上書きされるかどうかを指定することもでき [!DNL Commerce] ます。

![属性設定の作成](assets/amazon-attribute-settings-create.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Is Active] | この属性が、Amazon ととの間でライブにアクティブに同期されているかどうかを示し [!DNL Commerce] ます。 設定する `Yes` と、Amazon からの属性値が保証され、 [!DNL Commerce] 選択された属性に対して同期が維持されます。 |
| Magento 製品属性を選択します。 | 選択されている属性のうち、表示された Amazon Attribute Name にリンクする属性を示します。 属性を作成する場合は、「」を選択し `Create New Magento Attribute` ます。 |
| [!UICONTROL Amazon Attribute Name] | 選択した Amazon attribute の名前が表示されます。 選択された属性は、この Amazon 属性にリンクしています。 では、この値を編集することはできません [!DNL Commerce] 。 |
| [!UICONTROL Magento Product Attribute Name] | 属性名または &quot;label&quot; を指定します。 |
| [!UICONTROL Magento Product Attribute Code] | 属性コードを指定します。すべて小文字で空白なしで表示されます。 |
| [!UICONTROL Attribute Set Ids] | 属性を割り当てる属性セットを指定します。 属性は属性セットの一部として扱われます。例えば、カラーの属性には、青、緑、黄、赤などの属性を設定します。 |
| [!UICONTROL Type] | テキストや数字などの属性値の値の型を示します。 選択した属性の値は、選択した値に反映されます。 |
| [!UICONTROL Use for Promo Rule Conditions] | に切り替え `Yes` て、プロモーション条件内のパラメーターに属性を使用できるようにします。 |
| [!UICONTROL Used in Search] | 製品検索に属性と値を使用できるかどうかを示します。 |
| [!UICONTROL Comparable on Storefront] | 属性値が Amazon の &quot;比較&quot; 機能に使用できるかどうかを示します。 |
| [!UICONTROL Magento Product Attribute Scope] | [ ](https://docs.magento.com/user-guide/configuration/scope.html) 属性のスコープ {target = &quot;_blank&quot;} を示します。オプション: グローバル/ストアビュー <br> に設定した場合 `Global` 、属性の作成後にストアビューを編集することはできません。 |
| [!UICONTROL Store Views (to import values into to)] | これはスコープが「」に設定されている場合にのみ表示され `Store View` ます。 [ ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) Amazon 属性値が同期されるストアビュー {target = &quot;_blank&quot;} を選択します。選択 `All Store Views (Global)` すると、すべてのストアビューで値が更新され [!DNL Commerce] ます。 |

## 属性の編集 {#edit-an-attribute}

1. _管理者は_ 、> > を参照して **[!UICONTROL Marketing]** _[!UICONTROL Channels]_**[!UICONTROL Amazon Sales Channel]**ください。

1. **[!UICONTROL Attributes]**&#x200B;左側のメニューで「Amazon」属性をクリックし、 **[!UICONTROL Edit]** 列内をクリックし _[!UICONTROL Action]_ます。

1. 設定されている属性の Amazon 値を有効または無効にするには [!DNL Commerce] 、「or」に設定し **** `Yes` `No` ます。

   「」に設定されている場合、 `Yes` 設定に応じて値が同期されます。

1. につい **[!UICONTROL Select Magento Product Attribute]** ては、選択した属性にマップされるように属性を確認または更新することが **[!UICONTROL Amazon Attribute Name]** できます。

1. 受信した Amazon 属性の値が既存の属性値に上書きされるようにするかどうかを指定します。

   例えば、Amazon からの価格を上書きしないようにすることができ [!DNL Commerce] ます。

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** -その値を保持します。また、Amazon stores には別の値を [!DNL Commerce] 保存します。

   - **[!UICONTROL Overwrite Existing Magento Values]** -製品カタログ内の値を受信した [!DNL Commerce] Amazon value で上書きします。

1. 編集可能な場合は、1つまたは複数のオプションを選択し **[!UICONTROL Store Views (to import Amazon values into)]** ます。

   属性がスコープとして作成されている場合は、 `Global` __ 属性の作成後にストアビューを変更することはできません。

   このオプションを選択した場合は `All Store Views (Global)` 、すべてのストアビューに値が同期されて保存されます。 特定のストアビューに値を同期する必要があるのは1つだけです。

1. 完了したら、をクリックし **[!UICONTROL Save Attribute Settings]** ます。

![属性設定の編集](assets/amazon-attribute-settings-edit.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Is Active] | この属性が、Amazon ととの間でライブにアクティブに同期されているかどうかを示し [!DNL Commerce] ます。 設定する `Yes` と、Amazon からの属性値が保証され、 [!DNL Commerce] 選択された属性に対して同期が維持されます。 |
| [!UICONTROL Select Magento Product Attribute] | 選択され [!DNL Commerce] ている属性のうち、表示された Amazon Attribute Name にリンクする属性を示します。 リンクされた属性を変更する場合は [!DNL Commerce] 、ドロップダウンリストから別の属性を選択します。 設定に応じて値が同期されます。 |
| [!UICONTROL Amazon Attribute Name] | で定義されている Amazon 属性の名前が表示され [!DNL Amazon Seller Central] ます。 選択された属性は、 [!DNL Commerce] この Amazon 属性にリンクしています。 では、この値を編集することはできません [!DNL Commerce] 。 |
| [!UICONTROL Overwrite Existing Value] | Amazon attribute の値が既存の値を上書きするかどうかを示し [!DNL Commerce] ます。すべての製品は、この属性を使用して影響を及ぼし [!DNL Commerce] ます。<ul><li>**既存の Magento 値は上書きせず、** (デフォルト) 値を保持し [!DNL Commerce] ます。この値は、別の値 [!DNL Commerce] と Amazon stores ストアに保存されます。</li><li>**既存の Magento 値を上書きし** ます。製品カタログの値に Amazon の値を保存 [!DNL Commerce] [!DNL Commerce] します。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 属性がスコープとして作成されている場合は、属性を編集するときには表示されません `Global` 。 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/configuration/scope.html) {Target = &quot;_blank&quot;} のスコープが作成され、に設定されていることを示し `Store View` ます。 |
| [!UICONTROL Store Views (to import values into to)] | [!DNL Commerce] [ ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) Amazon attribute 値を同期するストアビューを選択します {target = &quot;_blank 「}」を選択します。選択 `All Store Views (Global)` すると、すべてのストアビューで値が更新されます。 |
