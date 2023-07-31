{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ADE ファイル形式と,ADE ファイルを作成して開くことができる API について学びます。",
  "title" :"ADE - アクセス プロジェクト拡張ファイル",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## .ADE ファイルとは何ですか?

拡張子が .ade のファイルは、Microsoft Access ADP プロジェクト ファイルに含まれる情報のコンパイル済み出力を含む Microsoft Access プロジェクト ファイルです。 Visual Basic for Applications (VBA) 以外の Access プロジェクト ファイルの情報は、ADE ファイルでコンパイルされた形式で利用できます。データはこれらのファイルに圧縮形式で格納され、ファイル サイズを縮小して Access のパフォーマンスを向上させます。 ADE は Access プロジェクト ファイルのコンパイル済み出力であるため、プロジェクトの一部である VBA ソース コードは、出力に含めないようにすることで保護されたままになります。 ADE ファイルは、Microsoft Access 365 で開くことができます。

## ADE ファイル形式 - 詳細情報

ADE は、バイナリ ファイルとしてディスクに格納されるコンパイル済みの Access データベース ファイルです。これらのファイルの内部ファイル構造は不明です。

ADE ファイルは、これらのファイルの作成に使用された Microsoft Access のバージョンに基づいて、開く際に問題を引き起こす可能性があります。 Microsoft Access 2010 の 64 ビット バージョンを使用し、MDE、[ACCDE](/database/accde/)、または ADE ファイルとしてコンパイルされている Access データベースは、Microsoft Access 2021 Service Pack 1 (SP1) で再コンパイルする必要があります。 Access 2010 SP1 で正しく動作します。この問題は、Access 2010 SP1 が新しいバージョンの VBE7.dll ファイル (バージョン 7.00.1619) を使用するために発生します。

## 参考文献

* [Access ADE ファイルの問題](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [使用する Access ファイル形式](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

