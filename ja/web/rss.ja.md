{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "部分", "拡張子", "ファイル", "フォーマット", "ウェブ", "Really Simple Syndication","ユーザーランド ソフトウェア" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - 本当にシンプルなシンジケーション",
  "description":"RSS ファイル形式と,RSS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## RSSファイルとは？ ##

拡張子が .rss のファイルは、Really Simple Syndication と呼ばれます。 RSS は、コンピューターで簡単に読み取れるファイルの種類である XML ファイルです。これらの XML ファイルは、データの変更や Web サイトまたは Web ページの更新によって自動的に更新されます。メタデータ (作成者名、発行者名、発行日など) とともに更新された情報、および Web サイトのその他の Web コンテンツは、ユーザーの RSS ファイルによって抽出され、読みやすい形式で表示されます。これらの RSS ファイルの最大の特徴は、リアルタイムで動作し、最新の更新、ニュース、公開がファイルの上部に表示されることです。 RSS ファイルを使用すると、関心のあるトピックの最新の更新を含むファイルを簡単に作成できます。関連するコンテンツを Web から取得し、RSS ファイルを使用してそれを読み取ることができます。

## 簡単な歴史 ##

実際には、RSS ファイルは Netscape によって最初に作成されました。Netscape は RSS ファイルの最初のバージョンを発明しましたが、その後アイデアを破棄し、新しいバージョンを継続しませんでした。その後、RSS ファイル形式に取り組み、新しいバージョンで革新を続けたのは **Userland Software** でした。これが、RSS v2 が市場に登場した方法です。ただし、RSS の発明は、1997 年に Ramanathan V によってリソース記述フレームワークに関連付けることができます。2 つのファイルの動作は非常に似ており、RSS の概念は RDF の動作に基づいて形成されたと想定しても安全です。メタデータの収集に使用されたファイル リーダー。

## 技術仕様 ##

RSS ファイルは XML ファイルの一種であり、すべての RSS ファイルは XML 1.0 の標準に従う必要があります。 0.91、0.92、2.0 など、さまざまな RSS ファイルのさまざまなバージョンがあります。各バージョンのファイルは、その特定のバージョンの仕様と標準に準拠しています。

## RSS の例 ##

以下は、RSS の簡単な例です。

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## 参照 ＃＃

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
