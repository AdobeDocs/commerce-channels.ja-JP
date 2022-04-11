---
title: オンボード [!DNL Channel Manager]
description: インスタンスを [!DNL Channel Manager] サービスを使用するには、いくつかのオンボーディング手順を完了します。
role: User
level: Intermediate
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 41a6afec60edbb23492627bd8e80632d3c952caf
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# オンボード [!DNL Channel Manager]

Channel Manager 拡張機能を [!DNL Commerce] インスタンスを作成し、API 接続を設定します。 これらの接続を使用すると、コマースインスタンスと [!DNL Walmart Marketplace].

オンボーディングが完了したら、 [!UICONTROL Channel Manager] オプションを [!UICONTROL Commerce Admin Marketing] メニュー

![[!DNL Channel Manager] 管理ビューのオプション](assets/channel-manager-admin-view.png)

## オンボーディングの概要

1. [のインストール [!DNL Channel Manager] 拡張](install.md).

1. [の設定 [!DNL Commerce Services Connector]](connect.md) :Channel Manager をコマースインスタンスや他のサポートサービスと統合します。

1. [接続 [!DNL Commerce] 保存先 [!DNL Walmart Marketplace]](connect.md).

1. [ストア設定の完了](complete-store-setup.md).

## 前提条件

- 必要な [Walmart Marketplace の前提条件](walmart-prerequisites.md) を使用して、チャネルマネージャーと統合します。

- **コマースアカウント情報** — ダウンロードとインストール [!DNL Channel Manager] にはが必要です [コマースアカウント](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;}。 に対する所有者または管理者アクセス権を持つアカウント ID と資格情報が必要です [!DNL Adobe Commerce] または [!DNL Magento Open Source] インスタンス。

   - **画像 ID**-[ログイン](https://account.magento.com/customer/account/login/) から Commerce アカウントに ID を取得します。 **[!UICONTROL My Account - Magento settings]**. に登録するには、この ID が必要です [!DNL Channel Manager] サービスベータプログラム。

      ![[!DNL MAGEID] コマースアカウント設定で](assets/mageid-my-commerce-account.png)

   - **アクセスキー —** Commerce Composer リポジトリから Commerce 拡張機能をダウンロードするための認証キーを取得します `([!DNL repo.magento.com]`) をクリックします。

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Adobe CommerceおよびMagento Open Sourceプロジェクトでは、所有者は [共有アクセス](https://docs.magento.com/user-guide/magento/magento-account-share.html) 信頼できる従業員およびサービスプロバイダーが所有者またはライセンス所有者のアカウントからの資格情報を使用して拡張機能をダウンロードできるようにする。

      の場合 [!DNL Adobe Commerce] クラウドインフラストラクチャプロジェクトでは、ソフトウェアインストーラーは、 [!DNL Commerce] インスタンス：

      - クラウドプロジェクトへのスーパーユーザーアクセス
      - 特定の環境への管理者アクセス
      - an [!DNL Adobe Commerce] または [!DNL Magento Open Source] Composer リポジトリにアクセスする権限を持つアカウント

      詳しくは、 [ユーザーアクセスを管理](https://devdocs.magento.com/cloud/project/user-admin.html).


- **Channel Manager Composer パッケージのダウンロードの認証**-Adobeチャネルのベータコーディネーターに、 [!DNL Commerce] 組織のサービスの管理に使用するアカウント。
- **Composer と[!DNL Commerce CLI]**  — 参照 [一般的な CLI のインストール](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}」を参照してください。 [!DNL Adobe Commerce] または [!DNL Magento Open Source] プラットフォーム。
- [[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — アクティブ化済みの場合 [!DNL Amazon Sales Channel] の [!DNL Commerce] サイト、 [!DNL Commerce] インストールする前に、プラットフォームにバージョン 4.42 がインストールされている [!DNL Channel Manager].

### 要件

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x 以降](https://devdocs.magento.com/cloud/reference/cloud-composer.html)
- [[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — アクティブ化済みの場合 [!DNL Amazon Sales Channel] の [!DNL Commerce] サイト、 [!DNL Commerce] インストールする前に、プラットフォームにバージョン 4.42 がインストールされている [!DNL Channel Manager].
- [!DNL Inventory Management]


### サポートされるプラットフォーム

- Adobe Commerce on Cloud (ECE) :2.4.x
- Adobe Commerceオンプレミス (EE) :2.4.x
- Magento Open Source2.4.x
