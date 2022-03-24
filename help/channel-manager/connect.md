---
title: Commerce Services に接続
description: Channel Manager インスタンスの接続先 [!DNL Commerce services] コマースインスタンス、チャネルマネージャー、およびその他のサポートサービス間でのデータ同期と通信を有効にする。
role: User
level: Intermediate
source-git-commit: ec950579a9b2220f9ec106b616779fc3503f3add
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Commerce Services に接続

Commerce Services コネクタは、チャネルマネージャーサービスをAdobe CommerceおよびMagento Open Sourceインスタンスと統合します。 コネクタは、 [!DNL Commerce] 例 [!DNL Channel Manager]、およびその他のサポートサービス。

Commerce Services コネクタの設定は、Adobeの使用に必要な 1 回限りのプロセスです [Commerce SaaS サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html){target=&quot;_blank&quot;} いいね！ [!DNL Channel Manager], [!DNL Live Search]、および [!DNL Product Recommendations]. コネクタを別のサービス用に既に設定している場合は、この手順をスキップできます。

## 前提条件

- **次を持つコマースアカウント [管理アクセス](https://docs.magento.com/user-guide/stores/admin.html){target=&quot;_blank&quot;}** をコマースインスタンスに設定します** — アカウントの所有者と管理者ユーザーは、コマースインスタンスから、またはコマンドラインから、 [!DNL Commerce] CLI コマンド `admin:user:create`.

- **Adobe Commerce [実稼動 API キー](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;}** — チャネルマネージャーで必要なサービスへの API アクセスを有効にする

   資格情報を提供するために、コマースのライセンス所有者またはアカウント所有者には、次のオプションがあります。
   [アクセスを共有](https://docs.magento.com/user-guide/magento/magento-account-share.html){target=&quot;_blank&quot;} または [API キー](https://docs.magento.com/user-guide/system/saas.html#apikey){target=&quot;_blank&quot;} 個の信頼できる開発者に対する資格情報。

## Commerce Services コネクタの設定

1. ストアサービスの設定を開きます。

   - 管理者から、 [!UICONTROL Stores].

   - の下 *設定*&#x200B;を選択します。 [!UICONTROL Configuration].

   - の [!UICONTROL Configuration] ページ、展開 [!UICONTROL Services] を選択し、 [!UICONTROL Commerce Services Connector].

1. Adobe Commerceアカウントから実稼動 API キーを追加します。

   ![[!DNL Commerce Service Connector] サービス [!DNL Admin] 表示](assets/commerce-services-connector-admin-service-view.png)


   >[!NOTE]
   >
   > 次に、 [!DNL Commerce] インスタンスが他の [!DNL Adobe Commerce] 次のようなサービス [!DNL Live Search] または [!DNL Product Recommendations] インストール済みの場合は、資格情報情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce Services が Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータ領域を設定します。

   ![[!DNL Commerce Service Connector] での SaaS 識別子の設定 [!DNL Admin] 表示](assets/commerce-services-connector-saas-config.png)

