---
title: '接続先 [!DNL Commerce] サービス'
description: 'チャネルマネージャーの接続先 [!DNL Commerce] 間のデータ同期と通信を可能にするサービス [!DNL Commerce] インスタンス、チャネルマネージャーおよびその他のサポートサービス。'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# の接続 [!DNL Commerce] サービス

この [!DNL Commerce Services Connector] channel Manager サービスをAdobe CommerceおよびMagento Open Sourceインスタンスと統合します。 コネクタにより、AEM と AEM 間のデータ同期と通信が可能になります。 [!DNL Commerce] インスタンス， [!DNL Channel Manager]、およびその他のサポートサービス。

[!DNL Commerce Services Connector] セットアップは、を使用するために必要な 1 回限りのプロセスです [Adobe Commerce SaaS サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) 例： [!DNL Channel Manager], [!DNL Live Search]、および [!DNL Product Recommendations]. 別のサービス用にコネクタを既に設定している場合は、この手順をスキップします。

## 要件

- **Commerce アカウント** – にソフトウェアをインストールする [!DNL Commerce] インスタンスにアクセスするには、所有者または管理者アクセス権を持つアカウントが必要です [!DNL Commerce] プラットフォーム。

  アカウント所有者とスーパーユーザーは、から管理者アカウントを作成できます。 [!DNL Commerce] を使用して、またはコマンドラインから [!DNL Commerce] CLI コマンド `admin:user:create`.

- **Adobe Commerce実稼動 API キー** – この [キー](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) チャネルマネージャーで必要なサービスへの API アクセスを有効にします。 このキーには、公開鍵と秘密鍵の秘密鍵証明書が必要です。

>[!TIP]
>
>資格情報を指定するには、次の手順に従います。 [!DNL Commerce] ライセンス所有者またはアカウント所有者には、次の操作を行うオプションがあります [アクセスを共有](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html)、または [API キー](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) 信頼できる開発者に対する資格情報。

## の設定 [!DNL Commerce Services Connector]

1. ストアサービス設定を開きます。

   - 管理者から、を選択します。 **[!UICONTROL Stores]**.

   - 次の下 *[!UICONTROL Settings]*&#x200B;を選択 **[!UICONTROL Configuration]**.

   - を展開 **[!UICONTROL Services]** を選択して、 **[!UICONTROL Commerce Services Connector]**.

1. 実稼動 API キーの資格情報をAdobe Commerce アカウントから追加します。

   ![[!DNL Commerce Services Connector] 内のサービス [!DNL Admin] 表示](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > 次の場合 [!DNL Commerce] インスタンスにその他あり [!DNL Adobe Commerce] などのサービス [!DNL Live Search] または [!DNL Product Recommendations] インストールされると、秘密鍵証明書の情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce サービスが Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータスペースを設定します。

   ![[!DNL Commerce Services Connector] での SaaS 識別子設定 [!DNL Admin] 表示](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

