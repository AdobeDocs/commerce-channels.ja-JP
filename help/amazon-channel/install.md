---
title: 拡張機能のインストール
description: ' [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] を統合し、 [!DNL Amazon Marketplace]を通じて販売するには、AmazonSales Channel拡張機能をダウンロードしてインストールします。'
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# 拡張機能のインストール

>[!IMPORTANT]
>
>AdobeコマースおよびMagento Open Source2.4.xバージョンでは、拡張機能4.0以降のバージョンのみがサポートされています。 [!DNL Amazon Sales Channel]2.3.xバージョンを実行している場合は、[互換性のあるAmazon販売チャネルリリース](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}のドキュメントを参照してください。 バージョンの互換性について詳しくは、開発者向けドキュメントの[Availability](https://devdocs.magento.com/release/availability.html){target=&quot;_blank&quot;}のページを参照してください。

[!UICONTROL Amazon Sales Channel]拡張機能は、[!DNL Amazon Marketplace]を通じて販売するために、コマースカタログを[!DNL Amazon Seller Accounts]と統合する機能をインストールし追加します。 追加情報を確認するには、[!DNL Commerce Marketplace]の[AmazonSales Channel](https://marketplace.magento.com/magento-module-amazon.html)のページと、開発者向けドキュメントの[リリースノート](https://devdocs.magento.com/extensions/amazon-sales/release-notes/)を参照してください。

## 要件

- **コマースインスタンス**:この拡 [!DNL Amazon Sales Channel] 張機能は、Magento Open Source、Adobeコマース、Adobeコマースを含むインスタンスに、クラウドインフラストラクチャバージョン2.3.x以降にインストールできます。2.1、2.2または1.xリリースではサポートされなくなりました。
- **コマースWebアカウント**:APIキーの作成と追跡に使用するCommerce Webアカウントが必要です。
- **APIキー**:コマースWebアカウントを使用して、Amazonの販売チャネルAPIキーを作成します。以下の手順は、これらの手順を含みます。

## インストール

このプロセスでのComposerの使用に関する詳細については、開発者向けドキュメントの[拡張機能のインストール](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}の手順を参照してください。

1. [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}にログインします。

1. 「**[!UICONTROL Marketplace]**」タブをクリックし、「**[!UICONTROL My Purchases]**」をクリックします。

1. **[!UICONTROL Amazon Sales Channel]**&#x200B;を探して選択します。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンに対して、**[!UICONTROL Technical Details]**&#x200B;をクリックします。

1. `composer.json`ファイル内のサービスコネクタエントリを更新するには、名前とバージョン情報を使用します。

   - 拡張機能の名前とバージョンを`composer.json`ファイルに追加します。

   - [!DNL Commerce]プロジェクトディレクトリに移動し、`composer.json`ファイルを更新します。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - [認証キー](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}を入力します。 公開鍵はユーザー名です。秘密鍵はパスワードです。

   - Composerがプロジェクトの依存関係の更新を完了するのを待ち、エラーがないことを確認します。


1. [拡張機能](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}を確認します。

## Amazon販売チャネルAPIキーの追加

インストール後、[APIキー](./amazon-verify-api-key.md)を入力して設定を完了します。

## Amazonチャネル設定オプションの設定

Amazonの販売チャネルを設定するには、次のオプションがあります。 Amazonでのオンボーディングと販売を開始するために、これらの設定を変更する必要はありません。 上級管理者には、これらのオプションを検討することをお勧めします。

1. 管理者にログインします。

1. _管理_&#x200B;サイドバーで、**ストア** / _設定_ / **設定**&#x200B;に移動します。

1. 「**Sales Channel**」、「**グローバル設定**」の順にクリックします。

1. **ログ履歴をクリア**&#x200B;の場合、収集したログをクリアする間隔を定義します。

   `Once Daily`、`Once Weekly`、`Once Monthly`（デフォルト）などのオプションがあります。

1. （オプション）**バックグラウンドタスク(CRON)ソース**&#x200B;の場合、設定を`Command Line (CLI) CRON`に変更します。

   この設定は、**_上級ユーザー/管理者_**&#x200B;に推奨されます。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## 拡張機能の更新

1. [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}にログインします。

1. 「**[!UICONTROL Marketplace]**」タブをクリックし、「**[!UICONTROL My Purchases]**」をクリックします。

1. **[!UICONTROL Amazon Sales Channel]**&#x200B;を探して選択します。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンに対して、**[!UICONTROL Technical Details]**&#x200B;をクリックします。

1. 開発者向けドキュメントの[拡張機能のアップグレード手順](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;}を実行します。
