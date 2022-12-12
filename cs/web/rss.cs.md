{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "částečné", "rozšíření", "soubor", "formát", "web", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Really Simple Syndication",
  "description":"Další informace o formátu souborů RSS a rozhraních API, která mohou vytvářet a otevírat soubory RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Co je to soubor RSS? ##

Soubor s příponou .rss je známý jako Really Simple Syndication. RSS je snadno nebo snadno čitelný typ souboru na počítači, soubor XML. Tyto soubory XML jsou automaticky aktualizovány při jakýchkoli změnách v datech nebo aktualizacích webové stránky nebo webové stránky. Aktualizované informace spolu s metadaty (jméno autora, jméno vydavatele, datum vydání atd.) a další webový obsah webové stránky jsou extrahovány pomocí souborů RSS uživatele a prezentovány ve snadno čitelném formátu. Nejlepší vlastností těchto souborů RSS je, že fungují v reálném čase a aktualizace, novinky, publikace, tedy nejnovější, se zobrazují v horní části souboru. Pomocí souboru RSS můžete snadno vytvořit soubor obsahující nejnovější aktualizace libovolného tématu, které vás zajímá, stažením souvisejícího obsahu z webu a jeho přečtením pomocí souboru RSS.

## Stručná historie ##

Ve své podstatě byl soubor RSS nejprve vytvořen společností Netscape, vynalezli první verzi souboru RSS, ale poté od této myšlenky upustili a nepokračovali s novějšími verzemi. Tehdy to byl **Userland Software**, který pracoval na formátu souborů RSS a pokračoval v jeho inovaci s novější verzí, takto přišla na trh RSS v2. Vynález RSS však může být propojen zpět s rámcem popisu zdrojů od Ramanathana V v roce 1997. Fungování těchto dvou souborů je velmi podobné a lze s jistotou předpokládat, že koncept RSS byl vytvořen na základě fungování RDF, čtečka souborů, která byla použita ke sběru metadat.

## Technická specifikace ##

Soubor RSS je typ souboru XML a všechny soubory RSS musí splňovat standardy XML 1.0. Existují různé verze různých souborů RSS, mimo jiné například 0.91, 0.92, 2.0. Soubor každé verze odpovídá specifikacím a standardům dané konkrétní verze.

## Příklad RSS ##

Následuje zjednodušený příklad RSS.

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
## reference ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
