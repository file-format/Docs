{
  "date" : "2023-01-11",
  "keywords" :["ac ファイル", "aci ファイルとは", "ファイル", "ac ファイルの開き方", "ac ファイル拡張子","拡張子"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDB ファイルを作成して開くことができる AC ファイル形式と API について学びます。",
  "title" :"AC ファイル形式 - Autoconf スクリプト ファイル",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## .AC オプション番号

AC ファイルは Autoconf スクリプト ファイルです。 **Autoconf** は、ソフトウェア ソース コード パッケージを自動的に構成するシェル スクリプトを生成する M4 マクロの拡張可能なパッケージです。これらのスクリプトは、ユーザーが手動で介入することなく、多くの種類の UNIX ライクなシステムにパッケージを適合させることができます。 Autoconf は、M4 マクロ呼び出しの形式で、パッケージが使用できるオペレーティング システムの機能を一覧表示するテンプレート ファイルから、パッケージの構成スクリプトを作成します。

Autoconf を使用して構成スクリプトを作成するには、GNU M4 が必要です。 Autoconf の構成スクリプトが検出できるように、Autoconf を構成する前に GNU M4 (少なくともバージョン 1.4.6、ただし 1.4.13 以降を推奨) をインストールする必要があります。 Autoconf によって生成される構成スクリプトは自己完結型であるため、ユーザーは Autoconf (または GNU M4) を使用する必要はありません。

## AC ファイルの開き方?

AC は自動構成の略です。これは GNU Autoconf によって生成されるスクリプトであり、パッケージ内の必要な機能をテストすることにより、ソフトウェア ソース コードをさまざまな Posix ライクなシステムに適合させることができます。このスクリプトは AC ファイルと呼ばれます。

## Autotools の主なコンポーネント

GNU autotools (`automake`、`autoconf` など) を理解していると、ebuild を使用する際に役立ちます。

Autotools は、関連するパッケージのコレクションであり、一緒に使用すると、移植可能なソフトウェアの作成に伴う困難の多くが解消されます。これらのツールは、アップストリームが提供するいくつかの比較的単純な入力ファイルと共に、パッケージのビルド システムを作成するために使用されます。

**主要な autotools コンポーネントがどのように組み合わされるかの基本的な概要。**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

簡単なセットアップでは:

- `autoconf` プログラムは `configure.in` または `configure.ac` から構成スクリプトを生成します。
- `automake` プログラムは、Makefile.am から Makefile.in を生成します。
- `configure` スクリプトが実行され、Makefile.in ファイルから 1 つまたは複数の Makefile ファイルが生成されます。
- `make` プログラムは Makefile を使用してプログラムをコンパイルします。

## 参考文献
* [Autoconf ソフトウェア](https://www.gnu.org/software/autoconf/)
* [Autotools の基本](https://devmanual.gentoo.org/general-concepts/autotools/index.html)


