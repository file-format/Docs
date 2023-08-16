{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "file", "extension", "format", "eBook", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az LRF fájlformátumról és az LRF-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"LRF fájlformátum – Sony hordozható olvasófájl",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Mi az LRF fájl?

Az .lrf kiterjesztésű fájl egy szélessávú eBook (BBeB) fájl, amely a Sony BBeB adatait tartalmazza, beleértve a szöveget, képeket és oldalszámozási adatokat. A fájl tömörített bináris formátumban kerül mentésre, amely egy fejlécet, meghatározott számú objektumot és egy objektumindexet tartalmaz. Az LRF és LRX fájlok a két elérhető BBeB könyvformátumot tartalmazzák. Az LRF fájlok nem titkosítottak, és [LRX](/hu/ebook/lrf/) fájlokból fordíthatók. Az LRF fájlok számos más fájltípusból konvertálhatók, beleértve a PDF és HTML fájlokat. Ha a számítógépe nem tudja megnyitni az LRF fájlt, akkor valószínűleg nincs telepítve az LRF fájlok megnyitásához vagy szerkesztéséhez szükséges szoftver. Az LRF-fájlokat megnyitó programok a következők: Caliber, BookDesigner, Makelrf és Canon Book Creator for Windows, Caliber for Linux, Caliber és Sony Reader for Macintosh.

## Rövid története

Az LRF fájltípus mindenekelőtt az [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) Line Rider termékéhez kapcsolódik. A Line Rider egy internetes fizikai játék, amelyet 2006 szeptemberében egy szlovén egyetemista, Boštjan Čadež talált fel. A Sony márkájú eBook e-olvasók (mint például a Sony PRS-500 olvasók és a Sony Librie) az LRF fájlkiterjesztést használják dokumentumaikhoz és szövegeikhez. Ez a védett fájltípus, valamint a kapcsolódó LRS- és LRX-fájlok mára elavulttá vált. Ez a három fájltípus alkotta a BroadBand eBookot (BBeB), amely 2010-ben megszűnt, amikor a Sony elkezdte EPUB formátumban árusítani e-könyveit.

## LRF fájlformátum

Az LRF fájlformátum részletes specifikációi a [webarchívum](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) címen érhetők el. Az LRF fájl a következőkből áll:
* egy fejléc
* számos objektum
* egy objektum index.

Mindezek az értékek Intel (LSB first) sorrendben vannak megadva.

### LRF fejléc

|Eltolás (hex) |Méret (byte) |Név/jelentés| Példaérték|
---|---|---|---|
|0 |8| LRF aláírás| 4C 00 52 00 46 00 00 00 = "LRF" Unicode-ban|
|8 |2| verzió?| 999 a legtöbb fájlban|
|A |2| "Psuedo-Encryption" |kulcsbyte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| Objektumok száma |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| ismeretlen| 0|
|24 |1| Zászlók| (16 - hátulról előre, 1 = elölről hátra) 16|
|25 |1| ismeretlen |(padding?) 0|
|26 |2| ismeretlen| 1600|
|28 |2| ismeretlen| (padding?) 0|
|2A |2| Magasság?| 600|
|2C |2| Szélesség?| 800|
|2E |1| ismeretlen| 24|
|2F |1| ismeretlen |(padding?) 0|
|30 |0x14| ismeretlen| nullák|
|44 |4| Csak a PlaneStream (0x1E) objektum objektumazonosítója| 0x0042|
|48 |4| ismeretlen |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Hivatkozások

* [LRF fájlformátum](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB – a Wikipedia által](https://en.wikipedia.org/wiki/BBeB)

