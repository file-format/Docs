{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - APPX ファイルとは?",
  "description":"APPXファイル形式と,APPXファイルを作成して開くことができるAPIについて学びます。",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## .APPX ファイルとは?

APPX ファイルは、アプリケーションの配布とインストールに使用される配布可能なパッケージ ファイル形式です。 Windows 8 で導入され、Microsoft Windows Store で公開されました。 Windows アプリケーションのインストールに必要なすべてのファイルが含まれています。これらには、メタデータ、ファイル、資格情報が含まれます。より最新のパッケージ ファイル形式は MSIX であり、APPX と比較して現在より一般的に使用されています。

## APPX ファイル形式 - 詳細情報

APPX ファイルは、[ZIP](/compression/zip/) ファイル形式の圧縮ファイルとして保存されます。これにより、パッケージ全体が圧縮されたファイル サイズのアーカイブ ファイルになり、Microsoft Store に簡単にアップロードできます。

## APPX ファイル内のファイルを表示するには?

APPX ファイル内のコンテンツまたはファイルを表示するには、次の手順に従う必要があります。

1. APPX ファイルは圧縮された ZIP ファイルとして保存されるため、ファイルの名前を .zip 拡張子に変更します。
1. 7-Zip、WinZip、WinRAR などの解凍ツールを使用して、APPX ファイルに含まれるファイルを抽出します。

## APPX ファイルの作成方法

APPX ファイルの作成に使用できる方法は 2 つあります。

1. MakeApp.exe の使用 - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) を使用して両方を作成します。アプリ パッケージ (.msix または .appx) およびアプリ パッケージ バンドル ファイル (.msixbundle または .appxbundle)。さらに、アプリ パッケージからファイルを抽出できます。 MakeApp.exe は Windows 10 SDK で利用でき、コマンド プロンプトから使用できます。
1. Microsoft Visual Studio の使用 - 開発者は通常、[APPX ファイルを作成](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) Microsoft Visual Studio を使用します。アプリケーションの開発が完了し、アプリを公開する準備ができたら、Visual Studio 内から公開することで APPX パッケージ ファイルを作成できます。

## 参考文献

* [MakeAppx.exe で MSIX パッケージまたはバンドルを作成する](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Microsoft Visual Studio を使用して APPX ファイルを作成する](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

