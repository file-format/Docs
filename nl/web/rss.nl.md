{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "gedeeltelijk", "extensie", "bestand", "format", "web", "Really Simple Syndication","Userland Software"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Echt eenvoudige syndicatie",
  "description":"Meer informatie over RSS-bestandsindeling en API's die RSS-bestanden kunnen maken en openen.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Wat is een RSS-bestand? ##

Een bestand met de extensie .rss staat bekend als Really Simple Syndication. RSS is een gemakkelijk of gemakkelijk door de computer te lezen bestandstype, het XML-bestand. Deze XML-bestanden worden automatisch bijgewerkt met eventuele wijzigingen in gegevens of updates van een website of webpagina. De bijgewerkte informatie samen met de metadata (naam van de auteur, naam van de uitgever, publicatiedatum, enz.) en andere webinhoud van de website worden geëxtraheerd door de RSS-bestanden van de gebruiker en gepresenteerd in een gemakkelijk te lezen formaat. De beste eigenschap van deze RSS-bestanden is dat het in realtime werkt en dat de updates, nieuws, publicaties, dat wil zeggen de laatste, bovenaan het bestand worden weergegeven. Met behulp van een RSS-bestand kunt u eenvoudig een bestand maken met de laatste updates van elk onderwerp waarin u geïnteresseerd bent, door de gerelateerde inhoud van internet te halen en deze te lezen met behulp van een RSS-bestand.

## Korte geschiedenis ##

In wezen werd het RSS-bestand voor het eerst gemaakt door Netscape, ze bedachten de eerste versie van het RSS-bestand, maar lieten het idee vallen en gingen niet verder met nieuwere versies. Het was toen de **Userland Software** die aan het RSS-bestandsformaat werkte en het bleef innoveren met een nieuwere versie, zo kwam RSS v2 op de markt. De uitvinding van RSS kan echter worden teruggekoppeld naar het Resource Description Framework, door Ramanathan V in 1997. De werking van de twee bestanden is vrij gelijkaardig en het is veilig om aan te nemen dat het concept van RSS werd gevormd op basis van de werking van RDF, een bestandslezer die werd gebruikt om metadata te verzamelen.

## Technische specificatie ##

Het RSS-bestand is een type XML-bestand en alle RSS-bestanden moeten voldoen aan de normen van XML 1.0. Er zijn verschillende versies van verschillende RSS-bestanden, zoals onder andere 0.91, 0.92, 2.0. Het bestand van elke versie voldoet aan de specificaties en normen van die specifieke versie.

## RSS-voorbeeld ##

Het volgende is een vereenvoudigd voorbeeld van de RSS.

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
## Referentie ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
