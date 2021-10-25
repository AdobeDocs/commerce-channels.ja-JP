---
title: エイリアスを作成する Amazon 売り手 SKU SKU
description: エイリアス Amazon 売り手 SKU を使用して、Commerce カタログ製品からマルチ地域の Amazon リストを作成することができます。
exl-id: df3cafbf-58df-4c93-9e63-20feb6f4e7ed
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# エイリアスを作成する Amazon 売り手 SKU SKU

[!DNL Alias Amazon Seller SKU]は、カタログ内の同じ製品から Amazon リストを作成するために使用され [!DNL Commerce] ます。Amazon 販売店が熟練した場合、 [ amazon のグローバル sku ](https://sellercentral.amazon.com/gp/help/external/help.html?itemID=201394090) {target = &quot;_blank&quot;} および Marketplace に関する sku については、在庫と出荷について理解している場合があります。 Amazon 販売チャンネルの同じ原則に従うと、Amazon 売り手 SKU は地域ごとに製品リスト情報を管理し、を使用して [!DNL Alias Amazon Seller SKU] 製品リスト情報を地域固有のレベルで制御することができます。

この関数は、次の2つの関数を実行するために使用できます。

- [!DNL Alias Amazon Seller SKU]カタログ製品のを作成して、 [!DNL Commerce] 地域固有のリスティング情報を制御します。

   **例** : あなたは、米国とカナダの両方で販売されています。 各 Amazon 販売チャンネルストアには、セットアップ中に1つの Amazon 地域しか割り当てられないことに注意してください。 そのため、en-us 販売チャンネルストアには、米国地域が定義され、カナダが定義されている別の店舗がある場合もあります。 どちらのストアも [!DNL Commerce] 、Amazon 売り手 SKU とアークサインの製品属性を含む両方の地域で情報を表示するために、カタログを共有しています。 そのため、カタログ製品のリストは、両方の店舗、価格の共有、株価、数量、その他の製品属性と同じになります。 ただし、カナダに保存した株は、カナダから出荷されています。 これにより、各ストアについてリストの数量を個別に制御する必要があります。 このような領域固有の制御を行うには、エイリアス Amazon 売り手 SKU を作成します。

   基本的には、同じカタログ製品にリンクされたエイリアス Amazon 売り手 SKU を作成し、その領域に同じ出展を再公開するために使用することができます。

- [!DNL Alias Amazon Seller SKU]カタログ製品を作成し、 [!DNL Commerce] 2 つの Amazon リストに適合させます。

   **例** : Amazon リスティングと一致するカタログ製品がある場合。 Amazon によって、同じ製品を表す複数の一覧が表示されていることがよくあるので、同じ製品について別の Amazon リストが見つかった場合でも、Amazon によって一覧の内容が異なります。 製品の可視性を高めるには、カタログ製品が別のアークサインに一致するようにして、アーク、両方の値について一覧を作成する必要があります。 これを実行するには、エイリアス Amazon 売り手 SKU の SKU を作成することができます。

   これを使用して、 [!DNL Alias Amazon Seller SKU] 1 つのカタログ製品を別の Amazon リスティングに一致させることができます。また、新しく一致したテキストのリストを作成することもできます。 このシナリオでは、同じカタログ製品について2つの Amazon リストがあると考えられます。

   エイリアス Amazon 売り手 SKU を作成した後は、リスティング設定、ルール、上書きを使用して、地域のリスト情報を制御することができます。 リストに対して地域別に定義できる製品属性には、数量/在庫、フルフィルメント方法、条件、製品の適格性、処理時間が含まれます。

## 領域固有の目的に使用されます。 {#region-specific}

ページに一覧表示されている _[!UICONTROL Product Listings]__[!UICONTROL Inactive]_ 場合は、「 _有効」、「有効」_ __ または「 _終了」_ タブが表示されます。

1. _[!UICONTROL Actions]_でをクリックし&#x200B;**[!UICONTROL Create Alias Seller SKU]**ます。

1. **[!UICONTROL Assign New Seller SKU]**「」には、一意の英数字の値を入力します。

   この値は一意である必要があります。これは、カタログ内の他の製品またはエイリアスには使用されません。

1. に **[!UICONTROL Assign New ASIN]** 変更を加えます。

   この値には、カタログ製品と一致する製品のアークサインが自動的に入力されます。 この値を変更すると、お客様のカタログ製品が、アークサインに基づいて2つの Amazon リストと一致するようになります。

1. **[!UICONTROL Remove Existing Seller SKU]**&#x200B;必要に応じてオプションを切り替えます。

   - `Yes` このオプションを選択すると、リストが削除され、指定した新しい情報を使用してリストが作成されます。

   - `No` -一覧を作成し、古い一覧は変更しないままにしておくことができます。

1. をクリックし **[!UICONTROL Save Listing Update]** ます。

## 単一カタログ製品を2つの Amazon リストに一致させるために使用されます。

1. _[!UICONTROL Product Listings]_ページ (、、、_[!UICONTROL Inactive]_ _[!UICONTROL Active]__[!UICONTROL Ineligible]_ またはタブ) のリストを表示し _[!UICONTROL Ended]_ます。

1. _[!UICONTROL Actions]_でをクリックし&#x200B;**[!UICONTROL Create Alias Seller SKU]**ます。

1. **[!UICONTROL Assign New Seller SKU]**「」には、一意の英数字の値を入力します。

   この値は一意である必要があります。これは、カタログ内の他の製品またはエイリアスには使用されません。

1. **[!UICONTROL Assign New ASIN]**「」には、一意の英数字の値を入力します。

   この値には、カタログ製品と一致する製品のアークサインが自動的に入力されます。 この値を変更すると、お客様のカタログ製品が、アークサインに基づいて2つの Amazon リストと一致するようになります。

1. **[!UICONTROL Remove Existing Seller SKU]**&#x200B;必要に応じてオプションを切り替えます。

   - `Yes` このオプションを選択すると、リストが削除され、指定した新しい情報を使用してリストが作成されます。

   - `No` -別の一覧を作成することを選択し、古い一覧は変更されません。

1. をクリックし **[!UICONTROL Save Listing Update]** ます。

![エイリアスを作成する Amazon 売り手 SKU SKU](assets/amazon-alias-sku-create.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Assign New Seller SKU] | 元の Amazon 売り手 SKU にリンクする新しい一意の英数字の値を入力します。 この数値は、カタログ製品に一致させるために Amazon 販売チャンネルによってのみ使用されます。 任意の SKU 値を使用できますが、この値は一度に1つのカタログでしか使用できません。 |
| [!UICONTROL Assign New ASIN] | カタログ製品と一致させるリストの「アーク」の値を入力します。 このフィールドは、同じ製品の別のリストのために単一のカタログ製品をアークにする場合にのみ修正してください。 この値は、Amazon によって割り当てられたアークまたはリストが Amazon によって拒否されることはありません。 |
| [!UICONTROL Remove Existing Seller SKU] | オプション：<ul><li>**[!UICONTROL Yes]** このオプションを選択すると、リストが削除され、指定した新しい情報を使用してリストが作成されます。 タブに新しいリストが表示され、 _[!UICONTROL Active]_古いリストが「_ 終了」タブに移動し _ます。</li><li>**[!UICONTROL No]** -別の一覧を作成することを選択し、古い一覧は変更されません。 リストが作成された後に、アクティブなタブに両方のリストが表示されます。</li></ul> |
