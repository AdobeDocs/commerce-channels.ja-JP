---
title: 属性の作成と編集
description: AmazonSales Channelには、現在のAmazon属性とリンクされたコマース属性を確認するのに役立つ属性ビューが用意されています。
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# 属性の作成と編集

Amazonを通じて販売し、ストアを更新する際に、[!DNL Commerce]属性を作成または更新します。 現在のAmazon属性とリンクされた[!DNL Commerce]属性を、Amazon販売チャネルホームページの&#x200B;[_[!UICONTROL Attributes]_ビュー](./attributes-view.md)で確認します。_[!UICONTROL Action]_&#x200B;列には、属性で使用可能なアクションが表示されます。 リンクが解除されたAmazon属性に対して新しい[!DNL Commerce]属性を作成してマッピングするか、既存の[!DNL Commerce]属性とそのAmazon属性へのマッピングを編集できます。

属性を作成および更新する際に、[!DNL Commerce]およびAmazon製品の属性値を確認する必要が生じる場合があります。 これらの値は、Amazonから値を同期および読み込まない場合に異なる場合があります。 これらの属性のAmazon値を確認するには、[Amazon属性マッピングの確認](./amazon-matching-attributes-values.md)を参照してください。 これらの値を変更する場合は、Amazonと[!DNL Commerce]の間のマッピング](./amazon-manually-update-incomplete-listing.md)を[編集または作成できます。

## 属性の作成 {#create-an-attribute}

以下の手順では、[!DNL Commerce]属性を作成し、Amazon属性にマッピングします。 設定によっては、値のカタログ間での同期が開始される場合があります。

1. _管理_&#x200B;サイドバーで、**[!UICONTROL Marketing]** / _[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューの&#x200B;**[!UICONTROL Attributes]**&#x200B;をクリックし、Amazon属性を探して、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Create Attribute]**をクリックします。

1. リンクされた[!DNL Commerce]属性に対してAmazonの値を同期できるようにするには、**[!UICONTROL Is Active]**&#x200B;を`Yes`に設定します。

   `Yes`に設定すると、設定に従って値が同期します。

1. **[!UICONTROL Select Magento Product Attribute]**&#x200B;に`Create New Magento Attribute`を選択します。

   属性は、**[!UICONTROL Amazon Attribute Name]**&#x200B;に対して選択されたにマッピングされます。

1. **[!UICONTROL Magento Product Attribute Name]**&#x200B;を入力します。

1. **[!UICONTROL Magento Product Attribute Code]**&#x200B;を入力します。

   この値は、スペースを含まないすべて小文字にする必要があります。

1. **[!UICONTROL Attribute Set Ids]**&#x200B;の場合、割り当てる属性セットを選択します。

   通常、アトリビュートはアトリビュートセットの一部です。例えば、青、緑、黄、赤のアトリビュートを持つカラーのセットなどです。

1. **[!UICONTROL Type]**&#x200B;の場合は、テキストや数値など、属性値のタイプを選択します。

   このオプションは、属性に許可されている値に影響を与えます。

1. **[!UICONTROL Use for Promo Rule Conditions]**&#x200B;の場合、`Yes`に設定して、プロモーション条件内のパラメーターで属性を使用できるようにします。

1. **[!UICONTROL Used in Search]**&#x200B;の場合、属性と値を製品検索で使用できる場合は`Yes`に設定します。

1. **[!UICONTROL Comparable on Storefront]**&#x200B;の場合、「比較」機能を使用してAmazonで属性値を使用できる場合は`Yes`に設定します。

1. 属性に[!DNL Commerce] [scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}を選択し、Amazon値の読み込み先として1つ以上のストアビューを選択します。

   スコープを`Global`に設定した場合、属性の作成後に&#x200B;_[!UICONTROL Store View]_を変更することはできません。

   `All Store Views (Global)`を選択すると、値が同期され、すべてのAmazonストアビューに保存されます。 特定のストアビューにのみ値を同期する必要がある場合があります。

1. 完了したら、「**[!UICONTROL Save Attribute Settings]**」をクリックします。

保存後、属性を編集して、設定を確認し、属性のAmazonと[!DNL Commerce]の値に一致させることができます。 また、Amazonの値で[!DNL Commerce]値が上書きされるかどうかを指定することもできます。

![属性設定の作成](assets/amazon-attribute-settings-create.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Is Active] | この属性がライブで、Amazonと[!DNL Commerce]の間でアクティブに同期しているかどうかを示します。 `Yes`に設定して、Amazonと[!DNL Commerce]の属性値が選択した属性に対して同期し続けます。 |
| Magento製品属性の選択 | リストに表示されているAmazon属性名にリンクする、選択した属性を示します。 属性を作成する場合は、`Create New Magento Attribute`を選択します。 |
| [!UICONTROL Amazon Attribute Name] | 選択したAmazon属性の名前が表示されます。 選択した属性は、このAmazon属性にリンクします。 この値は[!DNL Commerce]で編集できません。 |
| [!UICONTROL Magento Product Attribute Name] | 属性名または「label」を示します。 |
| [!UICONTROL Magento Product Attribute Code] | 属性コードを示します。すべてスペースを含まない小文字で表されます。 |
| [!UICONTROL Attribute Set Ids] | 属性を割り当てる属性セットを示します。 属性は、青、緑、黄、赤の属性を持つ色のセットなど、属性セットの一部になりがちです。 |
| [!UICONTROL Type] | テキストや数値など、属性値の値のタイプを示します。 選択は、属性の許容値に影響します。 |
| [!UICONTROL Use for Promo Rule Conditions] | `Yes`に切り替えて、プロモーション条件内のパラメーターで属性を使用できるようにします。 |
| [!UICONTROL Used in Search] | 属性と値が製品検索で使用できるかどうかを示します。 |
| [!UICONTROL Comparable on Storefront] | 属性値がAmazonの「比較」機能で使用できるかどうかを示します。 |
| [!UICONTROL Magento Product Attribute Scope] | 属性の[scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}を示します。 オプション：Global / Store View<br>`Global`に設定すると、属性の作成後にストアビューを編集できなくなります。 |
| [!UICONTROL Store Views (to import values into to)] | スコープが`Store View`に設定されている場合にのみ表示されます。 Amazon属性値の同期先となる[store view](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}を選択します。 `All Store Views (Global)`を選択すると、すべての[!DNL Commerce]ストアビューの値が更新されます。 |

## 属性の編集 {#edit-an-attribute}

1. _管理_&#x200B;サイドバーで、**[!UICONTROL Marketing]** / _[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューの&#x200B;**[!UICONTROL Attributes]**&#x200B;をクリックし、Amazon属性を探して、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Edit]**をクリックします。

1. リンクされた[!DNL Commerce]属性に対するAmazon値の同期を有効または無効にするには、**「アクティブ**」を`Yes`または`No`に設定します。

   `Yes`に設定すると、設定に従って値が同期します。

1. **[!UICONTROL Select Magento Product Attribute]**&#x200B;の場合は、選択した&#x200B;**[!UICONTROL Amazon Attribute Name]**&#x200B;にマッピングするように属性を確認または更新します。

1. 受信するAmazon属性値で既存の属性値を上書きするかどうかを示します。

   例えば、Amazonの価格を[!DNL Commerce]に上書きしたくない場合があります。

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**  — とAmazonストアで異なる値を保持し、 [!DNL Commerce] 値を保持します。

   - **[!UICONTROL Overwrite Existing Magento Values]**  — 商品カタログ内の値を [!DNL Commerce] 読み込んだAmazon値で上書きします。

1. 編集可能な場合は、1つ以上の&#x200B;**[!UICONTROL Store Views (to import Amazon values into)]**&#x200B;を選択します。

   属性が`Global`スコープで作成された場合、属性の作成後に&#x200B;_ストアビュー_&#x200B;を変更することはできません。

   `All Store Views (Global)`を選択すると、値が同期され、すべてのストアビューに保存されます。 特定のストアビューにのみ値を同期する必要がある場合があります。

1. 完了したら、「**[!UICONTROL Save Attribute Settings]**」をクリックします。

![属性設定の編集](assets/amazon-attribute-settings-edit.png)

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Is Active] | この属性がライブで、Amazonと[!DNL Commerce]の間でアクティブに同期しているかどうかを示します。 `Yes`に設定して、Amazonと[!DNL Commerce]の属性値が選択した属性に対して同期し続けます。 |
| [!UICONTROL Select Magento Product Attribute] | リストに表示されているAmazon属性名にリンクする、選択した[!DNL Commerce]属性を示します。 リンクされた[!DNL Commerce]属性を変更する場合は、ドロップダウンリストから別の属性を選択します。 値は設定に従って同期します。 |
| [!UICONTROL Amazon Attribute Name] | [!DNL Amazon Seller Central]で定義されたAmazon属性の名前を表示します。 選択した[!DNL Commerce]属性は、このAmazon属性にリンクします。 この値は[!DNL Commerce]で編集できません。 |
| [!UICONTROL Overwrite Existing Value] | Amazonの属性値が既存の[!DNL Commerce]値を上書きし、この[!DNL Commerce]属性を持つすべての製品に影響するかどうかを示します。<ul><li>**既存のMagento値を上書きしない**  — （デフォルト） [!DNL Commerce] とAmazonストアで異なる値を保持し、 [!DNL Commerce] 値を維持します。</li><li>**既存のMagento値を上書き**  - Amazon値を商品カタログ [!DNL Commerce] の値に上書き [!DNL Commerce] します。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 属性が`Global`スコープで作成された場合、属性の編集時に表示されません。 [!DNL Commerce] [scope](https://docs.magento.com/user-guide/configuration/scope.html){target=&quot;_blank&quot;}が作成され、`Store View`に設定されたことを示します。 |
| [!UICONTROL Store Views (to import values into to)] | Amazon属性値を同期する[!DNL Commerce] [store view](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}を選択します。 `All Store Views (Global)`を選択すると、すべてのストアビューの値が更新されます。 |
