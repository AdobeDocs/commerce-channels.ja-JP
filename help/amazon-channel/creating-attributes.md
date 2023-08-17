---
title: Amazonセールスチャネルの属性を作成および編集します
description: AmazonSales Channelには、現在のAmazon属性と、リンクされた Commerce 属性を確認できる属性ビューが用意されています。
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 0%

---

# 属性の作成と編集

作成または更新 [!DNL Commerce] 属性を設定します。 現在のAmazon属性とリンクを確認する [!DNL Commerce] 属性を [_[!UICONTROL Attributes]_表示](./attributes-view.md) Amazonセールスチャネルのホームページ The_[!UICONTROL Action]_ 列には、属性で使用可能なアクションが表示されます。 新しい [!DNL Commerce] 属性を指定します。または、既存の [!DNL Commerce] 属性とAmazon属性へのマッピング。

属性を作成および更新する際に、次の属性値を確認する必要があります。 [!DNL Commerce] およびAmazon製品。 これらの値は、Amazonから値を同期および読み込まない場合に異なる場合があります。 これらの属性のAmazon値を確認するには、 [Amazon属性マッピングの確認](./amazon-matching-attributes-values.md). これらの値を変更する場合は、 [マッピングの編集または作成](./amazon-manually-update-incomplete-listing.md) Amazonと [!DNL Commerce].

## 属性の作成 {#create-an-attribute}

以下の手順で、 [!DNL Commerce] 属性にマッピングし、Amazon属性にマッピングします。 設定によっては、値のカタログ間での同期が開始される場合があります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューで、Amazon属性を探し、 **[!UICONTROL Create Attribute]** （内） _[!UICONTROL Action]_列。

1. リンクされた [!DNL Commerce] 属性、設定 **[!UICONTROL Is Active]** から `Yes`.

   に設定する場合 `Yes`の場合、値は設定に従って同期されます。

1. 選択 `Create New Magento Attribute` 対象： **[!UICONTROL Select Magento Product Attribute]**.

   属性は、選択したにマッピングされます。 **[!UICONTROL Amazon Attribute Name]**.

1. を入力します。 **[!UICONTROL Magento Product Attribute Name]**.

1. を入力します。 **[!UICONTROL Magento Product Attribute Code]**.

   この値は、スペースを含まないすべて小文字にする必要があります。

1. の場合 **[!UICONTROL Attribute Set Ids]**&#x200B;割り当てる属性セットを選択します。

   通常、アトリビュートはアトリビュートセットの一部です。例えば、青、緑、黄、赤のアトリビュートを持つカラーのセットなどです。

1. の場合 **[!UICONTROL Type]**」で、属性値のタイプ（テキストや数値など）を選択します。

   このオプションは、属性に使用できる値に影響を与えます。

1. の場合 **[!UICONTROL Use for Promo Rule Conditions]**、に設定 `Yes` を使用して、プロモーション条件内のパラメーターで属性を使用できるようにします。

1. の場合 **[!UICONTROL Used in Search]**、に設定 `Yes` （製品の検索で属性と値が使用できる場合）。

1. の場合 **[!UICONTROL Comparable on Storefront]**、に設定 `Yes` ( 属性値がAmazonの「比較」機能で使用できる場合 )

1. を選択します。 [!DNL Commerce] [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) 属性に対して、Amazon値の読み込み先となる 1 つ以上のストアビューを選択します。

   スコープが `Global`、 _[!UICONTROL Store View]_属性の作成後は変更できません。

   次を選択した場合： `All Store Views (Global)`を呼び出すと、値が同期され、すべてのAmazonストアビューに保存されます。 特定のストアビューにのみ値を同期する必要がある場合があります。

1. 完了したら、「 **[!UICONTROL Save Attribute Settings]**.

保存後、属性を編集して、設定を確認し、Amazonと [!DNL Commerce] 属性の値。 また、Amazonの値を上書きするかどうかを指定できます [!DNL Commerce] 値。

