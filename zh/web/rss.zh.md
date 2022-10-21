{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "partial", "extension", "file", "format", "web", "Really Simple Syndication","Userland Software"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - 真正简单的联合",
  "description":"了解 RSS 文件格式和可以创建和打开 RSS 文件的 API。",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## 什么是 RSS 文件？ ##

扩展名为 .rss 的文件称为真正简单的联合。 RSS 是一种易于计算机读取的文件类型，即 XML 文件。这些 XML 文件会随着数据的任何更改或网站或网页的更新而自动更新。更新的信息连同元数据（作者姓名、出版商姓名、出版日期等）和网站的其他网页内容由用户的 RSS 文件提取并以易于阅读的格式呈现。这些RSS文件的最大特点是实时工作，更新、新闻、发布，也就是最新的，都显示在文件的顶部。使用 RSS 文件，您可以轻松地创建一个包含您感兴趣的任何主题的最新更新的文件，方法是从 Web 中提取相关内容并使用 RSS 文件进行阅读。

## 历史简介 ＃＃

从本质上讲，RSS 文件最初是由 Netscape 创建的，他们发明了 RSS 文件的第一个版本，但后来放弃了这个想法，并且没有继续使用新版本。正是 **Userland Software** 致力于 RSS 文件格式，并继续用更新的版本对其进行创新，这就是 RSS v2 进入市场的方式。然而，RSS 的发明可以追溯到 1997 年 Ramanathan V 的 Resource Description Framework。这两个文件的工作方式非常相似，可以肯定地假设 RSS 的概念是基于 RDF 的工作方式形成的，用于收集元数据的文件阅读器。

## 技术规格##

RSS 文件是一种 XML 文件，所有的 RSS 文件都必须遵循 XML 1.0 的标准。不同的 RSS 文件有不同的版本，例如 0.91、0.92、2.0 等。每个版本的文件都符合该特定版本的规范和标准。

## RSS 示例##

以下是 RSS 的简化示例。

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
## 参考 ＃＃

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
