{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MDB-Dateiformat und APIs, die MDB-Dateien erstellen und öffnen können.",
  "title" :"MDB-Dateiformat - Eine Microsoft Access-Datenbankdatei",
  "linktitle" :"MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Was ist eine MDB-Datei?

Eine Datei mit der Erweiterung .mdb ist eine Microsoft Access-Datenbankdatei, die ein relationales Datenbankverwaltungssystem (RDBMS) ist. Es speichert Daten in Datenbanktabellen, die über Primär- und Fremdschlüssel miteinander verknüpft sind. Die MDB-Datei enthält die vollständige Struktur der Datenbanktabellen, Abfragen und gespeicherten Prozeduren. MDB ist das Standarddateiformat für Microsoft Access 2003. Die lateralen Versionen von Microsoft Access verwenden die Dateiformate [ACCDB](/de/database/accdb/), das bisher neueste Dateiformat. MDB-Dateien können mit Anwendungen wie Microsoft Access, MDB Viewer, MDBOpener geöffnet und in ACCDB-, [CSV](/de/spreadsheet/csv/), Excel-Formate usw. konvertiert werden.

## MDB-Dateiformat

Für das MDB-Format sind öffentliche Spezifikationen verfügbar, und es bleibt das proprietäre Dateiformat von Microsoft. Microsoft bietet jedoch Konnektivitätszugriff auf die MDB-Datei mithilfe des Standards Open Database Connectivity (ODBC) und Visual Basic for Applications (VBA). Der inoffizielle MDB-Leitfaden bietet eine kurze informelle Beschreibung des MDB-Formats auf der Grundlage des Reverse Engineering und kann konsultiert werden, um mehr über die Spezifikationen zu erfahren.

### Seiten

Gemäß dem inoffiziellen MDB-Leitfaden besteht eine MDB-Datei aus Seiten mit fester Größe (2048 Bytes für Jeb DB3 und 4096 Bytes für Jet DB 4). Das erste Byte gibt den Seitentyp an. Im Folgenden sind die wichtigsten Seitentypen aufgeführt:

„Erste Seite“: Sie enthält Datenbank-Header-Informationen, die auch die Identifizierung der Jet DB-Version enthalten, mit der die Datei kompatibel ist. Darüber hinaus enthält es auch Dateisicherheitsinformationen und eine Karte der Seitennutzung.

`Tabellendefinitionsseite`: Eine Tabellendefinitionsseite spezifiziert Spalten, Datentypen, Index und andere Informationen. Es verwendet bei Bedarf zusätzliche Seiten und enthält eine Seitenzuordnung, die die Zeilendaten für diese Tabelle enthält.

„Datenseiten“: Die Datenseiten sind die eigentlichen Datencontainer, in denen Daten zeilenweise gespeichert werden. Es verwendet untergeordnete Seiten, um lange Datenwerte zu speichern.

Eine einzelne Microsoft Access-Datenbank kann aus mehreren Dateien bestehen, die es ermöglichen, Datei- und Tabellengrößenbeschränkungen zu überschreiten. Dies erleichtert das Ablegen von Formularen und Code in einer Front-End-MDB-Datei auf dem Desktop des Benutzers und von Daten in einer anderen Back-End-MDB-Datei auf Servern, die mit dem Netzwerk verbunden sind.

## Verweise ##

* [Zugriffsspezifikationen](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Der inoffizielle MDB-Leitfaden](http://jabakobob.net/mdb/)

