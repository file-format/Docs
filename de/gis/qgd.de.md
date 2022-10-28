{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Sqlite-Datenbank des QGIS-Projekts", "Erweiterung", "Format", "QGIS", "Hilfsdatenbank", "Was ist eine QGD-Datei"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Sqlite-Datenbank des QGIS-Projekts",
  "description":"Erfahren Sie mehr über QGD, eine SQLite-Datenbank des QGIS-Projekts und APIs, die QGD-Dateien erstellen und öffnen können.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Was ist eine QGD-Datei?

Die Datei mit der Erweiterung .QGD-Datei ist eigentlich die zugehörige SQLite-Datenbank des **QGIS**-Projekts, die die Hilfsdaten für das Projekt enthält. Die QGD-Datei bleibt leer, wenn keine Hilfsdaten für das Projekt vorhanden sind.

## Details zum QGD-Dateiformat

Im klassischen Modus wird die Hilfsdatenbank als Datei mit der Erweiterung .qgd zusammen mit der XML-Datei gespeichert. Das System **Hilfsdatenbank** ermöglicht alternativ das Lesen und Schreiben von Daten im System. Beim Erstellen des QGZ, bei dem es sich um einen gezippten Container handelt, wird die .qgd-Datei in die .qgz eingefügt.

## Was ist eine Hilfsdatenbank?
Die Hilfsdatenbank ist eigentlich ein Standby-DB-System, das als Reaktion auf die Duplizierung der Zieldatenbank erstellt wird. Die Hilfsdatenbank ist eigentlich ein Fall einer doppelten Datenbank, die die Datenbank wäre, in die Sie duplizieren. Wenn Sie beispielsweise eine Standby-Datenbank mit doppelter Datenbank einrichten, ist die Quelldatenbank das Ziel und die Standby-Datenbank wird als Hilfsdatenbank bezeichnet.


## Verweise

* [QGZ – Ein neues Standard-Projektdateiformat für QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [QGIS-Dateiformate](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

