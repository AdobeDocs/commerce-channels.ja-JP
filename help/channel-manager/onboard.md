---
title: Onboard [!DNL Channel Manager]
description: '''インスタンスをに接続します [!DNL Channel Manager] いくつかのオンボーディング手順を完了するサービス。」'
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

Channel Manager のオンボーディングプロセスが完了したら、Adobe Commerceから Walmart Marketplace のチャネルセールス業務にアクセス、設定、管理できます。 チャネルマネージャーは [!UICONTROL Channel Manager] のオプション [!UICONTROL Commerce Admin Marketing] メニュー。

![[!DNL Channel Manager] 管理ビューのオプション](assets/channel-manager-admin-view.png){width="500"}

## 要件

チャネルマネージャーの使用要件を確認し、拡張機能のダウンロード、インストール、設定に必要なアカウント情報と資格情報を収集します。

- **[Walmart Marketplace の要件](walmart-requirements.md)** – 次のようなチャネル・マネージャとの統合要件を満たしていることを確認します [販売者アカウントの設定](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) API キーを生成して統合を有効にします。

- **Commerce アカウント情報** – ダウンロードとインストール [!DNL Channel Manager] が必要 [Commerce アカウント](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). への所有者または管理者アクセス権を持つアカウント ID と資格情報が必要です [!DNL Adobe Commerce] または [!DNL Magento Open Source] インスタンス。

   - **画像 ID**-[ログイン](https://account.magento.com/customer/account/login/) に [!DNL Commerce] id を取得するアカウント **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] 日付： [!DNL Commerce] アカウント設定](assets/mageid-my-commerce-account.png){width="250"}

   - **アクセスキー –** ダウンロードする認証キーの取得 [!DNL Commerce] からの拡張機能 [!DNL Commerce] Composer リポジトリ `([!DNL repo.magento.com]`）に設定します。

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     Adobe CommerceおよびMagento Open Sourceプロジェクトでは、所有者は以下を設定できます [共有アクセス](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) 信頼できる従業員およびサービスプロバイダーが、所有者またはライセンス所有者アカウントからの資格情報を使用して拡張機能をダウンロードできるようにする。

     の場合 [!DNL Adobe Commerce] クラウドインフラストラクチャプロジェクトでは、ソフトウェアインストーラーは次の権限が必要です。 [!DNL Commerce] インスタンス：

      - Cloud プロジェクトへのスーパーユーザーのアクセス
      - 特定の環境への管理者アクセス
      - an [!DNL Adobe Commerce] composer リポジトリへのアクセス権限を持つアカウント

     参照： [ユーザーアクセスの管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) が含まれる *クラウドインフラストラクチャー上のCommerce ガイド*.

- **Composer と[!DNL Commerce CLI]** – 参照 [拡張機能のインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) が含まれる *インストールガイド* これらのツールを使用してに拡張機能をインストールおよび管理する方法について [!DNL Adobe Commerce] または [!DNL Magento Open Source] プラットフォーム。

- **[[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** – をアクティブにした場合 [!DNL Amazon Sales Channel] の場合 [!DNL Commerce] sites、を確認する [!DNL Commerce] platform には、インストール前にバージョン 4.4.2 以降がインストールされています [!DNL Channel Manager].

- **[!DNL Inventory Management]Adobe CommerceとMagento Open Sourceの拡張機能**

  Channel Manager を在庫管理および注文管理に使用する場合は、Adobe CommerceおよびMagento Open SourceインスタンスにInventory management拡張機能をインストールして有効にする必要があります。 通常、この拡張機能はAdobe Commerceにデフォルトでインストールされ、有効になります。 [!DNL Magento Open Source] 2.3.x 以降。

  Commerceを 2.2.x からアップグレードした場合、またはInventory managementを無効にしている場合は、必要なモジュールが含まれるようにインストールを更新します。 参照： [Inventory managementのインストール](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) が含まれる *Inventory management ガイド*.

### 必要システム構成

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x 以降](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) – をアクティブにした場合 [!DNL Amazon Sales Channel] の場合 [!DNL Commerce] sites、を確認する [!DNL Commerce] platform には、インストール前にバージョン 4.4.2 がインストールされています [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### サポートされるプラットフォーム

- クラウド上のAdobe Commerce（ECE） :2.4.x
- Adobe Commerce オンプレミス（EE） :2.4.x
- Magento Open Source 2.4.x

## オンボーディング手順

1. [Walmart Seller アカウントの設定](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [のインストール [!DNL Channel Manager] 拡張子](install.md).

1. [Commerce Services への接続](connect.md) を使用して、Channel Manager をCommerce インスタンスおよびその他のサポートサービスと統合します。

1. [を接続 [!DNL Commerce] に保存 [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [ストアの設定の完了](complete-sales-channel-store-setup.md).
