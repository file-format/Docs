{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI ファイル - Asterisk Gateway Interface ファイル形式",
  "description":"AGI ファイルを作成して開くことができる例と API を使用して,AGI ファイル形式とは何かについて学びます。",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AGI ファイルとは何ですか?

AGI ファイルは、オープン ソースのテレフォニー システムである Asterisk で使用されるスクリプト ファイルです。プロセスとアスタリスクのダイヤルプランを自動化するために使用できる情報が含まれています。 AGI スクリプト ファイルを使用して、PostgreSQL や MySQL などのリレーショナル データベースとの接続を確立できます。さらに、AGI スクリプトを使用して他の外部リソースにアクセスすることもできます。 AGI スクリプトはダイヤルプランの制御を外部の AGI スクリプトに引き渡すことができるため、Asterisk は複雑なタスクを実行できます。

## AGI ファイル形式 - 詳細情報

AGI スクリプト ファイルはテキスト ファイルとして保存され、任意のテキスト エディターで開いて変更を加えることができます。

### AGI通信の標準パターン

AGI スクリプトは、Asterisk から送信された変数とその値を読み込みます。これらの変数の一般的な外観は次のとおりです。

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

これらの変数の後には、Asterisk によって送信される空白行が続き、AGI スクリプトが現在ダイヤルプランを制御できることを示しています。

### AGI スクリプト ファイルのプログラミング言語

AGI スクリプトは通常、Perl、[PHP](/programming/php/)、[C](/programming/c/)、Pascal、または Bourne Shell で記述できます。

## 参考文献

* [アスタリスク AGI スクリプト](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

