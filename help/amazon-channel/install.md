---
title: 拡張機能のインストール
description: との統合につい  [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts]  ては、  [!DNL Amazon Marketplace] Amazon Sales Channel 拡張機能をダウンロードしてインストールします。
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# 拡張機能のインストール

>[!IMPORTANT]
>
>[!DNL Amazon Sales Channel]Adobe Commerce および Magento Open Source 2.4 .x 版では、extension 4.0 以降のバージョンのみがサポートされています。バージョン2.3 以降を実行している場合は、 [ 対応する Amazon sales channel channel release チャネルリリースのマニュアルを参照してください ](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html) {target = &quot;_blank 「}」を参照してください。 バージョンの互換性について詳しくは、 [ ](https://devdocs.magento.com/release/availability.html) 開発者向けドキュメントの Availability {target = &quot;_blank&quot;} ページを参照してください。

拡張機能を [!UICONTROL Amazon Sales Channel] 使用すると、によって、を通じて商取引カタログを統合する機能がインストールおよび追加され [!DNL Amazon Seller Accounts] [!DNL Amazon Marketplace] ます。 その他の情報については、 [ の Amazon Sales Channel ](https://marketplace.magento.com/magento-module-amazon.html) ページ [!DNL Commerce Marketplace] および [ ](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) 開発者向けドキュメントのリリースノートを参照してください。

## 要望

- **Commerce インスタンス** : [!DNL Amazon Sales Channel] 拡張機能は、Magento Open Source、adobe 経済、adobe commerce on cloud infrastructure .x 以降にインストールされている場合にのみ使用できます。 2.1、2.2、または 1. x リリースではサポートされなくなりました。
- **Commerce web アカウント** : API キーの作成と追跡に使用される commerce web アカウントを持っている必要があります。
- **API キー** : 電子商取引 web アカウントを使用して、Amazon sales CHANNEL API キーを作成します。 次の手順では、この手順について説明します。

## Install

この処理に対して Composer を使用する方法について詳しくは、 [ 拡張機能の _blank インストールに関する開発マニュアルを参照してください ](https://devdocs.magento.com/extensions/install/) 。

1. Commerce Marketplace にログインし [ ](https://marketplace.magento.com/customer/account/) ます {target = &quot;_blank&quot;}。

1. タブをクリックし、を **[!UICONTROL Marketplace]** クリックし **[!UICONTROL My Purchases]** ます。

1. 検索して選択し **[!UICONTROL Amazon Sales Channel]** ます。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンを指定するには、をクリックし **[!UICONTROL Technical Details]** ます。

1. 名前とバージョン情報を使用して、ファイル内の services connector エントリを更新し `composer.json` ます。

   - 拡張機能の名前とバージョンをファイルに追加し `composer.json` ます。

   - [!DNL Commerce]プロジェクトディレクトリに移動し、ファイルを更新し `composer.json` ます。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - 認証キーを入力してください ( [ ](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html) {target = &quot;_blank&quot;})。 公開キーはユーザー名です。秘密キーは、パスワードとして使用されます。

   - Composer によりプロジェクトの依存関係の更新が完了するのを待ち、エラーが発生しないようにします。


1. [拡張機能 ](https://devdocs.magento.com/extensions/install/#verify-the-extension) {target = &quot;_blank&quot;} を確認してください。

## Amazon sales channel API キーを追加します。

インストールが完了したら、API キーを入力して [ ](./amazon-verify-api-key.md) 設定を完了します。

## Amazon channel configuration オプションを設定します。

Amazon sales チャンネルを設定するには、次のオプションを使用します。 Amazon によってオンボードと販売が開始されるように、これらの設定を変更する必要はありません。 これらのオプションについては、高度な管理者が検討することをお勧めします。

1. 管理者にログインします。

1. _管理_ サイドバーで、「 **> の** 設定 > Configuration」に移動 __ **** します。

1. **「販売チャンネル** 」をクリックし、「グローバル設定」をクリックし **** ます。

1. **ログの履歴を消去するには、収集され** たログを消去する間隔を指定します。

   オプションには、、、 `Once Daily` `Once Weekly` および `Once Monthly` (デフォルト) を指定できます。

1. オプション **バックグラウンドタスク (CRON) ソース** では、の設定をに変更 `Command Line (CLI) CRON` します。

   この設定は、 **_上級ユーザー/管理者にお勧め_** します。

1. をクリックし **[!UICONTROL Save Config]** ます。

## 拡張機能の更新

1. Commerce Marketplace にログインし [ ](https://marketplace.magento.com/customer/account/) ます {target = &quot;_blank&quot;}。

1. タブをクリックし、を **[!UICONTROL Marketplace]** クリックし **[!UICONTROL My Purchases]** ます。

1. 検索して選択し **[!UICONTROL Amazon Sales Channel]** ます。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネントの名前とバージョンを指定するには、をクリックし **[!UICONTROL Technical Details]** ます。

1. [開発者向けドキュメントで、拡張機能のアップグレード手順 ](https://devdocs.magento.com/extensions/install/#upgrade-an-extension) {target = &quot;_blank&quot;} を入力します。
