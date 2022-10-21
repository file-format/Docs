{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDB-Dateiformat - ESRI File Geodatabase-Datei",
  "description":"Erfahren Sie mehr über das GDB-Dateiformat und APIs, die GDB-Dateien erstellen und öffnen können.",
  "linktitle" :"GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Was ist eine GDB-Datei?

ESRI File Geodatabase (FileGDB) ist eine Sammlung von Dateien in einem Ordner auf einer Disc, die zugehörige Geodaten wie Feature-Datasets, Feature-Classes und zugehörige Tabellen enthalten. Es erfordert, dass bestimmte andere Dateien neben der .gdb-Datei im selben Verzeichnis aufbewahrt werden, damit es funktioniert. Abfragen können auf der .gdb-Datei ausgeführt werden, um sowohl räumliche als auch nicht-räumliche Daten zu verwalten.

## GDB-Dateiformat – Weitere Informationen

File-Geodatabases bestehen aus sieben Systemtabellen plus Benutzerdaten. Benutzerdaten können in den folgenden Arten von Datensätzen gespeichert werden:

* Feature-Klasse
* Feature-Datensatz
* Mosaik-Datensatz
* Rasterkatalog
* Rasterdatensatz
* Schematischer Datensatz
* Tabelle (nicht räumlich)
* Werkzeugkästen

Feature-Datasets können Feature-Classes sowie die folgenden Arten von Datasets enthalten:

* Anhänge
* Feature-bezogene Anmerkung
* Geometrische Netzwerke
* Netzwerkdatensätze
* Paketstoffe
* Beziehungsklassen
* Gelände
* Topologien

Die standardmäßige maximale Größe von Datasets in File-Geodatabases beträgt 1 TB. Die maximale Größe kann für große Datasets (normalerweise Raster) auf 256 TB erhöht werden. Dies wird durch ein Konfigurationsschlüsselwort gesteuert. Weitere Informationen finden Sie unter Konfigurationsschlüsselwörter für File-Geodatabases.

File-Geodatabases können auch Subtypes und Domänen enthalten und an der Checkout/Check-in-Replikation und unidirektionalen Replikationen teilnehmen.

Auf eine File-Geodatabase kann gleichzeitig von mehreren Benutzern zugegriffen werden. Wenn die Benutzer bearbeiten, müssen sie verschiedene Datensätze bearbeiten.

## Spezifikationen des GDB-Dateiformats ##

File GDB ist ein proprietäres Format von ESRI und seine Spezifikationen sind nicht öffentlich verfügbar. Aus diesem Grund konnten die Dateiformatdetails für FIle GDB nirgendwo anders dokumentiert werden als einige Quellen, die dies [teilweise] (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) durch Reverse Engineering getan haben .

## Verweise ##

* [FGDB-Spezifikationen](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

