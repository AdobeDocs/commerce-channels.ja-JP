---
title: ' [!DNL Commerce] Amazon の属性を作成します。'
description: Amazon 販売チャンネルのオンボードプロセスを完了する前に、必要な製品属性があることを確認してください [!UICONTROL Commerce] 。
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# [!DNL Commerce]Amazon の属性を作成します。

取引先企業をオンにする前に、製品の属性を追加することをお勧めし [!DNL Amazon Seller Central] ます。これは、製品 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/stores/attributes-product.html) リストのマップを作成するには、{target = &quot;_blank&quot;} です。 オンボードを完了すると、 [ ](./managing-attributes.md) Amazon sales channel のホームページの「属性」タブを使用して製品属性を管理することができ [ ](./amazon-sales-channel-home.md) ます。

この手順 [!DNL Commerce] では、AMAZON アークや Amazon 条件に属性を作成する方法について詳しく説明しています。 Amazon EAN、Amazon ISBN、Amazon UPC など、追加の属性を作成することをお勧めします。 このような場合は、amazon Price 属性を作成すると、その価格設定ルールの価格のソースとして Amazon の表示価格を使用することもできます。 これらの属性は、オンになっているときにリスティングおよび価格設定を構成するときに使用されます。 この属性は、Amazon リストを作成する場合や、Amazon リストを使用してカタログをアップデートおよび同期する場合にも使用でき [!DNL Commerce] ます。

カタログ検索の設定を使用すると、Amazon リストを含む適格な製品をマップするための一致検索パラメーターを設定でき [!DNL Commerce] ます。 マップされた場合、Amazon は価格、数量、オーバーライド、および注文と製品の同期に関するアクションがアクティブになります。

このような値を定義すると、完全に一致する可能性が高くなるので、後で製品リストを手動で一致させる必要はありません。 事前設定タスクの一部として属性を追加すると [ ](./amazon-pre-setup-tasks.md) 、amazon sales channel によって、オンボード中に自動的に製品が照合され、Amazon とオンボードの間の製品データが同期される可能性が高くなり [!DNL Commerce] ます。

Amazon の &quot;属性&quot; 属性を作成するのは、製品ごとにアーク秒数を追加するのではなく、 [!DNL Commerce] 製品が amazon リストに自動的に一致しない場合があります。 製品は、ストアレビューによって手動で一致させることができ __ ます。 ただし、手動検索では、製品データの共有と同期に必要なデータエレメントは作成されません。

>[!IMPORTANT]
>
>合致する製品について、アーク、UPC、またはその他のデータエレメントを更新する場合は、両方の場所でデータを更新する必要があります。 [!DNL Commerce] カタログと、口座に記載されているリストです。 [!DNL Amazon Seller Central]

## Amazon アーク積属性の作成

1. [!DNL Commerce]管理者にログインします。

1. **[!UICONTROL Stores]**&#x200B;左側のメニューでクリックします。

1. セクションの _[!UICONTROL Attributes]_をクリックし&#x200B;**[!UICONTROL Product]**ます。

1. 属性のプロパティを表示するには、をクリックし **[!UICONTROL Add New Attribute]** ます。

1. **[!UICONTROL Default Label]**&#x200B;では、 `Amazon ASIN` 属性の名前を入力します。

1. について **[!UICONTROL Catalog Input Type for Store Owner]** は、を選択 `Text Field` します。

1. について **[!UICONTROL Values Required]** は、を選択 `No` します。

   Amazon によって、amazon によって製品が一覧表示されますが、amazon によっては、一部のカタログ製品がリストに表示されない場合があります。

1. セクションを展開 _[!UICONTROL Advanced Attribute Properties]_し、次のオプションを設定します。

   - につい **[!UICONTROL Attribute Code]** ては、「」を入力し `amazon_asin` ます。

   - について **[!UICONTROL Scope]** は、を選択 `Global` します。

   - について **[!UICONTROL Unique Value]** は、を選択 `No` します。

   - について **[!UICONTROL Input Validation for Store Owner]** は、を選択 `None` します。

   - について **[!UICONTROL Add to Column Options]** は、を選択 `Yes` します。

   - について **[!UICONTROL Use in Filter Options]** は、を選択 `Yes` します。

1. をクリックし **[!UICONTROL Save Attribute]** ます。

![Amazon アーク属性](assets/creating-asin-attribute.png)

## Amazon Condition 製品属性の作成

1. [!DNL Commerce]管理者にログインします。

1. **[!UICONTROL Stores]**&#x200B;左側のメニューでクリックします。

1. セクションの _[!UICONTROL Attributes]_をクリックし&#x200B;**[!UICONTROL Product]**ます。

1. 属性のプロパティを表示するには、をクリックし **[!UICONTROL Add New Attribute]** ます。

1. **[!UICONTROL Default Label]**&#x200B;では、 `Amazon Condition` 属性の名前を入力します。

1. について **[!UICONTROL Catalog Input Type for Store Owner]** は、を選択 `Dropdown` します。

   _[!UICONTROL Manage Options (Values of your Attribute)]_セクションが表示されます。

1. について **[!UICONTROL Values Required]** は、を選択 `No` します。

1. については **[!UICONTROL Manage Options (Values for your Attribute)]** 、条件の各オプションを追加します。

   標準的な Amazon 条件は、次のとおりです。

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. をクリックし **[!UICONTROL Add Option]** ます。

1. **[!UICONTROL Is Default]**&#x200B;初期設定の選択範囲にする条件のオプションを選択します。

1. 「」 _[!UICONTROL Admin]_列に、追加する条件のラベルのテキストを入力します (、、、など `New` `Used` `Used-Like New` )

1. 必要に応じ **[!UICONTROL Add Option]** てオプションを追加するには、これをクリックします。

1. _[!UICONTROL Advanced Attribute Properties]_「セクションを展開」を選択して、オプションを設定します。

   - につい **[!UICONTROL Attribute Code]** ては、「」を入力し `amazon_condition` ます。

   - について **[!UICONTROL Scope]** は、を選択 `Global` します。

   - について **[!UICONTROL Unique Value]** は、を選択 `No` します。

   - について **[!UICONTROL Input Validation for Store Owner]** は、を選択 `None` します。

   - について **[!UICONTROL Add to Column Options]** は、を選択 `Yes` します。

   - について **[!UICONTROL Use in Filter Options]** は、を選択 `Yes` します。

1. をクリックし **[!UICONTROL Save Attribute]** ます。

![Amazon Condition 属性](assets/creating-amazon-condition-attribute.png)

![次 ](assets/btn-next.png) [**のアイコンをクリックすると、API キーの追加または検証が続行します。**](./amazon-verify-api-key.md)
