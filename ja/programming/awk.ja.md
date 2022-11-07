{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK ファイル形式 - AWK スクリプト ファイル",
  "description":"AWK ファイル形式と,AWK ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## .AWK オプション番号

AWK ファイルは、Unix および Linux オペレーティング システムにバンドルされているテキスト処理アプリケーション **AWK** 用に作成されたスクリプト ファイルです。これには、テキストの照合、置換、印刷など、テキストまたはファイルの内容に対してアクションを実行するための論理的な命令が含まれています。これは、入力ファイルからレポートと書式設定されたテキストを生成するのに役立ちます。 awk ユーティリティは通常、ほとんどの linux/unix ディストリビューションで /usr/bin/awk にあります。

## AWK スクリプトの作成方法

AWK ファイルは、Linux/Unix OS の任意のテキスト エディターで作成または開くことができます。新しい AWK スクリプト ファイルは次のように作成できます。

```
$ vi script.awk
```

これにより、テキスト エディターで AWK ファイルが開きます。次のように、テキスト エディターにいくつかのステートメントを入力します。

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
このテキスト コンテンツの 1 行目は、次のように説明されています。

* \#! – 「シェバン」と呼ばれ、スクリプト内の命令のインタープリターを指定します
* /usr/bin/awk – インタープリターです
* -f – インタプリタ オプション、プログラム ファイルの読み取りに使用

## AWK スクリプトを実行するには?

ファイルを保存し、次のコマンドを発行してスクリプトを実行可能にします。
```
$ chmod +x script.awk
```

その後、スクリプトは次のように実行できます。

```
$ ./script.awk
```

その結果、次の出力が得られます。

```
Writing my first Awk executable script!
```

## 参照 ＃＃

* [Awk プログラミング言語を使用してスクリプトを作成する](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

