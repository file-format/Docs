{
  "date" : "2019-10-11",
  "keywords" :[ "b6z fájl", "b6z fájlformátum", "mi az a b6z fájl", "fájl", "b6z példa", "b6z fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"B6Z - B6ZIP archív fájlformátum",
  "description":"További információ a B6Z fájlformátumról és az API-król, amelyek B6Z fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "B6Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## Mi az a B6Z fájl?

A .b6z kiterjesztésű fájl egy tömörített archív fájl, amelyet macOS szoftveralkalmazás [B6Zip](http://b6zip.com) hozott létre, amely a fájlok tömörítésére és kibontására szolgál. Ez egy viszonylag új archív formátum, amely nagyobb tömörítési arányt tesz lehetővé. A B6Z nyitott architektúrájú, és támogatja a 900 000 PB-ig terjedő fájlméretet. Támogatja az adattömörítést, a hibajavítást és a fájlok átívelését. A B6Zip segédszoftver ingyenesen elérhető MacOS rendszeren különböző típusú tömörített fájlok megnyitásához, beleértve a B6Z fájlt is.

## B6Z fájlformátum

A B6Z fájlformátum nyílt architektúrán alapul, és szilárd tömörítést biztosít az AES-256 titkosítási algoritmussal. Alapértelmezett tömörítési módszerként az LZMA2-t használja, de más tömörítési módszereket is támogat az alábbiak szerint.

|Módszer|Leírás|
---|---|
|LZMA |Az LZ77 algoritmus optimalizált változata|
|LZMA2| Az LZMA továbbfejlesztett változata|
|Leereszteni| Szokásos LZ77 algoritmus|
|BZip2| Szabványos BWT algoritmus|
|PPMD| Dmitrij Skarin PPMdH|

A B6Zip segédprogram támogatja ezeket a tömörítési szabványokat, és rendkívül optimalizált, ami nagy sebességet eredményez. Támogatja a [ZIP](/hu/compression/zip/), [TAR](/hu/compression/tar/) és [RAR](/hu/compression/rar/) fájlformátumokkal való munkát. A B6Z fájlok MIME típusú application/x-b6z tömörítésűek.

## Hivatkozások

* [B6Zip](http://b6zip.com)

