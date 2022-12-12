{
  "date" : "2019-10-11",
  "keywords" :[ "qml fájl", "qml fájlformátum", "mi az a qml fájl", "fájl", "qml példa", "qml fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML – A QGIS stílusfájlformátum",
  "description":"További információ a QML fájlformátumról és az API-król, amelyek QML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Mi az a QML fájl?

A .qml kiterjesztésű fájl egy XML-fájl, amely a QGIS-rétegekhez tartozó rétegstílusinformációkat tárolja. A QGIS egy nyílt forráskódú, többplatformos térinformatikai alkalmazás, amely térinformatikai adatok megjelenítésére szolgál, és képes az adatokat rétegekbe rendezni. A QML-fájlok olyan információkat tartalmaznak, amelyeket a QGIS használ a jellemzők geometriájának megjelenítésére, beleértve a szimbólumdefiníciókat, a méreteket és az elforgatásokat, a címkézést, az átlátszatlanságot, a keverési módot és még sok mást. A QLR fájloktól eltérően a QML fájlok tartalmazzák az összes stílusinformációt. A QML-fájlok bármely szövegszerkesztőben megnyithatók, például a Notepad++-ban.

## QML fájl formátum

A QLR, hasonlóan a [QGS](/hu/gis/qgs/) és a [QLR](/hu/gis/qlr/) fájlokhoz, egy XML-fájl, amely a rétegek stílusinformációit tartalmazza.

Az alábbi ábra egy QML-fájl legfelső szintű címkéit mutatja (csak a renderer_v2-vel és a szimbólumcímkével kibontva).

{{< figure src="../qml.png" title="" >}}

## Hivatkozások

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

