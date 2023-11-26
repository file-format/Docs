
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4番目のファイル - 4番目の言語ファイル形式",
  "description":"4th ファイルを作成して開くことができる例と API を使用して,.4th ファイル形式とは何かについて学びます。",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## 4番目のファイルとは何ですか?

.4th ファイル拡張子を持つファイルは、**Forth プログラミング言語** 用に作成されたプログラミング ファイルです。これには、Forth プログラミング言語で書かれたプログラムのソース コードが含まれており、プログラムの実行時に出力が生成されます。これは、[C](/ja/programming/c/) および [C++](/ja/programming/cpp/) ソース ファイルに似た別のプログラミング言語ファイルです。

## 4 番目のファイル形式 - 詳細情報


### 4 番目のプログラミング言語のコード例

以下は、指定された数値の階乗を計算する Forth で書かれた簡単なプログラムの例です。

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

この例では、階乗ワードは単一の引数 n を受け取り、その階乗を返します。 dup ワードはスタックの一番上の値を複製し、drop はスタックの一番上の値を破棄し、* はスタックの一番上の 2 つの値を乗算します。 if および begin/until 構造は、プログラムのフローを制御します。

このプログラムを使用するには、Forth インタプリタに定義を入力し、階乗を求めたい数値を含む階乗ワードを呼び出します。

```
10 factorial .
```
これにより、10 の階乗である 3628800 が出力されます。

## 参考文献

* [Forth プログラミング言語](https://en.wikipedia.org/wiki/Forth_(プログラミング_言語))

