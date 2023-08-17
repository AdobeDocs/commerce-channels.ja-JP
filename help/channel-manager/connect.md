---
title: '''接続先 [!DNL Commerce] サービス`'
description: 'チャネルマネージャの接続先 [!DNL Commerce] データの同期と、 [!DNL Commerce] インスタンス、チャネルマネージャー、およびその他のサポートサービス。'
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# 接続先 [!DNL Commerce] サービス

The [!DNL Commerce Services Connector] は、Channel Manager サービスをAdobe CommerceおよびMagento Open Sourceインスタンスと統合します。 コネクタは、データの同期と、 [!DNL Commerce] 例 [!DNL Channel Manager]、およびその他のサポートサービス。

[!DNL Commerce Services Connector] の使用に必要な 1 回限りのプロセス [Adobe Commerce SaaS サービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) 例： [!DNL Channel Manager], [!DNL Live Search]、および [!DNL Product Recommendations]. コネクタを別のサービス用に既に設定している場合は、この手順をスキップします。

## 要件

- **コマースアカウント** — にソフトウェアをインストールする [!DNL Commerce] インスタンスの場合は、 [!DNL Commerce] プラットフォーム。

  アカウント所有者とスーパーユーザーは、 [!DNL Commerce] インスタンスを使用するか、 [!DNL Commerce] CLI コマンド `admin:user:create`.

- **Adobe Commerce Production API キー**-This [key](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) チャネルマネージャーで必要なサービスへの API アクセスを有効にします。 このキーの公開および非公開の資格情報が必要です。

>[!TIP]
>
>資格情報を指定するには、 [!DNL Commerce] ライセンス所有者またはアカウント所有者は、次のオプションを持っています。 [アクセスを共有](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html)または、 [API キー](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) 信頼できる開発者に対する資格情報。

## を設定します。 [!DNL Commerce Services Connector]

1. ストアサービスの設定を開きます。

   - 管理者で、「 」を選択します。 **[!UICONTROL Stores]**.

   - の下 *[!UICONTROL Settings]*&#x200B;を選択します。 **[!UICONTROL Configuration]**.

   - 展開 **[!UICONTROL Services]** を選択し、 **[!UICONTROL Commerce Services Connector]**.

1. Adobe Commerceアカウントから実稼動 API キーの資格情報を追加します。

   ![[!DNL Commerce Services Connector] サービス [!DNL Admin] 表示](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > 次の場合、 [!DNL Commerce] インスタンスが他にあります [!DNL Adobe Commerce] 次のようなサービス [!DNL Live Search] または [!DNL Product Recommendations] インストール済みの場合は、資格情報情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce Services が Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータ領域を設定します。

   ![[!DNL Commerce Services Connector] での SaaS 識別子の設定 [!DNL Admin] 表示](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

