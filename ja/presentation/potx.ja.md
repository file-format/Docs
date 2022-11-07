{
  "date" : "2019-10-11",
  "keywords" :[ "potx ファイル", "potx ファイル形式", "potx ファイルとは", "ファイル", "potx の例", "potx ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Microsoft PowerPoint プレゼンテーション テンプレート",
  "description":"POTX ファイル形式と,POTX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .POTX ファイルとは何ですか?

拡張子が .POTX のファイルは、Microsoft PowerPoint 2007 以降で作成された Microsoft PowerPoint テンプレート プレゼンテーションを表します。この形式は、バイナリ ファイル形式に基づいており、PowerPoint 97-2003 でサポートされている [POT](/presentation/pot/) ファイル形式を置き換えるために作成されました。生成されたファイルを使用して、新しいファイルに適用する必要がある同じレイアウトおよびその他の設定を持つプレゼンテーションを作成できます。これらの設定には、スタイル、背景、カラー パレット、フォント、およびデフォルトを含めることができます。このようなファイルは、正式な使用のためにすぐに使用できるテンプレート ファイルを作成するために生成されます。

## 簡単な歴史 ##

Microsoft が **Office Open XML** の標準に対応するために変更を行うことを決定したのは、2000 年初頭のことでした。この新しい標準に基づくさまざまなタイプのドキュメントは、拡張子に「X」を追加することで識別されました。「X」は XML を表します。 2007 年までに、この新しいファイル形式は Office 2007 の一部となり、Microsoft Office の新しいバージョンでも引き継がれています。新しいファイル タイプには、ファイル サイズが小さい、破損の少ない変更、適切にフォーマットされた画像表現などの利点が追加されています。

## ファイル形式の仕様 ##

オフィス オープン XML ファイル形式で生成されたファイルは、すべての構成ファイル間のリンクを提供する他のファイルと共に XML ファイルのコレクションです。このコレクションは、実際には圧縮されたアーカイブであり、解凍してその内容を表示できます。これを行うには、POTX ファイル拡張子の名前を zip に変更し、内容を観察するために解凍します。

次のセクションでは、これらのそれぞれについて説明します。

### [Content_Types].xml ###

これは、zip を解凍したときにベース レベルで見つかる唯一のファイルです。パッケージ内のパーツのコンテンツ タイプを一覧表示します。パッケージに含まれる XML ファイルへのすべての参照は、この XML ファイルで参照されます。以下は、スライド パーツのコンテンツ タイプです。
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
パッケージに新しいパーツを追加する必要がある場合は、新しいパーツを追加し、.rels ファイル内の関係を更新することで実行できます。このような変更では、Content_Types.xml も更新する必要があることに注意してください。

### \_rels (フォルダ) ###

パッケージ外の他のパーツとリソースの間の関係は、関係パーツによって維持されます。 Relationships フォルダーには、パッケージ レベルの関係を格納する単一の XML ファイルが含まれています。このファイルには、PPTX ファイルの主要部分へのリンクが URI として含まれています。これらの URI は、パッケージに対する各キー パーツの関係のタイプを識別します。これには、ppt/presentation.xml として配置された主要なオフィス ドキュメントとの関係、およびコアおよび拡張プロパティとしての docProps 内の他の部分が含まれます。
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

* [[MS-PPTX] - PPTX ファイル形式](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [オープン オフィス XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

