---
title: Alias Amazon Seller SKU の作成
description: Alias Amazon Seller SKU を使用して、コマースカタログ製品から複数の地域のAmazonリストを作成できます。
feature: Sales Channels, Products
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Alias Amazon Seller SKU の作成

An [!DNL Alias Amazon Seller SKU] を使用して、 [!DNL Commerce] カタログ。 経験豊富なAmazonの販売者であれば、 [Amazon Global SKU](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} および Marketplace 固有の SKU（在庫および出荷用）。 Amazonセールスチャネルに関する同様の原則に従い、Amazonセラー SKU は、複数の地域レベルで製品リスト情報を制御し、 [!DNL Alias Amazon Seller SKU] を使用して、地域固有のレベルで製品リスト情報を制御できます。

この関数は、次の 2 つの機能を実行するために使用できます。

- の作成 [!DNL Alias Amazon Seller SKU] お客様の [!DNL Commerce] 地域固有のリスト情報を制御するカタログ製品。

  **例**：米国とカナダの両方の地域の販売者です。 Amazonの各セールスチャネルストアに割り当てることができるAmazon地域は、セットアップ時に 1 つだけです。 そのため、米国の地域が定義されたAmazonのセールスチャネルストアと、カナダの地域が定義された別のストアがあります。 両方のストアが [!DNL Commerce] Amazonの売り手の SKU および ASIN の製品属性を含む、両方の地域の情報を一覧表示するためのカタログ。 したがって、カタログ商品のリストは、店舗、共有価格、在庫/数量、その他の製品属性の両方で同じになります。 しかし、カナダの店舗の在庫はカナダの場所から出荷され、米国の店舗は米国の場所から出荷されます。 したがって、各店舗ごとに個別にリストのリスト数を制御する必要があります。 このタイプの地域固有のコントロールを実現するには、Alias Amazon Seller SKU を作成します。

  基本的には、同じカタログ製品にリンクされ、その地域で同じリストを再公開するために使用できる、Alias Amazon Seller SKU を作成できます。

- の作成 [!DNL Alias Amazon Seller SKU] お使いの [!DNL Commerce] 2 つのAmazonリストに商品をカタログ化

  **例**:Amazonリストと一致するカタログ製品があります。 Amazonには同じ製品を表す複数のリストが頻繁に存在するので、同じ製品の別のAmazonリストが見つかりますが、Amazonには別の ASIN が割り当てられています。 商品の可視性を高めるには、カタログ商品を別の ASIN と照合し、両方の ASIN 値のリストを作成します。 これを達成するには、Alias Amazon Seller SKU を作成します。

  基本的に、 [!DNL Alias Amazon Seller SKU] これは、1 つのカタログ製品を 2 つ目のAmazonリストに一致させ、新しく一致した ASIN のリストを作成するために使用できます。 このシナリオでは、同じカタログ製品に対して 2 つのAmazonリストを使用します。

  Alias Amazon Seller SKU を作成したら、リスト設定、ルールおよび上書きを使用して、その地域のリスト情報を制御できます。 リストのリストに対してリージョンごとに定義できる製品属性には、数量/在庫、達成方法、条件、製品適格、処理時間などがあります。

## 地域固有の目的で使用 {#region-specific}

リストを _[!UICONTROL Product Listings]_ページ (_[!UICONTROL Inactive]_, _アクティブ_, _不適格_&#x200B;または _終了_ 」タブ ) をクリックします。

1. の下 _[!UICONTROL Actions]_をクリックし、**[!UICONTROL Create Alias Seller SKU]**.

1. の場合 **[!UICONTROL Assign New Seller SKU]**」に、一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用しません）。

1. の場合 **[!UICONTROL Assign New ASIN]**、変更を加えない。

   この値は、カタログ商品と一致する商品 ASIN で自動入力されます。 この値を変更すると、ASIN に基づく 2 つのAmazonリストにカタログ製品が一致します。

1. 切り替え **[!UICONTROL Remove Existing Seller SKU]** オプションを選択します。

   - `Yes`  — リストを削除し、提供された新しい情報を使用してリストを作成することを選択します。

   - `No`  — リストを作成し、古いリストは変更しないでください。

1. クリック **[!UICONTROL Save Listing Update]**.

## 1 つのカタログ製品を 2 つのAmazonリストに一致させるために使用します

1. リストを _[!UICONTROL Product Listings]_ページ (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_&#x200B;または _[!UICONTROL Ended]_」タブ ) を参照してください。

1. の下 _[!UICONTROL Actions]_をクリックし、**[!UICONTROL Create Alias Seller SKU]**.

1. の場合 **[!UICONTROL Assign New Seller SKU]**」に、一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用しません）。

1. の場合 **[!UICONTROL Assign New ASIN]**」に、一意の英数字の値を入力します。

   この値は、カタログ商品と一致する商品 ASIN で自動入力されます。 この値を変更すると、ASIN に基づく 2 つのAmazonリストにカタログ製品が一致します。

1. 切り替え **[!UICONTROL Remove Existing Seller SKU]** オプションを選択します。

   - `Yes`  — リストを削除し、提供された新しい情報を使用してリストを作成することを選択します。

   - `No`  — 別のリストを作成し、古いリストは変更しないでください。

1. クリック **[!UICONTROL Save Listing Update]**.

![Alias Amazon Seller SKU の作成](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | 元のAmazon販売者 SKU にリンクする新しい一意の英数字の値を入力します。 この数は、Amazonのセールスチャネルでカタログ製品と照合するためにのみ使用されます。 任意の SKU 値を使用できますが、カタログでは 1 回だけ使用できます。 |
| [!UICONTROL Assign New ASIN] | カタログ商品を照合するリストの ASIN 値を入力します。 同じ製品の別のリストに対して 1 つのカタログ製品を ASIN と照合する場合にのみ、このフィールドを変更します。 この値は、Amazonが割り当てた ASIN と一致する必要があります。一致しない場合、Amazonがリストを拒否することはありません。 |
| [!UICONTROL Remove Existing Seller SKU] | オプション：<ul><li>**[!UICONTROL Yes]**  — リストを削除し、提供された新しい情報を使用してリストを作成することを選択します。 新しいリストが _[!UICONTROL Active]_」タブに移動した場合、古いリストは_&#x200B;終了&#x200B;_タブをクリックします。</li><li>**[!UICONTROL No]**  — 別のリストを作成し、古いリストは変更しないでください。 両方のリストは、新しいリストが作成された後、[ アクティブ ] タブに表示されます。</li></ul> |
