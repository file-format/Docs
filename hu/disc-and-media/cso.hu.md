{
  "date" : "2021-08-09",
  "keywords" :[ "cso fájl", "cso fájl formátum", "mi az a cso fájl", "fájl", "cso példa", "cso fájl kiterjesztése", "kiterjesztés", "formátum", "iso", "DAX tömörítés"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"További információ a CSO fájlformátumról és az API-król, amelyek CSO-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"CSO – tömörített ISO lemezkép",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Mi az a CSO fájl?

A .cso kiterjesztésű fájl tömörített ISO-képfájl. A CSO a DAX tömörítési módszer alternatívája; más néven CISO; ez volt az első módszer az [ISO](/hu/compression/iso/) fájlok tömörítésére, és általában ez a preferált módszer a PlayStation Portable anyagok archiválására. Ez a formátum Deflate tömörítést használ, amely legfeljebb kilenc tömörítési réteget tartalmazhat. A képek létrehozásához olyan szoftvereket használnak, mint a Prometheus és a YACC.

## CSO fájlformátum

A CSO fájlformátum volt az első tömörítési módszer az ISO számára, hogy több memóriaterületet takarítson meg. A jobb tömörítés érdekében időről időre a fejlesztéseket elvégezték. A CSO kilenc szintű előre beállított Deflate tömörítést használ, általában mindegyik szint külön-külön 2 KiB blokkot tud kezelni. Míg a legmagasabb szintű tömörítés lelassíthatja és meghosszabbíthatja a betöltési időt a szoftverekben, ami nagymértékben függ a lemez adatfolyamától, az alacsonyabb szintek is jelentős tömörítést végezhetnek.

### CSO fájlszerkezet

A CSO fájlformátum egy 24 bájtos fejlécet, adatblokkokat és egy indextáblát tartalmaz. Little-endian egy bájtnál nagyobb mezők esetén feltételezhető. A PlayStation Portable architektúrája az alábbiakban látható.

#### Fejléc

| Eltolás (byte) | Név | Méret (byte) | Cél |
----------|----------|--------------|---------|
| 0x0 | Varázslat | 4 | Mindig CISO vagy 0x4F534943 32 bites egész számként olvasva. Ez a mező a CSO-fájlok azonosítására szolgál. Vegye figyelembe, hogy ez a mező a CSO többi származékánál eltérő lehet, például a ZSO a ZISO varázskódot használta. |
| 0x4 | Fejléc mérete | 4 | Az eredeti CSO „v1” fájlformátum esetében ezt a mezőt figyelmen kívül hagyja, ezért nem szükséges pontosnak lennie. A "v2" és a ZSO formátum azonban megköveteli, hogy a mező mindig 0x18 (24 bájt) legyen. |
| 0x8 | Tömörítetlen méret | 8 | Az eredeti tömörítetlen ISO mérete bájtban. |
| 0x10 | Blokkméret | 4 | Az egyes adatblokkok mérete bájtban a tömörítés előtt. Általában 2048 bájt, megegyezik az egyes ISO 9660 szektorok méretével. |
| 0x14 | Verzió | 1 | A használt fájlformátum verziója. A "v1" formátum esetén az érték 0 vagy 1 lehet. A "v2" formátum esetén ennek 2-nek kell lennie. Ezenkívül a ZSO formátum megköveteli, hogy ez 1 legyen.
| 0x15 | Index igazítás | 1 | Az egyes indexbejegyzések igazítása, bitben megadva. |
| 0x16 | Fenntartva | 2 | Ez a mező nem használt. A „v1” formátumban ez a mező figyelmen kívül marad, és tetszőleges értékeket tartalmazhat. „v2” formátumban ennek a mezőnek nullának kell lennie. |

#### Index táblázat

Az indextábla több 4 bájtos bejegyzést tartalmaz, amelyek az egyes adatblokkok pozícióját jelzik, és egy további, utolsó bejegyzést, amely a fájl végére mutat.
Az egyes bejegyzések tartalma a következő:
| Bit | Hossz | Maszk | Név | Cél |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFFF | Pozíció | Ez a mező a fejlécben megadott indexigazítás által balra tolva azt a pozíciót adja meg, ahol az adatblokk kezdődik. |
| 31 | 1 | 0x80000000 | Tömörítés típusa | A ZSO formátumnak hasonló a szemantikája, csak a 0 az LZ4-et jelenti a Deflate helyett. "v2" formátumban. A blokk implicit módon tömörítetlennek minősül, ha a blokk mérete egyenlő vagy nagyobb, mint a fájl fejlécében megadott blokkméret. |

#### Adatblokkok

Az adatblokkok tömörítetlen vagy tömörített adatokból állnak. Egy blokk méretét úgy számítjuk ki, hogy megkapjuk a pozícióját, majd kivonjuk a következő blokk pozíciójából. Ha az index igazítása nagyobb, mint nulla, akkor valószínű, hogy a blokk mérete nagyobb, mint a benne lévő adatok.


## Hivatkozások

* [CSO – a Wikipédia](https://en.wikipedia.org/wiki/.CSO)


