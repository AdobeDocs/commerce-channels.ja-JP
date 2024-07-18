---
title: 'インストール  [!DNL Channel Manager]'
description: '[!DNL Channel Manager] 拡張機能をインストールします。'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 1e74150e6ac88dbabb2e4bbb2fa2f243072eb03f
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# [!DNL Channel Manager] のインストール

[ 要件 ](onboard.md#requirements) を確認し、チャネルマネージャーをインストールする前に必要な情報を収集します。

## 拡張機能のインストール

Channel Manager のインストール手順は、Adobe CommerceとMagento Open Sourceのどちらがオンプレミスでデプロイされるか、クラウドインフラストラクチャでデプロイされるかによって異なります。

- [ オンプレミスのインスタンス ](#install-on-an-on-premises-instance) にインストールします。

- [[!DNL Adobe Commerce] on クラウドインフラストラクチャインスタンス ](#install-adobe-commerce-on-cloud-infrastructure) にをインストールします

どちらの方法でも、Command Line Interface （CLI; コマンドライン インターフェイス）を使用する必要があります。

>[!NOTE]
>
>CLI を使用してソフトウェア [!DNL Commerce] インストールする方法については、[ 拡張機能のインストール ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) を参照してください。

### オンプレミスのインスタンスへのインストール

Adobe Commerceに [!DNL Channel Manager] をインストールし、オンプレミスインスタンスにMagento Open Sourceするには、次の手順を使用します。

1. [ 権限を持つユーザー ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) として [!DNL Commerce] サーバーにログインし、[!DNL Commerce] ファイルシステムに書き込みます。

1. Web サイトを [ メンテナンスモード ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html) にします。

   ```bash
   $ bin/magento maintenance:enable
   ```

1. [!DNL Commerce] プロジェクトルートディレクトリから、チャネルマネージャーを `composer.json` に追加します。

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. プロンプトが表示されたら、[!DNL Commerce] アカウントのアクセスキーを入力します。

   公開鍵はユーザー名で、秘密鍵はパスワードです。

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/channel-manager
   ```

   `composer update` コマンドは、[!DNL Channel Manager] に必要な依存関係のみを更新します。 すべての依存関係を更新するには、代わりに次のコマンドを使用します：`composer update`。

1. Composer がプロジェクトの依存関係の更新を終了し、エラーを解決するまで待ちます。

1. モジュールのインストールを確認します。

   - モジュールのステータスを確認します。

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     応答の例：

     ```
     Module is enabled
     ```

   - モジュールが有効になっていない場合は有効にします。

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. 拡張機能を登録します。

   ```bash
   bin/magento setup:upgrade
   ```

1. プロンプトが表示されたら、[!DNL Commerce] プロジェクトを再コンパイルします。

   ```bash
   bin/magento setup:di:compile
   ```

1. キャッシュをクリーンアップします。

   ```bash
   bin/magento cache:clean
   ```

1. メンテナンスモードを無効にします。

   ```bash
   bin/magento maintenance:disable
   ```

### クラウドインフラストラクチャインスタンス上のAdobe Commerceへののインストール

クラウドインスタンスに拡張機能を追加する場合は、開発ブランチで作業します。

Commerce ブランチの使用に関するヘルプについては、{2[Cloud Infrastructure ガイドの ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) ブランチの作成の基本を学ぶ」を参照してください __

インストール時に、拡張機能名（`magento\channel-manager`）が [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) ファイルに自動的に挿入されます。 ファイルを直接編集する必要はありません。

1. ローカルワークステーションで、クラウドプロジェクトのルートディレクトリに変更します。

1. 開発 [ ブランチ ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) を作成またはチェックアウトします。

1. Composer 名を使用して、`composer.json` ファイルの `require` セクションに拡張子を追加します。

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   `composer update` コマンドは、[!DNL Channel Manager] に必要な依存関係のみを更新します。 すべての依存関係を更新するには、代わりに次のコマンドを使用します：`composer update`。

1. コードの変更を追加、コミット、プッシュします。これには、`composer.lock` ファイルと `composer.json` ファイルの両方に対する変更が含まれます。

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. ビルドおよびデプロイプロセスが完了したら、SSH を使用してリモート環境にログインし、拡張機能が正しくインストールされていることを確認します。

```bash
   bin/magento module:status Magento_SalesChannels
```

応答の例：

```
Module is enabled
```

モジュールが無効になっている場合は [ ローカル環境で有効にし ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) 変更をデプロイします。


1. 拡張機能を正常にインストールしたら、[!UICONTROL Admin] にログインして [Commerce サービスコネクタを設定 ](connect.md) します。

   >[!NOTE]
   >
   >チャネルマネージャーを新しいリリースに更新する手順については、[ モジュールと拡張機能をアップグレード ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) を参照してください。


## トラブルシューティング

次の情報を使用して、チャネルマネージャーのインストールプロセス中に発生するエラーを解決します。

### コンポーザーのキーが正しくありません

Composer リポジトリへの認証に使用される [ アクセス キー ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) が無効であるか、[!DNL Channel Manager] サービスへのサインアップに使用される [!DNL MAGE ID] にリンクされていない場合、次のエラーが表示されます。

```
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

キーの設定を確認します。

1. `auth.json` ファイルの場所を見つけます。

   ```bash
   $ composer config –global home
   ```

1. `auth.json` ファイルを表示します。

   ```bash
   $ cat /path/to/auth.json
   ```

1. チャネルマネージャーサービスへの登録に使用される [MAGE ID に関連付けられたキー ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)auth.json の資格情報が一致することを確認します。

### PHP のメモリ不足

次のエラーは、システムが PHP に十分なメモリを割り当てていない場合に表示されます。

```
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

メモリの問題を解決するには、次のいずれかの方法を使用します。

- [PHP のメモリ制限を増やす ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) 環境 `php.ini` ファイル内の。 また、Commerce インスタンスに他の PHP 設定の [ 推奨値 ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) が含まれていることを確認してください。

- コマンドラインからメモリ制限を指定します。

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  例：

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### ビューがありません

Channel Manager のインストール中に `process_catalog_exporter_view` が見つからないというエラーが発生した場合は、[ インデクサーを更新する ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html) ことを試してください。

```bash
php bin/magento indexer:refresh
```

### クラウドデプロイメントエラー

拡張機能をクラウドにデプロイする際の問題については、[ 拡張機能のデプロイメントの失敗 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html) を参照してください。
