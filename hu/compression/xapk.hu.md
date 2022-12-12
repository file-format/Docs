{
  "date" : "2021-04-11",
  "keywords" :[ "xapk fájl", "xapk fájlformátum", "mi az xapk fájl", "fájl", "xapk példa", "xapk fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - Meta csomagfájl formátum",
  "description":"További információ az XAPK fájlformátumról és az API-król, amelyek XAPK fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## Mi az XAPK fájl?

Az .xapk kiterjesztésű fájl egy tömörített csomagfájl, amely Android-alkalmazások mobileszközökre történő telepítésére szolgál. Ez egy tárolófájl formátum, amely magában foglalja az APK-t és a telepítéshez szükséges további kapcsolódó fájlokat. A másik társított fájl egy OBB-fájl, amely további fájlokat, például grafikákat, médiafájlokat és alkalmazásadatokat tárol, amelyek az alkalmazás futtatásához szükségesek. Az XAPK-fájlokat a Google Play nem támogatja, és kizárólag harmadik féltől származó Android-alkalmazás-letöltő webhelyeken terjesztik őket. Ezek az XAPK Installer segítségével telepíthetők Android-eszközre.

## XAPK fájlformátum

Az XAPK fájlok a szabványos [ZIP](/hu/compression/zip/) fájlformátum használatával vannak tömörítve. Ezeket szabványos tömörítő/kicsomagoló szoftverrel, például WinZIP-pel lehet kibontani. Miután az XAPK fájlt kicsomagolta a lemezre, a következő fájlokat tartalmazza a mappában.

* APK - Szabványos telepítőfájl az alkalmazás Android-eszközökre történő telepítéséhez
* OBB – További fájl, amely releváns erőforrásfájlokat tartalmaz

## Hivatkozások

* [Android-csomagfájl](https://en.wikipedia.org/wiki/Android_application_package)

