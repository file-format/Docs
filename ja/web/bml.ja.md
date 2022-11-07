{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML ファイル形式 - Bean マークアップ言語ファイル",
  "description":"BML ファイル形式と,BML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## .BML ファイルとは何ですか?

拡張子が .bml のファイルは、Java アプリをサポートするための Java クラスを格納する Bean マークアップ言語ファイルです。これにより、Java オブジェクトおよびメソッドへのアクセスが可能になり、Java クラスを使用して新しい機能を作成する必要がなくなります。有用なタスクを実行するためにコンポーネントを相互に接続する方法を指定します。 BML は、構造とコンポーネントの関係を記述するために IBM alphaWorks によって開発されました。 BML ファイルは、Web ブラウザ、Microsoft Notepad、Notepad++ などの任意のテキスト エディタを使用して開いて表示できます。

## BML ファイル形式

IBM alphaworks Web サイトでは、BML の 2 つの実装が提供されています。最初の実装は、目的の Bean 階層を生成するために BML スクリプトを「再生」するインタープリターです。 2 つ目の実装は、BML スクリプトをリフレクションのない Java コードにコンパイルするコンパイラです。これは、この特定の目的のために設計された言語を使用してアプリケーションのコンポーネント間の構造をキャプチャできるという意味で有利であり、それを「通常の」Java コードにコンパイルする機能が追加されています。

## BML タグ

以下は、BML 言語で使用されるいくつかのタグの説明です。

### の<bean>鬼ごっこ：

の<bean>要素は、新しい Bean を作成するか、名前で Bean を検索するために使用されます。の<bean>タグの形式は次のとおりです。
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
タグ内の「id」は、JavaBean のオブジェクト レジストリに関連付けられています。

###<string>鬼ごっこ

文字列タグを使用するには、次の 2 つの方法があります。

1. 空でない文字列を作成するには:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. 空の文字列を作成するには:

```
<string/>
```
## 参考文献

* [XML によるオブジェクト指向メッセージング](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)
* [Bean マークアップ言語](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

