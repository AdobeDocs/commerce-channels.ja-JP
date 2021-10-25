---
title: Amazon Order Details
description: Adobe Commerce または Magento Open Source Admins には、Amazon Marketplace の注文に関する詳細情報が表示されます。
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Amazon order details

![Amazon order details](assets/amazon-order-details-header.png)

## Amazon order details の表示

1. **[!UICONTROL View Store]** Store カードをクリックします。

1. セクションで _[!UICONTROL Recent Orders]_、注文番号をクリックします。

   _[!UICONTROL Amazon Order Details]_ページが開きます。

>[!NOTE]
>
>注文の設定で注文が有効になって [ ](./order-settings.md) おり、 [ Amazon (FBA) によって注文が満たされている場合は ](./fulfilled-by.md) 、注文明細の一部のフィールドにダミーデータが表示されることがあります。 Amazon は、FBA オーダーで次のデータを送信することはできません。
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


### 「注文と出荷」タブ

この _[!UICONTROL Order and Shipping Details]_タブには、Amazon から受信した詳細なオーダー情報が表示されます。

>[!IMPORTANT]
>
>Amazon は、Amazon sales channel に取り込むことができない標準的でない住所情報を受け付けます。これによって、州/国コードが特定の注文について正しく更新されないようにすることができます。 アドレスエラーを修正するには、次のフィールドを注文詳細で編集可能にします。
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`

>
>「編集後に注文を保存」をクリックしても構いません **** 。

![注文と出荷に関する詳細情報](assets/amazon-order-details.png)

### 「注文項目」タブ

このタブには、 _[!UICONTROL Order Items]_amazon から受信した amazon の注文に関連付けられたすべてのアイテムが表示されます。

![受注品目の詳細](assets/amazon-order-item-details.png)

### 「トラッキング」タブ

タブには、 _[!UICONTROL Tracking]_Amazon の順序に関連付けられた追跡情報が表示されます。

![詳細の追跡](assets/amazon-order-tracking-details.png)
