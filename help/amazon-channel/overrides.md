---
title: 価格
description: Amazon 販売チャンネルの「オーバーライド」タブでは、Amazon リストに上書きを適用する方法を確認および管理することができます。
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# 価格

このタブには、上書きを適用した _[!UICONTROL Overrides]_Amazon リストが表示されます。 オーバーライドは、定義済みの値をリストに設定できるようにするために、リスティングに使用される設定項目です。 リストに適用された上書きは、その他の定義済みリスティング設定またはリストが対象となっているルールに関係なく、リストの設定を定義します。 リストに上書きが適用されている場合は、そのリストがタブに表示され_[!UICONTROL Overrides]_ ます。 上書きによって定義された値がリストの適切な列に表示されます。 適用できる上書きには、価格、処理時間、条件、および販売者の4つのタイプがあります。

## 上書きの種類

| 入力 | つい |
|---|---|
| 定価 | 一覧の他のすべての価格設定を無視して、リストの価格を設定する上書き。 <br><br>**次の例では、** カタログの特定のカテゴリに属するすべての製品に適用される20% の割引価格ルールを定義しています。 新機能が市販されていて、需要が高い製品を使用している場合は、そのカテゴリーに製品が含まれていても、リストに適用された割引価格が表示されないようにする必要があります。 このリストを選択して [ 価格上書きを作成 ](./creating-editing-overrides.md#edit-override-single-listing) し、価格変更でリスト価格を定義することができます。 |
| 処理時間 | リスティング設定に設定されているデフォルトの処理時間を無視して、リスティングに処理時間を設定する上書き。<br><br>**例** : リストの処理時間の初期設定は、2日に設定されています。 製品には脆弱な点があります。また、別途出荷用にパッケージ化する必要があります。 一覧を表示し、 [ 取扱時間の上書きを作成 ](./creating-editing-overrides.md#edit-override-single-listing) し、処理時間を3日で定義することができます。<br><br>**注意:** 製品がに設定されている場合は使用できません `Fulfilled by Amazon` 。 |
| 条件 | リストに割り当てられている条件属性に関係なく、リストの条件値を設定するオーバーライド。<br><br>**例** : カタログ内のほとんどの製品が新機能ですが、製品が最新の状態であることを示しています。 一覧を表示し、 [ 条件の上書きを作成 ](./creating-editing-overrides.md#edit-override-single-listing) して、リストの変更条件を定義することができます。<br><br>**注意:** 製品がに設定されている場合は使用できません `Fulfilled by Amazon` 。 |
| 販売業者の注意事項 | _リストの「販売者の注意」セクションを定義する上書き_ 。このフィールドは、製品または上書きに関連する情報を追加するために使用されます。通常、「新規」以外の製品の状態を表すために使用されます。 このフィールドのテキストは、買物客の一覧と共に表示されます。 販売担当者のメモは、条件値がで表示されるリストに追加することはできません `New` 。 <br><br>**例** : 条件にある製品を使用してい `Refurbished` ます。 通常、この条件に含まれる製品にはマニュアルやドキュメントは収録されていませんが、この製品についてはマニュアルが含まれています。 リストを表示して、 [ 販売店のメモオーバーライドを作成し、マニュアルに関する情報が記載されていることを ](./creating-editing-overrides.md#edit-override-single-listing) ユーザーに知らせます。<br><br>**注意** : 製品に条件が定義されている場合は `New` 、販売店の上書きを入力することはできますが、Amazon は製品の販売者のコメントには表示されません `New` 。 |

1つのリストに対して、上書きを作成、編集、または削除することができ [ ](./creating-editing-overrides.md#edit-override-single-listing) ます。 、、 _[!UICONTROL Inactive]__[!UICONTROL Active]_ 、およびタブでは、列内をクリックして、を _[!UICONTROL Ineligible]_**[!UICONTROL Select]**選択でき_[!UICONTROL Action]_ **[!UICONTROL Create Override]** ます。 この _[!UICONTROL Edit Overrides]_アクションは、リストに上書きが適用されており、タブに表示されている場合にのみ使用でき_[!UICONTROL Overrides]_ ます。

また、複数のリストに対して上書きを作成、編集、または削除することもでき [ ](./creating-editing-overrides.md#edit-override-multiple-listings) ます。 、、 _[!UICONTROL Inactive]__[!UICONTROL Active]_ 、およびタブでは、列内をクリックして、を _[!UICONTROL Ineligible]_**[!UICONTROL Select]**選択でき_[!UICONTROL Action]_ **[!UICONTROL Edit Listing Overrides]** ます。

上書きを削除すると、リストの設定とルールによって定義された値を使用してリスティングに通知されます。

オーバーライドを定義するときに、1つのオーバーライドタイプまたはその他の任意の組み合わせを入力することもできます。

[オーバーライドの作成と編集を参照してください ](./creating-editing-overrides.md) 。

>[!NOTE]
>
>リストが作成されている場合は、タブの上のメッセージに一覧の数が表示されます。

![「オーバーライド」タブ](assets/amazon-overrides.png)

Amazon セールスチャンネルのホームページ [ ](./workspace-controls.md) は、表示されるデータをカスタマイズするための一般的なワークスペースコントロールの一部を共有しています。

## デフォルトの列

| 段 | つい |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazon によって製品に割り当てられた SKU (Stock 保存単位) です。製品、オプション、価格、メーカーを識別するために使用されます。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロックです。<br><br>アークは、Amazon 標準の Id 番号を表します。 アークサインとは、アイテムを識別する10文字または数字の一意のブロックです。 本のについては、アークサインの値は ISBN 数と同じですが、他のすべての製品では、アイテムがカタログにアップロードされるときに、新しいアークサインが作成されます。 Amazon の製品詳細ページでは、アイテムに関する詳細な情報が記載されたアイテムを検索することができます。 |
| [!UICONTROL Condition Override] | 上書きによって定義された新しい条件。 このリストに適用された上書きが条件上書きではない場合は、 `Not Selected` この列に表示されます。 |
| [!UICONTROL Product Listing Name] | 製品の名前を指定します。 |
| [!UICONTROL Seller Notes Override] | 上書きによって定義された新しい販売者のノート。 リストに適用された上書きがこのタイプの上書きではない場合、この列は空白になります。 |
| [!UICONTROL Handling Override] | 上書きによって定義された新しい処理時間 (日数)。 リストに適用された上書きが取扱時間をオーバーライドしていない場合、この列は空白になります。 |
| [!UICONTROL List Price Override] | 上書きによって定義された新しいリスト価格。 リストに適用された上書きが価格上書きではない場合は、 `N/A` この列に表示されます。 |
| [!UICONTROL Action] | 特定のリストに適用可能なアクションのリストです。 アクションを適用するには、 _[!UICONTROL Action]_列でをクリック&#x200B;**[!UICONTROL Select]**して、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
