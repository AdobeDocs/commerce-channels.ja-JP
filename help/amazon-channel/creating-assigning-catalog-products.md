---
title: 製品の作成と割り当て
description: Amazon Sales Channel タブには、 [!UICONTROL New Third Party] amazon リストを使用して一致する Commerce カタログ製品を作成し、割り当てることができます。
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# 製品の作成と割り当て

タブが表示されている場合は _[!UICONTROL New Third Party]_、 [!DNL Commerce] カタログ製品を既存の Amazon リスティングに合わせることができます。 この照合には2つのオプションがあります。 既存のカタログ製品に一覧を割り当てたり、その一覧から情報を使用してカタログ製品を作成することができます。 これらのオプションは、Amazon リストが自動的にカタログと一致しない場合に役立ち [!DNL Commerce] ます。

Amazon リストに製品を適合 (割り当て) すれば、Amazon channel の完全な機能セットを使用するために必要になります。

Amazon リスティングからカタログ製品を作成すると、次のようになります。

- この **アークが** SKU になり [!DNL Commerce] ます。
- **製品リスト名が** カタログリストの名前になります。
- **価格** と **数量は、Amazon の** 一覧から読み込まれます。

必要に応じて、その他の設定は、 [!DNL Commerce] 作成時に選択した製品設定によって決定されます。

リストが作成され、対応付けられると、その一覧はタブから削除され、 _[!UICONTROL New Third Party]_タブに表示され_[!UICONTROL Active]_ ます。

## 単一カタログ製品の Amazon の一覧への割り当て

1. タブに製品一覧を表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) します。

1. 目的のリストを検索し、列をクリックし **[!UICONTROL Select]** _[!UICONTROL Action]_て、をクリックし&#x200B;**[!UICONTROL Assign Catalog Product]**ます。

   この操作により、ページが開き _[!UICONTROL Assign Magento Catalog Product]_ます。

1. ワークスペースのコントロールを使用してリストにフィルターを適用するか、リストを選択して [ ](./workspace-controls.md) 、該当するカタログ製品を指定します。

1. リストに正しい製品が表示されたら、 **[!UICONTROL Assign Catalog Product]** 列内をクリックし _[!UICONTROL Action]_ます。

製品と一覧は対応するようになりました。 Amazon 販売チャンネルは、Amazon によって製品を共有し、そのデータを Amazon によって掲載し、出展価格、送料、在庫量、注文情報、状態などの情報を管理することができます。

## Amazon リスティング情報を使用した1つのカタログ製品の作成

1. タブに製品一覧を表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) します。

1. カタログに作成するリストを検索し [!DNL Commerce] 、列をクリックし **[!UICONTROL Select]** て、 _[!UICONTROL Action]_をクリックし&#x200B;**[!UICONTROL Create New Catalog Product]**ます。

   この操作により、ページが開き _[!UICONTROL Create Magento Catalog Product]_ます。

1. 製品のカタログ設定を完了します。

   - **[!UICONTROL Enable Product(s)]**「切り替え先」 `Yes` または `No` 「(必須)」を設定します。

      |はい |店頭販売に適合する製品を作成することを選択し [!DNL Commerce] ます。|
