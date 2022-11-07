{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG ファイル形式 - Python 配布ファイル",
  "description":"EGG ファイル形式と,EGG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## .EGG ファイルとは何ですか?

Python の卵としても知られる EGG ファイルは、古い配布形式の Python ディストリビューションです。これは [ZIP](/compression/zip/) 圧縮されたアーカイブで、拡張子は .egg で、Python アプリケーションのソース ファイルとディストリビューションに関するメタ情報が含まれています。 EGG ファイルは、Windows 実行可能 [EXE](/executable/exe/) ファイルに代わるものですが、クロスプラットフォームです。 Python ディストリビューションのこの古い形式は、2010 年初頭に新しい Wheel (WHL) ファイル形式に置き換えられました。

## EGG ファイル形式

EGG ファイルは、圧縮された ZIP アーカイブとして保存されます。つまり、.egg 拡張子を .zip に置き換えると、Corel WinZIP、Microsoft Explorer、RARLAB WinRAR などの標準の解凍ユーティリティで開くことができます。

EGG ファイルは、Python で利用可能な **distutils** パッケージを使用して作成できます。 EGG ファイルを作成して開くことができる別のツールは **SetupTools** です。 **easy_install** を使用して、EGG ファイルをパッケージとしてインストールできます。

`注 - EGG ファイル形式は廃止され、新しいホイール WHL ファイル形式が採用されました。`

## 参照 ＃＃

* [Python EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

