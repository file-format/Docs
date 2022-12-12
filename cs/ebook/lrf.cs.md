{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "soubor", "rozšíření", "formát", "elektronická kniha", "Digitální kniha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů LRF a rozhraních API, která mohou vytvářet a otevírat soubory LRF.",
  "title" :"Formát souboru LRF - soubor Sony Portable Reader",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Co je soubor LRF?

Soubor s příponou .lrf je soubor Broad Band eBook (BBeB), který obsahuje data pro Sony BBeB, včetně textu, obrázků a dat stránkování. Soubor je uložen v komprimovaném binárním formátu, který obsahuje záhlaví, určený počet objektů a index objektu. Soubory LRF a LRX zahrnují dva dostupné formáty knih BBeB. Soubory LRF nejsou zašifrovány a lze je zkompilovat ze souborů [LRX](/cs/ebook/lrf/). Soubory LRF lze převést z několika dalších typů souborů včetně PDF a HTML. Pokud váš počítač nemůže otevřít soubor LRF, pravděpodobně nemáte nainstalovaný software pro otevření nebo úpravu souborů LRF. Programy, které mohou otevřít soubory LRF, jsou Caliber, BookDesigner, Makelrf a Canon Book Creator pro Windows, Calibre pro Linux, Calibre a Sony Reader pro Macintosh.

## Stručná historie

Typ souboru LRF je v první řadě spojen s Line Rider od [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider je internetová fyzikální hračka a byla vynalezena v září 2006 slovinským univerzitním studentem Boštjanem Čadežem. Čtečky elektronických knih značky Sony (jako jsou čtečky Sony PRS-500 a Sony Librie) využívají pro své dokumenty a texty příponu souboru LRF. Tento proprietární typ souboru je nyní zastaralý, stejně jako související soubory LRS a LRX. Tyto tři typy souborů tvořily BroadBand eBook (BBeB), který byl ukončen v roce 2010, kdy Sony začala prodávat své e-knihy ve formátu EPUB.

## Formát souboru LRF

Podrobné specifikace formátu souboru LRF jsou k dispozici na [webovém archivu] (https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Soubor LRF se skládá z:
* záhlaví
* množství objektů
* index objektu.

Všechny tyto hodnoty jsou v Intel (LSB first) řádu.

### Záhlaví LRF

|Offset (hexadecimální) |Velikost (bajty) |Název/význam| Příklad hodnoty|
---|---|---|---|
|0 |8| Podpis LRF| 4C 00 52 00 46 00 00 00 = "LRF" v Unicode|
|8 |2| verze?| 999 ve většině souborů|
|A |2| "Psuedo-Encryption" |bajt klíče 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| PočetObjektů |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| neznámý| 0|
|24 |1| Vlajky| (16 - zezadu dopředu, 1 = zepředu dozadu) 16|
|25 |1| neznámý |(výplň?) 0|
|26 |2| neznámý| 1600|
|28 |2| neznámý| (vycpávka?) 0|
|2A |2| Výška?| 600|
|2C |2| Šířka?| 800|
|2E |1| neznámý| 24|
|2F |1| neznámý |(výplň?) 0|
|30 |0x14| neznámý| nuly|
|44 |4| ID objektu pouze objektu PlaneStream (0x1E)| 0x0042|
|48 |4| neznámý |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Reference

* [Formát souboru LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB – podle Wikipedie](https://en.wikipedia.org/wiki/BBeB)

