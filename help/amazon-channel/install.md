---
title: 拡張機能のインストール
description: を統合するには、以下を実行します。 [!DNL Commerce] 次のカタログ [!DNL Amazon Seller Accounts] そして、を通じて販売する [!DNL Amazon Marketplace]、 Amazon Extension をダウンロードしてインストールします。
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 拡張機能のインストール

>[!IMPORTANT]
>
>のみ [!DNL Amazon Sales Channel] Adobe CommerceとMagento Open Source2.4.x では、拡張機能 4.0 以降のバージョンがサポートされています。 2.3.x バージョンを実行している場合は、 [互換性のあるAmazonセールスチャネルリリース](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target="_blank"}. For more information about version compatibility, see the [Availability](https://devdocs.magento.com/release/availability.html){target="_blank"} ページを参照してください。

この [!UICONTROL Amazon Sales Channel] 拡張機能は、コマースカタログをと統合する機能をインストールして追加します。 [!DNL Amazon Seller Accounts] 通して売る [!DNL Amazon Marketplace]. 追加情報を確認するには、 [AmazonSales Channel](https://marketplace.magento.com/magento-module-amazon.html) ページ内 [!DNL Commerce Marketplace] そして [リリースノート](release-notes.md).

## 要件

- **コマースインスタンス**:この [!DNL Amazon Sales Channel] 拡張機能は、Magento Open Source、Adobe Commerce、Adobe Commerceの各クラウドインフラストラクチャバージョン 2.3.x 以降を使用して、インスタンスにインストールできます。 2.1、2.2 または 1.x リリースではサポートされなくなりました。
- **コマース Web アカウント**:API キーの作成と追跡に使用する Commerce Web アカウントが必要です。
- **API キー**:コマース Web アカウントを使用して、Amazonセールスチャネル API キーを作成します。 以下の手順に、これらの手順を示します。

## インストール

このプロセスでの Composer の使用について詳しくは、 [拡張機能のインストール](https://devdocs.magento.com/extensions/install/){target="_blank"} 開発者向けドキュメントの手順

1. にログインします。 [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target="_blank"}.

1. 次をクリック： **[!UICONTROL Marketplace]** 「 」タブで、「 」をクリックします。 **[!UICONTROL My Purchases]**.

1. を探して選択 **[!UICONTROL Amazon Sales Channel]**.

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンに対して、 **[!UICONTROL Technical Details]**.

1. 名前とバージョン情報を使用して、 `composer.json` ファイル。

   - 拡張機能の名前とバージョンを `composer.json` ファイル。

   - 次の場所に移動： [!DNL Commerce] プロジェクトディレクトリを作成し、 `composer.json` ファイル。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - を入力します。 [認証キー](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target="_blank"}. 公開鍵はユーザ名です。秘密鍵はパスワードです。

   - Composer がプロジェクトの依存関係の更新を完了するのを待ち、エラーが発生しないことを確認します。


1. [拡張機能の検証](https://devdocs.magento.com/extensions/install/#verify-the-extension){target="_blank"}.

## Amazonセールスチャネル API キーの追加

インストール後、 [API キー](./amazon-verify-api-key.md) 設定を完了します。

## Amazonチャネル設定オプションの設定

Amazonのセールスチャネルを設定するには、次のオプションがあります。 Amazonでのオンボーディングと販売を開始する際に、これらの設定を変更する必要はありません。 上級管理者は、これらのオプションを考慮することをお勧めします。

1. 管理者にログインします。

1. の _管理者_ サイドバー、移動 **ストア** > _設定_ > **設定**.

1. クリック **Sales Channel**&#x200B;を、 **グローバル設定**.

1. の場合 **ログ履歴をクリア**、収集したログをクリアする間隔を定義します。

   次のオプションがあります `Once Daily`, `Once Weekly`、および `Once Monthly` （デフォルト）。

1. （オプション）の **バックグラウンドタスク (CRON) のソース**、設定を `Command Line (CLI) CRON`.

   この設定は、 **_上級ユーザー/管理者_**.

1. クリック **[!UICONTROL Save Config]**.

## 拡張機能の更新

1. にログインします。 [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target="_blank"}.

1. 次をクリック： **[!UICONTROL Marketplace]** 「 」タブで、「 」をクリックします。 **[!UICONTROL My Purchases]**.

1. を探して選択 **[!UICONTROL Amazon Sales Channel]**.

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンに対して、 **[!UICONTROL Technical Details]**.

1. 次を完了： [拡張機能のアップグレード手順](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target="_blank"} （開発者向けドキュメント）。
