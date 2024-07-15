---
title: 設定の概要
description: 「認証を設定する  [!DNL Channel Manager settings]  と、と  [!DNL Walmart Marketplace] の間で販売業務を調整するために必要な製品カタログ属性と配送業者をマッピングする  [!DNL Commerce]  について説明します。」
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# 設定の概要

販売チャネル設定を使用すると、[!DNL Commerce] と [!DNL Walmart Marketplace] の間の通信およびデータ同期が可能になるので、[!DNL Commerce] Admin から [!DNL Walmart Marketplace] の販売操作を管理できます。

[!DNL Channel Manager] では、オンボーディングプロセス中に一部の販売チャネル設定を行います。 オンボーディング後は、[!UICONTROL Listings] ダッシュボードと [!UICONTROL Orders] ダッシュボードから **[!UICONTROL Channel Settings]** を選択して、設定を表示および管理できます。

* **[ウォルマート接続](manage-wmt-connection.md)**-[!DNL Channel Manager] のオンボーディングプロセス中に、[!DNL Walmart Marketplace] の販売者アカウントから [API 資格情報 ](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) を提供して、通信およびデータ同期のために [!DNL Commerce] を [!DNL Walmart Marketplace] に接続します。 必要に応じて、*チャネル設定* ページからこれらの資格情報を更新できます。

* **[一意の識別子をマッピング](map-catalog-attributes.md)** – リストを [!DNL Commerce] から [!DNL Walmart Marketplace] に接続する前に、[!DNL Commerce] カタログの少なくとも 1 つの一意の識別子を、ウォルマートの対応する識別子にマッピングします。 この手順は、[!DNL Commerce] 製品を既存の [!DNL Walmart] リストと照合し、[!DNL Commerce] と [!DNL Walmart] の間で製品データを同期するために必要です。

* **[配送業者のマッピング](map-shipping-carriers.md)** - [!DNL Commerce] からの注文を処理する前に、[!DNL Commerce] インスタンスの [!DNL Walmart Marketplace] 送業者を、[!DNL Walmart Marketplace] の対応する配送業者にマッピングする必要があります。
