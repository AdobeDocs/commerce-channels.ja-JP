---
title: 'インストール [!DNL Channel Manager]'
description: 'インストール[!DNL Channel Manager] 拡張。'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---


# インストール [!DNL Channel Manager]

をレビュー [要件](onboard.md#requirements) Channel Manager をインストールする前に、必要な情報を収集します。

## 拡張機能のインストール

Channel Manager のインストール手順は、Adobe CommerceとMagento Open Sourceのどちらがオンプレミスでデプロイされるか、クラウドインフラストラクチャでデプロイされるかによって異なります。

- へのインストール [オンプレミスインスタンス](#install-on-an-on-premises-instance).

- へのインストール [[!DNL Adobe Commerce] クラウドインフラストラクチャインスタンス上](#install-adobe-commerce-on-cloud-infrastructure)

どちらの方法でも、Command Line Interface （CLI; コマンドライン インターフェイス）を使用する必要があります。

>[!NOTE]
>
>のインストールに関するヘルプ [!DNL Commerce] CLI を使用したソフトウェア。を参照してください。 [拡張機能のインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### オンプレミスのインスタンスへのインストール

次の手順を使用して、インストールします [!DNL Channel Manager] （Adobe Commerce上およびオンプレミスインスタンスへのMagento Open Source）。

1. にログインします [!DNL Commerce] サーバー as a [権限を持つユーザー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) に書き込む [!DNL Commerce] ファイルシステム。

1. Web サイトの配置先 [メンテナンスモード](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. から [!DNL Commerce] プロジェクトのルートディレクトリ、にチャネルマネージャーを追加 `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. プロンプトが表示されたら、のアクセスキーを入力 [!DNL Commerce] アカウント。

   公開鍵はユーザー名で、秘密鍵はパスワードです。

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/channel-manager
   ```

   この `composer update` コマンドは、に必要な依存関係のみを更新します。 [!DNL Channel Manager]. すべての依存関係を更新するには、代わりに次のコマンドを使用します。 `composer update`.

1. Composer がプロジェクトの依存関係の更新を終了し、エラーを解決するまで待ちます。

1. モジュールのインストールを確認します。

   - モジュールのステータスを確認します。

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     応答の例：

     ```terminal
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

1. プロンプトが表示されたら、 [!DNL Commerce] プロジェクト。

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

ブランチの使用に関するヘルプについては、 [ブランチの作成の基本を学ぶ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) が含まれる _クラウドインフラストラクチャー上のCommerce ガイド_.

インストール時には、拡張機能名（`magento\channel-manager`）が [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) ファイル。 ファイルを直接編集する必要はありません。

1. ローカルワークステーションで、クラウドプロジェクトのルートディレクトリに変更します。

1. 開発の作成またはチェックアウト [分岐](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html).

1. Composer 名を使用して、拡張機能をに追加します `require` の節 `composer.json` ファイル。

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   この `composer update` コマンドは、に必要な依存関係のみを更新します。 [!DNL Channel Manager]. すべての依存関係を更新するには、代わりに次のコマンドを使用します。 `composer update`.

1. コードの変更を追加、コミット、プッシュします。これには、両方の `composer.lock` および `composer.json` ファイル。

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

```terminal
Module is enabled
```

モジュールが無効になっている場合、 [ローカル環境で有効にします](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) 変更をデプロイします。


1. 拡張機能を正常にインストールしたら、にログインします。 [!UICONTROL Admin] 対象： [Commerce サービスコネクタの設定](connect.md).

   >[!NOTE]
   >
   >チャネルマネージャーを新しいリリースに更新する手順については、を参照してください [モジュールおよび拡張機能のアップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## トラブルシューティング

次の情報を使用して、チャネルマネージャーのインストールプロセス中に発生するエラーを解決します。

### コンポーザーのキーが正しくありません

次の場合 [アクセスキー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) composer リポジトリへの認証に使用する証明書が無効であるか、にリンクされていません [!DNL MAGE ID] に新規登録します [!DNL Channel Manager] サービスで、次のエラーが表示されます。

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

キーの設定を確認します。

1. の場所を検索 `auth.json` ファイル：

   ```bash
   $ composer config –global home
   ```

1. を表示する `auth.json` ファイル。

   ```bash
   $ cat /path/to/auth.json
   ```

1. auth.json の資格情報が一致することを確認します。 [画像 ID に関連付けられたキー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) チャネルマネージャーサービスに登録するために使用されます。

### PHP のメモリ不足

次のエラーは、システムが PHP に十分なメモリを割り当てていない場合に表示されます。

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

メモリの問題を解決するには、次のいずれかの方法を使用します。

- [PHP のメモリ制限を増やす](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) 環境内 `php.ini` ファイル。 また、Commerce インスタンスにが含まれていることを確認します。 [推奨値](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) （その他の PHP 設定の場合）

- コマンドラインからメモリ制限を指定します。

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  例：

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### ビューがありません

欠落に関するエラーが発生した場合 `process_catalog_exporter_view` チャネルマネージャーのインストール中に、 [インデクサーの更新](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### クラウドデプロイメントエラー

拡張機能をクラウドにデプロイする際の問題については、を参照してください [拡張機能のデプロイメントの失敗](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
