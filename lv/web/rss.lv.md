{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"daļēja",
"pagarinājumu",
"failu",
"formātā",
"tīmeklī",
"Tiešām vienkārša sindikācija",
"Userland programmatūra"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS — patiešām vienkārša sindikācija",
  "description": "Uzziniet par RSS failu formātu un API, kas var izveidot un atvērt RSS failus.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-lvs"
}
},
  "lastmod": "2021-06-24"
}

## Kas ir RSS fails? ##

Fails ar paplašinājumu .rss ir pazīstams kā Really Simple Syndication. RSS ir viegli vai viegli nolasāms datora faila veids, XML fails. Šie XML faili tiek automātiski atjaunināti ar jebkādām izmaiņām datos vai vietnes vai tīmekļa lapas atjauninājumiem. Atjauninātā informācija kopā ar metadatiem (autora vārds, izdevēja vārds, publicēšanas datums utt.) un cits vietnes tīmekļa saturs tiek izvilkts ar lietotāja RSS failiem un tiek parādīts viegli lasāmā formātā. Šo RSS failu labākā īpašība ir tā, ka tie darbojas reāllaikā, un atjauninājumi, ziņas, publicētie, tas ir, jaunākie, tiek parādīti faila augšdaļā. Izmantojot RSS failu, varat viegli izveidot failu ar jaunākajiem atjauninājumiem par jebkuru jūs interesējošo tēmu, izvelkot saistīto saturu no tīmekļa un nolasot to, izmantojot RSS failu.

## Īsa vēsture ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. Abu failu darbība ir diezgan līdzīga, un var droši pieņemt, ka RSS jēdziens tika izveidots, pamatojoties uz RDF, failu lasītāja darbību, kas tika izmantota metadatu vākšanai.

## Tehniskā specifikācija Nr.

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Ir dažādas dažādu RSS failu versijas, piemēram, 0.91, 0.92, 2.0, cita starpā. Katras versijas fails atbilst konkrētās versijas specifikācijām un standartiem. 

## RSS piemērs ##

Tālāk ir sniegts vienkāršots RSS piemērs.

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
## Atsauce Nr.

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
