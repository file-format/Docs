{
  "date" : "2021-07-23",
  "keywords" :["PL","ファイル","拡張子","フォーマット","Perl","Perl言語","PLファイル","プログラミング"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"PL ファイル形式と,PL ファイルを作成して開くことができる API について学びます。",
  "title" :"PL ファイル - Perl スクリプト ファイル形式",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## .PL ファイルとは何ですか?

拡張子が .pl のファイルは、スクリプト言語である Perl スクリプト ファイルです。これらは、Perl Interpreter ソフトウェアを使用してコンパイルおよび実行されます。 PL スクリプト ファイルには、コード行、変数、およびコメントが含まれます。スクリプト言語は比較的難しい
[PHP](/programming/php/) などの他のプログラミング ファイル形式を理解します。 PL ファイルを作成でき、Windows、macOS、および Linux と互換性があります。

## Perl スクリプト言語の歴史

この言語は 1987 年に初めて使用されたため、これらのファイルはその年に作成されました。 1989 年に Perl 2 がリリースされました。その後、バージョン 5.35 まで更新・修正されており、次期バージョンは来年のリリースを目指しています。

すべての更新で、言語とファイルの機能、パフォーマンス、外観に関するツールが追加されています。ここ数年、バージョンに関して多くの改訂が行われてきました。もともとは基本的なスクリプト言語でしたが、現在では他の多くのモジュールも含まれています。もともとはとても単純な言語でしたが、この言語のスクリプトはコンパクトなため、理解するのが非常に困難でした。

## Perl ファイル形式拡張子の仕様

これらのプログラミング ファイルにはいくつかのプロパティまたは仕様があり、その一部は次のとおりです。

* これらのファイルに含まれるコードはプレーン テキスト形式であり、スクリプト開発に使用されます
* サーバーのスクリプト作成、テキストの解析、およびサーバー管理は、この言語のスクリプトがカバーする主な側面です。
* この言語に関連する多くの一般的なプログラムは、Active 状態 Active Perl および Bare Bones BBEdit (Mac OS と互換性あり) です。
* この言語は高級言語と見なされます
* Win32 の場合、ユーザーは言語のネイティブ バイナリ ディストリビューションをインストールする必要がある場合があります。
* さまざまな Windows リソース キットで実行できるようにするには、いくつかのスクリプト ツールが必要です。
* Visual Studio .NET は、プログラミング言語の開発で有名なフレームワークです。 Visual Perl として知られる Active State ツールは、Perl を Visual Studio に追加するために使用されます。
※ファイル内のソースコードの1行目には使用しているインタープリターの情報が記述されています。 PL ファイルは通常 **#!/usr/bin/perl** 行で始まり、コンピューターにインストールされている Perl インタープリターを使用してこのスクリプトを実行するようコンピューターに指示します。


## PL スクリプトの例

```
#!/usr/bin/perl
print "Hello, world\n";
```

これは印刷されます

```
Hello, World
```

### 一行コメント ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### 複数行コメント ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### 変数の割り当て ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### スカラー変数の代入 ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### 単純なスカラー演算 ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## 参照 ##

- [Python (プログラミング言語) - ウィキペディア](https://en.wikipedia.org/wiki/Python_(programming_language))

