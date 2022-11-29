{
  "date" : "2019-10-11",
  "keywords" :[ "qml-fil", "qml-filformat", "vad är en qml-fil", "fil", "qml-exempel", "qml-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QML - QGIS Style File Format",
  "description":"Läs mer om QML-filformat och API:er som kan skapa och öppna QML-filer.",
  "linktitle" : "QML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Vad är en QML fil?

En fil med .qml-extesion är en XML-fil som lagrar lagerstilsinformation för QGIS-lager. QGIS är en plattformsoberoende GIS-applikation med öppen källkod som används för att visa geospatial data med förmågan att organisera data i form av lager. QML-filer innehåller information som används av QGIS för att återge funktionsgeometrier inklusive symboldefinitioner, storlekar och rotationer, märkning, opacitet, blandningsläge och mycket mer. Till skillnad från QLR-filerna innehåller QML-filer all stylinginformation i sig. QML-filer kan öppnas i vilken textredigerare som helst som Notepad++.

## QML filformat

QLR, liknande [QGS](/sv/gis/qgs/) och [QLR](/sv/gis/qlr/), är en XML-fil som innehåller stilinformation för lagren.

Bilden nedan visar toppnivåtaggarna för en QML-fil (med endast renderer_v2 och dess symboltagg expanderad).

{{< figure src="../qml.png" title="" >}}

## Referenser

* [QGIS](https://www.qgis.org/en/site/)
* [QML](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

