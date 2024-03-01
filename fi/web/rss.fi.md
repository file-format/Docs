{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"osittainen",
"laajennus",
"tiedosto",
"muoto",
"web",
"Todella yksinkertainen syndikaatio",
"Userland-ohjelmisto"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS - Todella yksinkertainen jakelu",
  "description": "Opi RSS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RSS-tiedostoja.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-fis"
}
},
  "lastmod": "2021-06-24"
}

## Mikä on RSS-tiedosto? ##

Tiedosto, jonka tunniste on .rss, tunnetaan nimellä Really Simple Syndication. RSS on tietokoneen helposti tai helposti luettava tiedostotyyppi, XML-tiedosto. Nämä XML-tiedostot päivitetään automaattisesti tietomuutoksilla tai verkkosivuston tai verkkosivun päivityksillä. Päivitetyt tiedot sekä metatiedot (tekijän nimi, julkaisijan nimi, julkaisupäivä jne.) ja muu verkkosivuston verkkosisältö poimitaan käyttäjän RSS-tiedostoista ja esitetään helposti luettavassa muodossa. Näiden RSS-tiedostojen paras ominaisuus on, että ne toimivat reaaliajassa ja päivitykset, uutiset, julkaisut, eli uusimmat, näkyvät tiedoston yläosassa. RSS-tiedoston avulla voit helposti luoda tiedoston, joka sisältää viimeisimmät päivitykset mistä tahansa sinua kiinnostavasta aiheesta, vetämällä siihen liittyvän sisällön verkosta ja lukemalla sen RSS-tiedoston avulla.

## Lyhyt historia ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. Näiden kahden tiedoston toiminta on melko samankaltaista, ja on turvallista olettaa, että RSS:n käsite muodostettiin metatietojen keräämiseen käytetyn RDF:n tiedostonlukijan toiminnan perusteella.

## Tekniset tiedot ##

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Eri RSS-tiedostoista on olemassa erilaisia versioita, kuten 0.91, 0.92, 2.0, mm. Kunkin version tiedosto on kyseisen version spesifikaatioiden ja standardien mukainen. 

## RSS-esimerkki ##

Seuraava on yksinkertaistettu esimerkki RSS:stä.

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
## Viite ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