|No |店頭販売の対象外製品とする場合に選択し [!DNL Commerce] ます。 |

   - 「」に **[!UICONTROL Categories]** 、製品のカテゴリを割り当てます (オプション)。

      製品のカテゴリを選択するには、下向きの矢印をクリックし、カテゴリーのチェックボックスを選択します。 **[!UICONTROL Done]**&#x200B;終了したらをクリックします。

   - については、製品が関連付けられている **[!UICONTROL Website Ids]** web サイト (ストア) を選択します。

      このリストに表示されるオプションは、 [!DNL Commerce] [ microsoft store の設定 ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) {target = &quot;_blank&quot;} 設定によって異なります。

   - **[!UICONTROL Attribute Set Id]**(必須) には、いずれかのオプションを選択します。

      `Default` デフォルトでは、このオプションが選択されています。 このリストに表示されるオプションは、設定されて [!DNL Commerce] [ いる属性セット ](https://docs.magento.com/user-guide/stores/attribute-sets.html) {target = &quot;_blank&quot;} によって異なります。

   - については **[!UICONTROL Visibility]** 、新規製品のオプションを選択します。

      |**[!UICONTROL Not Visible Individually]** (デフォルト) |この製品は、店頭には含まれていませんが、他の製品よりもバリエーションがある場合もあります。|
|**[!UICONTROL Catalog]**|カタログリストに製品が表示されます。|
|**[!UICONTROL Search]**|この製品は、検索処理に使用することができます。|
|**[!UICONTROL Catalog and Search]**|この製品は、カタログリストに含まれており、検索操作に使用することができます。 |

   - の場合は、 **[!UICONTROL Assign Tax Class]** 製品のオプションを選択します。

      このリストに表示されるオプションは、設定されている [ tax クラス ](https://docs.magento.com/user-guide/tax/tax-class.html) {target = &quot;_blank&quot;} によって異なります。

   - 完了したら、をクリックし **[!UICONTROL Create Catalog Products]** ます。

カタログ製品がカタログに作成され、 [!DNL Commerce] 作成元の Amazon リスティングに割り当てられます。 既存の Amazon リストと一致するように一覧が表示されます。一覧はタブから削除され、 _[!UICONTROL New Third Party]_タブに表示され_[!UICONTROL Active]_ ます。

## Amazon リスティング情報を使用して、複数のカタログ製品を作成します。

1. タブに製品一覧を表示 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) します。

1. カタログ製品の作成対象となるリストを選択します。

   左側の列で個々のチェックボックスを選択することも、左上の列にある下向きの矢印をクリックして、またはを選択することもでき **[!UICONTROL Select All]** **[!UICONTROL Select All on this Page]** ます。

1. _[!UICONTROL Actions]_でをクリックし&#x200B;**[!UICONTROL Create New Catalog Product(s)]**ます。

1. 確認メッセージを受け入れ、ページを開くには _[!UICONTROL Create Magento Catalog Product]_、をクリックし&#x200B;**[!UICONTROL OK]**ます。

1. 製品のカタログ設定を完了します。

   >[!NOTE]
   >選択した複数のリストに対してカタログ製品を作成すると、入力した製品設定がすべてのリストに適用されます。

   - **[!UICONTROL Enable Product(s)]**「切り替え先」 `Yes` または `No` 「(必須)」を設定します。

      |はい |店頭販売に適合する製品を作成することを選択し [!DNL Commerce] ます。|
|No |店頭販売の対象外製品とする場合に選択し [!DNL Commerce] ます。 |

   - 「」に **[!UICONTROL Categories]** 、製品のカテゴリを割り当てます (オプション)。

      製品のカテゴリを選択するには、下向きの矢印をクリックし、カテゴリーのチェックボックスを選択します。 終了したら「終了」をクリックし **** ます。

   - については、製品が関連付けられている **[!UICONTROL Website Ids]** web サイト (ストア) を選択します。

      このリストに表示されるオプションは、 [!DNL Commerce] [ microsoft store の設定 ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) {target = &quot;_blank&quot;} 設定によって異なります。

   - **[!UICONTROL Attribute Set Id]**(必須) には、いずれかのオプションを選択します。

      `Default` デフォルトでは、このオプションが選択されています。 このリストに表示されるオプションは、設定されて [!DNL Commerce] [ いる属性セット ](https://docs.magento.com/user-guide/stores/attribute-sets.html) {target = &quot;_blank&quot;} によって異なります。

   - については **[!UICONTROL Visibility]** 、新規製品のオプションを選択します。

      |**[!UICONTROL Not Visible Individually]** (デフォルト) |この製品は、店頭には含まれていませんが、他の製品よりもバリエーションがある場合もあります。|
|**[!UICONTROL Catalog]**|カタログリストに製品が表示されます。|
|**[!UICONTROL Search]**|この製品は、検索処理に使用することができます。|
|**[!UICONTROL Catalog and Search]**|この製品は、カタログリストに含まれており、検索操作に使用することができます。 |

   - の場合は、 **[!UICONTROL Assign Tax Class]** 製品のオプションを選択します。

      このリストに表示されるオプションは、設定されている [ tax クラス ](https://docs.magento.com/user-guide/tax/tax-class.html) {target = &quot;_blank&quot;} によって異なります。

   - 完了したら、をクリックし **[!UICONTROL Create Catalog Products]** ます。

カタログ製品がカタログに作成され、 [!DNL Commerce] 作成元の Amazon リストに割り当てられます。 リストが各 Amazon リストと一致するようになった場合は、一覧はタブから削除され、 [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) タブに表示され [_[!UICONTROL Active]_](./active-listings.md) ます。

![Commerce カタログ製品の作成](assets/amazon-magento-catalog-product.png)

| 名 | つい |
|--- |--- |
| [!UICONTROL Enable Product(s)] | 必要この機能が有効になっている場合、製品は店頭で表示され [!DNL Commerce] ます。 オフにした場合、製品は店頭に表示されません [!DNL Commerce] 。 |
| [!UICONTROL Categories] | 新製品のカテゴリの名前を入力するか、下向きの矢印をクリックしてオプションを表示します。 オプションはカテゴリーによって異なり [ ](https://docs.magento.com/user-guide/catalog/category-create.html) ます {target = &quot;_blank&quot;} 設定によって異なります。 |
| [!UICONTROL Website Ids] | 必要製品が関連付けられている web サイト (ストア) を選択します。 オプションは microsoft store の設定によって異なります [!DNL Commerce] [ ](https://docs.magento.com/user-guide/stores/websites-stores-views.html) {target = &quot;_blank&quot;} 設定 |
| 属性セット Id | 属性セットを選択します。 オプションは設定されている属性セットによって異なり [!DNL Commerce] [ ](https://docs.magento.com/user-guide/stores/attribute-sets.html) ます {target = &quot;_blank&quot;}。 |
| [!UICONTROL Visibility] | オプション：<ul><li>**[!UICONTROL Not Visible Individually]** -製品は、店頭では表示されません [!DNL Commerce] (バリエーション製品に最もよく使用されます)。</li><li>**[!UICONTROL Catalog]** Web サイト内に関連付けられているカテゴリーを使用して製品にアクセスできるようにします。</li><li>**検索** -検索ツールを使用してのみ製品が検索されるようにします。</li><li>**[!UICONTROL Catalog and Search]** この機能を使用すると、検索ツールを使用して、カテゴリー構造を使用した製品へのアクセスが許可されます。</li></ul> |
| [!UICONTROL Assign Tax Class] | 新しい製品に税クラスを割り当てます。 オプションは、設定されている税クラスによって異なり [ ](https://docs.magento.com/user-guide/tax/tax-class.html) ます {target = &quot;_blank&quot;}。 |
