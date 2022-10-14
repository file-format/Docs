{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "pdb-Datei", "pdb", "Erweiterung", "Format", "Was ist eine pdb-Datei", "pdb-Dateiformat", "PDB-Metadaten" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDB-Dateiformat - Eine Programmdatenbankdatei",
  "description":"Erfahren Sie mehr über das PDB-Dateiformat und APIs, die PDB-Dateien erstellen und öffnen können.",
  "linktitle" :"PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine PDB-Datei?

Eine Datei mit der Erweiterung .pdb ist eine Programmdatenbankdatei, die Debugging-Informationen für eine kompilierte ausführbare Datei (EXE/DLL) enthält. PDB-Dateien werden von Microsoft-Compilern generiert, wenn ein Anwendungsprogramm im Debugmodus kompiliert wird. Das Vorhandensein einer PDB-Datei kann beim Reverse Engineering einer ausführbaren Datei hilfreich sein, da sie wichtige Informationen zu allen Symbolen der Module enthält. Aus diesem Grund werden diese Dateien von der endgültigen ausführbaren Datei getrennt aufbewahrt. Die [DgbHelp-API] von Microsoft (https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) kann eine PDB-Datei öffnen, um Informationen wie öffentliche und Exporte, globale Symbole, lokale Symbole, Typdaten, Quelldateien und Zeilennummern.

## PDB-Dateiformat

PDB ist das proprietäre Dateiformat von Microsoft und wurde noch nirgendwo offiziell dokumentiert. Eine Startdokumentation ist jedoch [hier](https://github.com/Microsoft/microsoft-pdb) verfügbar und kann referenziert werden.

### PDB-Streams

PDB-Dateien bestehen aus mehreren Streams, wobei jeder Stream als virtuelle Einzeldatei fungiert und Informationen enthält. PDB-Dateischreiber können in diese Dateien schreiben, und die Datei wird erst fertiggestellt, nachdem ein explizites Commit ausgegeben wurde. Ein Compiler kann weiterhin in eine PDB-Datei schreiben, aber nur dann festschreiben, wenn der gesamte Benutzercode erfolgreich kompiliert wurde. Eine PDB-Datei besteht aus folgenden Streams:

|Stream Nr. |Inhalt |Kurzbeschreibung|
---|---|---|
|1| Pdb (Header) |Versionsinformationen und Informationen zum Verbinden dieser PDB mit der EXE|
|2| Tpi (Type Manager) |Alle Typen, die in der ausführbaren Datei verwendet werden.|
|3| Dbi (Debug-Informationen) |Enthält Abschnittsbeiträge und eine Liste von 'Mods'|
|4| NameMap| Enthält eine Hash-String-Tabelle|
|4-(n+4)| n Mod's (Modulinformationen)| Jeder Mod-Stream enthält Symbole und Zeilennummern für eine Zusammenstellung|
|n+4| Globaler Symbol-Hash| Ein Index, der die Suche in globalen Symbolen nach Namen erlaubt|
|n+5| Öffentliches Symbol hash| Ein Index, der die Suche in öffentlichen Symbolen nach Adressen ermöglicht|
|n+6| Symbolaufzeichnungen| Tatsächliche Symbolaufzeichnungen globaler und öffentlicher Symbole|
|n+7| Geben Sie Hash| ein Vom TPI-Stream verwendeter Hash.|

Jeder Stream in einer PDB-Datei besteht aus mehreren Seiten, die nicht zwingend fortlaufend nummeriert sind.

### PDB-Header

Eine PDB-Datei enthält einen Header, der aus einer Signatur zum Identifizieren und Validieren des spezifischen Formats besteht. Die Länge der Signatur hängt vom PDB-Format ab. Die Kopfzeile kann länger als eine einzelne Seite sein.

### PDB-Metadaten
Die PDB-Metadaten sind dafür verantwortlich, alle Komponentenstreams zu erkennen, indem sie die Länge und Seitenfolge für jeden Stream angeben. Aufträge werden nacheinander an Streams erteilt; beginnend mit 0. Es gibt auch einen ungeordneten Root-Stream, der einige der Metadaten enthält.

## Verweise
* [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft-PDB](https://github.com/Microsoft/microsoft-pdb)

