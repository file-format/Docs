{
  "date" : "2021-04-21",
  "keywords" :[ "Erbsendatei", "Erbsendateiformat", "Was ist eine Erbsendatei", "Datei", "Erbsenbeispiel", "Erbsendateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - PeaZip-Archivdateiformat",
  "description":"Erfahren Sie mehr über das PEA-Dateiformat und APIs, die PEA-Dateien erstellen und öffnen können.",
  "linktitle" :"ERBSE",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Was ist eine PEA-Datei?

Eine Datei mit der Erweiterung .pea, Akronym für Pack, Encrypt, and Authenticate, ist ein [zip](/de/compression/zip/)-Archiv, das mit der Archivierungssoftwareanwendung [PeaZip](https://peazip.github.io/) erstellt wurde. Es verfügt über Komprimierung und Ausgabe mehrerer Volumes und bietet ein flexibles Sicherheitsmodell durch authentifizierte Verschlüsselung und Kryptografie. Dies bietet sowohl Datenschutz als auch Authentifizierung der Daten. Das PeaZip-Dienstprogramm ist als Open-Source-Engine verfügbar, die je nach Bedarf für verschiedene Betriebssysteme kompiliert werden kann.

## PEA-Dateiformat

Die [PEA-Dateiformatspezifikationen](https://peazip.github.io/pea_help.pdf) sind öffentlich als Referenz für Entwickler verfügbar. PEA-Archive sind Binärdateien mit flexiblem Sicherheitsmodell und redundanten Integritätsprüfungen, die von Prüfsummen bis hin zu kryptografisch starken Hashes reichen. Dies definiert drei verschiedene Ebenen der zu steuernden Kommunikation:

* Streams – der eigentliche Ausgabedatenstrom, der aus mehreren Eingabedateien besteht und auf mehrere Ausgabedatenträger geschrieben werden kann
* Objekte - Eingabedateien und Ordner, die an das .pea-Archiv gesendet werden
* Volumes - Ausgabearchivdatei, die auf eine benutzerdefinierte Größe ausgedehnt werden kann

Jedes davon ist optional und kann gemäß den Benutzeranforderungen integriert werden. Das PEA-Dateiformat kann einen einzelnen Stream mit unbegrenzt vielen Objekten speichern. Jeder Stream ist bis zu 2^64 Byte groß.

PEA-Dateien bieten optionale Integritätsprüfung und authentifizierte Verschlüsselung mit AES im EAX- oder HMAC-Modus, alternativ Twofish und Serpent im EAX-Modus.

### PEA-Archiv-Header

Der Archiv-Header ist 10 Bytes groß und wie folgt aufgebaut.

|Bytes|Beschreibung|
---|---|
|1 | Magic-Byte-Feld zur Disambiguierung des Dateiformats: $EA|
|1 | Versionsnummer|
|1 | Revisionsnummer|
|1 | Schema der Lautstärkeregelung|
|1 | Deklarieren des Betriebssystems, in dem der Stream erstellt wurde|
|1 | Datums- und Zeitcodierung des Betriebssystems deklarieren|
|1 | Zeichenkodierung für Objektnamen deklarieren|
|1 | CPU-Typ (in 7 Bit kodiert) und Endianness (in msb) deklarieren|
|1 | Reserviert für zukünftige Verwendung|

## Verweise

* [PEA-Dateiformatspezifikationen](https://peazip.github.io/pea_help.pdf)
* [PEA-Dateiformat](https://peazip.github.io/pea-file-format.html#.pea_specifications)

