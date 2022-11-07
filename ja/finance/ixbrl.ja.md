{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","ixbrl ファイル", "ixbrl ファイル形式", "ixbrl ファイルの種類", "ファイル", "種類", "ixbrl ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - ビジネスおよび財務報告ファイル形式",
  "description":"IXBRL ファイル形式と,IXBRL ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## .iXBRL ファイルとは何ですか?

iXBRL (ilnine XBRL) ファイル形式を使用すると、[XBRL](/web/xbrl/) データを HTML ファイルに埋め込んで、マシンと人間の両方が読み取れるようにすることができます。実際には、XBRL タグを使用する [xHTML](/web/xhtml/) ファイルであり、英国の HMRC の要件を満たすために XBRL International によって開発されました。 iXBRL を使用すると、元の文書のレイアウトを維持したまま財務諸表を作成できます。 iXBRL ファイルは、Windows オペレーティング システムのメモ帳や MacOS の TextEdit などの任意のテキスト エディタで開くことができます。

## iXBRL ファイル形式

iXBRL 内では、XBRL のコンテンツは XML タグを使用する xHTML ファイル形式でラップされます。 XBRLのように、<xbrl> iXBRL ファイルのルート要素です。 XHTML 形式は、そのコンテンツをさまざまなドキュメント タイプとモジュールのコレクションとして表します。 XHTML のすべてのファイルは XML ファイル形式に基づいており、XML ドキュメント標準に準拠しています。 XHTML は、依存する [HTML](/web/html/) ドキュメント オブジェクト モデル (DOM) または [XML](/web/xml/) ドキュメント オブジェクト モデルの運用上の使用に不可欠な使用形式です。外の世界では、iXBRL は [xHTML](/web/xhtml/) ファイル形式の仕様に従います。

### iXBRL 対 XBRL

XBRL は、次の要因に基づいて iXBRL と比較できます。

*複雑さ
* 書式設定オプション
* ファイルの種類/拡張子
* レンダリング オプション
* ファイリングプロセス

次の表は、これらの違いを示しています。

|パラメータ|XBRL|iXBRL|
---|---|---|
|複雑さ|iXBRL よりも複雑|XHTML の既存の組織スキームにより、それほど複雑ではありません|
|書式設定オプション|限られた柔軟性|コンテンツの書式設定の高い柔軟性|
|ファイルの種類/拡張子|正式には .xml 拡張子で保存|通常は .html または .xhtml 拡張子で保存|
|レンダリング オプション|これらを表示するために必要な XBRL ビューア|ブラウザで表示できる人間が読めるコンテンツ|
|出願手続き| XBRL (機械可読) と HTML (人間可読) のインスタンス ドキュメントは別々にファイルされます。|人間可読形式と機械可読形式の両方が 1 つのインスタンス ドキュメントで利用できます|

## 参考文献

* [XBRL - ウィキペディアによる](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

