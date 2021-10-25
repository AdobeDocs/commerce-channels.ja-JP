---
title: Amazon と Commerce カタログについて
description: Amazon sales チャンネルは、Amazon リストを Commerce バックエンドに取り込むと共に、製品と販売を継続的に同期します。
exl-id: 659c9830-0a1d-4a0d-bb9c-afb609c0fbba
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 0%

---

# Amazon とカタログについて [!DNL Commerce]

Adobe Commerce または Magento Open Source バックエンドには、すべての製品と、関連する設定と情報 (画像、オプション、価格、その他)、注文と出荷の設定が記載されています。 [!DNL Amazon Seller Central]また、取引先企業には、によって販売が厳重に管理されてい [!DNL Amazon Marketplace] ます。

1つの場所から製品カタログと販売の管理を改善するには、amazon channel channel によって Amazon リストがバックエンドにインポートさ [!DNL Commerce] れ、製品と販売の同期が継続されると共に問題と傾向が報告されます。 Storefronts では、複数のアカウントによる統合がサポートされているの [!DNL Amazon Seller Central] で、複数のインターフェイスを使用してすべてのデータを管理できます。

## 製品属性

Adobe Commerce と Magento Open Source manage catalog は、製品の [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) 設定とデータを定義するために製品属性を使用して同期されます ({target = &quot;_blank&quot;})。 Amazon は、属性を使用して、オンボードにマップされます。 [Amazon sales channel の事前設定タスクの実行中に ](./amazon-pre-setup-tasks.md) 、amazon リストをカタログにインポートする際に正しい製品マッピングを保証するために、必要に応じて追加の Amazon 属性を定義することができ [!DNL Commerce] ます。これらの属性には、UPC、EAN、ISBN、およびアーク () があり [!DNL Amazon Standard Identification Number] ます。 オンボードでは、属性を使用して Amazon とカタログとの間で製品が同期さ [!DNL Commerce] れます。 また、Amazon 製品の適切なマッピングに [!DNL Commerce] より、製品情報、注文、および在庫が常に同期されるようになっています。

これらの属性をカタログに作成していない場合は、 [!DNL Commerce] [ ](https://docs.magento.com/user-guide/catalog/product-attributes.html) オンにする前に製品属性 {target = &quot;_blank&quot;}、および値を製品に追加する必要があります。 Amazon attribute がインポートされると、検索、ナビゲーション、価格ルールなどに使用できます。 これらの属性について詳しくは、 [ Amazon: UPCs、EANs、ISBNs および ASINs を参照してください。](https://www.amazon.com/gp/seller/asin-upc-isbn-info.html){target = &quot;_blank&quot;}

オンにした後は、製品属性と Amazon マッピングをいつでも管理して更新できます。

## 製品一覧

Amazon リスティングは、から製品の [!DNL Amazon Marketplace] 説明、価格、イメージが表示されると、さらに属性によりマップされているすべての製品の製品ページです。 オンボードの際に、 [!DNL Commerce] 製品を Amazon リストに自動的に公開するように設定することができます。 また、既存の Amazon リストを製品にマップすることによって、それらをインポートすることもでき [!DNL Commerce] ます。

出展製品を作成した後 [!DNL Commerce] 、それらの製品は、Amazon に提出されて承認が求められます。 ほとんどの場合、成功したリストは数時間以内に承認されます。 登録が承認されると、に [!DNL Amazon Marketplace] よってはの顧客によって直ちに注文で表示されます。 拡張機能には、 [!DNL Amazon Sales Channel] Amazon リストを確認するためのタブのセットが用意されています。 問題または必要なデータによっては、これらの一覧について詳しくは、アカウントを確認する必要があり [!DNL Amazon Seller Central] ます。

- [Active ](./active-listings.md) : marketplace 経由で利用可能な承認済み製品一覧の一覧が表示されます。

- [「リストの準備」: 「製品リスト」を掲載し ](./ready-to-list.md) ており、Amazon に公開する準備ができています。

- [Inactive ](./inactive-listings.md) : 特定の理由 (ブランドに起因する問題など)、relisting、その他の必要な理由によってブロックされているため、marketplace で利用できない製品が表示されます。

- [不適格 ](./ineligible-listings.md) : リストルールにより、marketplace にアクティブに表示されない製品がリストに表示され `0` ます (量や販売日など)。

- [不完全 ](./incomplete-listings.md) : 表示されない製品に必要な情報が不足しています。 別のレビュー用に製品データを更新します。

- [終了 ](./ended-listings.md) : リストに適合しているが、Amazon から手動で削除された製品一覧を一覧表示します。 これらの製品は、再表示することができます。

## データの同期

Adobe Commerce および Magento Open Source [!DNL Amazon Seller Central] は、アカウントとバックエンドの間で製品と注文データをやり取りし [!DNL Commerce] ます。 この継続的なアップデートでは、 [!DNL Commerce] インベントリの管理、注文の実行、販売の追跡、負担の軽減、および作業の複製を行うための1つのソースが提供されます。 レポートには、2つのシステム間でキャッチされるトレンドを追跡し、通信に関する問題を解決するための最新のデータが記録されます。

すべての同期は、 [ cron ジョブ ](https://docs.magento.com/user-guide/system/cron.html) {target = &quot;_blank&quot;} によって管理され、セットアップ前のタスクの5分ごとに更新するように設定されてい [ ](./amazon-pre-setup-tasks.md) ます。
