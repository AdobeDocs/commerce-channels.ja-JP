---
title: 拡張機能のイ  [!DNL Amazon Sales Channel]  ストール
description: カタログを  [!DNL Commerce]  に統合し、を通じて販売するには  [!DNL Amazon Seller Accounts] Amazon Sales Channel拡張機能をダウンロ  [!DNL Amazon Marketplace] ドしてインストールします。
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# [!DNL Amazon Sales Channel] 拡張機能のインストール

>[!IMPORTANT]
>
>Adobe CommerceとMagento Open Source 2.4.x のバージョンでは、[!DNL Amazon Sales Channel] 拡張機能 4.0 以降のバージョンのみがサポートされています。 2.3.x バージョンを実行している場合は、[ 互換性のあるAmazon sales channel リリース ](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html) のドキュメントを参照してください。 バージョンの互換性について詳しくは、開発者ドキュメントの [ 可用性 ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) ページを参照してください。

[!UICONTROL Amazon Sales Channel] 拡張機能は、Commerce カタログを [!DNL Amazon Seller Accounts] と統合して [!DNL Amazon Marketplace] を通じて販売するための機能をインストールして追加します。 追加情報を確認するには、[!DNL Commerce Marketplace] の [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) ページと [ リリースノート ](release-notes.md) を参照してください。

## 要件

- **Commerce インスタンス**: [!DNL Amazon Sales Channel] 拡張機能は、クラウドインフラストラクチャバージョン 2.3.x 以降に、Magento Open Source、Adobe Commerce、およびAdobe Commerceを備えたインスタンスにインストールできます。 2.1、2.2、1.x リリースではサポートされなくなりました。
- **Commerce web アカウント**: API キーの作成とトラックに使用するCommerce web アカウントが必要です。
- **API キー**:Commerce web アカウントを使用してAmazon Sales Channel API キーを作成します。 以下の手順には、これらの手順が含まれます。

## インストール

このプロセスで Composer を使用する方法の詳細については、開発者向けドキュメントの [ 拡張機能のインストール ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 手順を参照してください。

1. [Commerce Marketplace](https://marketplace.magento.com/customer/account/) にログインします。

1. [**[!UICONTROL Marketplace]**] タブをクリックし、[**[!UICONTROL My Purchases]**] をクリックします。

1. を見つけて、「**[!UICONTROL Amazon Sales Channel]**」を選択します。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネント名とバージョンについては、「**[!UICONTROL Technical Details]**」をクリックします。

1. 名前とバージョン情報を使用して、`composer.json` ファイルのサービスコネクタエントリを更新します。

   - `composer.json` ファイルに拡張機能名とバージョンを追加します。

   - [!DNL Commerce] プロジェクトディレクトリに移動して、`composer.json` ファイルを更新します。

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - [ 認証キー ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) を入力します。 公開鍵はユーザー名で、秘密鍵はパスワードです。

   - Composer がプロジェクトの依存関係の更新を終了し、エラーがないことを確認するまで待ちます。

1. [ 拡張機能を確認します ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html)。

## Amazon sales channel API キーを追加します。

インストール後、[API キー ](./amazon-verify-api-key.md) を入力して設定を完了します。

## Amazon チャネル設定オプションの指定

Amazon Sales Channel の設定には、次のオプションがあります。 Amazonでオンボーディングと販売を開始するために、これらの設定を変更する必要はありません。 上級管理者には、これらのオプションを検討することをお勧めします。

1. 管理者にログインします。

1. _管理者_ サイドバーで、**ストア**/_設定_/**設定** に移動します。

1. 「**Sales Channel**」をクリックし、「**グローバル設定**」をクリックします。

1. **ログ履歴を消去** には、収集したログを消去する間隔を定義します。

   オプションには、`Once Daily`、`Once Weekly`、`Once Monthly` （デフォルト）があります。

1. （オプション） **バックグラウンドタスク（CRON）Source** の場合は、設定を `Command Line (CLI) CRON` に変更します。

   この設定は、**_上級ユーザー/管理者_** にお勧めします。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 拡張機能の更新

1. [Commerce Marketplace](https://marketplace.magento.com/customer/account/) にログインします。

1. [**[!UICONTROL Marketplace]**] タブをクリックし、[**[!UICONTROL My Purchases]**] をクリックします。

1. を見つけて、「**[!UICONTROL Amazon Sales Channel]**」を選択します。

1. 拡張機能ページで、バージョンを選択します。

1. コンポーネント名とバージョンについては、「**[!UICONTROL Technical Details]**」をクリックします。

1. [ インストール ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) の _拡張機能のアップグレード手順_ を実行します。
