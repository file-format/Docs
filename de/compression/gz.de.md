{
  "date" : "2019-10-11",
  "keywords" :[ "gz-Datei", "gz-Dateiformat", "was ist eine gz-Datei", "Datei", "gz-Beispiel", "gz-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ-Dateiformat - GNU-Zip-Archivdatei",
  "description":"Erfahren Sie, was eine GZ-Datei und APIs sind, die GZ-Dateien erstellen und öffnen können.",
  "linktitle" :"GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GZ-Datei?

Eine GZ-Datei ist ein komprimiertes Archiv, das mit dem standardmäßigen Komprimierungsalgorithmus [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) erstellt wird. Es kann mehrere komprimierte Dateien, Verzeichnisse und Datei-Stubs enthalten. Dieses Format wurde ursprünglich entwickelt, um Komprimierungsformate auf UNIX-Systemen zu ersetzen. und ist immer noch einer der häufigsten Archivtypen auf Linux-Systemen. Anwendungen wie [WinZip](https://www.winzip.com/en/) können GZ-Dateien öffnen, um ihren Inhalt sowohl unter Windows als auch unter MacOS anzuzeigen.

## GZ-Dateiformat - Weitere Informationen

Gzip verwendet den [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE)-Algorithmus zur Komprimierung von Archiven und unterscheidet sich vom [ZIP](/de/compression/zip/)-Archivformat durch die Anwendung des Komprimierungsalgorithmus auf das vollständige Archiv statt einzelner Dateien. Die von der Internet Engineering Task Force (IETF) veröffentlichte GZIP-Dateiformatspezifikation Version 4.3 enthält detaillierte Informationen zum Dateiformat. Das Dateiformat besteht aus:

* Dateikopf
* Optionale Header
* Komprimierte Daten
* Datei-Fußzeile

## Header der GZ-Datei ##

Der Header der GZ-Datei besteht aus 10 Bytes wie folgt:

|Offset|Größe|Wert|Beschreibung
---|---|---|---|
|0|2|0x1f 0x8b|Magische Nummer zur Identifizierung des Dateityps
|2|1| |Kompressionsmethode * 0-7 (Reserviert) * 8 (Entleeren)
|3|1| |Datei-Flags
|4|4| |32-Bit-Zeitstempel
|8|1| |Komprimierungs-Flags
|9|1| |Betriebssystem-ID

### Datei-Flags ###

|Wert|Bezeichner|Beschreibung
---|---|---|
|0x01|FTEXT|Wenn gesetzt, müssen die unkomprimierten Daten als Text statt als Binärdaten behandelt werden. Dieses Flag weist auf die Konvertierung am Zeilenende für plattformübergreifende Textdateien hin, erzwingt sie jedoch nicht.
|0x02|FHRCC|Die Datei enthält eine Header-Prüfsumme (CRC-16)
|0x04|FEXTRA|Die Datei enthält zusätzliche Felder
|0x08|FNAME|Die Datei enthält einen ursprünglichen Dateinamen-String
|0x10|FCOMMENT|Die Datei enthält einen Kommentar
|0x20| |Reserviert
|0x40| |Reserviert
|0x80| |Reserviert

### Betriebssystem ###

|Wert|Beschreibung
---|---|
|0|FAT-Dateisystem (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (oder OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari-Nutzungsbedingungen
|6|HPFS-Dateisystem (OS/2, NT)
|7|Macintosh
|8|Z-System
|9|CP/M
|10|TOPS-20
|11|NTFS-Dateisystem (NT)
|12|QDOS
|13|Eichel RISCOS
|255|unbekannt

## Optionale GZ-Header ##

Die optionalen zusätzlichen Header sind diejenigen, die durch die Datei-Flags gekennzeichnet sind, und enthalten Informationen wie den ursprünglichen Dateinamen, zusätzliche Felder, Kommentare und Header-Prüfsumme.

## Komprimierte Daten ##

Dieser Abschnitt enthält die komprimierten Daten unter Verwendung des DEFLATE-Komprimierungsalgorithmus.

## Fußzeile der GZ-Datei ##

Der Dateifuß ist 8 Bytes groß und enthält folgende Informationen.

|Offset|Größe|Beschreibung
---|---|---|
|0|4|Prüfsumme (CRC-32)
|4|4|Unkomprimierter Datengrößenwert in Byte

## Verweise ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP-Dateiformatspezifikation](http://tools.ietf.org/html/rfc1952), von IETF.

