---
title: Amazon注文の詳細
description: Adobe CommerceまたはMagento Open Source管理者で、Amazon Marketplace 注文の詳細を表示できます。
feature: Sales Channels, Orders
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon注文の詳細

![Amazon注文の詳細](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## Amazonの注文の詳細を表示

1. クリック **[!UICONTROL View Store]** ストアカードに。

1. が含まれる _[!UICONTROL Recent Orders]_セクションで、注文番号をクリックします。

   この _[!UICONTROL Amazon Order Details]_ページが開きます。

>[!NOTE]
>
>で注文の読み込みを有効にしている場合 [オーダー設定](./order-settings.md) そして順序は [Amazon（FBA）によって履行](./fulfilled-by.md)の場合、注文の詳細のいくつかのフィールドにダミーデータが表示されることがあります。 Amazonは、FBA 注文に関して次のデータを送信しません。
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`

### 「受注および出荷詳細」タブ

この _[!UICONTROL Order and Shipping Details]_tab キーを押すと、Amazonから受信した詳細な注文情報が表示されます。

>[!IMPORTANT]
>
>Amazonは、Amazon sales channel にインポートできない非標準の住所情報を受け入れます。そのため、一部の注文で都道府県/国コードが正しく更新されません。 住所エラーを修正するために、次のフィールドを注文の詳細で編集できます。
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>クリックすることを忘れないでください **注文を保存** 編集を行った後。

![注文と配送の詳細](assets/amazon-order-details.png){width="600" zoomable="yes"}

### 「注文項目」タブ

この _[!UICONTROL Order Items]_tab キーを押すと、Amazonから受け取った、Amazonの注文に関連付けられているすべての項目が表示されます。

![注文項目の詳細](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### 「トラッキング」タブ

この _[!UICONTROL Tracking]_タブには、Amazonの注文に関連付けられたトラッキング情報が表示されます。

![トラッキングの詳細](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
