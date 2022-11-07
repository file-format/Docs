{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl ファイル", "拡張子", "形式", "wpl ファイルとは", "音楽", "wpl ファイル形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WPL ファイル形式と,WPL ファイルを作成,変換,開くことができる API について学びます。",
  "title" :"WPL - Windows Media Player プレイリスト ファイル",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## .WPL オプション番号

拡張子が .wpl のファイルには、Microsoft Windows Media Player で実行される曲のプレイリストが含まれています。これらのファイルは通常、ユーザーがビデオおよびオーディオ コレクション用に作成します。 WPL ファイルに書き込まれたコンテンツは、.wpl ファイルの作成者が選択したマルチメディア ファイルのディレクトリ パスまたは場所であるため、メディア プレーヤー アプリケーションは、ディレクトリの場所からマルチメディア コンテンツをすばやく見つけて再生できます。

## WPL ファイル形式

WPL (Windows Media Player Playlist) は、Microsoft Windows Media Player バージョン 9 以降で使用される独自のファイル形式です。マルチメディア プレイリストを格納するコンピュータ ファイル形式です。デフォルトでは、プレイリストは .wpl (Windows Media Player Playlist) 拡張子で保存されます。 [.m3u](/audio/m3u) 拡張子をサポートしていないデバイスでデータ ディスクを再生する場合は、代わりに [.m3u](/audio/m3u) 拡張子を使用できます。 WPL ファイルの要素は XML 形式で表されます。

最上位要素「smil」は、ファイルの要素が Synchronized Multimedia Integration Language (SMIL) 構造に従うことを指定します。ファイルは .wpl 拡張子で作成および保存され、その MIME タイプは application/vnd.ms-wpl です。

### WPL の例

wpl ファイルの例を次に示します。
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## 参照 ##

* [MPEG-1 オーディオ層 II - ウィキペディアによる](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

