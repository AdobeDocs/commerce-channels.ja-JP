---
title: 「オンボード [!DNL Channel Manager]"
description: インスタンスを [!DNL Channel Manager] サービスを使用するには、いくつかのオンボーディング手順を完了します。
role: User
level: Intermediate
source-git-commit: ff87f31fec7a689385a93b8cab260fd93ff15f90
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# オンボード [!DNL Channel Manager]

Channel Manager 拡張機能を [!DNL Commerce] Commerce インスタンスと Walmart Marketplace 間の通信とデータの同期を有効にするための API 接続のインスタンスと設定。

オンボーディングが完了したら、 [!UICONTROL Channel Manager] オプションを [!UICONTROL Commerce Admin Marketing] メニュー

![[!DNL Channel Manager] 管理ビューのオプション](assets/channel-manager-admin-view.png)

## オンボーディングの概要

1. [のインストール [!DNL Channel Manager] 拡張](install.md).

1. [の設定 [!DNL Commerce Services Connector]](connect.md) :Channel Manager をコマースインスタンスや他のサポートサービスと統合します。

1. [接続 [!DNL Commerce] 保存先 [!DNL Walmart Marketplace]](connect.md).

## 前提条件

- Walmart Marketplace セラーアカウント Walmart Marketplace での販売に関する要件があることを確認します。

- **コマースアカウント情報** — ダウンロードとインストール [!DNL Channel Manager] には、からの ID と資格情報が必要です [コマースアカウント](https://docs.magento.com/user-guide/magento/magento-account.html){target=&quot;_blank&quot;} ( 所有者が [!DNL Adobe Commerce] または [!DNL Magento Open Source] インスタンス。

   - **画像 ID**-[ログイン](https://account.magento.com/customer/account/login/) から Commerce アカウントに ID を取得します。 [!UICONTROL My Account - Magento settings]. に登録するには、この ID が必要です [!DNL Channel Manager] サービスベータプログラム。

      ![[!DNL MAGEID] コマースアカウント設定で](assets/mageid-my-commerce-account.png)

   - **アクセスキー —** Commerce Composer リポジトリ ([!DNL repo.magento.com]) をクリックします。

      ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png)

      Adobe CommerceおよびMagento Open Sourceプロジェクトでは、所有者は [共有アクセス](https://docs.magento.com/user-guide/magento/magento-account-share.html) 信頼できる従業員およびサービスプロバイダーが所有者またはライセンス所有者のアカウントからの資格情報を使用して拡張機能をダウンロードできるようにする。

      オン [!DNL Adobe Commerce] クラウドインフラストラクチャプロジェクトで、ユーザーは、 [!DNL Commerce] インスタンス：

      - クラウドプロジェクトへのスーパーユーザーアクセス
      - 特定の環境への管理者アクセス
      - an [!DNL Adobe Commerce] または [!DNL Magento Open Source] Composer リポジトリにアクセスする権限を持つアカウント。 詳しくは、 [ユーザーアクセスを管理](https://devdocs.magento.com/cloud/project/user-admin.html).

- **Channel Manager Composer パッケージのダウンロードの認証** — サービスの管理に使用するコマースアカウントから、組織のベータプログラムを調整するAdobe担当者に MAGE ID を提供します。
- **Composer と[!DNL Commerce CLI]**  — 参照 [一般的な CLI のインストール](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} を参照してください。[!DNL Adobe Commerce] または [!DNL Magento Open Source] プラットフォーム。
- AmazonSales Channelがインストールされているコマースインスタンスの場合は、 [AmazonSales Channelバージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) は、Channel Manager をインストールする前にインストールされます。


### 要件

- [Adobe Commerce 2.4.x](https://devdocs.magento.com/release/released-versions.html)
- [PHP 7.3 / 7.4](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html)
- [Composer 1.x 以降](https://devdocs.magento.com/cloud/reference/cloud-composer.html)


### サポートされるプラットフォーム

- Adobe Commerce on Cloud (ECE) :2.4.x
- Adobe Commerceオンプレミス (EE) :2.4.x
- Magento Open Source2.4.x
