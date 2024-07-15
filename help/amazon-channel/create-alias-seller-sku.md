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

ア [!DNL Alias Amazon Seller SKU] ットを使用して、[!DNL Commerce] カタログに含まれる同じ商品のAmazon リストを作成します。 経験豊富なAmazonのセラーであれば、[Amazonのグローバル SKU と ](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090){target="_blank"} 在庫および配送用のマーケットプレイス固有の SKU をご存知かもしれません。 Amazonの販売チャネルと同様の原則に従って、Amazonの販売者 SKU は、複数地域のレベルで商品リスト情報を制御し、[!DNL Alias Amazon Seller SKU] を使用して、地域固有のレベルで商品リスト情報を制御できます。

この関数は、次の 2 つの関数を実行するために使用できます。

- [!DNL Commerce] カタログ製品の 1 つに [!DNL Alias Amazon Seller SKU] を作成して、地域固有のリスト情報を制御します。

  **例**：米国とカナダの両方の地域で販売者となっている。 セットアップ時に、Amazonの各セールスチャネルストアに割り当てることができるAmazonリージョンは 1 つだけであることに注意してください。 つまり、米国リージョンが定義されたAmazonのセールスチャネルストアと、カナダ リージョンが定義された別のストアがあるということです。 どちらの店舗も、Amazonの販売者 SKU や ASIN 製品属性を含む両方の地域のリスト情報について、[!DNL Commerce] ールカタログを共有しています。 したがって、カタログ製品のリストは、価格、在庫/数量、その他の製品属性を共有して、両方の店舗で同じになります。 ただし、カナダの店舗の在庫はカナダの場所から、米国の店舗の在庫は米国の場所から出荷されます。 したがって、リストのリスト数量は、ストアごとに個別に制御する必要があります。 このタイプの地域固有のコントロールを実現するには、Alias Amazon販売者 SKU を作成します。

  基本的に、同じカタログ商品にリンクされ、そのリージョンで同じリストを再公開するために使用できる Alias Amazonの販売者 SKU を作成できます。

- [!DNL Alias Amazon Seller SKU] を作成し、[!DNL Commerce] のカタログ商品の 1 つを 2 つのAmazon リストに一致させます。

  **例**:Amazon リストと一致するカタログ商品があるとします。 Amazonには、同じ商品を表す複数のリストが頻繁に存在するので、同じ商品に対して別のAmazonのリストを発見しましたが、Amazonは別の ASIN をリストに割り当てました。 製品の表示域を含めるようにするには、カタログ製品を別の ASIN と一致させ、両方の ASIN 値の一覧を作成します。 これを実現するには、Alias Amazon販売者 SKU を作成します。

  基本的に、1 つのカタログ商品を 2 つ目のAmazon リストと照合して、新しく照合された ASIN のリストを作成するために使用できる [!DNL Alias Amazon Seller SKU] ールを作成できます。 このシナリオでは、同じカタログ商品に対して 2 つのAmazonのリストが作成されます。

  Alias Amazon Seller SKU を作成したら、リスト設定、ルール、上書きを使用して、リージョンのリスト情報を制御できます。 リストの地域ごとに定義できる製品属性には、数量/在庫、履行方法、条件、製品の適格性、処理時間などがあります。

## 地域固有の目的に使用されます {#region-specific}

_[!UICONTROL Product Listings]_ページでリストを表示します（_[!UICONTROL Inactive]_、_アクティブ_、_不適格_ または _終了_ タブ）。

1. [_[!UICONTROL Actions]_] で、[**[!UICONTROL Create Alias Seller SKU]**] をクリックします。

1. **[!UICONTROL Assign New Seller SKU]** の場合は、一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用されません）。

1. **[!UICONTROL Assign New ASIN]** の場合は、変更を加えません。

   この値は、カタログ製品に一致する製品 ASIN を自動入力します。 この値を変更すると、カタログ製品が ASIN に基づく 2 つのAmazon リストに一致します。

1. 必要に応じて「**[!UICONTROL Remove Existing Seller SKU]**」オプションを切り替えます。

   - `Yes` – 新しく提供された情報を使用して、リストを削除および作成することを選択します。

   - `No` - リストの作成を選択し、古いリストを変更しません。

1. 「**[!UICONTROL Save Listing Update]**」をクリックします。

## 1 つのカタログ製品を 2 つのAmazon一覧と照合するために使用します

1. リストを _[!UICONTROL Product Listings]_ページ（_[!UICONTROL Inactive]_、_[!UICONTROL Active]_、_[!UICONTROL Ineligible]_、_[!UICONTROL Ended]_の各タブ）で表示します。

1. [_[!UICONTROL Actions]_] で、[**[!UICONTROL Create Alias Seller SKU]**] をクリックします。

1. **[!UICONTROL Assign New Seller SKU]** の場合は、一意の英数字の値を入力します。

   この値は一意である必要があります（カタログ内の他の製品やエイリアスには使用されません）。

1. **[!UICONTROL Assign New ASIN]** の場合は、一意の英数字の値を入力します。

   この値は、カタログ製品に一致する製品 ASIN を自動入力します。 この値を変更すると、カタログ製品が ASIN に基づく 2 つのAmazon リストに一致します。

1. 必要に応じて「**[!UICONTROL Remove Existing Seller SKU]**」オプションを切り替えます。

   - `Yes` – 新しく提供された情報を使用して、リストを削除および作成することを選択します。

   - `No` – 別のリストを作成し、古いリストを変更しないようにします。

1. 「**[!UICONTROL Save Listing Update]**」をクリックします。

![Alias Amazon販売者 SKU の作成 ](assets/amazon-alias-sku-create.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Assign New Seller SKU] | 元のAmazon販売者 SKU にリンクする、一意の新しい英数字の値を入力します。 この番号は、カタログ商品と照合するために、Amazonのセールスチャネルでのみ使用されます。 任意の SKU 値を使用できますが、値はカタログで 1 回だけ使用できます。 |
| [!UICONTROL Assign New ASIN] | カタログ製品と照合するリストの ASIN 値を入力します。 同じ製品の別のリストで 1 つのカタログ製品を ASIN に一致させる場合にのみ、このフィールドを変更します。 この値は、Amazonによって割り当てられた ASIN と一致する必要があります。一致しない場合、リストはAmazonによって拒否されません。 |
| [!UICONTROL Remove Existing Seller SKU] | オプション：<ul><li>**[!UICONTROL Yes]** – 新しく提供された情報を使用して、リストを削除および作成することを選択します。 新しいリストが「_[!UICONTROL Active]_」タブに表示され、古いリストが「_ 終了 _」タブに移動します。</li><li>**[!UICONTROL No]** – 別のリストを作成し、古いリストを変更しないようにします。 新しいリストが作成されると、両方のリストが「アクティブ」タブに表示されます。</li></ul> |
