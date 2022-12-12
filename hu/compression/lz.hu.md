{
  "date" : "2021-04-08",
  "keywords" :[ "lz fájl", "lz fájlformátum", "mi az lz fájl", "fájl", "lz példa", "lz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip tömörített fájlformátum",
  "description":"További információ az LZ fájlformátumról és az LZ-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Mi az LZ fájl?

Az .lz kiterjesztésű fájl egy tömörített archív fájl, amelyet az Lzip programmal hoztak létre, amely egy ingyenes parancssori eszköz a tömörítéshez. Támogatja az összefűzést a támogató fájlok tömörítéséhez. Az LZ-fájlok médiatípusa application/lzip, és nagyobb tömörítési arányt támogatnak, mint a [BZ2](/hu/compression/bz2). Az LZ az LZMA (Lempel-Ziv-Markov lánc) algoritmuson alapul, és egy 32 bites CRC ellenőrző összeget és azonosító bájtokat tartalmaz a fájl integritásának ellenőrzésére.

## LZMA tömörített formátum

Az LZMA tömörített formátum egy tömörített bitfolyamból áll, amelyet adaptív bináris tartománykódolóval kódolnak. A folyam csomagokra van osztva. Minden csomag egy bájtot vagy egy LZ77 sorozatot ír le. Az egyes csomagok hossza és távolsága implicit vagy explicit módon kódolt.

A hét csomagtípus a következő ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Csomagolt kód (bitsorozat) |Csomagnév |Csomag leírása|
---|---|---|
|0 + byteCode| LIT| Egyetlen bájt, amely adaptív bináris tartománykódolóval van kódolva.|
|1+0 + len + dist| MATCH| Egy tipikus LZ77 sorozat, amely leírja a sorozat hosszát és távolságát.|
|1+1+0+0| SHORTREP| Egy bájtos LZ77 sorozat. A távolság megegyezik az utoljára használt LZ77 távolsággal.|
|1+1+0+1 + len| LONGREP[0]| LZ77 sorozat. A távolság megegyezik az utoljára használt LZ77 távolsággal.|
|1+1+1+0 + len| LONGREP[1]| LZ77 sorozat. A távolság megegyezik a második legutoljára használt LZ77 távolsággal.|
|1+1+1+1+0 + len| LONGREP[2]| LZ77 sorozat. A távolság egyenlő a harmadik utoljára használt LZ77 távolsággal.|
|1+1+1+1+1 + len| LONGREP[3]| LZ77 sorozat. A távolság megegyezik a negyedik utoljára használt LZ77 távolsággal.|


## Hivatkozások

* [LZMA – Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

