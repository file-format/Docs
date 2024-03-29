{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "ファイル", "拡張子", "ファイル形式", "Excel Open XML マクロ", "スプレッドシート" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLTM ファイルとは何か,およびそれらを作成して開くことができる API を知るためのファイル形式ガイド。",
  "title" :"XLTM ファイルとは?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLTM オプション番号

XLTM ファイル拡張子は、マクロが有効なテンプレート ファイルとして Microsoft Excel によって生成されるファイルを表します。 XLTM ファイルの構造は [XLTX](/spreadsheet/xltx/) に似ていますが、後者はマクロを使用したテンプレート ファイルの作成をサポートしていません。このようなテンプレート ファイルは、同様の XLSX ファイルの作成を容易にするマクロと共に、レイアウト、書式設定、およびその他の設定を生成および設定するために使用されます。

## 簡単な歴史 ##

Microsoft が **Office Open XML** の標準に対応するために変更を行うことを決定したのは、2000 年初頭のことでした。この新しい標準に基づくさまざまなタイプのドキュメントは、拡張子に「X」を追加することで識別されました。「X」は XML を表します。 2007 年までに、この新しいファイル形式は Office 2007 の一部となり、Microsoft Office の新しいバージョンでも引き継がれています。新しいファイル タイプには、ファイル サイズが小さい、破損の少ない変更、適切にフォーマットされた画像表現などの利点が追加されています。

## XLTM ファイル形式の仕様 ##

XLTM ファイルは Office OpenXML ファイル形式に基づいており、XML と [ZIP](/compression/zip/) を使用してファイル サイズを縮小します。これらは、ファイルをダブルクリックして Microsoft Excel で開くことができます。 XLTM ファイル形式のファイル編成は、ファイルの名前を ZIP に変更し、その内容をディスクに抽出することで確認できます。

### [Content_Types].xml ###

これは、zip を解凍したときにベース レベルで見つかる唯一のファイルです。パッケージ内のパーツのコンテンツ タイプを一覧表示します。パッケージに含まれる XML ファイルへのすべての参照は、この XML ファイルで参照されます。

### \_rels (フォルダー) ###

これは、パッケージ レベルのリレーションシップを格納する単一の XML ファイルを含む Relationships フォルダーです。 Xltx ファイルの主要部分へのリンクは、このファイルに URI として含まれています。これらの URI は、パッケージに対する各キー パーツの関係のタイプを識別します。これには、xl/workbook.xml として配置されたプライマリ オフィス ドキュメントとの関係、およびコアおよび拡張プロパティとしての docProps 内の他の部分が含まれます。

### docProps ###

このフォルダーには、全体的なドキュメント プロパティが含まれています。これらには、コア プロパティのセット、拡張またはアプリケーション固有のプロパティのセット、およびドキュメントのサムネイル プレビューが含まれます。空のワークブックには、このフォルダーに app.xml と core.xml という 2 つのファイルがあります。 core.xml には、作成者、作成日、保存日、変更日などの情報が含まれています。 App.xml には、ファイルの内容に関する情報が含まれています。

### xl (フォルダー) ###

これは、ワークブックの内容に関するすべての詳細を含むメイン フォルダーです。デフォルトでは、次のフォルダーがあります。

* \_rels
* テーマ
* ワークシート

および次の xml ファイル:

* スタイル.xml
* ワークブック.xml

## 参照 ##

* [MS-XLSX ファイル形式](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [オープン オフィス XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

