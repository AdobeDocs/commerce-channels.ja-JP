---
title: AmazonのCommerce属性の作成
description: Amazon セールスチャネルのオンボーディングプロセスを完了する前に、必要なものを用意します [!UICONTROL Commerce] 製品属性。
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# AmazonのCommerce属性の作成

オンボーディングの前に [!DNL Amazon Seller Central] アカウントの場合、次を追加することがベストプラクティスです [!DNL Commerce] [製品属性](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) 製品リストをマッピングします。 オンボーディングが完了したら、以下を通じて製品属性を管理できます。 [属性](./managing-attributes.md) タブ [Amazon販売チャネルホーム](./amazon-sales-channel-home.md) ページ。

この手順では、の作成方法について詳しく説明します [!DNL Commerce] Amazon ASIN およびAmazon条件の属性。 Amazon EAN、Amazon ISBN、Amazon UPC などの属性を追加することをお勧めします。 また、Amazonの価格を価格ルールの価格ソースとして使用する場合は、Amazonの価格属性を作成することもできます。 これらの属性は、オンボーディング中にリストと価格の設定を行う際に使用されます。 また、これらの属性は、Amazonのリストを作成する際や、 [!DNL Commerce] Amazonのリストを使用したカタログ。

カタログ検索設定を使用すると、対象をマッピングするのに役立つ、一致する検索パラメーターを設定できます [!DNL Commerce] Amazonの製品リストを使用した製品。 マッピングされると、Amazonでは価格設定、数量、オーバーライド、注文と商品の同期に関連するアクションがアクティブになります。

これらの値を定義すると、完全一致の可能性が高まり、後で製品リストを手動で一致させる必要が最小限に抑えられます。 オンボーディングの一環としての属性の追加 [事前設定タスク](./amazon-pre-setup-tasks.md)を使用すると、Amazonのセールスチャネルは、オンボーディング中に商品を自動的に照合し、Amazonとの間で商品データを同期する可能性が高くなります [!DNL Commerce] オンボーディング後。

Amazonの ASIN 属性のみを作成し（製品ごとの ASIN 値を追加しない）、 [!DNL Commerce] 商品がAmazonのリストと自動的に一致しない場合があります。 を使用すると、製品を手動で一致させることができます _ストアのレビュー_. ただし、手動での照合では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>手動で一致した製品の ASIN、UPC またはその他のデータ要素を更新する場合は、次の両方の場所でデータを更新する必要があります。 [!DNL Commerce] カタログとリスト [!DNL Amazon Seller Central] アカウント。

## Amazon ASIN 製品属性の作成

1. にログイン [!DNL Commerce] 管理者。

1. クリック **[!UICONTROL Stores]** 左側のメニューの

1. が含まれる _[!UICONTROL Attributes]_セクションで、をクリック&#x200B;**[!UICONTROL Product]**.

1. 属性プロパティを開くには、をクリックします。 **[!UICONTROL Add New Attribute]**.

1. の場合 **[!UICONTROL Default Label]**、と入力します `Amazon ASIN` （属性の名前）。

1. の場合 **[!UICONTROL Catalog Input Type for Store Owner]**、を選択 `Text Field`.

1. の場合 **[!UICONTROL Values Required]**、を選択 `No`.

   Amazonに商品を一覧表示するにはAmazon ASIN が必要ですが、カタログ商品の一部がAmazonに一覧表示されない場合があります。

1. を展開します。 _[!UICONTROL Advanced Attribute Properties]_「」セクションを選択して、次のオプションを設定します。

   - の場合 **[!UICONTROL Attribute Code]**、と入力します `amazon_asin`.

   - の場合 **[!UICONTROL Scope]**、を選択 `Global`.

   - の場合 **[!UICONTROL Unique Value]**、を選択 `No`.

   - の場合 **[!UICONTROL Input Validation for Store Owner]**、を選択 `None`.

   - の場合 **[!UICONTROL Add to Column Options]**、を選択 `Yes`.

   - の場合 **[!UICONTROL Use in Filter Options]**、を選択 `Yes`.

1. クリック **[!UICONTROL Save Attribute]**.

![Amazon ASIN 属性](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## 「Amazon条件」製品属性の作成

1. にログイン [!DNL Commerce] 管理者。

1. クリック **[!UICONTROL Stores]** 左側のメニューの

1. が含まれる _[!UICONTROL Attributes]_セクションで、をクリック&#x200B;**[!UICONTROL Product]**.

1. 属性プロパティを開くには、をクリックします。 **[!UICONTROL Add New Attribute]**.

1. の場合 **[!UICONTROL Default Label]**、と入力します `Amazon Condition` （属性の名前）。

1. の場合 **[!UICONTROL Catalog Input Type for Store Owner]**、を選択 `Dropdown`.

   この _[!UICONTROL Manage Options (Values of your Attribute)]_セクションが表示されます。

1. の場合 **[!UICONTROL Values Required]**、を選択 `No`.

1. の場合 **[!UICONTROL Manage Options (Values for your Attribute)]**&#x200B;条件の各オプションを追加します。

   Amazonの標準的な条件は次のとおりです。

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. クリック **[!UICONTROL Add Option]**.

1. 「」を選択します **[!UICONTROL Is Default]** デフォルトとして選択する条件のオプション。

1. が含まれる _[!UICONTROL Admin]_列に、追加する条件のラベルのテキスト（など）を入力します `New`, `Used`、および `Used-Like New`）

1. クリック **[!UICONTROL Add Option]** 必要に応じて、オプションを追加します。

1. を展開 _[!UICONTROL Advanced Attribute Properties]_を選択して、オプションを設定します。

   - の場合 **[!UICONTROL Attribute Code]**、と入力します `amazon_condition`.

   - の場合 **[!UICONTROL Scope]**、を選択 `Global`.

   - の場合 **[!UICONTROL Unique Value]**、を選択 `No`.

   - の場合 **[!UICONTROL Input Validation for Store Owner]**、を選択 `None`.

   - の場合 **[!UICONTROL Add to Column Options]**、を選択 `Yes`.

   - の場合 **[!UICONTROL Use in Filter Options]**、を選択 `Yes`.

1. クリック **[!UICONTROL Save Attribute]**.

![Amazon条件属性](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![次へアイコン](assets/btn-next.png) [**API キーの追加または検証を続行**](./amazon-verify-api-key.md)
