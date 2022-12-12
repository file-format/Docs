{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "részleges", "kiterjesztés", "fájl", "formátum", "web", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS – Tényleg egyszerű híradás",
  "description":"További információ az RSS-fájlformátumról és az RSS-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Mi az RSS fájl? ##

Az .rss kiterjesztésű fájl Really Simple Syndication néven ismert. Az RSS a számítógép által könnyen vagy könnyen olvasható fájltípus, az XML-fájl. Ezeket az XML-fájlokat a rendszer automatikusan frissíti a webhely vagy weboldal bármely adatváltozásával vagy frissítésével. A frissített információkat a metaadatokkal (szerző neve, kiadó neve, közzétételi dátum stb.) és a weboldal egyéb webes tartalmával együtt a felhasználó RSS-fájljai nyerik ki, és könnyen olvasható formátumban jelenítik meg. Ezeknek az RSS-fájloknak a legjobb tulajdonsága, hogy valós időben működnek, és a frissítések, hírek, közzétételek, azaz a legfrissebbek a fájl tetején jelennek meg. Az RSS-fájl használatával könnyedén létrehozhat egy fájlt, amely tartalmazza az Önt érdeklő témák legújabb frissítéseit, ha leveszi a kapcsolódó tartalmat az internetről, és elolvassa egy RSS-fájl segítségével.

## Rövid története ##

Húsában az RSS fájlt először a Netscape készítette, ők találták ki az RSS fájl első verzióját, de aztán elvetették az ötletet, és nem folytatták az újabb verziókkal. Ekkor a **Userland Software** dolgozott az RSS fájlformátumon, és folytatta az innovációt egy újabb verzióval, így került a piacra az RSS v2. Az RSS feltalálása azonban visszavezethető Ramanathan V 1997-es Resource Description Framework-jéhez. A két fájl működése meglehetősen hasonló, és nyugodtan feltételezhetjük, hogy az RSS koncepciója az RDF működése alapján alakult ki, egy fájlolvasó, amelyet metaadatok gyűjtésére használtak.

## Műszaki specifikáció ##

Az RSS-fájl egyfajta XML-fájl, és minden RSS-fájlnak meg kell felelnie az XML 1.0 szabványának. A különböző RSS-fájloknak különböző verziói léteznek, például 0.91, 0.92, 2.0 stb. Az egyes verziók fájljai megfelelnek az adott verzió specifikációinak és szabványainak.

## RSS példa ##

A következő egy egyszerűsített példa az RSS-re.

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
## Hivatkozási szám

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
