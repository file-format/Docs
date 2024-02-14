{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR-Datei – dBASE-Strukturlistenobjektdatei – Was ist eine .str-Datei und wie öffnet man sie?",
  "description" : "Erfahren Sie mehr über die STR dBASE-Strukturlistenobjektdatei und wie Sie sie öffnen.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Was ist eine STR-Datei?

Das STR-Dateiformat wird häufig mit dBASE, einem Datenbankverwaltungssystem, in Verbindung gebracht. In dBASE stellt eine .str-Datei normalerweise eine Strukturlistenobjektdatei dar. Diese Datei enthält die Struktur einer Datenbanktabelle, einschließlich Informationen zu Feldern (Spalten) und ihren Eigenschaften.

Die Strukturlistenobjektdatei (.str) enthält Metadaten wie Feldnamen, Datentypen, Feldlängen und alle anderen Eigenschaften, die jedem Feld in der Datenbanktabelle zugeordnet sind. Es wird verwendet, um die Struktur einer Datenbanktabelle zu definieren, ohne tatsächliche Datensätze zu enthalten.

Programme wie dBASE oder andere Datenbankverwaltungstools können diese Datei nutzen, um das Layout der Datenbanktabelle zu verstehen und Vorgänge wie Abfragen, Aktualisierungen oder das Erstellen neuer Datensätze basierend auf dieser Struktur auszuführen.

Hier ist ein einfaches Beispiel dafür, was eine STR-Datei enthalten könnte:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Dieses Beispiel beschreibt eine Tabelle mit vier Feldern: ID, Name, Alter und Geburtsdatum, zusammen mit ihren jeweiligen Datentypen und Längen.

## Wie öffne ich eine STR-Datei?

Die primäre Möglichkeit zum Öffnen von .str-Dateien ist die Verwendung von dBASE selbst, insbesondere auf Windows-Betriebssystemen. dBASE ist in der Lage, den Inhalt dieser Dateien zu lesen und zu interpretieren, sodass Benutzer die Datenbankstruktur anzeigen und damit arbeiten können.

Da es sich bei .str-Dateien im Wesentlichen um reine Textdateien handelt, die Informationen über die Struktur der Datenbank enthalten, können Sie sie auch mit einem Texteditor öffnen. Beispiele für Texteditoren sind Microsoft Notepad unter Windows und Apple TextEdit auf dem Mac. Beim Öffnen in einem Texteditor können Sie den Inhalt der Datei, einschließlich Feldnamen, Datentypen und anderen Strukturinformationen, in einem für Menschen lesbaren Format sehen.

## Verweise
* [dBase](https://en.wikipedia.org/wiki/DBase)


