{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "일부", "확장자", "파일", "형식", "웹", "정말 단순 신디케이션","유저랜드 소프트웨어" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - 정말 간단한 신디케이션",
  "description":"RSS 파일 형식과 RSS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## RSS 파일이란? ##

확장자가 .rss인 파일을 "Really Simple Syndication"이라고 합니다. RSS는 컴퓨터에서 쉽게 또는 쉽게 읽을 수 있는 파일 형식인 XML 파일입니다. 이러한 XML 파일은 웹 사이트 또는 웹 페이지의 데이터 변경 또는 업데이트로 자동 업데이트됩니다. 웹사이트의 메타데이터(저자명, 발행자명, 발행일 등) 및 기타 웹 콘텐츠와 함께 업데이트된 정보를 사용자의 RSS 파일로 추출하여 읽기 쉬운 형식으로 제공합니다. 이 RSS 파일의 가장 큰 특징은 실시간으로 작동하며 최신 업데이트, 뉴스, 발행물이 파일 상단에 표시된다는 것입니다. RSS 파일을 사용하면 웹에서 관련 콘텐츠를 가져오고 RSS 파일을 사용하여 읽어 관심 있는 주제의 최신 업데이트가 포함된 파일을 쉽게 만들 수 있습니다.

## 간략한 역사 ##

실제로 RSS 파일은 Netscape에 의해 처음 만들어졌으며 RSS 파일의 첫 번째 버전을 발명했지만 아이디어를 버리고 새 버전을 계속 만들지 않았습니다. RSS 파일 형식으로 작업하고 새 버전으로 계속 혁신한 것은 **Userland Software**였습니다. 이것이 RSS v2가 시장에 나온 방법입니다. 그러나 RSS의 발명은 1997년 Ramanathan V의 Resource Description Framework로 다시 연결될 수 있습니다. 두 파일의 작동은 매우 유사하며 RSS의 개념이 RDF의 작동을 기반으로 형성되었다고 가정하는 것이 안전합니다. 메타데이터를 수집하는 데 사용된 파일 판독기입니다.

## 기술 사양 ##

RSS 파일은 XML 파일의 일종으로 모든 RSS 파일은 XML 1.0의 표준을 따라야 한다. 0.91, 0.92, 2.0 등과 같은 다양한 RSS 파일 버전이 있습니다. 각 버전의 파일은 해당 버전의 사양 및 표준을 따릅니다.

## RSS 예 ##

다음은 RSS의 단순화된 예입니다.

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
## 참조 ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
