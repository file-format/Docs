{
  "date" : "2022-01-23",
  "keywords" :[ "xz fájl", "fájl formátum", "mi az xz fájl", "fájl", "xz példa", "xz fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ fájl - XZ tömörített archívum",
  "description":"További információ az XZ fájlformátumról és az API-król, amelyek XZ fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Mi az XZ fájl?

Az XZ egy tömörített fájlformátum, amely az LZMA2 tömörítési algoritmust használja. Úgy tervezték, hogy helyettesítse a népszerű gzip és bzip2 formátumokat, és számos előnnyel rendelkezik ezekkel a régebbi szabványokkal szemben. Az XZ fájlok számos platformon jól támogatottak, és gyorsan és egyszerűen kicsomagolhatók. Bár nem olyan gyakoriak, mint a [ZIP](/hu/compression/zip/) vagy [RAR](/hu/compression/rar/) fájlok, az XZ archívumok nagy mennyiségű adat tárolására használhatók a tömörítés minőségének feláldozása nélkül. Ha nagy fájlokat kell tömöríteni vagy ki kell tömöríteni, érdemes megfontolni az XZ fájlkiterjesztést.

## XZ fájlformátum

Az XZ fájlokat generálja és bináris fájlként menti a lemezre. Az LZMA algoritmust használja az adatok tömörítésére, és akár 50%-os tömörítési arányt is elérhet. Az XZ fájlokat általában szoftverterjesztéshez és biztonsági mentési archívumokhoz használják. Kicsomagolhatók az XZ segédprogrammal, amely a legtöbb Linux disztribúcióban megtalálható.

## Csomagolja ki az XZ fájlokat Linux/Unix rendszeren

Az XZ fájlok kicsomagolásához először telepítse az "xz-utils" csomagot:
```
$ sudo apt-get install xz-utils
```

Használja az "unxz" parancsot az .xz fájlok kibontásához:
```
$ unxz compressed_xz_file.xz
```

vagy használja az XZ --decompress opciójával:
```
$ xz --decompress compressed_xz_file.xz
```

## Hivatkozások

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

