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

作成または更新 [!DNL Commerce] Amazonを通じて販売し、店舗を更新する際の属性。 現在のAmazon属性とリンクの確認 [!DNL Commerce] を使用した属性 [_[!UICONTROL Attributes]_表示](./attributes-view.md) （Amazon sales channel ホームページ）。 この_[!UICONTROL Action]_ 列には、属性で使用可能なアクションが表示されます。 新しいを作成してマッピングできます [!DNL Commerce] リンクされていないAmazon属性の属性。または既存の [!DNL Commerce] 属性と、Amazon属性へのマッピング。

属性を作成および更新する際に、の属性値を確認することをお勧めします。 [!DNL Commerce] とAmazon製品。 これらの値は、Amazonと同期して値をインポートしない場合は異なる可能性があります。 これらの属性のAmazon値を確認するには、を参照してください。 [Amazon属性マッピングの確認](./amazon-matching-attributes-values.md). これらの値を変更する場合は、次の操作を行います [マッピングの編集または作成](./amazon-manually-update-incomplete-listing.md) Amazonからまで [!DNL Commerce].

## 属性の作成 {#create-an-attribute}

以下の手順では、 [!DNL Commerce] 属性を設定し、Amazon属性にマッピングします。 設定によっては、カタログ間で値の同期が開始される場合があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューで、Amazon属性を見つけて、をクリックします。 **[!UICONTROL Create Attribute]** が含まれる _[!UICONTROL Action]_列。

1. リンクされたへのAmazon値の同期を有効にするには [!DNL Commerce] 属性、設定#ゾクセイ セッテイ# **[!UICONTROL Is Active]** 対象： `Yes`.

   に設定されている場合 `Yes`の場合、値は設定に応じて同期されます。

1. を選択 `Create New Magento Attribute` （用） **[!UICONTROL Select Magento Product Attribute]**.

   属性は、に選択されたにマッピングされます **[!UICONTROL Amazon Attribute Name]**.

1. を入力 **[!UICONTROL Magento Product Attribute Name]**.

1. を入力 **[!UICONTROL Magento Product Attribute Code]**.

   この値は、スペースを含めず、すべて小文字にする必要があります。

1. の場合 **[!UICONTROL Attribute Set Ids]**：割り当てる属性セットを選択します。

   通常、属性は属性セットの一部です。たとえば、青、緑、黄、赤の属性を持つ色のセットなどです。

1. の場合 **[!UICONTROL Type]**&#x200B;で、テキストや数値などの属性値のタイプを選択します。

   このオプションは、属性に使用できる値に影響します。

1. の場合 **[!UICONTROL Use for Promo Rule Conditions]**、に設定 `Yes` プロモーション条件内でパラメーターに属性を使用できるようにします。

1. の場合 **[!UICONTROL Used in Search]**、に設定 `Yes` 属性と値が製品の検索で使用できる場合。

1. の場合 **[!UICONTROL Comparable on Storefront]**、に設定 `Yes` 属性値がAmazonの「比較」機能で使用できる場合。

1. を選択します。 [!DNL Commerce] [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) 属性で、Amazon値の読み込み先の 1 つ以上のストアビューを選択します。

   範囲がに設定されている場合 `Global`, _[!UICONTROL Store View]_は、属性の作成後に変更できません。

   次を選択した場合： `All Store Views (Global)`を選択すると、値が同期され、Amazonのすべてのストアビューに保存されます。 特定のストアビューにのみ値を同期することができます。

1. 完了したら、 **[!UICONTROL Save Attribute Settings]**.

保存した後、設定を確認し、Amazonとに一致させるために、属性を編集することができます。 [!DNL Commerce] 属性の値。 また、Amazonの値を上書きするかどうかを指定することもできます [!DNL Commerce] 値。

