{
  "date" : "2022-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BR ファイル - Brotli 圧縮ファイル形式",
  "description":"BR ファイル形式と,BR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-20"
}

## .BR ファイルとは何ですか?

BR ファイルは、オープン ソースのデータ圧縮アルゴリズム **Brotli** を適用して生成された圧縮 Web ファイルです。スタイルシート ([CSS](/web/css/))、画像 ([SVG](/page-description-language/svg/))、[XML](/web/xml/)、スクリプトなどの Web ページ アセットを格納するために使用されます。ファイル ([JS](/web/js/))。 Chrome や Firefox などの現代の Web サイトでは、BR ファイルを使用してページの読み込み時間を短縮し、ユーザー エクスペリエンスを向上させています。

## BR ファイル形式

BR ファイルは、Brotli 圧縮アルゴリズムを使用して生成される圧縮された Web ファイルです。 Brotli 圧縮はロスレス データ圧縮アルゴリズムであり、Google によって Zopfli 圧縮アルゴリズムに開発されました。これは、LZ77 ロスレス圧縮アルゴリズムとハフマン コーディングの組み合わせに基づいています。

サイズが小さいため、BR ファイルは Web サーバーやコンテンツ配信ネットワーク (CDN) で使用されます。これらのサーバーに対して行われた要求により、HTTP コンテンツが圧縮され、Web サイトの読み込みが速くなります。 Brotli はより一般的になり、gzip よりも優れた圧縮を提供します。

## 参考文献

* [ブロトリ - ウィキペディア](https://en.wikipedia.org/wiki/Brotli)

