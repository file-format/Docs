{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "partiell", "tillägg", "fil", "format", "webb", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Really Simple Syndication",
  "description":"Läs mer om RSS-filformat och API:er som kan skapa och öppna RSS-filer.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Vad är en RSS-fil? ##

En fil med tillägget .rss kallas Really Simple Syndication. RSS är en lätt eller lättläst filtyp av datorn, XML-filen. Dessa XML-filer uppdateras automatiskt med eventuella ändringar i data eller uppdateringar av en webbplats eller webbsida. Den uppdaterade informationen tillsammans med metadata (författarens namn, utgivarens namn, publiceringsdatum, etc.) och annat webbinnehåll på webbplatsen extraheras av användarens RSS-filer och presenteras i ett lättläst format. Det bästa med dessa RSS-filer är att det fungerar i realtid, och uppdateringarna, nyheterna, publiceringarna, det vill säga de senaste, visas överst i filen. Med hjälp av en RSS-fil kan du enkelt skapa en fil som innehåller de senaste uppdateringarna av alla ämnen som du är intresserad av, genom att hämta det relaterade innehållet från webben och läsa det med en RSS-fil.

## Kortfattad bakgrund ##

I sitt kött skapades RSS-filen först av Netscape, de uppfann den första versionen av RSS-filen men släppte sedan idén och fortsatte inte med nyare versioner. Det var då **Userland Software** som arbetade på RSS-filformatet och fortsatte att förnya det med en nyare version, det var så RSS v2 kom in på marknaden. Uppfinningen av RSS kan dock kopplas tillbaka till Resource Description Framework, av Ramanathan V 1997. De två filerna fungerar ganska lika och det är säkert att anta att konceptet RSS bildades baserat på hur RDF fungerar, en filläsare som användes för att samla in metadata.

## Teknisk specifikation ##

RSS-filen är en typ av XML-fil och alla RSS-filer måste följa standarderna för XML 1.0. Det finns olika versioner av olika RSS-filer, såsom 0.91, 0.92, 2.0, bland annat. Filen för varje version överensstämmer med specifikationerna och standarderna för den specifika versionen.

## RSS-exempel ##

Följande är ett förenklat exempel på RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>,
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
## Referens ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
