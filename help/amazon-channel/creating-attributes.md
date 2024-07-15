---
title: Amazon Sales Channel の属性を作成および編集します
description: Amazon Sales Channelには、現在のAmazon属性とリンクされたCommerce属性を確認するのに役立つ属性ビューが用意されています。
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# 属性の作成と編集

Amazonを通じて販売する際に [!DNL Commerce] 属性を作成または更新し、店舗を更新します。 Amazon sales channel ホームページの [_[!UICONTROL Attributes]_ビューを使用して ](./attributes-view.md) 現在のAmazon属性およびリンクされた [!DNL Commerce] 属性を確認します。_[!UICONTROL Action]_ の列には、属性で使用可能なアクションが表示されます。 リンクされていないAmazon属性に対して新しい [!DNL Commerce] 属性を作成してマッピングするか、既存の [!DNL Commerce] 属性とそのAmazon属性へのマッピングを編集できます。

属性を作成および更新する際に、[!DNL Commerce] 製品とAmazon製品の属性値を確認することをお勧めします。 これらの値は、Amazonと同期して値をインポートしない場合は異なる可能性があります。 これらの属性のAmazon値を確認するには、[Amazon属性マッピングの確認 ](./amazon-matching-attributes-values.md) を参照してください。 これらの値を変更する場合は、Amazonと [!DNL Commerce] の間で [ マッピングを編集または作成 ](./amazon-manually-update-incomplete-listing.md) できます。

## 属性の作成 {#create-an-attribute}

これらの手順では、[!DNL Commerce] 属性を作成し、Amazon属性にマッピングします。 設定によっては、カタログ間で値の同期が開始される場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューで「**[!UICONTROL Attributes]**」をクリックし、Amazon属性を見つけて「_[!UICONTROL Action]_」列の「**[!UICONTROL Create Attribute]**」をクリックします。

1. リンクされた [!DNL Commerce] 属性にAmazon値を同期できるようにするには、**[!UICONTROL Is Active]** を `Yes` に設定します。

   `Yes` に設定すると、設定に応じて値が同期されます。

1. **[!UICONTROL Select Magento Product Attribute]** の `Create New Magento Attribute` を選択してください。

   属性は、**[!UICONTROL Amazon Attribute Name]** 用に選択されたにマッピングされます。

1. **[!UICONTROL Magento Product Attribute Name]** を入力します。

1. **[!UICONTROL Magento Product Attribute Code]** を入力します。

   この値は、スペースを含めず、すべて小文字にする必要があります。

1. **[!UICONTROL Attribute Set Ids]** の場合は、割り当てる属性セットを選択します。

   通常、属性は属性セットの一部です。たとえば、青、緑、黄、赤の属性を持つ色のセットなどです。

1. **[!UICONTROL Type]** の場合は、テキストや数値など、属性値のタイプを選択します。

   このオプションは、属性に使用できる値に影響します。

1. **[!UICONTROL Use for Promo Rule Conditions]**：を `Yes` に設定すると、プロモーション条件内でパラメーターに属性を使用できます。

1. **[!UICONTROL Used in Search]**：属性と値を製品の検索で使用できる場合は、`Yes` に設定します。

1. **[!UICONTROL Comparable on Storefront]**:Amazonの「比較」機能で属性値を使用できる場合は、`Yes` に設定します。

1. 属性の [!DNL Commerce] [ 範囲 ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) を選択してから、Amazonの値の読み込み先となる 1 つ以上のストアビューを選択します。

   スコープが `Global` に設定されている場合、属性の作成後に _[!UICONTROL Store View]_を変更することはできません。

   `All Store Views (Global)` を選択すると、値が同期され、Amazonのすべてのストアビューに値が保存されます。 特定のストアビューにのみ値を同期することができます。

1. 完了したら、「**[!UICONTROL Save Attribute Settings]**」をクリックします。

保存した後で、属性を編集して、設定を確認し、属性のAmazonと [!DNL Commerce] の値を一致させる必要がある場合があります。 また、Amazonの値が [!DNL Commerce] の値を上書きする必要があるかどうかを指定することもできます。

