---
title: のインストール [!DNL Amazon Sales Channel] 拡張子
description: を統合するには [!DNL Commerce] のカタログ [!DNL Amazon Seller Accounts] を通じて販売します [!DNL Amazon Marketplace]で、Amazon Sales Channel拡張機能をダウンロードしてインストールします。
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# のインストール [!DNL Amazon Sales Channel] 拡張子

>[!IMPORTANT]
>
>のみ [!DNL Amazon Sales Channel] 拡張機能 4.0 以降のバージョンは、Adobe CommerceおよびMagento Open Source 2.4.x のバージョンでサポートされています。 2.3.x バージョンを実行している場合は、のドキュメントを参照してください [互換性のあるAmazon セールスチャネルリリース](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). バージョンの互換性の詳細については、 [対象](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) このページについては、開発者向けドキュメントを参照してください。

この [!UICONTROL Amazon Sales Channel] 拡張機能は、Commerce カタログとを統合するための機能をインストールして追加します [!DNL Amazon Seller Accounts] 店を通じて売る [!DNL Amazon Marketplace]. 追加情報を確認するには、を参照してください [AmazonSales Channel](https://marketplace.magento.com/magento-module-amazon.html) のページ [!DNL Commerce Marketplace] および [リリースノート](release-notes.md).

## 要件

- **Commerce インスタンス**：です [!DNL Amazon Sales Channel] 拡張機能は、Magento Open Source、Adobe Commerce、Adobe Commerce（クラウドインフラストラクチャバージョン 2.3.x 以降）のインスタンスにインストールできます。 2.1、2.2、1.x リリースではサポートされなくなりました。
- **Commerce web アカウント**:API キーの作成とトラックに使用するCommerce web アカウントが必要です。
- **API キー**:Commerce web アカウントを使用してAmazon販売チャネル API キーを作成します。 以下の手順には、これらの手順が含まれます。

## インストール

このプロセスで Composer を使用する方法の詳細については、 [拡張機能のインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 手順については、開発者ドキュメントを参照してください。

1. にログインします [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. 「」をクリックします **[!UICONTROL Marketplace]** タブをクリックし、 **[!UICONTROL My Purchases]**.

1. を見つけて選択します。 **[!UICONTROL Amazon Sales Channel]**.

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネント名とバージョンで、 **[!UICONTROL Technical Details]**.

1. の名前とバージョン情報を使用して、のサービスコネクタエントリを更新します `composer.json` ファイル。

   - 拡張機能の名前とバージョンを `composer.json` ファイル。

   - に移動します [!DNL Commerce] プロジェクトディレクトリとアップデート `composer.json` ファイル。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - を入力 [認証キー](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). 公開鍵はユーザー名で、秘密鍵はパスワードです。

   - Composer がプロジェクトの依存関係の更新を終了し、エラーがないことを確認するまで待ちます。

1. [拡張機能の検証](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Amazon sales channel API キーを追加します。

インストール後、 [API キー](./amazon-verify-api-key.md) をクリックして設定を完了します。

## Amazon チャネル設定オプションの指定

Amazon Sales Channel の設定には、次のオプションがあります。 Amazonでオンボーディングと販売を開始するために、これらの設定を変更する必要はありません。 上級管理者には、これらのオプションを検討することをお勧めします。

1. 管理者にログインします。

1. 日 _Admin_ サイドバー、に移動 **ストア** > _設定_ > **設定**.

1. クリック **Sales Channel**、次に **グローバル設定**.

1. の場合 **ログ履歴のクリア**、収集したログを消去する間隔を定義します。

   次のようなオプションがあります `Once Daily`, `Once Weekly`、および `Once Monthly` （デフォルト）。

1. （オプション） **バックグラウンドタスク（CRON）ソース**、設定をに変更します `Command Line (CLI) CRON`.

   この設定は、 **_上級ユーザー/管理者_**.

1. クリック **[!UICONTROL Save Config]**.

## 拡張機能の更新

1. にログインします [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. 「」をクリックします **[!UICONTROL Marketplace]** タブをクリックし、 **[!UICONTROL My Purchases]**.

1. を見つけて選択します。 **[!UICONTROL Amazon Sales Channel]**.

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネント名とバージョンで、 **[!UICONTROL Technical Details]**.

1. を完了する [拡張機能のアップグレード手順](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) が含まれる _インストールガイド_.
