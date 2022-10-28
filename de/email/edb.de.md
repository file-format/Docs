{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EDB-Dateiformat - Eine Exchange Mail-Datenbankdatei",
  "description":"Erfahren Sie mehr über das EDB-Dateiformat und APIs, die EDB-Dateien erstellen und öffnen können.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Was ist eine EDB-Datei?

Eine Datei mit der Dateierweiterung .edb ist eine von Microsoft Exchange Server erstellte Postfachdatenbank zum Speichern von E-Mail-bezogenen Daten. EDB, Exchange Database, speichert In-Process-Nachrichten und Nicht-SMTP-Nachrichten. EDB sind auch als ESE-Datenbankdateien (Extensible Storage Engine) bekannt und speichern Dateien mit einer B-Tree-Struktur. Als Speicherdateien können EDB-Dateien in andere E-Mail-Speicherdateiformate wie [PST](/de/email/pst/) und [OST](/de/email/ost/) konvertiert werden.

## EDB-Dateiformat

Es sind keine offiziellen/offenen EDB-Dateiformatspezifikationen verfügbar, auf die verwiesen werden kann. Beim Reverse Engineering des Dateiformats wurden einige Fortschritte erzielt, was zu einer teilweisen Dekodierung der Spezifikationen führte. Danach besteht eine EDB-Datei aus:
* Datei-Header - Enthält Header-Informationen der Datenbankdatei
* Seiten mit fester Größe - Enthält die Datenbank, die aus Tabellen und Indizes besteht

### Header der Datenbankdatei
Der Header der Datenbankdatei befindet sich auf der ersten Datenbankseite und ist mindestens 668 Byte groß. Der Dateiheader enthält neben anderen Feldern „Dateiformatversion“ und „Dateityp“.

#### Datentypen
|Typ|Beschreibung
---|---|
|0| Datenbank|
|1| Streamen|

`Hinweis:` Bezeichner für diese Typen sind nicht bekannt.

#### Version des Dateiformats
Das ursprüngliche Format von EDB begann im April 1997 und wurde danach ständig weiterentwickelt.

|Revisionsdatum|Version|Revision|Beschreibung
---|---|---|---|
|April 1997| 0x00000620|0x00000000| Beta-Format des ursprünglichen Betriebssystems.|
|Mai 1997 |0x00000620|0x00000001| Fügen Sie im Katalog Spalten für die bedingte Indizierung und OLD.| hinzu
|Juni 1997|0x00000620|0x00000002|Fügt das fLocalizedText-Flag in IDB hinzu.|
|Okt 1997|0x00000620|0x00000003|SPLIT_BUFFER zu Space-Tree-Stammseiten hinzufügen.|
|Jan 1998|0x00000620|0x00000002|Überarbeitung zurücksetzen, damit ESE97 aufwärtskompatibel bleibt.|
||0x00000620|0x00000003|Fügt dem Katalog neue getaggte Spalten hinzu ("CallbackData" und "CallbackDependencies").|
|Mai 1998|0x00000620|0x00000004|Unterstützung für Super Long Value (SLV): signSLV, fSLVExists in dbheader.|
|Mai 1998|0x00000620|0x00000005|Neuer SLV-Weltraumbaum.|
|Okt 1998|0x00000620|0x00000006|SLV-Weltraumkarte.|
|Dezember 1998|0x00000620|0x00000007|4-Byte-IDXSEG.|
|Jan 1999|0x00000620|0x00000008|Neues Vorlagenspaltenformat.|
|Juni 1999|0x00000620|0x00000009|Sortierte Vorlagenspalten. Verwendet in Windows XP SP3|
||0x00000620|0x0000000b|Enthält den Seitenkopf mit der in Exchange verwendeten ECC-Prüfsumme|
||0x00000620|0x0000000c|Verwendet in Windows Vista (SP0)|
||0x00000620|0x00000011|Unterstützung für 2-KiB-, 16-KiB- und 32-KiB-Seiten.Erweiterter Seitenkopf mit zusätzlichen ECC-Prüfsummen.Spaltenkomprimierung.Leerzeichen.Verwendet in Windows 7 (SP0)|
|Mai 1999|0x00000623|0x00000000|Neuer Raummanager.|

### Datenbankdateien

Die EDB-Datenbankdatei enthält das Schema für alle Tabellen in der Datenbank. Darüber hinaus enthält es auch Datensätze für alle Datenbanktabellen und Indizes für die Tabellen. Seine Position wird durch die folgenden Kennungen bestimmt.

* JetCreateDatenbank
* JetCreateDatabase2
* JetAttachDatenbank
* JetAttachDatabase2

Anhand dieser kann der Zustand der Datenbank wie folgt beurteilt werden.

|Wert|Bezeichner|Beschreibung
---|---|---|
|1|JET_dbstateJustCreated|Die Datenbank wurde gerade erstellt.|
|2|JET_dbstateDirtyShutdown|Die Datenbank erfordert eine Hard- oder Soft-Recovery, um verwendet oder verschiebbar zu werden. Man sollte nicht versuchen, Datenbanken in diesem Zustand zu verschieben.|
|3|JET_dbstateCleanShutdown|Die Datenbank befindet sich in einem sauberen Zustand. Die Datenbank kann ohne Protokolldateien angehängt werden.|
|4|JET_dbstateBeingConverted|Die Datenbank wird aktualisiert.|
|5|JET_dbstateForceDetachInternal|Dieser Wert wurde in WindowsXP eingeführt|
 

## Verweise
* [Extensible Storage Engine (ESE) Database File (EDB) Specifications](https://github.com/libyal/libesedb/tree/master/documentation)

