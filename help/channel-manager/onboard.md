---
title: オンボード [!DNL Channel Manager]
description: '''インスタンスを [!DNL Channel Manager] サービスを使用するには、いくつかのオンボーディング手順を完了する必要があります。」'
level: Intermediate
role: Leader, Admin, Developer
feature: Sales Channels, Install
exl-id: 7c4ccd9e-ae32-4511-8d1e-baa690604612
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# オンボード [!DNL Channel Manager]

チャネルマネージャのオンボーディングプロセスが完了すると、Adobe Commerceから Walmart Marketplace チャネルの販売操作にアクセスし、設定し、管理できます。 チャネルマネージャは、 [!UICONTROL Channel Manager] オプションを [!UICONTROL Commerce Admin Marketing] メニュー。

![[!DNL Channel Manager] 管理ビューのオプション](assets/channel-manager-admin-view.png){width="500"}

## 要件

Channel Manager の使用に関する要件を確認し、拡張機能をダウンロード、インストール、設定するために必要なアカウント情報と資格情報を収集します。

- **[Walmart Marketplace の要件](walmart-requirements.md)** — 次を含む Channel Manager と統合するための要件を満たしていることを確認する [セラーアカウントの設定](https://sellerhelp.walmart.com/seller/s/guide?article=000008219) 統合を有効にする API キーを生成する際に使用されます。

- **コマースアカウント情報** — ダウンロードとインストール [!DNL Channel Manager] にはが必要です [コマースアカウント](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html). に対する所有者または管理者アクセス権を持つアカウント ID と資格情報が必要です [!DNL Adobe Commerce] または [!DNL Magento Open Source] インスタンス。

   - **画像 ID**-[ログイン](https://account.magento.com/customer/account/login/) から [!DNL Commerce] ID を取得するアカウント **[!UICONTROL My Account - Magento settings]**.

     ![[!DNL MAGEID] オン [!DNL Commerce] アカウント設定](assets/mageid-my-commerce-account.png){width="250"}

   - **アクセスキー —** ダウンロードする認証キーの取得 [!DNL Commerce] からの拡張 [!DNL Commerce] Composer リポジトリ `([!DNL repo.magento.com]`) をクリックします。

     ![[!UICONTROL Commerce Marketplace access keys]](assets/commerce-marketplace-access-keys.png){width="400"}

     Adobe CommerceおよびMagento Open Sourceプロジェクトでは、所有者は [共有アクセス](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-share.html) 信頼できる従業員およびサービスプロバイダーが所有者またはライセンス所有者のアカウントからの資格情報を使用して拡張機能をダウンロードできるようにする。

     の場合 [!DNL Adobe Commerce] クラウドインフラストラクチャプロジェクトでは、ソフトウェアインストーラーは、 [!DNL Commerce] インスタンス：

      - クラウドプロジェクトへのスーパーユーザーアクセス
      - 特定の環境への管理者アクセス
      - an [!DNL Adobe Commerce] Composer リポジトリにアクセスする権限を持つアカウント

     詳しくは、 [ユーザーアクセスを管理](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) （内） *Commerce on Cloud Infrastructure ガイド*.

- **Composer とを使用したエクスペリエンス[!DNL Commerce CLI]** — 参照 [拡張機能のインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) （内） *インストールガイド* を参照してください。 [!DNL Adobe Commerce] または [!DNL Magento Open Source] プラットフォーム。

- **[[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html)** — アクティブ化した場合 [!DNL Amazon Sales Channel] の [!DNL Commerce] サイト、 [!DNL Commerce] プラットフォームには、インストール前にバージョン 4.4.2 以降がインストールされています [!DNL Channel Manager].

- **[!DNL Inventory Management]Adobe Commerce andMagento Open Sourceの拡張**

  在庫と注文の管理にチャネルマネージャーを使用する予定がある場合は、Adobe CommerceおよびMagento Open SourceインスタンスにInventory management拡張機能をインストールし、有効にしておく必要があります。 通常、この拡張機能は、Adobe Commerceおよび [!DNL Magento Open Source] 2.3.x 以降。

  Commerce を 2.2.x からアップグレードした場合、またはInventory managementを無効にした場合は、必要なモジュールを含めるようにインストールを更新します。 詳しくは、 [Inventory managementのインストール](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html) （内） *Inventory managementガイド*.

### 必要システム構成

- [Adobe Commerce 2.4.x](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html)
- [PHP 7.3 / 7.4](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)
- [Composer 1.x 以降](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/overview.html)
- [[!DNL Amazon Sales Channel] バージョン 4.4.2 以降](https://experienceleague.adobe.com/docs/commerce-channels/amazon/release-notes.html) — アクティブ化済みの場合 [!DNL Amazon Sales Channel] の [!DNL Commerce] サイト、 [!DNL Commerce] プラットフォームには、インストール前にバージョン 4.4.2 がインストールされています [!DNL Channel Manager].
- [[!DNL Inventory Management]](https://experienceleague.adobe.com/docs/commerce-admin/inventory/get-started/install-update.html)

### サポートされるプラットフォーム

- Adobe Commerce on Cloud(ECE) :2.4.x
- Adobe Commerceオンプレミス (EE) :2.4.x
- MAGENTO OPEN SOURCE2.4.x

## オンボーディング手順

1. [Walmart Seller アカウントを設定する](https://seller.walmart.com/signup?q=&amp;origin=solution_provider&amp;src=0014M00001zivMp).

1. [をインストールします。 [!DNL Channel Manager] 拡張](install.md).

1. [Commerce Services に接続](connect.md) :Channel Manager をコマースインスタンスや他のサポートサービスと統合します。

1. [接続する [!DNL Commerce] 保存先 [!DNL Walmart Marketplace]](connect-marketplace.md).

1. [ストア設定の完了](complete-sales-channel-store-setup.md).
