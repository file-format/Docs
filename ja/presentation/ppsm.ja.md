{
  "date" : "2019-10-11",
  "keywords" :[ "ppsm ファイル","ppsm ファイル形式","ppsm ファイルとは","ファイル","ppsm の例","ppsm ファイルの拡張子","拡張子","形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - マクロ有効 PowerPoint プレゼンテーション ファイル",
  "description":"PPSM ファイル形式と,PPSM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .PPSM オプション番号

PPSM 拡張子を持つファイルは、Microsoft PowerPoint 2007 以降で作成されたマクロ有効スライド ショー ファイル形式を表します。もう 1 つの同様のファイル形式は [PPTM](/presentation/pptm/) で、スライド ショーとして実行するのではなく、Microsoft PowerPoint で編集可能な形式で開く点が異なります。スライド ショーとして実行すると、PPSM ファイルはプレゼンテーション スライドをそのままの状態でスライド ショーに表示し、既定では読み取り専用モードになります。 PPSM ファイルは、PowerPoint で開いて Microsoft PowerPoint で編集できます。

## ファイル形式 ##

PPSM ファイル形式は PowerPoint 2007 で導入され、XML と [ZIP](/compression/zip/) の組み合わせを使用してコンテンツを保存する OpenXML ファイル形式に基づいています。オフィス オープン XML ファイル形式で生成されたファイルは、すべての構成ファイル間のリンクを提供する他のファイルと共に XML ファイルのコレクションです。このコレクションは実際には圧縮されたアーカイブであり、解凍してその内容を表示できます。これを行うには、PPSM ファイル拡張子の名前を zip に変更し、内容を観察するために解凍します。

次のセクションでは、これらのそれぞれについて説明します。

### [Content_Types].xml ###

これは、zip を解凍したときにベース レベルで見つかる唯一のファイルです。パッケージ内のパーツのコンテンツ タイプを一覧表示します。パッケージに含まれる XML ファイルへのすべての参照は、この XML ファイルで参照されます。以下は、スライド パーツのコンテンツ タイプです。
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
パッケージに新しいパーツを追加する必要がある場合は、新しいパーツを追加し、.rels ファイル内の関係を更新することで実行できます。このような変更では、Content_Types.xml も更新する必要があることに注意してください。

### \_rels (フォルダ) ###

パッケージ外の他のパーツとリソースの間の関係は、関係パーツによって維持されます。 Relationships フォルダーには、パッケージ レベルの関係を格納する単一の XML ファイルが含まれています。プレゼンテーション ファイルの主要部分へのリンクは、このファイルに URI として含まれています。これらの URI は、パッケージに対する各キー パーツの関係のタイプを識別します。これには、ppt/presentation.xml として配置された主要なオフィス ドキュメントとの関係、およびコアおよび拡張プロパティとしての docProps 内の他の部分が含まれます。
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
1 つまたは複数のリレーションシップのソースであるドキュメントの各部分には、独自のリレーションシップ パーツがあり、そのような各リレーションシップ パーツはパーツの \_rels サブフォルダー内にあり、名前に「.rels」を追加して名前が付けられます。部。メイン コンテンツ パーツ (presentation.xml) には、独自の関係パーツ (presentation.xml.rels) があります。これには、slideMaster1.xml、notesMaster1.xml、handoutMaster1.xml、slide1.xml、presProps.xml、tableStyles.xml、theme1.xml などのコンテンツの他の部分との関係、および外部リンクの URI が含まれています。

#### 明示的な関係 ####

明示的な関係の場合、リソースはの Id 属性を使用して参照されます。<Relationship>エレメント。つまり、ソースの Id は、ターゲットへの明示的な参照を使用して、関係アイテムの Id に直接マップされます。

たとえば、スライドには次のようなハイパーリンクが含まれている場合があります。
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" は、スライドの関係部分 (slide1.xml.rels) 内の次の関係を参照します。
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### 暗黙の関係 ####

暗黙的な関係の場合、` へのそのような直接参照はありません。<Relationship>同上。代わりに、参照が理解されます。

### ppt フォルダ ###

これは、プレゼンテーションの内容に関するすべての詳細を含むメイン フォルダーです。デフォルトでは、次のフォルダーがあります。

* \_rels
* テーマ
* スライド
* スライドレイアウト
* スライドマスターズ

および次の xml ファイル:

* プレゼンテーション.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## 参照 ##

* [OpenXML プレゼンテーション ファイル形式](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [オープン オフィス XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

