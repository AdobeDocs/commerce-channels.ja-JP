---
title: Amazonのコマース属性の作成
description: Amazonセールスチャネルのオンボーディングプロセスを完了する前に、必要な情報が揃っていることを確認します。 [!UICONTROL Commerce] 製品属性。
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Amazonのコマース属性の作成

オンボーディングの前に [!DNL Amazon Seller Central] アカウントを追加する場合は、 [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) 製品リストをマッピングするには： オンボーディングが完了したら、 [属性](./managing-attributes.md) タブ [Amazonセールスチャネルホーム](./amazon-sales-channel-home.md) ページに貼り付けます。

以下の手順で、 [!DNL Commerce] Amazon ASIN とAmazon条件の属性。 Amazon EAN、Amazon ISBN、Amazon UPC などの追加の属性を作成することをお勧めします。 Amazon上場価格を価格設定ルールの価格ソースとして使用する場合は、 Amazon Price 属性も作成できます。 これらの属性は、オンボーディング時にリストと価格の設定を指定する際に使用します。 また、Amazonのリストを作成する際や、の更新と同期をおこなう際にも、これらの属性を使用します [!DNL Commerce] カタログとAmazonのリスト。

カタログ検索設定を使用すると、対象をマッピングするのに役立つ一致する検索パラメーターを設定できます [!DNL Commerce] Amazonリストに含まれる製品。 マッピングが完了すると、Amazonは、価格、数量、上書き、注文および製品の同期に関連するアクションを有効化します。

これらの値を定義すると完全一致の可能性が高まり、後で製品リストを手動で照合する必要が最小限に抑えられます。 オンボーディングの一環として属性を追加する [事前設定タスク](./amazon-pre-setup-tasks.md)Amazonセールスチャネルは、Amazonとの間で製品データのオンボーディングおよび同期をおこなう際に、製品を自動的に照合する可能性が高くなります [!DNL Commerce] オンボーディング後

Amazon ASIN 属性のみを作成する場合（製品ごとに ASIN 値を追加しない場合）、 [!DNL Commerce] 製品は、Amazonのリストと自動的に一致しない場合があります。 手動で製品を照合するには、 _ストアレビュー_. ただし、手動での照合では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>手動で一致した製品に対して ASIN、UPC、または他のデータ要素を更新する場合は、両方の場所でデータを更新する必要があります。 [!DNL Commerce] カタログとリスト ( [!DNL Amazon Seller Central] アカウント。

## Amazon ASIN 製品属性の作成

1. 次にログイン： [!DNL Commerce] 管理者。

1. クリック **[!UICONTROL Stores]** をクリックします。

1. Adobe Analytics の _[!UICONTROL Attributes]_セクションで、**[!UICONTROL Product]**.

1. 属性プロパティを開くには、 **[!UICONTROL Add New Attribute]**.

1. の場合 **[!UICONTROL Default Label]**，と入力します。 `Amazon ASIN` （属性の名前）。

1. の場合 **[!UICONTROL Catalog Input Type for Store Owner]**&#x200B;を選択します。 `Text Field`.

1. の場合 **[!UICONTROL Values Required]**&#x200B;を選択します。 `No`.

   Amazon上の製品をリストするにはAmazon ASIN が必要ですが、一部のカタログ製品がAmazon上に表示されない場合があります。

1. を展開します。 _[!UICONTROL Advanced Attribute Properties]_」セクションに移動して、次のオプションを設定します。

   - の場合 **[!UICONTROL Attribute Code]**，と入力します。 `amazon_asin`.

   - の場合 **[!UICONTROL Scope]**&#x200B;を選択します。 `Global`.

   - の場合 **[!UICONTROL Unique Value]**&#x200B;を選択します。 `No`.

   - の場合 **[!UICONTROL Input Validation for Store Owner]**&#x200B;を選択します。 `None`.

   - の場合 **[!UICONTROL Add to Column Options]**&#x200B;を選択します。 `Yes`.

   - の場合 **[!UICONTROL Use in Filter Options]**&#x200B;を選択します。 `Yes`.

1. クリック **[!UICONTROL Save Attribute]**.

![Amazon ASIN 属性](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## Amazon Condition 製品属性の作成

1. 次にログイン： [!DNL Commerce] 管理者。

1. クリック **[!UICONTROL Stores]** をクリックします。

1. Adobe Analytics の _[!UICONTROL Attributes]_セクションで、**[!UICONTROL Product]**.

1. 属性プロパティを開くには、 **[!UICONTROL Add New Attribute]**.

1. の場合 **[!UICONTROL Default Label]**，と入力します。 `Amazon Condition` （属性の名前）。

1. の場合 **[!UICONTROL Catalog Input Type for Store Owner]**&#x200B;を選択します。 `Dropdown`.

   The _[!UICONTROL Manage Options (Values of your Attribute)]_セクションが表示されます。

1. の場合 **[!UICONTROL Values Required]**&#x200B;を選択します。 `No`.

1. の場合 **[!UICONTROL Manage Options (Values for your Attribute)]**、各条件オプションを追加します。

   標準のAmazon条件は次のとおりです。

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. クリック **[!UICONTROL Add Option]**.

1. を選択します。 **[!UICONTROL Is Default]** オプションを選択します。

1. Adobe Analytics の _[!UICONTROL Admin]_列に、追加する条件のラベルのテキストを入力します ( 例： `New`, `Used`、および `Used-Like New`)

1. クリック **[!UICONTROL Add Option]** 必要に応じてオプションを追加します。

1. 展開 _[!UICONTROL Advanced Attribute Properties]_」セクションに移動して、オプションを設定します。

   - の場合 **[!UICONTROL Attribute Code]**，と入力します。 `amazon_condition`.

   - の場合 **[!UICONTROL Scope]**&#x200B;を選択します。 `Global`.

   - の場合 **[!UICONTROL Unique Value]**&#x200B;を選択します。 `No`.

   - の場合 **[!UICONTROL Input Validation for Store Owner]**&#x200B;を選択します。 `None`.

   - の場合 **[!UICONTROL Add to Column Options]**&#x200B;を選択します。 `Yes`.

   - の場合 **[!UICONTROL Use in Filter Options]**&#x200B;を選択します。 `Yes`.

1. クリック **[!UICONTROL Save Attribute]**.

![Amazon条件属性](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![次のアイコン](assets/btn-next.png) [**API キーの追加または検証を続行します。**](./amazon-verify-api-key.md)
