---
title: '''接続先 [!DNL Commerce] サービス'
description: '''チャネルマネージャの接続先 [!DNL Commerce] データの同期と、 [!DNL Commerce] インスタンス、チャネルマネージャー、およびその他のサポートサービス。'''
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 7e7a3e854bbc6062e2d15c1962ddf787451e7275
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# 接続先 [!DNL Commerce] サービス

この [!DNL Commerce Services Connector] は、Channel Manager サービスをAdobe CommerceおよびMagento Open Sourceインスタンスと統合します。 コネクタは、 [!DNL Commerce] 例 [!DNL Channel Manager]、およびその他のサポートサービス。

[!DNL Commerce Services Connector] 設定は、 [Adobe Commerce SaaS サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} 例： [!DNL Channel Manager], [!DNL Live Search]、および [!DNL Product Recommendations]. コネクタを別のサービス用に既に設定している場合は、この手順をスキップします。

## 要件

- **コマースアカウント** — にソフトウェアをインストールする [!DNL Commerce] インスタンスの場合は、 [!DNL Commerce] プラットフォーム。

   アカウント所有者とスーパーユーザーは、 [!DNL Commerce] インスタンスを使用するか、 [!DNL Commerce] CLI コマンド `admin:user:create`.

- **Adobe Commerce Production API キー**-This [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} は、チャネルマネージャーで必要なサービスへの API アクセスを有効にします。 このキーの公開および非公開の資格情報が必要です。

>[!TIP]
>
>資格情報を指定するには、 [!DNL Commerce] ライセンス所有者またはアカウント所有者は、次のオプションを持っています。 [アクセスを共有](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} または [API キー](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} 個の信頼できる開発者に対する資格情報。

## の設定 [!DNL Commerce Services Connector]

1. ストアサービスの設定を開きます。

   - 管理者から、 **[!UICONTROL Stores]**.

   - の下 *[!UICONTROL Settings]*&#x200B;を選択します。 **[!UICONTROL Configuration]**.

   - 展開 **[!UICONTROL Services]** を選択し、 **[!UICONTROL Commerce Services Connector]**.

1. Adobe Commerceアカウントから実稼動 API のキー資格情報を追加します。

   ![[!DNL Commerce Services Connector] サービス [!DNL Admin] 表示](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > 次に、 [!DNL Commerce] インスタンスが他の [!DNL Adobe Commerce] 次のようなサービス [!DNL Live Search] または [!DNL Product Recommendations] インストール済みの場合は、資格情報情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce Services が Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータ領域を設定します。

   ![[!DNL Commerce Services Connector] での SaaS 識別子の設定 [!DNL Admin] 表示](assets/commerce-services-connector-saas-config.png)

