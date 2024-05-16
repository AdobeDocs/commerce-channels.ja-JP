---
title: Alias Amazon販売者 SKU の作成
description: Alias Amazon Seller SKU を使用して、Commerceカタログ商品から複数の地域に対応するAmazonリストを作成できます。
feature: Sales Channels, Products
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---

# Alias Amazon販売者 SKU の作成

An [!DNL Alias Amazon Seller SKU] は、内の同じ商品からAmazonのリストを作成するために使用されます [!DNL Commerce] カタログ。 経験豊富なAmazonのセラーであれば、に精通しているかもしれません。 [Amazon グローバル SKU](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} 在庫および配送用のマーケットプレイス固有の SKU。 Amazon販売チャネルと同様の原則に従って、Amazon販売者 SKU は、複数の地域レベルで商品リスト情報を制御します。 [!DNL Alias Amazon Seller SKU] 地域固有のレベルで製品リスト情報を制御するために使用できます。

この関数は、次の 2 つの関数を実行するために使用できます。

- を作成 [!DNL Alias Amazon Seller SKU] ユーザーのアカウントの場合 [!DNL Commerce] 地域固有のリスト情報を管理するカタログ製品。

  **例**：あなたは米国とカナダの両方の地域で売り手です。 セットアップ時に、Amazonの各セールスチャネルストアに割り当てることができるAmazonリージョンは 1 つだけであることに注意してください。 つまり、米国リージョンが定義されたAmazonのセールスチャネルストアと、カナダ リージョンが定義された別のストアがあるということです。 両方のストアで [!DNL Commerce] Amazonの販売者 SKU と ASIN 製品属性を含む、両方の地域の情報をリストするカタログ。 したがって、カタログ製品のリストは、価格、在庫/数量、その他の製品属性を共有して、両方の店舗で同じになります。 ただし、カナダの店舗の在庫はカナダの場所から、米国の店舗の在庫は米国の場所から出荷されます。 したがって、リストのリスト数量は、ストアごとに個別に制御する必要があります。 このタイプの地域固有のコントロールを実現するには、Alias Amazon販売者 SKU を作成します。

  基本的に、同じカタログ商品にリンクされ、そのリージョンで同じリストを再公開するために使用できる Alias Amazonの販売者 SKU を作成できます。

- を作成 [!DNL Alias Amazon Seller SKU] を検索して、いずれかの [!DNL Commerce] 2 つのAmazonリストへのカタログ製品。

  **例**:Amazonのリストと一致するカタログ商品があります。 Amazonには、同じ商品を表す複数のリストが頻繁に存在するので、同じ商品に対して別のAmazonのリストを発見しましたが、Amazonは別の ASIN をリストに割り当てました。 製品の表示域を含めるようにするには、カタログ製品を別の ASIN と一致させ、両方の ASIN 値の一覧を作成します。 これを実現するには、Alias Amazon販売者 SKU を作成します。

  基本的には、以下を作成できます。 [!DNL Alias Amazon Seller SKU] これを使用すれば、1 つのカタログ商品を 2 つ目のAmazon リストと照合し、新しく一致した ASIN のリストを作成できます。 このシナリオでは、同じカタログ商品に対して 2 つのAmazonのリストが作成されます。

  Alias Amazon Seller SKU を作成したら、リスト設定、ルール、上書きを使用して、リージョンのリスト情報を制御できます。 リストの地域ごとに定義できる製品属性には、数量/在庫、履行方法、条件、製品の適格性、処理時間などがあります。

## 地域固有の目的に使用されます {#region-specific}

のリストを表示 _[!UICONTROL Product Listings]_ページ （_[!UICONTROL Inactive]_, _アクティブ_, _不適格_、または _終了_ タブ）。

1. 次の下 _[!UICONTROL Actions]_を選択し、**[!UICONTROL Create Alias Seller SKU]**.

1. の場合 **[!UICONTROL Assign New Seller SKU]**&#x200B;一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用されません）。

1. の場合 **[!UICONTROL Assign New ASIN]**&#x200B;何も変更しないでください。

   この値は、カタログ製品に一致する製品 ASIN を自動入力します。 この値を変更すると、カタログ製品が ASIN に基づく 2 つのAmazon リストに一致します。

1. を切り替え **[!UICONTROL Remove Existing Seller SKU]** 必要に応じてオプションを選択します。

   - `Yes`  – 新しく提供された情報を使用して、リストを削除および作成することを選択します。

   - `No`  – 古いリストを変更せずに、リストを作成することを選択します。

1. クリック **[!UICONTROL Save Listing Update]**.

## 1 つのカタログ製品を 2 つのAmazon一覧と照合するために使用します

1. のリストを表示 _[!UICONTROL Product Listings]_ページ （_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Ineligible]_、または _[!UICONTROL Ended]_タブ）。

1. 次の下 _[!UICONTROL Actions]_を選択し、**[!UICONTROL Create Alias Seller SKU]**.

1. の場合 **[!UICONTROL Assign New Seller SKU]**&#x200B;一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用されません）。

1. の場合 **[!UICONTROL Assign New ASIN]**&#x200B;一意の英数字の値を入力します。

   この値は、カタログ製品に一致する製品 ASIN を自動入力します。 この値を変更すると、カタログ製品が ASIN に基づく 2 つのAmazon リストに一致します。

1. を切り替え **[!UICONTROL Remove Existing Seller SKU]** 必要に応じてオプションを選択します。

   - `Yes`  – 新しく提供された情報を使用して、リストを削除および作成することを選択します。

   - `No`  – 別のリストを作成し、古いリストは変更しないようにしてください。

1. クリック **[!UICONTROL Save Listing Update]**.

![alias Amazon販売者 SKU の作成](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | 元のAmazon販売者 SKU にリンクする、一意の新しい英数字の値を入力します。 この番号は、カタログ商品と照合するために、Amazonのセールスチャネルでのみ使用されます。 任意の SKU 値を使用できますが、値はカタログで 1 回だけ使用できます。 |
| [!UICONTROL Assign New ASIN] | カタログ製品と照合するリストの ASIN 値を入力します。 同じ製品の別のリストで 1 つのカタログ製品を ASIN に一致させる場合にのみ、このフィールドを変更します。 この値は、Amazonによって割り当てられた ASIN と一致する必要があります。一致しない場合、リストはAmazonによって拒否されません。 |
| [!UICONTROL Remove Existing Seller SKU] | オプション：<ul><li>**[!UICONTROL Yes]**  – 新しく提供された情報を使用して、リストを削除および作成することを選択します。 新しいリストがに表示されます。 _[!UICONTROL Active]_タブをクリックすると、古いリストがに移動します_&#x200B;終了&#x200B;_タブ。</li><li>**[!UICONTROL No]**  – 別のリストを作成し、古いリストは変更しないようにしてください。 新しいリストが作成されると、両方のリストが「アクティブ」タブに表示されます。</li></ul> |
