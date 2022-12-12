{
  "date" : "2019-10-11",
  "keywords" :[ "bz2 fájl", "bz2 fájlformátum", "mi az a bz2 fájl", "fájl", "bz2 példa", "bz2 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - Tömörített fájlformátum",
  "description":"Tanulja meg, hogy mi az a BZ2 fájl és API-k, amelyek BZ2 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Mi az a BZ2 fájl?

A BZ2 tömörített fájlok, amelyeket a [BZIP2](http://www.bzip.org/) nyílt forráskódú tömörítési módszerrel hoztak létre, többnyire UNIX vagy Linux rendszeren. Egyetlen fájl tömörítésére szolgál, és nem több fájl archiválására szolgál. Ez ellentétben áll a TAR fájlformátummal ugyanazokon a platformokon, amelyek több fájlt egyetlen fájlba archiválnak, de tömörítés nélkül. A BZ2-ként tömörített fájlok kitömöríthetők olyan alkalmazásokkal, mint a [WinZip](https://www.winzip.com/win/en/). A BZIP2 Run-Length Encoding (RLE) vagy [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) tömörítési algoritmust használ a magas szintű tömörítés eléréséhez.

## BZ2 fájlformátum

Ehhez a fájlformátumhoz nem állnak rendelkezésre hivatalos előírások. Egy nem hivatalos [reverse engineered specifikáció] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) azonban azt mutatja, hogy a .bz2 adatfolyam egy 4 bájtos fejlécből áll, amelyet követnek nulla vagy több tömörített blokk által. Ezt közvetlenül követi egy folyamvégi jelző, amely 32 bites CRC-t tartalmaz a feldolgozott sima szöveges teljes adatfolyamhoz. A tömörített blokkok között nincs párnázás, és az összes blokk bitre van igazítva.

## Csomagolja ki/bontsa ki a BZ2 fájlt

A BZ2 fájlt Windows és Mac OS rendszeren olyan szoftverek segítségével csomagolhatja ki, mint a WinZip. Linuxon a következő parancs a terminálban.

```
bzip2 -d filename.bz2
```

## Hivatkozások

* [A BZIP2 formátum specifikációi](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

