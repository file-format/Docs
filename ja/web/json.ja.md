---
date: 2019-10-11
keywords: json,.json,jsonファイル形式,jsonファイルの開き方,javascriptオブジェクト表記,jsonデータ形式,.jsonファイル形式
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON ファイル形式 - JSON ファイルとは?
linktitle: JSON
description: "JSON ファイル形式と,JSON ファイルを作成して開くことができる API について学習します。"
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## JSON ファイルとは何ですか?

JSON (JavaScript Object Notation) は、人間が判読できるテキストを使用してデータを保存および送信するデータ共有用のオープン スタンダード ファイル形式です。 JSON ファイルは .json 拡張子で保存されます。 JSON は必要なフォーマットが少なく、[XML](/web/xml/) の優れた代替手段です。 JSON は JavaScript から派生したものですが、言語に依存しないデータ形式です。 JSON の生成と解析は、多くの最新のプログラミング言語でサポートされています。 *application/json* は JSON に使用されるメディア タイプです。

## JSON ファイル形式 - 簡単な歴史

JSON の作成につながるリアルタイムのサーバーからクライアントへの通信が必要でした。 JSON 形式は、2001 年 3 月に Douglas Crockford によって最初に指定されました。JSON は、JavaScript のサブセットである Standard ECMA-262 3rd Edition (1999 年 12 月) に基づいていました。

JSON 標準 ECMA-404 の初版は、2013 年 10 月に Ecma International によって発行されました。 RFC 7159 は、2014 年に JSON のインターネット使用の主要なリファレンスになりました。2017 年 11 月には、ISO/IEC 21778:2017 が国際標準として発行されました。 RFC 8259 は、2017 年 12 月 13 日にインターネット標準 STD 90 の最新バージョンである Internet Engineering Task Force によって公開されました。

## JSON ファイル構造

JSON データは **key/value** ペアで書き込まれます。キーと値はコロン (:) で区切られ、左側にキー、右側に値が表示されます。異なるキー/値のペアはコンマ (,) で区切られます。キーは、"name" などの二重引用符で囲まれた文字列です。値は、次のタイプにすることができます。

- `番号`
- `String`: 二重引用符で囲まれた一連の Unicode 文字。
- `Boolean`: True または False。
- `Array`: 角括弧で囲まれた値のリスト。たとえば

json
[「りんご」「バナナ」「オレンジ」]
```

- `Object`: 中かっこで囲まれたキーと値のペアのコレクション。

json
{"name": "Jack", "age": 30, "favoriteSport" : "Football"}
```

JSON オブジェクトをネストして、データの構造を表すこともできます。以下は、JSON オブジェクトの例です。

### JSON 形式の例

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON ファイルの最大サイズは？

JSON ファイルの最大サイズに事実上制限はありません。収納する内容物が必要とするスペースに限ります。

インターネット経由でデータを転送するために JSON ファイル形式を使用する場合、コンピューターの利用可能なリソースに注意する必要があります。大きな JSON データが転送される場合、クライアント ブラウザのメモリが限られている場合、転送は影響を受けます。


仕様で定義された厳密な制限はありませんが、ユーザー エクスペリエンスが急速に低下し、ユーザーがアプリを放棄する可能性があるため、ユーザーのコンピューターのリソースを使い果たしてしまわないように注意する必要があります。

## JSON と XML

**XML** は、インターネット上でデータを交換するために広く使用されている、もう 1 つの一般的なファイル形式です。アプリケーション間のデータ交換に関しては、開発者は XML と JSON の両方のファイル形式を使用できます。ただし、JSON は、次の理由により、インターネットを介したアプリケーション間のデータ交換に最も便利な方法として採用されています。

1. JSON は、XML ファイル形式と比較して、明確で読みやすいデータ ビューを提供します。
1. JSON は、XML と比較して同じデータ セットを定義するための文字数が少ないため、インターネットを介したデータ転送のオーバーヘッドを削減します。
1. 最新のプログラミング言語には、Web 経由で JSON 応答を解析する組み込みのパーサーが用意されています。

## 知ってますか？

FileFormat.com の寄稿者になって、ファイル形式コミュニティを最新の状態に保つことができます。 JSON または Web ファイル形式について共有する必要がある場合は、[Web ファイル形式ニュース](https://news.fileformat.com/t/Web) セクションに調査結果を投稿して、人々がこれらから詳細を学べるようにすることができます。

## 参考文献

- [JSON - ウィキペディア](https://en.wikipedia.org/wiki/CSS)
- [JSON の紹介](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

