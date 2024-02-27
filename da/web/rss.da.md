{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"delvis",
"udvidelse",
"fil",
"format",
"web",
"Virkelig simpel syndikering",
"Userland Software"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS - Really Simple Syndication",
  "description": "Lær om RSS-filformat og API'er, der kan oprette og åbne RSS-filer.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-das"
}
},
  "lastmod": "2021-06-24"
}

## Hvad er en RSS fil? ##

En fil med filtypenavnet .rss er kendt som Really Simple Syndication. RSS er en let eller let læselig filtype af computeren, XML-filen. Disse XML-filer opdateres automatisk med eventuelle ændringer i data eller opdateringer af et websted eller en webside. De opdaterede oplysninger sammen med metadataene (forfatterens navn, udgiverens navn, udgivelsesdato osv.) og andet webindhold på hjemmesiden udtrækkes af brugerens RSS-filer og præsenteres i et letlæseligt format. Det bedste ved disse RSS-filer er, at det fungerer i realtid, og opdateringer, nyheder, udgivelser, det er de seneste, vises øverst i filen. Ved hjælp af en RSS-fil kan du nemt oprette en fil, der indeholder de seneste opdateringer af ethvert emne, du er interesseret i, ved at trække det relaterede indhold fra nettet og læse det ved hjælp af en RSS-fil.

## Kort historie ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. Funktionerne af de to filer er ret ens, og det er sikkert at antage, at konceptet RSS blev dannet baseret på RDF, en fillæser, der blev brugt til at indsamle metadata.

## Teknisk specifikation ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Der er forskellige versioner af forskellige RSS-filer, såsom 0.91, 0.92, 2.0, blandt andre. Filen for hver version er i overensstemmelse med specifikationerne og standarderne for den specifikke version. 

## RSS-eksempel ##

Det følgende er et forenklet eksempel på RSS.

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
