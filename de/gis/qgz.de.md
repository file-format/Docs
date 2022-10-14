{
  "date" : "2021-03-18",
  "keywords" :[ "qgz-Datei", "qgz-Dateiformat", "was ist eine qgz-Datei", "Datei", "qgz-Beispiel", "qgz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Komprimiertes Quanten-GIS-Projekt",
  "description":"Erfahren Sie mehr über das QGZ-Dateiformat, das nur ein komprimiertes QGS und APIs ist, die QGZ-Dateien erstellen und öffnen können.",
  "linktitle" :"QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Was ist eine QGZ-Datei?

Das **QGZ**-Dateiformat ist ein komprimiertes Archiv, das eine [QGS](https://docs.fileformat.com/gis/qgs/)-Datei und eine QGD-Datei enthält. Während die QGD-Datei die SQLite-Datenbank des qgis-Projekts ist, die aus Hilfsdaten für das Projekt besteht. Wenn keine Hilfsdaten vorhanden sind, bleibt die QGD-Datei leer.

## Details zum QGZ-Dateiformat

Das QGZ wurde als neue Variante des **QGIS 3-Projektdateiformats** eingeführt. Dieses Format ist ein gezippter Container für die QGS-XML-Datei. Wenn Benutzer QGD wählen, das ein optionales Format ist, ist der Container in diesem Fall vorteilhaft, um die Hilfsspeicherdatenbank zu speichern.

Im klassischen Modus wird die Hilfsdatenbank als Datei mit der Erweiterung .qgd zusammen mit der XML-Datei gespeichert. Bei der Auswahl des gezippten Containers schließt die .qgd-Datei in die .qgz-Datei ein. Dies erleichtert den Benutzern nur das Problem, die Benutzer können sie nicht löschen oder vergessen, sie zu kopieren, wenn sie Projektdateien freigeben!


## Verweise

* [QGZ – Ein neues Standard-Projektdateiformat für QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS-Dateiformate](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

