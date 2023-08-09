{
  "date" : "2021-08-24",
  "keywords" :[ "wdb-Datei", "wdb-Dateiformat", "was ist eine wdb-Datei", "Datei", "wdb-Beispiel", "wdb-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das WDB-Dateiformat und APIs, die WDB-Dateien erstellen und öffnen können.",
  "title" :"WDB - SQL Server-Ablaufverfolgungsdatei",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Was ist eine WDB-Datei?
Eine Datei mit der Erweiterung .wdb ist eigentlich eine von Microsoft Works erstellte Datenbankdatei, die verwendet wurde, um Funktionen wie ein Datenbankverwaltungssystem auszuführen. Die WDB-Datei ähnelt der Access-Datenbankdatei ([MDB](/de/database/mdb/)), ist jedoch weniger effizient und hat größere Einschränkungen. Die WDB-Dateien können nicht mit Microsoft Access geöffnet werden. Sie können die WDB-Datei jedoch in Microsoft Works öffnen und sie dann in eine MDB-Datei exportieren, um eine WDB-Datei in MS Access zu öffnen.

## WDB-Dateiformat
Die Microsoft Works-Datenbank ist das native Datenbankformat der Office-Suite Microsoft Works. Aufgrund der proprietären Natur des Formats und einiger Einschränkungen. Die WDB-Dateien können in keiner anderen Software als Microsoft Works geöffnet werden. Im Dateiformat befindet sich vor jedem der ASCII-Textstrings ein wiederkehrender 10-Byte-Header, der die Werte der Felder darstellt, die mit einem NULL-Wert abgeschlossen wurden. Der Header beginnt im Allgemeinen mit einem **\x0f** Byte und NULL, gefolgt von 4 Datenbytes abwechselnd mit NULLen.

### Dateistruktur

Die Struktur der WDB-Datei ist unten angegeben:
- **1. Header**: vom Anfang der Datei, endend mit \x25\x00\xf2 und 244 NULL-Bytes
- **2. Header**: beginnt mit \xffT - dh \xff\x54 und erstreckt sich über 4096 Bytes, enthält Spalten-/Feldnamen und andere Dinge und scheint bei Byteposition 6144 zu beginnen.
- **Feld**: Wert hat einen 10-Byte-Header mit folgendem Format: {Typ Byte} {Typ Byte, Teil 2} {Datenbyte 1} \x00 {db 2} \x00 {db 3} {db 3 , Teil 2} {db 4} \x00. Datenbyte 2 ist die Feldnummer, Datenbyte 3 ist die Datensatznummer (addiert Datenbyte 3, Teil 2, wenn es über 256 Datensätze geht).


## Verweise ##

* [Benutzer:JesseW/wdb-Format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

