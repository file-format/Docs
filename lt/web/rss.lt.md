{
  "date": "2021-06-24",
  "keywords": [
"RSS",
"dalinis",
"pratęsimas",
"failą",
"formatu",
"žiniatinklio",
"Tikrai paprastas sindikavimas",
"Userland programinė įranga"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "RSS – tikrai paprastas sindikavimas",
  "description": "Sužinokite apie RSS failo formatą ir API, kurios gali kurti ir atidaryti RSS failus.",
  "linktitle": "RSS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rs-lts"
}
},
  "lastmod": "2021-06-24"
}

## Kas yra RSS failas? ##

Failas su plėtiniu .rss žinomas kaip Really Simple Syndication. RSS yra lengvai arba lengvai nuskaitomas kompiuterio failo tipas, XML failas. Šie XML failai automatiškai atnaujinami atsižvelgiant į bet kokius duomenų pakeitimus arba svetainės ar tinklalapio atnaujinimus. Atnaujinta informacija kartu su metaduomenimis (autoriaus vardas, leidėjo vardas, išleidimo data ir kt.) ir kitu svetainės žiniatinklio turiniu ištraukiami vartotojo RSS failais ir pateikiami lengvai skaitomu formatu. Geriausia šių RSS failų savybė yra ta, kad jie veikia realiuoju laiku, o naujinimai, naujienos, publikacijos, tai yra naujausios, yra rodomos failo viršuje. Naudodami RSS failą galite lengvai sukurti failą su naujausiais bet kurios jus dominančios temos atnaujinimais, ištraukę susijusį turinį iš žiniatinklio ir perskaitę jį naudodami RSS failą.

## Trumpa istorija ##

In its flesh, the RSS file was first created by Netscape, they invented the first version of the RSS file but then dropped the idea, and did not continue with newer versions. It was then the **Userland Software** that worked on the RSS file format and continued to innovate it with a newer version, this is how RSS v2 came into the market. However, the invention of RSS can be linked back to Resource Description Framework, by Ramanathan V in 1997. Dviejų failų veikimas yra gana panašus ir galima drąsiai manyti, kad RSS koncepcija buvo suformuota remiantis RDF, failų skaitytuvo, kuris buvo naudojamas metaduomenims rinkti, veikimu.

## Techninė specifikacija Nr.

The RSS file is a type of XML file and all RSS files must follow the standards of XML 1.0. Yra įvairių skirtingų RSS failų versijų, tokių kaip 0.91, 0.92, 2.0 ir kt. Kiekvienos versijos failas atitinka tos konkrečios versijos specifikacijas ir standartus. 

## RSS pavyzdys Nr.

Toliau pateikiamas supaprastintas RSS pavyzdys.

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
## Nuoroda ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
