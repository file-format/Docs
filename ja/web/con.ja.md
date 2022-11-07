{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON ファイル - コンセプト アプリケーション ソース ファイル形式",
  "description" :"CON ファイルとは何か,および CON ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## .CON ファイルとは何ですか?

CON ファイルは、**Concept Application Server** 用に開発されたアプリケーションのソース コード ファイルです。サーバーとユーザーの間でデータを交換するためのアプリケーションを作成するために使用されます。 Concept Client がユーザー側にインストールされていれば、サーバーでホストされている CON ファイルに Web ブラウザーでアクセスできます。コンセプト アプリケーション サーバーは、[SQL](/database/sql/) サブセット データベース エンジン (TinDB) を持つ小規模なプログラミング言語を使用した Web サーバーです。

CON ファイルは、RadGs Concept Application Server で開いて実行できます。

## CON ファイル形式 - 詳細情報

CON ファイルはサーバー上でホストされ、ユーザー マシンの Web ブラウザーを使用してアクセスされます。コンセプト [URL](/web/url/) は通常の HTTP URL とは異なり、**concept://** で始まります。

### CON ファイルの URL の例

Concept Application Server でホストされている CON ファイルには、次のような URL を使用して Web ブラウザーからアクセスできます。

```
concept://domain.server.com/web_application/main.con.
```
## 参考文献

* [コンセプト アプリケーション サーバー](https://github.com/Devronium/ConceptApplicationServer)

