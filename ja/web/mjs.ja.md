{
  "date" : "2021-07-20",
  "keywords" :["MJS","ファイル","拡張子","ファイル形式","ファイル拡張子","Node.js ESモジュールファイル"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES モジュール Javascript ファイル",
  "description" :"MJS ファイルとは何か,および MJS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## .MJS オプション番号

拡張子が .mjs のファイルは、Node.js アプリケーションで ECMA モジュール (ECMAScript モジュール) として使用される JavaScript ソース コード ファイルです。 Node.js の natvie モジュール システムは CommonJS であり、[JS](/web/js/) コードを整理するためにコードを異なるファイルに分割するために使用されます。 MJS は、Node.js がモジュールが CommonJS か ES6 かを識別するために使用する唯一の方法です。 ECMAScript モジュールは、再利用のために JavaScript コードをパッケージ化するための標準形式です。 MJS ファイルは、Atom、Vim、Apple xCode、Microsoft Visual Studio、メモ帳などのテキスト エディターで開くことができます。

## MJS ファイル形式 - 詳細情報

MJS ファイルは、JavaScript 構文のプレーン テキスト形式でディスクに保存されます。これらは任意のテキスト エディターで開くことができ、人間が判読できます。 2018 年以降、ほぼすべての主要なブラウザーが ES モジュールをサポートするようになりました。

## ES モジュールと CommonJS の違い

では、MJS ファイルはプレーンな JS ファイルと何が違うのでしょうか? ES モジュールと CommonJS の違いは、次のように要約できます。

* require、exports、または module.exports はありません
* \__filename または \__dirname はありません
* JSON モジュールの読み込みなし
* ネイティブ モジュールの読み込みなし
* require.resolve なし
* NODE_PATH なし
* require.extensions なし
* require.cache なし

## 参考文献

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [JS と MJS の違い](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

