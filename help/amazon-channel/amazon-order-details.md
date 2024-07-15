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

![Amazon注文の詳細 ](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## Amazonの注文の詳細を表示

1. ストアカードの **[!UICONTROL View Store]** をクリックします。

1. [_[!UICONTROL Recent Orders]_] セクションで、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが開きます。

>[!NOTE]
>
>[ 注文設定 ](./order-settings.md) で注文のインポートを有効にしており、その注文が [Amazon（FBA）によって履行 ](./fulfilled-by.md) されている場合、注文の詳細の一部のフィールドにダミーデータが表示されることがあります。 Amazonは、FBA 注文に関して次のデータを送信しません。
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

「_[!UICONTROL Order and Shipping Details]_」タブには、Amazonから受け取った詳細な注文情報が表示されます。

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
>編集を行った後は、必ず **注文を保存** をクリックしてください。

![ 注文および発送明細 ](assets/amazon-order-details.png){width="600" zoomable="yes"}

### 「注文項目」タブ

「_[!UICONTROL Order Items]_」タブには、Amazonから受け取った、Amazonの注文に関連付けられたすべての項目が表示されます。

![ 注文品目詳細 ](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### 「トラッキング」タブ

「_[!UICONTROL Tracking]_」タブには、Amazonの注文に関連付けられたトラッキング情報が表示されます。

![ トラッキングの詳細 ](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
