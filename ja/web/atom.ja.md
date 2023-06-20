{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ATOM ファイル - Atom Syndication フォーマット",
  "description" :"ATOM ファイルとは何か,および ATOM ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## .ATOM ファイルとは何ですか?

ATOM ファイルは、Atom フィードおよびエントリ ドキュメントの構造のシンジケーション フォーマットです。 .RSS ファイルと同様に、ATOM ファイル形式は XML ベースのシンジケーション形式であり、コンテンツ公開の標準です。 ATOM ファイルは、ソフトウェア プログラムが Web サイトで公開されている更新を確認できるようにする Web フィードに使用されます。見出し、全文記事、抜粋、または Web サイトのコンテンツへのリンクなど、さまざまな種類のエントリが含まれています。

**ATOM ファイルを開く**ことができるアプリケーションには、**Apple Safari** があります。

## ATOM ファイル形式 - 詳細情報

ATOM ファイルは、情報交換用の汎用形式である一般的な XML ファイル形式で保存および公開されます。これは、RSS ファイル形式の制限と欠点を考慮して、RSS の代替として開発されました。

### Atom ドキュメントの種類

1. `Atom Entry Documents` - これは、Atom フィードのエントリーと呼ばれる単一の情報項目で構成される XML ドキュメントです。それはatom-entry多数の子要素を含む要素。 Atom エントリのコンテンツは、プレーン テキスト、HTML、XHTML、または別の IANA (Internet Assigned Numbers Authority) メディア タイプにすることができます。
1. `Atom フィード ドキュメント` - Atom フィードに関するメタデータと、フィードの 1 つ以上のエントリを提供する XML ドキュメントです。クライアントがフィードからの情報を要求すると、要求を満たすための多数の Atom エントリを含むフィード ドキュメントがサーバーによって生成されます。
1. `Atom コレクション` - 編集可能な Atom エントリの URL を含む特別な種類の Atom フィード ドキュメントです。

## 参考文献

* [Atom Syndication Format - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Atom フィードの概要 - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Web 標準](https://en.wikipedia.org/wiki/Atom_(web_standard))

