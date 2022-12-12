{
  "date" : "2019-10-11",
  "keywords" :[ "qlr fájl", "qlr fájlformátum", "mi az a qlr fájl", "fájl", "qlr példa", "qlr fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS rétegdefiníciós fájl",
  "description":"További információ a QLR fájlformátumról és az API-król, amelyek QLR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Mi az a QLR fájl?

A .qlr fájl egy rétegdefiníciós fájl, amely a réteg adatforrására mutató mutatót tartalmaz. Ez kiegészíti a réteg [QGIS](https://www.qgis.org/en/site/) stílusinformációit. Mivel az összes kapcsolódó stílusra hivatkozik, ez a fájl egyetlen forrásként szolgál a stílusinformációk megszerzéséhez használt adatok számára. A QLR fájlok használatával az adatforrásokhoz tartozó információk ebbe az egyetlen fájlba helyezhetők, amelyet más alkalmazások is elolvashatnak a stílusinformációk betöltéséhez. A QLR-fájlok bármely szövegszerkesztővel megnyithatók, például a Notepad++-val.

## QLR fájlformátum

A QLR, hasonlóan a [QGS]-hez (/hu/gis/qgs/), egy XML-fájl, amely XML-címkék formájában tartalmaz mutatókat a rétegbeli adatforrásra. Hasonló az ArcGIS .lyr fájlhoz. A QML-fájlok legfelső szintű címkéi az alábbi képen láthatók.

{{< figure src="../qlr.png" title="" >}}

## Hivatkozások

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

