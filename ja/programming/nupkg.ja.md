{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG ファイル - NuGet パッケージ ファイル",
  "description":"NUPKG ファイル形式と,NUPKG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## NUPKG ファイルとは?

NUPKG ファイルは、.NET プロジェクトで使用されるパッケージを作成するために NuGet ソフトウェアで使用されるソース コードを含むパッケージ ファイルです。 NuGet パッケージ マネージャー コンポーネントは、オンライン パッケージ ホスティング リポジトリからパッケージを取得するために、Microsoft Visual Studio の一部としてインストールされます。 NUPKG ファイルは、開発者が開発パッケージを手動でダウンロードしてインストールする代わりに、NuGet パッケージ マネージャーを使用して [Nuget.org](https://nuget.org) から最新のパッケージを取得するのに役立ちます。 NUPKG ファイルは NUSPEC ファイルから構築され、フェッチされると、ユーザー システムにパッケージをインストールします。

## NUPKG ファイル形式

NUPKG ファイルは、パッケージ化されたライブラリを含む [ZIP](/compression/zip/) アーカイブです。ダウンロードすると、名前を .zip に変更し、WinZIP、7-Zip、Apple Archive Utility などの標準の zip ユーティリティで抽出できます。

## 参照

* [Nuget.org](https://nuget.org)
* [クイック スタート: Visual Studio でパッケージをインストールして使用する (Windows のみ)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [Nuget パッケージを作成して公開する方法](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

