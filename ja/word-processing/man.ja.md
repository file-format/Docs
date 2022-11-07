{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix マニュアル",
  "description":"FODT ファイル形式と,MAN ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## .MAN オプション番号

拡張子が .man のファイルは、ソフトウェア ドキュメント形式の Unix プログラミング ユーザーズ マニュアルであるマニュアル ページを表します。これは、ドキュメントを表示するために使用される Unix に含まれる `Man` ユーティリティによって使用されます。ソフトウェア ドキュメントには、コマンドを発行してコマンド ターミナルから Man ユーティリティを使用して取得できるセクションとページの情報が含まれています。ドキュメントのソフト コピーとしてコンピュータで利用できるため、印刷したコピーやインターネット接続を必要とせずにアクセスできます。

## Unix マニュアル Man ファイル形式 - 詳細情報

マニュアル ページはプレーン テキスト形式で保存され、表示または編集のために任意のテキスト エディタで作成および開くことができます。 UNIX では、マニュアルのセクション番号とページ番号への参照を含むコマンドを端末から発行することにより、マニュアル ページからの情報を取得します。

### セクションとページ

Unix man は、コマンドの各ページ引数がプログラム、ユーティリティ、または関数の名前を参照するシステムのマニュアルです。セクション情報が指定されている場合、コマンドはその特定のセクション内のページを検索します。ただし、デフォルトの動作では、すべてのセクションでページを検索し、複数のセクションに存在するかどうかに関係なく最初のページを表示します。

### セクション番号

以下は、マニュアルのセクション番号とそれに続くページのタイプに関する情報です。

|セクション番号|ページの種類|
---|---|
|1|実行可能なプログラムまたはシェル コマンド|
|2|システムコール (カーネルが提供する関数)|
|3|ライブラリ呼び出し (プログラム ライブラリ内の関数)|
|4|特殊ファイル (通常は /dev にあります)|
|5|ファイル形式と規則、例えば /etc/passwd|
|6|ゲーム|
|7|その他 (マクロパッケージと規約を含む)、例えば man(7), groff(7)|
|8|システム管理コマンド (通常は root のみ)|
|9|カーネルルーチン [非標準]|

## 例 - MAN ページの読み方

以下は、Man コマンドを使用して MkDir コマンドに関する情報を取得する方法の例です。

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## 参考文献

* [OpenDocument 技術仕様 - ウィキペディアによる](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux マニュアル ページ](https://man7.org/linux/man-pages/man1/man.1.html)

