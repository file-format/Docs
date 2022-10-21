{
  "date" : "2019-10-11",
  "keywords" :[ "rar-Datei", "rar-Dateiformat", "was ist eine rar-Datei", "Datei", "rar-Beispiel", "rar-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Was ist eine RAR-Dateierweiterung und APIs, die RAR-Dateien erstellen und öffnen können.",
  "linktitle" :"RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine RAR-Datei?

Dateien mit der Erweiterung .rar sind Archivdateien, die zum Speichern von Informationen in komprimierter oder normaler Form erstellt werden. RAR steht für Roshal ARchive-Dateiformat und ist ein proprietäres Dateiformat, das 1995 von Eugene Roshal, einem russischen Softwareingenieur, entwickelt wurde. Das Format wird verwendet, um Dateien mit verschiedenen Methoden zu archivieren, einschließlich verschiedener Komprimierungstechniken. Es gibt verschiedene Anwendungssoftware für Windows, Linux und MacOS zum Extrahieren von RAR-Dateien. Die WinRAR-Software von RARLab ist das Shareware-Dateiarchivierungsprogramm (kostenlos für 40 Tage) für die Microsoft Windows-Plattform; die Software wurde vom selben Autor, Eugene Roshal, auf Linux portiert (nur als Extraktor).

## Versionsgeschichte des RAR-Dateiformats

* v1.3 (Original, hat keine "Rar!"-Signatur)
* v1.5
* v2.0 - veröffentlicht mit WinRAR 2.0 und Rar für MS-DOS 2.0
* v2.9 - veröffentlicht in WinRAR-Version 3.00
* v5.0 - unterstützt von WinRAR 5.0 und höher

## Hauptmerkmale des RAR-Formats

RAR ist schon seit geraumer Zeit im Einsatz und eines der beliebtesten Dateiformate für die Archivierung. Hauptmerkmale des RAR-Formats sind:

**`Hohe Komprimierungsrate:`** Überlegen im Vergleich zu [ZIP](/de/compression/zip/), vergleichbar mit 7z- und Zipx-Format.

**`Strong File Encryption by Design:`** Verschlüsselte RAR4-Archive basieren auf AES-128-basierter Verschlüsselung, während verschlüsselte RAR5-Archive auf AES-256-Verschlüsselung mit verbesserter Schlüsselplanung basieren

**`Erweiterte Fehlerkorrektur- und Datenwiederherstellungsfunktionen:`** optionale Wiederherstellungsaufzeichnungen während der Archiverstellung

**`Dateigröße:`** Mindestens 20 Bytes und maximal 2^63 Bytes groß (8 Exabyte Gesamtgröße des Archivs)

**`Mehrbändige RAR-Archive:`** Möglichkeit, große Archive in mehrere kleinere Dateien aufzuteilen, um die Übertragung über das Netzwerk zu erleichtern. In diesem Fall werden die Dateierweiterungen um 1 erhöht, um geteilte Volumes darzustellen

## RAR-Dateiformat

Vollständige Spezifikationen des RAR-Formats sind nicht öffentlich verfügbar, weshalb Details zum Format nicht prägnant formuliert werden können.

### Allgemeines Archiv-Layout

Das allgemeine Layout eines in Version 5.0 eingeführten RAR-Dateiformats sieht wie folgt aus:

|Dateiformat
---|
|Selbstextrahierendes Modul (optional)
|RAR 5.0-Signatur
|Verschlüsselungs-Header archivieren (optional)
|Kopfzeile des Hauptarchivs
|Header des Kommentardienstes archivieren (optional)
Dateikopf 1
|Dienst-Header (NTFS-ACL, Streams usw.) für vorangehende Datei (optional)
|...
|Dateikopf N
|Dienst-Header (NTFS-ACL, Streams usw.) für vorangehende Datei (optional)
|Wiederherstellungsaufzeichnung (optional)
|Ende des Archivheaders

Informationen zu jedem Abschnitt der oben erwähnten RAR-Datei finden Sie im Dokument [Spezifikationen des RAR 5.0-Dateiformats] (https://www.rarlab.com/technote.htm#arcstruct).

#### Selbstextrahierende RAR-Archive

Wenn die RAR-Datei selbst selbstextrahierend ist, sind die selbstextrahierenden Informationen am Anfang der Datei vor der Archivsignatur enthalten. Größe und Inhalt sind nicht definiert.

#### RAR 5.0-Signatur

Die RAR-Signatur ist ein 8-Byte-Header, der aus der folgenden magischen Zahl besteht:

0x 52 61 72 21 1A 07 00

wo

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Verweise

* [RAR 5.0 Archivformat](https://www.rarlab.com/technote.htm)
* [RAR - Von Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

