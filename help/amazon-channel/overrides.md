---
title: 上書き
description: AmazonSales Channelには、Amazonリストで上書きを適用する方法を特定し、管理するのに役立つ「上書き」タブが用意されています。
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# 上書き

_[!UICONTROL Overrides]_タブには、上書きを適用したAmazonのリストが表示されます。 上書きとは、リスト固有の設定で、定義済みの値をリストに設定するのに使用できます。 リストに適用される上書きは、その他の定義済みのリスト設定や、リストに適用されるルールに関係なく、リストの設定を定義します。 リストに上書きを適用すると、リストが「_[!UICONTROL Overrides]_」タブに表示されます。 上書きで定義された値が、リストの適切な列に表示されます。 次の4種類のオーバーライドを適用できます。価格、取り扱い時間、条件、販売者向けメモ。

## 上書きのタイプ

| タイプ | 説明 |
|---|---|
| 価格 | リストの価格を設定する上書き。リストの他のすべての価格設定は無視します。 <br><br>**例**:カタログの特定のカテゴリのすべての製品に適用される20%割引価格ルールを定義しました。市場に出回りやすく需要が高い商品があるので、商品がそのカテゴリにあっても、その商品に対して割引価格を適用したくない。 リストを選択し、[価格の上書き](./creating-editing-overrides.md#edit-override-single-listing)を作成して、価格の上書きで価格を定義できます。 |
| 処理時間 | リストの処理時間を設定するオーバーライドで、リスト設定で設定されたデフォルトの処理時間は無視します。<br><br>**例**:リストの既定の処理時間は2日に設定されています。あなたは壊れやすい製品を持っていて、特別な荷物を出荷するために余分な日を必要とします。 リストを表示し、[処理時間の上書き](./creating-editing-overrides.md#edit-override-single-listing)を作成して、3日で処理時間を定義できます。<br><br>**注意：** は、に設定された製品では使用できま `Fulfilled by Amazon`せん。 |
| 条件 | リストに割り当てられた条件属性に関係なく、リストの条件値を設定する上書き。<br><br>**例**:カタログ内の製品のほとんどはNew Conditionですが、Refurshed Conditionの製品があります。リストを表示し、[条件の上書き](./creating-editing-overrides.md#edit-override-single-listing)を作成して、リストの更新済み条件を定義できます。<br><br>**注意：** は、に設定された製品では使用できま `Fulfilled by Amazon`せん。 |
| 販売者向けメモ | リストの&#x200B;_販売者のメモ_&#x200B;セクションを定義するオーバーライド。 このフィールドは、製品に関する追加情報を追加したり、適用された上書きを追加したりする場合に使用できます。通常は、「新規」でない製品の条件を示すために使用されます。 このフィールドのテキストが表示され、買い物客のリストが表示されます。 条件値が`New`のリストに売り手のメモを追加することはできません。 <br><br>**例**:あなたは条件の製品を持って `Refurbished` いる。通常、この条件の製品にはマニュアルや文書は含まれませんが、マニュアルを含むこの製品の別のサプライヤが存在します。 リストを表示し、[販売者向けメモのオーバーライド](./creating-editing-overrides.md#edit-override-single-listing)を作成し、マニュアルに関するこのリストに固有のテキストメモを追加して、買い物客がそのメモが含まれていることを把握できるようにします。<br><br>**注意**:製品にという条件が定義されている場合は、販売者ノートの上書きを入力できま `New`すが、Amazonではその製品の販売者ノートは表示され `New` ません。 |

[単一のリスト](./creating-editing-overrides.md#edit-override-single-listing)に対する上書きを作成、編集、または削除できます。 「_[!UICONTROL Inactive]_」、「_[!UICONTROL Active]_」、「_[!UICONTROL Ineligible]_」の各タブで、「_[!UICONTROL Action]_」列の「**[!UICONTROL Select]**」をクリックし、「**[!UICONTROL Create Override]**」を選択します。 _[!UICONTROL Edit Overrides]_アクションは、リストに上書きが適用され、「_[!UICONTROL Overrides]_」タブに表示される場合にのみ使用できます。

[複数のリスト](./creating-editing-overrides.md#edit-override-multiple-listings)に対する上書きの作成、編集、削除もできます。 「_[!UICONTROL Inactive]_」、「_[!UICONTROL Active]_」、「_[!UICONTROL Ineligible]_」の各タブで、「_[!UICONTROL Action]_」列の「**[!UICONTROL Select]**」をクリックし、「**[!UICONTROL Edit Listing Overrides]**」を選択します。

上書きを削除すると、リストの設定とルールで定義された値を使用するようにリストに指示します。

オーバーライドを定義する際に、1つのタイプのオーバーライドを入力するか、任意のタイプの組み合わせを入力するかを選択することもできます。

[上書きの作成と編集](./creating-editing-overrides.md)を参照してください。

>[!NOTE]
>
>リストが処理中の場合は、タブの上にあるメッセージにリスト数が表示されます。

![「上書き」タブ](assets/amazon-overrides.png)

Amazonの販売チャネルのホームページは、表示されるデータをカスタマイズできる、一般的な[workspaceコントロール](./workspace-controls.md)を共有します。

## デフォルトの列

| 列 | 説明 |
|---|---|
| [!UICONTROL Amazon Seller SKU] | Amazonが製品に割り当てたSKU(Stock Keeping Unit)。製品、オプション、価格および製造元を識別します。 |
| [!UICONTROL ASIN] | アイテムを識別する10文字または数字の一意のブロック。<br><br>ASINは、Amazon Standard Identification Numberの略です。ASINは、項目を識別する10文字または数字の一意のブロックです。 本の場合、ASINはISBN番号と同じですが、他のすべての製品の場合は、品目がカタログにアップロードされると新しいASINが作成されます。 ASINは、Amazonの製品の詳細ページで、品目に関する詳細と共に検索できます。 |
| [!UICONTROL Condition Override] | 上書きで定義された新しい条件。 リストに適用された上書きが条件の上書きでない場合は、この列に`Not Selected`が表示されます。 |
| [!UICONTROL Product Listing Name] | 製品の名前。 |
| [!UICONTROL Seller Notes Override] | 上書きで定義された新しい販売者のメモ。 リストに適用された上書きがこのタイプの上書きでない場合、この列は空白になります。 |
| [!UICONTROL Handling Override] | 上書きで定義された新しい処理時間（日数）。 リストに適用された上書きが処理時間の上書きでない場合、この列は空白になります。 |
| [!UICONTROL List Price Override] | 上書きで定義された新しい上場価格。 リストに適用された上書きが価格の上書きでない場合は、この列に`N/A`が表示されます。 |
| [!UICONTROL Action] | 特定のリストに適用できるアクションのリスト。 アクションを適用するには、「_[!UICONTROL Action]_」列で「**[!UICONTROL Select]**」をクリックし、次のいずれかのオプションを選択します。<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
