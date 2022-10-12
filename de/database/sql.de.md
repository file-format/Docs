{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das SQL-Dateiformat und APIs, die SQL-Dateien erstellen und öffnen können.",
  "title" :"SQL-Dateiformat - Eine strukturierte Abfragesprachen-Datendatei",
  "linktitle" :"SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Was ist eine SQL-Datei?

Eine Datei mit der Erweiterung .sql ist eine SQL-Datei (Structured Query Language), die Code für die Arbeit mit relationalen Datenbanken enthält. Es wird verwendet, um SQL-Anweisungen für CRUD-Operationen (Create, Read, Update, and Delete) auf Datenbanken zu schreiben. SQL-Dateien sind bei der Arbeit mit Desktop- und webbasierten Datenbanken üblich. Es gibt mehrere Alternativen zu SQL wie Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL und einige andere. SQL-Dateien können mit Abfrage-Editoren von Microsoft SQL Server, MySQL und anderen einfachen Texteditoren wie Notepad unter Windows OS geöffnet werden.

## Kurze Geschichte

* Anfang der 1970er Jahre von Donal D. Chamberlin und Raymond F. Boyce bei IBM entwickelt und eingeführt
* Wird zum Speichern und Abrufen von Daten aus dem ursprünglichen quasi-relationalen Datenbankverwaltungssystem von IBM, System R, verwendet
* Beginnend mit der Verwendung in kommerziellen Produkten basierend auf ihrem System R-Prototyp, einschließlich System/38, SQL/DS und DB2, die 1979, 1981 bzw. 1983 im Handel erhältlich waren.
* 1986 offiziell von ANSI- und ISO-Standardgruppen als Standard "Datenbanksprache SQL" für relationale Datenbankverwaltungssysteme (RDBMS) übernommen

## SQL-Dateiformat

SQL-Dateien sind im Klartextformat und können aus mehreren Sprachelementen bestehen. Mehrere Anweisungen können einer einzigen SQL-Datei hinzugefügt werden, wenn ihre Ausführung ohne Abhängigkeit möglich ist. Diese SQL-Befehle können von Abfrageeditoren zum Ausführen von CRUD-Operationen ausgeführt werden.

### Elemente der SQL-Sprache

Die SQL-Sprachelemente sind unten aufgeführt.

|Element|Beschreibung|
---|---|
|Klauseln| Bestandteile von Anweisungen und Abfragen.|
|Ausdrücke| Kann entweder skalare Werte oder Tabellen erzeugen, die aus Spalten und Zeilen von Daten bestehen|
|Prädikate| Geben Sie Bedingungen an, die zu dreiwertiger SQL-Logik (3VL) (wahr/falsch/unbekannt) oder booleschen Wahrheitswerten ausgewertet werden können und verwendet werden, um die Auswirkungen von Anweisungen und Abfragen zu begrenzen oder den Programmablauf zu ändern.|
|Abfragen| Rufen Sie die Daten nach bestimmten Kriterien ab. Dies ist ein wichtiges Element von SQL.|
|Aussagen| Kann dauerhafte Auswirkungen auf Schemata und Daten haben oder Transaktionen, Programmablauf, Verbindungen, Sitzungen oder Diagnosen steuern.|

### SQL-Beispiel
Die folgende SQL-Anweisung erstellt eine Tabelle namens **DATA**, gefolgt von zusätzlichen `INSERT`-Befehlen, um Datensätze in diese Tabelle einzufügen.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Verweise ##

* [SQL von Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [SQL-Syntax](https://en.wikipedia.org/wiki/SQL_syntax)

