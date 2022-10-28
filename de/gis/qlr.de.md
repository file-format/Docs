{
  "date" : "2019-10-11",
  "keywords" :[ "qlr-Datei", "qlr-Dateiformat", "was ist eine qlr-Datei", "Datei", "qlr-Beispiel", "qlr-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - QGIS Layer-Definitionsdatei",
  "description":"Erfahren Sie mehr über das QLR-Dateiformat und APIs, die QLR-Dateien erstellen und öffnen können.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Was ist eine QLR-Datei?

Eine Datei mit .qlr ist eine Layer-Definitionsdatei, die einen Zeiger auf die Layer-Datenquelle enthält. Dies ist zusätzlich zu den Stilinformationen [QGIS](https://www.qgis.org/en/site/) für die Ebene. Diese Datei enthält Verweise auf alle verwandten Stile und wird als einzige Quelle für Daten verwendet, die zum Abrufen der Stilinformationen verwendet werden. Unter Verwendung der QLR-Dateien können Informationen zu den Datenquellen in diese einzelne Datei gestellt werden, die von anderen Anwendungen gelesen werden kann, um die Gestaltungsinformationen zu laden. QLR-Dateien können mit jedem Texteditor wie Notepad++ geöffnet werden.

## QLR-Dateiformat

QLR, ähnlich wie [QGS](/de/gis/qgs/), ist eine XML-Datei, die Zeiger auf Layer-Datenquellen in Form von XML-Tags enthält. Sie ähnelt der ArcGIS .lyr-Datei. Die Tags der obersten Ebene einer QML-Datei sind wie in der Abbildung unten dargestellt.

{{< figure src="../qlr.png" title="" >}}

## Verweise

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