![属性設定を作成](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブかどうかを示し、Amazonと [!DNL Commerce]. をに設定します。 `Yes` Amazonと [!DNL Commerce] 選択した属性の同期を維持します。 |
| Magento製品属性を選択 | リストに表示されているAmazon属性名にリンクする、選択した属性を示します。 属性を作成する場合は、「 `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | 選択したAmazon属性の名前が表示されます。 選択した属性は、このAmazon属性にリンクします。 この値は、 [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | 属性名または「label」を示します。 |
| [!UICONTROL Magento Product Attribute Code] | 属性コードを示します。すべてスペースを含まない小文字で表されます。 |
| [!UICONTROL Attribute Set Ids] | 属性を割り当てる属性セットを示します。 属性は、通常、属性セットの一部になります。例えば、青、緑、黄、赤の属性を持つ色のセットなどです。 |
| [!UICONTROL Type] | 属性値の値のタイプを示します（テキストや数値など）。 選択は、属性に使用できる値に影響します。 |
| [!UICONTROL Use for Promo Rule Conditions] | 切り替え `Yes` を使用して、プロモーション条件内のパラメーターで属性を使用できるようにします。 |
| [!UICONTROL Used in Search] | 属性と値が製品検索で使用できるかどうかを示します。 |
| [!UICONTROL Comparable on Storefront] | 属性値がAmazonの「比較」機能で使用できるかどうかを示します。 |
| [!UICONTROL Magento Product Attribute Scope] | を示します。 [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) 属性の。 オプション：グローバル/ストア表示<br>に設定する場合 `Global`の場合、属性の作成後はストア表示を編集できません。 |
| [!UICONTROL Store Views (to import values into to)] | 範囲がに設定されている場合にのみ表示されます `Store View`. を選択します。 [ストア表示](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) Amazon属性値が同期される宛先です。 選択 `All Store Views (Global)` すべての値を更新 [!DNL Commerce] ストアビュー数。 |

## 属性の編集 {#edit-an-attribute}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューで、Amazon属性を探し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. リンクされた [!DNL Commerce] 属性、設定 **アクティブ** から `Yes` または `No`.

   に設定する場合 `Yes`の場合、値は設定に従って同期されます。

1. の場合 **[!UICONTROL Select Magento Product Attribute]**、選択したにマッピングする属性を確認または更新します。 **[!UICONTROL Amazon Attribute Name]**.

1. 読み込むAmazon属性値で既存の属性値を上書きするかどうかを示します。

   例えば、Amazonから [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**  — 値を保持し、 [!DNL Commerce] Amazon店

   - **[!UICONTROL Overwrite Existing Magento Values]** - [!DNL Commerce] 受信するAmazon値を含む製品カタログ。

1. 編集可能な場合は、1 つ以上の **[!UICONTROL Store Views (to import Amazon values into)]**.

   属性が `Global` 範囲、 _ストア表示_ 属性の作成後は変更できません。

   次を選択した場合： `All Store Views (Global)`を呼び出すと、値が同期され、すべてのストアビューに保存されます。 特定のストアビューにのみ値を同期する必要がある場合があります。

1. 完了したら、「 **[!UICONTROL Save Attribute Settings]**.

![属性設定を編集](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブかどうかを示し、Amazonと [!DNL Commerce]. をに設定します。 `Yes` Amazonと [!DNL Commerce] 選択した属性の同期を維持します。 |
| [!UICONTROL Select Magento Product Attribute] | 選択した [!DNL Commerce] 属性を指定します。 リンクされた [!DNL Commerce] 属性を選択し、ドロップダウンリストから別の属性を選択します。 値は設定に従って同期されます。 |
| [!UICONTROL Amazon Attribute Name] | Amazon属性の名前を表示します ( [!DNL Amazon Seller Central]. 選択した [!DNL Commerce] 属性は、このAmazon属性にリンクします。 この値は、 [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Amazon属性値が既存の値を上書きするかどうかを示します [!DNL Commerce] 値、この値を持つすべての製品に影響 [!DNL Commerce] 属性。<ul><li>**既存のMagento値を上書きしない** - （デフォルト） [!DNL Commerce] 値，異なる値を保持 [!DNL Commerce] Amazon店</li><li>**既存のMagento値を上書き** - Amazon値を [!DNL Commerce] 値を [!DNL Commerce] 商品カタログ。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | 属性が `Global` 範囲。 は、 [!DNL Commerce] [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) が作成され、に設定されている `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | 選択： [!DNL Commerce] [ストア表示](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) Amazon属性値の同期先となる。 選択 `All Store Views (Global)` すべてのストア表示で値を更新します。 |
