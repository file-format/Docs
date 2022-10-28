{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DDL-Dateiformat und APIs, die DDL-Dateien erstellen und öffnen können.",
  "title" :"DDL-Dateiformat - Eine Datendefinitionssprachdatei",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Was ist eine DDL-Datei?

Eine Datei mit der Erweiterung .ddl ist eine Data Definition Language-Datei, die verwendet wird, um das Schema einer Datenbank zu definieren. Es enthält Anweisungen/Befehle zum Arbeiten mit Datenbankstrukturen wie Tabellen, Spalten, Datensätzen und anderen Feldern. Befehle in einer DDL-Datei sind in [SQL](/de/database/sql/) geschrieben und können Vorgänge wie das Erstellen einer Tabelle in der Datenbank, Löschen und Aktualisieren ausführen. Ein Datenbankschema gehört dem erstellten Schema und alle CRUD-Vorgänge können darauf ausgeführt werden. Beliebte Anwendungen, die DDL-Dateien erstellen und öffnen können, sind Windows Texteditor, Jetbrains Intellij Idea und EclipseLink.

## DDL-Befehle

Eine einzelne DDL-Datei kann mehrere Befehle enthalten, die aufgrund der korrekten Syntax nacheinander ausgeführt werden und Änderungen am Schema vornehmen, z. B. Zeichensätze und Tabellen erstellen, Tabellen löschen, Tabellen umbenennen und ändern. Die folgenden DDL-Befehle werden häufig beim Arbeiten mit Datenbankschemata verwendet.

`CREATE` - Wird verwendet, um die Datenbank oder ihre Objekte (wie Tabelle, Index, Funktion, Ansichten, Speicherprozedur und Trigger) zu erstellen.

`DROP` – Wird verwendet, um Objekte aus der Datenbank zu löschen.

„ALTER“ – Wird verwendet, um die Struktur der Datenbank zu ändern.

„TRUNCATE“ – Wird verwendet, um alle Datensätze aus einer Tabelle zu entfernen, einschließlich aller für die Datensätze zugewiesenen Leerzeichen.

„KOMMENTAR“ – Fügt Kommentare zum Datenwörterbuch hinzu.

`RENAME` – Benennt ein bestehendes Objekt in der Datenbank um.

## DDL-Beispiel

Das folgende Beispiel zeigt eine DDL-Anweisung für den CREATE-Befehl, der eine Tabelle erstellt und ihre Felder definiert.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Verweise ##

* [DDL von Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

