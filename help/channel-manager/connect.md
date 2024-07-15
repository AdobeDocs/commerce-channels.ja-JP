---
title: 'サービスへ  [!DNL Commerce]  接続'
description: 「チャネルマネージャーを  [!DNL Commerce] services に接続して、 [!DNL Commerce]  インスタンス、チャネルマネージャー、その他のサポートサービス間のデータ同期と通信を有効にします」
role: Admin, Developer
level: Intermediate
feature: Sales Channels, Install, Integration
exl-id: 97da2142-ecef-44dc-91d8-5dc55c713d31
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# [!DNL Commerce] Services への接続

[!DNL Commerce Services Connector] は、Channel Manager サービスとAdobe CommerceおよびMagento Open Sourceインスタンスを統合します。 コネクタにより、[!DNL Commerce] インスタンス、[!DNL Channel Manager]、およびその他のサポートサービス間のデータ同期と通信が可能になります。

[!DNL Commerce Services Connector] の設定は、[Adobe Commerce SaaS サービス（[!DNL Channel Manager]、[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html)[!DNL Product Recommendations] など）を使用するために必要な 1 回限りのプロセスです。 別のサービス用にコネクタを既に設定している場合は、この手順をスキップします。

## 要件

- **Commerce アカウント** - [!DNL Commerce] インスタンスにソフトウェアをインストールするには、[!DNL Commerce] プラットフォームへの所有者または管理者アクセス権を持つアカウントが必要です。

  アカウント所有者とスーパーユーザーは、[!DNL Commerce] インスタンスまたはコマンドラインから [!DNL Commerce] CLI コマンド `admin:user:create` ードを使用して管理者アカウントを作成できます。

- **Adobe Commerce実稼動 API キー** – この [ キー ](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#genapikey) を使用すると、Channel Manager で必要なサービスに API でアクセスできます。 このキーには、公開鍵と秘密鍵の秘密鍵証明書が必要です。

>[!TIP]
>
>資格情報を指定するには、[!DNL Commerce] のライセンス所有者またはアカウント所有者が [ アクセスを共有 ](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) するか、[API キー ](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html) 資格情報を信頼できる開発者に付与するオプションを持っています。

## [!DNL Commerce Services Connector] の設定

1. ストアサービス設定を開きます。

   - 管理者から、「**[!UICONTROL Stores]**」を選択します。

   - 「*[!UICONTROL Settings]*」で、「**[!UICONTROL Configuration]**」を選択します。

   - 「**[!UICONTROL Services]**」を展開し、「**[!UICONTROL Commerce Services Connector]**」を選択します。

1. 実稼動 API キーの資格情報をAdobe Commerce アカウントから追加します。

   [!DNL Admin]![[!DNL Commerce Services Connector] 表示でのサービス ](assets/commerce-services-connector-admin-service-view.png){width="600" zoomable="yes"}


   >[!NOTE]
   >
   > [!DNL Commerce] インスタンスに [!DNL Live Search] や [!DNL Product Recommendations] などの他の [!DNL Adobe Commerce] サービスがインストールされている場合は、資格情報がインターフェイスに表示され、それ以上の設定は必要ありません。

1. Commerce サービスが Channel Manager サービスにデータを送信できるように、SaaS プロジェクトとデータスペースを設定します。

   [!DNL Admin] ビュー ![[!DNL Commerce Services Connector]SaaS 識別子設定 ](assets/commerce-services-connector-saas-config.png){width="600" zoomable="yes"}

