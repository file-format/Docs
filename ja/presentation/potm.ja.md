{
  "date" : "2019-10-11",
  "keywords" :[ "potm ファイル", "potm ファイル形式", "potm ファイルとは", "ファイル", "potm の例", "potm ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM - マクロを含む Microsoft PowerPoint テンプレート ファイル",
  "description":"POTM ファイル形式と,POTM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .POTM オプション番号

POTM 拡張子を持つファイルは、マクロをサポートする Microsoft PowerPoint テンプレート ファイルです。 POTM ファイルは PowerPoint 2007 以降で作成され、さらにプレゼンテーション ファイルを作成するために使用できるデフォルト設定が含まれています。これらの設定には、スタイル、背景、カラー パレット、フォント、デフォルト、および特定のタスクを実行するためのカスタム関数で構成されるマクロを含めることができます。また、Open XML ドキュメント サポートがインストールされている以前のバージョンの PowerPoint で開くこともできます。 POTM ファイルは、Microsoft PowerPoint で開いて、他の PowerPoint ファイルと同様に編集できます。

## ファイル形式の仕様 ##

POTM ファイル形式は Office OpenXML 仕様に基づいており、圧縮された [ZIP](/compression/zip/) アーカイブである [PPTX](/presentation/pptx/) ファイルの構造に似ています。

POTM ファイル内のスライドには、ページ内で自由に配置できるテキスト、写真、ビデオ、グラフィックス、およびその他のオブジェクトが含まれている場合があります。次に、POTM テンプレートを使用して、ファイルのすべての書式設定オプションを継承する複数のファイルを作成します。したがって、POTM ファイルに含まれるマクロは、他のプレゼンテーションにも継承されます。それらをドキュメントの構造に埋め込むには、MS Office に含まれるマクロ レコーダーを使用します。マクロ レコーダーは、コマンド シーケンスを保存し、マクロを作成してそれらを自動的に複製します。

オフィス オープン XML ファイル形式で生成されたファイルは、すべての構成ファイル間のリンクを提供する他のファイルと共に XML ファイルのコレクションです。このコレクションは実際には圧縮されたアーカイブであり、解凍してその内容を表示できます。これを行うには、POTM ファイル拡張子の名前を zip に変更し、内容を観察するために解凍します。

次のセクションでは、これらのそれぞれについて説明します。

### [Content_Types].xml ###

これは、zip を解凍したときにベース レベルで見つかる唯一のファイルです。パッケージ内のパーツのコンテンツ タイプを一覧表示します。パッケージに含まれる XML ファイルへのすべての参照は、この XML ファイルで参照されます。以下は、スライド パーツのコンテンツ タイプです。
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
パッケージに新しいパーツを追加する必要がある場合は、新しいパーツを追加し、.rels ファイル内の関係を更新することで実行できます。このような変更では、Content_Types.xml も更新する必要があることに注意してください。

### \_rels (フォルダ) ###

パッケージ外の他のパーツとリソース間の関係は、関係パーツによって維持されます。 Relationships フォルダーには、パッケージ レベルの関係を格納する単一の XML ファイルが含まれています。プレゼンテーション ファイルの主要部分へのリンクは、このファイルに URI として含まれています。これらの URI は、パッケージに対する各キー パーツの関係のタイプを識別します。これには、ppt/presentation.xml として配置された主要なオフィス ドキュメントとの関係、およびコアおよび拡張プロパティとしての docProps 内の他の部分が含まれます。
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

