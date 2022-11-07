{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "ファイル", "拡張子", "フォーマット", "eBook", "デジタルブック" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"LRF ファイル形式と,LRF ファイルを作成して開くことができる API について学びます。",
  "title" :"LRF ファイル形式 - ソニーのポータブル リーダー ファイル",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## .LRF オプション番号

拡張子が .lrf のファイルは、テキスト、画像、ページネーション データなど、Sony BBeB のデータを含むブロード バンド eBook (BBeB) ファイルです。ファイルは、ヘッダー、指定された数のオブジェクト、およびオブジェクト インデックスを含む圧縮バイナリ形式で保存されます。 LRF および LRX ファイルには、利用可能な 2 つの BBeB ブック形式が含まれています。 LRF ファイルは暗号化されておらず、[LRX](/ebook/lrf/) ファイルからコンパイルできます。 LRF ファイルは、PDF や HTML など、他のいくつかのファイル タイプから変換できます。コンピュータがLRF ファイルを開くことができない場合は、LRF ファイルを開く、または編集するためのソフトウェアがインストールされていない可能性があります。 LRFファイルを開くことができるプログラムは、Windows用のCalibre、BookDesigner、MakelrfおよびCanon Book Creator、Linux用のCalibre、Macintosh用のCalibre、およびSony Readerです。

## 簡単な歴史

LRF ファイル タイプは、何よりもまず [inXile エンターテイメント](https://en.wikipedia.org/wiki/InXile_Entertainment) によって Line Rider に関連付けられています。 Line Rider は、インターネット物理学のおもちゃで、2006 年 9 月にスロベニアの大学生 Boštjan Čadež によって発明されました。 Sony ブランドの eBook 電子書籍リーダー (Sony PRS-500 リーダーや Sony Librie など) は、ドキュメントとテキストに LRF ファイル拡張子を使用します。このプロプライエタリなファイル タイプは、関連する LRS および LRX ファイルと同様に廃止されました。これら 3 つのファイル タイプは、ソニーが EPUB 形式で電子ブックの販売を開始した 2010 年に廃止された BroadBand eBook (BBeB) を構成していました。

## LRF ファイル形式

LRF ファイル形式の詳細な仕様は、[Web アーカイブ](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) で入手できます。 LRF ファイルは次のもので構成されます。
* ヘッダー
* オブジェクトの数
* オブジェクト インデックス。

これらの値はすべて Intel (LSB first) 順です。

### LRFヘッダー

|オフセット(16進数) |サイズ(バイト) |名称・意味|値の例|
---|---|---|---|
|0 |8| LRF署名| 4C 00 52 00 46 00 00 00 = Unicode の「LRF」|
|8 |2|バージョン?|ほとんどのファイルで 999|
|A |2| "疑似暗号化" |キーバイト 48|
|0C |4|ルート オブジェクト ID| 0x0044|
|10 |8|オブジェクト数 |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4|不明| 0|
|24 |1|フラグ| (16 - 後ろから前、1 = 前から後ろ) 16|
|25 |1|不明 |(パディング?) 0|
|26 |2|不明| 1600|
|28 |2|不明| (パディング?) 0|
|2A |2|身長？| 600|
|2C |2|幅?| 800|
|2E |1|不明| 24|
|2F |1|不明 |(パディング?) 0|
|30 |0x14|不明|ゼロ|
|44 |4| PlaneStream (0x1E) オブジェクトのみのオブジェクト ID| 0x0042|
|48 |4|不明 |0x1536|
|4C |2| XMLCompSize| 0x035C|


## 参考文献

* [LRF ファイル形式](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - ウィキペディアによる](https://en.wikipedia.org/wiki/BBeB)

