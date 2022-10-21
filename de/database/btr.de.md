{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extension", "file", "file format", "Database File Type", "Database File Format", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das BTR-Dateiformat und APIs, die BTR-Dateien erstellen und öffnen können.",
  "title" :"BTR - Btrieve-Datenbankdatei",
  "linktitle" :"BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Was ist eine BTR-Datei?

Eine Datei mit der Erweiterung .btr ist eine Datenbankdatei, die von der transaktionalen Datenbankanwendung [Btrieve](https://www.actian.com/) erstellt wurde. Im Gegensatz zu relationalen Datenbankverwaltungssystemen (RBMS) basiert Btrieve auf der Indexed Sequential Access Method (ISAM), einer Möglichkeit, Daten für einen schnellen Abruf zu speichern. Die BTR-Datei speichert eine Sammlung von Datensätzen und wird verwendet, um Berichte gemäß den Anforderungen zu erstellen. BTR-Dateien können mit Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility und Legend Software BTRIEVE Viewer geöffnet werden.

## BTR-Dateistruktur - Weitere Informationen

Die interne Datenstruktur und Ausrichtung jedes Bytes in der Struktur einer BTR-Datei ist nicht öffentlich verfügbar. Allerdings Btrieve
stellt die [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) bereit, die verwendet werden kann, um die Informationen aus BTR-Dateien zu lesen. Es ist mit den folgenden Programmiersprachen und Entwicklungsumgebungen kompatibel.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU-C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Das Abrufen von Daten aus einer BTR-Datei ist von der zugehörigen DDF-Datei abhängig. Ohne das DDF ist es nicht einfach, die Informationen aus einer solchen Datei abzurufen.

## Verweise

* [Btrieve – Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Einführung in Btreive-APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

