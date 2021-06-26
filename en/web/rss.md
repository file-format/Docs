{
  "date" : "2021-06-24",
  "keywords" : [ "RSS", "partial", "extension", "file", "format", "web", "Really Simple Syndication","Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RSS - Really Simple Syndication",
  "description":"Learn about RSS file format and APIs that can create and open RSS files.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-06-24"
}

## What is an RSS file? ##

A file with the extension .rss is known as Really Simple Syndication. RSS is a readily or easily read file type by the computer, the XML file. These XML files are automatically updated with any changes in data or updates of a website or webpage. The updated information along with the metadata (author's name, publisher's name, publishing date, etc.), and other web content of the website are extracted by the user's RSS files and presented in an easy-to-read format. The best feature of these RSS files is that it works in real-time, and the updates, news, publishes, that is the latest, are displayed on the top of the file. Using an RSS file, you can easily create a file containing the latest updates of any topic that you are interested in, by pulling the related content from the web and reading it using an RSS file.

## Brief History ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. The workings of the two files are pretty similar and it is safe to assume that the concept of RSS was formed based on the workings of RDF, a file reader that was used to collect metadata.

## Technichal Specification ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. There are different versions of different RSS files, such as 0.91, 0.92, 2.0, amongst others. The file of each version conforms to the specifications and standards of that specific version. 

## RSS Example ##

The following is a simplified example of the RSS.

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
## Reference ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)