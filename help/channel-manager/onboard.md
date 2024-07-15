---
title: オンボード  [!DNL Channel Manager]
description: 「いくつかのオンボーディング手順を完了して、インスタンスを  [!DNL Channel Manager]  サービスに接続します。」
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Onboard [!DNL Channel Manager]

Channel Manager のオンボーディングプロセスが完了したら、Adobe Commerceから Walmart Marketplace のチャネルセールス業務にアクセス、設定、管理できます。 チャネルマネージャーは、[!UICONTROL Commerce Admin Marketing] メニューの「[!UICONTROL Channel Manager]」オプションから使用できます。

管理ビューの ![[!DNL Channel Manager] のオプション ](assets/channel-manager-admin-view.png){width="500"}

## 要件

チャネルマネージャーの使用要件を確認し、拡張機能のダウンロード、インストール、設定に必要なアカウント情報と資格情報を収集します。

- **[Walmart Marketplace の要件](walmart-requirements.md)** – チャネルマネージャーとの統合に関する要件（[ 販売者アカウントの設定 ](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) と、統合を有効にするための API キーの生成など）を満たしていることを確認します。

- **Commerce アカウント情報**-[!DNL Channel Manager] をダウンロードしてインストールするには、[Commerce アカウント ](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html) が必要です。 [!DNL Adobe Commerce] または [!DNL Magento Open Source] インスタンスに対する所有者または管理者のアクセス権を持つアカウント ID と資格情報が必要です。

   - **MAGE ID**-[[!DNL Commerce] アカウントにログイン ](https://account.magento.com/customer/account/login/) して、**[!UICONTROL My Account - Magento settings]** から ID を取得します。

     [!DNL Commerce] アカウント設定で ![[!DNL MAGEID] 定 ](assets/mageid-my-commerce-account.png){width="250"}

   - **アクセスキー –** 認証キーを取得して、[!DNL Commerce] Composer リポジトリーコン `([!DNL repo.magento.com]` ールから [!DNL Commerce] 拡張機能をダウンロードします）。

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     Adobe CommerceおよびMagento Open Sourceプロジェクトでは、のオーナーは、信頼できる従業員やサービスプロバイダーがオーナーまたはライセンスホルダーアカウントの資格情報を使用して拡張機能をダウンロードできるように、[ 共有アクセス ](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) を設定できます。

     クラウドインフラストラクチャプロジェクトの [!DNL Adobe Commerce] 合、ソフトウェアインストーラーは、[!DNL Commerce] インスタンスに対する次のアクセス権を持っている必要があります。

      - Cloud プロジェクトへのスーパーユーザーのアクセス
      - 特定の環境への管理者アクセス
      - composer リポジトリへのアクセス権を持つ [!DNL Adobe Commerce] アカウント

     [2}Cloud Infrastructure ガイドのCommerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) ユーザーアクセスの管理 *を参照してください。*

- これらのツールを使用して [!DNL Adobe Commerce] または [!DNL Magento Open Source] のプラットフォームで拡張機能をインストールおよび管理する方法については、**Composer の使用および *インストール ガイド* の[!DNL Commerce CLI]** 参照 [](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 拡張機能のインストール）を参照してください。

- **[[!DNL Amazon Sales Channel] バージョン 4.4.2 以降 ](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** - [!DNL Commerce] サイトに対して [!DNL Amazon Sales Channel] をアクティブ化した場合は、[!DNL Channel Manager] をインストールする前に、[!DNL Commerce] プラットフォームにバージョン 4.4.2 以降がインストールされていることを確認します。

- Adobe CommerceとMagento Open Sourceの **[!DNL Inventory Management]拡張機能**

  Channel Manager を在庫管理および注文管理に使用する場合は、Adobe CommerceおよびMagento Open SourceインスタンスにInventory management拡張機能をインストールして有効にする必要があります。 通常、この拡張機能はAdobe Commerceおよび [!DNL Magento Open Source] 2.3.x 以降にインストールされ、デフォルトで有効になっています。

  Commerceを 2.2.x からアップグレードした場合、またはInventory managementを無効にしている場合は、必要なモジュールが含まれるようにインストールを更新します。 [2}Inventory management ガイド ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)Inventory managementのインストール *を参照してください。*

### 必要システム構成

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x 以降 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel]  バージョン 4.4.2 以降 ](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) - [!DNL Commerce] サイトの [!DNL Amazon Sales Channel] をアクティベートした場合は、[!DNL Channel Manager] をインストールする前に、[!DNL Commerce] プラットフォームにバージョン 4.4.2 がインストールされていることを確認します。
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### サポートされるプラットフォーム

- クラウド上のAdobe Commerce（ECE） :2.4.x
- Adobe Commerce オンプレミス（EE） :2.4.x
- Magento Open Source 2.4.x

## オンボーディング手順

1. [Walmart Seller アカウントを設定します ](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp)。

1. [ 拡張機能をイ  [!DNL Channel Manager]  ストールします ](install.md)。

1. [Commerce サービスに接続 ](connect.md) して、Channel Manager をCommerce インスタンスおよびその他のサポートサービスと統合します。

1. [ ストア  [!DNL Commerce]  接続先  [!DNL Walmart Marketplace]](connect-marketplace.md)。

1. [ ストアの設定を完了 ](complete-sales-channel-store-setup.md) します。
