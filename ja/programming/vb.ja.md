{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "ファイル", "拡張子", "ファイル形式", "Visual Basic", "プログラミング ガイド" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic コード ファイル",
  "description":"VB ファイル形式と,VB ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .VB オプション番号

VB ファイルは、Microsoft が .NET アプリケーションの開発用に作成した Visual Basic 言語で作成されたソース コード ファイルです。構文が異なる別の同様の言語は C# で、そのファイルは [.CS](/programming/cs/) ファイル拡張子で保存されます。ファイル形式は、EXE または DLL の形式で最終的な出力ファイルを生成するためにコンパイルされるコードを記述するための低レベルのプログラミング言語を提供します。これらは、Microsoft Visual Studio で作成およびコンパイルできます。無料の IDE である Microsoft Visual Studio Express を使用して、このようなファイルを作成および更新することもできます。 VB 言語で作成された単純な Visual Studio プロジェクト [ソリューション](/programming/sln/) は、1 つ以上のそのようなファイルで構成できます。コンパイルに含めるようにマークされたファイルは、プロジェクトの一部である [CSPROJ](/programming/csproj/) ファイルに一覧表示され、マークされたファイルを使用するようにコンパイラに指示します。

## VB ファイル形式 - 詳細情報

VB ファイルはテキスト ベースのファイル形式で、任意のテキスト エディターで開いて編集できます。ただし、サポートされている IDE で適切な構文の強調表示を使用して開くと、コードが読みやすく、整理しやすくなります。シンプルな VB ファイルには次のものが含まれます。

* 名前空間の宣言 - 特定の名前空間によって定義された特定の機能を参照するため
* 変数宣言 - 特定の実装のクラス レベル変数を宣言する
* メソッド宣言 - 特定の機能のメソッド宣言を宣言する

## VB ファイル形式の例

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



