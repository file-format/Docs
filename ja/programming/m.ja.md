{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab ソース コード ファイル",
  "description":"Matlab .m ソース コード ファイルと,MF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab ソース コード ファイル

## M (Matlab) ファイルとは?

拡張子が .m のファイルは、解析、アルゴリズム開発、およびシミュレーション モデリングに使用されるプログラミングおよび数値計算プラットフォームである Matlab で使用されるソース コード ファイルです。他のプログラミング ファイル形式と同様に、M ファイルには、Matlab コマンドを実行してグラフのプロット、シミュレーションの実行、およびその他の数学演算を実行するソース コードが含まれています。 1 つの Matlab シミュレーションは、スクリプト、クラス、関数、または宣言でアプリケーションを分類できる複数の .m ファイルにまたがることができます。 Matlab M ファイルは、任意のテキスト エディターで開くことができます。

## Matlab M ファイル形式 - 詳細情報

Matlab .m ファイルは、Matlab プログラミング言語のプログラミング コードを含むテキスト ファイルです。これらは任意のテキスト エディターで開いて編集し、Matlab ソフトウェアで実行するために保存することができます。 Matlab 自体には、コード、出力、および書式設定されたテキストの組み合わせであるスクリプトを作成するために使用されるライブ エディターが含まれています。

### Matlab 関数ファイル

他のプログラミング言語と同様に、特定のタスクのみを実行する関数の定義のみを含む .m ファイルを作成できます。このようなファイルも .m 拡張子で保存され、その機能に関連する機能のみを実装します。

### .M ファイルの例

以下は、高さ h から物体を落下させるのにかかる時間を計算する Matlab 関数ファイルの例です。

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

この関数を Matlab エディターまたは別の .m ファイルから呼び出すには、次のコードを使用できます。
```C++
TimeToGround(100)
```

## 参考文献

* [Matlab - 対応ファイル形式](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Matlab の使用](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C 実装ファイル

## M (Objective-C) ファイルとは何ですか?

Mファイルは、OS XおよびiOS用のソフトウェアアプリケーションを作成するために使用されるプログラミング言語であるObjective-C言語で書かれたクラスのソースコードを含む実装ファイルとも呼ばれます。 Objective-C は、Apple の主要な API である Cocoa および Cocoa Touch でこれらのプラットフォームに使用される主要なプログラミング言語です。この言語で開発された単一のソフトウェア アプリケーションには、プログラム クラスの実装を含む複数の .m ファイルが含まれる場合があります。これらは、Apple XCode、jEdit、およびその他の一般的なテキスト エディターを使用して開くことができます。

## Objective-C M ファイル形式 - 詳細情報

M ファイルは、Objective-C のプログラミング構文を使用してプレーン テキスト形式で書き込まれます。クラスのすべてのメソッドは、これらの実装ファイルで必要なすべてのコードで定義する必要があります。これらの実装 M ファイルは、要件に従って 1 つ以上の .h ヘッダー ファイルをインポートできます。 import ステートメントは、この実装ファイルに属するヘッダー ファイルの場所をコンパイラに伝えます。 import ステートメントは次のように記述します。

```C++
#import "network.h"
```

各 M ファイルの実装は、`@implementation` ディレクティブで始まり、その後に実装クラス ファイル名が続きます。この後に、ヘッダー ファイルで宣言されているすべてのメソッドの実装が続きます。

### M ファイル形式の例

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## 参考文献
※【Objective Cについて】(https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C ガイド](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

