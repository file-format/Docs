{
  "date" : "2019-10-11",
  "keywords" :[ "qgs fájl", "qgs fájlformátum", "mi az a qgs fájl", "fájl", "qgs példa", "qgs fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - QGIS projektfájl formátum",
  "description":"További információ a QGS fájlformátumról és az API-król, amelyek QGS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a QGS fájl?

A .qgs kiterjesztésű fájl a [QGIS] (https://www.qgis.org/en/site/) segítségével létrehozott projektfájl, amely egy nyílt forráskódú, többplatformos GIS-alkalmazás. Az összes projektbeállítás, például a fóliatulajdonságok és a projekt segédadatai. Akkor jön létre, amikor egy térképprojektet lemezre mentünk. Ez valójában egy konfigurációs fájl, amely olyan információkat tárol, mint a GIS adatokra mutató mutatók, a fóliák stílusinformációi és a projekt címe. A QGS fájlok a QGIS szoftverrel nyithatók meg, amely ingyenesen letölthető.

## QGS fájlformátum

A QGS-fájlok [XML](/hu/web/xml/) formátumúak, és XML-címkeként tárolják a projektadatokat. A QGS fájl olyan információkat tartalmaz, mint:

* projekt címe
* CRS projekt
* a rétegfa
* pattintó beállítások
* kapcsolatok
* a térkép vászon kiterjedése
* projekt modellek
* legenda
* Térképnézet dokkok (2D és 3D)
* A rétegek az alapul szolgáló adatkészletekre (adatforrásokra) és más rétegtulajdonságokra mutató hivatkozásokkal, beleértve a kiterjedést, az SRS-t, az összekapcsolásokat, a stílusokat, a megjelenítőt, a keverési módot, az átlátszatlanságot és még sok mást.
* projekt tulajdonságai

### QGS felső szintű XML címkék

{{< figure src="../qgstoplevel.png" title="" >}}

### Kiterjesztett felső szintű projektréteg címkék

{{< figure src="../qgstoplevel.png" title="" >}}

## Hivatkozások

* [QGIS](https://www.qgis.org/en/site/)

