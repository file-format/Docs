{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - MSIX ファイルとは?",
  "description":"MSIX ファイルと,MSIX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## .MSIX オプション番号

MSIX ファイルは、Windows 10 でアプリケーションを作成および配布するために使用される Windows アプリ パッケージ形式です。この新しいファイル形式に。 Win32、WPF、および Windows フォーム アプリの展開に使用できます。 MSIX ファイルは信頼性が高く、ネットワークとディスク領域の最適化をターゲットにしています。開発者はこれらを使用して、Microsoft ストア (以前は Windows ストアと呼ばれていました) を通じてプログラムをエンド ユーザーに配布します。

## MSIX ファイル形式 - 詳細情報

MSIX ファイルは [ZIP](/compression/zip/) 圧縮されており、すべてのファイルがパッケージ ファイル内に含まれています。アプリ関連のファイルに加えて、MSIX ファイルには、アプリのインストールに関連する情報を含む [.xml](/web/xml/) 構成ファイルが含まれています。

## MSIX パッケージの内容

MSIX パッケージは、次のファイルで構成されます。

* `AppxBlockMap.xml` - パッケージ ブロック マップ ファイルと呼ばれ、パッケージに格納されている各データ ブロックのインデックスと暗号ハッシュを含むアプリ ファイルのリストを含む XML ドキュメントです。
* `AppxManifest.xml` - MSIX アプリの展開、表示、および更新に必要な情報を含む XML ドキュメント。この情報には、パッケージ ID、パッケージの依存関係、必要な機能、視覚要素、および拡張ポイントが含まれます。
* `AppxSignature.p7x` - パッケージが署名されたときに生成されるファイル。すべての MSIX パッケージは、インストール前に署名する必要があります。 AppxBlockmap.xml を使用すると、プラットフォームはパッケージをインストールして検証できます。

## 参考文献

* [MSIX の概要](https://docs.microsoft.com/en-us/windows/msix/overview)
* [Microsoft Visual Studio を使用して APPX ファイルを作成する](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

