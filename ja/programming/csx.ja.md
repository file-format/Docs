{
"日付": "2023-05-15",
  "keywords": [
"csx ファイル",
"csx ファイルとは何ですか",
"csx ファイルには何が含まれていますか",
"csx ファイルの形式は何ですか",
"ファイル",
"csx ファイル拡張子",
"拡大"
],
  "author": {
"display_name": "シャキール・ファイズ"
},
"ドラフト": "偽",
"toc": true,
"title": "CSX ファイル形式 - Visual C# スクリプト",
  "description":"CSX 形式と,CSX ファイルを作成して開くことができる API について学びます。",
"リンクタイトル": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent": "プログラミング"
}
},
"lastmod": "2023-05-15"
}

## .CSX ファイルとは何ですか?

Visual C# Script (CSX とも呼ばれる) は、Microsoft の .NET エコシステムの Roslyn スクリプト エンジンで使用されるファイル形式です。 CSX ファイルには、別のコンパイル手順を必要とせずに直接実行できる C# コードが含まれています。

CSX 形式は Microsoft エコシステムに固有のものであり、一般的なプログラミングで広く使用されているファイル形式ではありません。 CSX ファイルは、迅速なプロトタイピングまたはスクリプト機能が必要なシナリオでよく使用されます。これらを使用すると、本格的なコンパイル済みアプリケーションを作成する場合と比較して、より軽量な方法で C# プログラムを作成して実行できます。

CSX ファイルを実行するには、C# コードを実行するための対話型環境を提供する .NET Interactive Notebooks などのツールを使用できます。 C# 拡張機能を備えた Visual Studio Code と .NET Core SDK を使用して、CSX ファイルを操作することもできます。

## CSXファイルには何が含まれていますか?

CSX (C# スクリプト) ファイルには、直接実行できる C# コードが含まれています。変数宣言、関数、クラス、その他のプログラミング構造など、有効な C# コードを含めることができます。

CSX ファイルに含まれる内容の例を次に示します。

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX ファイルには、コードの機能をサポートするインポート ステートメント、外部ライブラリ参照、その他の C# 言語機能を含めることもできます。コードはコンパイルを必要とせずにオンザフライで解釈および実行されるため、スクリプト作成や迅速なプロトタイピング タスクに適しています。

## CSXファイルの形式は何ですか?

CSX (C# スクリプト) 形式は、単純なテキストベースの形式に従います。通常、通常の C# ソース コード ファイル (.cs) と区別するために、ファイル拡張子 .csx が付いています。

CSX ファイルは、C# 構文の強調表示をサポートするテキスト エディターまたは統合開発環境 (IDE) を使用して編集できます。 CSX ファイルの準備ができたら、.NET Interactive Notebooks、.NET Core コマンド ライン インターフェイス (CLI)、または C# スクリプト サポートを備えた IDE などのツールを使用して実行できます。

## 参考文献
* [Visual Studio Code を使用した C# プログラミング](https://code.visualstudio.com/docs/langages/csharp)