![属性設定を作成](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブで、Amazonとの間でアクティブに同期されているかどうかを示します [!DNL Commerce]. をに設定 `Yes` Amazonからの属性値を確実に保持するには、および [!DNL Commerce] 選択した属性の同期を維持します。 |
| Magentoの製品属性を選択 | リストされたAmazonの属性名にリンクする、選択した属性を示します。 属性を作成する場合は、を選択します `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | 選択したAmazon属性の名前を示します。 選択した属性は、このAmazon属性にリンクしています。 この値は、を使用して編集することはできません [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | 属性名または「ラベル」を示します。 |
| [!UICONTROL Magento Product Attribute Code] | 属性コードを示します。すべて小文字で指定し、スペースは含めません。 |
| [!UICONTROL Attribute Set Ids] | 属性を割り当てる属性セットを示します。 属性は、青、緑、黄、赤の属性を持つ色のセットなど、属性セットの一部になる傾向があります。 |
| [!UICONTROL Type] | テキスト、数値など、属性値の値タイプを示します。 選択は、属性に使用できる値に影響します。 |
| [!UICONTROL Use for Promo Rule Conditions] | 切り替え `Yes` プロモーション条件内でパラメーターに属性を使用できるようにします。 |
| [!UICONTROL Used in Search] | 属性と値が製品検索で使用できるかどうかを示します。 |
| [!UICONTROL Comparable on Storefront] | Amazonの「比較」機能で属性値を使用できるかどうかを示します。 |
| [!UICONTROL Magento Product Attribute Scope] | は、 [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) 属性のを参照してください。 オプション：グローバル/ストア表示<br>に設定されている場合 `Global`を選択すると、属性の作成後にストア表示を編集することはできません。 |
| [!UICONTROL Store Views (to import values into to)] | 範囲がに設定されている場合にのみ表示されます `Store View`. を選択します。 [ストア表示](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) に変更した場合、Amazonの属性値が同期されます。 選択 `All Store Views (Global)` すべての値を更新します [!DNL Commerce] ビューを保存します。 |

## 属性の編集 {#edit-an-attribute}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. クリック **[!UICONTROL Attributes]** 左側のメニューで、Amazon属性を見つけて、をクリックします。 **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. リンクされたへのAmazon値の同期を有効または無効にするには [!DNL Commerce] 属性、設定#ゾクセイ セッテイ# **アクティブ** 対象： `Yes` または `No`.

   に設定されている場合 `Yes`の場合、値は設定に応じて同期されます。

1. の場合 **[!UICONTROL Select Magento Product Attribute]**、選択したにマッピングするために属性を検証または更新 **[!UICONTROL Amazon Attribute Name]**.

1. 受信Amazon属性値で既存の属性値を上書きするかどうかを指定します。

   例えば、Amazonの価格をに上書きしたくないことがあります [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]**  – 値を保持し、ユーザーに異なる値を保持します [!DNL Commerce] とAmazon ストアがあります。

   - **[!UICONTROL Overwrite Existing Magento Values]**  – の値を [!DNL Commerce] 受信したAmazon値を含む製品カタログ。

1. 編集できる場合は、1 つ以上を選択します **[!UICONTROL Store Views (to import Amazon values into)]**.

   で属性が作成された場合 `Global` 範囲、 _ストア表示_ は、属性の作成後に変更できません。

   次を選択した場合： `All Store Views (Global)`を選択すると、値が同期され、すべてのストアビューに保存されます。 特定のストアビューにのみ値を同期することができます。

1. 完了したら、 **[!UICONTROL Save Attribute Settings]**.

![属性設定を編集](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | この属性がライブで、Amazonとの間でアクティブに同期されているかどうかを示します [!DNL Commerce]. をに設定 `Yes` Amazonからの属性値を確実に保持するには、および [!DNL Commerce] 選択した属性の同期を維持します。 |
| [!UICONTROL Select Magento Product Attribute] | 選択されたを示します [!DNL Commerce] リストに表示されたAmazon属性名にリンクさせる属性。 リンクされた [!DNL Commerce] 属性。ドロップダウンリストから別の属性を選択します。 値は設定に従って同期されます。 |
| [!UICONTROL Amazon Attribute Name] | で定義されたAmazon属性の名前を示します。 [!DNL Amazon Seller Central]. 選択された [!DNL Commerce] 属性は、このAmazon属性にリンクしています。 この値は、を使用して編集することはできません [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Amazon属性値が既存の値を上書きするかどうかを示します [!DNL Commerce] 値、この値を含むすべての製品に影響する [!DNL Commerce] 属性。<ul><li>**既存のMagentoー値を上書きしない** - （デフォルト）を保持 [!DNL Commerce] 値、異なる値を保持#アタイシキ# [!DNL Commerce] とAmazon ストアがあります。</li><li>**既存のMagento値を上書き** - Amazonの値を [!DNL Commerce] の値 [!DNL Commerce] 商品カタログ。</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | で作成された属性の場合、その属性を編集するときに表示されない `Global` スコープ。 は、次のことを示します [!DNL Commerce] [範囲](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) が作成され、に設定されました `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | を選択 [!DNL Commerce] [ストア表示](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) :Amazonの属性値を同期します。 選択 `All Store Views (Global)` すべてのストアビューの値を更新します。 |
