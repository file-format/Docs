{
  "date" : "2019-12-09",
  "keywords" :[ "zl fájl", "zl fájl formátum", "mi az a zl fájl", "fájl", "zl példa", "zl fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP tömörített fájlformátum",
  "description":"További információ a ZL fájlformátumról és az API-król, amelyek ZL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Mi az a ZL fájl?

A .zl kiterjesztésű fájl egy ZLIP tömörített fájlformátum, amely a DEFLATE tömörítési algoritmus egy változatát használja a fájlok tömörítésére. Független a CPU típusától, az operációs rendszertől, a fájlrendszertől és a karakterkészlettől, ezért használható információcserére. A ZLIP-tömörítés műszaki specifikációi az [IETF webhelyen](https://tools.ietf.org/html/rfc1950) érhetők el, és a fejlesztők szemszögéből is hivatkozhatnak rájuk.

## ZL fájl formátum

A zlib adatfolyam a következő szerkezettel rendelkezik:

* `CMF (tömörítési módszer és zászlók) - Ez a bájt a tömörítési módszertől függően 4 bites tömörítési módszerre és 4 bites információs mezőre van felosztva.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (tömörítési módszer)` - A fájlban használt tömörítési módszert azonosítja. Értékei és a megfelelő tömörítési módszer a következők.

| CM Value| Tömörítés|
|---|---|
|CM = 8|DEFLATE 32K-ig terjedő ablakmérettel
|CM = 15|Fenntartva|

* `CINFO (Tömörítési információ)` - CM = 8 esetén a CINFO az LZ77 ablakméretének 2-es bázis logaritmusa, mínusz nyolc (a CINFO=7 32K-os ablakméretet jelöl).

* "FLG (FLaGs)" - Ez a jelző bájt a következőképpen oszlik meg:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referenciák ##

* [A Zlib fájlformátum specifikációi](https://tools.ietf.org/html/rfc1950)

