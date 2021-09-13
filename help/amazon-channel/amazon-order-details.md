---
title: Amazon注文の詳細
description: Amazon Marketplaceの注文の詳細をAdobeコマースまたはMagento Open Source管理で表示します。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazonの注文の詳細

![Amazonの注文の詳細](assets/amazon-order-details-header.png)

## Amazon注文の詳細の表示

1. ストアカードの&#x200B;**[!UICONTROL View Store]**&#x200B;をクリックします。

1. _[!UICONTROL Recent Orders]_セクションで、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが開きます。

>[!NOTE]
>
>[注文の設定](./order-settings.md)で注文のインポートが有効になっていて、注文がAmazon(FBA)](./fulfilled-by.md)で処理されている場合、注文の詳細に一部のフィールドのダミーデータが表示されることがあります。 [Amazonは、FBA注文に対して次のデータを送信しません。
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
>Amazonは、Amazonの販売チャネルにインポートできない非標準の住所情報を受け入れるので、一部の注文に対して州/国コードが正しく更新されません。 アドレスエラーを修正するには、次のフィールドを注文の詳細で編集できます。
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>編集後、「**並べ替えを保存**」をクリックすることを忘れないでください。

![注文と発送の詳細](assets/amazon-order-details.png)

### 「項目を並べ替え」タブ

「 _[!UICONTROL Order Items]_」タブには、Amazonから受信した、Amazonの注文に関連するすべての項目が表示されます。

![注文品目の詳細](assets/amazon-order-item-details.png)

### 「トラッキング」タブ

「_[!UICONTROL Tracking]_」タブには、Amazonの注文に関連付けられた追跡情報が表示されます。

![トラッキングの詳細](assets/amazon-order-tracking-details.png)
