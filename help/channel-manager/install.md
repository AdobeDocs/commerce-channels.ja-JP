---
title: 'インストール [!DNL Channel Manager]'
description: '[!DNL Channel Manager] 拡張子。'
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# インストール [!DNL Channel Manager]

以下を確認します。 [要件](onboard.md#requirements) を参照して、必要な情報を収集してから Channel Manager をインストールします。

## 拡張機能のインストール

Channel Manager のインストール手順は、Adobe CommerceまたはMagento Open Sourceがオンプレミスとクラウドインフラストラクチャのどちらにデプロイされているかによって異なります。

- にインストールする [オンプレミスインスタンス](#install-on-an-on-premises-instance).

- にインストールする [[!DNL Adobe Commerce] クラウドインフラストラクチャインスタンス上](#install-adobe-commerce-on-cloud-infrastructure)

どちらの方法でも、CLI（コマンドラインインターフェイス）を使用する必要があります。

>[!NOTE]
>
>インストールに関するヘルプ [!DNL Commerce] CLI を使用するソフトウェア： [拡張機能のインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### オンプレミスインスタンスにインストールする

次の手順を使用して、 [!DNL Channel Manager] オンプレミスインスタンスに対するAdobe CommerceとMagento Open Source。

1. にログインします。 [!DNL Commerce] サーバ as a [権限を持つユーザー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) 宛に書く [!DNL Commerce] ファイルシステム。

1. Web サイトを [メンテナンスモード](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. 次の [!DNL Commerce] プロジェクトのルートディレクトリ、チャネルマネージャーの追加先 `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. プロンプトが表示されたら、 [!DNL Commerce] アカウント

   公開鍵はユーザ名です。秘密鍵はパスワードです。

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/channel-manager
   ```

   この `composer update` コマンドは、 [!DNL Channel Manager]. すべての依存関係を更新するには、代わりに次のコマンドを使用します。 `composer update`.

1. Composer がプロジェクトの依存関係の更新を完了するのを待ち、エラーを解決します。

1. モジュールのインストールを確認します。

   - モジュールのステータスを確認します。

      ```bash
      bin/magento module:status Magento_SalesChannels
      ```

      レスポンスのサンプル：

      ```terminal
      Module is enabled
      ```

   - モジュールが有効になっていない場合は、有効にします。

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

### クラウドインフラストラクチャインスタンス上のAdobe Commerceにインストールする

クラウドインスタンスに拡張機能を追加する際に、開発ブランチで作業します。

分岐の使用に関するヘルプについては、 [ブランチの作成を開始する](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) 内 _Commerce on Cloud Infrastructure ガイド_.

インストール時に、拡張子の名前 (`magento\channel-manager`) は [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) ファイル。 ファイルを直接編集する必要はありません。

1. ローカルワークステーションで、クラウドプロジェクトのルートディレクトリに移動します。

1. 開発の作成またはチェックアウト [分岐](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html).

1. コンポーザー名を使用して、拡張機能を `require` セクション `composer.json` ファイル。

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. 依存関係を更新し、拡張機能をインストールします。

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   この `composer update` コマンドは、 [!DNL Channel Manager]. すべての依存関係を更新するには、代わりに次のコマンドを使用します。 `composer update`.

1. コードの変更を追加、コミット、およびプッシュします。両方の `composer.lock` および `composer.json` ファイル。

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

レスポンスのサンプル：

```terminal
Module is enabled
```

モジュールが無効な場合、 [ローカル環境で有効にする](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) 変更をデプロイします。


1. 拡張機能が正常にインストールされたら、 [!UICONTROL Admin] から [Commerce Services コネクタの設定](connect.md).

   >[!NOTE]
   >
   >Channel Manager を新しいリリースに更新する手順については、 [モジュールと拡張機能のアップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## トラブルシューティング

Channel Manager のインストールプロセス中に発生したエラーを解決するには、次の情報を使用します。

### コンポーザーのキーが正しくありません

この [アクセスキー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) Composer リポジトリへの認証に使用された値が無効か、 [!DNL MAGE ID] ～に新規登録するのに使われる [!DNL Channel Manager] サービスの場合、次のエラーが表示されます。

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

キー設定を確認します。

1. 次の場所を検索： `auth.json` ファイル：

   ```bash
   $ composer config –global home
   ```

1. 次を表示： `auth.json` ファイル。

   ```bash
   $ cat /path/to/auth.json
   ```

1. auth.json の資格情報が一致していることを確認します。 [画像 ID に関連付けられているキー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) Channel Manager サービスの登録に使用します。

### PHP のメモリ不足

次のエラーは、PHP 用に割り当てられたメモリがシステムにない場合に表示されます。

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

メモリの問題を解決するには、次のいずれかの方法を使用します。

- [PHP のメモリ制限を引き上げる](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) 環境内 `php.ini` ファイル。 また、Commerce インスタンスに [推奨値](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) 他の PHP 設定の場合。

- コマンドラインからメモリ制限を指定します。

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   例：

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### ビューが見つかりません

見つからない `process_catalog_exporter_view` Channel Manager のインストール中に、 [インデクサーを更新しています](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### クラウドデプロイメントエラー

拡張機能をクラウドにデプロイする際に問題が発生した場合は、 [拡張機能のデプロイメント失敗](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
