{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "ファイル", "拡張子", "ファイル形式", "Excel", "スプレッドシート" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLSX ファイルとは何か,および XLSX ファイルを作成して開くことができる API について学びます。",
  "title" :"XLSX ファイル形式 - XLSX ファイルとは?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLSX ファイルは何ですか?

**XLSX** は、Microsoft Office 2007 のリリースで Microsoft によって導入された Microsoft Excel ドキュメントのよく知られた形式です。[パート 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) の OOXML 標準 ECMA-376 の新しい形式は、多数の XML ファイルを含む zip パッケージです。基になる構造とファイルは、.xlsx ファイルを解凍するだけで調べることができます。

## XLSX ファイル形式の歴史

XLSX ファイル形式は 2007 年に導入され、2000 年に Microsoft によって採用された Open XML 標準を使用します。新しいファイル タイプには、ファイル サイズが小さい、破損の少ない変更、適切にフォーマットされた画像表現という利点が追加されています。 Microsoft が **Office Open XML** の標準に対応するために変更を行うことを決定したのは、2000 年初頭のことでした。 2007 年までに、この新しいファイル形式は Office 2007 の一部となり、Microsoft Office の新しいバージョンでも引き継がれています。

## XLSX ファイル形式の仕様

公式の [XLSX ファイル形式の仕様](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) は、Microsoft からオンラインで入手できます。 XLSX ファイルの内容を確認するには、拡張子を変更して [ZIP](/compression/zip/) ファイルに名前を変更し、解凍してこの Excel ワークブックの構成ファイルを表示します。空白のブックをファイルに展開すると、次の構成ファイルとフォルダーが含まれます。

### [Content_Types].xml ###

これは、zip を解凍したときにベース レベルで見つかる唯一のファイルです。パッケージ内のパーツのコンテンツ タイプを一覧表示します。パッケージに含まれる XML ファイルへのすべての参照は、この XML ファイルで参照されます。

### \_rels (フォルダ) ###

これは、パッケージ レベルのリレーションシップを格納する単一の XML ファイルを含む Relationships フォルダーです。 Xlsx ファイルの主要部分へのリンクは、このファイルに URI として含まれています。これらの URI は、パッケージに対する各キー パーツの関係のタイプを識別します。これには、xl/workbook.xml として配置された主要なオフィス ドキュメントとの関係、およびコアおよび拡張プロパティとしての docProps 内の他の部分が含まれます。

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

## XLSX 形式の例 ##


ワークブックに含まれる Excel ワークシートごとに、1 つの XML ファイルがあります。これらの XML ファイルは、xl/worksheets フォルダーにあります。ワークシートに含まれるすべての情報は、XML ファイル内のさまざまなセクションに編成されています。次の図に示すワークブックのサンプル ワークシートを調べてみましょう。

{{< figure src="../XLSX file format.png" alt="XLSX ファイル形式" >}}

ご覧のとおり、このワークシートにはセル A1 から B2 の内容と画像が含まれています。さらに、セル G13 は現在、ワークシートのアクティブ セルです。次に、xl/worksheets/sheet1.xml ファイルを調べて、この情報が XML ファイルでどのように表現されているかを確認しましょう。この XML ファイルの内容は以下のとおりです。

{{< figure src="../XLSX File Format Details.png" alt="XPS ファイル形式" >}}

1. タブにテーマカラーが適用されています。タグ付きのXMLファイルに記載されています<tabColor>テーマIDに続きます。
1. tabSelected 値が 1 に設定され、これが選択されたシートであることを示します
1. 上の最初の画像でわかるように、ワークシートのセル G13 は、XML ファイルにも記載されているアクティブなセルです。
1. sheetData タブは、ワークシートに含まれるデータを表します。ただし、ワークシートの元の内容がこのセクションのどこにもないことがわかります。これは、テキストが「sharedStrings」XML シートから間接的に参照されているためです。このリンクにより、各テキストが一度だけ保存され、スペースを節約するために再度参照できるようになります。
1. 表示されている画像は、参照 ID「rId2」によって参照されます。

## 助ける

XLSX またはスプレッドシート ファイル形式について共有する必要がありますか? [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet) セクションに調査結果を投稿できます。

## 参考文献

* [[MS-XLSX] - XLSX ファイル形式](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [オープン オフィス XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

