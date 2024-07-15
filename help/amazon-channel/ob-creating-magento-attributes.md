---
title: AmazonのCommerce属性の作成
description: Amazon セールスチャネルのオンボーディングプロセスを完了する前に、必要な [!UICONTROL Commerce] 製品属性があることを確認します。
role: Admin
feature: Sales Channels, Products, Configuration
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# AmazonのCommerce属性の作成

[!DNL Amazon Seller Central] アカウントをオンボーディングする前に、[!DNL Commerce] [ 製品属性 ](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) を追加して、製品リストをマッピングすることをお勧めします。 オンボーディングが完了したら、[Amazon販売チャネルホーム [ ページの ](./managing-attributes.md) 属性 ](./amazon-sales-channel-home.md) タブで製品属性を管理できます。

これらの手順では、Amazon ASIN とAmazon条件の [!DNL Commerce] 属性を作成する方法について詳しく説明します。 Amazon EAN、Amazon ISBN、Amazon UPC などの属性を追加することをお勧めします。 また、Amazonの価格を価格ルールの価格ソースとして使用する場合は、Amazonの価格属性を作成することもできます。 これらの属性は、オンボーディング中にリストと価格の設定を行う際に使用されます。 また、これらの属性は、Amazonのリストを作成する際や、[!DNL Commerce] カタログを更新してAmazonのリストと同期する際にも使用します。

カタログ検索を使用すると、条件を満たす [!DNL Commerce] 品をAmazonのリストにマッピングするのに役立つ、一致する検索パラメーターを設定できます。 マッピングされると、Amazonでは価格設定、数量、オーバーライド、注文と商品の同期に関連するアクションがアクティブになります。

これらの値を定義すると、完全一致の可能性が高まり、後で製品リストを手動で一致させる必要が最小限に抑えられます。 Amazon セールスチャネルは、オンボーディング [ 事前設定タスク ](./amazon-pre-setup-tasks.md) の一環として属性を追加することで、オンボーディング中に商品を自動的に照合し、オンボーディング後にAmazonと [!DNL Commerce] の間で商品データを同期する可能性が高くなります。

Amazonの ASIN 属性のみを作成する（製品ごとの ASIN 値を追加しない）場合、[!DNL Commerce] の製品はAmazonのリストと自動的に一致しない可能性があります。 _ストアレビュー_ を通じて、製品を手動で一致させることができます。 ただし、手動での照合では、製品データの共有と同期に必要なデータ要素は作成されません。

>[!IMPORTANT]
>
>手動で一致した製品の ASIN、UPC、またはその他のデータ要素を更新する場合は、[!DNL Commerce] カタログと [!DNL Amazon Seller Central] アカウントのリストの両方でデータを更新する必要があります。

## Amazon ASIN 製品属性の作成

1. [!DNL Commerce] 管理者にログインします。

1. 左側のメニューの「**[!UICONTROL Stores]**」をクリックします。

1. 「_[!UICONTROL Attributes]_」セクションで、「**[!UICONTROL Product]**」をクリックします。

1. 属性プロパティを開くには、「**[!UICONTROL Add New Attribute]**」をクリックします。

1. **[!UICONTROL Default Label]** には、`Amazon ASIN` （属性の名前）と入力します。

1. **[!UICONTROL Catalog Input Type for Store Owner]** の場合は、「`Text Field`」を選択します。

1. **[!UICONTROL Values Required]** の場合は、「`No`」を選択します。

   Amazonに商品を一覧表示するにはAmazon ASIN が必要ですが、カタログ商品の一部がAmazonに一覧表示されない場合があります。

1. _[!UICONTROL Advanced Attribute Properties]_セクションを展開し、オプションを設定します。

   - **[!UICONTROL Attribute Code]** には、`amazon_asin` と入力します。

   - **[!UICONTROL Scope]** の場合は、「`Global`」を選択します。

   - **[!UICONTROL Unique Value]** の場合は、「`No`」を選択します。

   - **[!UICONTROL Input Validation for Store Owner]** の場合は、「`None`」を選択します。

   - **[!UICONTROL Add to Column Options]** の場合は、「`Yes`」を選択します。

   - **[!UICONTROL Use in Filter Options]** の場合は、「`Yes`」を選択します。

1. 「**[!UICONTROL Save Attribute]**」をクリックします。

![Amazon ASIN 属性 ](assets/creating-asin-attribute.png){width="600" zoomable="yes"}

## 「Amazon条件」製品属性の作成

1. [!DNL Commerce] 管理者にログインします。

1. 左側のメニューの「**[!UICONTROL Stores]**」をクリックします。

1. 「_[!UICONTROL Attributes]_」セクションで、「**[!UICONTROL Product]**」をクリックします。

1. 属性プロパティを開くには、「**[!UICONTROL Add New Attribute]**」をクリックします。

1. **[!UICONTROL Default Label]** には、`Amazon Condition` （属性の名前）と入力します。

1. **[!UICONTROL Catalog Input Type for Store Owner]** の場合は、「`Dropdown`」を選択します。

   _[!UICONTROL Manage Options (Values of your Attribute)]_セクションが表示されます。

1. **[!UICONTROL Values Required]** の場合は、「`No`」を選択します。

1. **[!UICONTROL Manage Options (Values for your Attribute)]** しくは、各条件オプションを追加します。

   Amazonの標準的な条件は次のとおりです。

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. 「**[!UICONTROL Add Option]**」をクリックします。

1. デフォルトに設定する条件の **[!UICONTROL Is Default]** のオプションを選択します。

1. _[!UICONTROL Admin]_列に、追加する条件のラベルのテキスト（`New`、`Used`、`Used-Like New` など）を入力します

1. 必要に応じて、「**[!UICONTROL Add Option]**」をクリックしてオプションをさらに追加します。

1. セクション _[!UICONTROL Advanced Attribute Properties]_展開し、オプションを設定します。

   - **[!UICONTROL Attribute Code]** には、`amazon_condition` と入力します。

   - **[!UICONTROL Scope]** の場合は、「`Global`」を選択します。

   - **[!UICONTROL Unique Value]** の場合は、「`No`」を選択します。

   - **[!UICONTROL Input Validation for Store Owner]** の場合は、「`None`」を選択します。

   - **[!UICONTROL Add to Column Options]** の場合は、「`Yes`」を選択します。

   - **[!UICONTROL Use in Filter Options]** の場合は、「`Yes`」を選択します。

1. 「**[!UICONTROL Save Attribute]**」をクリックします。

![Amazon条件属性 ](assets/creating-amazon-condition-attribute.png){width="600" zoomable="yes"}

![ 次へアイコン ](assets/btn-next.png)[**API キーの追加または確認を続行**](./amazon-verify-api-key.md)
