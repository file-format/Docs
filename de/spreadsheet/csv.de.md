{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "Datei", "Erweiterung", "Dateiformat", "Comma Separated Values", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das CSV-Dateiformat und APIs, die CSV-Dateien erstellen und öffnen können.",
  "title" :"CSV-Dateiformat",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine CSV-Datei?

Dateien mit der Erweiterung .csv (Comma Separated Values) stellen einfache Textdateien dar, die Datensätze mit kommagetrennten Werten enthalten. Jede Zeile in einer CSV-Datei ist ein neuer Datensatz aus der Gruppe von Datensätzen, die in der Datei enthalten sind. Solche Dateien werden erzeugt, wenn eine Datenübertragung von einem Speichersystem zu einem anderen beabsichtigt ist. Da alle Anwendungen durch Komma getrennte Datensätze erkennen können, erfolgt der Import solcher Datendateien in die Datenbank sehr bequem. Fast alle Tabellenkalkulationsanwendungen wie Microsoft Excel oder OpenOffice Calc können CSV ohne großen Aufwand importieren. Aus solchen Dateien importierte Daten werden in Zellen einer Tabellenkalkulation zur Darstellung für den Benutzer angeordnet.

## Kurze Geschichte ##

Im Folgenden finden Sie einige kurze Fakten über den Ursprung und die Geschichte des CSV-Dateiformats.

* 1972 - Der Compiler IBM Fortran (Level H erweitert) unterstützte sie unter OS/360

* 1978 - Listengesteuerte Eingabe/Ausgabe wurde von FORTRAN 77 unterstützt, das Kommas und Leerzeichen als Trennzeichen verwendete

* 2005 - CSV wurde mit [RFC4180](https://tools.ietf.org/html/rfc4180) als MIME-Inhaltstyp standardisiert.

* 2013 - Die Mängel von RFC4180 wurden durch eine W3C-Empfehlung behoben

* 2015 - W3C hat die ersten Empfehlungen für CSV-Metadatenstandards erstellt, die im Dezember 2015 als Empfehlung begannen

## CSV-Dateien konvertieren ##

CSV-Dateien können mit den Anwendungen, die diese Dateien öffnen können, in verschiedene Dateiformate konvertiert werden. Beispielsweise kann Microsoft Excel Daten aus dem CSV-Dateiformat importieren und in XLS, [XLSX](/de/spreadsheet/xlsx/), [PDF](/de/pdf/), [TXT](/de/word-processing/txt/) speichern. , XML und [HTML](/de/web/html/) Dateiformate. Ebenso bieten andere Desktop- und Online-Dienste die Möglichkeit, CSV-Dateien in HTML, ODS und [RTF](/de/word-processing/rtf/) zu exportieren.

## CSV-Dateiformat ##

Das CSV-Dateiformat ist bekanntermaßen unter [RFC4180](https://tools.ietf.org/html/rfc4180) spezifiziert. Es definiert jede Datei als CSV-konform, wenn:

* Jeder Datensatz befindet sich in einer separaten Zeile, die durch einen Zeilenumbruch (CRLF) getrennt ist. Zum Beispiel:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* Der letzte Datensatz in der Datei kann einen Zeilenumbruch am Ende haben oder auch nicht. Zum Beispiel:
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx
* Es kann eine optionale Kopfzeile geben, die als erste Zeile der Datei mit dem gleichen Format wie normale Datensatzzeilen erscheint. Dieser Header enthält Namen, die den Feldern in der Datei entsprechen, und sollte die gleiche Anzahl von Feldern enthalten wie die Datensätze im Rest der Datei (das Vorhandensein oder Fehlen der Header-Zeile sollte über den optionalen Parameter "header" dieser Datei angegeben werden Mime Typ). Zum Beispiel:
* Feldname,Feldname,Feldname CRLF
* aaa, bbb, ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿In der Kopfzeile und jedem Datensatz können ein oder mehrere Felder vorhanden sein, die durch Kommas getrennt sind. Jede Zeile sollte in der gesamten Datei die gleiche Anzahl von Feldern enthalten. Leerzeichen werden als Teil eines Feldes betrachtet und sollten nicht ignoriert werden. Dem letzten Feld im Datensatz darf kein Komma folgen. Zum Beispiel:
* aaa,bbb,ccc
* Jedes Feld kann in doppelte Anführungszeichen gesetzt werden oder nicht (einige Programme, wie z. B. Microsoft Excel, verwenden jedoch überhaupt keine doppelten Anführungszeichen). Wenn Felder nicht in doppelte Anführungszeichen eingeschlossen sind, dürfen innerhalb der Felder keine doppelten Anführungszeichen erscheinen. Zum Beispiel:\
* „aaa“, „bbb“, „ccc“ CRLF
* zzz,yyy,xxx
* Felder mit Zeilenumbrüchen (CRLF), doppelten Anführungszeichen und Kommas sollten in doppelte Anführungszeichen gesetzt werden. Zum Beispiel:
* "aaa","bCRLF
* bb","ccc"CRLF
* zzz,yyy,xxx
* Wenn doppelte Anführungszeichen verwendet werden, um Felder einzuschließen, muss ein doppeltes Anführungszeichen, das innerhalb eines Felds erscheint, durch ein vorangestelltes doppeltes Anführungszeichen maskiert werden. Zum Beispiel:
* "aaa","b""bb","ccc"

Angesichts der modernen Verwendung ist das Trennzeichen jedoch nicht nur auf Komma beschränkt und kann auch Semikolon, Tabulator oder Leerzeichen sein. Anwendungen wie Microsoft Excel bieten die Möglichkeit, das Trennzeichen zum Importieren von Datensätzen aus einer CSV-Datei anzugeben.

## Verweise

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

