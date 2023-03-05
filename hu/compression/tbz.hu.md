{
  "date" : "2019-10-11",
  "keywords" :[ "tbz fájl", "tbz fájl formátum", "mi az a tbz fájl", "fájl", "tbz példa", "tbz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip tömörített tar archívum",
  "description":"További információ a TBZ fájlformátumról és az API-król, amelyek TBZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Mi az a TBZ fájl?

A .tbz kiterjesztésű fájl olyan tömörített archívum, amely BZIP-tömörítést használ a tartalomfájlok méretének csökkentésére. A TBZ fájlok valójában UNIX [TAR](/hu/compression/tar/) archivált fájlok, amelyeket ezután BZIP-pel tömörítenek. A legutóbbi második szintű tömörítés a [BZIP2](/hu/compression/bz2/), amely a BZIP-et váltotta fel. A TBZ fájlformátum alkalmas nagy fájlok átvitelére. A TBZ fájlok megnyithatók/kibonthatók olyan szoftveralkalmazásokkal, mint a 7-Zip, PeaZip és jZip. A Linux és a macOS felhasználók terminálablakból is megnyithatnak egy TBZ-t a BZIP2 paranccsal.

## TBZ fájlformátum

A TBZ-fájlok valójában BZIP/[BZIP2](/hu/compression/bz2) tömörítéssel létrehozott tömörített archívumok. Ehhez a fájlformátumhoz nem állnak rendelkezésre hivatalos előírások. Egy nem hivatalos [reverse engineered specifikáció](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) azonban azt mutatja, hogy a .bz2 adatfolyam egy 4 bájtos fejlécből áll, amelyet követnek nulla vagy több tömörített blokk által.

## Referenciák ##

* [A BZIP2 formátum specifikációi](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

