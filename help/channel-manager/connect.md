---
title: 接続先 [!DNL Commerce] サービス
description: チャネルマネージャの接続先 [!DNL Commerce] データの同期と、 [!DNL Commerce] インスタンス、チャネルマネージャー、およびその他のサポートサービス。
role: User
level: Intermediate
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: aaab7aa7feb05264c24386e62193564dc5ae8fe3
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# 接続先 [!DNL Commerce] サービス

Commerce Services コネクタは、チャネルマネージャーサービスをAdobe CommerceおよびMagento Open Sourceインスタンスと統合します。 コネクタは、 [!DNL Commerce] 例 [!DNL Channel Manager]、およびその他のサポートサービス。

Commerce Services コネクタの設定は、Adobeの使用に必要な 1 回限りのプロセスです [Commerce SaaS サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} いいね！ [!DNL Channel Manager], [!DNL Live Search]、および [!DNL Product Recommendations]. コネクタを別のサービス用に既に設定している場合は、この手順をスキップします。

## 要件

- **コマースアカウント** — コマースインスタンスにソフトウェアをインストールするには、コマースプラットフォームへの所有者または管理者アクセス権を持つアカウントが必要です。

   アカウントの所有者とスーパーユーザーは、コマースインスタンスから、または、 [!DNL Commerce] CLI コマンド `admin:user:create`.

- **Adobe Commerce Production API キー**-This [key](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} は、チャネルマネージャーで必要なサービスへの API アクセスを有効にします。 このキーの公開および非公開の資格情報が必要です。

>[!TIP]
>
>資格情報を提供するために、コマースのライセンス所有者またはアカウント所有者には、次のオプションがあります。 [アクセスを共有](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} または [API キー](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} 個の信頼できる開発者に対する資格情報。

## Commerce Services コネクタの設定

1. ストアサービスの設定を開きます。

   - 管理者から、 **[!UICONTROL Stores]**.

   - の下 *[!UICONTROL Settings]*&#x200B;を選択します。 **[!UICONTROL Configuration]**.

   - 展開 **[!UICONTROL Services]** を選択し、 **[!UICONTROL Commerce Services Connector]**.

1. Adobe Commerceアカウントから実稼動 API のキー資格情報を追加します。

   ![[!DNL Commerce Service Connector] サービス [!DNL Admin] 表示](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > 次に、 [!DNL Commerce] インスタンスが他の [!DNL Adobe Commerce] 次のようなサービス [!DNL Live Search] または [!DNL Product Recommendations] インストール済みの場合は、資格情報情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce Services が Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータ領域を設定します。

   ![[!DNL Commerce Service Connector] での SaaS 識別子の設定 [!DNL Admin] 表示](assets/commerce-services-connector-saas-config.png)

