{
  "date" : "2021-04-22",
  "keywords": [ "addin file", "visual studio addin file", "extension", "format","addin file visual studio","addin file extension","how to open addin file","addin file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADDIN - Visual Studio アドイン定義ファイル",
  "description":"例と,ADDIN ファイルを作成して開くことができる API を使用して,ADDIN ファイル形式とは何かについて学びます。",
  "linktitle" : "ADDIN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-12"
}

## ADDINファイル形式とは何ですか?

拡張子が .addin のファイルは、アドイン プロジェクト用に Microsoft Visual Studio によって作成されたアドイン定義ファイルです。 Visual Studio IDE のアドイン マネージャーに新しいアドインを登録して、再作成せずに他のプロジェクトで使用できるようにするために使用されます。アドイン自体は小さなソフトウェア アプリケーションであり、主要なプログラムにアクセスすることで、より大きなプログラムの機能を拡張します。アドイン ファイルは、アドイン プロジェクトが作成された場所と同じ場所に [XML](/web/xml/) ファイル形式で保存されます。

## ADDIN ファイル形式 - 詳細情報

ADDIN ファイルは、人間が読める XML ファイル形式でディスクに保存されます。 Notepad、Notepad++、Microsoft Visual Studio IDE などの一般的なテキスト エディターで開くことができます。 Microsoft は Office Add の [XML マニフェスト ファイル](https://docs.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1) を定義しています-アドインがインストールされ、Office ドキュメントやアプリケーションで使用された後にアドインをアクティブ化する方法を記述します。

**参照:** [Visual C# .NET を使用して Office COM アドインを構築する方法](https://docs.microsoft.com/en-us/previous-versions/office/troubleshoot/office-developer /office-com-add-in-using-visual-c)

## 参考文献

* [Office アドイン XML マニフェスト](https://docs.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1)

