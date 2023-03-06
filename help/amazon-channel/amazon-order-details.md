---
title: Amazon注文の詳細
description: Adobe CommerceまたはMagento Open Source管理で、Amazon Marketplace の注文に関する詳細を表示します。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon注文の詳細

![Amazonの注文の詳細](assets/amazon-order-details-header.png)

## Amazon注文の詳細を表示

1. クリック **[!UICONTROL View Store]** をストアカードに貼り付けます。

1. 内 _[!UICONTROL Recent Orders]_「 」セクションで、注文番号をクリックします。

   この _[!UICONTROL Amazon Order Details]_ページが開きます。

>[!NOTE]
>
>の [注文の設定](./order-settings.md) そして順序は [Amazon(FBA) で実現](./fulfilled-by.md)の場合、注文の詳細に一部のフィールドのダミーデータが表示されることがあります。 Amazonは、FBA 注文に関して次のデータを送信しません。
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


### 「注文と発送の詳細」タブ

この _[!UICONTROL Order and Shipping Details]_「 」タブには、Amazonから受け取った詳細な注文情報が表示されます。

>[!IMPORTANT]
>
>Amazonは、Amazonセールスチャネルに読み込めない非標準の住所情報を受け取るので、一部の注文で州/国コードが正しく更新されません。 アドレスエラーを修正するには、次のフィールドを注文の詳細で編集できます。
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>忘れずに **注文を保存** 編集後

![注文と発送の詳細](assets/amazon-order-details.png)

### 「注文項目」タブ

この _[!UICONTROL Order Items]_「 」タブには、Amazonから受け取った、Amazonの注文に関連するすべての項目が表示されます。

![注文項目の詳細](assets/amazon-order-item-details.png)

### 「トラッキング」タブ

この _[!UICONTROL Tracking]_「 」タブには、Amazonの注文に関連付けられた追跡情報が表示されます。

![トラッキングの詳細](assets/amazon-order-tracking-details.png)
