{
  "date" : "2021-09-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IPR ファイル形式 - IntelliJ IDEA プロジェクト ファイル",
  "description":"IPR ファイル形式と,IPR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "IPR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## .IPR ファイルとは何ですか?

IPR ファイルは、Java IDE **IntelliJ IDEA** で作成されたプロジェクト ファイルです。ディレクトリ構造、ソース コード ファイル、プロジェクトに含まれるライブラリ、コンパイラの設定など、プロジェクトの設定に関するすべての情報が IPR ファイルに格納されます。 IntelliJ IDEA 内からプロジェクトを開くと、IDE は IPR ファイルの情報を読み取り、対応するファイルと設定を読み込みます。 IPR ファイルは、設定ディレクトリとしてすべての情報を含む .IDEA ファイルに置き換えられました。

## IPR ファイル形式

IPR ファイルは、人間が判読できる普遍的に理解できる [XML](/web/xml/) ファイル形式で保存されます。プロジェクト関連のコンテンツを表示するために読み込まれるタグに、すべてのプロジェクト関連情報が含まれています。

IPR ファイルは XML ファイル形式で保存されるため、メモ帳、メモ帳++、Atom、Apple TextEdit などの任意のテキスト エディターで開くことができます。

## 参照 ＃＃

* [管理プロジェクトの作成 - IntelliJ IDEA](https://www.jetbrains.com/help/idea/creating-and-managing-projects.html)