![ 属性設定を作成 ](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブで、Amazonと [!DNL Commerce] の間でアクティブに同期されるかどうかを示します。 `Yes` に設定すると、選択した属性のAmazonと [!DNL Commerce] の属性値が常に同期されます。 |
| Magentoの製品属性を選択 | リストされたAmazonの属性名にリンクする、選択した属性を示します。 属性を作成する場合は、「`Create New Magento Attribute`」を選択します。 |
| [!UICONTROL Amazon Attribute Name] | 選択したAmazon属性の名前を示します。 選択した属性は、このAmazon属性にリンクしています。 この値を [!DNL Commerce] から編集することはできません。 |
| [!UICONTROL Magento Product Attribute Name] | 属性名または「ラベル」を示します。 |
| [!UICONTROL Magento Product Attribute Code] | 属性コードを示します。すべて小文字で指定し、スペースは含めません。 |
| [!UICONTROL Attribute Set Ids] | 属性を割り当てる属性セットを示します。 属性は、青、緑、黄、赤の属性を持つ色のセットなど、属性セットの一部になる傾向があります。 |
| [!UICONTROL Type] | テキスト、数値など、属性値の値タイプを示します。 選択は、属性に使用できる値に影響します。 |
| [!UICONTROL Use for Promo Rule Conditions] | `Yes` に切り替えて、プロモーション条件内でパラメーターに属性を使用できるようにします。 |
| [!UICONTROL Used in Search] | 属性と値が製品検索で使用できるかどうかを示します。 |
| [!UICONTROL Comparable on Storefront] | Amazonの「比較」機能で属性値を使用できるかどうかを示します。 |
| [!UICONTROL Magento Product Attribute Scope] | 属性の [ スコープ ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) を示します。 オプション：グローバル/ストア表示 <br>`Global` に設定した場合、属性の作成後にストア表示を編集することはできません。 |
| [!UICONTROL Store Views (to import values into to)] | 範囲が `Store View` に設定されている場合にのみ表示されます。 Amazonの属性値を同期する [ ストア表示 ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) を選択します。 `All Store Views (Global)` を選択すると、すべての [!DNL Commerce] ストアビューの値が更新されます。 |

## 属性の編集 {#edit-an-attribute}

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Channels]_/**[!UICONTROL Amazon Sales Channel]**に移動します。

1. 左側のメニューで「**[!UICONTROL Attributes]**」をクリックし、Amazon属性を見つけて「_[!UICONTROL Action]_」列の「**[!UICONTROL Edit]**」をクリックします。

1. リンクされた [!DNL Commerce] 属性に対するAmazon値の同期を有効または無効にするには、**アクティブ** を `Yes` または `No` に設定します。

   `Yes` に設定すると、設定に応じて値が同期されます。

1. **[!UICONTROL Select Magento Product Attribute]** しくは、選択した **[!UICONTROL Amazon Attribute Name]** にマッピングするように属性を検証または更新します。

1. 受信Amazon属性値で既存の属性値を上書きするかどうかを指定します。

   例えば、Amazonの価格を [!DNL Commerce] に上書きしたくない場合があります。

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** – 値を保持し、[!DNL Commerce] ストアとAmazon ストアで異なる値を保持します。

   - **[!UICONTROL Overwrite Existing Magento Values]** - [!DNL Commerce] 製品カタログの値を、受信したAmazonの値で上書きします。

1. 編集が可能な場合は、1 つ以上の **[!UICONTROL Store Views (to import Amazon values into)]** を選択します。

   属性が `Global` スコープで作成された場合、属性の作成後に _ストア表示_ を変更することはできません。

   `All Store Views (Global)` を選択すると、値が同期され、すべてのストアビューに保存されます。 特定のストアビューにのみ値を同期することができます。

1. 完了したら、「**[!UICONTROL Save Attribute Settings]**」をクリックします。

![ 属性設定を編集 ](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブで、Amazonと [!DNL Commerce] の間でアクティブに同期されるかどうかを示します。 `Yes` に設定すると、選択した属性のAmazonと [!DNL Commerce] の属性値が常に同期されます。 |
| [!UICONTROL Select Magento Product Attribute] | リストされたAmazonの属性名にリンクする、選択した [!DNL Commerce] 属性を示します。 リンクされた [!DNL Commerce] 属性を変更する場合は、ドロップダウンリストから別の属性を選択します。 値は設定に従って同期されます。 |
| [!UICONTROL Amazon Attribute Name] | [!DNL Amazon Seller Central] で定義されたAmazon属性の名前を示します。 選択した [!DNL Commerce] 属性は、このAmazon属性にリンクしています。 この値を [!DNL Commerce] から編集することはできません。 |
| [!UICONTROL Overwrite Existing Value] | Amazonの属性値が既存の [!DNL Commerce] 値を上書きし、この [!DNL Commerce] 属性を持つすべての商品に影響を与えるかどうかを示します。<ul><li>**既存のMagento値を上書きしない** - （デフォルト） [!DNL Commerce] 値を保持し、[!DNL Commerce] ストアとAmazon ストアで異なる値を保持します。</li><li>**既存のMagento値を上書き** - Amazonの値を、[!DNL Commerce] 製品カタログの [!DNL Commerce] の値に上書きします。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 属性が `Global` スコープで作成された場合、属性の編集時に表示されません。 [!DNL Commerce] [ スコープ ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) が作成され、`Store View` に設定されたことを示します。 |
| [!UICONTROL Store Views (to import values into to)] | Amazon属性値を同期する [!DNL Commerce] ール ](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) ストアビュー [ を選択します。 `All Store Views (Global)` を選択すると、すべてのストアビューで値が更新されます。 |
