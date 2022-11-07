{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc","ファイル","拡張子","ファイル形式","mrc 実装","プログラミング ガイド","mrc の例","mIRC","mIRC スクリプト言語","INI のファイル"," mSL スクリプト言語", "mIRC 言語", "mIRC スクリプト", "スクリプト言語" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC スクリプト言語ファイル",
  "description":"MRC ファイル形式と,MRC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## .MRC オプション番号

mIRC は、Windows オペレーティング システムに IRC クライアント (インターネット リレー チャット) として組み込まれているスクリプト言語です。これは、個人およびチャネルでの使用をスパムから保護する機能を提供します。ユーザーの互換性を向上させるために、この mIRC スクリプト言語ではダイアログ ウィンドウを作成できます。ほとんどがプレーンテキスト形式のスクリプトを含むファイルは、MRC の拡張子で、または [INI](/system/ini/) のファイルとして保存されます。この言語の関数は、コマンドおよび識別子 (値を返す場合) として知られています。

mIRC 言語では、一度に複数のスクリプト ファイルをロードできます。一方、一方のファイルが同時にロードされると、もう一方のファイルが使用されなくなる可能性があります。コマンドは保存され、IRC に自動的に存在できます。この言語で使用されるコマンドとエイリアスには、どの文字の優先順位も含まれていません。

mIRC は、ボットにチャネルを自動的に管理させるために広く使用されていますが、mSL スクリプト言語でも変更できます。マクロ、音楽再生機能、小さなマクロと関数、基本的なゲーム、小さなアプリケーションの操作など、多くの新機能を導入できます。


## 簡単な歴史 ##

このスクリプト言語は、1995 年に Khaled Adam Bey によって最初に開発されました。スクリプト言語の設計も Khalid によって作成されました。この言語のターゲットは、イベント駆動型プログラミングでした。当初、このプログラミング言語のファイルに使用されたファイル拡張子は .mrc および .ini でした。また、プロプライエタリ ソフトウェアのライセンスの下で開発されました。

## 技術仕様 ##

一部の関数は、この mIRC 言語を介してカスタム スクリプト化されており、エイリアスとして知られています。これらのエイリアスが値を返す場合、カスタム識別子と呼ばれます。この mIRC 言語に含まれるすべての変数は、動的に型付けされます。シジルは mIRC スクリプトによって使用されます。このスクリプト言語のもう 1 つの機能は、ポップアップです。ユーザーはポップアップを選択するだけで呼び出すことができます。リモートは、特定のイベントに指定されています。相対イベントが発生すると、リモートが呼び出されます。

スペースで区切られたトークンは、この言語のコードの各行を分割するために使用されます。 MDX (mIRC Dialog Extension) や DCX (Dialog Control Extension) など、mIRC ファイルに使用されるその他の一般的な拡張子がいくつかあります。これらは両方とも対話拡張機能であり、比較的人気があります。言語構造は、このスクリプト言語の命名法によって参照されます。 mIRC 言語には、ローカル変数とグローバル変数、バイナリ変数、ハッシュ テーブル、ファイル処理など、スクリプト言語のさまざまな側面が含まれます。


## MRC ファイル形式の例 ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## 参照 ＃＃

* [MIRC - ウィキペディアによる](https://en.wikipedia.org/wiki/MIRC_scripting_language)



